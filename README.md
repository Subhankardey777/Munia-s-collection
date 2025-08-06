<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Munia's Collection - Handmade Jewelry</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&family=Dancing+Script:wght@400;500;600;700&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        beige: {
                            50: '#faf9f7',
                            100: '#f5f2ed',
                            200: '#ebe4d9',
                            300: '#ddd1c0',
                            400: '#c9b896',
                            500: '#b8a082'
                        },
                        gold: {
                            100: '#fef3c7',
                            400: '#d4af37',
                            500: '#b8941f',
                            600: '#9c7c1a'
                        }
                    },
                    fontFamily: {
                        'serif': ['Playfair Display', 'serif'],
                        'script': ['Dancing Script', 'cursive'],
                        'sans': ['Inter', 'sans-serif']
                    },
                    animation: {
                        'shimmer': 'shimmer 2s linear infinite',
                        'shimmer-fast': 'shimmer 1s linear infinite',
                        'float': 'float 6s ease-in-out infinite',
                        'bounce-slow': 'bounce 3s infinite',
                        'spin-slow': 'spin 20s linear infinite',
                        'pulse-slow': 'pulse 3s infinite',
                        'fade-in-up': 'fadeInUp 1s ease-out'
                    },
                    keyframes: {
                        shimmer: {
                            '0%': { transform: 'translateX(-100%)' },
                            '100%': { transform: 'translateX(100%)' }
                        },
                        float: {
                            '0%, 100%': { transform: 'translateY(0px)' },
                            '50%': { transform: 'translateY(-20px)' }
                        },
                        fadeInUp: {
                            '0%': { opacity: '0', transform: 'translateY(30px)' },
                            '100%': { opacity: '1', transform: 'translateY(0)' }
                        }
                    }
                }
            }
        }
    </script>
