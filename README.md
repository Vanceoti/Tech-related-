
<html lang="en" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="VickTech.org — Cutting-edge insights on AI, quantum computing, cybersecurity, and future technology .">
    <title>VickTech.org | Where Vision Meets Code</title>
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Space+Grotesk:wght@500;600;700&display=swap');
        
        .logo-font {
            font-family: 'Space Grotesk', sans-serif;
        }
        
        .card {
            transition: all 0.4s cubic-bezier(0.4, 0.0, 0.2, 1);
        }
        
        .card:hover {
            transform: translateY(-12px);
            box-shadow: 0 25px 50px -12px rgb(0 245 255 / 0.15);
        }
        
        .nav-link {
            position: relative;
        }
        
        .nav-link:after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 0;
            height: 2px;
            background: rgb(34 211 238);
            transition: width 0.3s ease;
        }
        
        .nav-link:hover:after {
            width: 100%;
        }
        
        .hero-bg {
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 100%);
        }
        
        .article-img {
            transition: transform 0.6s cubic-bezier(0.4, 0.0, 0.2, 1);
        }
        
        .card:hover .article-img {
            transform: scale(1.08);
        }
    </style>
</head>
<body class="bg-zinc-50 dark:bg-zinc-950 text-zinc-900 dark:text-zinc-100 min-h-screen font-sans">
    
    <!-- HEADER NAVIGATION -->
    <nav class="bg-white dark:bg-zinc-900 border-b border-zinc-200 dark:border-zinc-800 sticky top-0 z-50">
        <div class="max-w-screen-2xl mx-auto px-6 py-5">
            <div class="flex items-center justify-between">
                <!-- Logo -->
                <div class="flex items-center gap-x-3">
                    <svg width="46" height="46" viewBox="0 0 42 42" fill="none" xmlns="http://www.w3.org/2000/svg" class="text-cyan-400">
                        <rect x="4" y="4" width="34" height="34" rx="8" stroke="currentColor" stroke-width="3"/>
                        <path d="M13 13L29 29" stroke="currentColor" stroke-width="3" stroke-linecap="round"/>
                        <path d="M29 13L13 29" stroke="currentColor" stroke-width="3" stroke-linecap="round"/>
                    </svg>
                    <div>
                        <span class="logo-font text-3xl font-semibold tracking-tighter">VickTech</span>
                        <span class="text-xs tracking-[2px] text-cyan-400 font-medium">.ORG</span>
                    </div>
                </div>

                <!-- Desktop Menu -->
                <div class="hidden md:flex items-center gap-x-9 text-sm font-medium">
                    <a href="#" class="nav-link text-zinc-700 dark:text-zinc-300 hover:text-cyan-400">Home</a>
                    <a href="#articles" class="nav-link text-zinc-700 dark:text-zinc-300 hover:text-cyan-400">Articles</a>
                    <a href="#" class="nav-link text-zinc-700 dark:text-zinc-300 hover:text-cyan-400">Categories</a>
                    <a href="#" class="nav-link text-zinc-700 dark:text-zinc-300 hover:text-cyan-400">About</a>
                </div>

                <!-- Right Side Controls -->
                <div class="flex items-center gap-x-4">
                    <!-- Search -->
                    <div class="relative hidden sm:block">
                        <input 
                            type="text" 
                            id="search-input"
                            placeholder="Search articles..."
                            class="bg-zinc-100 dark:bg-zinc-800 border border-transparent focus:border-cyan-400 w-72 pl-11 py-3 rounded-2xl text-sm outline-none placeholder:text-zinc-400">
                        <i class="fa-solid fa-magnifying-glass absolute left-4 top-1/2 -translate-y-1/2 text-zinc-400"></i>
                    </div>

                    <!-- Theme Toggle -->
                    <button onclick="toggleTheme()" 
                            class="w-11 h-11 flex items-center justify-center rounded-2xl bg-zinc-100 dark:bg-zinc-800 hover:bg-zinc-200 dark:hover:bg-zinc-700 transition-colors">
                        <i id="theme-icon" class="fa-solid fa-moon text-xl"></i>
                    </button>

                    <!-- Mobile Menu Button -->
                    <button onclick="toggleMobileMenu()" 
                            class="md:hidden w-11 h-11 flex items-center justify-center text-2xl text-zinc-700 dark:text-zinc-300">
                        <i id="mobile-menu-icon" class="fa-solid fa-bars"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white dark:bg-zinc-900 border-t border-zinc-200 dark:border-zinc-800">
            <div class="px-6 py-8 flex flex-col gap-y-6 text-lg font-medium">
                <a href="#" class="nav-link">Home</a>
                <a href="#articles" class="nav-link">Articles</a>
                <a href="#" class="nav-link">Categories</a>
                <a href="#" class="nav-link">About Vance</a>
            </div>
        </div>
    </nav>

    <!-- HERO SECTION -->
    <header class="hero-bg py-24 md:py-32">
        <div class="max-w-screen-2xl mx-auto px-6">
            <div class="max-w-3xl">
                <h1 class="text-5xl md:text-6xl lg:text-7xl font-semibold logo-font tracking-tighter leading-none">
                    TECH THAT SHAPES<br>THE FUTURE
                </h1>
                <p class="mt-6 text-xl md:text-2xl text-zinc-400 max-w-lg">
                    Independent insights on AI, quantum computing, cybersecurity, and emerging technology from Nairobi.
                </p>
                <div class="mt-10">
                    <a href="#articles" 
                       class="inline-flex items-center gap-x-3 bg-cyan-400 hover:bg-cyan-300 text-zinc-950 font-semibold px-8 py-4 rounded-2xl text-lg transition-all">
                        Explore Latest Articles
                        <i class="fa-solid fa-arrow-right"></i>
                    </a>
                </div>
            </div>
        </div>
    </header>

    <!-- RESPONSIVE ARTICLE GRID -->
    <section id="articles" class="max-w-screen-2xl mx-auto px-6 py-20">
        <div class="flex justify-between items-end mb-12">
            <h2 class="text-4xl font-semibold logo-font tracking-tight">Latest from VickTech</h2>
            <a href="#" class="text-cyan-400 hover:text-cyan-300 flex items-center gap-x-2 text-sm font-medium">
                View all articles 
                <i class="fa-solid fa-arrow-right"></i>
            </a>
        </div>

        <!-- Responsive News Card Grid -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
            
            <!-- Article Card -->
            <article class="card bg-white dark:bg-zinc-900 rounded-3xl overflow-hidden border border-zinc-200 dark:border-zinc-800 group">
                <div class="relative h-56 overflow-hidden">
                    <img src="https://picsum.photos/id/1015/800/600" 
                         alt="AI Agents 2028" 
                         loading="lazy"
                         decoding="async"
                         class="article-img w-full h-full object-cover">
                    <div class="absolute top-4 left-4 bg-black/70 text-white text-xs px-4 py-1.5 rounded-2xl font-medium">Artificial Intelligence</div>
                </div>
                <div class="p-6">
                    <h3 class="font-semibold text-xl leading-tight line-clamp-3 group-hover:text-cyan-400 transition-colors">
                        Why AI Agents Will Replace Most Software Engineers by 2028
                    </h3>
                    <p class="mt-4 text-zinc-600 dark:text-zinc-400 text-sm line-clamp-3">
                        A deep dive into autonomous coding agents and the future of software development in Africa and beyond.
                    </p>
                    <div class="mt-6 flex items-center justify-between text-xs text-zinc-500">
                        <div class="flex items-center gap-x-2">
                            <span>Vance</span>
                        </div>
                        <div>Mar 28, 2026 • 8 min read</div>
                    </div>
                </div>
            </article>

            <!-- Article Card 2 -->
            <article class="card bg-white dark:bg-zinc-900 rounded-3xl overflow-hidden border border-zinc-200 dark:border-zinc-800 group">
                <div class="relative h-56 overflow-hidden">
                    <img src="https://picsum.photos/id/201/800/600" 
                         alt="Quantum Lab Kenya" 
                         loading="lazy"
                         decoding="async"
                         class="article-img w-full h-full object-cover">
                    <div class="absolute top-4 left-4 bg-black/70 text-white text-xs px-4 py-1.5 rounded-2xl font-medium">Quantum Computing</div>
                </div>
                <div class="p-6">
                    <h3 class="font-semibold text-xl leading-tight line-clamp-3 group-hover:text-cyan-400 transition-colors">
                        Kenya’s First Quantum Research Lab Goes Live
                    </h3>
                    <p class="mt-4 text-zinc-600 dark:text-zinc-400 text-sm line-clamp-3">
                        Inside the groundbreaking partnership between Strathmore University and IBM Quantum.
                    </p>
                    <div class="mt-6 flex items-center justify-between text-xs text-zinc-500">
                        <div class="flex items-center gap-x-2">
                            <span>Vance</span>
                        </div>
                        <div>Mar 25, 2026 • 12 min read</div>
                    </div>
                </div>
            </article>

            <!-- Article Card 3 -->
            <article class="card bg-white dark:bg-zinc-900 rounded-3xl overflow-hidden border border-zinc-200 dark:border-zinc-800 group">
                <div class="relative h-56 overflow-hidden">
                    <img src="https://picsum.photos/id/870/800/600" 
                         alt="Cybersecurity" 
                         loading="lazy"
                         decoding="async"
                         class="article-img w-full h-full object-cover">
                    <div class="absolute top-4 left-4 bg-black/70 text-white text-xs px-4 py-1.5 rounded-2xl font-medium">Cybersecurity</div>
                </div>
                <div class="p-6">
                    <h3 class="font-semibold text-xl leading-tight line-clamp-3 group-hover:text-cyan-400 transition-colors">
                        The $2.3 Billion Ransomware Attack That Almost Took Down M-PESA
                    </h3>
                    <p class="mt-4 text-zinc-600 dark:text-zinc-400 text-sm line-clamp-3">
                        Critical lessons every African fintech founder and developer must learn.
                    </p>
                    <div class="mt-6 flex items-center justify-between text-xs text-zinc-500">
                        <div class="flex items-center gap-x-2">
                            <span>Vance</span>
                        </div>
                        <div>Mar 22, 2026 • 6 min read</div>
                    </div>
                </div>
            </article>

            <!-- Article Card 4 -->
            <article class="card bg-white dark:bg-zinc-900 rounded-3xl overflow-hidden border border-zinc-200 dark:border-zinc-800 group">
                <div class="relative h-56 overflow-hidden">
                    <img src="https://picsum.photos/id/106/800/600" 
                         alt="Future Tech" 
                         loading="lazy"
                         decoding="async"
                         class="article-img w-full h-full object-cover">
                    <div class="absolute top-4 left-4 bg-black/70 text-white text-xs px-4 py-1.5 rounded-2xl font-medium">Future Tech</div>
                </div>
                <div class="p-6">
                    <h3 class="font-semibold text-xl leading-tight line-clamp-3 group-hover:text-cyan-400 transition-colors">
                        The Rise of Edge AI in African Smart Cities
                    </h3>
                    <p class="mt-4 text-zinc-600 dark:text-zinc-400 text-sm line-clamp-3">
                        How decentralized intelligence is transforming urban infrastructure across the continent.
                    </p>
                    <div class="mt-6 flex items-center justify-between text-xs text-zinc-500">
                        <div class="flex items-center gap-x-2">
                            <span>Vance</span>
                        </div>
                        <div>Mar 20, 2026 • 9 min read</div>
                    </div>
                </div>
            </article>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="bg-zinc-900 text-zinc-400 py-16 border-t border-zinc-800">
        <div class="max-w-screen-2xl mx-auto px-6 text-center">
            <div class="flex items-center justify-center gap-x-3 mb-6">
                <svg width="32" height="32" viewBox="0 0 42 42" fill="none" xmlns="http://www.w3.org/2000/svg" class="text-cyan-400">
                    <rect x="4" y="4" width="34" height="34" rx="8" stroke="currentColor" stroke-width="3"/>
                    <path d="M13 13L29 29" stroke="currentColor" stroke-width="3" stroke-linecap="round"/>
                    <path d="M29 13L13 29" stroke="currentColor" stroke-width="3" stroke-linecap="round"/>
                </svg>
                <span class="logo-font text-2xl font-medium">VickTech</span>
            </div>
            <p class="text-sm">© 2026 Vance • Independent Tech Intelligence</p>
            <p class="text-xs mt-4 text-zinc-500">Made with passion for technology that moves the world forward</p>
        </div>
    </footer>

    <script>
        // Initialize Tailwind (already loaded via CDN)

        function initTheme() {
            const saved = localStorage.getItem('theme');
            const html = document.documentElement;
            
            if (saved === 'light') {
                html.classList.remove('dark');
            } else {
                html.classList.add('dark'); // Default to dark mode
            }
            updateThemeIcon();
        }

        function toggleTheme() {
            const html = document.documentElement;
            const isDark = html.classList.contains('dark');
            
            if (isDark) {
                html.classList.remove('dark');
                localStorage.setItem('theme', 'light');
            } else {
                html.classList.add('dark');
                localStorage.setItem('theme', 'dark');
            }
            updateThemeIcon();
        }

        function updateThemeIcon() {
            const icon = document.getElementById('theme-icon');
            const isDark = document.documentElement.classList.contains('dark');
            
            if (isDark) {
                icon.classList.remove('fa-moon');
                icon.classList.add('fa-sun');
            } else {
                icon.classList.remove('fa-sun');
                icon.classList.add('fa-moon');
            }
        }

        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu');
            const icon = document.getElementById('mobile-menu-icon');
            
            menu.classList.toggle('hidden');
            
            if (!menu.classList.contains('hidden')) {
                icon.classList.remove('fa-bars');
                icon.classList.add('fa-xmark');
            } else {
                icon.classList.remove('fa-xmark');
                icon.classList.add('fa-bars');
            }
        }

        // Simple search functionality (demo)
        document.getElementById('search-input').addEventListener('keypress', (e) => {
            if (e.key === 'Enter') {
                const query = e.target.value.trim();
                if (query) {
                    alert(`Searching for "${query}"...\n\n(In a full site this would filter the article grid dynamically)`);
                }
            }
        });

        // Initialize everything on load
        window.onload = () => {
            initTheme();
            console.log('%c✅ VickTech.org — Modern responsive version loaded successfully', 'color:#22d3ee; font-family:Space Grotesk;');
        };
    </script>
</body>
</html>
