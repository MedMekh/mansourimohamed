!DOCTYPE html>
<html lang="ar" dir="rtl" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منصوري محمد | حزب جبهة التحرير الوطني - المترشح 13</title>
    
    <!-- خطوط عربية عصرية من Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;800;900&family=Tajawal:wght@400;500;700;800&display=swap" rel="stylesheet">
    
    <!-- مكتبة Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- مكتبة أيقونات Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

    <!-- إعدادات Tailwind المخصصة لألوان شعار حزب جبهة التحرير الوطني -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        cairo: ['Cairo', 'sans-serif'],
                        tajawal: ['Tajawal', 'sans-serif'],
                    },
                    colors: {
                        fln: {
                            green: '#006633',
                            dark: '#004d26',
                            light: '#e6f2ec',
                            red: '#D21034',
                            gold: '#EAB308',
                            goldLight: '#fef9c3',
                        }
                    }
                }
            }
        }
    </script>

    <style>
        body {
            font-family: 'Tajawal', sans-serif;
            background-color: #F8FAFC;
            color: #1e293b;
        }
        h1, h2, h3, h4, .font-heading {
            font-family: 'Cairo', sans-serif;
        }
        /* خلفية مزخرفة مستوحاة من راية وشعار الحزب */
        .hero-bg-pattern {
            background-color: #004d26;
            background-image: 
                radial-gradient(circle at 20% 30%, rgba(234, 179, 8, 0.14) 0%, transparent 45%),
                radial-gradient(circle at 80% 70%, rgba(210, 16, 52, 0.16) 0%, transparent 45%),
                linear-gradient(135deg, rgba(0, 77, 38, 0.94) 0%, rgba(0, 102, 51, 0.90) 100%);
        }
        .sunburst-rays {
            background: repeating-conic-gradient(
                from 0deg,
                rgba(234, 179, 8, 0.06) 0deg 10deg,
                transparent 10deg 20deg
            );
        }
        .ballot-box-check {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
    </style>
</head>
<body class="antialiased selection:bg-fln-green selection:text-white overflow-x-hidden">

    <!-- 1. شريط التنقل العلوي (Top Navigation Bar) -->
    <header class="sticky top-0 z-50 bg-white/95 backdrop-blur-md border-b-4 border-fln-green shadow-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                
                <!-- شعار الحزب واسمه -->
                <a href="#home" class="flex items-center gap-3 group">
                    <div class="relative w-12 h-12 sm:w-14 sm:h-14 rounded-full p-1 bg-white border-2 border-fln-green shadow-sm group-hover:scale-105 transition-transform">
                        <img src="FLN_LOGO.webp" 
                             onerror="this.src='https://placehold.co/100x100/006633/FFFFFF?text=FLN'" 
                             alt="شعار حزب جبهة التحرير الوطني" 
                             class="w-full h-full object-contain rounded-full">
                    </div>
                    <div class="flex flex-col">
                        <span class="font-heading font-extrabold text-fln-dark text-sm sm:text-lg leading-tight">
                            حزب جبهة التحرير الوطني
                        </span>
                        <span class="text-xs text-fln-red font-bold">
                            جبهة التحرير أعطيناك عهداً
                        </span>
                    </div>
                </a>

                <!-- روابط التنقل السريعة (سطح المكتب) -->
                <nav class="hidden lg:flex items-center gap-6 font-heading font-bold text-slate-700">
                    <a href="#home" class="hover:text-fln-green transition-colors py-2">الرئيسية</a>
                    <a href="#vision" class="hover:text-fln-green transition-colors py-2">السيرة والرؤية</a>
                    <a href="#program" class="hover:text-fln-green transition-colors py-2">البرنامج الانتخابي</a>
                    <a href="#how-to-vote" class="hover:text-fln-green transition-colors py-2">طريقة التصويت</a>
                    <a href="#supporter-card" class="hover:text-fln-green transition-colors py-2">بطاقة الدعم</a>
                </nav>

                <!-- شارة القائمة ورقم المترشح البارزة -->
                <div class="flex items-center gap-2 sm:gap-3">
                    <div class="flex items-center bg-fln-light border-2 border-fln-green rounded-xl overflow-hidden shadow-sm">
                        <div class="bg-fln-green text-white px-2.5 sm:px-3 py-1.5 text-center">
                            <span class="block text-[10px] sm:text-xs font-medium opacity-90">القائمة</span>
                            <span class="font-heading font-black text-sm sm:text-base text-fln-gold">01</span>
                        </div>
                        <div class="bg-white text-fln-dark px-2.5 sm:px-3 py-1.5 text-center border-r border-fln-green/20">
                            <span class="block text-[10px] sm:text-xs font-bold text-slate-500">المترشح</span>
                            <span class="font-heading font-black text-sm sm:text-base text-fln-red">13</span>
                        </div>
                    </div>

                    <!-- زر القائمة للهواتف -->
                    <button id="mobile-menu-btn" aria-label="فتح القائمة" class="lg:hidden p-2.5 rounded-xl bg-slate-100 text-fln-dark hover:bg-fln-light focus:outline-none">
                        <i class="fa-solid fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- القائمة المنسدلة للهواتف -->
        <div id="mobile-menu" class="hidden lg:hidden bg-white border-t border-slate-200 px-4 pt-2 pb-4 space-y-1 shadow-lg">
            <a href="#home" class="mobile-link block px-3 py-2.5 rounded-xl font-heading font-bold text-slate-800 hover:bg-fln-light hover:text-fln-green">الرئيسية</a>
            <a href="#vision" class="mobile-link block px-3 py-2.5 rounded-xl font-heading font-bold text-slate-800 hover:bg-fln-light hover:text-fln-green">السيرة والرؤية</a>
            <a href="#program" class="mobile-link block px-3 py-2.5 rounded-xl font-heading font-bold text-slate-800 hover:bg-fln-light hover:text-fln-green">البرنامج الانتخابي</a>
            <a href="#how-to-vote" class="mobile-link block px-3 py-2.5 rounded-xl font-heading font-bold text-slate-800 hover:bg-fln-light hover:text-fln-green">طريقة التصويت</a>
            <a href="#supporter-card" class="mobile-link block px-3 py-2.5 rounded-xl font-heading font-bold text-fln-green bg-fln-light">سجل دعمك الآن</a>
        </div>
    </header>

    <!-- 2. القسم الرئيسي (Hero Section) -->
    <section id="home" class="relative hero-bg-pattern text-white overflow-hidden pt-10 pb-16 lg:py-20">
        <!-- خلفية الراية من صورة FLN.jpeg بتأثير شفاف -->
        <div class="absolute inset-0 opacity-15 pointer-events-none mix-blend-luminosity">
            <img src="FLN.jpeg" 
                 onerror="this.style.display='none'" 
                 alt="" 
                 class="w-full h-full object-cover object-center">
        </div>
        <!-- أشعة ذهبية مستوحاة من شمس الشعار -->
        <div class="absolute inset-0 sunburst-rays pointer-events-none"></div>

        <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-10 lg:gap-12 items-center">
                
                <!-- العمود الأيمن: بيانات المترشح وأرقام ورقة الاقتراع -->
                <div class="lg:col-span-7 text-center lg:text-right space-y-6">
                    <!-- شارة الحزب -->
                    <div class="inline-flex items-center gap-3 bg-white/10 backdrop-blur-md border border-white/25 rounded-full px-4 py-2 shadow-sm">
                        <img src="FLN_LOGO.webp" 
                             onerror="this.src='https://placehold.co/60x60/FFFFFF/006633?text=FLN'" 
                             alt="شعار الحزب" 
                             class="w-7 h-7 rounded-full bg-white p-0.5 object-contain">
                        <span class="font-heading font-bold text-sm sm:text-base text-fln-gold">
                            حزب جبهة التحرير الوطني — "جبهة التحرير أعطيناك عهداً"
                        </span>
                    </div>

                    <!-- اسم المترشح -->
                    <div>
                        <p class="text-emerald-200 font-bold text-lg sm:text-xl mb-1">مرشحكم لخدمة الوطن والمواطن</p>
                        <h1 class="font-heading font-black text-4xl sm:text-6xl lg:text-7xl tracking-tight text-white drop-shadow-md">
                            منصوري محمد
                        </h1>
                    </div>

                    <!-- بطاقات التعريف الانتخابية الرسمية (القائمة 01 | المترشح 13) -->
                    <div class="grid grid-cols-2 gap-4 max-w-lg mx-auto lg:mx-0 pt-2">
                        <!-- بطاقة القائمة رقم 01 -->
                        <div class="bg-white text-slate-900 rounded-2xl p-4 sm:p-5 border-b-8 border-fln-gold shadow-xl relative overflow-hidden">
                            <div class="flex items-center justify-between mb-1">
                                <span class="text-xs sm:text-sm font-extrabold text-fln-green uppercase">رقم القائمة</span>
                                <span class="w-6 h-6 rounded-full bg-fln-light text-fln-green flex items-center justify-center text-xs font-bold">
                                    <i class="fa-solid fa-check"></i>
                                </span>
                            </div>
                            <div class="font-heading font-black text-4xl sm:text-5xl text-fln-dark tracking-wider">
                                01
                            </div>
                            <div class="text-xs font-bold text-slate-500 mt-1">حزب جبهة التحرير الوطني</div>
                        </div>

                        <!-- بطاقة رقم المترشح 13 -->
                        <div class="bg-white text-slate-900 rounded-2xl p-4 sm:p-5 border-b-8 border-fln-red shadow-xl relative overflow-hidden">
                            <div class="flex items-center justify-between mb-1">
                                <span class="text-xs sm:text-sm font-extrabold text-fln-red uppercase">رقم المترشح</span>
                                <span class="w-6 h-6 rounded-full bg-red-50 text-fln-red flex items-center justify-center text-xs font-bold">
                                    <i class="fa-solid fa-star"></i>
                                </span>
                            </div>
                            <div class="font-heading font-black text-4xl sm:text-5xl text-fln-red tracking-wider">
                                13
                            </div>
                            <div class="text-xs font-bold text-slate-500 mt-1">منصوري محمد</div>
                        </div>
                    </div>

                    <!-- أزرار التفاعل الرئيسية -->
                    <div class="flex flex-col sm:flex-row items-center justify-center lg:justify-start gap-4 pt-3">
                        <a href="#supporter-card" class="w-full sm:w-auto inline-flex items-center justify-center gap-3 bg-fln-red hover:bg-red-700 text-white font-heading font-extrabold text-base sm:text-lg px-7 py-4 rounded-2xl shadow-lg shadow-red-950/30 transition-all transform hover:-translate-y-0.5">
                            <i class="fa-solid fa-id-card-clip text-xl"></i>
                            <span>شارك بطاقة الدعم</span>
                        </a>
                        <a href="#program" class="w-full sm:w-auto inline-flex items-center justify-center gap-3 bg-white hover:bg-fln-goldLight text-fln-dark font-heading font-extrabold text-base sm:text-lg px-7 py-4 rounded-2xl shadow-lg transition-all transform hover:-translate-y-0.5">
                            <i class="fa-solid fa-file-lines text-fln-green text-xl"></i>
                            <span>تعرف على البرنامج</span>
                        </a>
                    </div>
                </div>

                <!-- العمود الأيسر: صورة المترشح مؤطرة بألوان الهوية -->
                <div class="lg:col-span-5 flex justify-center">
                    <div class="relative w-full max-w-sm sm:max-w-md">
                        <!-- إطار خلفي زخرفي بالأحمر والأصفر الذهبي -->
                        <div class="absolute -inset-3 bg-gradient-to-tr from-fln-gold via-white to-fln-red rounded-[2rem] opacity-90 blur-[1px]"></div>
                        
                        <!-- حاوية الصورة البيضاء النظيفة -->
                        <div class="relative bg-gradient-to-b from-slate-50 to-slate-200 rounded-[1.85rem] overflow-hidden border-4 border-white shadow-2xl">
                            <!-- شريط علوي يحمل شعار الحزب -->
                            <div class="bg-fln-dark/95 text-white px-4 py-2.5 flex items-center justify-between border-b-2 border-fln-gold">
                                <div class="flex items-center gap-2">
                                    <img src="FLN_LOGO.webp" 
                                         onerror="this.src='https://placehold.co/50x50/006633/FFFFFF?text=FLN'" 
                                         alt="شعار جبهة التحرير الوطني" 
                                         class="w-7 h-7 rounded-full bg-white p-0.5 object-contain">
                                    <span class="font-heading font-bold text-xs sm:text-sm">حزب جبهة التحرير الوطني</span>
                                </div>
                                <span class="bg-fln-gold text-fln-dark font-heading font-black text-xs px-2.5 py-0.5 rounded-full">
                                    قائمة 01
                                </span>
                            </div>

                            <!-- صورة المترشح منصوري محمد -->
                            <div class="pt-4 px-4 bg-white flex justify-center items-end">
                                <img src="mansouri mohamed.jpeg" 
                                     onerror="this.src='https://placehold.co/500x600/e2e8f0/004d26?text=%D9%85%D9%86%D8%B5%D9%88%D8%B1%D9%8A+%D9%85%D8%AD%D9%85%D8%AF'" 
                                     alt="المترشح منصوري محمد - قائمة 01 رقم 13" 
                                     class="w-full h-auto max-h-[430px] object-contain object-bottom">
                            </div>

                            <!-- شريط سفلي باسم المترشح ورقمه -->
                            <div class="bg-fln-green text-white px-5 py-3.5 flex items-center justify-between border-t-4 border-fln-red">
                                <div>
                                    <p class="text-xs text-emerald-200 font-medium">المترشح</p>
                                    <p class="font-heading font-black text-lg sm:text-xl">منصوري محمد</p>
                                </div>
                                <div class="bg-white text-fln-red font-heading font-black text-2xl px-4 py-1.5 rounded-xl shadow-inner border-2 border-fln-gold">
                                    13
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- 3. كلمة المترشح ورؤيته (Candidate Profile & Vision) -->
    <section id="vision" class="py-16 sm:py-20 bg-white">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="bg-slate-50 rounded-3xl border border-slate-200 shadow-xl overflow-hidden">
                <div class="grid grid-cols-1 lg:grid-cols-12">
                    
                    <!-- الشريط الجانبي التعريفي -->
                    <div class="lg:col-span-4 bg-fln-dark text-white p-8 sm:p-10 flex flex-col justify-between relative overflow-hidden">
                        <div class="relative z-10 space-y-6">
                            <div class="w-16 h-16 bg-white rounded-2xl p-2 shadow-md">
                                <img src="FLN_LOGO.webp" 
                                     onerror="this.src='https://placehold.co/80x80/006633/FFFFFF?text=FLN'" 
                                     alt="شعار الحزب" 
                                     class="w-full h-full object-contain">
                            </div>
                            <div>
                                <span class="inline-block bg-fln-red text-white text-xs font-bold px-3 py-1 rounded-full mb-3">
                                    التزام ومسؤولية
                                </span>
                                <h2 class="font-heading font-black text-2xl sm:text-3xl leading-snug">
                                    كلمة المترشح ورؤيته
                                </h2>
                                <p class="text-emerald-200 text-sm mt-2 font-medium">
                                    منصوري محمد — القائمة رقم 01، المترشح رقم 13
                                </p>
                            </div>
                            <div class="border-t border-white/15 pt-5 space-y-3 text-sm">
                                <div class="flex items-center gap-3">
                                    <i class="fa-solid fa-shield-halved text-fln-gold text-lg"></i>
                                    <span>الوفاء لثوابت الأمة وقيم نوفمبر</span>
                                </div>
                                <div class="flex items-center gap-3">
                                    <i class="fa-solid fa-handshake-angle text-fln-gold text-lg"></i>
                                    <span>خدمة المواطن بصدق ونزاهة</span>
                                </div>
                                <div class="flex items-center gap-3">
                                    <i class="fa-solid fa-chart-line text-fln-gold text-lg"></i>
                                    <span>دفع عجلة التنمية المحلية المستدامة</span>
                                </div>
                            </div>
                        </div>
                        <!-- دائرة زخرفية -->
                        <div class="absolute -bottom-16 -left-16 w-48 h-48 rounded-full bg-fln-green/50 pointer-events-none"></div>
                    </div>

                    <!-- نص كلمة المترشح -->
                    <div class="lg:col-span-8 p-8 sm:p-12 flex flex-col justify-center space-y-6">
                        <div class="flex items-center gap-2 text-fln-green font-heading font-extrabold text-sm">
                            <span class="w-8 h-1 bg-fln-red rounded-full"></span>
                            <span>رسالة إلى بنات وأبناء دائرتنا الانتخابية</span>
                        </div>

                        <blockquote class="text-slate-700 text-lg sm:text-xl leading-relaxed font-medium space-y-4">
                            <p>
                                "بسم الله الرحمن الرحيم، أتوجه إليكم بكل تقدير واعتزاز مترشحاً ضمن قائمة <strong class="text-fln-green font-extrabold">حزب جبهة التحرير الوطني (القائمة رقم 01 — المترشح رقم 13)</strong>، حاملاً معي تطلعاتكم وانشغالاتكم اليومية، ومؤمناً بأن العمل الميداني الجاد هو السبيل الوحيد لتحقيق التغيير الإيجابي."
                            </p>
                            <p>
                                "إن التزامنا اليوم نابع من مسؤولية وطنية وأخلاقية تجاه شبابنا وعائلاتنا، من أجل تحسين الإطار المعيشي، وتطوير المرافق العمومية، ومرافقة المشاريع التنموية، مع فتح أبواب الحوار والتواصل الدائم مع كل المواطنين دون إقصاء."
                            </p>
                        </blockquote>

                        <div class="pt-4 border-t border-slate-200 flex flex-wrap items-center justify-between gap-4">
                            <div>
                                <p class="font-heading font-black text-xl text-fln-dark">منصوري محمد</p>
                                <p class="text-sm text-slate-500 font-bold">مرشح حزب جبهة التحرير الوطني • قائمة 01 • رقم 13</p>
                            </div>
                            <div class="flex items-center gap-2 bg-fln-light px-4 py-2 rounded-xl border border-fln-green/30">
                                <span class="w-2.5 h-2.5 rounded-full bg-fln-green animate-pulse"></span>
                                <span class="text-fln-dark font-heading font-bold text-sm">معاً نصنع المستقبل</span>
                            </div>
                        </div>
                    </div>

                </div>
            </div>
        </div>
    </section>

    <!-- 4. محاور البرنامج الانتخابي (Electoral Program Pillars) -->
    <section id="program" class="py-16 sm:py-20 bg-slate-100/80 border-y border-slate-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            
            <!-- عنوان القسم -->
            <div class="text-center max-w-3xl mx-auto mb-14 space-y-3">
                <span class="inline-block bg-fln-green/10 text-fln-green font-heading font-extrabold text-sm px-4 py-1.5 rounded-full border border-fln-green/20">
                    رؤية عملية قابلة للتجسيد
                </span>
                <h2 class="font-heading font-black text-3xl sm:text-4xl text-fln-dark">
                    محاور البرنامج الانتخابي
                </h2>
                <p class="text-slate-600 text-base sm:text-lg">
                    أربعة محاور أساسية نلتزم بالدفاع عنها ومتابعة تنفيذها ميدانياً لخدمة المواطن والارتقاء بالتنمية المحلية.
                </p>
            </div>

            <!-- شبكة المحاور الأربعة -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 sm:gap-8">
                
                <!-- المحور 1 -->
                <div class="bg-white rounded-3xl p-7 shadow-md hover:shadow-xl transition-all border-t-4 border-fln-green flex flex-col justify-between group">
                    <div>
                        <div class="w-14 h-14 rounded-2xl bg-fln-light text-fln-green flex items-center justify-center text-2xl mb-6 group-hover:bg-fln-green group-hover:text-white transition-colors">
                            <i class="fa-solid fa-city"></i>
                        </div>
                        <span class="text-xs font-extrabold text-fln-green bg-fln-light px-2.5 py-1 rounded-md">المحور الأول</span>
                        <h3 class="font-heading font-extrabold text-xl text-slate-900 mt-3 mb-3 leading-snug">
                            التنمية المحلية وتحسين الإطار المعيشي
                        </h3>
                        <p class="text-slate-600 text-sm leading-relaxed">
                            تهيئة الأحياء السكنية، فك العزلة عن المناطق الريفية، تحسين شبكات الطرق والإنارة العمومية، وضمان التزود المنتظم بالماء الشروب والغاز والكهرباء.
                        </p>
                    </div>
                    <div class="mt-6 pt-4 border-t border-slate-100 flex items-center text-xs font-bold text-fln-green">
                        <i class="fa-solid fa-circle-check ml-2"></i>
                        <span>أولوية البنية التحتية</span>
                    </div>
                </div>

                <!-- المحور 2 -->
                <div class="bg-white rounded-3xl p-7 shadow-md hover:shadow-xl transition-all border-t-4 border-fln-red flex flex-col justify-between group">
                    <div>
                        <div class="w-14 h-14 rounded-2xl bg-red-50 text-fln-red flex items-center justify-center text-2xl mb-6 group-hover:bg-fln-red group-hover:text-white transition-colors">
                            <i class="fa-solid fa-briefcase"></i>
                        </div>
                        <span class="text-xs font-extrabold text-fln-red bg-red-50 px-2.5 py-1 rounded-md">المحور الثاني</span>
                        <h3 class="font-heading font-extrabold text-xl text-slate-900 mt-3 mb-3 leading-snug">
                            دعم الشباب والتشغيل والمقاولاتية
                        </h3>
                        <p class="text-slate-600 text-sm leading-relaxed">
                            مرافقة حاملي المشاريع والمؤسسات الناشئة، تسهيل الولوج إلى آليات الدعم والتمويل، وتوفير فضاءات رياضية وثقافية لائقة لتفجير طاقات الشباب.
                        </p>
                    </div>
                    <div class="mt-6 pt-4 border-t border-slate-100 flex items-center text-xs font-bold text-fln-red">
                        <i class="fa-solid fa-circle-check ml-2"></i>
                        <span>تمكين الطاقات الشابة</span>
                    </div>
                </div>

                <!-- المحور 3 -->
                <div class="bg-white rounded-3xl p-7 shadow-md hover:shadow-xl transition-all border-t-4 border-fln-gold flex flex-col justify-between group">
                    <div>
                        <div class="w-14 h-14 rounded-2xl bg-yellow-50 text-amber-600 flex items-center justify-center text-2xl mb-6 group-hover:bg-fln-gold group-hover:text-fln-dark transition-colors">
                            <i class="fa-solid fa-heart-pulse"></i>
                        </div>
                        <span class="text-xs font-extrabold text-amber-700 bg-yellow-50 px-2.5 py-1 rounded-md">المحور الثالث</span>
                        <h3 class="font-heading font-extrabold text-xl text-slate-900 mt-3 mb-3 leading-snug">
                            ترقية الخدمات العمومية والصحة والتعليم
                        </h3>
                        <p class="text-slate-600 text-sm leading-relaxed">
                            العمل على تحسين ظروف التمدرس والنقل المدرسي، دعم المراكز الصحية الجوارية بالتجهيزات الضرورية، وتقريب الإدارة من المواطن ورقمنتها.
                        </p>
                    </div>
                    <div class="mt-6 pt-4 border-t border-slate-100 flex items-center text-xs font-bold text-amber-700">
                        <i class="fa-solid fa-circle-check ml-2"></i>
                        <span>جودة الصحة والتعليم</span>
                    </div>
                </div>

                <!-- المحور 4 -->
                <div class="bg-white rounded-3xl p-7 shadow-md hover:shadow-xl transition-all border-t-4 border-fln-dark flex flex-col justify-between group">
                    <div>
                        <div class="w-14 h-14 rounded-2xl bg-fln-light text-fln-dark flex items-center justify-center text-2xl mb-6 group-hover:bg-fln-dark group-hover:text-white transition-colors">
                            <i class="fa-solid fa-comments"></i>
                        </div>
                        <span class="text-xs font-extrabold text-fln-dark bg-fln-light px-2.5 py-1 rounded-md">المحور الرابع</span>
                        <h3 class="font-heading font-extrabold text-xl text-slate-900 mt-3 mb-3 leading-snug">
                            الإصغاء الدائم للمواطن والشفافية
                        </h3>
                        <p class="text-slate-600 text-sm leading-relaxed">
                            تنظيم لقاءات دورية مفتوحة مع المواطنين وفعاليات المجتمع المدني، نقل الانشغالات بأمانة إلى الهيئات المعنية، وترسيخ الشفافية في المتابعة.
                        </p>
                    </div>
                    <div class="mt-6 pt-4 border-t border-slate-100 flex items-center text-xs font-bold text-fln-dark">
                        <i class="fa-solid fa-circle-check ml-2"></i>
                        <span>تواصل مستمر ومفتوح</span>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- 5. دليل "كيف تصوت؟" التفاعلي (Interactive How to Vote Guide) -->
    <section id="how-to-vote" class="py-16 sm:py-20 bg-white">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-12 space-y-3">
                <span class="inline-block bg-red-50 text-fln-red font-heading font-extrabold text-sm px-4 py-1.5 rounded-full border border-red-200">
                    صوتك أمانة ومسؤولية
                </span>
                <h2 class="font-heading font-black text-3xl sm:text-4xl text-fln-dark">
                    كيف تصوت يوم الاقتراع؟
                </h2>
                <p class="text-slate-600 text-base sm:text-lg">
                    خطوات بسيطة لضمان احتساب صوتك لصالح قائمة <strong class="text-fln-green">حزب جبهة التحرير الوطني (01)</strong> والمترشح <strong class="text-fln-red">منصوري محمد (13)</strong>.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
                
                <!-- خطوات التصويت -->
                <div class="lg:col-span-5 space-y-4">
                    <div class="flex items-start gap-4 p-5 rounded-2xl bg-slate-50 border border-slate-200">
                        <div class="w-10 h-10 rounded-xl bg-fln-green text-white font-heading font-black text-lg flex items-center justify-center shrink-0">
                            1
                        </div>
                        <div>
                            <h3 class="font-heading font-extrabold text-lg text-slate-900">اسحب ورقة القائمة رقم 01</h3>
                            <p class="text-sm text-slate-600 mt-1">
                                داخل مكتب التصويت، اختر ورقة التصويت الخاصة بـ <strong>حزب جبهة التحرير الوطني</strong> الحاملة للرقم <strong>01</strong>.
                            </p>
                        </div>
                    </div>

                    <div class="flex items-start gap-4 p-5 rounded-2xl bg-fln-light/60 border-2 border-fln-green">
                        <div class="w-10 h-10 rounded-xl bg-fln-red text-white font-heading font-black text-lg flex items-center justify-center shrink-0">
                            2
                        </div>
                        <div>
                            <h3 class="font-heading font-extrabold text-lg text-fln-dark">أشّر على المترشح رقم 13</h3>
                            <p class="text-sm text-slate-700 mt-1">
                                داخل المعزل، ضع علامة (<strong>✓</strong> أو <strong>✕</strong>) بوضوح داخل المربع المقابل لاسم المترشح <strong>منصوري محمد — رقم 13</strong>.
                            </p>
                        </div>
                    </div>

                    <div class="flex items-start gap-4 p-5 rounded-2xl bg-slate-50 border border-slate-200">
                        <div class="w-10 h-10 rounded-xl bg-fln-gold text-fln-dark font-heading font-black text-lg flex items-center justify-center shrink-0">
                            3
                        </div>
                        <div>
                            <h3 class="font-heading font-extrabold text-lg text-slate-900">ضع الورقة في الظرف ثم الصندوق</h3>
                            <p class="text-sm text-slate-600 mt-1">
                                اطوِ ورقة التصويت وضعها داخل الظرف المخصص، ثم ضعه في صندوق الاقتراع.
                            </p>
                        </div>
                    </div>
                </div>

                <!-- محاكاة تفاعلية لورقة الاقتراع -->
                <div class="lg:col-span-7">
                    <div class="bg-slate-100 p-4 sm:p-8 rounded-3xl border-2 border-slate-300 shadow-inner">
                        <div class="bg-white rounded-2xl border-2 border-slate-800 shadow-lg overflow-hidden max-w-md mx-auto">
                            
                            <!-- ترويسة ورقة الاقتراع -->
                            <div class="bg-fln-green text-white p-4 flex items-center justify-between border-b-2 border-slate-800">
                                <div class="flex items-center gap-3">
                                    <img src="FLN_LOGO.webp" 
                                         onerror="this.src='https://placehold.co/60x60/FFFFFF/006633?text=FLN'" 
                                         alt="شعار الحزب" 
                                         class="w-11 h-11 rounded-full bg-white p-0.5 object-contain">
                                    <div>
                                        <span class="block text-xs text-emerald-100">قائمة المترشحين</span>
                                        <h4 class="font-heading font-black text-base sm:text-lg">حزب جبهة التحرير الوطني</h4>
                                    </div>
                                </div>
                                <div class="bg-white text-fln-dark px-3 py-1.5 rounded-xl text-center border-2 border-fln-gold">
                                    <span class="block text-[10px] font-bold">رقم القائمة</span>
                                    <span class="font-heading font-black text-2xl leading-none">01</span>
                                </div>
                            </div>

                            <!-- قائمة المترشحين المحاكاة -->
                            <div class="p-1 space-y-2.5 bg-slate-50">
                        

                                <!-- خانة المترشح منصوري محمد رقم 13 التفاعلية -->
                                <div id="ballot-row-13" onclick="toggleBallotMark()" class="cursor-pointer flex items-center justify-between px-4 py-3.5 bg-emerald-50 hover:bg-emerald-100 rounded-xl border-2 border-fln-green shadow-sm transition-all">
                                    <div class="flex items-center gap-3">
                                        <span class="w-8 h-8 rounded-lg bg-fln-red text-white font-heading font-black text-base flex items-center justify-center">
                                            13
                                        </span>
                                        <div>
                                            <span class="font-heading font-black text-base sm:text-lg text-slate-900 block">منصوري محمد</span>
                                            <span class="text-xs font-bold text-fln-green">اضغط للتأشير وتجربة التصويت</span>
                                        </div>
                                    </div>
                                    <!-- مربع التأشير -->
                                    <div id="ballot-checkbox" class="ballot-box-check w-10 h-10 bg-white border-2 border-slate-800 rounded-lg flex items-center justify-center text-fln-red text-2xl font-black shadow-inner">
                                        <i id="ballot-check-icon" class="fa-solid fa-check scale-100 transition-transform"></i>
                                    </div>
                                </div>

                                <div class="flex items-center justify-between px-3 py-2 bg-white rounded-lg border border-slate-200 opacity-50 text-xs">
                                    <span class="font-bold">14 — مترشح القائمة</span>
                                    <span class="w-6 h-6 border border-slate-400 rounded"></span>
                                </div>
                            </div>

                            <!-- تذييل ورقة الاقتراع -->
                            <div class="bg-slate-800 text-white text-center py-2.5 px-4 text-xs font-bold">
                                <span id="ballot-status-text" class="text-fln-gold">
                                    <i class="fa-solid fa-circle-check ml-1"></i> تم التأشير بنجاح على المترشح رقم 13 (منصوري محمد)
                                </span>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- 6. مولد بطاقة الدعم الرقمية التفاعلية (Interactive Supporter Card Generator) -->
    <section id="supporter-card" class="py-16 sm:py-20 hero-bg-pattern text-white relative overflow-hidden">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            
            <div class="text-center max-w-3xl mx-auto mb-12 space-y-3">
                <span class="inline-block bg-fln-gold text-fln-dark font-heading font-black text-sm px-4 py-1.5 rounded-full">
                    كن شريكاً في الحملة
                </span>
                <h2 class="font-heading font-black text-3xl sm:text-4xl">
                    سجل دعمك وأنشئ بطاقتك الرقمية
                </h2>
                <p class="text-emerald-100 text-base sm:text-lg">
                    أدخل اسمك وبلديتك لإنشاء بطاقة مساندة رسمية للمترشح <strong>منصوري محمد</strong> ومشاركتها مع عائلتك وأصدقائك.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
                
                <!-- نموذج إدخال بيانات الداعم -->
                <div class="lg:col-span-5 bg-white text-slate-900 rounded-3xl p-6 sm:p-8 shadow-2xl border-t-8 border-fln-gold">
                    <h3 class="font-heading font-black text-xl text-fln-dark mb-5">
                        بيانات بطاقة المساندة
                    </h3>
                    
                    <form id="supporter-form" class="space-y-4" onsubmit="event.preventDefault(); updateSupporterCard();">
                        <div>
                            <label for="supporter-name" class="block text-sm font-bold text-slate-700 mb-1.5">
                                الاسم الكامل أو اللقب
                            </label>
                            <input type="text" id="supporter-name" placeholder="مثال: أحمد بن علي" maxlength="35"
                                   oninput="updateSupporterCard()"
                                   class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-fln-green focus:ring-2 focus:ring-fln-green/20 outline-none font-bold text-slate-800">
                        </div>

                        <div>
                            <label for="supporter-city" class="block text-sm font-bold text-slate-700 mb-1.5">
                                البلدية / الحي (اختياري)
                            </label>
                            <input type="text" id="supporter-city" placeholder="مثال: بلدية الجلفة" maxlength="35"
                                   oninput="updateSupporterCard()"
                                   class="w-full px-4 py-3 rounded-xl border border-slate-300 focus:border-fln-green focus:ring-2 focus:ring-fln-green/20 outline-none font-bold text-slate-800">
                        </div>

                        <div class="pt-2 space-y-3">
                            <button type="button" onclick="copySupportMessage()" 
                                    class="w-full bg-fln-green hover:bg-fln-dark text-white font-heading font-extrabold py-3.5 px-5 rounded-xl shadow-md transition-all flex items-center justify-center gap-2">
                                <i class="fa-solid fa-copy"></i>
                                <span>نسخ رسالة الدعم للمشاركة</span>
                            </button>

                            <button type="button" onclick="downloadCardCanvas()" 
                                    class="w-full bg-fln-red hover:bg-red-700 text-white font-heading font-extrabold py-3.5 px-5 rounded-xl shadow-md transition-all flex items-center justify-center gap-2">
                                <i class="fa-solid fa-download"></i>
                                <span>تحميل بطاقة الدعم كصورة</span>
                            </button>
                        </div>

                        <!-- إشعار تفاعلي بدل alert() -->
                        <div id="feedback-toast" class="hidden p-3 rounded-xl bg-emerald-50 border border-fln-green text-fln-dark text-sm font-bold text-center">
                        </div>
                    </form>
                </div>

                <!-- معاينة بطاقة الدعم المباشرة -->
                <div class="lg:col-span-7 flex justify-center">
                    <div id="digital-badge-preview" class="w-full max-w-lg bg-white text-slate-900 rounded-3xl overflow-hidden shadow-2xl border-4 border-fln-gold">
                        
                        <!-- رأس البطاقة -->
                        <div class="bg-fln-dark text-white p-4 sm:p-5 flex items-center justify-between border-b-4 border-fln-red">
                            <div class="flex items-center gap-3">
                                <img src="FLN_LOGO.webp" 
                                     onerror="this.src='https://placehold.co/60x60/FFFFFF/006633?text=FLN'" 
                                     alt="شعار الحزب" 
                                     class="w-12 h-12 rounded-full bg-white p-0.5 object-contain">
                                <div>
                                    <span class="block text-xs text-fln-gold font-bold">حزب جبهة التحرير الوطني</span>
                                    <span class="font-heading font-black text-base sm:text-lg">بطاقة مساندة رسمية</span>
                                </div>
                            </div>
                            <div class="flex items-center gap-1.5">
                                <span class="bg-fln-green border border-white/30 text-white text-xs font-black px-2.5 py-1.5 rounded-lg">
                                    قائمة 01
                                </span>
                                <span class="bg-fln-red text-white text-xs font-black px-2.5 py-1.5 rounded-lg">
                                    رقم 13
                                </span>
                            </div>
                        </div>

                        <!-- محتوى البطاقة -->
                        <div class="p-5 sm:p-6 bg-gradient-to-br from-white via-slate-50 to-emerald-50">
                            <div class="flex flex-col sm:flex-row items-center gap-5">
                                <!-- صورة مصغرة للمترشح -->
                                <div class="w-28 h-32 sm:w-32 sm:h-36 rounded-2xl overflow-hidden border-2 border-fln-green bg-white shrink-0 shadow-md">
                                    <img src="mansouri mohamed.jpeg" 
                                         onerror="this.src='https://placehold.co/200x240/e2e8f0/004d26?text=%D9%85%D9%86%D8%B5%D9%88%D8%B1%D9%8A'" 
                                         alt="منصوري محمد" 
                                         class="w-full h-full object-cover object-top">
                                </div>

                                <!-- نص المساندة -->
                                <div class="text-center sm:text-right space-y-2 flex-1">
                                    <div class="inline-block bg-fln-light text-fln-green text-xs font-extrabold px-3 py-1 rounded-full">
                                        أنا أدعم وأساند
                                    </div>
                                    <h4 class="font-heading font-black text-2xl text-fln-dark">
                                        المترشح منصوري محمد
                                    </h4>
                                    <p class="text-sm text-slate-600 font-medium">
                                        مرشح حزب جبهة التحرير الوطني — القائمة رقم <strong class="text-fln-green">01</strong>، رقم المترشح <strong class="text-fln-red">13</strong>.
                                    </p>

                                    <div class="pt-2 mt-2 border-t border-slate-200">
                                        <span class="text-xs text-slate-500 block">المساند(ة):</span>
                                        <p id="preview-supporter-name" class="font-heading font-extrabold text-lg text-fln-red">
                                            مواطن(ة) داعم(ة) للتنمية
                                        </p>
                                        <p id="preview-supporter-city" class="text-xs font-bold text-slate-600">
                                            معاً من أجل مستقبل أفضل
                                        </p>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <!-- شريط ختامي للبطاقة -->
                        <div class="bg-fln-green text-white px-5 py-2.5 text-center text-xs sm:text-sm font-heading font-bold">
                            "جبهة التحرير أعطيناك عهداً" • نصوّت للقائمة 01 — رقم 13
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- 7. تذييل الصفحة (Footer) -->
    <footer class="bg-slate-950 text-slate-300 border-t-4 border-fln-green">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="flex flex-col md:flex-row items-center justify-between gap-8 pb-8 border-b border-slate-800">
                
                <!-- معلومات الحزب والمترشح -->
                <div class="flex items-center gap-4 text-center md:text-right">
                    <img src="FLN_LOGO.webp" 
                         onerror="this.src='https://placehold.co/80x80/006633/FFFFFF?text=FLN'" 
                         alt="شعار حزب جبهة التحرير الوطني" 
                         class="w-16 h-16 rounded-full bg-white p-1 object-contain shrink-0">
                    <div>
                        <h3 class="font-heading font-black text-xl text-white">حزب جبهة التحرير الوطني</h3>
                        <p class="text-fln-gold font-bold text-sm mt-0.5">الحملة الانتخابية للمترشح منصوري محمد</p>
                    </div>
                </div>

                <!-- أرقام التعريف الرسمية -->
                <div class="flex items-center gap-4">
                    <div class="bg-slate-900 border border-fln-green/50 px-5 py-3 rounded-2xl text-center">
                        <span class="block text-xs text-slate-400">رقم القائمة</span>
                        <span class="font-heading font-black text-2xl text-fln-gold">01</span>
                    </div>
                    <div class="bg-slate-900 border border-fln-red/50 px-5 py-3 rounded-2xl text-center">
                        <span class="block text-xs text-slate-400">رقم المترشح</span>
                        <span class="font-heading font-black text-2xl text-fln-red">13</span>
                    </div>
                </div>
            </div>

            <div class="pt-6 flex flex-col sm:flex-row items-center justify-between gap-4 text-xs text-slate-400">
                <p>جميع الحقوق محفوظة © الحملة الانتخابية للمترشح منصوري محمد — حزب جبهة التحرير الوطني.</p>
                <div class="flex items-center gap-4">
                    <a href="#home" class="hover:text-white transition-colors">الرئيسية</a>
                    <a href="#vision" class="hover:text-white transition-colors">الرؤية</a>
                    <a href="#program" class="hover:text-white transition-colors">البرنامج</a>
                    <a href="#how-to-vote" class="hover:text-white transition-colors">طريقة التصويت</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- السكربتات التفاعلية -->
    <script>
        // التحكم في قائمة الهاتف المحمول
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        const mobileLinks = document.querySelectorAll('.mobile-link');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        mobileLinks.forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // تفاعل محاكاة ورقة الاقتراع (التأشير على رقم 13)
        let isMarked = true;
        function toggleBallotMark() {
            isMarked = !isMarked;
            const icon = document.getElementById('ballot-check-icon');
            const statusText = document.getElementById('ballot-status-text');
            const row = document.getElementById('ballot-row-13');

            if (isMarked) {
                icon.classList.remove('scale-0');
                icon.classList.add('scale-100');
                row.classList.add('bg-emerald-50', 'border-fln-green');
                row.classList.remove('bg-white', 'border-slate-300');
                statusText.innerHTML = '<i class="fa-solid fa-circle-check ml-1"></i> تم التأشير بنجاح على المترشح رقم 13 (منصوري محمد)';
                statusText.className = 'text-fln-gold';
            } else {
                icon.classList.remove('scale-100');
                icon.classList.add('scale-0');
                row.classList.remove('bg-emerald-50', 'border-fln-green');
                row.classList.add('bg-white', 'border-slate-300');
                statusText.innerHTML = '<i class="fa-solid fa-hand-pointer ml-1"></i> اضغط على مربع المترشح رقم 13 لوضع علامة التصويت';
                statusText.className = 'text-slate-300';
            }
        }

        // تحديث بطاقة الدعم الرقمية مباشرة
        function updateSupporterCard() {
            const nameInput = document.getElementById('supporter-name').value.trim();
            const cityInput = document.getElementById('supporter-city').value.trim();

            const previewName = document.getElementById('preview-supporter-name');
            const previewCity = document.getElementById('preview-supporter-city');

            previewName.textContent = nameInput ? nameInput : 'مواطن(ة) داعم(ة) للتنمية';
            previewCity.textContent = cityInput ? cityInput : 'معاً من أجل مستقبل أفضل';
        }

        // عرض إشعار مخصص بدلاً من alert()
        function showToast(message) {
            const toast = document.getElementById('feedback-toast');
            toast.textContent = message;
            toast.classList.remove('hidden');
            setTimeout(() => {
                toast.classList.add('hidden');
            }, 4000);
        }

        // نسخ رسالة الدعم باستخدام document.execCommand('copy') للتوافق التام
        function copySupportMessage() {
            const nameInput = document.getElementById('supporter-name').value.trim();
            const cityInput = document.getElementById('supporter-city').value.trim();
            
            const sender = nameInput ? `أنا ${nameInput}${cityInput ? ' من ' + cityInput : ''}، ` : '';
            const textToCopy = `${sender}أعلن دعمي ومساندتي للمترشح "منصوري محمد" عن حزب جبهة التحرير الوطني — القائمة رقم 01، المترشح رقم 13. معاً لخدمة الوطن والمواطن! 🇩🇿`;

            const tempTextarea = document.createElement('textarea');
            tempTextarea.value = textToCopy;
            tempTextarea.style.position = 'fixed';
            tempTextarea.style.opacity = '0';
            document.body.appendChild(tempTextarea);
            tempTextarea.select();

            try {
                document.execCommand('copy');
                showToast('تم نسخ رسالة الدعم بنجاح! يمكنك لصقها ومشاركتها الآن.');
            } catch (err) {
                showToast('تعذر النسخ التلقائي، يرجى تحديد النص ونسخه يدوياً.');
            }
            document.body.removeChild(tempTextarea);
        }

        // توليد وتحميل بطاقة الدعم كصورة PNG عبر Canvas
        function downloadCardCanvas() {
            const nameInput = document.getElementById('supporter-name').value.trim() || 'مواطن(ة) داعم(ة) للتنمية';
            const cityInput = document.getElementById('supporter-city').value.trim() || 'معاً من أجل مستقبل أفضل';

            const canvas = document.createElement('canvas');
            canvas.width = 900;
            canvas.height = 520;
            const ctx = canvas.getContext('2d');

            // الخلفية الأساسية
            ctx.fillStyle = '#004d26';
            ctx.fillRect(0, 0, canvas.width, canvas.height);

            // إطار ذهبي خارجي
            ctx.strokeStyle = '#EAB308';
            ctx.lineWidth = 14;
            ctx.strokeRect(14, 14, canvas.width - 28, canvas.height - 28);

            // بطاقة داخلية بيضاء
            ctx.fillStyle = '#FFFFFF';
            ctx.beginPath();
            ctx.roundRect(45, 45, canvas.width - 90, canvas.height - 90, 24);
            ctx.fill();

            // شريط علوي أخضر
            ctx.fillStyle = '#006633';
            ctx.fillRect(45, 45, canvas.width - 90, 85);

            // خط أحمر فاصل
            ctx.fillStyle = '#D21034';
            ctx.fillRect(45, 130, canvas.width - 90, 8);

            // نصوص البطاقة
            ctx.direction = 'rtl';
            ctx.textAlign = 'right';

            // عنوان الحزب
            ctx.fillStyle = '#FFFFFF';
            ctx.font = 'bold 28px Cairo, sans-serif';
            ctx.fillText('حزب جبهة التحرير الوطني', canvas.width - 80, 98);

            // شارة القائمة والرقم في الأعلى يسار
            ctx.fillStyle = '#EAB308';
            ctx.font = 'bold 24px Cairo, sans-serif';
            ctx.textAlign = 'left';
            ctx.fillText('القائمة 01  |  المترشح 13', 80, 98);

            // محتوى الوسط
            ctx.textAlign = 'center';
            ctx.fillStyle = '#006633';
            ctx.font = 'bold 24px Tajawal, sans-serif';
            ctx.fillText('بطاقة مساندة رسمية للمترشح', canvas.width / 2, 195);

            ctx.fillStyle = '#004d26';
            ctx.font = '900 48px Cairo, sans-serif';
            ctx.fillText('منصوري محمد', canvas.width / 2, 255);

            // خط فاصل
            ctx.strokeStyle = '#e2e8f0';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.moveTo(180, 285);
            ctx.lineTo(canvas.width - 180, 285);
            ctx.stroke();

            // اسم الداعم
            ctx.fillStyle = '#64748b';
            ctx.font = 'bold 20px Tajawal, sans-serif';
            ctx.fillText('المساند(ة):', canvas.width / 2, 325);

            ctx.fillStyle = '#D21034';
            ctx.font = 'bold 34px Cairo, sans-serif';
            ctx.fillText(nameInput, canvas.width / 2, 370);

            ctx.fillStyle = '#334155';
            ctx.font = 'bold 22px Tajawal, sans-serif';
            ctx.fillText(cityInput, canvas.width / 2, 410);

            // تذييل البطاقة
            ctx.fillStyle = '#004d26';
            ctx.font = 'bold 20px Cairo, sans-serif';
            ctx.fillText('جبهة التحرير أعطيناك عهداً • نصوّت للقائمة 01 — رقم 13', canvas.width / 2, 455);

            // تنزيل الصورة
            try {
                const link = document.createElement('a');
                link.download = 'بطاقة-دعم-منصوري-محمد-13.png';
                link.href = canvas.toDataURL('image/png');
                link.click();
                showToast('تم تحميل بطاقة الدعم بنجاح!');
            } catch (e) {
                showToast('تم تجهيز البطاقة بنجاح.');
            }
        }
    </script>
</body>
</html>
