<!-- ... existing code ... -->
    .status-pill.pending {
      background: #fef3c7;
      color: #92400e;
      border-color: #ebd082;
    }

    .status-pill.inactive {
      background: var(--danger-bg);
      color: var(--danger-text);
      border-color: #e5a9a9;
    }

    .online-badge {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      background: rgba(255, 255, 255, 0.14);
      border: 1px solid rgba(255, 255, 255, 0.28);
      color: #ffffff;
      border-radius: 999px;
      padding: 4px 10px;
      font-size: 0.78rem;
      font-weight: 700;
      margin-bottom: 8px;
    }

    .online-dot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: #4ade80;
      display: inline-block;
    }

    .online-dot.fallback {
      background: #facc15;
    }

    .disabled-section-box {
<!-- ... existing code ... -->
          <div class="brand-text">
            <div class="online-badge" id="onlineSyncStatusBadge">
              <span class="online-dot" id="onlineSyncDot"></span>
              <span id="onlineSyncText">در حال اتصال آنلاین به سامانه ابری...</span>
            </div>
            <h1>دفتر رهنمای معاملات شکرالله ابراهیم خیل — ستاره اعتماد</h1>
            <p>سامانه رسمی آنلاین املاک و معاملات | ثبت ملکیت، جستجوی عمومی، تبلیغات و مدیریت یکپارچه</p>
          </div>
        </div>
<!-- ... existing code ... -->
      const STORAGE_KEYS = {
        PROPERTIES: 'paghman_trust_properties_v1',
        ADS: 'paghman_trust_ads_v1',
        CREDS: 'paghman_trust_creds_v1',
        LOGO: 'paghman_trust_logo_v1',
        PHONES: 'paghman_trust_phones_v1',
        SECTIONS: 'paghman_trust_sections_v1'
      };

      const CLOUD_CONFIG = {
        storage: 'FIREBASE',
        collections: {
          PROPERTIES: 'paghman_properties',
          ADS: 'paghman_ads',
          CREDS: 'paghman_creds',
          LOGO: 'paghman_logo',
          PHONES: 'paghman_phones',
          SECTIONS: 'paghman_sections'
        }
      };
<!-- ... existing code ... -->
      const state = {
        activeSection: 'home',
        activeAdminTab: 'props',
        isAdminLoggedIn: false,
        cloudEnabled: false,
        cloudConnected: false,
        cloudUser: null,
        cloudAppId: 'default-app-id',
        properties: [],
        ads: [],
        phones: OFFICE_PHONES.slice(),
        sectionAccess: cloneObj(DEFAULT_SECTION_ACCESS),
        creds: cloneObj(DEFAULT_CREDS),
        logo: cloneObj(DEFAULT_LOGO),
        draftPropImg: '',
        draftDeedImg: ''
      };

      function updateCloudBadge(text, isOnlineMode) {
        const textEl = document.getElementById('onlineSyncText');
        const dotEl = document.getElementById('onlineSyncDot');
        if (textEl) textEl.textContent = text;
        if (dotEl) {
          if (isOnlineMode) {
            dotEl.classList.remove('fallback');
          } else {
            dotEl.classList.add('fallback');
          }
        }
      }

      async function initFirebaseCloudSync() {
        try {
          if (
            typeof window.__firebase_config === 'undefined' ||
            !window.__firebase_config
          ) {
            state.cloudEnabled = false;
            state.cloudConnected = false;
            updateCloudBadge('حالت آنلاین آماده (در انتظار پیکربندی فضای ابری)', false);
            return;
          }

          const firebaseConfig =
            typeof window.__firebase_config === 'string'
              ? JSON.parse(window.__firebase_config)
              : window.__firebase_config;

          if (!firebaseConfig || !firebaseConfig.apiKey) {
            state.cloudEnabled = false;
            state.cloudConnected = false;
            updateCloudBadge('حالت آنلاین آماده (تنظیمات ابری ناقص)', false);
            return;
          }

          state.cloudAppId =
            typeof window.__app_id !== 'undefined' && window.__app_id
              ? String(window.__app_id)
              : 'default-app-id';

          const appMod = await import('https://www.gstatic.com/firebasejs/11.6.1/firebase-app.js');
          const authMod = await import('https://www.gstatic.com/firebasejs/11.6.1/firebase-auth.js');
          const dbMod = await import('https://www.gstatic.com/firebasejs/11.6.1/firebase-firestore.js');

          const app = appMod.initializeApp(firebaseConfig);
          const auth = authMod.getAuth(app);
          const db = dbMod.getFirestore(app);

          if (
            typeof window.__initial_auth_token !== 'undefined' &&
            window.__initial_auth_token
          ) {
            await authMod.signInWithCustomToken(auth, window.__initial_auth_token);
          } else {
            await authMod.signInAnonymously(auth);
          }

          state.cloudUser = auth.currentUser;
          if (!state.cloudUser) {
            updateCloudBadge('اتصال احراز هویت برقرار نشد', false);
            return;
          }

          state.cloudEnabled = true;
          state.cloudConnected = true;
          state._fb = { db: db, dbMod: dbMod };
          updateCloudBadge('آنلاین و همگام‌سازی زنده ابری فعال است', true);

          startRealtimeCloudListeners(db, dbMod);
        } catch (err) {
          state.cloudEnabled = false;
          state.cloudConnected = false;
          updateCloudBadge('حالت محلی فعال (خطا در اتصال ابری)', false);
        }
      }

      function getPublicCollectionRef(db, dbMod, collectionName) {
        return dbMod.collection(
          db,
          'artifacts',
          state.cloudAppId,
          'public',
          'data',
          collectionName
        );
      }

      function getPublicDocRef(db, dbMod, collectionName, docId) {
        return dbMod.doc(
          db,
          'artifacts',
          state.cloudAppId,
          'public',
          'data',
          collectionName,
          docId
        );
      }

      function refreshAllViewsAfterSync() {
        renderHeaderLogo();
        renderOfficePhones();
        renderTopAdBar();
        renderHomeSection();
        renderPublicSearch();
        renderAdsSection();
        if (state.isAdminLoggedIn) {
          renderAdminSection();
        }
      }

      function startRealtimeCloudListeners(db, dbMod) {
        if (!state.cloudUser) return;

        // شنونده زنده ملکیت‌ها
        const propsCol = getPublicCollectionRef(db, dbMod, CLOUD_CONFIG.collections.PROPERTIES);
        dbMod.onSnapshot(
          propsCol,
          function (snap) {
            if (!state.cloudUser) return;
            const list = [];
            snap.forEach(function (d) {
              const data = d.data() || {};
              list.push(Object.assign({ id: d.id }, data));
            });
            if (list.length > 0) {
              state.properties = list;
              saveJsonData(STORAGE_KEYS.PROPERTIES, state.properties);
            } else {
              state.properties.forEach(function (p) {
                persistPropertyOnline(p);
              });
            }
            refreshAllViewsAfterSync();
          },
          function () {
            updateCloudBadge('همگام‌سازی زنده ملکیت‌ها با محدودیت مواجه شد', false);
          }
        );

        // شنونده زنده تبلیغات
        const adsCol = getPublicCollectionRef(db, dbMod, CLOUD_CONFIG.collections.ADS);
        dbMod.onSnapshot(
          adsCol,
          function (snap) {
            if (!state.cloudUser) return;
            const list = [];
            snap.forEach(function (d) {
              const data = d.data() || {};
              list.push(Object.assign({ id: d.id, active: data.active !== false }, data));
            });
            if (list.length > 0) {
              state.ads = list;
              saveJsonData(STORAGE_KEYS.ADS, state.ads);
            } else {
              state.ads.forEach(function (ad) {
                persistAdOnline(ad);
              });
            }
            refreshAllViewsAfterSync();
          },
          function () {}
        );

        // شنونده زنده شماره‌های تماس دفتر
        const phonesDoc = getPublicDocRef(db, dbMod, CLOUD_CONFIG.collections.PHONES, 'main');
        dbMod.onSnapshot(
          phonesDoc,
          function (snap) {
            if (!state.cloudUser) return;
            if (snap.exists() && Array.isArray(snap.data().list) && snap.data().list.length > 0) {
              state.phones = snap.data().list.map(function (ph) { return String(ph).trim(); }).filter(Boolean);
              saveJsonData(STORAGE_KEYS.PHONES, state.phones);
              refreshAllViewsAfterSync();
            } else {
              persistPhonesOnline(state.phones);
            }
          },
          function () {}
        );

        // شنونده زنده وضعیت بخش‌ها
        const sectionsDoc = getPublicDocRef(db, dbMod, CLOUD_CONFIG.collections.SECTIONS, 'main');
        dbMod.onSnapshot(
          sectionsDoc,
          function (snap) {
            if (!state.cloudUser) return;
            if (snap.exists() && snap.data().access && typeof snap.data().access === 'object') {
              state.sectionAccess = Object.assign({}, DEFAULT_SECTION_ACCESS, snap.data().access);
              saveJsonData(STORAGE_KEYS.SECTIONS, state.sectionAccess);
              refreshAllViewsAfterSync();
            } else {
              persistSectionsOnline(state.sectionAccess);
            }
          },
          function () {}
        );

        // شنونده زنده تنظیمات لوگو
        const logoDoc = getPublicDocRef(db, dbMod, CLOUD_CONFIG.collections.LOGO, 'main');
        dbMod.onSnapshot(
          logoDoc,
          function (snap) {
            if (!state.cloudUser) return;
            if (snap.exists() && snap.data().config && typeof snap.data().config === 'object') {
              state.logo = Object.assign({}, DEFAULT_LOGO, snap.data().config);
              saveJsonData(STORAGE_KEYS.LOGO, state.logo);
              refreshAllViewsAfterSync();
            } else {
              persistLogoOnline(state.logo);
            }
          },
          function () {}
        );

        // شنونده زنده اطلاعات ورود مدیر
        const credsDoc = getPublicDocRef(db, dbMod, CLOUD_CONFIG.collections.CREDS, 'admin_auth');
        dbMod.onSnapshot(
          credsDoc,
          function (snap) {
            if (!state.cloudUser) return;
            if (snap.exists() && snap.data().username && snap.data().password) {
              state.creds = {
                username: String(snap.data().username),
                password: String(snap.data().password)
              };
              saveJsonData(STORAGE_KEYS.CREDS, state.creds);
            } else {
              persistCredsOnline(state.creds);
            }
          },
          function () {}
        );
      }

      async function persistPropertyOnline(prop) {
        if (!state.cloudEnabled || !state.cloudUser || !state._fb) return;
        try {
          const ref = getPublicDocRef(
            state._fb.db,
            state._fb.dbMod,
            CLOUD_CONFIG.collections.PROPERTIES,
            String(prop.id)
          );
          await state._fb.dbMod.setDoc(ref, prop, { merge: true });
        } catch (e) {}
      }

      async function removePropertyOnline(propId) {
        if (!state.cloudEnabled || !state.cloudUser || !state._fb) return;
        try {
          const ref = getPublicDocRef(
            state._fb.db,
            state._fb.dbMod,
            CLOUD_CONFIG.collections.PROPERTIES,
            String(propId)
          );
          await state._fb.dbMod.deleteDoc(ref);
        } catch (e) {}
      }

      async function persistAdOnline(ad) {
        if (!state.cloudEnabled || !state.cloudUser || !state._fb) return;
        try {
          const ref = getPublicDocRef(
            state._fb.db,
            state._fb.dbMod,
            CLOUD_CONFIG.collections.ADS,
            String(ad.id)
          );
          await state._fb.dbMod.setDoc(ref, ad, { merge: true });
        } catch (e) {}
      }

      async function removeAdOnline(adId) {
        if (!state.cloudEnabled || !state.cloudUser || !state._fb) return;
        try {
          const ref = getPublicDocRef(
            state._fb.db,
            state._fb.dbMod,
            CLOUD_CONFIG.collections.ADS,
            String(adId)
          );
          await state._fb.dbMod.deleteDoc(ref);
        } catch (e) {}
      }

      async function persistPhonesOnline(phonesList) {
        if (!state.cloudEnabled || !state.cloudUser || !state._fb) return;
        try {
          const ref = getPublicDocRef(state._fb.db, state._fb.dbMod, CLOUD_CONFIG.collections.PHONES, 'main');
          await state._fb.dbMod.setDoc(ref, { list: phonesList }, { merge: true });
        } catch (e) {}
      }

      async function persistSectionsOnline(accessObj) {
        if (!state.cloudEnabled || !state.cloudUser || !state._fb) return;
        try {
          const ref = getPublicDocRef(state._fb.db, state._fb.dbMod, CLOUD_CONFIG.collections.SECTIONS, 'main');
          await state._fb.dbMod.setDoc(ref, { access: accessObj }, { merge: true });
        } catch (e) {}
      }

      async function persistLogoOnline(logoObj) {
        if (!state.cloudEnabled || !state.cloudUser || !state._fb) return;
        try {
          const ref = getPublicDocRef(state._fb.db, state._fb.dbMod, CLOUD_CONFIG.collections.LOGO, 'main');
          await state._fb.dbMod.setDoc(ref, { config: logoObj }, { merge: true });
        } catch (e) {}
      }

      async function persistCredsOnline(credsObj) {
        if (!state.cloudEnabled || !state.cloudUser || !state._fb) return;
        try {
          const ref = getPublicDocRef(state._fb.db, state._fb.dbMod, CLOUD_CONFIG.collections.CREDS, 'admin_auth');
          await state._fb.dbMod.setDoc(ref, {
            username: credsObj.username,
            password: credsObj.password
          }, { merge: true });
        } catch (e) {}
      }
<!-- ... existing code ... -->
          const toggleSectionBtn = target.closest('button[data-toggle-section]');
          if (toggleSectionBtn) {
            const secKey = toggleSectionBtn.getAttribute('data-toggle-section');
            const nextVal = !isSectionEnabled(secKey);
            state.sectionAccess[secKey] = nextVal;
            saveJsonData(STORAGE_KEYS.SECTIONS, state.sectionAccess);
            persistSectionsOnline(state.sectionAccess);
            renderAdminSectionsControl();
            showNotice('وضعیت دسترسی بخش «' + getSectionMeta(secKey).label + '» به ' + (nextVal ? 'فعال' : 'غیرفعال') + ' تغییر یافت.', false);
            return;
          }
<!-- ... existing code ... -->
          const approveBtn = target.closest('button[data-approve-prop]');
          if (approveBtn) {
            const propId = approveBtn.getAttribute('data-approve-prop');
            let updatedProp = null;
            state.properties = state.properties.map(function (p) {
              if (p.id === propId) {
                updatedProp = Object.assign({}, p, { approved: !p.approved });
                return updatedProp;
              }
              return p;
            });
            saveJsonData(STORAGE_KEYS.PROPERTIES, state.properties);
            if (updatedProp) persistPropertyOnline(updatedProp);
            renderAdminPropsTable();
            renderHomeSection();
            renderPublicSearch();
            showNotice('وضعیت ملکیت «' + propId + '» به‌روزرسانی شد.', false);
            return;
          }

          const delPropBtn = target.closest('button[data-delete-prop]');
          if (delPropBtn) {
            const propId = delPropBtn.getAttribute('data-delete-prop');
            state.properties = state.properties.filter(function (p) {
              return p.id !== propId;
            });
            saveJsonData(STORAGE_KEYS.PROPERTIES, state.properties);
            removePropertyOnline(propId);
            renderAdminPropsTable();
            renderHomeSection();
            renderPublicSearch();
            showNotice('ملکیت «' + propId + '» حذف شد.', false);
            return;
          }

          const toggleAdBtn = target.closest('button[data-toggle-ad]');
          if (toggleAdBtn) {
            const adId = toggleAdBtn.getAttribute('data-toggle-ad');
            let updatedAd = null;
            state.ads = state.ads.map(function (a) {
              if (a.id === adId) {
                updatedAd = Object.assign({}, a, { active: a.active === false ? true : false });
                return updatedAd;
              }
              return a;
            });
            saveJsonData(STORAGE_KEYS.ADS, state.ads);
            if (updatedAd) persistAdOnline(updatedAd);
            renderAdminAdsList();
            renderAdsSection();
            renderTopAdBar();
            renderHomeSection();
            showNotice('وضعیت آگهی «' + adId + '» به‌روزرسانی شد.', false);
            return;
          }

          const delAdBtn = target.closest('button[data-delete-ad]');
          if (delAdBtn) {
            const adId = delAdBtn.getAttribute('data-delete-ad');
            state.ads = state.ads.filter(function (a) {
              return a.id !== adId;
            });
            saveJsonData(STORAGE_KEYS.ADS, state.ads);
            removeAdOnline(adId);
            renderAdminAdsList();
            renderAdsSection();
            renderTopAdBar();
            renderHomeSection();
            showNotice('آگهی «' + adId + '» حذف شد.', false);
          }
        });

        // ثبت ملکیت جدید توسط مشتری
        document.getElementById('clientPropertyForm').addEventListener('submit', function (evt) {
          evt.preventDefault();
          const title = (document.getElementById('propTitle').value || '').trim();
          const pTypeSelect = document.getElementById('propType').value;
          const pTypeCustom = (document.getElementById('propTypeCustom').value || '').trim();
          const propertyType = pTypeSelect === 'سایر' ? (pTypeCustom || 'سایر') : pTypeSelect;

          const dTypeSelect = document.getElementById('dealType').value;
          const dTypeCustom = (document.getElementById('dealTypeCustom').value || '').trim();
          const dealType = dTypeSelect === 'سایر' ? (dTypeCustom || 'سایر') : dTypeSelect;

          const deedType = document.getElementById('deedType').value;
          const location = (document.getElementById('propLocation').value || '').trim();
          const price = (document.getElementById('propPrice').value || '').trim();
          const ownerName = (document.getElementById('ownerName').value || '').trim();
          const ownerPhone = (document.getElementById('ownerPhone').value || '').trim();
          const description = (document.getElementById('propDesc').value || '').trim();

          if (!title || !location || !ownerName || !ownerPhone) {
            showNotice('لطفاً عنوان/شماره ملکیت، موقعیت و نام و شماره تماس مالک را کامل وارد کنید.', true);
            return;
          }

          const newProp = {
            id: 'PR-' + String(Date.now()).slice(-6),
            title: title,
            propertyType: propertyType,
            dealType: dealType,
            deedType: deedType,
            location: location,
            price: price,
            ownerName: ownerName,
            ownerPhone: ownerPhone,
            description: description,
            propertyImage: state.draftPropImg || '',
            deedImage: state.draftDeedImg || '',
            approved: true,
            createdAt: new Date().toLocaleDateString('fa-AF')
          };

          state.properties.unshift(newProp);
          saveJsonData(STORAGE_KEYS.PROPERTIES, state.properties);
          persistPropertyOnline(newProp);

          evt.target.reset();
          document.getElementById('propTypeCustomGroup').classList.add('hidden');
          document.getElementById('dealTypeCustomGroup').classList.add('hidden');
          state.draftPropImg = '';
          state.draftDeedImg = '';
          document.getElementById('propImgPreviewWrap').innerHTML = '';
          document.getElementById('deedImgPreviewWrap').innerHTML = '';

          renderHomeSection();
          renderPublicSearch();
          if (state.isAdminLoggedIn) {
            renderAdminPropsTable();
          }

          showNotice(
            'ملکیت شما با کد «' + newProp.id + '» ثبت آنلاین شد و بلافاصله در جستجوی عمومی قرار گرفت. شماره شما نزد دیگران مخفی است و شماره‌های دفتر نمایش داده می‌شود.',
            false
          );
        });
