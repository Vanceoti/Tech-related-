<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="VickTech.org — Cutting-edge insights on AI, future tech, cybersecurity, and innovation. Powered by curiosity.">
    <title>VickTech.org | Where Vision Meets Code</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500&amp;family=Space+Grotesk:wght@500&amp;display=swap');
        
        :root {
            --tw-color-primary: #00f5ff;
        }
        
        * {
            transition-property: color, background-color, border-color, text-decoration-color, fill, stroke;
            transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
            transition-duration: 150ms;
        }
        
        .tailwind-ready .logo-text {
            font-family: 'Space Grotesk', sans-serif;
        }
        
        .hero-bg {
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 100%);
        }
        
        .nav-link {
            position: relative;
        }
        
        .nav-link:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -2px;
            left: 0;
            background-color: #00f5ff;
        }
        
        .nav-link:hover:after {
            width: 100%;
        }
        
        .blog-card {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        
        .blog-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 20px 25px -5px rgb(0 245 255 / 0.1);
        }
        
        .glow {
            text-shadow: 0 0 20px rgb(0 245 255);
        }
        
        .donation-float {
            animation: float 3s ease-in-out infinite;
        }
    </style>
</head>
<body class="tailwind-ready bg-zinc-950 text-white">
    <!-- NAVBAR -->
    <nav class="bg-zinc-900 border-b border-white/10 sticky top-0 z-50">
        <div class="max-w-screen-2xl mx-auto">
            <div class="px-8 py-5 flex items-center justify-between">
                
                <!-- LOGO -->
                <div class="flex items-center gap-x-3">
                    <!-- Slick SVG Logo -->
                    <svg width="42" height="42" viewBox="0 0 42 42" fill="none" xmlns="http://www.w3.org/2000/svg" class="drop-shadow-[0_0_15px_#00f5ff]">
                        <rect x="4" y="4" width="34" height="34" rx="8" stroke="#00f5ff" stroke-width="3"/>
                        <path d="M13 13L29 29" stroke="#00f5ff" stroke-width="3" stroke-linecap="round"/>
                        <path d="M29 13L13 29" stroke="#00f5ff" stroke-width="3" stroke-linecap="round"/>
                        <!-- Circuit dots -->
                        <circle cx="13" cy="13" r="3" fill="#00f5ff"/>
                        <circle cx="29" cy="29" r="3" fill="#00f5ff"/>
                        <circle cx="21" cy="21" r="2" fill="#fff"/>
                    </svg>
                    <div>
                        <h1 class="logo-text text-3xl font-semibold tracking-[-1px] glow">VickTech</h1>
                        <p class="text-[10px] text-cyan-300 -mt-1 tracking-[1px] font-medium">.org</p>
                    </div>
                    <span class="text-xs px-2.5 py-px bg-cyan-950 text-cyan-300 rounded-full border border-cyan-400/30 font-medium">EST 2025</span>
                </div>

                <!-- MENU -->
                <div class="hidden md:flex items-center gap-x-8 text-sm font-medium">
                    <a href="#" onclick="navigateToSection('home')" class="nav-link text-white hover:text-cyan-300">Home</a>
                    <a href="#" onclick="navigateToSection('blog')" class="nav-link text-white hover:text-cyan-300">Blog</a>
                    <a href="#" onclick="navigateToSection('categories')" class="nav-link text-white hover:text-cyan-300">Categories</a>
                    <a href="#" onclick="navigateToSection('about')" class="nav-link text-white hover:text-cyan-300">About Vick</a>
                    <a href="#" onclick="navigateToSection('newsletter')" class="nav-link text-white hover:text-cyan-300">Newsletter</a>
                </div>

                <!-- RIGHT SIDE: Search + Donation Button -->
                <div class="flex items-center gap-x-4">
                    <!-- Search -->
                    <div class="relative group">
                        <input 
                            id="search-input"
                            type="text" 
                            placeholder="Search innovation..."
                            onkeyup="if(event.key==='Enter') handleSearch()"
                            class="bg-zinc-800 text-sm border border-white/10 focus:border-cyan-300 rounded-2xl px-5 py-3 w-72 outline-none placeholder:text-zinc-400">
                        <i onclick="handleSearch()" class="fa-solid fa-magnifying-glass absolute right-5 top-1/2 -translate-y-1/2 text-cyan-300 cursor-pointer"></i>
                    </div>

                    <!-- Donation Button (to the right) -->
                    <button onclick="showDonationModal()"
                            class="donation-float flex items-center gap-x-2 bg-gradient-to-r from-cyan-400 to-blue-500 hover:from-cyan-300 hover:to-blue-400 text-zinc-950 font-semibold px-7 py-3 rounded-3xl text-sm uppercase tracking-widest shadow-[0_0_25px_-5px] shadow-cyan-400">
                        <i class="fa-solid fa-heart"></i>
                        DONATE
                    </button>

                    <!-- Mobile menu toggle -->
                    <button onclick="toggleMobileMenu()" class="md:hidden text-2xl">
                        <i class="fa-solid fa-bars"></i>
                    </button>
                </div>
            </div>
            
            <!-- Mobile Menu -->
            <div id="mobile-menu" class="hidden md:hidden bg-zinc-900 border-t border-white/10 px-8 py-6">
                <div class="flex flex-col gap-y-4 text-sm font-medium">
                    <a href="#" onclick="navigateToSection('home');toggleMobileMenu()" class="py-2">Home</a>
                    <a href="#" onclick="navigateToSection('blog');toggleMobileMenu()" class="py-2">Blog</a>
                    <a href="#" onclick="navigateToSection('categories');toggleMobileMenu()" class="py-2">Categories</a>
                    <a href="#" onclick="navigateToSection('about');toggleMobileMenu()" class="py-2">About Vick</a>
                    <a href="#" onclick="navigateToSection('newsletter');toggleMobileMenu()" class="py-2">Newsletter</a>
                    <div class="pt-4 border-t border-white/10">
                        <button onclick="showDonationModal();toggleMobileMenu()" 
                                class="w-full flex justify-center items-center gap-x-2 bg-gradient-to-r from-cyan-400 to-blue-500 text-zinc-950 font-semibold py-4 rounded-3xl">
                            <i class="fa-solid fa-heart"></i> SUPPORT VICKTECH
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </nav>

    <!-- HERO -->
    <section id="home" class="hero-bg pt-16 pb-20">
        <div class="max-w-screen-2xl mx-auto px-8">
            <div class="grid md:grid-cols-12 gap-12 items-center">
                <div class="md:col-span-7">
                    <div class="inline-flex items-center gap-x-2 bg-white/5 text-cyan-300 text-xs font-medium px-4 py-2 rounded-3xl mb-6 border border-cyan-400/20">
                        <span class="relative flex h-2 w-2">
                            <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-cyan-400 opacity-75"></span>
                            <span class="relative inline-flex rounded-full h-2 w-2 bg-cyan-400"></span>
                        </span>
                        LIVE FROM NAIROBI • MARCH 2026
                    </div>
                    
                    <h1 class="text-6xl md:text-7xl font-semibold leading-none logo-text tracking-[-2px] max-w-2xl">
                        TECH THAT<br>SHAPES TOMORROW
                    </h1>
                    
                    <p class="mt-6 text-xl text-zinc-400 max-w-md">
                        VickTech.org delivers sharp, no-fluff insights on AI, quantum computing, cybersecurity, and the tools that will define the next decade.
                    </p>
                    
                    <div class="flex items-center gap-x-4 mt-10">
                        <button onclick="navigateToSection('blog')"
                                class="px-8 py-4 bg-white text-zinc-950 font-semibold rounded-3xl flex items-center gap-x-3 hover:scale-105">
                            <i class="fa-solid fa-arrow-right"></i>
                            EXPLORE LATEST POSTS
                        </button>
                        
                        <a href="https://www.VickTech.org" target="_blank" 
                           class="text-sm flex items-center gap-x-2 text-cyan-300 hover:text-cyan-400">
                            <span class="underline">www.VickTech.org</span>
                            <i class="fa-solid fa-external-link"></i>
                        </a>
                    </div>
                    
                    <div class="mt-12 flex items-center gap-x-8 text-xs uppercase tracking-widest">
                        <div class="flex items-center">
                            <i class="fa-solid fa-certificate text-amber-400 mr-2"></i>
                            FEATURED IN WIRED
                        </div>
                        <div class="flex items-center">
                            <i class="fa-solid fa-certificate text-amber-400 mr-2"></i>
                            TECHCRUNCH
                        </div>
                        <div class="flex items-center">
                            <i class="fa-solid fa-certificate text-amber-400 mr-2"></i>
                            THE NEXT WEB
                        </div>
                    </div>
                </div>
                
                <!-- Hero visual -->
                <div class="md:col-span-5 relative">
                    <div class="aspect-square bg-gradient-to-br from-cyan-400/10 to-transparent rounded-3xl border border-cyan-400/20 p-8 flex items-center justify-center">
                        <div class="text-center">
                            <div class="w-48 h-48 mx-auto rounded-2xl bg-zinc-900/80 border border-cyan-400/30 flex items-center justify-center relative">
                                <svg width="120" height="120" viewBox="0 0 120 120" class="text-cyan-400">
                                    <circle cx="60" cy="60" r="48" fill="none" stroke="currentColor" stroke-width="8" stroke-dasharray="10 15"/>
                                    <text x="60" y="75" text-anchor="middle" fill="#fff" font-size="42" font-family="Space Grotesk">VT</text>
                                </svg>
                                <div class="absolute -top-3 -right-3 bg-cyan-400 text-zinc-950 text-xs font-bold px-4 py-1 rounded-3xl rotate-12">LIVE</div>
                            </div>
                            <p class="mt-8 text-cyan-300 text-sm font-medium">VickTech Pulse • Real-time innovation feed</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- BLOG SECTION -->
    <section id="blog" class="max-w-screen-2xl mx-auto px-8 py-20">
        <div class="flex justify-between items-baseline mb-8">
            <h2 class="text-4xl font-semibold logo-text">Latest from VickTech</h2>
            <a onclick="navigateToSection('blog')" class="text-cyan-300 flex items-center gap-x-2 text-sm font-medium hover:gap-x-3">
                VIEW ENTIRE ARCHIVE 
                <i class="fa-solid fa-arrow-right"></i>
            </a>
        </div>
        
        <div class="grid md:grid-cols-3 gap-8">
            <!-- Post 1 -->
            <div onclick="viewPost(1)" class="blog-card bg-zinc-900 rounded-3xl overflow-hidden cursor-pointer group">
                <div class="h-64 bg-gradient-to-br from-purple-500/20 to-cyan-500/20 flex items-center justify-center relative">
                    <div class="text-6xl font-bold text-white/10 group-hover:text-white/20">AI</div>
                    <div class="absolute bottom-6 left-6 bg-black/70 text-xs px-3 py-1 rounded-2xl">MAR 28, 2026</div>
                </div>
                <div class="p-6">
                    <span class="text-xs uppercase bg-purple-900 text-purple-300 px-3 py-1 rounded-2xl">Artificial Intelligence</span>
                    <h3 class="text-2xl font-semibold mt-4 leading-tight">Why AI Agents Will Replace Most Software Engineers by 2028</h3>
                    <p class="text-zinc-400 mt-3 line-clamp-3">A deep dive into autonomous coding agents, the new agentic workflow, and what it means for the future of development in Africa and beyond.</p>
                    <div class="flex items-center justify-between mt-6 text-xs">
                        <div class="flex items-center">
                            <span class="font-medium">Vick Omondi</span>
                        </div>
                        <div>8 min read • 14K views</div>
                    </div>
                </div>
            </div>
            
            <!-- Post 2 -->
            <div onclick="viewPost(2)" class="blog-card bg-zinc-900 rounded-3xl overflow-hidden cursor-pointer group">
                <div class="h-64 bg-gradient-to-br from-amber-500/20 to-red-500/20 flex items-center justify-center relative">
                    <div class="text-6xl font-bold text-white/10 group-hover:text-white/20">QUANTUM</div>
                    <div class="absolute bottom-6 left-6 bg-black/70 text-xs px-3 py-1 rounded-2xl">MAR 25, 2026</div>
                </div>
                <div class="p-6">
                    <span class="text-xs uppercase bg-amber-900 text-amber-300 px-3 py-1 rounded-2xl">Quantum Computing</span>
                    <h3 class="text-2xl font-semibold mt-4 leading-tight">Kenya’s First Quantum Research Lab Just Went Live – Here’s What It Means</h3>
                    <p class="text-zinc-400 mt-3 line-clamp-3">Inside the groundbreaking partnership between Strathmore University and IBM Quantum. Real use cases for East Africa already in production.</p>
                    <div class="flex items-center justify-between mt-6 text-xs">
                        <div class="flex items-center">
                            <span class="font-medium">Vick Omondi</span>
                        </div>
                        <div>12 min read • 9.2K views</div>
                    </div>
                </div>
            </div>
            
            <!-- Post 3 -->
            <div onclick="viewPost(3)" class="blog-card bg-zinc-900 rounded-3xl overflow-hidden cursor-pointer group">
                <div class="h-64 bg-gradient-to-br from-emerald-500/20 to-cyan-500/20 flex items-center justify-center relative">
                    <div class="text-6xl font-bold text-white/10 group-hover:text-white/20">CYBER</div>
                    <div class="absolute bottom-6 left-6 bg-black/70 text-xs px-3 py-1 rounded-2xl">MAR 22, 2026</div>
                </div>
                <div class="p-6">
                    <span class="text-xs uppercase bg-emerald-900 text-emerald-300 px-3 py-1 rounded-2xl">Cybersecurity</span>
                    <h3 class="text-2xl font-semibold mt-4 leading-tight">The $2.3 Billion Ransomware Attack That Almost Took Down M-PESA</h3>
                    <p class="text-zinc-400 mt-3 line-clamp-3">How a new breed of AI-powered ransomware nearly collapsed East Africa’s largest fintech. Lessons every developer and founder must learn.</p>
                    <div class="flex items-center justify-between mt-6 text-xs">
                        <div class="flex items-center">
                            <span class="font-medium">Vick Omondi</span>
                        </div>
                        <div>6 min read • 21K views</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CATEGORIES + SIDEBAR DONATION -->
    <section id="categories" class="max-w-screen-2xl mx-auto px-8 pb-20">
        <div class="grid md:grid-cols-12 gap-12">
            <!-- Categories grid -->
            <div class="md:col-span-8">
                <h2 class="text-4xl font-semibold logo-text mb-8">Explore by Category</h2>
                <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
                    <div onclick="filterByCategory('AI')" class="bg-zinc-900 hover:bg-zinc-800 rounded-3xl p-6 flex flex-col items-center justify-center text-center cursor-pointer border border-transparent hover:border-cyan-400/30">
                        <i class="fa-solid fa-brain text-4xl text-purple-400 mb-4"></i>
                        <span class="font-semibold">Artificial Intelligence</span>
                        <span class="text-xs text-zinc-500 mt-1">47 articles</span>
                    </div>
                    <div onclick="filterByCategory('Quantum')" class="bg-zinc-900 hover:bg-zinc-800 rounded-3xl p-6 flex flex-col items-center justify-center text-center cursor-pointer border border-transparent hover:border-cyan-400/30">
                        <i class="fa-solid fa-atom text-4xl text-amber-400 mb-4"></i>
                        <span class="font-semibold">Quantum &amp; Future Tech</span>
                        <span class="text-xs text-zinc-500 mt-1">19 articles</span>
                    </div>
                    <div onclick="filterByCategory('Cyber')" class="bg-zinc-900 hover:bg-zinc-800 rounded-3xl p-6 flex flex-col items-center justify-center text-center cursor-pointer border border-transparent hover:border-cyan-400/30">
                        <i class="fa-solid fa-shield-halved text-4xl text-emerald-400 mb-4"></i>
                        <span class="font-semibold">Cybersecurity</span>
                        <span class="text-xs text-zinc-500 mt-1">34 articles</span>
                    </div>
                    <div onclick="filterByCategory('Dev')" class="bg-zinc-900 hover:bg-zinc-800 rounded-3xl p-6 flex flex-col items-center justify-center text-center cursor-pointer border border-transparent hover:border-cyan-400/30">
                        <i class="fa-solid fa-code text-4xl text-cyan-400 mb-4"></i>
                        <span class="font-semibold">Developer Tools</span>
                        <span class="text-xs text-zinc-500 mt-1">62 articles</span>
                    </div>
                </div>
            </div>
            
            <!-- Sticky Sidebar with Donation -->
            <div class="md:col-span-4">
                <div class="sticky top-24 bg-zinc-900 rounded-3xl p-8 border border-cyan-400/10">
                    <div class="text-center">
                        <i class="fa-solid fa-hand-holding-heart text-5xl text-cyan-400 mb-6"></i>
                        <h3 class="text-2xl font-semibold">Fuel the Vision</h3>
                        <p class="text-zinc-400 mt-3">VickTech is 100% independent. No ads. No sponsors. Just pure signal. Your donation keeps the lights on and the ideas flowing.</p>
                        
                        <!-- Donation button (prominently to the right of content, but here in sidebar) -->
                        <button onclick="showDonationModal()" 
                                class="mt-8 w-full py-5 bg-gradient-to-r from-cyan-400 to-blue-500 text-zinc-950 font-bold rounded-3xl flex items-center justify-center gap-x-3 text-lg">
                            <i class="fa-solid fa-heart-pulse"></i>
                            DONATE NOW
                        </button>
                        
                        <div class="text-xs text-zinc-500 mt-6 flex justify-center gap-x-8">
                            <div>💰 $12,847 raised this month</div>
                            <div>🔥 184 new patrons</div>
                        </div>
                        
                        <p class="text-[10px] mt-8 text-zinc-500">Accepted: M-PESA • Bitcoin • USDT • PayPal • Visa</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ABOUT VICK -->
    <section id="about" class="bg-white/5 py-20">
        <div class="max-w-screen-2xl mx-auto px-8">
            <div class="grid md:grid-cols-12 gap-12 items-center">
                <div class="md:col-span-5">
                    <div class="rounded-3xl bg-gradient-to-br from-cyan-400/10 to-transparent p-1">
                        <div class="bg-zinc-950 rounded-3xl px-8 py-12 text-center">
                            <div class="w-32 h-32 mx-auto bg-zinc-800 rounded-2xl flex items-center justify-center text-6xl mb-6">👨🏾‍💻</div>
                            <h2 class="text-3xl font-semibold">Hi, I’m Vick Omondi</h2>
                            <p class="text-cyan-300 mt-1">Founder • Engineer • Futurist</p>
                            <p class="mt-8 text-zinc-400 leading-relaxed">
                                Nairobi-born builder obsessed with technology that actually moves humanity forward. Previously led engineering at Safaricom, now writing the future at VickTech.org.
                            </p>
                            <div class="flex justify-center gap-x-6 mt-8 text-2xl">
                                <a href="#" class="hover:text-cyan-400"><i class="fa-brands fa-x-twitter"></i></a>
                                <a href="#" class="hover:text-cyan-400"><i class="fa-brands fa-linkedin"></i></a>
                                <a href="#" class="hover:text-cyan-400"><i class="fa-brands fa-github"></i></a>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="md:col-span-7">
                    <h2 class="text-5xl font-semibold logo-text leading-none">“I don’t just report on tech.<br>I build it, break it, and tell you what actually works.”</h2>
                    <div class="mt-12 grid grid-cols-3 gap-8 text-center">
                        <div>
                            <div class="text-5xl font-bold text-cyan-300">124</div>
                            <div class="text-xs uppercase tracking-widest">Articles published</div>
                        </div>
                        <div>
                            <div class="text-5xl font-bold text-cyan-300">1.2M</div>
                            <div class="text-xs uppercase tracking-widest">Monthly readers</div>
                        </div>
                        <div>
                            <div class="text-5xl font-bold text-cyan-300">42</div>
                            <div class="text-xs uppercase tracking-widest">Countries reached</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- NEWSLETTER -->
    <section id="newsletter" class="max-w-screen-2xl mx-auto px-8 py-20 border-t border-white/10">
        <div class="rounded-3xl bg-gradient-to-r from-zinc-900 to-black p-12 md:p-16 flex flex-col md:flex-row items-center justify-between gap-8">
            <div>
                <span class="px-4 py-2 bg-cyan-300 text-zinc-950 rounded-3xl text-xs font-bold">FREE</span>
                <h2 class="text-4xl font-semibold mt-4">Weekly Signal Drop</h2>
                <p class="text-xl text-zinc-400 mt-3 max-w-md">Every Sunday I send the 5 most important tech breakthroughs you actually need to know. No spam. Ever.</p>
            </div>
            <div class="flex-1 max-w-md">
                <div class="flex">
                    <input type="email" id="email-input" placeholder="your@email.com" 
                           class="flex-1 bg-white text-zinc-950 rounded-l-3xl px-7 py-6 outline-none text-lg">
                    <button onclick="subscribe()" 
                            class="bg-cyan-400 hover:bg-white text-zinc-950 font-semibold px-10 rounded-r-3xl">JOIN</button>
                </div>
                <p class="text-xs text-zinc-500 mt-4">4,872 people joined this month • You’re in good company</p>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="bg-black py-16 border-t border-white/10">
        <div class="max-w-screen-2xl mx-auto px-8">
            <div class="flex flex-wrap justify-between items-start gap-y-12">
                <div>
                    <div class="flex items-center gap-x-3">
                        <svg width="32" height="32" viewBox="0 0 42 42" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <rect x="4" y="4" width="34" height="34" rx="8" stroke="#00f5ff" stroke-width="3"/>
                            <path d="M13 13L29 29" stroke="#00f5ff" stroke-width="3" stroke-linecap="round"/>
                            <path d="M29 13L13 29" stroke="#00f5ff" stroke-width="3" stroke-linecap="round"/>
                        </svg>
                        <h1 class="logo-text text-2xl">VickTech.org</h1>
                    </div>
                    <p class="text-zinc-500 text-sm mt-4 max-w-xs">Independent tech intelligence from Nairobi, Kenya. Building the future, one byte at a time.</p>
                </div>
                
                <div class="grid grid-cols-3 gap-x-16">
                    <div>
                        <span class="text-xs font-medium text-zinc-400">PLATFORM</span>
                        <ul class="mt-4 space-y-2 text-sm">
                            <li><a href="#" class="hover:text-cyan-300">Archive</a></li>
                            <li><a href="#" class="hover:text-cyan-300">Podcast</a></li>
                            <li><a href="#" class="hover:text-cyan-300">Videos</a></li>
                            <li><a href="#" class="hover:text-cyan-300">Resources</a></li>
                        </ul>
                    </div>
                    <div>
                        <span class="text-xs font-medium text-zinc-400">COMMUNITY</span>
                        <ul class="mt-4 space-y-2 text-sm">
                            <li><a href="#" class="hover:text-cyan-300">Discord</a></li>
                            <li><a href="#" class="hover:text-cyan-300">Twitter / X</a></li>
                            <li><a href="#" class="hover:text-cyan-300">Telegram</a></li>
                            <li><a href="#" class="hover:text-cyan-300">Meetups</a></li>
                        </ul>
                    </div>
                    <div>
                        <span class="text-xs font-medium text-zinc-400">LEGAL</span>
                        <ul class="mt-4 space-y-2 text-sm">
                            <li><a href="#" class="hover:text-cyan-300">Privacy</a></li>
                            <li><a href="#" class="hover:text-cyan-300">Ethics</a></li>
                            <li><a href="#" class="hover:text-cyan-300">Transparency</a></li>
                        </ul>
                    </div>
                </div>
                
                <div class="text-right">
                    <p class="text-xs text-zinc-400">© 2026 Vick Omondi • All Rights Reserved</p>
                    <p class="text-xs text-cyan-400 mt-6">Made with ❤️ in Nairobi, Kenya</p>
                    <p class="text-xs mt-2">Domain: <a href="https://www.VickTech.org" class="underline">www.VickTech.org</a></p>
                </div>
            </div>
        </div>
    </footer>

    <!-- DONATION MODAL -->
    <div id="donation-modal" onclick="if(event.target.id === 'donation-modal') hideDonationModal()" 
         class="hidden fixed inset-0 bg-black/80 backdrop-blur-xl z-[9999] flex items-center justify-center">
        <div onclick="event.stopImmediatePropagation()" 
             class="bg-zinc-900 rounded-3xl max-w-lg w-full mx-4 p-8">
            <div class="flex justify-between items-center">
                <h3 class="text-3xl font-semibold">Support VickTech</h3>
                <button onclick="hideDonationModal()" class="text-3xl text-zinc-400">×</button>
            </div>
            
            <p class="text-zinc-400 mt-2">Your contribution keeps this independent tech publication alive and ad-free.</p>
            
            <div class="grid grid-cols-3 gap-4 my-10">
                <button onclick="selectAmount(5)" class="amount-btn border border-white/20 hover:border-cyan-400 rounded-2xl py-6 text-center">
                    <div class="text-2xl">$5</div>
                    <div class="text-xs text-zinc-400">Coffee</div>
                </button>
                <button onclick="selectAmount(10)" class="amount-btn border border-white/20 hover:border-cyan-400 rounded-2xl py-6 text-center bg-cyan-400 text-zinc-950">
                    <div class="text-2xl">$10</div>
                    <div class="text-xs text-zinc-950">Monthly signal</div>
                </button>
                <button onclick="selectAmount(25)" class="amount-btn border border-white/20 hover:border-cyan-400 rounded-2xl py-6 text-center">
                    <div class="text-2xl">$25</div>
                    <div class="text-xs text-zinc-400">Deep dive</div>
                </button>
            </div>
            
            <div class="flex items-center gap-4">
                <input id="custom-amount" type="text" placeholder="Custom amount" 
                       class="flex-1 bg-white text-zinc-950 rounded-3xl px-6 py-4 text-2xl outline-none font-medium">
                <button onclick="processDonation()" 
                        class="px-10 py-4 bg-gradient-to-r from-cyan-400 to-blue-500 text-zinc-950 font-semibold rounded-3xl">DONATE SECURELY</button>
            </div>
            
            <div class="text-center text-xs text-zinc-500 mt-8 flex justify-center items-center gap-x-6">
                <div class="flex items-center"><i class="fa-brands fa-bitcoin mr-1"></i> BTC</div>
                <div class="flex items-center"><i class="fa-brands fa-ethereum mr-1"></i> ETH</div>
                <div class="flex items-center">M-PESA • PayPal • Stripe</div>
            </div>
            
            <p class="text-[10px] text-center text-zinc-400 mt-6">Thank you. Every dollar powers better tech journalism from Africa.</p>
        </div>
    </div>

    <!-- Single post modal (demo) -->
    <div id="post-modal" onclick="if(event.target.id === 'post-modal') hidePostModal()" 
         class="hidden fixed inset-0 bg-black/90 z-[10000] flex items-center justify-center overflow-auto">
        <div onclick="event.stopImmediatePropagation()" class="max-w-3xl w-full mx-4 bg-zinc-900 rounded-3xl p-8 md:p-12">
            <div id="modal-content">
                <!-- Dynamically filled by JS -->
            </div>
        </div>
    </div>

    <script>
        // Tailwind initialization
        function initializeTailwind() {
            return {
                config(userConfig = {}) {
                    return {
                        content: [],
                        theme: {
                            extend: {}
                        },
                        darkMode: 'class',
                        ...userConfig
                    }
                },
                theme(userConfig = {}) {
                    return {
                        configUser: userConfig,
                        get colors() {
                            return {
                                primary: '#00f5ff'
                            }
                        }
                    }
                }
            }
        }
        
        // Make everything interactive
        function init() {
            // Tailwind ready
            const config = initializeTailwind().config()
            document.documentElement.setAttribute('data-tailwind-config', JSON.stringify(config))
            
            console.log('%c🚀 VickTech.org full site loaded – classy, simple, slick and ready to deploy!', 'color:#00f5ff; font-family:Space Grotesk; font-size:13px')
            
            // Fake live counter in hero (optional flair)
            let counter = 1248
            setInterval(() => {
                counter += Math.floor(Math.random() * 7) + 3
                // Could update DOM if we had a live readers element
            }, 4000)
            
            console.log('✅ Donation button placed to the right in navbar + prominent sidebar')
        }
        
        // Navigation helper
        function navigateToSection(section) {
            document.getElementById(section).scrollIntoView({ behavior: 'smooth' })
        }
        
        // Mobile menu
        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu')
            menu.classList.toggle('hidden')
        }
        
        // Donation modal
        let selectedAmount = 10
        
        function showDonationModal() {
            document.getElementById('donation-modal').classList.remove('hidden')
            document.getElementById('donation-modal').classList.add('flex')
        }
        
        function hideDonationModal() {
            const modal = document.getElementById('donation-modal')
            modal.classList.add('hidden')
            modal.classList.remove('flex')
        }
        
        function selectAmount(amount) {
            selectedAmount = amount
            // Reset all buttons
            document.querySelectorAll('.amount-btn').forEach(btn => {
                btn.classList.remove('bg-cyan-400', 'text-zinc-950')
                btn.classList.add('border-white/20')
            })
            // Highlight selected
            event.currentTarget.classList.add('bg-cyan-400', 'text-zinc-950')
        }
        
        function processDonation() {
            const custom = document.getElementById('custom-amount').value
            const amount = custom ? parseInt(custom) : selectedAmount
            
            hideDonationModal()
            
            // Fake success animation
            const notif = document.createElement('div')
            notif.style.cssText = 'position:fixed; bottom:24px; right:24px; background:#00f5ff; color:#111; padding:16px 24px; border-radius:9999px; font-weight:600; box-shadow:0 0 30px #00f5ff;'
            notif.innerHTML = `🎉 Thank you! \[ {amount} received. VickTech appreciates you.`
            document.body.appendChild(notif)
            
            setTimeout(() => notif.remove(), 4200)
            
            console.log(`💰 Simulated donation of \]{amount} to VickTech.org`)
        }
        
        // Search
        function handleSearch() {
            const query = document.getElementById('search-input').value.trim()
            if (!query) return
            alert(`🔎 Searching VickTech archive for “${query}”…\n\n(In a real site this would filter posts or redirect to search results)`)
            document.getElementById('search-input').value = ''
            navigateToSection('blog')
        }
        
        // Fake post viewer
        const postsData = {
            1: {
                title: "Why AI Agents Will Replace Most Software Engineers by 2028",
                date: "March 28, 2026",
                readTime: "8 min",
                category: "Artificial Intelligence",
                content: `
                    <h1 class="text-4xl font-semibold mb-4">Why AI Agents Will Replace Most Software Engineers by 2028</h1>
                    <p class="text-zinc-400 mb-8">The era of autonomous coding agents is here. Here’s what that actually means for developers in Africa and around the world.</p>
                    <div class="prose prose-invert text-zinc-300 leading-relaxed">
                        <p>Autonomous agents like Devin, Cursor, and the new wave of open-source models are not just tools — they are full-stack collaborators that can plan, code, test, and deploy entire features with a single prompt.</p>
                        <p>At VickTech we’ve been running internal experiments. The results are staggering: a senior developer’s output increased 14× when paired with an agentic workflow.</p>
                        <h2 class="text-2xl mt-8 mb-3">What this means for Kenya &amp; East Africa</h2>
                        <p>Instead of competing with Silicon Valley on salary, we can leapfrog by becoming the best prompt engineers and system architects in the world.</p>
                    </div>
                    <div class="flex justify-end mt-10 text-xs text-cyan-300">— Vick Omondi</div>
                `
            },
            2: {
                title: "Kenya’s First Quantum Research Lab Just Went Live",
                date: "March 25, 2026",
                readTime: "12 min",
                category: "Quantum Computing",
                content: `
                    <h1 class="text-4xl font-semibold mb-4">Kenya’s First Quantum Research Lab Just Went Live – Here’s What It Means</h1>
                    <p class="text-zinc-400 mb-8">Strathmore University + IBM Quantum partnership is the biggest tech leap East Africa has ever seen.</p>
                    <div class="prose prose-invert text-zinc-300 leading-relaxed">
                        <p>Today, the new quantum lab at Strathmore officially came online with access to IBM’s 127-qubit Eagle processor via the cloud. The first African quantum research node is now live.</p>
                    </div>
                `
            },
            3: {
                title: "The $2.3 Billion Ransomware Attack That Almost Took Down M-PESA",
                date: "March 22, 2026",
                readTime: "6 min",
                category: "Cybersecurity",
                content: `
                    <h1 class="text-4xl font-semibold mb-4">The $2.3 Billion Ransomware Attack That Almost Took Down M-PESA</h1>
                    <p class="text-zinc-400 mb-8">A story that should keep every fintech founder awake at night.</p>
                `
            }
        }
        
        function viewPost(id) {
            const post = postsData[id]
            if (!post) return
            
            const modalContent = document.getElementById('modal-content')
            modalContent.innerHTML = `
                <button onclick="hidePostModal()" class="float-right text-4xl text-zinc-400 hover:text-white">×</button>
                ${post.content}
                <div class="text-xs flex items-center gap-x-2 mt-12 pt-8 border-t border-white/10">
                    <span class="bg-white/10 text-white px-3 py-1 rounded-3xl">${post.category}</span>
                    <span>${post.date} • ${post.readTime} read</span>
                </div>
            `
            document.getElementById('post-modal').classList.remove('hidden')
            document.getElementById('post-modal').classList.add('flex')
        }
        
        function hidePostModal() {
            const modal = document.getElementById('post-modal')
            modal.classList.add('hidden')
            modal.classList.remove('flex')
        }
        
        function filterByCategory(cat) {
            alert(`📂 Filtered to ${cat} articles on VickTech.org\n\n(Full category archive would load here in production)`)
            navigateToSection('blog')
        }
        
        function subscribe() {
            const email = document.getElementById('email-input').value
            if (email) {
                alert(`✅ Thank you! You’re now subscribed to the VickTech Signal Drop.\n\nWelcome to the future.`)
                document.getElementById('email-input').value = ''
            }
        }
        
        // Launch everything
        window.onload = init
    </script>
</body>
</html>
