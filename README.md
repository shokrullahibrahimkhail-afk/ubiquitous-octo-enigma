</گگ<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>دفتر رهنمای معاملات شکرالله ابراهیم خیل | ستاره اعتماد - املاک رسمی</title>
  <meta name="description" content="وب‌سایت رسمی دفتر رهنمای معاملات شکرالله ابراهیم خیل (ستاره اعتماد) - مرجع معتبر خرید، فروش، کرایه، گروی، بیع وفا، اجاره و شراکت آباد املاک در سراسر افغانستان." />
  <meta name="keywords" content="رهنمای معاملات, شکرالله ابراهیم خیل, ستاره اعتماد, خرید و فروش خانه کابل, کرایه آپارتمان, زمین, دوکان, سرای, املاک افغانستان" />
  <meta name="author" content="دفتر رهنمای معاملات شکرالله ابراهیم خیل" />
  <meta name="robots" content="index, follow" />
  
  <!-- OpenGraph Meta Tags برای اشتراک‌گذاری رسمی و شناخت گوگل -->
  <meta property="og:title" content="دفتر رهنمای معاملات شکرالله ابراهیم خیل | ستاره اعتماد" />
  <meta property="og:description" content="سامانه رسمی ثبت، جستجو و معاملات املاک (خرید، فروش، کرایه، گروی، بیع وفا، اجاره و شراکت آباد) در سراسر افغانستان." />
  <meta property="og:type" content="website" />
  <meta property="og:locale" content="fa_AF" />

  <!-- داده‌های ساختاریافته گوگل (JSON-LD Schema) -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "RealEstateAgent",
    "name": "دفتر رهنمای معاملات شکرالله ابراهیم خیل - ستاره اعتماد",
    "description": "مرجع رسمی معاملات املاک، خرید، فروش، کرایه، گروی، اجاره و شراکت آباد در افغانستان",
    "telephone": ["+93705875878", "+93792928897", "+93731364644", "+93777514602", "+93747789284"],
    "address": {
      "@type": "PostalAddress",
      "addressCountry": "AF",
      "addressLocality": "Kabul"
    }
  }
  </script>

  <!-- فونت رسمی وزیرمتن -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
  
  <!-- آیکون‌های رسمی FontAwesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" />

  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            sans: ['Vazirmatn', 'sans-serif'],
          },
          colors: {
            navy: {
              950: '#060F1D',
              900: '#0B192C',
              800: '#102A43',
              700: '#1E3E62',
            },
            gold: {
              300: '#F3E5AB',
              400: '#E5C158',
              500: '#D4AF37',
              600: '#B59020',
              700: '#8E6F12',
            }
          }
        }
      }
    }
  </script>

  <style>
    :root {
      --bg-main: #f4f6f9;
      --primary-navy: #0B192C;
      --accent-gold: #D4AF37;
    }
    body {
      font-family: 'Vazirmatn', sans-serif;
      background-color: var(--bg-main);
      color: #1e293b;
      overflow-x: hidden;
    }
    .gold-gradient-text {
      background: linear-gradient(135deg, #F3E5AB 0%, #D4AF37 50%, #AA8218 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
    .gold-border-glow {
      box-shadow: 0 0 20px rgba(212, 175, 55, 0.25);
    }
    .ministry-pattern {
      background-color: var(--primary-navy);
      background-image: radial-gradient(rgba(212, 175, 55, 0.12) 1px, transparent 1px);
      background-size: 24px 24px;
    }
    .nav-tab.active {
      background: linear-gradient(135deg, #D4AF37 0%, #B59020 100%);
      color: #0B192C;
      font-weight: 800;
      box-shadow: 0 4px 12px rgba(212, 175, 55, 0.35);
    }
    /* اسکرول بار سفارشی */
    ::-webkit-scrollbar {
      width: 8px;
      height: 8px;
    }
    ::-webkit-scrollbar-track {
      background: #0B192C;
    }
    ::-webkit-scrollbar-thumb {
      background: #D4AF37;
      border-radius: 4px;
    }
  </style>
</head>
<body class="min-h-screen flex flex-col">

  <!-- نوار اعلان پیام (Toast Notification) -->
  <div id="toast-container" class="fixed bottom-5 left-5 z-50 flex flex-col gap-2 max-w-sm w-full pointer-events-none px-4 sm:px-0"></div>

  <!-- نوار رسمی بالای سایت (شبیه پورتال‌های وزارتی) -->
  <div class="bg-navy-950 text-slate-200 border-b border-gold-500/40 text-xs py-2 px-4">
    <div class="max-w-7xl mx-auto flex flex-wrap items-center justify-between gap-2">
      <div class="flex items-center gap-3">
        <span id="cloud-status-badge" class="inline-flex items-center gap-1.5 bg-gold-500/20 text-gold-400 border border-gold-500/40 px-2.5 py-0.5 rounded-full font-semibold">
          <span id="cloud-status-dot" class="w-2 h-2 rounded-full bg-amber-400 animate-pulse"></span>
          <span id="cloud-status-text">در حال اتصال به دیتابیس ابری زنده...</span>
        </span>
        <span id="top-announcement" class="hidden md:inline text-slate-300">مرجع معتبر خرید، فروش، کرایه، گروی، بیع وفا، اجاره و شراکت آباد در سراسر افغانستان</span>
      </div>
      <div class="flex flex-wrap items-center gap-3">
        <span id="current-date" class="text-gold-300 font-medium"></span>
        <button onclick="copyCurrentUrl('آدرس رسمی وب‌سایت کاپی شد!')" class="bg-navy-800 hover:bg-gold-500 hover:text-navy-950 text-gold-400 border border-gold-500/40 px-2.5 py-1 rounded-lg transition flex items-center gap-1.5 font-semibold cursor-pointer">
          <i class="fa-solid fa-share-nodes"></i>
          <span>کاپی لینک وب‌سایت</span>
        </button>
      </div>
    </div>
  </div>

  <!-- هدر رسمی با نشان اختصاصی مطابق عکس -->
  <header id="main-header" class="ministry-pattern text-white border-b-4 border-gold-500 shadow-2xl relative">
    <div class="max-w-7xl mx-auto px-4 py-5 sm:py-6">
      <div class="flex flex-col lg:flex-row items-center justify-between gap-6">
        
        <!-- لوگو و عنوان رسمی -->
        <div class="flex flex-col sm:flex-row items-center text-center sm:text-right gap-4">
          <!-- نشان رسمی SVG برگرفته دقیق از تصویر ارسالی -->
          <div class="w-24 h-24 sm:w-28 sm:h-28 rounded-full bg-white p-1.5 border-4 border-gold-500 gold-border-glow shrink-0 flex items-center justify-center shadow-xl">
            <svg viewBox="0 0 200 200" class="w-full h-full">
              <defs>
                <linearGradient id="goldGrad" x1="0%" y1="0%" x2="100%" y2="100%">
                  <stop offset="0%" stop-color="#F7E7A9"/>
                  <stop offset="50%" stop-color="#D4AF37"/>
                  <stop offset="100%" stop-color="#9A7213"/>
                </linearGradient>
                <linearGradient id="navyGrad" x1="0%" y1="0%" x2="0%" y2="100%">
                  <stop offset="0%" stop-color="#143254"/>
                  <stop offset="100%" stop-color="#071222"/>
                </linearGradient>
              </defs>
              <!-- حلقه بیرونی طلایی و سرمه‌ای -->
              <circle cx="100" cy="100" r="94" fill="none" stroke="url(#goldGrad)" stroke-width="5"/>
              <circle cx="100" cy="100" r="88" fill="none" stroke="url(#navyGrad)" stroke-width="3"/>
              <!-- برج‌های پشت ستاره -->
              <rect x="63" y="45" width="16" height="42" rx="2" fill="url(#navyGrad)" stroke="url(#goldGrad)" stroke-width="1.5"/>
              <line x1="67" y1="53" x2="75" y2="53" stroke="#D4AF37" stroke-width="2"/>
              <line x1="67" y1="60" x2="75" y2="60" stroke="#D4AF37" stroke-width="2"/>
              <line x1="67" y1="67" x2="75" y2="67" stroke="#D4AF37" stroke-width="2"/>
              
              <rect x="121" y="45" width="16" height="42" rx="2" fill="url(#navyGrad)" stroke="url(#goldGrad)" stroke-width="1.5"/>
              <line x1="125" y1="53" x2="133" y2="53" stroke="#D4AF37" stroke-width="2"/>
              <line x1="125" y1="60" x2="133" y2="60" stroke="#D4AF37" stroke-width="2"/>
              <line x1="125" y1="67" x2="133" y2="67" stroke="#D4AF37" stroke-width="2"/>

              <rect x="86" y="26" width="28" height="60" rx="2" fill="url(#navyGrad)" stroke="url(#goldGrad)" stroke-width="2"/>
              <line x1="93" y1="36" x2="93" y2="65" stroke="#D4AF37" stroke-width="2.5"/>
              <line x1="100" y1="32" x2="100" y2="65" stroke="#D4AF37" stroke-width="2.5"/>
              <line x1="107" y1="36" x2="107" y2="65" stroke="#D4AF37" stroke-width="2.5"/>

              <!-- ستاره بزرگ طلایی -->
              <polygon points="100,42 114,76 152,78 122,100 132,135 100,114 68,135 78,100 48,78 86,76" fill="url(#goldGrad)" stroke="#0B192C" stroke-width="2"/>
              <!-- سقف خانه زیر ستاره -->
              <polyline points="68,125 100,101 132,125" fill="none" stroke="url(#navyGrad)" stroke-width="7" stroke-linecap="round"/>
              <polyline points="68,125 100,101 132,125" fill="none" stroke="url(#goldGrad)" stroke-width="2.5" stroke-linecap="round"/>
              <!-- پنجره چهارخانه طلایی -->
              <rect x="92" y="117" width="6.5" height="6.5" fill="url(#goldGrad)" stroke="#0B192C" stroke-width="0.8"/>
              <rect x="101.5" y="117" width="6.5" height="6.5" fill="url(#goldGrad)" stroke="#0B192C" stroke-width="0.8"/>
              <rect x="92" y="126.5" width="6.5" height="6.5" fill="url(#goldGrad)" stroke="#0B192C" stroke-width="0.8"/>
              <rect x="101.5" y="126.5" width="6.5" height="6.5" fill="url(#goldGrad)" stroke="#0B192C" stroke-width="0.8"/>

              <!-- ریبون سرمه‌ای پایین لوگو -->
              <rect x="34" y="143" width="132" height="22" rx="11" fill="url(#navyGrad)" stroke="url(#goldGrad)" stroke-width="2"/>
              <text x="100" y="158" text-anchor="middle" fill="#F3E5AB" font-size="11" font-weight="bold" font-family="Vazirmatn, sans-serif">ستاره اعتماد • املاک</text>
            </svg>
          </div>

          <!-- عناوین رسمی دفتر -->
          <div>
            <div class="inline-flex items-center gap-2 bg-navy-800/90 border border-gold-500/50 px-3 py-1 rounded-full text-gold-300 text-xs sm:text-sm font-bold mb-2">
              <i class="fa-solid fa-landmark text-gold-400"></i>
              <span>دفتر رسمی رهنمای معاملات املاک</span>
            </div>
            <h1 id="site-main-title" class="text-2xl sm:text-3xl lg:text-4xl font-black tracking-tight text-white drop-shadow">
              دفتر رهنمای معاملات شکرالله ابراهیم خیل
            </h1>
            <p id="site-sub-title" class="text-lg sm:text-xl font-extrabold gold-gradient-text mt-1">
              ★ ستاره اعتماد — مرجع خرید، فروش، کرایه، گروی، بیع وفا، اجاره و شراکت آباد ★
            </p>
          </div>
        </div>

        <!-- باکس شماره‌های تماس رسمی (مطابق عکس) -->
        <div class="bg-navy-950/90 border-2 border-gold-500/60 rounded-2xl p-3.5 shadow-xl w-full lg:w-auto">
          <div class="text-xs text-gold-400 font-bold mb-2 flex items-center justify-between gap-2 border-b border-gold-500/20 pb-1.5">
            <span><i class="fa-solid fa-phone-volume ml-1"></i> شماره‌های تماس رسمی دفتر:</span>
            <span class="text-[11px] text-emerald-400">پاسخگویی مستقیم</span>
          </div>
          <div id="header-phones-list" class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-2 gap-1.5 text-xs sm:text-sm font-bold" dir="ltr">
            <!-- توسط جاوااسکریپت پر می‌شود -->
          </div>
        </div>

      </div>

      <!-- منوی ناوبری اصلی با لینک‌های جداگانه (#hash) -->
      <nav aria-label="منوی اصلی" class="mt-6 pt-4 border-t border-gold-500/30 flex flex-wrap items-center justify-between gap-2">
        <div class="flex flex-wrap items-center gap-2 w-full lg:w-auto">
          <a href="#home" data-route="home" onclick="navigateTo('home')" class="nav-tab active px-4 py-2.5 rounded-xl text-sm font-bold text-white hover:bg-navy-800 border border-gold-500/30 transition flex items-center gap-2">
            <i class="fa-solid fa-building-columns"></i>
            <span>صفحه اصلی</span>
          </a>
          <a href="#properties" data-route="properties" onclick="navigateTo('properties')" class="nav-tab px-4 py-2.5 rounded-xl text-sm font-bold text-white hover:bg-navy-800 border border-gold-500/30 transition flex items-center gap-2">
            <i class="fa-solid fa-magnifying-glass-location"></i>
            <span>جستجو و لیست ملکیت‌ها</span>
          </a>
          <a href="#register" data-route="register" onclick="navigateTo('register')" class="nav-tab px-4 py-2.5 rounded-xl text-sm font-bold text-white hover:bg-navy-800 border border-gold-500/30 transition flex items-center gap-2">
            <i class="fa-solid fa-file-signature"></i>
            <span>ثبت ملکیت جدید</span>
          </a>
          <a href="#contact" data-route="contact" onclick="navigateTo('contact')" class="nav-tab px-4 py-2.5 rounded-xl text-sm font-bold text-white hover:bg-navy-800 border border-gold-500/30 transition flex items-center gap-2">
            <i class="fa-solid fa-headset"></i>
            <span>تماس با مشتریان و دفتر</span>
          </a>
        </div>

        <div class="flex items-center gap-2 w-full lg:w-auto justify-end">
          <a href="#admin" data-route="admin" onclick="navigateTo('admin')" class="nav-tab px-4 py-2.5 rounded-xl text-sm font-bold bg-navy-800 text-gold-300 hover:bg-navy-700 border border-gold-500/60 transition flex items-center gap-2">
            <i class="fa-solid fa-user-shield"></i>
            <span>بخش مدیریت و کنترول</span>
          </a>
        </div>
      </nav>
    </div>
  </header>

  <!-- محتوای اصلی صفحات -->
  <main class="flex-grow max-w-7xl w-full mx-auto px-4 py-6 sm:py-8">

    <!-- ==================== بخش ۱: صفحه اصلی (#home) ==================== -->
    <section id="section-home" class="route-section space-y-8">
      
      <!-- بنر رسمی خوش‌آمدگویی و آمار -->
      <div id="hero-banner" class="bg-gradient-to-l from-navy-900 via-navy-800 to-navy-900 rounded-3xl p-6 sm:p-10 text-white border-2 border-gold-500/50 shadow-xl relative overflow-hidden">
        <div class="flex flex-col lg:flex-row items-center justify-between gap-8 relative z-10">
          <div class="space-y-4 max-w-2xl">
            <div class="inline-flex items-center gap-2 bg-gold-500/20 text-gold-300 px-3.5 py-1.5 rounded-xl text-xs sm:text-sm font-bold border border-gold-500/40">
              <i class="fa-solid fa-certificate"></i>
              <span>معاملات شفاف، قانونی و مطمئن زیر نظر متخصصین املاک</span>
            </div>
            <h2 id="hero-heading" class="text-2xl sm:text-4xl font-black leading-snug">
              سامانه رسمی ثبت و معاملات املاک <span class="text-gold-400">ستاره اعتماد</span>
            </h2>
            <p id="hero-desc" class="text-slate-200 text-sm sm:text-base leading-relaxed">
              دفتر رهنمای معاملات شکرالله ابراهیم خیل با سال‌ها تجربه و اعتبار درخشان، آماده ارائه خدمات معیاری در بخش خرید، فروش، کرایه، گروی، بیع وفا، اجاره و شراکت آباد انواع خانه، حویلی، آپارتمان، زمین، دوکان و سرای در سراسر افغانستان می‌باشد.
            </p>
            <div class="flex flex-wrap items-center gap-3 pt-2">
              <a href="#properties" onclick="navigateTo('properties')" class="bg-gold-500 hover:bg-gold-400 text-navy-950 font-extrabold px-6 py-3 rounded-xl shadow-lg transition flex items-center gap-2">
                <i class="fa-solid fa-search"></i>
                <span>جستجوی ملکیت‌ها</span>
              </a>
              <a href="#register" onclick="navigateTo('register')" class="bg-navy-950/80 hover:bg-navy-950 text-gold-300 border border-gold-500 font-bold px-6 py-3 rounded-xl transition flex items-center gap-2">
                <i class="fa-solid fa-plus-circle"></i>
                <span>ثبت ملکیت شما</span>
              </a>
              <button onclick="copySectionLink('home', 'صفحه اصلی')" class="bg-white/10 hover:bg-white/20 text-white px-4 py-3 rounded-xl text-sm font-semibold transition flex items-center gap-2 cursor-pointer">
                <i class="fa-solid fa-link"></i>
                <span>کاپی لینک این بخش</span>
              </button>
            </div>
          </div>

          <!-- کارت‌های آمار زنده -->
          <div class="grid grid-cols-2 gap-3 sm:gap-4 w-full lg:w-96 shrink-0">
            <div class="bg-navy-950/80 border border-gold-500/40 p-4 rounded-2xl text-center">
              <div class="text-gold-400 text-2xl mb-1"><i class="fa-solid fa-building"></i></div>
              <div id="stat-total-props" class="text-2xl sm:text-3xl font-black text-white">0</div>
              <div class="text-xs text-slate-300 mt-1">کل ملکیت‌های ثبت‌شده</div>
            </div>
            <div class="bg-navy-950/80 border border-gold-500/40 p-4 rounded-2xl text-center">
              <div class="text-emerald-400 text-2xl mb-1"><i class="fa-solid fa-handshake"></i></div>
              <div class="text-2xl sm:text-3xl font-black text-white">۸ نوع</div>
              <div class="text-xs text-slate-300 mt-1">معامله رسمی و شرعی</div>
            </div>
            <div class="bg-navy-950/80 border border-gold-500/40 p-4 rounded-2xl text-center">
              <div class="text-sky-400 text-2xl mb-1"><i class="fa-solid fa-map-location-dot"></i></div>
              <div class="text-2xl sm:text-3xl font-black text-white">۳۴ ولایت</div>
              <div class="text-xs text-slate-300 mt-1">پوشش سراسری افغانستان</div>
            </div>
            <div class="bg-navy-950/80 border border-gold-500/40 p-4 rounded-2xl text-center">
              <div class="text-gold-400 text-2xl mb-1"><i class="fa-solid fa-shield-halved"></i></div>
              <div class="text-2xl sm:text-3xl font-black text-white">۱۰۰٪</div>
              <div class="text-xs text-slate-300 mt-1">حفظ محرمیت مشتریان</div>
            </div>
          </div>
        </div>
      </div>

      <!-- خدمات رسمی دفتر (مطابق آیکون‌های پایین لوگو) -->
      <div>
        <div class="flex items-center justify-between mb-4">
          <h3 class="text-xl sm:text-2xl font-black text-navy-900 flex items-center gap-2">
            <span class="w-2 h-7 bg-gold-500 rounded-full inline-block"></span>
            خدمات رسمی معاملات املاک
          </h3>
          <span class="text-xs text-slate-500 font-semibold">انتخاب سریع برای جستجو</span>
        </div>
        <div class="grid grid-cols-2 sm:grid-cols-4 lg:grid-cols-8 gap-3">
          <button onclick="quickFilterTransaction('خرید')" class="bg-white hover:bg-navy-900 hover:text-white border border-slate-200 hover:border-gold-500 p-4 rounded-2xl shadow-sm transition text-center group cursor-pointer">
            <div class="w-12 h-12 mx-auto rounded-xl bg-gold-500/15 text-gold-600 group-hover:bg-gold-500 group-hover:text-navy-950 flex items-center justify-center text-xl mb-2 transition">
              <i class="fa-solid fa-house-chimney"></i>
            </div>
            <div class="font-extrabold text-sm">خرید</div>
          </button>
          <button onclick="quickFilterTransaction('فروش')" class="bg-white hover:bg-navy-900 hover:text-white border border-slate-200 hover:border-gold-500 p-4 rounded-2xl shadow-sm transition text-center group cursor-pointer">
            <div class="w-12 h-12 mx-auto rounded-xl bg-gold-500/15 text-gold-600 group-hover:bg-gold-500 group-hover:text-navy-950 flex items-center justify-center text-xl mb-2 transition">
              <i class="fa-solid fa-handshake"></i>
            </div>
            <div class="font-extrabold text-sm">فروش</div>
          </button>
          <button onclick="quickFilterTransaction('کرایه')" class="bg-white hover:bg-navy-900 hover:text-white border border-slate-200 hover:border-gold-500 p-4 rounded-2xl shadow-sm transition text-center group cursor-pointer">
            <div class="w-12 h-12 mx-auto rounded-xl bg-gold-500/15 text-gold-600 group-hover:bg-gold-500 group-hover:text-navy-950 flex items-center justify-center text-xl mb-2 transition">
              <i class="fa-solid fa-key"></i>
            </div>
            <div class="font-extrabold text-sm">کرایه</div>
          </button>
          <button onclick="quickFilterTransaction('گروی')" class="bg-white hover:bg-navy-900 hover:text-white border border-slate-200 hover:border-gold-500 p-4 rounded-2xl shadow-sm transition text-center group cursor-pointer">
            <div class="w-12 h-12 mx-auto rounded-xl bg-gold-500/15 text-gold-600 group-hover:bg-gold-500 group-hover:text-navy-950 flex items-center justify-center text-xl mb-2 transition">
              <i class="fa-solid fa-vault"></i>
            </div>
            <div class="font-extrabold text-sm">گروی</div>
          </button>
          <button onclick="quickFilterTransaction('بیع وفا')" class="bg-white hover:bg-navy-900 hover:text-white border border-slate-200 hover:border-gold-500 p-4 rounded-2xl shadow-sm transition text-center group cursor-pointer">
            <div class="w-12 h-12 mx-auto rounded-xl bg-gold-500/15 text-gold-600 group-hover:bg-gold-500 group-hover:text-navy-950 flex items-center justify-center text-xl mb-2 transition">
              <i class="fa-solid fa-file-contract"></i>
            </div>
            <div class="font-extrabold text-sm">بیع وفا</div>
          </button>
          <button onclick="quickFilterTransaction('اجاره')" class="bg-white hover:bg-navy-900 hover:text-white border border-slate-200 hover:border-gold-500 p-4 rounded-2xl shadow-sm transition text-center group cursor-pointer">
            <div class="w-12 h-12 mx-auto rounded-xl bg-gold-500/15 text-gold-600 group-hover:bg-gold-500 group-hover:text-navy-950 flex items-center justify-center text-xl mb-2 transition">
              <i class="fa-solid fa-briefcase"></i>
            </div>
            <div class="font-extrabold text-sm">اجاره</div>
          </button>
          <button onclick="quickFilterTransaction('شراکت آباد')" class="bg-white hover:bg-navy-900 hover:text-white border border-slate-200 hover:border-gold-500 p-4 rounded-2xl shadow-sm transition text-center group cursor-pointer">
            <div class="w-12 h-12 mx-auto rounded-xl bg-gold-500/15 text-gold-600 group-hover:bg-gold-500 group-hover:text-navy-950 flex items-center justify-center text-xl mb-2 transition">
              <i class="fa-solid fa-city"></i>
            </div>
            <div class="font-extrabold text-sm">شراکت آباد</div>
          </button>
          <button onclick="quickFilterTransaction('سایر')" class="bg-white hover:bg-navy-900 hover:text-white border border-slate-200 hover:border-gold-500 p-4 rounded-2xl shadow-sm transition text-center group cursor-pointer">
            <div class="w-12 h-12 mx-auto rounded-xl bg-gold-500/15 text-gold-600 group-hover:bg-gold-500 group-hover:text-navy-950 flex items-center justify-center text-xl mb-2 transition">
              <i class="fa-solid fa-layer-group"></i>
            </div>
            <div class="font-extrabold text-sm">سایر</div>
          </button>
        </div>
      </div>

      <!-- تازه‌ترین ملکیت‌های ثبت‌شده -->
      <div>
        <div class="flex flex-wrap items-center justify-between gap-2 mb-4">
          <h3 class="text-xl sm:text-2xl font-black text-navy-900 flex items-center gap-2">
            <span class="w-2 h-7 bg-gold-500 rounded-full inline-block"></span>
            تازه‌ترین ملکیت‌های ثبت‌شده در سیستم
          </h3>
          <a href="#properties" onclick="navigateTo('properties')" class="text-navy-800 hover:text-gold-600 font-bold text-sm flex items-center gap-1">
            <span>مشاهده همه و جدول جستجو</span>
            <i class="fa-solid fa-arrow-left"></i>
          </a>
        </div>
        <div id="home-featured-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
          <!-- کارت‌های ملکیت‌ها توسط جاوااسکریپت رندر می‌شوند -->
        </div>
      </div>
    </section>

    <!-- ==================== بخش ۲: جستجو و جدول ملکیت‌ها (#properties) ==================== -->
    <section id="section-properties" class="route-section hidden space-y-6">
      <div class="bg-white rounded-3xl p-6 border border-slate-200 shadow-sm">
        <div class="flex flex-wrap items-center justify-between gap-4 border-b border-slate-200 pb-4 mb-5">
          <div>
            <h2 class="text-2xl font-black text-navy-900 flex items-center gap-2">
              <i class="fa-solid fa-magnifying-glass-location text-gold-600"></i>
              سامانه جستجو و جدول رسمی ملکیت‌ها
            </h2>
            <p class="text-xs sm:text-sm text-slate-500 mt-1">
              جهت حفظ محرمیت مالکین، شماره تلفن مشتریان تنها نزد مدیریت دفتر محفوظ است. برای معلومات بیشتر با دفتر تماس بگیرید.
            </p>
          </div>
          <div class="flex items-center gap-2">
            <button onclick="copySectionLink('properties', 'جستجو و لیست ملکیت‌ها')" class="bg-navy-900 hover:bg-navy-800 text-gold-400 px-3.5 py-2 rounded-xl text-xs sm:text-sm font-bold flex items-center gap-1.5 cursor-pointer">
              <i class="fa-solid fa-share-nodes"></i>
              <span>ارسال لینک بخش جستجو</span>
            </button>
          </div>
        </div>

        <!-- فرم فیلتر و جستجوی پیشرفته -->
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-5 gap-3">
          <div>
            <label class="block text-xs font-bold text-slate-700 mb-1">جستجو در آدرس / مشخصات</label>
            <input type="text" id="filter-keyword" oninput="renderProperties()" placeholder="مثلاً: شهر نو، کارته چهار..." class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 focus:border-gold-500 focus:ring-2 focus:ring-gold-500/20 outline-none text-sm" />
          </div>
          <div>
            <label class="block text-xs font-bold text-slate-700 mb-1">ولایت</label>
            <select id="filter-province" onchange="renderProperties()" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm bg-white">
              <option value="">همه ولایات</option>
            </select>
          </div>
          <div>
            <label class="block text-xs font-bold text-slate-700 mb-1">نوع ملکیت</label>
            <select id="filter-type" onchange="renderProperties()" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm bg-white">
              <option value="">همه انواع ملکیت</option>
              <option value="خانه">خانه</option>
              <option value="حویلی">حویلی</option>
              <option value="آپارتمان">آپارتمان</option>
              <option value="زمین">زمین</option>
              <option value="دوکان">دوکان</option>
              <option value="سرای">سرای</option>
              <option value="سایر">سایر</option>
            </select>
          </div>
          <div>
            <label class="block text-xs font-bold text-slate-700 mb-1">نوع معامله</label>
            <select id="filter-transaction" onchange="renderProperties()" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm bg-white">
              <option value="">همه معاملات</option>
              <option value="خرید">خرید</option>
              <option value="فروش">فروش</option>
              <option value="گروی">گروی</option>
              <option value="کرایه">کرایه</option>
              <option value="اجاره">اجاره</option>
              <option value="بیع وفا">بیع وفا</option>
              <option value="شراکت آباد">شراکت آباد</option>
              <option value="سایر">سایر</option>
            </select>
          </div>
          <div>
            <label class="block text-xs font-bold text-slate-700 mb-1">نوع قباله</label>
            <select id="filter-deed" onchange="renderProperties()" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm bg-white">
              <option value="">همه انواع قباله</option>
              <option value="قباله شرعی">قباله شرعی</option>
              <option value="قباله عرفی">قباله عرفی</option>
              <option value="کتابچه صفایی">کتابچه صفایی</option>
              <option value="سایر">سایر</option>
            </select>
          </div>
        </div>

        <div class="flex flex-wrap items-center justify-between gap-3 mt-4 pt-4 border-t border-slate-100">
          <div class="text-sm font-bold text-navy-900">
            تعداد نتایج یافت‌شده: <span id="search-results-count" class="text-gold-600 font-black">0</span> ملکیت
          </div>
          <div class="flex items-center gap-2">
            <button onclick="resetFilters()" class="text-xs font-bold text-slate-600 hover:text-navy-900 px-3 py-2 rounded-lg bg-slate-100 hover:bg-slate-200 transition cursor-pointer">
              <i class="fa-solid fa-rotate-right ml-1"></i> پاک کردن فیلترها
            </button>
            <div class="bg-slate-100 p-1 rounded-xl flex items-center">
              <button id="btn-view-cards" onclick="setViewMode('cards')" class="px-3 py-1.5 rounded-lg text-xs font-bold bg-navy-900 text-gold-400 transition cursor-pointer">
                <i class="fa-solid fa-grip ml-1"></i> نمایش کارتی
              </button>
              <button id="btn-view-table" onclick="setViewMode('table')" class="px-3 py-1.5 rounded-lg text-xs font-bold text-slate-600 hover:text-navy-900 transition cursor-pointer">
                <i class="fa-solid fa-table-list ml-1"></i> جدول جستجو
              </button>
            </div>
          </div>
        </div>
      </div>

      <!-- نمایش کارتی ملکیت‌ها -->
      <div id="properties-cards-container" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6"></div>

      <!-- نمایش جدولی ملکیت‌ها (بدون نمایش شماره تلفن مشتری) -->
      <div id="properties-table-container" class="hidden bg-white rounded-3xl border border-slate-200 shadow-sm overflow-hidden">
        <div class="overflow-x-auto">
          <table class="w-full text-right border-collapse">
            <thead>
              <tr class="bg-navy-900 text-gold-300 text-xs sm:text-sm">
                <th class="p-3.5 font-bold">تصویر</th>
                <th class="p-3.5 font-bold">کد ملکیت</th>
                <th class="p-3.5 font-bold">اسم مشتری / مالک</th>
                <th class="p-3.5 font-bold">نوع ملکیت</th>
                <th class="p-3.5 font-bold">نوع معامله</th>
                <th class="p-3.5 font-bold">قیمت</th>
                <th class="p-3.5 font-bold">نوع قباله</th>
                <th class="p-3.5 font-bold">ولایت و آدرس</th>
                <th class="p-3.5 font-bold text-center">عملیات و لینک</th>
              </tr>
            </thead>
            <tbody id="properties-table-body" class="divide-y divide-slate-200 text-xs sm:text-sm">
              <!-- ردیف‌ها توسط جاوااسکریپت پر می‌شوند -->
            </tbody>
          </table>
        </div>
      </div>
    </section>

    <!-- ==================== بخش ۳: ثبت ملکیت جدید (#register) ==================== -->
    <section id="section-register" class="route-section hidden">
      <div class="max-w-4xl mx-auto bg-white rounded-3xl border-2 border-gold-500/40 shadow-xl overflow-hidden">
        <div class="bg-navy-900 text-white p-6 border-b-4 border-gold-500 flex flex-wrap items-center justify-between gap-4">
          <div>
            <h2 class="text-xl sm:text-2xl font-black text-gold-400 flex items-center gap-2">
              <i class="fa-solid fa-file-signature"></i>
              فورم رسمی ثبت ملکیت در سیستم
            </h2>
            <p class="text-xs sm:text-sm text-slate-300 mt-1">
              لطفاً مشخصات ملکیت را دقیق درج نمایید. شماره تماس شما کاملاً محرم بوده و فقط برای مدیر دفتر نمایش داده می‌شود.
            </p>
          </div>
          <button onclick="copySectionLink('register', 'فورم ثبت ملکیت')" class="bg-navy-800 hover:bg-gold-500 hover:text-navy-950 text-gold-300 border border-gold-500/40 px-3.5 py-2 rounded-xl text-xs font-bold flex items-center gap-1.5 transition cursor-pointer">
            <i class="fa-solid fa-link"></i>
            <span>کاپی لینک فورم ثبت</span>
          </button>
        </div>

        <form id="property-register-form" onsubmit="handlePropertySubmit(event)" class="p-6 sm:p-8 space-y-6">
          <div class="grid grid-cols-1 sm:grid-cols-2 gap-5">
            <!-- اسم مشتری -->
            <div>
              <label class="block text-sm font-bold text-navy-900 mb-1.5">
                اسم مشتری / مالک <span class="text-red-600">*</span>
              </label>
              <input type="text" id="reg-customer-name" required placeholder="نام و تخلص مشتری را بنویسید" class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 focus:ring-2 focus:ring-gold-500/20 outline-none text-sm" />
            </div>

            <!-- شماره تلفن مشتری (محرم) -->
            <div>
              <label class="block text-sm font-bold text-navy-900 mb-1.5">
                شماره تلفن مشتری <span class="text-red-600">*</span>
                <span class="text-[11px] bg-amber-100 text-amber-800 px-2 py-0.5 rounded-full mr-1">فقط برای مدیر نمایان است</span>
              </label>
              <input type="tel" id="reg-customer-phone" required dir="ltr" placeholder="07XXXXXXXX" class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 focus:ring-2 focus:ring-gold-500/20 outline-none text-sm text-right" />
            </div>

            <!-- نوع ملکیت -->
            <div>
              <label class="block text-sm font-bold text-navy-900 mb-1.5">
                نوع ملکیت <span class="text-red-600">*</span>
              </label>
              <select id="reg-property-type" required class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm bg-white">
                <option value="خانه">خانه</option>
                <option value="حویلی">حویلی</option>
                <option value="آپارتمان">آپارتمان</option>
                <option value="زمین">زمین</option>
                <option value="دوکان">دوکان</option>
                <option value="سرای">سرای</option>
                <option value="سایر">سایر</option>
              </select>
            </div>

            <!-- نوع معامله -->
            <div>
              <label class="block text-sm font-bold text-navy-900 mb-1.5">
                نوع معامله <span class="text-red-600">*</span>
              </label>
              <select id="reg-transaction-type" required class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm bg-white">
                <option value="فروش">فروش</option>
                <option value="خرید">خرید</option>
                <option value="گروی">گروی</option>
                <option value="کرایه">کرایه</option>
                <option value="اجاره">اجاره</option>
                <option value="بیع وفا">بیع وفا</option>
                <option value="شراکت آباد">شراکت آباد</option>
                <option value="سایر">سایر</option>
              </select>
            </div>

            <!-- قیمت ملکیت -->
            <div>
              <label class="block text-sm font-bold text-navy-900 mb-1.5">
                قیمت ملکیت <span class="text-red-600">*</span>
              </label>
              <div class="flex gap-2">
                <input type="text" id="reg-price" required placeholder="مثلاً: 45,000 یا 3,500,000" class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm" />
                <select id="reg-currency" class="px-3 py-3 rounded-xl border border-slate-300 bg-slate-50 font-bold text-sm outline-none">
                  <option value="دالر ($)">دالر ($)</option>
                  <option value="افغانی (؋)">افغانی (؋)</option>
                </select>
              </div>
            </div>

            <!-- نوع قباله ملکیت -->
            <div>
              <label class="block text-sm font-bold text-navy-900 mb-1.5">
                نوع قباله ملکیت <span class="text-red-600">*</span>
              </label>
              <select id="reg-deed-type" required class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm bg-white">
                <option value="قباله شرعی">قباله شرعی</option>
                <option value="قباله عرفی">قباله عرفی</option>
                <option value="قباله کلانتر">قباله کلانتر</option>
                <option value="کتابچه صفایی">کتابچه صفایی</option>
                <option value="سایر">سایر</option>
              </select>
            </div>

            <!-- ولایت -->
            <div>
              <label class="block text-sm font-bold text-navy-900 mb-1.5">
                ولایت <span class="text-red-600">*</span>
              </label>
              <select id="reg-province" required class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm bg-white">
                <!-- توسط جاوااسکریپت با ۳۴ ولایت پر می‌شود -->
              </select>
            </div>

            <!-- آدرس دقیق ملکیت -->
            <div>
              <label class="block text-sm font-bold text-navy-900 mb-1.5">
                آدرس دقیق ملکیت <span class="text-red-600">*</span>
              </label>
              <input type="text" id="reg-address" required placeholder="ناحیه، سرک، کوچه و نمبر خانه/دوکان" class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm" />
            </div>
          </div>

          <!-- بخش آپلود عکس‌ها -->
          <div class="grid grid-cols-1 sm:grid-cols-2 gap-5 pt-2 border-t border-slate-200">
            <!-- عکس ملکیت (ضروری) -->
            <div class="bg-slate-50 p-4 rounded-2xl border-2 border-dashed border-gold-500/70">
              <label class="block text-sm font-bold text-navy-900 mb-1">
                <i class="fa-solid fa-image text-gold-600 ml-1"></i>
                عکس ملکیت <span class="text-red-600 font-extrabold">(ضروری *)</span>
              </label>
              <p class="text-xs text-slate-500 mb-3">تصویر واضح از نمای بیرونی یا داخلی ملکیت انتخاب کنید.</p>
              <input type="file" id="reg-property-photo" accept="image/*" required onchange="previewImageFile(this, 'preview-prop-img')" class="block w-full text-xs text-slate-600 file:ml-3 file:py-2 file:px-4 file:rounded-xl file:border-0 file:text-xs file:font-bold file:bg-navy-900 file:text-gold-400 hover:file:bg-navy-800 cursor-pointer" />
              <div id="preview-prop-img-box" class="hidden mt-3">
                <img id="preview-prop-img" src="" alt="پیش‌نمایش ملکیت" class="w-full h-40 object-cover rounded-xl border border-slate-300" />
              </div>
            </div>

            <!-- عکس قباله (اختیاری) -->
            <div class="bg-slate-50 p-4 rounded-2xl border-2 border-dashed border-slate-300">
              <label class="block text-sm font-bold text-navy-900 mb-1">
                <i class="fa-solid fa-file-shield text-navy-700 ml-1"></i>
                عکس قباله ملکیت <span class="text-slate-500 font-normal">(اختیاری)</span>
              </label>
              <p class="text-xs text-slate-500 mb-3">تصویر قباله صرفاً نزد مدیر دفتر محفوظ می‌ماند و در سایت نشر نمی‌شود.</p>
              <input type="file" id="reg-deed-photo" accept="image/*" onchange="previewImageFile(this, 'preview-deed-img')" class="block w-full text-xs text-slate-600 file:ml-3 file:py-2 file:px-4 file:rounded-xl file:border-0 file:text-xs file:font-bold file:bg-slate-200 file:text-slate-800 hover:file:bg-slate-300 cursor-pointer" />
              <div id="preview-deed-img-box" class="hidden mt-3">
                <img id="preview-deed-img" src="" alt="پیش‌نمایش قباله" class="w-full h-40 object-cover rounded-xl border border-slate-300" />
              </div>
            </div>
          </div>

          <!-- توضیحات تکمیلی -->
          <div>
            <label class="block text-sm font-bold text-navy-900 mb-1.5">جزئیات و مشخصات اضافی (مساحت، تعداد اتاق، منزل و...)</label>
            <textarea id="reg-notes" rows="3" placeholder="مثلاً: ۴ بسوه، دارای ۵ اتاق، تهکوی، آب و برق مستقل..." class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm"></textarea>
          </div>

          <div class="flex flex-wrap items-center justify-end gap-3 pt-2">
            <button type="submit" id="btn-submit-property" class="w-full sm:w-auto bg-navy-900 hover:bg-navy-800 text-gold-400 border-2 border-gold-500 font-black px-8 py-3.5 rounded-xl shadow-lg transition flex items-center justify-center gap-2 cursor-pointer">
              <i class="fa-solid fa-check-circle"></i>
              <span>ثبت رسمی ملکیت در سامانه</span>
            </button>
          </div>
        </form>
      </div>
    </section>

    <!-- ==================== بخش ۴: تماس با مشتریان و دفتر (#contact) ==================== -->
    <section id="section-contact" class="route-section hidden space-y-6">
      <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
        
        <!-- اطلاعات تماس و شماره‌های رسمی -->
        <div class="bg-navy-900 text-white rounded-3xl p-6 sm:p-8 border-2 border-gold-500/50 shadow-xl space-y-6">
          <div class="flex items-center justify-between">
            <h2 class="text-xl sm:text-2xl font-black text-gold-400">ارتباط مستقیم با دفتر</h2>
            <button onclick="copySectionLink('contact', 'تماس با مشتریان')" class="bg-navy-800 text-gold-300 p-2 rounded-xl text-xs hover:bg-gold-500 hover:text-navy-950 transition cursor-pointer" title="کاپی لینک بخش تماس">
              <i class="fa-solid fa-link"></i>
            </button>
          </div>
          <p class="text-sm text-slate-300 leading-relaxed">
            مشتریان گرامی می‌توانند جهت استعلام ملکیت‌ها، هماهنگی بازدید حضوری و دریافت مشوره‌های حقوقی و معاملاتی با شماره‌های رسمی ذیل در تماس شوند:
          </p>

          <div id="contact-phones-cards" class="space-y-3">
            <!-- شماره‌های تماس + دکمه تماس و واتساپ توسط JS ساخته می‌شوند -->
          </div>

          <div class="bg-navy-950/70 p-4 rounded-2xl border border-gold-500/30 text-xs text-slate-300 space-y-2">
            <div class="font-bold text-gold-400"><i class="fa-solid fa-clock ml-1"></i> اوقات کاری دفتر:</div>
            <div>شنبه الی پنج‌شنبه: ۸:۰۰ صبح الی ۶:۰۰ عصر</div>
            <div>خدمات آنلاین وب‌سایت: ۲۴ ساعته در تمام مرورگرها</div>
          </div>
        </div>

        <!-- فورم ارسال پیام / درخواست مشتری -->
        <div class="lg:col-span-2 bg-white rounded-3xl p-6 sm:p-8 border border-slate-200 shadow-sm">
          <h3 class="text-xl sm:text-2xl font-black text-navy-900 mb-2">ارسال پیام و درخواست به مدیریت</h3>
          <p class="text-sm text-slate-500 mb-6">
            اگر ملکیت خاصی مد نظر دارید یا می‌خواهید کارشناسان ما با شما تماس بگیرند، فورم ذیل را خانه‌پری نمایید.
          </p>

          <form onsubmit="handleContactSubmit(event)" class="space-y-4">
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
              <div>
                <label class="block text-sm font-bold text-navy-900 mb-1">اسم مکمل شما <span class="text-red-600">*</span></label>
                <input type="text" id="contact-name" required placeholder="نام و تخلص" class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm" />
              </div>
              <div>
                <label class="block text-sm font-bold text-navy-900 mb-1">شماره تماس / واتساپ <span class="text-red-600">*</span></label>
                <input type="tel" id="contact-phone" required dir="ltr" placeholder="07XXXXXXXX" class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm text-right" />
              </div>
            </div>

            <div>
              <label class="block text-sm font-bold text-navy-900 mb-1">موضوع / کد ملکیت مورد نظر</label>
              <input type="text" id="contact-subject" placeholder="مثلاً: درخواست بازدید ملکیت کد #102 یا خرید خانه در کابل" class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm" />
            </div>

            <div>
              <label class="block text-sm font-bold text-navy-900 mb-1">متن پیام شما <span class="text-red-600">*</span></label>
              <textarea id="contact-message" rows="4" required placeholder="جزئیات درخواست یا سوال خود را اینجا بنویسید..." class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm"></textarea>
            </div>

            <button type="submit" class="bg-navy-900 hover:bg-navy-800 text-gold-400 border-2 border-gold-500 font-black px-8 py-3.5 rounded-xl shadow-md transition flex items-center gap-2 cursor-pointer">
              <i class="fa-solid fa-paper-plane"></i>
              <span>ارسال پیام به دفتر</span>
            </button>
          </form>
        </div>
      </div>
    </section>

    <!-- ==================== بخش ۵: مدیریت و کنترول (#admin) ==================== -->
    <section id="section-admin" class="route-section hidden">
      
      <!-- صفحه ورود مدیر -->
      <div id="admin-login-box" class="max-w-md mx-auto bg-white rounded-3xl border-2 border-gold-500/60 shadow-2xl overflow-hidden my-4">
        <div class="bg-navy-900 text-white p-6 text-center border-b-4 border-gold-500">
          <div class="w-16 h-16 mx-auto rounded-2xl bg-gold-500/20 border border-gold-500 text-gold-400 flex items-center justify-center text-3xl mb-3">
            <i class="fa-solid fa-user-shield"></i>
          </div>
          <h2 class="text-xl font-black">ورود به پنل مدیریت و کنترول</h2>
          <p class="text-xs text-slate-300 mt-1">دفتر رهنمای معاملات شکرالله ابراهیم خیل</p>
        </div>

        <form onsubmit="handleAdminLogin(event)" class="p-6 space-y-4">
          <div>
            <label class="block text-sm font-bold text-navy-900 mb-1">نام کاربری (Username)</label>
            <input type="text" id="login-username" required dir="ltr" placeholder="admin" class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm" />
          </div>
          <div>
            <label class="block text-sm font-bold text-navy-900 mb-1">رمز عبور (Password)</label>
            <input type="password" id="login-password" required dir="ltr" placeholder="••••••" class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm" />
          </div>
          <button type="submit" class="w-full bg-navy-900 hover:bg-navy-800 text-gold-400 border border-gold-500 font-black py-3.5 rounded-xl shadow-lg transition cursor-pointer">
            <i class="fa-solid fa-right-to-bracket ml-1"></i> ورود به سیستم مدیریت
          </button>
          <div class="bg-slate-100 p-3 rounded-xl text-xs text-slate-600 text-center border border-slate-200">
            نام کاربری پیش‌فرض: <strong dir="ltr" class="text-navy-900">admin</strong> | رمز پیش‌فرض: <strong dir="ltr" class="text-navy-900">123456</strong>
            <br><span class="text-[11px] text-slate-500">(پس از ورود می‌توانید هر زمان نام کاربری و رمز را تغییر دهید)</span>
          </div>
        </form>
      </div>

      <!-- داشبورد کامل مدیریت (پس از ورود) -->
      <div id="admin-dashboard" class="hidden space-y-6">
        <!-- نوار بالای داشبورد -->
        <div class="bg-navy-900 text-white rounded-3xl p-5 border-2 border-gold-500 flex flex-wrap items-center justify-between gap-4">
          <div class="flex items-center gap-3">
            <div class="w-12 h-12 rounded-2xl bg-gold-500 text-navy-950 flex items-center justify-center text-xl font-black">
              <i class="fa-solid fa-crown"></i>
            </div>
            <div>
              <h2 class="text-lg sm:text-xl font-black text-gold-400">پنل مرکزی مدیریت و کنترول</h2>
              <p class="text-xs text-slate-300">خوش آمدید، مدیر محترم (<span id="admin-current-user-label" class="font-bold text-white">admin</span>)</p>
            </div>
          </div>
          <div class="flex flex-wrap items-center gap-2">
            <button onclick="switchAdminTab('security')" class="bg-gold-500 hover:bg-gold-400 text-navy-950 px-3.5 py-2 rounded-xl text-xs font-extrabold shadow cursor-pointer flex items-center gap-1.5">
              <i class="fa-solid fa-key"></i> تغییر یوزر و رمز مدیریت
            </button>
            <button onclick="copySectionLink('admin', 'پنل مدیریت')" class="bg-navy-800 hover:bg-navy-700 text-gold-300 px-3.5 py-2 rounded-xl text-xs font-bold border border-gold-500/40 cursor-pointer">
              <i class="fa-solid fa-link ml-1"></i> کاپی لینک پنل
            </button>
            <button onclick="handleAdminLogout()" class="bg-red-600 hover:bg-red-700 text-white px-4 py-2 rounded-xl text-xs font-bold cursor-pointer">
              <i class="fa-solid fa-right-from-bracket ml-1"></i> خروج از مدیریت
            </button>
          </div>
        </div>

        <!-- تب‌های داخلی پنل مدیریت -->
        <div class="flex flex-wrap gap-2 bg-white p-2 rounded-2xl border border-slate-200 shadow-sm">
          <button onclick="switchAdminTab('manage-props')" id="admin-tab-manage-props" class="admin-subtab bg-navy-900 text-gold-400 px-4 py-2.5 rounded-xl text-xs sm:text-sm font-bold cursor-pointer">
            <i class="fa-solid fa-building-lock ml-1"></i> مدیریت ملکیت‌ها و شماره مشتریان
          </button>
          <button onclick="switchAdminTab('security')" id="admin-tab-security" class="admin-subtab text-slate-700 hover:bg-slate-100 px-4 py-2.5 rounded-xl text-xs sm:text-sm font-bold cursor-pointer border border-gold-500/40">
            <i class="fa-solid fa-user-lock text-gold-600 ml-1"></i> تغییر یوزر و رمز مدیریت
          </button>
          <button onclick="switchAdminTab('messages')" id="admin-tab-messages" class="admin-subtab text-slate-700 hover:bg-slate-100 px-4 py-2.5 rounded-xl text-xs sm:text-sm font-bold cursor-pointer">
            <i class="fa-solid fa-envelope-open-text ml-1"></i> پیام‌های مشتریان (<span id="admin-msg-badge">0</span>)
          </button>
          <button onclick="switchAdminTab('appearance')" id="admin-tab-appearance" class="admin-subtab text-slate-700 hover:bg-slate-100 px-4 py-2.5 rounded-xl text-xs sm:text-sm font-bold cursor-pointer">
            <i class="fa-solid fa-palette ml-1"></i> تغییر پس‌زمینه، عنوان و بخش‌ها
          </button>
        </div>

        <!-- تب ۱ مدیریت: جدول کامل ملکیت‌ها با شماره تلفن محرم مشتری و قباله -->
        <div id="admin-panel-manage-props" class="admin-panel bg-white rounded-3xl border border-slate-200 shadow-sm overflow-hidden">
          <div class="p-5 border-b border-slate-200 flex flex-wrap items-center justify-between gap-3">
            <div>
              <h3 class="text-lg font-black text-navy-900">لیست کامل ملکیت‌ها (دسترسی ویژه مدیر)</h3>
              <p class="text-xs text-slate-500">شماره تماس مشتریان و تصویر قباله فقط در این بخش قابل مشاهده است.</p>
            </div>
            <a href="#register" onclick="navigateTo('register')" class="bg-gold-500 hover:bg-gold-400 text-navy-950 font-bold px-4 py-2 rounded-xl text-xs flex items-center gap-1.5">
              <i class="fa-solid fa-plus"></i> ثبت ملکیت جدید
            </a>
          </div>
          <div class="overflow-x-auto">
            <table class="w-full text-right border-collapse">
              <thead>
                <tr class="bg-navy-900 text-gold-300 text-xs">
                  <th class="p-3">کد</th>
                  <th class="p-3">اسم مشتری</th>
                  <th class="p-3 bg-amber-900/60 text-amber-200">شماره تلفن مشتری (محرم)</th>
                  <th class="p-3">نوع ملکیت / معامله</th>
                  <th class="p-3">قیمت</th>
                  <th class="p-3">قباله</th>
                  <th class="p-3">ولایت / آدرس</th>
                  <th class="p-3">وضعیت</th>
                  <th class="p-3 text-center">ارسال لینک و مدیریت</th>
                </tr>
              </thead>
              <tbody id="admin-properties-tbody" class="divide-y divide-slate-200 text-xs">
                <!-- توسط جاوااسکریپت پر می‌شود -->
              </tbody>
            </table>
          </div>
        </div>

        <!-- تب ۲ مدیریت: پیام‌های مشتریان -->
        <div id="admin-panel-messages" class="admin-panel hidden bg-white rounded-3xl border border-slate-200 p-6 shadow-sm space-y-4">
          <h3 class="text-lg font-black text-navy-900">پیام‌ها و درخواست‌های دریافت‌شده از مشتریان</h3>
          <div id="admin-messages-list" class="grid grid-cols-1 md:grid-cols-2 gap-4">
            <!-- توسط JS پر می‌شود -->
          </div>
        </div>

        <!-- تب ۳ مدیریت: تغییر پس‌زمینه، عنوان و بخش‌های سایت -->
        <div id="admin-panel-appearance" class="admin-panel hidden bg-white rounded-3xl border border-slate-200 p-6 shadow-sm">
          <h3 class="text-lg font-black text-navy-900 mb-1">تنظیمات ظاهری، پس‌زمینه و عناوین وب‌سایت</h3>
          <p class="text-xs text-slate-500 mb-6">هر تغییری که اینجا ذخیره کنید بلافاصله در کل وب‌سایت اعمال و ذخیره می‌شود.</p>
          
          <form onsubmit="handleSaveSettings(event)" class="space-y-5 max-w-3xl">
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
              <div>
                <label class="block text-xs font-bold text-navy-900 mb-1">عنوان اصلی وب‌سایت (هدر)</label>
                <input type="text" id="set-main-title" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-sm" />
              </div>
              <div>
                <label class="block text-xs font-bold text-navy-900 mb-1">عنوان فرعی / شعار برند</label>
                <input type="text" id="set-sub-title" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-sm" />
              </div>
              <div class="sm:col-span-2">
                <label class="block text-xs font-bold text-navy-900 mb-1">متن نوار اعلان بالای سایت</label>
                <input type="text" id="set-announcement" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-sm" />
              </div>
              <div class="sm:col-span-2">
                <label class="block text-xs font-bold text-navy-900 mb-1">عنوان بنر صفحه اصلی</label>
                <input type="text" id="set-hero-heading" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-sm" />
              </div>
              <div class="sm:col-span-2">
                <label class="block text-xs font-bold text-navy-900 mb-1">توضیحات بنر صفحه اصلی</label>
                <textarea id="set-hero-desc" rows="2" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-sm"></textarea>
              </div>
              <div>
                <label class="block text-xs font-bold text-navy-900 mb-1">رنگ پس‌زمینه عمومی سایت</label>
                <input type="color" id="set-bg-color" value="#f4f6f9" class="w-full h-10 rounded-xl border border-slate-300 cursor-pointer" />
              </div>
              <div>
                <label class="block text-xs font-bold text-navy-900 mb-1">رنگ اصلی هدر و بخش‌های رسمی</label>
                <input type="color" id="set-navy-color" value="#0B192C" class="w-full h-10 rounded-xl border border-slate-300 cursor-pointer" />
              </div>
              <div class="sm:col-span-2">
                <label class="block text-xs font-bold text-navy-900 mb-1">شماره‌های تماس رسمی (با خط عمودی | جدا کنید)</label>
                <input type="text" id="set-phones" dir="ltr" class="w-full px-3.5 py-2.5 rounded-xl border border-slate-300 text-sm" />
              </div>
            </div>

            <div class="flex flex-wrap items-center gap-3 pt-2">
              <button type="submit" class="bg-navy-900 hover:bg-navy-800 text-gold-400 border border-gold-500 font-bold px-6 py-2.5 rounded-xl text-sm cursor-pointer">
                <i class="fa-solid fa-floppy-disk ml-1"></i> ذخیره و اعمال تغییرات در سرور ابری
              </button>
              <button type="button" onclick="resetSiteSettings()" class="bg-slate-200 hover:bg-slate-300 text-slate-800 font-bold px-4 py-2.5 rounded-xl text-xs cursor-pointer">
                بازگشت به تنظیمات پیش‌فرض
              </button>
            </div>
          </form>
        </div>

        <!-- تب ۴ مدیریت: تغییر یوزر و رمز عبور مدیریت -->
        <div id="admin-panel-security" class="admin-panel hidden bg-white rounded-3xl border-2 border-gold-500/60 p-6 sm:p-8 shadow-lg max-w-2xl">
          <div class="flex items-center gap-3 border-b border-slate-200 pb-4 mb-6">
            <div class="w-12 h-12 rounded-2xl bg-navy-900 text-gold-400 flex items-center justify-center text-xl">
              <i class="fa-solid fa-user-lock"></i>
            </div>
            <div>
              <h3 class="text-lg sm:text-xl font-black text-navy-900">تغییر یوزر (نام کاربری) و رمز عبور مدیریت</h3>
              <p class="text-xs text-slate-500 mt-0.5">مدیر محترم می‌تواند هر زمان نام کاربری و رمز ورود به پنل کنترول را تغییر دهد.</p>
            </div>
          </div>
          
          <form onsubmit="handleChangeCredentials(event)" class="space-y-4">
            <div class="bg-amber-50 border border-amber-200 rounded-2xl p-3.5 text-xs text-amber-900 flex items-center justify-between">
              <span>نام کاربری فعلی سیستم:</span>
              <strong dir="ltr" id="security-current-user-display" class="text-sm font-black bg-white px-3 py-1 rounded-lg border border-amber-300">admin</strong>
            </div>

            <div>
              <label class="block text-xs font-bold text-navy-900 mb-1">رمز عبور فعلی (Current Password) <span class="text-red-600">*</span></label>
              <div class="relative">
                <input type="password" id="current-admin-password" required dir="ltr" placeholder="رمز فعلی را وارد کنید" class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm" />
                <button type="button" onclick="togglePasswordField('current-admin-password', this)" class="absolute left-3 top-1/2 -translate-y-1/2 text-slate-400 hover:text-navy-900 cursor-pointer">
                  <i class="fa-solid fa-eye"></i>
                </button>
              </div>
            </div>

            <div>
              <label class="block text-xs font-bold text-navy-900 mb-1">نام کاربری جدید (New Username) <span class="text-red-600">*</span></label>
              <input type="text" id="new-admin-username" required dir="ltr" placeholder="نام کاربری جدید" class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm font-bold" />
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
              <div>
                <label class="block text-xs font-bold text-navy-900 mb-1">رمز عبور جدید (New Password) <span class="text-red-600">*</span></label>
                <div class="relative">
                  <input type="password" id="new-admin-password" required dir="ltr" minlength="4" placeholder="حداقل ۴ کاراکتر" class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm" />
                  <button type="button" onclick="togglePasswordField('new-admin-password', this)" class="absolute left-3 top-1/2 -translate-y-1/2 text-slate-400 hover:text-navy-900 cursor-pointer">
                    <i class="fa-solid fa-eye"></i>
                  </button>
                </div>
              </div>
              <div>
                <label class="block text-xs font-bold text-navy-900 mb-1">تکرار رمز عبور جدید <span class="text-red-600">*</span></label>
                <div class="relative">
                  <input type="password" id="confirm-admin-password" required dir="ltr" minlength="4" placeholder="تکرار رمز عبور جدید" class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-gold-500 outline-none text-sm" />
                  <button type="button" onclick="togglePasswordField('confirm-admin-password', this)" class="absolute left-3 top-1/2 -translate-y-1/2 text-slate-400 hover:text-navy-900 cursor-pointer">
                    <i class="fa-solid fa-eye"></i>
                  </button>
                </div>
              </div>
            </div>

            <div class="flex flex-wrap items-center gap-3 pt-3 border-t border-slate-100">
              <button type="submit" class="bg-navy-900 hover:bg-navy-800 text-gold-400 border-2 border-gold-500 font-black px-6 py-3 rounded-xl text-sm shadow-md transition flex items-center gap-2 cursor-pointer">
                <i class="fa-solid fa-floppy-disk"></i>
                <span>ذخیره یوزر و رمز جدید</span>
              </button>
              <button type="button" onclick="handleAdminLogout()" class="bg-slate-100 hover:bg-slate-200 text-navy-900 font-bold px-4 py-3 rounded-xl text-xs transition flex items-center gap-1.5 cursor-pointer">
                <i class="fa-solid fa-right-to-bracket"></i>
                <span>خروج و آزمایش ورود با رمز جدید</span>
              </button>
            </div>
          </form>
        </div>
      </div>
    </section>

  </main>

  <!-- مودال نمایش جزئیات ملکیت (برای مشتریان - بدون شماره تلفن مالک) -->
  <div id="property-detail-modal" class="fixed inset-0 bg-navy-950/80 backdrop-blur-sm z-50 hidden items-center justify-center p-4 overflow-y-auto">
    <div class="bg-white rounded-3xl max-w-3xl w-full border-2 border-gold-500 shadow-2xl overflow-hidden my-8">
      <div class="bg-navy-900 text-white px-6 py-4 flex items-center justify-between border-b-2 border-gold-500">
        <h3 id="modal-prop-title" class="text-lg font-black text-gold-400">جزئیات رسمی ملکیت</h3>
        <button onclick="closePropertyModal()" class="text-slate-300 hover:text-white text-xl cursor-pointer">
          <i class="fa-solid fa-xmark"></i>
        </button>
      </div>
      <div id="modal-prop-body" class="p-6 space-y-5">
        <!-- محتوا توسط JS پر می‌شود -->
      </div>
    </div>
  </div>

  <!-- فوتر رسمی وب‌سایت -->
  <footer class="bg-navy-950 text-slate-300 border-t-4 border-gold-500 mt-12">
    <div class="max-w-7xl mx-auto px-4 py-10 grid grid-cols-1 md:grid-cols-3 gap-8">
      <div>
        <h4 class="text-lg font-black text-gold-400 mb-3">دفتر رهنمای معاملات شکرالله ابراهیم خیل</h4>
        <p class="text-xs leading-relaxed text-slate-400">
          مرجع رسمی و قابل اعتماد در امور خرید، فروش، کرایه، گروی، بیع وفا، اجاره و شراکت آباد املاک در سراسر افغانستان. تمامی معاملات با اسناد معتبر و حفظ کامل محرمیت مشتریان انجام می‌گردد.
        </p>
      </div>
      <div>
        <h4 class="text-sm font-black text-white mb-3">دسترسی سریع به بخش‌ها (لینک‌های مستقیم)</h4>
        <ul class="space-y-2 text-xs">
          <li><a href="#home" onclick="navigateTo('home')" class="hover:text-gold-400 transition">• صفحه اصلی سامانه</a></li>
          <li><a href="#properties" onclick="navigateTo('properties')" class="hover:text-gold-400 transition">• جستجو و جدول ملکیت‌ها</a></li>
          <li><a href="#register" onclick="navigateTo('register')" class="hover:text-gold-400 transition">• ثبت ملکیت جدید</a></li>
          <li><a href="#contact" onclick="navigateTo('contact')" class="hover:text-gold-400 transition">• تماس با مشتریان و دفتر</a></li>
          <li><a href="#admin" onclick="navigateTo('admin')" class="hover:text-gold-400 transition">• بخش مدیریت و کنترول</a></li>
        </ul>
      </div>
      <div>
        <h4 class="text-sm font-black text-white mb-3">شماره‌های تماس رسمی دفتر</h4>
        <div id="footer-phones" class="space-y-1.5 text-xs font-bold text-gold-300" dir="ltr"></div>
      </div>
    </div>
    <div class="bg-black/40 py-3 px-4 text-center text-xs text-slate-400 border-t border-white/10">
      © ۱۴۰۵ - تمامی حقوق این سامانه متعلق به <span class="text-gold-400 font-bold">دفتر رهنمای معاملات شکرالله ابراهیم خیل (ستاره اعتماد)</span> می‌باشد.
    </div>
  </footer>

  <!-- اسکریپت اصلی و اتصال به Firebase Firestore برای آنلاین بودن در تمام مرورگرها -->
  <script type="module">
    import { initializeApp } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-app.js";
    import { getAuth, signInAnonymously, signInWithCustomToken } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-auth.js";
    import { getFirestore, doc, setDoc, addDoc, updateDoc, deleteDoc, onSnapshot, collection } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-firestore.js";

    // ==================== لیست ۳۴ ولایت افغانستان ====================
    const AFGHANISTAN_PROVINCES = [
      "کابل", "هرات", "بلخ", "قندهار", "ننگرهار", "کندز", "بغلان", "تخار", "بدخشان", "غزنی",
      "پکتیا", "پکتیکا", "خوست", "لوگر", "میدان وردک", "پروان", "کاپیسا", "پنجشیر", "بامیان",
      "دایکندی", "غور", "بادغیس", "فاریاب", "جوزجان", "سرپل", "سمنگان", "لغمان", "کنر",
      "نورستان", "فراه", "نیمروز", "هلمند", "زابل", "ارزگان"
    ];

    // ==================== تنظیمات پیش‌فرض سایت ====================
    const DEFAULT_SETTINGS = {
      mainTitle: "دفتر رهنمای معاملات شکرالله ابراهیم خیل",
      subTitle: "★ ستاره اعتماد — مرجع خرید، فروش، کرایه، گروی، بیع وفا، اجاره و شراکت آباد ★",
      announcement: "مرجع معتبر خرید، فروش، کرایه، گروی، بیع وفا، اجاره و شراکت آباد در سراسر افغانستان",
      heroHeading: "سامانه رسمی ثبت و معاملات املاک ستاره اعتماد",
      heroDesc: "دفتر رهنمای معاملات شکرالله ابراهیم خیل با سال‌ها تجربه و اعتبار درخشان، آماده ارائه خدمات معیاری در بخش خرید، فروش، کرایه، گروی، بیع وفا، اجاره و شراکت آباد انواع خانه، حویلی، آپارتمان، زمین، دوکان و سرای در سراسر افغانستان می‌باشد.",
      bgColor: "#f4f6f9",
      navyColor: "#0B192C",
      phones: "0705875878 | 0792928897 | 0731364644 | 0777514602 | 0747789284"
    };

    // ==================== نمونه‌های اولیه ملکیت برای نمایش فوری ====================
    const INITIAL_PROPERTIES = [
      {
        id: "PROP-101",
        code: "101",
        customerName: "حاجی محمد اکبر",
        customerPhone: "0700112233",
        propertyType: "حویلی",
        transactionType: "فروش",
        price: "145,000",
        currency: "دالر ($)",
        deedType: "قباله شرعی",
        province: "کابل",
        address: "کارته چهار، سرک سوم، نزدیک مسجد جامع",
        notes: "۴ بسوه پخته کاری، دارای ۶ اتاق مفشن، تهکوی مکمل، پارکینگ برای ۳ موتر و آب شیرین.",
        propertyPhoto: "https://images.unsplash.com/photo-1600596542815-ffad4c1539a9?auto=format&fit=crop&w=800&q=80",
        deedPhoto: "",
        createdAt: Date.now() - 86400000 * 2
      },
      {
        id: "PROP-102",
        code: "102",
        customerName: "انجنیر فرهاد ناصری",
        customerPhone: "0799445566",
        propertyType: "آپارتمان",
        transactionType: "کرایه",
        price: "18,000",
        currency: "افغانی (؋)",
        deedType: "قباله شرعی",
        province: "کابل",
        address: "شهر نو، چهارراهی انصاری، بلاک ستاره",
        notes: "۴ اتاقه آفتاب‌رخ، منزل سوم، دارای لفت ۲۴ ساعته، مرکزگرمی و نگهبانی.",
        propertyPhoto: "https://images.unsplash.com/photo-1545324418-cc1a3fa10c00?auto=format&fit=crop&w=800&q=80",
        deedPhoto: "",
        createdAt: Date.now() - 86400000
      },
      {
        id: "PROP-103",
        code: "103",
        customerName: "حاجی عبدالرحمن",
        customerPhone: "0788776655",
        propertyType: "دوکان",
        transactionType: "گروی",
        price: "25,000",
        currency: "دالر ($)",
        deedType: "کتابچه صفایی",
        province: "هرات",
        address: "چوک گلها، مارکیت تجارتی اعتماد، منزل اول",
        notes: "موقعیت عالی تجارتی، دارای دکوریشن مدرن، برق مستقل و امنیت کامل.",
        propertyPhoto: "https://images.unsplash.com/photo-1441986300917-64674bd600d8?auto=format&fit=crop&w=800&q=80",
        deedPhoto: "",
        createdAt: Date.now() - 3600000 * 5
      }
    ];

    // ==================== وضعیت سراسری برنامه ====================
    let state = {
      properties: [...INITIAL_PROPERTIES],
      messages: [],
      settings: { ...DEFAULT_SETTINGS },
      adminCreds: { username: "admin", password: "123456" },
      isAdminLoggedIn: false,
      viewMode: "cards",
      dbReady: false,
      user: null
    };

    let db = null;
    let auth = null;
    const appId = typeof __app_id !== 'undefined' ? __app_id : 'shukrullah-real-estate';

    // ==================== مقداردهی اولیه Firebase ====================
    function updateCloudBadge(status) {
      const dot = document.getElementById('cloud-status-dot');
      const text = document.getElementById('cloud-status-text');
      if (!dot || !text) return;
      if (status === 'online') {
        dot.className = "w-2 h-2 rounded-full bg-emerald-400 animate-pulse";
        text.textContent = "متصل به دیتابیس ابری زنده (همگام‌سازی خودکار)";
      } else {
        dot.className = "w-2 h-2 rounded-full bg-sky-400";
        text.textContent = "حالت آماده به کار (پشتیبان محلی فعال)";
      }
    }

    async function initCloudStorage() {
      try {
        if (typeof __firebase_config !== 'undefined' && __firebase_config) {
          const firebaseConfig = JSON.parse(__firebase_config);
          const app = initializeApp(firebaseConfig);
          auth = getAuth(app);
          db = getFirestore(app);

          if (typeof __initial_auth_token !== 'undefined' && __initial_auth_token) {
            await signInWithCustomToken(auth, __initial_auth_token);
          } else {
            await signInAnonymously(auth);
          }

          state.user = auth.currentUser;
          state.dbReady = true;
          updateCloudBadge('online');
          setupRealtimeListeners();
        } else {
          updateCloudBadge('fallback');
        }
      } catch (err) {
        console.warn("Running in fallback mode:", err);
        updateCloudBadge('fallback');
      }
    }

    function setupRealtimeListeners() {
      if (!db || !state.user) return;

      // ۱. گوش دادن به تغییرات ملکیت‌ها
      const propsCol = collection(db, 'artifacts', appId, 'public', 'data', 'properties');
      onSnapshot(propsCol, (snapshot) => {
        if (!snapshot.empty) {
          const list = [];
          snapshot.forEach(docSnap => {
            list.push({ id: docSnap.id, ...docSnap.data() });
          });
          list.sort((a, b) => (b.createdAt || 0) - (a.createdAt || 0));
          state.properties = list;
        }
        renderAll();
      }, (err) => console.error("Properties listener error:", err));

      // ۲. گوش دادن به پیام‌های مشتریان
      const msgsCol = collection(db, 'artifacts', appId, 'public', 'data', 'messages');
      onSnapshot(msgsCol, (snapshot) => {
        const list = [];
        snapshot.forEach(docSnap => {
          list.push({ id: docSnap.id, ...docSnap.data() });
        });
        list.sort((a, b) => (b.createdAt || 0) - (a.createdAt || 0));
        state.messages = list;
        renderAdminMessages();
      }, (err) => console.error("Messages listener error:", err));

      // ۳. گوش دادن به تنظیمات سایت و اعتبارنامه مدیر
      const configDoc = doc(db, 'artifacts', appId, 'public', 'data', 'config', 'main');
      onSnapshot(configDoc, (docSnap) => {
        if (docSnap.exists()) {
          const data = docSnap.data();
          if (data.settings) {
            state.settings = { ...DEFAULT_SETTINGS, ...data.settings };
            applySiteSettings();
          }
          if (data.adminCreds) {
            state.adminCreds = data.adminCreds;
            if (state.isAdminLoggedIn) {
              document.getElementById('admin-current-user-label').textContent = state.adminCreds.username;
              document.getElementById('security-current-user-display').textContent = state.adminCreds.username;
            }
          }
        }
      }, (err) => console.error("Config listener error:", err));
    }

    // ==================== توابع کمکی و نوتیفیکیشن ====================
    window.showToast = function(message, type = 'success') {
      const container = document.getElementById('toast-container');
      const toast = document.createElement('div');
      const bgClass = type === 'error' ? 'bg-red-700 border-red-400' : 'bg-navy-900 border-gold-500';
      const iconClass = type === 'error' ? 'fa-circle-exclamation text-red-300' : 'fa-circle-check text-gold-400';
      
      toast.className = `${bgClass} text-white border-2 px-4 py-3 rounded-2xl shadow-2xl flex items-center gap-3 text-xs sm:text-sm font-bold pointer-events-auto transition-all duration-300`;
      toast.innerHTML = `<i class="fa-solid ${iconClass} text-lg"></i><span>${message}</span>`;
      container.appendChild(toast);
      setTimeout(() => {
        toast.style.opacity = '0';
        setTimeout(() => toast.remove(), 300);
      }, 3500);
    };

    window.copyTextToClipboard = function(text, successMsg = 'لینک با موفقیت کاپی شد!') {
      const tempInput = document.createElement('input');
      tempInput.value = text;
      document.body.appendChild(tempInput);
      tempInput.select();
      document.execCommand('copy');
      document.body.removeChild(tempInput);
      showToast(successMsg);
    };

    window.copyCurrentUrl = function(msg) {
      copyTextToClipboard(window.location.href, msg);
    };

    window.copySectionLink = function(route, sectionTitle) {
      const baseUrl = window.location.href.split('#')[0];
      const fullLink = `${baseUrl}#${route}`;
      copyTextToClipboard(fullLink, `لینک بخش «${sectionTitle}» کاپی شد! می‌توانید برای مشتریان ارسال کنید.`);
    };

    window.copyPropertyLink = function(propId, propCode) {
      const baseUrl = window.location.href.split('#')[0];
      const fullLink = `${baseUrl}#property=${propId}`;
      copyTextToClipboard(fullLink, `لینک مستقیم ملکیت کد #${propCode} کاپی شد! آماده ارسال به مشتری.`);
    };

    // ==================== مسیریابی لینک‌های جداگانه (#hash) ====================
    window.navigateTo = function(route) {
      const validRoutes = ['home', 'properties', 'register', 'contact', 'admin'];
      if (!validRoutes.includes(route)) route = 'home';

      document.querySelectorAll('.route-section').forEach(sec => sec.classList.add('hidden'));
      const targetSec = document.getElementById(`section-${route}`);
      if (targetSec) targetSec.classList.remove('hidden');

      document.querySelectorAll('.nav-tab').forEach(tab => {
        if (tab.dataset.route === route) {
          tab.classList.add('active');
        } else {
          tab.classList.remove('active');
        }
      });

      if (window.location.hash !== `#${route}` && !window.location.hash.startsWith('#property=')) {
        history.replaceState(null, '', `#${route}`);
      }
      window.scrollTo({ top: 0, behavior: 'smooth' });
    };

    function handleHashChange() {
      const hash = window.location.hash.replace('#', '');
      if (hash.startsWith('property=')) {
        const propId = hash.split('=')[1];
        navigateTo('properties');
        setTimeout(() => openPropertyModal(propId), 200);
      } else if (hash) {
        navigateTo(hash);
      } else {
        navigateTo('home');
      }
    }

    // ==================== اعمال تنظیمات ظاهری و محتوایی سایت ====================
    function applySiteSettings() {
      const s = state.settings;
      document.documentElement.style.setProperty('--bg-main', s.bgColor);
      document.documentElement.style.setProperty('--primary-navy', s.navyColor);
      document.body.style.backgroundColor = s.bgColor;

      document.getElementById('site-main-title').textContent = s.mainTitle;
      document.getElementById('site-sub-title').textContent = s.subTitle;
      document.getElementById('top-announcement').textContent = s.announcement;
      document.getElementById('hero-heading').textContent = s.heroHeading;
      document.getElementById('hero-desc').textContent = s.heroDesc;

      // پر کردن فیلدهای فرم تنظیمات در پنل مدیریت
      document.getElementById('set-main-title').value = s.mainTitle;
      document.getElementById('set-sub-title').value = s.subTitle;
      document.getElementById('set-announcement').value = s.announcement;
      document.getElementById('set-hero-heading').value = s.heroHeading;
      document.getElementById('set-hero-desc').value = s.heroDesc;
      document.getElementById('set-bg-color').value = s.bgColor;
      document.getElementById('set-navy-color').value = s.navyColor;
      document.getElementById('set-phones').value = s.phones;

      // رندر شماره‌های تماس در هدر، صفحه تماس و فوتر
      const phoneList = s.phones.split('|').map(p => p.trim()).filter(Boolean);
      
      const headerPhonesEl = document.getElementById('header-phones-list');
      headerPhonesEl.innerHTML = phoneList.map(ph => `
        <a href="tel:${ph}" class="flex items-center justify-center gap-1.5 bg-navy-900 hover:bg-gold-500 hover:text-navy-950 text-gold-300 px-2.5 py-1.5 rounded-lg border border-gold-500/30 transition">
          <i class="fa-solid fa-phone text-[11px]"></i>
          <span>${ph}</span>
        </a>
      `).join('');

      const contactPhonesEl = document.getElementById('contact-phones-cards');
      contactPhonesEl.innerHTML = phoneList.map(ph => `
        <div class="bg-navy-950/90 border border-gold-500/40 p-3 rounded-2xl flex items-center justify-between gap-2">
          <span class="font-black text-gold-300 text-base" dir="ltr">${ph}</span>
          <div class="flex items-center gap-2">
            <a href="tel:${ph}" class="bg-gold-500 hover:bg-gold-400 text-navy-950 px-3 py-1.5 rounded-xl text-xs font-extrabold flex items-center gap-1">
              <i class="fa-solid fa-phone"></i> تماس
            </a>
            <a href="https://wa.me/93${ph.replace(/^0/, '')}" target="_blank" class="bg-emerald-600 hover:bg-emerald-500 text-white px-3 py-1.5 rounded-xl text-xs font-extrabold flex items-center gap-1">
              <i class="fa-brands fa-whatsapp"></i> واتساپ
            </a>
          </div>
        </div>
      `).join('');

      document.getElementById('footer-phones').innerHTML = phoneList.map(ph => `
        <div><a href="tel:${ph}" class="hover:text-white transition"><i class="fa-solid fa-phone ml-1.5"></i>${ph}</a></div>
      `).join('');
    }

    // ==================== آپلود و فشرده‌سازی تصویر ====================
    let compressedPropertyPhoto = "";
    let compressedDeedPhoto = "";

    window.previewImageFile = function(input, previewImgId) {
      const file = input.files[0];
      if (!file) return;

      const reader = new FileReader();
      reader.onload = function(e) {
        const img = new Image();
        img.onload = function() {
          const canvas = document.createElement('canvas');
          const MAX_WIDTH = 680;
          let width = img.width;
          let height = img.height;
          if (width > MAX_WIDTH) {
            height *= MAX_WIDTH / width;
            width = MAX_WIDTH;
          }
          canvas.width = width;
          canvas.height = height;
          const ctx = canvas.getContext('2d');
          ctx.drawImage(img, 0, 0, width, height);
          const dataUrl = canvas.toDataURL('image/jpeg', 0.65);

          document.getElementById(previewImgId).src = dataUrl;
          document.getElementById(`${previewImgId}-box`).classList.remove('hidden');

          if (previewImgId === 'preview-prop-img') {
            compressedPropertyPhoto = dataUrl;
          } else {
            compressedDeedPhoto = dataUrl;
          }
        };
        img.src = e.target.result;
      };
      reader.readAsDataURL(file);
    };

    // ==================== ثبت ملکیت جدید ====================
    window.handlePropertySubmit = async function(e) {
      e.preventDefault();
      if (!compressedPropertyPhoto) {
        showToast('لطفاً عکس ملکیت را انتخاب نمایید (ضروری است).', 'error');
        return;
      }

      const submitBtn = document.getElementById('btn-submit-property');
      if (submitBtn) {
        submitBtn.disabled = true;
        submitBtn.innerHTML = '<i class="fa-solid fa-spinner fa-spin"></i> <span>در حال ذخیره در دیتابیس ابری...</span>';
      }

      const newCode = String(100 + state.properties.length + 1);
      const newProp = {
        code: newCode,
        customerName: document.getElementById('reg-customer-name').value.trim(),
        customerPhone: document.getElementById('reg-customer-phone').value.trim(),
        propertyType: document.getElementById('reg-property-type').value,
        transactionType: document.getElementById('reg-transaction-type').value,
        price: document.getElementById('reg-price').value.trim(),
        currency: document.getElementById('reg-currency').value,
        deedType: document.getElementById('reg-deed-type').value,
        province: document.getElementById('reg-province').value,
        address: document.getElementById('reg-address').value.trim(),
        notes: document.getElementById('reg-notes').value.trim(),
        propertyPhoto: compressedPropertyPhoto,
        deedPhoto: compressedDeedPhoto || "",
        approved: true,
        createdAt: Date.now()
      };

      try {
        if (db && state.user) {
          const propsCol = collection(db, 'artifacts', appId, 'public', 'data', 'properties');
          await addDoc(propsCol, newProp);
        } else {
          newProp.id = `PROP-${Date.now()}`;
          state.properties.unshift(newProp);
          renderAll();
        }

        e.target.reset();
        compressedPropertyPhoto = "";
        compressedDeedPhoto = "";
        document.getElementById('preview-prop-img-box').classList.add('hidden');
        document.getElementById('preview-deed-img-box').classList.add('hidden');

        showToast(`ملکیت شما با کد #${newCode} در دیتابیس ابری ثبت و برای همه کاربران فعال شد!`);
        navigateTo('properties');
      } catch (err) {
        console.error(err);
        showToast('خطا در ثبت ملکیت. لطفاً حجم عکس را کمتر انتخاب کنید.', 'error');
      } finally {
        if (submitBtn) {
          submitBtn.disabled = false;
          submitBtn.innerHTML = '<i class="fa-solid fa-check-circle"></i> <span>ثبت رسمی ملکیت در سامانه</span>';
        }
      }
    };

    // ==================== ارسال پیام از بخش تماس با مشتریان ====================
    window.handleContactSubmit = async function(e) {
      e.preventDefault();
      const msgObj = {
        name: document.getElementById('contact-name').value.trim(),
        phone: document.getElementById('contact-phone').value.trim(),
        subject: document.getElementById('contact-subject').value.trim() || "استعلام عمومی",
        message: document.getElementById('contact-message').value.trim(),
        createdAt: Date.now()
      };

      try {
        if (db && state.user) {
          const msgsCol = collection(db, 'artifacts', appId, 'public', 'data', 'messages');
          await addDoc(msgsCol, msgObj);
        } else {
          msgObj.id = `MSG-${Date.now()}`;
          state.messages.unshift(msgObj);
          renderAdminMessages();
        }
        e.target.reset();
        showToast('پیام شما با موفقیت به دفتر ارسال شد. همکاران ما به زودی تماس می‌گیرند.');
      } catch (err) {
        console.error(err);
        showToast('خطا در ارسال پیام.', 'error');
      }
    };

    // ==================== رندر کارت‌ها و جدول عمومی (بدون نمایش شماره تلفن مشتری!) ====================
    function createPropertyCardHTML(prop) {
      return `
        <article class="bg-white rounded-3xl border border-slate-200 hover:border-gold-500 shadow-sm hover:shadow-xl transition overflow-hidden flex flex-col">
          <div class="relative h-52 bg-navy-900 overflow-hidden">
            <img src="${prop.propertyPhoto}" alt="${prop.propertyType} در ${prop.province}" onerror="this.src='https://placehold.co/600x400/0B192C/D4AF37?text=ستاره+اعتماد'" class="w-full h-full object-cover hover:scale-105 transition duration-500" />
            <div class="absolute top-3 right-3 flex flex-wrap gap-1.5">
              <span class="bg-navy-900/90 text-gold-400 border border-gold-500/60 px-3 py-1 rounded-xl text-xs font-extrabold">
                ${prop.transactionType}
              </span>
              <span class="bg-gold-500 text-navy-950 px-3 py-1 rounded-xl text-xs font-black">
                ${prop.propertyType}
              </span>
            </div>
            <div class="absolute bottom-3 left-3 bg-navy-950/90 text-white px-2.5 py-1 rounded-lg text-xs font-bold border border-white/20">
              کد: #${prop.code}
            </div>
          </div>

          <div class="p-5 flex-grow flex flex-col justify-between space-y-4">
            <div>
              <div class="flex items-center justify-between gap-2 mb-2">
                <span class="text-xs font-bold text-slate-500 flex items-center gap-1">
                  <i class="fa-solid fa-location-dot text-gold-600"></i>
                  ولایت ${prop.province}
                </span>
                <span class="text-xs font-bold bg-slate-100 text-navy-900 px-2.5 py-1 rounded-lg">
                  <i class="fa-solid fa-file-contract text-gold-600 ml-1"></i>${prop.deedType}
                </span>
              </div>

              <h4 class="font-black text-navy-900 text-base line-clamp-1 mb-1">
                ${prop.propertyType} برای ${prop.transactionType} - ${prop.address}
              </h4>
              <p class="text-xs text-slate-600 line-clamp-2 leading-relaxed">
                ${prop.notes || 'ثبت‌شده در دفتر رسمی رهنمای معاملات شکرالله ابراهیم خیل'}
              </p>
            </div>

            <div class="pt-3 border-t border-slate-100 space-y-3">
              <div class="flex items-center justify-between">
                <span class="text-xs text-slate-500 font-semibold">قیمت تعیین‌شده:</span>
                <span class="text-base font-black text-emerald-700">${prop.price} ${prop.currency}</span>
              </div>

              <div class="flex items-center gap-2">
                <button onclick="openPropertyModal('${prop.id}')" class="flex-grow bg-navy-900 hover:bg-navy-800 text-gold-400 font-bold py-2.5 px-3 rounded-xl text-xs transition cursor-pointer">
                  <i class="fa-solid fa-eye ml-1"></i> جزئیات و تماس با دفتر
                </button>
                <button onclick="copyPropertyLink('${prop.id}', '${prop.code}')" title="کاپی لینک مستقیم این ملکیت" class="bg-gold-500/20 hover:bg-gold-500 text-navy-900 px-3 py-2.5 rounded-xl text-xs font-bold transition cursor-pointer">
                  <i class="fa-solid fa-share-nodes"></i>
                </button>
              </div>
            </div>
          </div>
        </article>
      `;
    }

    window.renderProperties = function() {
      const keyword = (document.getElementById('filter-keyword')?.value || '').trim().toLowerCase();
      const province = document.getElementById('filter-province')?.value || '';
      const type = document.getElementById('filter-type')?.value || '';
      const transaction = document.getElementById('filter-transaction')?.value || '';
      const deed = document.getElementById('filter-deed')?.value || '';

      const filtered = state.properties.filter(p => {
        const matchKey = !keyword || 
          (p.address && p.address.toLowerCase().includes(keyword)) ||
          (p.notes && p.notes.toLowerCase().includes(keyword)) ||
          (p.customerName && p.customerName.toLowerCase().includes(keyword)) ||
          (p.code && p.code.includes(keyword));
        const matchProv = !province || p.province === province;
        const matchType = !type || p.propertyType === type;
        const matchTrans = !transaction || p.transactionType === transaction;
        const matchDeed = !deed || p.deedType === deed;
        return matchKey && matchProv && matchType && matchTrans && matchDeed;
      });

      document.getElementById('search-results-count').textContent = filtered.length;
      document.getElementById('stat-total-props').textContent = state.properties.length;

      // رندر کارت‌های صفحه اصلی (۳ مورد اول)
      const homeGrid = document.getElementById('home-featured-grid');
      if (homeGrid) {
        homeGrid.innerHTML = state.properties.slice(0, 3).map(createPropertyCardHTML).join('');
      }

      // رندر کارت‌های بخش جستجو
      const cardsContainer = document.getElementById('properties-cards-container');
      if (filtered.length === 0) {
        cardsContainer.innerHTML = `
          <div class="col-span-full bg-white rounded-3xl p-10 text-center border border-slate-200">
            <i class="fa-solid fa-folder-open text-4xl text-slate-300 mb-3"></i>
            <p class="font-bold text-slate-600">هیچ ملکیتی با این مشخصات یافت نشد.</p>
          </div>
        `;
      } else {
        cardsContainer.innerHTML = filtered.map(createPropertyCardHTML).join('');
      }

      // رندر جدول جستجو (STRICT PRIVACY: بدون شماره تلفن مشتری!)
      const tbody = document.getElementById('properties-table-body');
      tbody.innerHTML = filtered.map(p => `
        <tr class="hover:bg-slate-50 transition">
          <td class="p-3">
            <img src="${p.propertyPhoto}" alt="ملکیت" class="w-14 h-12 object-cover rounded-lg border border-slate-200" />
          </td>
          <td class="p-3 font-black text-navy-900">#${p.code}</td>
          <td class="p-3 font-bold text-slate-800">${p.customerName}</td>
          <td class="p-3"><span class="bg-gold-500/20 text-navy-900 px-2.5 py-1 rounded-lg font-bold">${p.propertyType}</span></td>
          <td class="p-3"><span class="bg-navy-900 text-gold-400 px-2.5 py-1 rounded-lg font-bold">${p.transactionType}</span></td>
          <td class="p-3 font-black text-emerald-700">${p.price} ${p.currency}</td>
          <td class="p-3 text-slate-600">${p.deedType}</td>
          <td class="p-3 text-slate-700"><strong>${p.province}</strong> - ${p.address}</td>
          <td class="p-3 text-center">
            <div class="flex items-center justify-center gap-1.5">
              <button onclick="openPropertyModal('${p.id}')" class="bg-navy-900 text-gold-400 px-2.5 py-1.5 rounded-lg font-bold hover:bg-navy-800 cursor-pointer">مشاهده</button>
              <button onclick="copyPropertyLink('${p.id}', '${p.code}')" title="کاپی لینک ملکیت" class="bg-gold-500 text-navy-950 px-2.5 py-1.5 rounded-lg font-bold hover:bg-gold-400 cursor-pointer">
                <i class="fa-solid fa-link"></i>
              </button>
            </div>
          </td>
        </tr>
      `).join('');
    };

    window.setViewMode = function(mode) {
      state.viewMode = mode;
      const cardsEl = document.getElementById('properties-cards-container');
      const tableEl = document.getElementById('properties-table-container');
      const btnCards = document.getElementById('btn-view-cards');
      const btnTable = document.getElementById('btn-view-table');

      if (mode === 'cards') {
        cardsEl.classList.remove('hidden');
        tableEl.classList.add('hidden');
        btnCards.className = "px-3 py-1.5 rounded-lg text-xs font-bold bg-navy-900 text-gold-400 transition cursor-pointer";
        btnTable.className = "px-3 py-1.5 rounded-lg text-xs font-bold text-slate-600 hover:text-navy-900 transition cursor-pointer";
      } else {
        cardsEl.classList.add('hidden');
        tableEl.classList.remove('hidden');
        btnTable.className = "px-3 py-1.5 rounded-lg text-xs font-bold bg-navy-900 text-gold-400 transition cursor-pointer";
        btnCards.className = "px-3 py-1.5 rounded-lg text-xs font-bold text-slate-600 hover:text-navy-900 transition cursor-pointer";
      }
    };

    window.quickFilterTransaction = function(transType) {
      document.getElementById('filter-transaction').value = transType;
      navigateTo('properties');
      renderProperties();
    };

    window.resetFilters = function() {
      document.getElementById('filter-keyword').value = '';
      document.getElementById('filter-province').value = '';
      document.getElementById('filter-type').value = '';
      document.getElementById('filter-transaction').value = '';
      document.getElementById('filter-deed').value = '';
      renderProperties();
    };

    // ==================== مودال جزئیات ملکیت (محافظت از حریم خصوصی مالک) ====================
    window.openPropertyModal = function(propId) {
      const prop = state.properties.find(p => p.id === propId);
      if (!prop) return;

      const officePhones = state.settings.phones.split('|').map(p => p.trim()).filter(Boolean);
      const primaryPhone = officePhones[0] || "0705875878";

      document.getElementById('modal-prop-title').textContent = `ملکیت کد #${prop.code} — ${prop.propertyType} (${prop.transactionType})`;
      document.getElementById('modal-prop-body').innerHTML = `
        <div class="grid grid-cols-1 md:grid-cols-2 gap-5">
          <div>
            <img src="${prop.propertyPhoto}" alt="${prop.propertyType}" class="w-full h-64 object-cover rounded-2xl border border-slate-200 shadow" />
          </div>
          <div class="space-y-3 text-sm">
            <div class="flex justify-between border-b pb-2">
              <span class="text-slate-500">نوع ملکیت:</span>
              <span class="font-black text-navy-900">${prop.propertyType}</span>
            </div>
            <div class="flex justify-between border-b pb-2">
              <span class="text-slate-500">نوع معامله:</span>
              <span class="font-black text-gold-700">${prop.transactionType}</span>
            </div>
            <div class="flex justify-between border-b pb-2">
              <span class="text-slate-500">قیمت:</span>
              <span class="font-black text-emerald-700 text-base">${prop.price} ${prop.currency}</span>
            </div>
            <div class="flex justify-between border-b pb-2">
              <span class="text-slate-500">نوع قباله:</span>
              <span class="font-bold text-navy-900">${prop.deedType}</span>
            </div>
            <div class="flex justify-between border-b pb-2">
              <span class="text-slate-500">ولایت:</span>
              <span class="font-bold text-navy-900">${prop.province}</span>
            </div>
            <div>
              <span class="text-slate-500 block mb-1">آدرس دقیق:</span>
              <span class="font-bold text-navy-900">${prop.address}</span>
            </div>
          </div>
        </div>

        <div class="bg-slate-50 p-4 rounded-2xl border border-slate-200 text-xs sm:text-sm text-slate-700">
          <strong class="text-navy-900 block mb-1">توضیحات تکمیلی:</strong>
          ${prop.notes || 'بدون توضیحات اضافی.'}
        </div>

        <div class="bg-navy-900 text-white p-4 rounded-2xl border border-gold-500/50 flex flex-wrap items-center justify-between gap-3">
          <div>
            <div class="text-xs text-gold-400 font-bold">جهت بازدید حضوری و انجام معامله با دفتر تماس بگیرید:</div>
            <div class="text-sm font-black mt-1" dir="ltr">${state.settings.phones}</div>
          </div>
          <div class="flex flex-wrap items-center gap-2">
            <a href="tel:${primaryPhone}" class="bg-gold-500 hover:bg-gold-400 text-navy-950 font-black px-4 py-2.5 rounded-xl text-xs flex items-center gap-1.5">
              <i class="fa-solid fa-phone"></i> تماس با دفتر
            </a>
            <button onclick="copyPropertyLink('${prop.id}', '${prop.code}')" class="bg-white/10 hover:bg-white/20 text-white font-bold px-4 py-2.5 rounded-xl text-xs flex items-center gap-1.5 cursor-pointer">
              <i class="fa-solid fa-share-nodes"></i> اشتراک‌گذاری لینک
            </button>
          </div>
        </div>
      `;

      const modal = document.getElementById('property-detail-modal');
      modal.classList.remove('hidden');
      modal.classList.add('flex');
    };

    window.closePropertyModal = function() {
      const modal = document.getElementById('property-detail-modal');
      modal.classList.add('hidden');
      modal.classList.remove('flex');
      if (window.location.hash.startsWith('#property=')) {
        history.replaceState(null, '', '#properties');
      }
    };

    // ==================== بخش مدیریت و کنترول (Admin Panel) ====================
    window.togglePasswordField = function(inputId, btn) {
      const input = document.getElementById(inputId);
      const icon = btn.querySelector('i');
      if (input.type === 'password') {
        input.type = 'text';
        icon.classList.remove('fa-eye');
        icon.classList.add('fa-eye-slash');
      } else {
        input.type = 'password';
        icon.classList.remove('fa-eye-slash');
        icon.classList.add('fa-eye');
      }
    };

    window.handleAdminLogin = function(e) {
      e.preventDefault();
      const user = document.getElementById('login-username').value.trim();
      const pass = document.getElementById('login-password').value.trim();

      if (user === state.adminCreds.username && pass === state.adminCreds.password) {
        state.isAdminLoggedIn = true;
        document.getElementById('admin-login-box').classList.add('hidden');
        document.getElementById('admin-dashboard').classList.remove('hidden');
        document.getElementById('admin-current-user-label').textContent = user;
        document.getElementById('security-current-user-display').textContent = user;
        document.getElementById('new-admin-username').value = user;
        renderAdminDashboard();
        showToast('ورود موفقیت‌آمیز به پنل مدیریت و کنترول!');
      } else {
        showToast('نام کاربری یا رمز عبور اشتباه است!', 'error');
      }
    };

    window.handleAdminLogout = function() {
      state.isAdminLoggedIn = false;
      document.getElementById('admin-login-box').classList.remove('hidden');
      document.getElementById('admin-dashboard').classList.add('hidden');
      document.getElementById('login-password').value = '';
      showToast('از پنل مدیریت خارج شدید.');
    };

    window.switchAdminTab = function(tabName) {
      document.querySelectorAll('.admin-panel').forEach(p => p.classList.add('hidden'));
      document.getElementById(`admin-panel-${tabName}`).classList.remove('hidden');

      document.querySelectorAll('.admin-subtab').forEach(btn => {
        btn.className = "admin-subtab text-slate-700 hover:bg-slate-100 px-4 py-2.5 rounded-xl text-xs sm:text-sm font-bold cursor-pointer";
      });
      const activeBtn = document.getElementById(`admin-tab-${tabName}`);
      if (activeBtn) {
        activeBtn.className = "admin-subtab bg-navy-900 text-gold-400 px-4 py-2.5 rounded-xl text-xs sm:text-sm font-bold cursor-pointer";
      }
    };

    function renderAdminDashboard() {
      if (!state.isAdminLoggedIn) return;
      
      // جدول ملکیت‌ها با شماره تلفن محرم مشتری و قباله
      const tbody = document.getElementById('admin-properties-tbody');
      tbody.innerHTML = state.properties.map(p => `
        <tr class="hover:bg-slate-50">
          <td class="p-3 font-black">#${p.code}</td>
          <td class="p-3 font-bold text-navy-900">${p.customerName}</td>
          <td class="p-3 bg-amber-50 font-black text-amber-900" dir="ltr">
            <a href="tel:${p.customerPhone}" class="underline hover:text-gold-600">${p.customerPhone}</a>
          </td>
          <td class="p-3">${p.propertyType} / <strong>${p.transactionType}</strong></td>
          <td class="p-3 font-bold text-emerald-700">${p.price} ${p.currency}</td>
          <td class="p-3">
            ${p.deedType}
            ${p.deedPhoto ? `<button type="button" onclick="viewDeedPhotoModal('${p.id}')" class="block text-[11px] text-blue-600 underline mt-0.5 cursor-pointer">مشاهده عکس قباله</button>` : ''}
          </td>
          <td class="p-3">${p.province} - ${p.address}</td>
          <td class="p-3">
            <span class="bg-emerald-100 text-emerald-800 px-2 py-0.5 rounded-full font-bold text-[11px]">منتشر شده</span>
          </td>
          <td class="p-3 text-center">
            <div class="flex items-center justify-center gap-1.5">
              <button onclick="copyPropertyLink('${p.id}', '${p.code}')" class="bg-gold-500 text-navy-950 px-2.5 py-1.5 rounded-lg font-bold hover:bg-gold-400 cursor-pointer" title="ارسال لینک به مشتری">
                <i class="fa-solid fa-share-nodes"></i> لینک
              </button>
              <button onclick="deleteProperty('${p.id}')" class="bg-red-600 text-white px-2.5 py-1.5 rounded-lg font-bold hover:bg-red-700 cursor-pointer" title="حذف ملکیت">
                <i class="fa-solid fa-trash"></i>
              </button>
            </div>
          </td>
        </tr>
      `).join('');

      renderAdminMessages();
    }

    window.viewDeedPhotoModal = function(propId) {
      const prop = state.properties.find(p => p.id === propId);
      if (!prop || !prop.deedPhoto) return;
      document.getElementById('modal-prop-title').textContent = `تصویر قباله محرم — ملکیت کد #${prop.code} (${prop.customerName})`;
      document.getElementById('modal-prop-body').innerHTML = `
        <div class="text-center space-y-3">
          <p class="text-xs text-amber-800 bg-amber-50 border border-amber-200 p-2.5 rounded-xl font-bold">
            <i class="fa-solid fa-lock ml-1"></i> این سند صرفاً برای مدیر سیستم قابل مشاهده است.
          </p>
          <img src="${prop.deedPhoto}" alt="تصویر قباله" class="max-h-[70vh] mx-auto rounded-2xl border-2 border-navy-900 shadow-lg" />
        </div>
      `;
      const modal = document.getElementById('property-detail-modal');
      modal.classList.remove('hidden');
      modal.classList.add('flex');
    };

    function renderAdminMessages() {
      document.getElementById('admin-msg-badge').textContent = state.messages.length;
      const listEl = document.getElementById('admin-messages-list');
      if (!listEl) return;

      if (state.messages.length === 0) {
        listEl.innerHTML = `<div class="col-span-full text-center text-slate-500 py-8 text-sm">تاکنون پیامی ثبت نشده است.</div>`;
        return;
      }

      listEl.innerHTML = state.messages.map(m => `
        <div class="bg-slate-50 border border-slate-200 rounded-2xl p-4 space-y-2">
          <div class="flex items-center justify-between">
            <span class="font-black text-navy-900 text-sm">${m.name}</span>
            <a href="tel:${m.phone}" dir="ltr" class="bg-emerald-600 text-white px-2.5 py-1 rounded-lg text-xs font-bold">${m.phone}</a>
          </div>
          <div class="text-xs font-bold text-gold-700">موضوع: ${m.subject}</div>
          <p class="text-xs text-slate-700 leading-relaxed bg-white p-3 rounded-xl border border-slate-200">${m.message}</p>
        </div>
      `).join('');
    }

    window.deleteProperty = async function(propId) {
      try {
        if (db && state.user && !propId.startsWith('PROP-')) {
          await deleteDoc(doc(db, 'artifacts', appId, 'public', 'data', 'properties', propId));
        } else {
          state.properties = state.properties.filter(p => p.id !== propId);
          renderAll();
        }
        showToast('ملکیت مورد نظر حذف شد.');
      } catch (err) {
        console.error(err);
        showToast('خطا در حذف ملکیت.', 'error');
      }
    };

    window.handleSaveSettings = async function(e) {
      e.preventDefault();
      const updatedSettings = {
        mainTitle: document.getElementById('set-main-title').value.trim(),
        subTitle: document.getElementById('set-sub-title').value.trim(),
        announcement: document.getElementById('set-announcement').value.trim(),
        heroHeading: document.getElementById('set-hero-heading').value.trim(),
        heroDesc: document.getElementById('set-hero-desc').value.trim(),
        bgColor: document.getElementById('set-bg-color').value,
        navyColor: document.getElementById('set-navy-color').value,
        phones: document.getElementById('set-phones').value.trim()
      };

      state.settings = updatedSettings;
      applySiteSettings();

      if (db && state.user) {
        await setDoc(doc(db, 'artifacts', appId, 'public', 'data', 'config', 'main'), {
          settings: updatedSettings,
          adminCreds: state.adminCreds
        }, { merge: true });
      }
      showToast('تغییرات ظاهری، پس‌زمینه و عناوین با موفقیت ذخیره و اعمال شد!');
    };

    window.resetSiteSettings = async function() {
      state.settings = { ...DEFAULT_SETTINGS };
      applySiteSettings();
      if (db && state.user) {
        await setDoc(doc(db, 'artifacts', appId, 'public', 'data', 'config', 'main'), {
          settings: state.settings
        }, { merge: true });
      }
      showToast('تنظیمات سایت به حالت اولیه بازگردانده شد.');
    };

    window.handleChangeCredentials = async function(e) {
      e.preventDefault();
      const currentPass = document.getElementById('current-admin-password').value.trim();
      const newUser = document.getElementById('new-admin-username').value.trim();
      const newPass = document.getElementById('new-admin-password').value.trim();
      const confirmPass = document.getElementById('confirm-admin-password').value.trim();

      if (currentPass !== state.adminCreds.password) {
        showToast('رمز عبور فعلی اشتباه وارد شده است!', 'error');
        return;
      }

      if (!newUser) {
        showToast('نام کاربری جدید نمی‌تواند خالی باشد!', 'error');
        return;
      }

      if (newPass !== confirmPass) {
        showToast('رمز عبور جدید و تکرار آن مطابقت ندارند!', 'error');
        return;
      }

      state.adminCreds = { username: newUser, password: newPass };
      document.getElementById('admin-current-user-label').textContent = newUser;
      document.getElementById('security-current-user-display').textContent = newUser;

      if (db && state.user) {
        await setDoc(doc(db, 'artifacts', appId, 'public', 'data', 'config', 'main'), {
          adminCreds: state.adminCreds
        }, { merge: true });
      }

      document.getElementById('current-admin-password').value = '';
      document.getElementById('new-admin-password').value = '';
      document.getElementById('confirm-admin-password').value = '';
      showToast(`یوزر جدید (${newUser}) و رمز عبور مدیریت با موفقیت ذخیره شد!`);
    };

    function renderAll() {
      renderProperties();
      if (state.isAdminLoggedIn) {
        renderAdminDashboard();
      }
    }

    // ==================== راه‌اندازی اولیه صفحه ====================
    window.addEventListener('DOMContentLoaded', () => {
      // پر کردن لیست ۳۴ ولایت در فرم‌ها
      const regProv = document.getElementById('reg-province');
      const filterProv = document.getElementById('filter-province');
      AFGHANISTAN_PROVINCES.forEach(prov => {
        regProv.innerHTML += `<option value="${prov}">${prov}</option>`;
        filterProv.innerHTML += `<option value="${prov}">${prov}</option>`;
      });

      // نمایش تاریخ روز به فارسی
      try {
        const todayStr = new Intl.DateTimeFormat('fa-AF', { dateStyle: 'full' }).format(new Date());
        document.getElementById('current-date').textContent = todayStr;
      } catch (e) {
        document.getElementById('current-date').textContent = "سامانه آنلاین املاک";
      }

      applySiteSettings();
      renderAll();
      handleHashChange();
      initCloudStorage();
    });

    window.addEventListener('hashchange', handleHashChange);
  </script>
</body>
</html>