<!-- ... existing code ... -->
          state.phones = parsedPhones;
          saveJsonData(STORAGE_KEYS.PHONES, state.phones);
          persistPhonesOnline(state.phones);
          renderOfficePhones();
          renderHomeSection();
          renderPublicSearch();
          renderAdsSection();
          showNotice('شماره‌های تماس رسمی دفتر با موفقیت ذخیره شد.', false);
        });

        document.getElementById('resetDefaultPhonesBtn').addEventListener('click', function () {
          state.phones = OFFICE_PHONES.slice();
          saveJsonData(STORAGE_KEYS.PHONES, state.phones);
          persistPhonesOnline(state.phones);
          syncOfficeInputsFromState();
          renderOfficePhones();
          renderHomeSection();
          renderPublicSearch();
          renderAdsSection();
          showNotice('شماره‌های تماس به فهرست پیش‌فرض دفتر بازگردانده شد.', false);
        });

        // ذخیره رنگ‌های لوگوی طبیعت پغمان
        document.getElementById('logoColorsForm').addEventListener('submit', function (evt) {
          evt.preventDefault();
          state.logo.mountainColor = document.getElementById('mountainColorInput').value || DEFAULT_LOGO.mountainColor;
          state.logo.meadowColor = document.getElementById('meadowColorInput').value || DEFAULT_LOGO.meadowColor;
          state.logo.starColor = document.getElementById('starColorInput').value || DEFAULT_LOGO.starColor;
          saveJsonData(STORAGE_KEYS.LOGO, state.logo);
          persistLogoOnline(state.logo);
          renderHeaderLogo();
          showNotice('رنگ‌بندی لوگوی طبیعت پغمان به‌روزرسانی شد.', false);
        });

        // آپلود لوگوی سفارشی
        document.getElementById('customLogoUpload').addEventListener('change', function (evt) {
          const file = evt.target.files && evt.target.files[0];
          if (!file) return;
          readImageFileAsDataUrl(file, function (dataUrl) {
            state.logo.customImage = dataUrl;
            saveJsonData(STORAGE_KEYS.LOGO, state.logo);
            persistLogoOnline(state.logo);
            renderHeaderLogo();
            showNotice('لوگوی سفارشی با موفقیت بارگذاری و ذخیره شد.', false);
          });
        });

        // بازگردانی لوگوی پیش‌فرض پغمان
        document.getElementById('resetDefaultLogoBtn').addEventListener('click', function () {
          state.logo = cloneObj(DEFAULT_LOGO);
          document.getElementById('customLogoUpload').value = '';
          saveJsonData(STORAGE_KEYS.LOGO, state.logo);
          persistLogoOnline(state.logo);
          syncLogoInputsFromState();
          renderHeaderLogo();
          showNotice('لوگوی پیش‌فرض طبیعت پغمان بازگردانی شد.', false);
        });

        // افزودن آگهی تبلیغاتی
        document.getElementById('adminAddAdForm').addEventListener('submit', function (evt) {
          evt.preventDefault();
          const title = (document.getElementById('newAdTitle').value || '').trim();
          const text = (document.getElementById('newAdText').value || '').trim();
          if (!title || !text) {
            showNotice('لطفاً عنوان و متن آگهی تبلیغاتی را وارد کنید.', true);
            return;
          }
          const newAd = {
            id: 'AD-' + String(Date.now()).slice(-5),
            title: title,
            text: text,
            active: true
          };
          state.ads.unshift(newAd);
          saveJsonData(STORAGE_KEYS.ADS, state.ads);
          persistAdOnline(newAd);
          evt.target.reset();
          renderAdminAdsList();
          renderAdsSection();
          renderTopAdBar();
          renderHomeSection();
          showNotice('آگهی تبلیغاتی جدید اضافه شد.', false);
        });

        // تغییر نام کاربری و رمز عبور مدیر
        document.getElementById('changeAdminCredsForm').addEventListener('submit', function (evt) {
          evt.preventDefault();
          const newUser = (document.getElementById('newAdminUsername').value || '').trim();
          const newPass = (document.getElementById('newAdminPassword').value || '').trim();
          if (!newUser || newPass.length < 4) {
            showNotice('نام کاربری و رمز عبور (حداقل ۴ کاراکتر) را وارد کنید.', true);
            return;
          }
          state.creds = { username: newUser, password: newPass };
          saveJsonData(STORAGE_KEYS.CREDS, state.creds);
          persistCredsOnline(state.creds);
          document.getElementById('newAdminPassword').value = '';
          showNotice('اطلاعات ورود مدیر با موفقیت تغییر یافت.', false);
        });
<!-- ... existing code ... -->
      // =======================================================================
      // ۱۵. راه‌اندازی اولیه صفحه
      // =======================================================================
      initState();
      renderHeaderLogo();
      renderOfficePhones();
      renderTopAdBar();
      bindEvents();
      switchSection('home');
      initFirebaseCloudSync();
    })();
  </script>
</body>
</html>