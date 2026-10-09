```html
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>إبراهيم ستور | Ibrahim Store - لأحدث صيحات الموضة والملابس</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brand: {
                            gold: '#D4AF37',
                            dark: '#121212',
                            gray: '#1E1E1E',
                            accent: '#F39C12',
                            light: '#F8F9FA'
                        }
                    },
                    fontFamily: {
                        sans: ['Cairo', 'sans-serif']
                    }
                }
            }
        }
    </script>
    <!-- Google Fonts: Cairo -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;900&display=swap" rel="stylesheet">
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        body {
            font-family: 'Cairo', sans-serif;
            background-color: #0d0d0d;
            color: #f3f4f6;
            scroll-behavior: smooth;
        }
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #121212;
        }
        ::-webkit-scrollbar-thumb {
            background: #333;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #D4AF37;
        }
        .glass-card {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }
        .glass-nav {
            background: rgba(18, 18, 18, 0.85);
            backdrop-filter: blur(12px);
        }
        .gold-gradient-text {
            background: linear-gradient(135deg, #FFF 30%, #D4AF37 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .gold-btn {
            background: linear-gradient(135deg, #D4AF37 0%, #AA7C11 100%);
            transition: all 0.3s ease;
        }
        .gold-btn:hover {
            box-shadow: 0 0 20px rgba(212, 175, 55, 0.4);
            transform: translateY(-2px);
        }
    </style>
</head>
<body class="bg-black text-gray-100 min-h-screen flex flex-col justify-between overflow-x-hidden">

    <!-- Header / Navbar -->
    <header class="fixed top-0 right-0 left-0 z-40 glass-nav border-b border-zinc-800 transition-all duration-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                
                <!-- Logo -->
                <div class="flex-shrink-0">
                    <a href="#" class="flex items-center gap-2">
                        <span class="w-10 h-10 rounded-full gold-btn flex items-center justify-center text-black font-black text-xl shadow-lg">IS</span>
                        <div class="flex flex-col">
                            <span class="text-xl sm:text-2xl font-black tracking-wider gold-gradient-text">إبراهيم ستور</span>
                            <span class="text-[10px] tracking-widest text-zinc-400 uppercase -mt-1 font-semibold">Ibrahim Store</span>
                        </div>
                    </a>
                </div>

                <!-- Desktop Navigation Links -->
                <nav class="hidden md:flex items-center space-x-1 space-x-reverse text-sm font-semibold">
                    <a href="#home" class="px-3 py-2 text-white hover:text-brand-gold transition-colors duration-200">الرئيسية</a>
                    <a href="#categories" class="px-3 py-2 text-zinc-300 hover:text-brand-gold transition-colors duration-200">الأقسام</a>
                    <a href="#products" class="px-3 py-2 text-zinc-300 hover:text-brand-gold transition-colors duration-200">التشكيلة الجديدة</a>
                    <a href="#offers" class="px-3 py-2 text-zinc-300 hover:text-brand-gold transition-colors duration-200">العروض المميزة</a>
                    <a href="#features" class="px-3 py-2 text-zinc-300 hover:text-brand-gold transition-colors duration-200">لماذا نحن؟</a>
                </nav>

                <!-- Actions (Search, Wishlist, Cart) -->
                <div class="flex items-center space-x-4 space-x-reverse">
                    <!-- Search Input Toggle -->
                    <div class="relative hidden sm:block">
                        <input type="text" id="searchInput" placeholder="بحث عن منتج..." onkeyup="filterProductsBySearch()" class="bg-zinc-900 border border-zinc-700 text-xs text-zinc-200 rounded-full py-2 pr-9 pl-4 focus:outline-none focus:border-brand-gold w-36 focus:w-48 transition-all">
                        <i class="fa-solid fa-magnifying-glass absolute right-3 top-2.5 text-zinc-400 text-xs"></i>
                    </div>

                    <!-- Wishlist Toggle -->
                    <button onclick="toggleWishlistModal()" class="relative p-2 text-zinc-300 hover:text-brand-gold transition-colors">
                        <i class="fa-regular fa-heart text-xl"></i>
                        <span id="wishlistCount" class="absolute -top-1 -left-1 bg-red-600 text-white text-[10px] font-bold rounded-full h-4 w-4 flex items-center justify-center opacity-0 transition-opacity">0</span>
                    </button>

                    <!-- Cart Toggle -->
                    <button onclick="toggleCartDrawer()" class="relative p-2 text-zinc-300 hover:text-brand-gold transition-colors">
                        <i class="fa-solid fa-bag-shopping text-xl"></i>
                        <span id="cartBadge" class="absolute -top-1 -left-1 bg-brand-gold text-black text-[10px] font-bold rounded-full h-5 w-5 flex items-center justify-center">0</span>
                    </button>

                    <!-- Mobile Menu Button -->
                    <button onclick="toggleMobileMenu()" class="md:hidden p-2 text-zinc-300 hover:text-white">
                        <i class="fa-solid fa-bars text-xl" id="menuIcon"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Menu Dropdown -->
        <div id="mobileMenu" class="hidden md:hidden bg-zinc-950 border-b border-zinc-800 px-4 pt-2 pb-6 space-y-3">
            <input type="text" placeholder="بحث عن منتج..." onkeyup="filterProductsBySearch()" class="w-full bg-zinc-900 border border-zinc-700 text-xs text-zinc-200 rounded-lg py-2.5 px-3 focus:outline-none focus:border-brand-gold mb-2">
            <a href="#home" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-lg text-white hover:bg-zinc-900">الرئيسية</a>
            <a href="#categories" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-lg text-zinc-300 hover:bg-zinc-900">الأقسام</a>
            <a href="#products" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-lg text-zinc-300 hover:bg-zinc-900">التشكيلة الجديدة</a>
            <a href="#offers" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-lg text-zinc-300 hover:bg-zinc-900">العروض المميزة</a>
            <a href="#features" onclick="toggleMobileMenu()" class="block px-3 py-2 rounded-lg text-zinc-300 hover:bg-zinc-900">لماذا إبراهيم ستور؟</a>
        </div>
    </header>

    <main class="mt-20">
        <!-- Hero Section -->
        <section id="home" class="relative min-h-[85vh] flex items-center justify-center overflow-hidden py-16">
            <!-- Background Image Overlay -->
            <div class="absolute inset-0 z-0">
                <img src="https://images.unsplash.com/photo-1490481651871-ab68de25d43d?q=80&w=1600&auto=format&fit=crop" 
                     alt="Ibrahim Store Banner" 
                     class="w-full h-full object-cover object-top opacity-30 scale-105 transition-transform duration-10000 hover:scale-100">
                <div class="absolute inset-0 bg-gradient-to-t from-black via-black/60 to-transparent"></div>
            </div>

            <!-- Hero Content -->
            <div class="relative z-10 max-w-5xl mx-auto px-4 text-center">
                <span class="inline-block px-4 py-1.5 rounded-full bg-brand-gold/10 border border-brand-gold/30 text-brand-gold text-xs sm:text-sm font-semibold mb-6 animate-pulse">
                    ✨ تشكيلة الشتاء والمواسم الجديدة 2026
                </span>
                <h1 class="text-4xl sm:text-6xl md:text-7xl font-black text-white leading-tight mb-6">
                    أناقة فاخرة تعبر عن <br class="hidden sm:inline">
                    <span class="gold-gradient-text">شخصيتك الفريدة</span>
                </h1>
                <p class="text-base sm:text-lg text-zinc-300 max-w-2xl mx-auto mb-8 font-light leading-relaxed">
                    اكتشف المزيج المثالي بين الراحة العصرية والجودة العالية مع أحدث تصاميم الملابس الرجالية والنسائية من إبراهيم ستور.
                </p>
                <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
                    <a href="#products" class="w-full sm:w-auto gold-btn text-black font-bold px-8 py-4 rounded-xl text-base flex items-center justify-center gap-2 shadow-lg">
                        <span>تسوق التشكيلة الآن</span>
                        <i class="fa-solid fa-arrow-left text-xs"></i>
                    </a>
                    <a href="#categories" class="w-full sm:w-auto bg-zinc-900/80 hover:bg-zinc-800 border border-zinc-700 text-white font-semibold px-8 py-4 rounded-xl text-base flex items-center justify-center transition">
                        استكشف الأقسام
                    </a>
                </div>
            </div>
        </section>

        <!-- Categories Section -->
        <section id="categories" class="py-16 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-white mb-3">تصفح حسب القسم</h2>
                <p class="text-zinc-400 text-sm">اختر الفئة التي تبحث عنها لاستعراض أفضل المنتجات</p>
            </div>

            <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-5 gap-4 sm:gap-6">
                <!-- Hoodie Category -->
                <div onclick="filterCategory('hoodies')" class="group cursor-pointer rounded-2xl overflow-hidden glass-card p-4 text-center hover:border-brand-gold transition duration-300">
                    <div class="h-32 rounded-xl overflow-hidden mb-3">
                        <img src="https://images.unsplash.com/photo-1556905055-8f358a7a47b2?q=80&w=400&auto=format&fit=crop" alt="هوديز" class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="font-bold text-white text-sm group-hover:text-brand-gold transition">هوديز وسويت شيرت</h3>
                </div>

                <!-- T-Shirts/Shirts -->
                <div onclick="filterCategory('shirts')" class="group cursor-pointer rounded-2xl overflow-hidden glass-card p-4 text-center hover:border-brand-gold transition duration-300">
                    <div class="h-32 rounded-xl overflow-hidden mb-3">
                        <img src="https://images.unsplash.com/photo-1618354691373-d851c5c3a990?q=80&w=400&auto=format&fit=crop" alt="تيشرتات" class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="font-bold text-white text-sm group-hover:text-brand-gold transition">تيشرتات وقمصان</h3>
                </div>

                <!-- Pants -->
                <div onclick="filterCategory('pants')" class="group cursor-pointer rounded-2xl overflow-hidden glass-card p-4 text-center hover:border-brand-gold transition duration-300">
                    <div class="h-32 rounded-xl overflow-hidden mb-3">
                        <img src="https://images.unsplash.com/photo-1542272604-780c36856d62?q=80&w=400&auto=format&fit=crop" alt="بنطلونات" class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="font-bold text-white text-sm group-hover:text-brand-gold transition">بنطلونات جينز وترينجات</h3>
                </div>

                <!-- Jackets -->
                <div onclick="filterCategory('jackets')" class="group cursor-pointer rounded-2xl overflow-hidden glass-card p-4 text-center hover:border-brand-gold transition duration-300">
                    <div class="h-32 rounded-xl overflow-hidden mb-3">
                        <img src="https://images.unsplash.com/photo-1551028719-00167b16eac5?q=80&w=400&auto=format&fit=crop" alt="جاكيتات" class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="font-bold text-white text-sm group-hover:text-brand-gold transition">جاكيتات ومعاطف</h3>
                </div>

                <!-- Accessories -->
                <div onclick="filterCategory('accessories')" class="group cursor-pointer rounded-2xl overflow-hidden glass-card p-4 text-center hover:border-brand-gold transition duration-300">
                    <div class="h-32 rounded-xl overflow-hidden mb-3">
                        <img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?q=80&w=400&auto=format&fit=crop" alt="إكسسوارات" class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="font-bold text-white text-sm group-hover:text-brand-gold transition">إكسسوارات ومكملات</h3>
                </div>
            </div>
        </section>

        <!-- Products Grid Section -->
        <section id="products" class="py-16 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 border-t border-zinc-900">
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-8 gap-4">
                <div>
                    <span class="text-brand-gold text-xs font-bold tracking-widest uppercase">متجر إبراهيم ستور</span>
                    <h2 class="text-3xl font-black text-white mt-1">التشكيلة المختارة لك</h2>
                </div>

                <!-- Category Filters -->
                <div class="flex flex-wrap gap-2 text-xs font-semibold">
                    <button onclick="filterCategory('all')" id="btn-all" class="filter-btn active px-4 py-2 rounded-xl bg-brand-gold text-black">الكل</button>
                    <button onclick="filterCategory('men')" id="btn-men" class="filter-btn px-4 py-2 rounded-xl bg-zinc-900 text-zinc-300 hover:bg-zinc-800">رجالي</button>
                    <button onclick="filterCategory('women')" id="btn-women" class="filter-btn px-4 py-2 rounded-xl bg-zinc-900 text-zinc-300 hover:bg-zinc-800">حريمي</button>
                    <button onclick="filterCategory('hoodies')" id="btn-hoodies" class="filter-btn px-4 py-2 rounded-xl bg-zinc-900 text-zinc-300 hover:bg-zinc-800">هوديز</button>
                    <button onclick="filterCategory('jackets')" id="btn-jackets" class="filter-btn px-4 py-2 rounded-xl bg-zinc-900 text-zinc-300 hover:bg-zinc-800">جاكيتات</button>
                </div>
            </div>

            <!-- Products Grid Container -->
            <div id="productsGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- JavaScript rendered items will appear here -->
            </div>
        </section>

        <!-- Promo Offer Banner -->
        <section id="offers" class="py-12 my-12 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="relative rounded-3xl overflow-hidden glass-card border border-brand-gold/30 p-8 sm:p-12">
                <div class="absolute -right-20 -bottom-20 w-80 h-80 bg-brand-gold/10 rounded-full blur-3xl pointer-events-none"></div>
                
                <div class="relative z-10 flex flex-col md:flex-row items-center justify-between gap-8">
                    <div class="text-center md:text-right space-y-3 max-w-xl">
                        <span class="bg-red-600/20 text-red-400 border border-red-500/30 text-xs font-bold px-3 py-1 rounded-full">عرض لفترة محدودة 🔥</span>
                        <h3 class="text-3xl sm:text-4xl font-black text-white">خصم يصل إلى 30% على جاكيتات الشتاء</h3>
                        <p class="text-zinc-400 text-sm leading-relaxed">احصل على إطلالة دافئة وأنيقة مع أقوى خصومات الموسم من إبراهيم ستور. الشحن مجاني للطلبات لأكثر من 1500 ج.م!</p>
                    </div>

                    <div class="flex-shrink-0">
                        <a href="#products" onclick="filterCategory('jackets')" class="gold-btn text-black font-bold px-8 py-4 rounded-xl text-base block text-center shadow-xl">
                            احصل على العرض الآن
                        </a>
                    </div>
                </div>
            </div>
        </section>

        <!-- Brand Features / Highlights -->
        <section id="features" class="py-16 bg-zinc-950/50 border-t border-b border-zinc-900">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    
                    <!-- Feature 1 -->
                    <div class="flex items-start gap-4 p-6 rounded-2xl glass-card">
                        <div class="w-12 h-12 rounded-xl gold-btn text-black flex items-center justify-center text-xl font-bold flex-shrink-0">
                            <i class="fa-solid fa-truck-fast"></i>
                        </div>
                        <div>
                            <h4 class="text-lg font-bold text-white mb-1">شحن سريع لكل مصر</h4>
                            <p class="text-xs text-zinc-400 leading-relaxed">توصيل سريع ومباشر لباب منزلك في جميع محافظات الجمهورية خلال 2 - 4 أيام عمل.</p>
                        </div>
                    </div>

                    <!-- Feature 2 -->
                    <div class="flex items-start gap-4 p-6 rounded-2xl glass-card">
                        <div class="w-12 h-12 rounded-xl gold-btn text-black flex items-center justify-center text-xl font-bold flex-shrink-0">
                            <i class="fa-solid fa-gem"></i>
                        </div>
                        <div>
                            <h4 class="text-lg font-bold text-white mb-1">خامات ممتازة 100%</h4>
                            <p class="text-xs text-zinc-400 leading-relaxed">نضمن لك أعلى خامات القماش مع تقفيل واهتمام بالتفاصيل يرضي ذوقك العالي.</p>
                        </div>
                    </div>

                    <!-- Feature 3 -->
                    <div class="flex items-start gap-4 p-6 rounded-2xl glass-card">
                        <div class="w-12 h-12 rounded-xl gold-btn text-black flex items-center justify-center text-xl font-bold flex-shrink-0">
                            <i class="fa-solid fa-arrows-rotate"></i>
                        </div>
                        <div>
                            <h4 class="text-lg font-bold text-white mb-1">معاينة واستبدال مرن</h4>
                            <p class="text-xs text-zinc-400 leading-relaxed">يمكنك معاينة المنتج عند الاستلام، مع سياسة استبدال واسترجاع سهلة ومريحة.</p>
                        </div>
                    </div>

                </div>
            </div>
        </section>

    </main>

    <!-- Shopping Cart Drawer Overlay -->
    <div id="cartOverlay" class="fixed inset-0 bg-black/70 backdrop-blur-sm z-50 opacity-0 pointer-events-none transiti