</head>
<body class="bg-beige-50 text-gray-800 font-sans">
    <!-- Navigation -->
    <nav class="bg-white shadow-sm sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <div class="flex items-center">
                    <h1 class="text-2xl font-script font-bold text-gold-500">Munia's Collection</h1>
                </div>
                <div class="hidden md:flex space-x-6">
                    <a href="#home" class="flex items-center space-x-1 text-gray-700 hover:text-gold-500 transition-all duration-300 px-3 py-2 rounded-lg hover:bg-gold-50">
                        <span>🏠</span><span class="font-medium">Home</span>
                    </a>
                    <a href="#collections" class="flex items-center space-x-1 text-gray-700 hover:text-gold-500 transition-all duration-300 px-3 py-2 rounded-lg hover:bg-gold-50">
                        <span>✨</span><span class="font-medium">Collections</span>
                    </a>
                    <a href="#shop" class="flex items-center space-x-1 text-gray-700 hover:text-gold-500 transition-all duration-300 px-3 py-2 rounded-lg hover:bg-gold-50">
                        <span>🛍️</span><span class="font-medium">Shop</span>
                    </a>
                    <a href="#about" class="flex items-center space-x-1 text-gray-700 hover:text-gold-500 transition-all duration-300 px-3 py-2 rounded-lg hover:bg-gold-50">
                        <span>💎</span><span class="font-medium">About</span>
                    </a>
                    <a href="#contact" class="flex items-center space-x-1 text-gray-700 hover:text-gold-500 transition-all duration-300 px-3 py-2 rounded-lg hover:bg-gold-50">
                        <span>📞</span><span class="font-medium">Contact</span>
                    </a>
                </div>
                <div class="flex items-center space-x-4">
                    <button id="cart-btn" class="relative p-2 text-gray-700 hover:text-gold-500 transition-colors">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4m0 0L7 13m0 0l-1.5 6M7 13l-1.5 6m0 0h9m-9 0h9"></path>
                        </svg>
                        <span id="cart-count" class="absolute -top-1 -right-1 bg-gold-500 text-white text-xs rounded-full h-5 w-5 flex items-center justify-center">0</span>
                    </button>
                    <button id="mobile-menu-btn" class="md:hidden p-2 text-gray-700">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                        </svg>
                    </button>
                </div>
            </div>
        </div>
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-gradient-to-r from-white to-gold-50 border-t border-gold-200">
            <div class="px-4 pt-4 pb-4 space-y-2">
                <a href="#home" class="flex items-center space-x-3 px-4 py-3 text-gray-700 hover:text-gold-500 hover:bg-gold-100 rounded-lg transition-all duration-300">
                    <span class="text-xl">🏠</span><span class="font-medium">Home</span>
                </a>
                <a href="#collections" class="flex items-center space-x-3 px-4 py-3 text-gray-700 hover:text-gold-500 hover:bg-gold-100 rounded-lg transition-all duration-300">
                    <span class="text-xl">✨</span><span class="font-medium">Collections</span>
                </a>
                <a href="#shop" class="flex items-center space-x-3 px-4 py-3 text-gray-700 hover:text-gold-500 hover:bg-gold-100 rounded-lg transition-all duration-300">
                    <span class="text-xl">🛍️</span><span class="font-medium">Shop</span>
                </a>
                <a href="#about" class="flex items-center space-x-3 px-4 py-3 text-gray-700 hover:text-gold-500 hover:bg-gold-100 rounded-lg transition-all duration-300">
                    <span class="text-xl">💎</span><span class="font-medium">About</span>
                </a>
                <a href="#contact" class="flex items-center space-x-3 px-4 py-3 text-gray-700 hover:text-gold-500 hover:bg-gold-100 rounded-lg transition-all duration-300">
                    <span class="text-xl">📞</span><span class="font-medium">Contact</span>
                </a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="relative bg-gradient-to-br from-beige-100 via-beige-50 to-gold-100 py-20 overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-r from-transparent via-gold-200/20 to-transparent animate-pulse"></div>
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div class="text-center lg:text-left animate-fade-in-up">
                    <div class="inline-block bg-gradient-to-r from-gold-400 to-gold-600 text-white px-4 py-2 rounded-full text-sm font-medium mb-4 animate-bounce">
                        ✨ Trending Collection 2024 ✨
                    </div>
                    <h2 class="text-5xl md:text-7xl font-serif font-bold text-gray-800 mb-6 leading-tight">
                        Handcrafted
                        <span class="text-transparent bg-clip-text bg-gradient-to-r from-gold-400 via-gold-500 to-gold-600 font-script animate-shimmer">Elegance</span>
                    </h2>
                    <p class="text-xl text-gray-600 mb-8 leading-relaxed">
                        Discover our exquisite collection of handmade jewelry, where each piece tells a story of craftsmanship and timeless beauty. ✨ Made in India with love! 🇮🇳
                    </p>
                    <div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start">
                        <button onclick="document.getElementById('shop').scrollIntoView({behavior: 'smooth'})" class="bg-gradient-to-r from-gold-500 to-gold-600 hover:from-gold-600 hover:to-gold-700 text-white px-8 py-4 rounded-full text-lg font-medium transition-all duration-300 transform hover:scale-105 shadow-xl hover:shadow-2xl animate-pulse-slow">
                            🛍️ Shop Now
                        </button>
                        <button onclick="document.getElementById('collections').scrollIntoView({behavior: 'smooth'})" class="border-2 border-gold-500 text-gold-600 hover:bg-gold-500 hover:text-white px-8 py-4 rounded-full text-lg font-medium transition-all duration-300 transform hover:scale-105">
                            💎 View Collections
                        </button>
                    </div>
                </div>
                <div class="flex justify-center">
                    <div class="relative animate-float">
                        <div class="w-80 h-80 bg-gradient-to-br from-gold-400 via-gold-500 to-gold-600 rounded-full flex items-center justify-center shadow-2xl animate-spin-slow relative overflow-hidden">
                            <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/20 to-transparent animate-shimmer-fast"></div>
                            <div class="text-8xl animate-bounce-slow">💎</div>
                        </div>
                        <div class="absolute -top-4 -right-4 w-20 h-20 bg-gradient-to-br from-pink-300 to-pink-400 rounded-full opacity-60 animate-pulse"></div>
                        <div class="absolute -bottom-6 -left-6 w-16 h-16 bg-gradient-to-br from-purple-300 to-purple-400 rounded-full opacity-40 animate-bounce"></div>
                        <div class="absolute top-1/2 -right-8 w-12 h-12 bg-gradient-to-br from-yellow-300 to-yellow-400 rounded-full opacity-50 animate-ping"></div>
                        <div class="absolute -top-8 left-1/4 w-8 h-8 bg-gradient-to-br from-blue-300 to-blue-400 rounded-full opacity-60 animate-pulse"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Featured Collections -->
    <section id="collections" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-serif font-bold text-gray-800 mb-4">Featured Collections</h2>
                <p class="text-lg text-gray-600">Explore our carefully curated jewelry collections</p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <div class="group cursor-pointer transform hover:scale-105 transition-all duration-300">
                    <div class="bg-gradient-to-br from-beige-100 to-beige-200 rounded-xl p-8 text-center hover:from-gold-100 hover:to-gold-200 transition-all duration-300 shadow-lg hover:shadow-xl border border-gold-200/50">
                        <div class="w-16 h-16 bg-gradient-to-br from-gold-400 to-gold-600 rounded-full flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition-transform shadow-lg">
                            <div class="text-2xl">📿</div>
                        </div>
                        <h3 class="text-xl font-serif font-semibold text-gray-800 mb-2">Necklaces</h3>
                        <p class="text-gray-600">Elegant statement pieces ✨</p>
                        <div class="mt-3 text-sm text-gold-600 font-medium">Starting ₹1,899</div>
                    </div>
                </div>
                <div class="group cursor-pointer transform hover:scale-105 transition-all duration-300">
                    <div class="bg-gradient-to-br from-beige-100 to-beige-200 rounded-xl p-8 text-center hover:from-gold-100 hover:to-gold-200 transition-all duration-300 shadow-lg hover:shadow-xl border border-gold-200/50">
                        <div class="w-16 h-16 bg-gradient-to-br from-gold-400 to-gold-600 rounded-full flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition-transform shadow-lg">
                            <div class="text-2xl">👂</div>
                        </div>
                        <h3 class="text-xl font-serif font-semibold text-gray-800 mb-2">Earrings</h3>
                        <p class="text-gray-600">Delicate & bold designs 💫</p>
                        <div class="mt-3 text-sm text-gold-600 font-medium">Starting ₹1,899</div>
                    </div>
                </div>
                <div class="group cursor-pointer transform hover:scale-105 transition-all duration-300">
                    <div class="bg-gradient-to-br from-pink-100 to-pink-200 rounded-xl p-8 text-center hover:from-pink-200 hover:to-pink-300 transition-all duration-300 shadow-lg hover:shadow-xl border border-pink-200/50">
                        <div class="w-16 h-16 bg-gradient-to-br from-pink-400 to-pink-600 rounded-full flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition-transform shadow-lg">
                            <div class="text-2xl">💄</div>
                        </div>
                        <h3 class="text-xl font-serif font-semibold text-gray-800 mb-2">Lipstick</h3>
                        <p class="text-gray-600">Bold & beautiful colors 💋</p>
                        <div class="mt-3 text-sm text-pink-600 font-medium">Starting ₹299</div>
                    </div>
                </div>
                <div class="group cursor-pointer transform hover:scale-105 transition-all duration-300">
                    <div class="bg-gradient-to-br from-purple-100 to-purple-200 rounded-xl p-8 text-center hover:from-purple-200 hover:to-purple-300 transition-all duration-300 shadow-lg hover:shadow-xl border border-purple-200/50">
                        <div class="w-16 h-16 bg-gradient-to-br from-purple-400 to-purple-600 rounded-full flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition-transform shadow-lg">
                            <div class="text-2xl">👁️</div>
                        </div>
                        <h3 class="text-xl font-serif font-semibold text-gray-800 mb-2">Kajol</h3>
                        <p class="text-gray-600">Traditional eye beauty 👀</p>
                        <div class="mt-3 text-sm text-purple-600 font-medium">Starting ₹199</div>
                    </div>
                </div>
                <div class="group cursor-pointer transform hover:scale-105 transition-all duration-300">
                    <div class="bg-gradient-to-br from-blue-100 to-blue-200 rounded-xl p-8 text-center hover:from-blue-200 hover:to-blue-300 transition-all duration-300 shadow-lg hover:shadow-xl border border-blue-200/50">
                        <div class="w-16 h-16 bg-gradient-to-br from-blue-400 to-blue-600 rounded-full flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition-transform shadow-lg">
                            <div class="text-2xl">🦵</div>
                        </div>
                        <h3 class="text-xl font-serif font-semibold text-gray-800 mb-2">Leg Anklets</h3>
                        <p class="text-gray-600">Graceful ankle charm ✨</p>
                        <div class="mt-3 text-sm text-blue-600 font-medium">Starting ₹899</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Shop Section -->
    <section id="shop" class="py-20 bg-beige-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-serif font-bold text-gray-800 mb-4">Our Collection</h2>
                <p class="text-lg text-gray-600">Handpicked pieces for the discerning jewelry lover</p>
            </div>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8" id="products-grid">
                <!-- Products will be populated by JavaScript -->
            </div>
        </div>
    </section>

    <!-- About Us Section -->
    <section id="about" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div>
                    <h2 class="text-4xl font-serif font-bold text-gray-800 mb-6">About Munia's Collection</h2>
                    <p class="text-lg text-gray-600 mb-6 leading-relaxed">
                        Founded with a passion for creating timeless beauty, Munia's Collection has been crafting exquisite handmade jewelry for over a decade. Each piece in our collection is meticulously designed and handcrafted by skilled artisans who pour their heart and soul into every creation.
                    </p>
                    <p class="text-lg text-gray-600 leading-relaxed">
                        We believe that jewelry is more than just an accessory – it's a reflection of your unique story, your dreams, and your most precious moments. That's why we use only the finest materials and time-honored techniques to create pieces that will be treasured for generations.
                    </p>
                </div>
                <div class="flex justify-center">
                    <div class="relative">
                        <div class="w-80 h-80 bg-gradient-to-br from-beige-200 to-beige-300 rounded-lg flex items-center justify-center shadow-lg">
                            <svg class="w-32 h-32 text-gold-500" fill="currentColor" viewBox="0 0 24 24">
                                <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
                            </svg>
                        </div>
                        <div class="absolute -top-4 -right-4 w-16 h-16 bg-gold-400 rounded-full opacity-30"></div>
                        <div class="absolute -bottom-4 -left-4 w-12 h-12 bg-beige-400 rounded-full opacity-50"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="py-20 bg-beige-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-serif font-bold text-gray-800 mb-4">What Our Customers Say</h2>
                <p class="text-lg text-gray-600">Hear from those who've experienced our craftsmanship</p>
            </div>
            <div class="relative">
                <div id="testimonials-container" class="overflow-hidden">
                    <div id="testimonials-track" class="flex transition-transform duration-500 ease-in-out">
                        <div class="w-full flex-shrink-0 px-4">
                            <div class="bg-white rounded-lg p-8 shadow-lg text-center max-w-2xl mx-auto">
                                <div class="flex justify-center mb-4">
                                    <div class="flex space-x-1">
                                        <svg class="w-5 h-5 text-gold-500" fill="currentColor" viewBox="0 0 20 20">
                                            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                                        </svg>
                                        <svg class="w-5 h-5 text-gold-500" fill="currentColor" viewBox="0 0 20 20">
                                            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                                        </svg>
                                        <svg class="w-5 h-5 text-gold-500" fill="currentColor" viewBox="0 0 20 20">
                                            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                                        </svg>
                                        <svg class="w-5 h-5 text-gold-500" fill="currentColor" viewBox="0 0 20 20">
                                            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                                        </svg>
                                        <svg class="w-5 h-5 text-gold-500" fill="currentColor" viewBox="0 0 20 20">
                                            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                                        </svg>
                                    </div>
                                </div>
                                <p class="text-lg text-gray-600 mb-6 italic">"The craftsmanship is absolutely stunning! I've received so many compliments on my necklace. It's clear that each piece is made with love and attention to detail."</p>
                                <h4 class="font-serif font-semibold text-gray-800">Sarah Johnson</h4>
                                <p class="text-gray-500">Verified Customer</p>
                            </div>
                        </div>
                        <div class="w-full flex-shrink-0 px-4">
                            <div class="bg-white rounded-lg p-8 shadow-lg text-center max-w-2xl mx-auto">
                                <div class="flex justify-center mb-4">
                                    <div class="flex space-x-1">
                                        <svg class="w-5 h-5 text-gold-500" fill="currentColor" viewBox="0 0 20 20">
                                            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                                        </svg>
                                        <svg class="w-5 h-5 text-gold-500" fill="currentColor" viewBox="0 0 20 20">
                                            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                                        </svg>
                                        <svg class="w-5 h-5 text-gold-500" fill="currentColor" viewBox="0 0 20 20">
                                            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                                        </svg>
                                        <svg class="w-5 h-5 text-gold-500" fill="currentColor" viewBox="0 0 20 20">
                                            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                                        </svg>
                                        <svg class="w-5 h-5 text-gold-500" fill="currentColor" viewBox="0 0 20 20">
                                            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                                        </svg>
                                    </div>
                                </div>
                                <p class="text-lg text-gray-600 mb-6 italic">"I bought my engagement ring here and it exceeded all expectations. The quality is exceptional and the customer service was outstanding. Highly recommended!"</p>
                                <h4 class="font-serif font-semibold text-gray-800">Michael Chen</h4>
                                <p class="text-gray-500">Verified Customer</p>
                            </div>
                        </div>
                        <div class="w-full flex-shrink-0 px-4">
                            <div class="bg-white rounded-lg p-8 shadow-lg text-center max-w-2xl mx-auto">
                                <div class="flex justify-center mb-4">
                                    <div class="flex space-x-1">
                                        <svg class="w-5 h-5 text-gold-500" fill="currentColor" viewBox="0 0 20 20">
                                            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                                        </svg>
                                        <svg class="w-5 h-5 text-gold-500" fill="currentColor" viewBox="0 0 20 20">
                                            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                                        </svg>
                                        <svg class="w-5 h-5 text-gold-500" fill="currentColor" viewBox="0 0 20 20">
                                            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                                        </svg>
                                        <svg class="w-5 h-5 text-gold-500" fill="currentColor" viewBox="0 0 20 20">
                                            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                                        </svg>
                                        <svg class="w-5 h-5 text-gold-500" fill="currentColor" viewBox="0 0 20 20">
                                            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                                        </svg>
                                    </div>
                                </div>
                                <p class="text-lg text-gray-600 mb-6 italic">"Beautiful, unique pieces that make perfect gifts. I've ordered multiple times and each piece has been flawless. The packaging is also gorgeous!"</p>
                                <h4 class="font-serif font-semibold text-gray-800">Emma Rodriguez</h4>
                                <p class="text-gray-500">Verified Customer</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="flex justify-center mt-8 space-x-2">
                    <button id="prev-testimonial" class="p-2 rounded-full bg-gold-500 text-white hover:bg-gold-600 transition-colors">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"></path>
                        </svg>
                    </button>
                    <button id="next-testimonial" class="p-2 rounded-full bg-gold-500 text-white hover:bg-gold-600 transition-colors">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path>
                        </svg>
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact" class="bg-gray-800 text-white py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <div>
                    <h3 class="text-2xl font-script font-bold text-gold-400 mb-4">Munia's Collection</h3>
                    <p class="text-gray-300 mb-4">Crafting timeless elegance, one piece at a time.</p>
                    <div class="flex space-x-4">
                        <a href="https://instagram.com/muniascollection" target="_blank" class="text-gray-300 hover:text-gold-400 transition-colors">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                                <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                            </svg>
                        </a>
                    </div>
                </div>
                <div>
                    <h4 class="text-lg font-serif font-semibold mb-4">Contact Info</h4>
                    <div class="space-y-2 text-gray-300">
                        <p>📧 deysubh1637@gmail.com</p>
                        <p>📞 +91 6289029627</p>
                        <p>📍 2/60, Sree Colony, Kolkata - 700092</p>
                    </div>
                    <a href="https://wa.me/916289029627" target="_blank" class="inline-flex items-center mt-4 bg-green-600 hover:bg-green-700 text-white px-4 py-2 rounded-lg transition-colors">
                        <svg class="w-5 h-5 mr-2" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893A11.821 11.821 0 0020.885 3.488"/>
                        </svg>
                        WhatsApp Us
                    </a>
                </div>
                <div>
                    <h4 class="text-lg font-serif font-semibold mb-4">Quick Links</h4>
                    <div class="space-y-2">
                        <a href="#home" class="block text-gray-300 hover:text-gold-400 transition-colors">Home</a>
                        <a href="#collections" class="block text-gray-300 hover:text-gold-400 transition-colors">Collections</a>
                        <a href="#shop" class="block text-gray-300 hover:text-gold-400 transition-colors">Shop</a>
                        <a href="#about" class="block text-gray-300 hover:text-gold-400 transition-colors">About</a>
                    </div>
                </div>
                <div>
                    <h4 class="text-lg font-serif font-semibold mb-4">Newsletter</h4>
                    <p class="text-gray-300 mb-4">Subscribe for exclusive offers and new arrivals</p>
                    <form id="newsletter-form" class="space-y-3">
                        <input type="email" id="newsletter-email" placeholder="Your email address" class="w-full px-4 py-2 bg-gray-700 text-white rounded-lg focus:outline-none focus:ring-2 focus:ring-gold-400" required>
                        <button type="submit" class="w-full bg-gold-500 hover:bg-gold-600 text-white px-4 py-2 rounded-lg transition-colors">
                            Subscribe
                        </button>
                    </form>
                </div>
            </div>
            <div class="border-t border-gray-700 mt-12 pt-8 text-center text-gray-300">
                <p>&copy; 2024 Munia's Collection. All rights reserved. | Handcrafted with ❤️</p>
            </div>
        </div>
    </footer>

    <!-- Floating Action Buttons -->
    <div class="fixed bottom-6 right-6 z-40 flex flex-col space-y-3">
        <a href="https://wa.me/916289029627" target="_blank" class="bg-green-500 hover:bg-green-600 text-white p-4 rounded-full shadow-2xl hover:shadow-3xl transition-all duration-300 transform hover:scale-110 animate-bounce">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893A11.821 11.821 0 0020.885 3.488"/>
            </svg>
        </a>
        <button onclick="document.getElementById('shop').scrollIntoView({behavior: 'smooth'})" class="bg-gold-500 hover:bg-gold-600 text-white p-4 rounded-full shadow-2xl hover:shadow-3xl transition-all duration-300 transform hover:scale-110 animate-pulse">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4m0 0L7 13m0 0l-1.5 6M7 13l-1.5 6m0 0h9m-9 0h9"></path>
            </svg>
        </button>
    </div>

    <!-- Cart Modal -->
    <div id="cart-modal" class="fixed inset-0 bg-black bg-opacity-60 z-50 hidden backdrop-blur-sm">
        <div class="flex items-center justify-center min-h-screen p-4">
            <div class="bg-white rounded-2xl max-w-md w-full max-h-96 overflow-y-auto shadow-2xl border-2 border-gold-200">
                <div class="p-6">
                    <div class="flex justify-between items-center mb-6">
                        <div class="flex items-center space-x-2">
                            <span class="text-2xl">🛒</span>
                            <h3 class="text-2xl font-serif font-bold text-transparent bg-clip-text bg-gradient-to-r from-gold-500 to-gold-600">Shopping Cart</h3>
                        </div>
                        <button id="close-cart" class="text-gray-500 hover:text-red-500 p-2 rounded-full hover:bg-red-50 transition-all duration-300">
                            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                            </svg>
                        </button>
                    </div>
                    <div id="cart-items" class="space-y-4">
                        <!-- Cart items will be populated here -->
                    </div>
                    <div class="border-t-2 border-gold-200 pt-6 mt-6">
                        <div class="flex justify-between items-center mb-6">
                            <span class="text-xl font-serif font-semibold">Total Amount:</span>
                            <span id="cart-total" class="text-2xl font-serif font-bold text-transparent bg-clip-text bg-gradient-to-r from-green-500 to-green-600">₹0</span>
                        </div>
                        <button id="checkout-btn" class="w-full bg-gradient-to-r from-gold-500 to-gold-600 hover:from-gold-600 hover:to-gold-700 text-white py-4 px-6 rounded-xl transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-xl font-bold text-lg">
                            🚀 Proceed to Checkout
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Product data
        const products = [
            { id: 1, name: "Golden Sunset Necklace", price: 2499, category: "necklace", emoji: "📿" },
            { id: 2, name: "Pearl Drop Earrings", price: 1899, category: "earrings", emoji: "👂" },
            { id: 3, name: "Matte Red Lipstick", price: 299, category: "lipstick", emoji: "💄" },
            { id: 4, name: "Traditional Black Kajol", price: 199, category: "kajol", emoji: "👁️" },
            { id: 5, name: "Crystal Cascade Necklace", price: 3499, category: "necklace", emoji: "📿" },
            { id: 6, name: "Diamond Stud Earrings", price: 4299, category: "earrings", emoji: "👂" },
            { id: 7, name: "Rose Gold Anklet", price: 899, category: "anklet", emoji: "🦵" },
            { id: 8, name: "Glossy Pink Lipstick", price: 349, category: "lipstick", emoji: "💄" }
        ];

        // Cart functionality
        let cart = [];

        function updateCartCount() {
            const cartCount = document.getElementById('cart-count');
            cartCount.textContent = cart.reduce((sum, item) => sum + item.quantity, 0);
        }

        function updateCartTotal() {
            const total = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
            document.getElementById('cart-total').textContent = `₹${total.toLocaleString('en-IN')}`;
        }

        function addToCart(productId) {
            const product = products.find(p => p.id === productId);
            const existingItem = cart.find(item => item.id === productId);
            
            if (existingItem) {
                existingItem.quantity += 1;
            } else {
                cart.push({ ...product, quantity: 1 });
            }
            
            updateCartCount();
            updateCartDisplay();
            
            // Show success message
            showNotification('Item added to cart!');
        }

        function removeFromCart(productId) {
            cart = cart.filter(item => item.id !== productId);
            updateCartCount();
            updateCartDisplay();
        }

        function updateCartDisplay() {
            const cartItems = document.getElementById('cart-items');
            
            if (cart.length === 0) {
                cartItems.innerHTML = '<p class="text-gray-500 text-center py-4">Your cart is empty</p>';
                updateCartTotal();
                return;
            }
            
            cartItems.innerHTML = cart.map(item => `
                <div class="flex justify-between items-center p-3 bg-gray-50 rounded-lg">
                    <div>
                        <h4 class="font-medium">${item.name}</h4>
                        <p class="text-sm text-gray-600">₹${item.price.toLocaleString('en-IN')} x ${item.quantity}</p>
                    </div>
                    <button onclick="removeFromCart(${item.id})" class="text-red-500 hover:text-red-700">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"></path>
                        </svg>
                    </button>
                </div>
            `).join('');
            
            updateCartTotal();
        }

        function showNotification(message) {
            const notification = document.createElement('div');
            notification.className = 'fixed top-4 right-4 bg-green-500 text-white px-6 py-3 rounded-lg shadow-lg z-50 transform translate-x-full transition-transform duration-300';
            notification.textContent = message;
            document.body.appendChild(notification);
            
            setTimeout(() => {
                notification.classList.remove('translate-x-full');
            }, 100);
            
            setTimeout(() => {
                notification.classList.add('translate-x-full');
                setTimeout(() => {
                    document.body.removeChild(notification);
                }, 300);
            }, 3000);
        }

        // Render products
        function renderProducts() {
            const productsGrid = document.getElementById('products-grid');
            productsGrid.innerHTML = products.map(product => {
                const categoryColors = {
                    necklace: 'from-gold-100 via-beige-200 to-gold-200',
                    earrings: 'from-gold-100 via-beige-200 to-gold-200',
                    lipstick: 'from-pink-100 via-pink-200 to-pink-300',
                    kajol: 'from-purple-100 via-purple-200 to-purple-300',
                    anklet: 'from-blue-100 via-blue-200 to-blue-300'
                };
                
                const buttonColors = {
                    necklace: 'from-gold-500 to-gold-600 hover:from-gold-600 hover:to-gold-700',
                    earrings: 'from-gold-500 to-gold-600 hover:from-gold-600 hover:to-gold-700',
                    lipstick: 'from-pink-500 to-pink-600 hover:from-pink-600 hover:to-pink-700',
                    kajol: 'from-purple-500 to-purple-600 hover:from-purple-600 hover:to-purple-700',
                    anklet: 'from-blue-500 to-blue-600 hover:from-blue-600 hover:to-blue-700'
                };
                
                return `
                <div class="bg-white rounded-2xl shadow-xl overflow-hidden hover:shadow-2xl transition-all duration-500 transform hover:scale-105 hover:-rotate-1 border-2 border-transparent hover:border-gradient-to-r group">
                    <div class="relative h-64 bg-gradient-to-br ${categoryColors[product.category]} flex items-center justify-center overflow-hidden">
                        <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/30 to-transparent animate-shimmer-fast"></div>
                        <div class="text-8xl animate-bounce-slow group-hover:scale-110 transition-transform duration-300">${product.emoji}</div>
                        <div class="absolute top-3 right-3 bg-gradient-to-r from-red-400 to-red-500 text-white text-xs px-3 py-1 rounded-full animate-pulse shadow-lg">
                            🔥 HOT
                        </div>
                        <div class="absolute bottom-3 left-3 bg-white/90 backdrop-blur-sm text-gray-800 text-xs px-2 py-1 rounded-full font-medium">
                            ⚡ Fast Delivery
                        </div>
                    </div>
                    <div class="p-6 bg-gradient-to-b from-white to-gray-50">
                        <h3 class="text-xl font-serif font-bold text-gray-800 mb-3 group-hover:text-transparent group-hover:bg-clip-text group-hover:bg-gradient-to-r group-hover:from-purple-600 group-hover:to-pink-600 transition-all duration-300">${product.name}</h3>
                        <div class="flex items-center justify-between mb-4">
                            <div class="flex flex-col">
                                <p class="text-3xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-green-500 to-green-600">₹${product.price.toLocaleString('en-IN')}</p>
                                <p class="text-sm text-gray-500 line-through">₹${Math.round(product.price * 1.3).toLocaleString('en-IN')}</p>
                            </div>
                            <div class="flex flex-col items-end">
                                <div class="flex text-yellow-400 text-lg">
                                    ${'★'.repeat(5)}
                                </div>
                                <p class="text-xs text-gray-500 mt-1">4.9 (127 reviews)</p>
                            </div>
                        </div>
                        <div class="flex gap-2 mb-4">
                            <span class="bg-green-100 text-green-800 text-xs px-2 py-1 rounded-full">✅ In Stock</span>
                            <span class="bg-blue-100 text-blue-800 text-xs px-2 py-1 rounded-full">🚚 Free Shipping</span>
                        </div>
                        <button onclick="addToCart(${product.id})" class="w-full bg-gradient-to-r ${buttonColors[product.category]} text-white py-4 px-6 rounded-xl transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-2xl font-bold text-lg group-hover:animate-pulse">
                            🛒 Add to Cart - Buy Now!
                        </button>
                    </div>
                </div>
            `;
            }).join('');
        }

        // Testimonials carousel
        let currentTestimonial = 0;
        const totalTestimonials = 3;

        function showTestimonial(index) {
            const track = document.getElementById('testimonials-track');
            track.style.transform = `translateX(-${index * 100}%)`;
        }

        function nextTestimonial() {
            currentTestimonial = (currentTestimonial + 1) % totalTestimonials;
            showTestimonial(currentTestimonial);
        }

        function prevTestimonial() {
            currentTestimonial = (currentTestimonial - 1 + totalTestimonials) % totalTestimonials;
            showTestimonial(currentTestimonial);
        }

        // Event listeners
        document.addEventListener('DOMContentLoaded', function() {
            renderProducts();
            updateCartDisplay();

            // Mobile menu toggle
            document.getElementById('mobile-menu-btn').addEventListener('click', function() {
                const mobileMenu = document.getElementById('mobile-menu');
                mobileMenu.classList.toggle('hidden');
            });

            // Cart modal
            document.getElementById('cart-btn').addEventListener('click', function() {
                document.getElementById('cart-modal').classList.remove('hidden');
            });

            document.getElementById('close-cart').addEventListener('click', function() {
                document.getElementById('cart-modal').classList.add('hidden');
            });

            // Testimonials navigation
            document.getElementById('next-testimonial').addEventListener('click', nextTestimonial);
            document.getElementById('prev-testimonial').addEventListener('click', prevTestimonial);

            // Auto-rotate testimonials
            setInterval(nextTestimonial, 5000);

            // Newsletter form
            document.getElementById('newsletter-form').addEventListener('submit', function(e) {
                e.preventDefault();
                const email = document.getElementById('newsletter-email').value;
                showNotification('Thank you for subscribing!');
                document.getElementById('newsletter-email').value = '';
            });

            // Checkout button
            document.getElementById('checkout-btn').addEventListener('click', function() {
                if (cart.length === 0) {
                    showNotification('Your cart is empty!');
                    return;
                }
                
                // Create WhatsApp message with cart details
                let message = "🛍️ *New Order from Munia's Collection*\n\n";
                message += "📋 *Order Details:*\n";
                
                cart.forEach((item, index) => {
                    message += `${index + 1}. ${item.name}\n`;
                    message += `   Price: ₹${item.price.toLocaleString('en-IN')}\n`;
                    message += `   Quantity: ${item.quantity}\n`;
                    message += `   Subtotal: ₹${(item.price * item.quantity).toLocaleString('en-IN')}\n\n`;
                });
                
                const total = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
                message += `💰 *Total Amount: ₹${total.toLocaleString('en-IN')}*\n\n`;
                message += "📞 Please confirm this order and provide delivery details.\n";
                message += "🚚 We offer free shipping across India!\n\n";
                message += "Thank you for choosing Munia's Collection! ✨";
                
                // Encode message for WhatsApp URL
                const encodedMessage = encodeURIComponent(message);
                const whatsappURL = `https://wa.me/916289029627?text=${encodedMessage}`;
                
                // Open WhatsApp
                window.open(whatsappURL, '_blank');
                
                // Show success message
                showNotification('Redirecting to WhatsApp for order confirmation!');
                
                // Clear cart after successful checkout
                setTimeout(() => {
                    cart = [];
                    updateCartCount();
                    updateCartDisplay();
                    document.getElementById('cart-modal').classList.add('hidden');
                    showNotification('Order sent! We will contact you soon.');
                }, 2000);
            });

            // Smooth scrolling for navigation links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        target.scrollIntoView({
                            behavior: 'smooth',
                            block: 'start'
                        });
                    }
                    // Close mobile menu if open
                    document.getElementById('mobile-menu').classList.add('hidden');
                });
            });

            // Close cart modal when clicking outside
            document.getElementById('cart-modal').addEventListener('click', function(e) {
                if (e.target === this) {
                    this.classList.add('hidden');
                }
            });
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'96ae2c02b769c203',t:'MTc1NDQ3OTUwOS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
