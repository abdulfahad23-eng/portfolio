<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Muhammad Obiad - Portfolio</title>

    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link
        href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500&family=Inter:wght@400;500;600;700;800&display=swap"
        rel="stylesheet">

    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
</head>

<body class="bg-[#0b101d] text-white min-h-screen flex flex-col overflow-x-hidden font-['Inter',sans-serif]">

    <!-- Navigation Bar -->
    <nav class="w-full max-w-[1480px] mx-auto px-4 md:px-6 py-4 md:py-6 flex items-center justify-between">
        <!-- Logo -->
        <a href="#" class="flex items-center gap-3">
            <!-- Custom SVG Logo matching the screenshot -->
            <svg width="28" height="28" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M12 2L2 22H6L12 10L18 22H22L12 2Z" fill="#14b8e3" />
                <path d="M12 10L6 22H10L12 18L14 22H18L12 10Z" fill="rgba(255,255,255,0.7)" />
            </svg>
            <span class="text-[18px] md:text-[20px] font-bold tracking-wide text-white">Muhammad Obaid</span>
        </a>

        <!-- Desktop Menu Links (hidden on mobile/tablet) -->
        <ul class="hidden lg:flex flex-wrap items-center gap-8 text-[17px] font-semibold text-gray-200">
            <li><a href="#" class="text-white hover:text-[#14b8e3] transition-colors">Home</a></li>
            <li><a href="#" class="hover:text-[#14b8e3] transition-colors">About</a></li>
            <li><a href="#" class="hover:text-[#14b8e3] transition-colors">Skills</a></li>
            <li><a href="#" class="hover:text-[#14b8e3] transition-colors">Resume</a></li>
            <li><a href="#" class="hover:text-[#14b8e3] transition-colors">Services</a></li>
            <li><a href="#" class="hover:text-[#14b8e3] transition-colors">Projects</a></li>
        </ul>

        <!-- Desktop Nav Contact Button (hidden on mobile/tablet) -->
        <a href="https://wa.me/" target="_blank"
            class="hidden lg:inline-block bg-[#14b8e3] hover:bg-[#109cc2] text-white font-bold py-2.5 px-6 rounded text-[14px] transition-colors">
            Contact Me
        </a>

        <!-- Mobile Hamburger Menu Button (visible on mobile/tablet) -->
        <button id="menu-toggle" class="lg:hidden flex flex-col gap-1.5 p-2" aria-label="Toggle menu">
            <span class="w-6 h-0.5 bg-white transition-transform"></span>
            <span class="w-6 h-0.5 bg-white transition-transform"></span>
            <span class="w-6 h-0.5 bg-white transition-transform"></span>
        </button>

        <!-- Mobile Menu Overlay (hidden by default) -->
        <div id="mobile-menu" class="hidden fixed inset-0 bg-[#0b101d]/95 z-50 lg:hidden">
            <div class="flex flex-col items-center justify-center h-full gap-8">
                <button id="menu-close" class="absolute top-6 right-6 p-2" aria-label="Close menu">
                    <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M6 18L18 6M6 6l12 12" />
                    </svg>
                </button>
                <ul class="flex flex-col items-center gap-8 text-[24px] font-semibold text-gray-200">
                    <li><a href="#" class="text-white hover:text-[#14b8e3] transition-colors">Home</a></li>
                    <li><a href="#" class="hover:text-[#14b8e3] transition-colors">About</a></li>
                    <li><a href="#" class="hover:text-[#14b8e3] transition-colors">Skills</a></li>
                    <li><a href="#" class="hover:text-[#14b8e3] transition-colors">Resume</a></li>
                    <li><a href="#" class="hover:text-[#14b8e3] transition-colors">Services</a></li>
                    <li><a href="#" class="hover:text-[#14b8e3] transition-colors">Projects</a></li>
                </ul>
                <a href="https://wa.me/" target="_blank"
                    class="bg-[#14b8e3] hover:bg-[#109cc2] text-white font-bold py-3 px-8 rounded text-[16px] transition-colors mt-4">
                    Contact Me
                </a>
            </div>
        </div>
    </nav>

    <script>
        // Mobile menu toggle functionality
        const menuToggle = document.getElementById('menu-toggle');
        const mobileMenu = document.getElementById('mobile-menu');
        const menuClose = document.getElementById('menu-close');

        menuToggle.addEventListener('click', () => {
            mobileMenu.classList.remove('hidden');
            document.body.style.overflow = 'hidden';
        });

        menuClose.addEventListener('click', () => {
            mobileMenu.classList.add('hidden');
            document.body.style.overflow = 'auto';
        });

        // Close menu when clicking on a link
        const mobileLinks = mobileMenu.querySelectorAll('a');
        mobileLinks.forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
                document.body.style.overflow = 'auto';
            });
        });
    </script>

    <!-- Hero Section -->
    <main
        class="w-full max-w-[1480px] mx-auto px-4 md:px-6 py-12 lg:py-20 flex flex-col lg:flex-row items-center justify-between gap-12 lg:gap-[120px] xl:gap-[160px] relative border border-[#29a8ff]/30 rounded-xl p-6 sm:p-10 bg-[#0f1525] shadow-[0_0_40px_rgba(41,168,255,0.05)]">
        <!-- Left Side: Text Content -->
        <div class="lg:w-[55%] flex flex-col items-start text-left z-10 w-full ">

            <p class="text-[#14b8e3] text-[15px] tracking-[0.15em] mb-4 font-['Fira_Code',monospace]">
                Hello, I'm
            </p>

            <!-- Precisely controlled font sizes -->
            <h1 class="text-[44px] lg:text-[92px] font-bold text-white leading-[1.1] tracking-tight mb-6 ">
                Muhammad Obaid
            </h1>

            <p class="text-gray-300 text-[16px] leading-relaxed mb-8 max-w-[520px]">
                Turning Data into Intelligent Solutions | Machine Learning • <br class="hidden sm:block">
                Deep Learning • Data Analysis •Model Optimization
            </p>

            <!-- Buttons -->
            <div class="flex flex-wrap items-center gap-4">
                <a href="https://wa.me/" target="_blank"
                    class="bg-[#14b8e3] hover:bg-[#109cc2] text-white font-semibold py-3.5 px-7 rounded flex items-center gap-2 transition-colors text-[15px]">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-5 h-5">
                        <path
                            d="M3.478 2.404a.75.75 0 00-.926.941l2.432 7.905H13.5a.75.75 0 010 1.5H4.984l-2.432 7.905a.75.75 0 00.926.94 60.519 60.519 0 0018.445-8.986.75.75 0 000-1.218A60.517 60.517 0 003.478 2.404z" />
                    </svg>
                    Contact Me
                </a>

                <a href="#"
                    class="bg-transparent hover:bg-blue-500 border border-[#2a3852] hover:border-[#14b8e3] text-white font-semibold py-3.5 px-7 rounded flex items-center gap-2 transition-colors text-[15px]">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"
                        class="w-5 h-5 text-[#14b8e3] ">
                        <path fill-rule="evenodd"
                            d="M9.315 7.584C12.195 3.883 16.695 1.5 21.5 1.5a.75.75 0 01.75.75c0 5.056-2.283 9.437-5.986 12.188-1.51.115-3.042.16-4.597.16-1.597 0-3.174-.047-4.726-.168A14.966 14.966 0 014.28 17.5l-1.956 1.955a.75.75 0 01-1.27-.53v-2.025C.324 15.023 0 13.047 0 11.002c0-1.555.045-3.087.16-4.597.114-1.513.27-3.003.468-4.462A14.957 14.957 0 013.111 4.54l1.956-1.955a.75.75 0 011.06 0l2.025 2.025c.571-.242 1.157-.457 1.753-.642zm-5.46 9.07l1.096-1.096a16.48 16.48 0 01-1.096 1.096z"
                            clip-rule="evenodd" />
                    </svg>
                    View Projects
                </a>
            </div>
        </div>

        <!-- Right Side: Graphic & Image -->
        <div class="lg:w-[45%] flex justify-center lg:justify-end items-center mt-20 lg:mt-0 relative w-full pr-4">

            <!-- Concentric Rings Setup -->
            <div class="relative w-[340px] h-[340px] flex items-center justify-center">

                <!-- 1. Outer Thin Cyan Ring -->
                <div class="absolute w-[100%] h-[100%] rounded-full border-[1.5px] border-[#14b8e3]/30"></div>

                <!-- 2. Middle Thick Cyan Ring -->
                <div class="absolute w-[90%] h-[90%] rounded-full border-[4px] border-[#14b8e3]"></div>

                <!-- 3. Inner White/Gray Circle for Image -->
                <div
                    class="absolute w-[82%] h-[82%] bg-[#f2f2f2] rounded-full overflow-hidden flex items-end justify-center">
                    <!-- Image placeholder fitting perfectly at the bottom -->
                    <img src="/WhatsApp Image 2026-05-01 at 5.20.32 AM (1).jpeg" alt="Muhammad Obaid"
                        class="w-[85%] h-auto object-cover translate-y-2">
                </div>

                <!-- 4. Floating Badges -->

                <!-- Flutter Developer Badge (Top Left) -->


                <!-- App Developer Badge (Bottom Right) -->
                <div class="absolute bottom-[10%] right-[0%] z-20">
                    <!-- WhatsApp Link to WA.me -->
                    <div
                        class="bg-[#a855f7] text-white text-[14px] font-bold py-2 px-4 rounded shadow-lg whitespace-nowrap">
                        Machine Learner
                    </div>
                </div>

            </div>
        </div>
    </main>

    <!-- Floating WhatsApp Icon Link -->
    <!-- Replace the href with your actual whatsapp number e.g. https://wa.me/1234567890 -->
    <a href="https://wa.me/" target="_blank" rel="noopener noreferrer"
        class="fixed bottom-8 right-8 bg-[#25D366] text-white p-[15px] rounded-full shadow-[0_4px_14px_rgba(37,211,102,0.4)] hover:-translate-y-1 transition-transform duration-300 z-50">
        <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="currentColor" viewBox="0 0 16 16">
            <path
                d="M13.601 2.326A7.854 7.854 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.933 7.933 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93A7.898 7.898 0 0 0 13.6 2.326zM7.994 14.521a6.573 6.573 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.557 6.557 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592zm3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.099-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.729.729 0 0 0-.529.247c-.182.198-.691.677-.691 1.654 0 .977.71 1.916.81 2.049.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232z" />
        </svg>
    </a>

    <!-- Main Background -->

    <body class="bg-[#0b101e] text-white min-h-screen flex items-center justify-center p-4 sm:p-8">

        <!-- Container / "Page" Wrapper with Border and Gap -->
        <!-- Added border, rounded corners, padding, and full width for the second page -->
        <div
            class="w-full flex flex-col lg:flex-row items-center justify-between gap-16 lg:gap-[120px] xl:gap-[160px] border border-[#29a8ff]/30 rounded-xl p-8 sm:p-12 lg:p-20 shadow-[0_0_40px_rgba(41,168,255,0.05)] bg-[#0f1525]">

            <!-- Left Column: Image Section -->
            <div class="relative flex justify-center items-center w-full lg:w-[40%]">

                <!-- Outer Glowing Ring -->
                <div
                    class="relative w-[280px] h-[280px] sm:w-[350px] sm:h-[350px] lg:w-[420px] lg:h-[420px] rounded-full border-[3px] border-[#29a8ff] shadow-[0_0_30px_rgba(41,168,255,0.15)] p-2 sm:p-3 flex items-center justify-center">

                    <!-- Inner Ring -->
                    <div
                        class="w-full h-full rounded-full border border-[#29a8ff]/40 p-2 sm:p-3 flex items-center justify-center">

                        <!-- Profile Image Container -->
                        <div class="w-full h-full rounded-full overflow-hidden bg-[#1a233a]">
                            <!-- REPLACE THE SRC ATTRIBUTE BELOW WITH YOUR ACTUAL IMAGE LINK -->
                            <img src="/WhatsApp Image 2026-05-01 at 5.20.32 AM (1).jpeg" alt="Muhammad Obaid"
                                class="w-full h-full object-cover">

                        </div>

                    </div>
                </div>

                <!-- Floating Badge: Flutter Developer -->
                <div
                    class="absolute top-[12%] left-[-5%] sm:left-[0%] lg:left-[-10%] bg-[#29a8ff] text-white text-xs sm:text-sm font-bold py-2 px-5 rounded-md shadow-lg z-10 tracking-wide">
                    Machine Learner
                </div>

                <!-- Floating Badge: App Developer -->
                <div
                    class="absolute bottom-[12%] right-[-5%] sm:right-[0%] lg:right-[-10%] bg-[#8c38ff] text-white text-xs sm:text-sm font-bold py-2 px-5 rounded-md shadow-lg z-10 tracking-wide">
                    Python Expert
                </div>

            </div>

            <!-- Right Column: Text Section -->
            <div class="w-full lg:w-[60%] flex flex-col gap-6 lg:gap-8 text-center lg:text-left">

                <!-- Main Heading -->
                <h1 class="text-4xl sm:text-5xl lg:text-[64px] font-bold tracking-tight">
                    About <span class="text-[#29a8ff]">Me</span>
                </h1>

                <!-- Sub Heading -->
                <h2 class="text-2xl sm:text-3xl lg:text-[32px] font-bold leading-tight">
                    I'm <span class="text-[#29a8ff]">Muhammad Obaid</span>, Solving Complex Problems with Machine
                    Learning
                </h2>

                <!-- Paragraph -->
                <p class="text-[#a1abbd] leading-loose text-sm sm:text-base lg:text-lg font-normal">
                    I am a passionate Machine Learning Expert who specializes in transforming complex data into
                    intelligent, high-impact solutions. I focus on building scalable, data-driven models with strong
                    accuracy and real-world applicability. With hands-on experience in Python, TensorFlow, Scikit-learn,
                    and deep learning frameworks, I develop end-to-end solutions—from data preprocessing and model
                    training to deployment and performance optimization. I am committed to writing efficient algorithms,
                    solving real-world problems, and continuously improving model performance and user outcomes.
                </p>

                <!-- Button Container -->
                <div class="mt-4 flex justify-center lg:justify-start">
                    <a href="#"
                        class="inline-flex items-center gap-2 bg-[#29a8ff] hover:bg-[#1f8cdd] transition-all duration-300 hover:scale-105 text-white font-semibold py-3.5 px-8 rounded-md shadow-lg shadow-[#29a8ff]/30 text-sm sm:text-base">
                        Download CV
                        <!-- SVG Download Icon -->
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2.5"
                            stroke="currentColor" class="w-5 h-5">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M3 16.5v2.25A2.25 2.25 0 0 0 5.25 21h13.5A2.25 2.25 0 0 0 21 18.75V16.5M16.5 12 12 16.5m0 0L7.5 12m4.5 4.5V3" />
                        </svg>
                    </a>
                </div>

            </div>
        </div>
        <!-- Machine Learning Skills Section Start -->
        <section
            class="bg-[#0a0f1c] py-16 px-4 md:px-8 font-sans  border-[#0ea5e9] border border-[#29a8ff]/30 rounded-xl p-6 sm:p-10 bg-[#0f1525] shadow-[0_0_40px_rgba(41,168,255,0.05)] ">

            <!-- Section Title -->
            <div class="text-center mb-16  ">
                <h2 class="text-4xl font-bold text-white tracking-wide">
                    My <span class="text-[#0ea5e9]">Skills</span>
                </h2>
            </div>

            <!-- Skills Grid -->
            <div class="max-w-6xl mx-auto grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-10">

                <!-- Skill 1: Python -->
                <div
                    class="bg-[#131b2f] border border-[#1e293b] rounded-xl p-10 flex flex-col items-center shadow-lg transition-transform hover:-translate-y-1 duration-300">
                    <!-- Icon -->
                    <div
                        class="w-14 h-14 bg-gradient-to-br from-[#1e293b] to-[#131b2f] rounded-2xl flex items-center justify-center mb-5 shadow-inner">
                        <svg class="w-7 h-7 text-[#3b82f6]" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                            xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"></path>
                        </svg>
                    </div>
                    <!-- Title -->
                    <h3 class="text-white font-semibold text-base mb-6">Python</h3>
                    <!-- Progress Bar -->
                    <div class="w-full bg-[#2a354d] rounded-full h-[6px] mb-2">
                        <div class="bg-[#2563eb] h-full rounded-full" style="width: 95%"></div>
                    </div>
                    <p class="text-slate-400 text-[11px] font-bold tracking-wider">Proficiency: 95%</p>
                </div>

                <!-- Skill 2: TensorFlow -->
                <div
                    class="bg-[#131b2f] border border-[#1e293b] rounded-xl p-6 flex flex-col items-center shadow-lg transition-transform hover:-translate-y-1 duration-300">
                    <!-- Icon -->
                    <div
                        class="w-14 h-14 bg-gradient-to-br from-[#1e293b] to-[#131b2f] rounded-2xl flex items-center justify-center mb-5 shadow-inner">
                        <svg class="w-7 h-7 text-[#f59e0b]" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                            xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M13 10V3L4 14h7v7l9-11h-7z"></path>
                        </svg>
                    </div>
                    <!-- Title -->
                    <h3 class="text-white font-semibold text-base mb-6">TensorFlow</h3>
                    <!-- Progress Bar -->
                    <div class="w-full bg-[#2a354d] rounded-full h-[6px] mb-2">
                        <div class="bg-[#eab308] h-full rounded-full" style="width: 85%"></div>
                    </div>
                    <p class="text-slate-400 text-[11px] font-bold tracking-wider">Proficiency: 85%</p>
                </div>

                <!-- Skill 3: PyTorch -->
                <div
                    class="bg-[#131b2f] border border-[#1e293b] rounded-xl p-6 flex flex-col items-center shadow-lg transition-transform hover:-translate-y-1 duration-300">
                    <!-- Icon -->
                    <div
                        class="w-14 h-14 bg-gradient-to-br from-[#1e293b] to-[#131b2f] rounded-2xl flex items-center justify-center mb-5 shadow-inner">
                        <svg class="w-7 h-7 text-[#ef4444]" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                            xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M17.657 18.657A8 8 0 016.343 7.343S7 9 9 10c0-2 .5-5 2.986-7C14 5 16.09 5.777 17.656 7.343A7.975 7.975 0 0120 13a7.975 7.975 0 01-2.343 5.657z">
                            </path>
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M9.879 16.121A3 3 0 1012.015 11L11 14H9c0 .768.293 1.536.879 2.121z"></path>
                        </svg>
                    </div>
                    <!-- Title -->
                    <h3 class="text-white font-semibold text-base mb-6">PyTorch</h3>
                    <!-- Progress Bar -->
                    <div class="w-full bg-[#2a354d] rounded-full h-[6px] mb-2">
                        <div class="bg-[#ef4444] h-full rounded-full" style="width: 80%"></div>
                    </div>
                    <p class="text-slate-400 text-[11px] font-bold tracking-wider">Proficiency: 80%</p>
                </div>

                <!-- Skill 4: Scikit-Learn -->
                <div
                    class="bg-[#131b2f] border border-[#1e293b] rounded-xl p-6 flex flex-col items-center shadow-lg transition-transform hover:-translate-y-1 duration-300">
                    <!-- Icon -->
                    <div
                        class="w-14 h-14 bg-gradient-to-br from-[#1e293b] to-[#131b2f] rounded-2xl flex items-center justify-center mb-5 shadow-inner">
                        <svg class="w-7 h-7 text-[#38bdf8]" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                            xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z">
                            </path>
                        </svg>
                    </div>
                    <!-- Title -->
                    <h3 class="text-white font-semibold text-base mb-6">Scikit-Learn</h3>
                    <!-- Progress Bar -->
                    <div class="w-full bg-[#2a354d] rounded-full h-[6px] mb-2">
                        <div class="bg-[#38bdf8] h-full rounded-full" style="width: 90%"></div>
                    </div>
                    <p class="text-slate-400 text-[11px] font-bold tracking-wider">Proficiency: 90%</p>
                </div>

                <!-- Skill 5: Data Preprocessing -->
                <div
                    class="bg-[#131b2f] border border-[#1e293b] rounded-xl p-6 flex flex-col items-center shadow-lg transition-transform hover:-translate-y-1 duration-300">
                    <!-- Icon -->
                    <div
                        class="w-14 h-14 bg-gradient-to-br from-[#1e293b] to-[#131b2f] rounded-2xl flex items-center justify-center mb-5 shadow-inner">
                        <svg class="w-7 h-7 text-[#2563eb]" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                            xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4m0 5c0 2.21-3.582 4-8 4s-8-1.79-8-4">
                            </path>
                        </svg>
                    </div>
                    <!-- Title -->
                    <h3 class="text-white font-semibold text-base mb-6">Data Preprocessing</h3>
                    <!-- Progress Bar -->
                    <div class="w-full bg-[#2a354d] rounded-full h-[6px] mb-2">
                        <div class="bg-[#2563eb] h-full rounded-full" style="width: 88%"></div>
                    </div>
                    <p class="text-slate-400 text-[11px] font-bold tracking-wider">Proficiency: 88%</p>
                </div>

                <!-- Skill 6: Deep Learning -->
                <div
                    class="bg-[#131b2f] border border-[#1e293b] rounded-xl p-6 flex flex-col items-center shadow-lg transition-transform hover:-translate-y-1 duration-300">
                    <!-- Icon -->
                    <div
                        class="w-14 h-14 bg-gradient-to-br from-[#1e293b] to-[#131b2f] rounded-2xl flex items-center justify-center mb-5 shadow-inner">
                        <svg class="w-7 h-7 text-[#10b981]" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                            xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M14 10l-2 1m0 0l-2-1m2 1v2.5M20 7l-2 1m2-1l-2-1m2 1v2.5M14 4l-2-1-2 1M4 7l2-1M4 7l2 1M4 7v2.5M12 21l-2-1m2 1l2-1m-2 1v-2.5M6 18l-2-1v-2.5M18 18l2-1v-2.5">
                            </path>
                        </svg>
                    </div>
                    <!-- Title -->
                    <h3 class="text-white font-semibold text-base mb-6">Deep Learning</h3>
                    <!-- Progress Bar -->
                    <div class="w-full bg-[#2a354d] rounded-full h-[6px] mb-2">
                        <div class="bg-[#10b981] h-full rounded-full" style="width: 75%"></div>
                    </div>
                    <p class="text-slate-400 text-[11px] font-bold tracking-wider">Proficiency: 75%</p>
                </div>

                <!-- Skill 7: NLP -->
                <div
                    class="bg-[#131b2f] border border-[#1e293b] rounded-xl p-6 flex flex-col items-center shadow-lg transition-transform hover:-translate-y-1 duration-300">
                    <!-- Icon -->
                    <div
                        class="w-14 h-14 bg-gradient-to-br from-[#1e293b] to-[#131b2f] rounded-2xl flex items-center justify-center mb-5 shadow-inner">
                        <svg class="w-7 h-7 text-[#f97316]" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                            xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M8 10h.01M12 10h.01M16 10h.01M9 16H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-5l-5 5v-5z">
                            </path>
                        </svg>
                    </div>
                    <!-- Title -->
                    <h3 class="text-white font-semibold text-base mb-6">NLP</h3>
                    <!-- Progress Bar -->
                    <div class="w-full bg-[#2a354d] rounded-full h-[6px] mb-2">
                        <div class="bg-[#f97316] h-full rounded-full" style="width: 80%"></div>
                    </div>
                    <p class="text-slate-400 text-[11px] font-bold tracking-wider">Proficiency: 80%</p>
                </div>

                <!-- Skill 8: Computer Vision -->
                <div
                    class="bg-[#131b2f] border border-[#1e293b] rounded-xl p-6 flex flex-col items-center shadow-lg transition-transform hover:-translate-y-1 duration-300">
                    <!-- Icon -->
                    <div
                        class="w-14 h-14 bg-gradient-to-br from-[#1e293b] to-[#131b2f] rounded-2xl flex items-center justify-center mb-5 shadow-inner">
                        <svg class="w-7 h-7 text-[#8b5cf6]" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                            xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z">
                            </path>
                        </svg>
                    </div>
                    <!-- Title -->
                    <h3 class="text-white font-semibold text-base mb-6">Computer Vision</h3>
                    <!-- Progress Bar -->
                    <div class="w-full bg-[#2a354d] rounded-full h-[6px] mb-2">
                        <div class="bg-[#8b5cf6] h-full rounded-full" style="width: 82%"></div>
                    </div>
                    <p class="text-slate-400 text-[11px] font-bold tracking-wider">Proficiency: 82%</p>
                </div>

            </div>
        </section>
        <!-- Machine Learning Skills Section End -->
        <!-- Development Timeline Section Start -->
        <section
            class="bg-[#0B1120] py-20 px-4 md:px-8 font-sans overflow-hidden  border border-[#29a8ff]/30 rounded-xl p-6 sm:p-10 bg-[#0f1525] shadow-[0_0_40px_rgba(41,168,255,0.05)]">
            <div class="text-center mb-16 ">
                <h2 class="text-4xl font-bold text-white tracking-wide">
                    Work <span class="text-[#0ea5e9]"> Process
                </h2>
                <p class="text-slate-400 text-center max-w-2xl mx-auto mb-16 pt-2">
                    A systematic approach to building Machine Learning solutions.
                </p>
            </div>

            <div class="max-w-6xl mx-auto relative">

                <!-- Central Vertical Line (Desktop & Mobile) -->
                <div
                    class="absolute left-[28px] md:left-1/2 top-0 bottom-0 w-[2px] bg-[#1e293b] transform md:-translate-x-1/2">
                </div>

                <!-- TIMELINE ITEM 01: Planning (Left side on desktop) -->
                <div class="relative flex flex-col md:flex-row items-center justify-between mb-16 md:mb-12 group">
                    <!-- Glowing Dot -->
                    <div
                        class="absolute left-[28px] md:left-1/2 top-8 md:top-1/2 w-[10px] h-[10px] bg-[#38bdf8] rounded-full transform -translate-x-1/2 md:-translate-y-1/2 shadow-[0_0_15px_rgba(56,189,248,0.9)] z-10 transition-transform group-hover:scale-150 duration-300">
                    </div>

                    <!-- Content Card -->
                    <div class="w-full md:w-[46%] pl-16 md:pl-0 flex justify-end">
                        <div
                            class="bg-[#111827] border border-[#1e293b] p-6 md:p-8 rounded-xl w-full max-w-xl relative overflow-hidden transition-all duration-300 hover:border-[#38bdf8]/40 hover:bg-[#131b2f]">
                            <!-- Background Number -->
                            <span
                                class="absolute top-2 right-4 text-7xl font-extrabold text-[#1e293b]/50 select-none z-0">01</span>

                            <div class="relative z-10">
                                <!-- Header -->
                                <div class="flex items-center gap-3 mb-4">
                                    <div
                                        class="w-8 h-8 rounded bg-[#1e293b] flex items-center justify-center text-[#38bdf8]">
                                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                                d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z">
                                            </path>
                                        </svg>
                                    </div>
                                    <h3 class="text-white font-bold text-lg tracking-wide">Planning</h3>
                                </div>
                                <!-- Description -->
                                <p class="text-slate-400 text-sm leading-relaxed mb-6 pr-6">
                                    Analyzing requirements, defining project scope, and creating a roadmap for
                                    successful delivery.
                                </p>
                                <!-- Tags -->
                                <div class="flex flex-wrap gap-2">
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Requirement
                                        Analysis</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Feasibility
                                        Study</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Timeline
                                        Estimation</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Resource
                                        Allocation</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <!-- Empty Space -->
                    <div class="hidden md:block w-[46%]"></div>
                </div>

                <!-- TIMELINE ITEM 02: Defining (Right side on desktop) -->
                <div class="relative flex flex-col md:flex-row items-center justify-between mb-16 md:mb-12 group">
                    <div
                        class="absolute left-[28px] md:left-1/2 top-8 md:top-1/2 w-[10px] h-[10px] bg-[#38bdf8] rounded-full transform -translate-x-1/2 md:-translate-y-1/2 shadow-[0_0_15px_rgba(56,189,248,0.9)] z-10 transition-transform group-hover:scale-150 duration-300">
                    </div>

                    <!-- Empty Space -->
                    <div class="hidden md:block w-[46%]"></div>

                    <!-- Content Card -->
                    <div class="w-full md:w-[46%] pl-16 md:pl-0 flex justify-start">
                        <div
                            class="bg-[#111827] border border-[#1e293b] p-6 md:p-8 rounded-xl w-full max-w-xl relative overflow-hidden transition-all duration-300 hover:border-[#38bdf8]/40 hover:bg-[#131b2f]">
                            <span
                                class="absolute top-2 right-4 text-7xl font-extrabold text-[#1e293b]/50 select-none z-0">02</span>
                            <div class="relative z-10">
                                <div class="flex items-center gap-3 mb-4">
                                    <div
                                        class="w-8 h-8 rounded bg-[#1e293b] flex items-center justify-center text-[#38bdf8]">
                                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                                d="M11 5H6a2 2 0 00-2 2v11a2 2 0 002 2h11a2 2 0 002-2v-5m-1.414-9.414a2 2 0 112.828 2.828L11.828 15H9v-2.828l8.586-8.586z">
                                            </path>
                                        </svg>
                                    </div>
                                    <h3 class="text-white font-bold text-lg tracking-wide">Defining</h3>
                                </div>
                                <p class="text-slate-400 text-sm leading-relaxed mb-6 pr-6">
                                    Documenting specifications, outlining features, and establishing clear project
                                    goals.
                                </p>
                                <div class="flex flex-wrap gap-2">
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">UI/UX
                                        Requirements</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Functional
                                        Specs</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Technical
                                        Architecture</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">API
                                        Planning</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- TIMELINE ITEM 03: Designing (Left side on desktop) -->
                <div class="relative flex flex-col md:flex-row items-center justify-between mb-16 md:mb-12 group">
                    <div
                        class="absolute left-[28px] md:left-1/2 top-8 md:top-1/2 w-[10px] h-[10px] bg-[#38bdf8] rounded-full transform -translate-x-1/2 md:-translate-y-1/2 shadow-[0_0_15px_rgba(56,189,248,0.9)] z-10 transition-transform group-hover:scale-150 duration-300">
                    </div>

                    <div class="w-full md:w-[46%] pl-16 md:pl-0 flex justify-end">
                        <div
                            class="bg-[#111827] border border-[#1e293b] p-6 md:p-8 rounded-xl w-full max-w-xl relative overflow-hidden transition-all duration-300 hover:border-[#38bdf8]/40 hover:bg-[#131b2f]">
                            <span
                                class="absolute top-2 right-4 text-7xl font-extrabold text-[#1e293b]/50 select-none z-0">03</span>
                            <div class="relative z-10">
                                <div class="flex items-center gap-3 mb-4">
                                    <div
                                        class="w-8 h-8 rounded bg-[#1e293b] flex items-center justify-center text-[#38bdf8]">
                                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                                d="M7 21a4 4 0 01-4-4V5a2 2 0 012-2h4a2 2 0 012 2v12a4 4 0 01-4 4zm0 0h12a2 2 0 002-2v-4a2 2 0 00-2-2h-2.343M11 7.343l1.657-1.657a2 2 0 012.828 0l2.829 2.829a2 2 0 010 2.828l-8.486 8.485M7 17h.01">
                                            </path>
                                        </svg>
                                    </div>
                                    <h3 class="text-white font-bold text-lg tracking-wide">Designing</h3>
                                </div>
                                <p class="text-slate-400 text-sm leading-relaxed mb-6 pr-6">
                                    Creating intuitive user interfaces, designing databases, and building wireframes.
                                </p>
                                <div class="flex flex-wrap gap-2">
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Wireframe
                                        Design</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Database
                                        Schema</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Component
                                        Architecture</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">User
                                        Flow</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="hidden md:block w-[46%]"></div>
                </div>

                <!-- TIMELINE ITEM 04: Coding (Right side on desktop) -->
                <div class="relative flex flex-col md:flex-row items-center justify-between mb-16 md:mb-12 group">
                    <div
                        class="absolute left-[28px] md:left-1/2 top-8 md:top-1/2 w-[10px] h-[10px] bg-[#38bdf8] rounded-full transform -translate-x-1/2 md:-translate-y-1/2 shadow-[0_0_15px_rgba(56,189,248,0.9)] z-10 transition-transform group-hover:scale-150 duration-300">
                    </div>

                    <div class="hidden md:block w-[46%]"></div>

                    <div class="w-full md:w-[46%] pl-16 md:pl-0 flex justify-start">
                        <div
                            class="bg-[#111827] border border-[#1e293b] p-6 md:p-8 rounded-xl w-full max-w-xl relative overflow-hidden transition-all duration-300 hover:border-[#38bdf8]/40 hover:bg-[#131b2f]">
                            <span
                                class="absolute top-2 right-4 text-7xl font-extrabold text-[#1e293b]/50 select-none z-0">04</span>
                            <div class="relative z-10">
                                <div class="flex items-center gap-3 mb-4">
                                    <div
                                        class="w-8 h-8 rounded bg-[#1e293b] flex items-center justify-center text-[#38bdf8]">
                                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                                d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"></path>
                                        </svg>
                                    </div>
                                    <h3 class="text-white font-bold text-lg tracking-wide">Coding</h3>
                                </div>
                                <p class="text-slate-400 text-sm leading-relaxed mb-6 pr-6">
                                    Implementing features using Flutter, writing clean code, and integrating backend
                                    services.
                                </p>
                                <div class="flex flex-wrap gap-2">
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Frontend
                                        Development</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Backend
                                        Integration</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">State
                                        Management</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">API
                                        Integration</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- TIMELINE ITEM 05: Testing (Left side on desktop) -->
                <div class="relative flex flex-col md:flex-row items-center justify-between mb-16 md:mb-12 group">
                    <div
                        class="absolute left-[28px] md:left-1/2 top-8 md:top-1/2 w-[10px] h-[10px] bg-[#38bdf8] rounded-full transform -translate-x-1/2 md:-translate-y-1/2 shadow-[0_0_15px_rgba(56,189,248,0.9)] z-10 transition-transform group-hover:scale-150 duration-300">
                    </div>

                    <div class="w-full md:w-[46%] pl-16 md:pl-0 flex justify-end">
                        <div
                            class="bg-[#111827] border border-[#1e293b] p-6 md:p-8 rounded-xl w-full max-w-xl relative overflow-hidden transition-all duration-300 hover:border-[#38bdf8]/40 hover:bg-[#131b2f]">
                            <span
                                class="absolute top-2 right-4 text-7xl font-extrabold text-[#1e293b]/50 select-none z-0">05</span>
                            <div class="relative z-10">
                                <div class="flex items-center gap-3 mb-4">
                                    <div
                                        class="w-8 h-8 rounded bg-[#1e293b] flex items-center justify-center text-[#38bdf8]">
                                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                                d="M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z">
                                            </path>
                                        </svg>
                                    </div>
                                    <h3 class="text-white font-bold text-lg tracking-wide">Testing</h3>
                                </div>
                                <p class="text-slate-400 text-sm leading-relaxed mb-6 pr-6">
                                    Performing unit tests, integration testing, and ensuring bug-free functionality.
                                </p>
                                <div class="flex flex-wrap gap-2">
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Unit
                                        Testing</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Widget
                                        Testing</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Debugging</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Quality
                                        Assurance</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="hidden md:block w-[46%]"></div>
                </div>

                <!-- TIMELINE ITEM 06: Deploying (Right side on desktop) -->
                <div class="relative flex flex-col md:flex-row items-center justify-between group">
                    <div
                        class="absolute left-[28px] md:left-1/2 top-8 md:top-1/2 w-[10px] h-[10px] bg-[#38bdf8] rounded-full transform -translate-x-1/2 md:-translate-y-1/2 shadow-[0_0_15px_rgba(56,189,248,0.9)] z-10 transition-transform group-hover:scale-150 duration-300">
                    </div>

                    <div class="hidden md:block w-[46%]"></div>

                    <div class="w-full md:w-[46%] pl-16 md:pl-0 flex justify-start">
                        <div
                            class="bg-[#111827] border border-[#1e293b] p-6 md:p-8 rounded-xl w-full max-w-xl relative overflow-hidden transition-all duration-300 hover:border-[#38bdf8]/40 hover:bg-[#131b2f]">
                            <span
                                class="absolute top-2 right-4 text-7xl font-extrabold text-[#1e293b]/50 select-none z-0">06</span>
                            <div class="relative z-10">
                                <div class="flex items-center gap-3 mb-4">
                                    <div
                                        class="w-8 h-8 rounded bg-[#1e293b] flex items-center justify-center text-[#38bdf8]">
                                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                                d="M13.828 10.172a4 4 0 00-5.656 0l-4 4a4 4 0 105.656 5.656l1.102-1.101m-.758-4.899a4 4 0 005.656 0l4-4a4 4 0 00-5.656-5.656l-1.1 1.1">
                                            </path>
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                                d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064">
                                            </path>
                                        </svg>
                                    </div>
                                    <h3 class="text-white font-bold text-lg tracking-wide">Deploying</h3>
                                </div>
                                <p class="text-slate-400 text-sm leading-relaxed mb-6 pr-6">
                                    Building release APKs, publishing to app stores, and configuring CI/CD pipelines.
                                </p>
                                <div class="flex flex-wrap gap-2">
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">App
                                        Store Submission</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Release
                                        Build</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Performance
                                        Testing</span>
                                    <span
                                        class="px-3 py-1 rounded-full border border-slate-700 bg-slate-800/40 text-slate-300 text-[11px] font-medium">Post-Launch
                                        Support</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </section>
        <!-- Development Timeline Section End -->
        <!-- Education & Experience Section Start -->
        <section class="bg-[#0B1120] py-20 px-4 md:px-8 font-sans">
            <div
                class="max-w-[1480] mx-auto border border-[#29a8ff]/30 rounded-xl p-6 sm:p-10 bg-[#0f1525] shadow-[0_0_40px_rgba(41,168,255,0.05)]">

                <!-- Section Title -->
                <div class="text-center mb-16">
                    <h2 class="text-4xl md:text-5xl font-bold text-white tracking-wide">
                        <span class="text-[#0ea5e9]">Education</span> Experience
                    </h2>
                </div>

                <!-- Main Layout Grid (2 Columns on Desktop) -->
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-16">

                    <!-- ================= COLUMN 1: EDUCATION ================= -->
                    <div>
                        <!-- Column Header -->
                        <div class="flex items-center gap-4 mb-10">
                            <div
                                class="w-14 h-14 bg-[#1e293b] rounded-xl flex items-center justify-center shadow-lg border border-slate-700/50">
                                <!-- Graduation Cap Icon -->
                                <svg class="w-7 h-7 text-slate-400" fill="none" stroke="currentColor"
                                    viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                    <path d="M12 14l9-5-9-5-9 5 9 5z"></path>
                                    <path
                                        d="M12 14l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14z">
                                    </path>
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                        d="M12 14l9-5-9-5-9 5 9 5zm0 0l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14zm-4 6v-7.5l4-2.222">
                                    </path>
                                </svg>
                            </div>
                            <h3 class="text-2xl font-bold text-white tracking-wide">Education</h3>
                        </div>

                        <!-- Timeline Container -->
                        <div class="border-l-2 border-[#1e293b] ml-6 pb-4">

                            <!-- Item 1 -->
                            <div class="relative pl-10 mb-10">
                                <!-- Node Icon -->
                                <div
                                    class="absolute -left-[17px] top-6 w-8 h-8 bg-[#0ea5e9] rounded-md flex items-center justify-center shadow-[0_0_10px_rgba(14,165,233,0.5)]">
                                    <svg class="w-4 h-4 text-white" fill="none" stroke="currentColor"
                                        viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                            d="M12 14l9-5-9-5-9 5 9 5zm0 0l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14zm-4 6v-7.5l4-2.222">
                                        </path>
                                    </svg>
                                </div>
                                <!-- Content Card -->
                                <div
                                    class="bg-[#111827] border border-[#1e293b] rounded-xl py-8 px-6 flex flex-col items-center text-center transition-all duration-300 hover:bg-[#131b2f] hover:border-[#0ea5e9]/30 hover:-translate-y-1">
                                    <h4 class="text-white font-bold text-[17px] mb-2">Bachelor of Artificial
                                        Intelligence</h4>
                                    <p class="text-[#0ea5e9] text-sm font-semibold tracking-wider mb-3">2024 - 2028</p>
                                    <p class="text-slate-300 text-sm">The Islamia University of Bahawalpur</p>
                                </div>
                            </div>

                            <!-- Item 2 -->
                            <div class="relative pl-10">
                                <!-- Node Icon -->
                                <div
                                    class="absolute -left-[17px] top-6 w-8 h-8 bg-[#0ea5e9] rounded-md flex items-center justify-center shadow-[0_0_10px_rgba(14,165,233,0.5)]">
                                    <svg class="w-4 h-4 text-white" fill="none" stroke="currentColor"
                                        viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                            d="M12 14l9-5-9-5-9 5 9 5zm0 0l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14zm-4 6v-7.5l4-2.222">
                                        </path>
                                    </svg>
                                </div>
                                <!-- Content Card -->
                                <div
                                    class="bg-[#111827] border border-[#1e293b] rounded-xl py-8 px-6 flex flex-col items-center text-center transition-all duration-300 hover:bg-[#131b2f] hover:border-[#0ea5e9]/30 hover:-translate-y-1">
                                    <h4 class="text-white font-bold text-[17px] mb-2">Intermediate</h4>
                                    <p class="text-[#0ea5e9] text-sm font-semibold tracking-wider mb-3">2021 - 2023</p>
                                    <p class="text-slate-300 text-sm">Post Graduate College, Bahawalpur</p>
                                </div>
                            </div>

                        </div>
                    </div>

                    <!-- ================= COLUMN 2: EXPERIENCE ================= -->
                    <div>
                        <!-- Column Header -->
                        <div class="flex items-center gap-4 mb-10">
                            <div
                                class="w-14 h-14 bg-[#1e293b] rounded-xl flex items-center justify-center shadow-lg border border-slate-700/50">
                                <!-- Briefcase Icon -->
                                <svg class="w-7 h-7 text-slate-400" fill="none" stroke="currentColor"
                                    viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                        d="M21 13.255A23.931 23.931 0 0112 15c-3.183 0-6.22-.62-9-1.745M16 6V4a2 2 0 00-2-2h-4a2 2 0 00-2 2v2m4 6h.01M5 20h14a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z">
                                    </path>
                                </svg>
                            </div>
                            <h3 class="text-2xl font-bold text-white tracking-wide">Experience</h3>
                        </div>

                        <!-- Timeline Container -->
                        <div class="border-l-2 border-[#1e293b] ml-6 pb-4">

                            <!-- Item 1 -->
                            <div class="relative pl-10 mb-10">
                                <!-- Node Icon -->
                                <div
                                    class="absolute -left-[17px] top-6 w-8 h-8 bg-[#0ea5e9] rounded-md flex items-center justify-center shadow-[0_0_10px_rgba(14,165,233,0.5)]">
                                    <svg class="w-4 h-4 text-white" fill="none" stroke="currentColor"
                                        viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                            d="M21 13.255A23.931 23.931 0 0112 15c-3.183 0-6.22-.62-9-1.745M16 6V4a2 2 0 00-2-2h-4a2 2 0 00-2 2v2m4 6h.01M5 20h14a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z">
                                        </path>
                                    </svg>
                                </div>
                                <!-- Content Card -->
                                <div
                                    class="bg-[#111827] border border-[#1e293b] rounded-xl py-8 px-6 flex flex-col items-center text-center transition-all duration-300 hover:bg-[#131b2f] hover:border-[#0ea5e9]/30 hover:-translate-y-1">
                                    <h4 class="text-white font-bold text-[17px] mb-2">Python Developer – Fiverr</h4>
                                    <p class="text-[#0ea5e9] text-sm font-semibold tracking-wider mb-3">July 2025 –
                                        Present</p>
                                    <p class="text-slate-300 text-sm">Freelance</p>
                                </div>
                            </div>

                            <!-- Item 2 -->
                            <div class="relative pl-10">
                                <!-- Node Icon -->
                                <div
                                    class="absolute -left-[17px] top-6 w-8 h-8 bg-[#0ea5e9] rounded-md flex items-center justify-center shadow-[0_0_10px_rgba(14,165,233,0.5)]">
                                    <svg class="w-4 h-4 text-white" fill="none" stroke="currentColor"
                                        viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                            d="M21 13.255A23.931 23.931 0 0112 15c-3.183 0-6.22-.62-9-1.745M16 6V4a2 2 0 00-2-2h-4a2 2 0 00-2 2v2m4 6h.01M5 20h14a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z">
                                        </path>
                                    </svg>
                                </div>
                                <!-- Content Card -->
                                <div
                                    class="bg-[#111827] border border-[#1e293b] rounded-xl py-8 px-6 flex flex-col items-center text-center transition-all duration-300 hover:bg-[#131b2f] hover:border-[#0ea5e9]/30 hover:-translate-y-1">
                                    <h4 class="text-white font-bold text-[17px] mb-2">Machine Learner</h4>
                                    <p class="text-[#0ea5e9] text-sm font-semibold tracking-wider mb-3">Mar 2026 –
                                        Present</p>
                                    <p class="text-slate-300 text-sm">Code'sThinker</p>
                                </div>
                            </div>

                        </div>
                    </div>

                </div>
            </div>
        </section>
        <!-- Education & Experience Section End -->
        <!-- Services Section Start -->
        <section class="bg-[#0B1120] py-20 px-4 md:px-8 font-sans">
            <div
                class="max-w-6xl mx-auto border border-[#29a8ff]/30 rounded-xl p-6 sm:p-10 bg-[#0f1525] shadow-[0_0_40px_rgba(41,168,255,0.05)]">

                <!-- Section Title -->
                <div class="text-center mb-16">
                    <h2 class="text-4xl md:text-5xl font-bold text-white tracking-wide">
                        My <span class="text-[#0ea5e9]">Services</span>
                    </h2>
                </div>

                <!-- Services Grid -->
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8">

                    <!-- Service Card 1: Cross-Platform Apps -->
                    <div
                        class="bg-[#111827] border border-[#1e293b] rounded-xl p-8 flex flex-col items-center text-center transition-all duration-300 hover:-translate-y-2 hover:border-[#0ea5e9]/40 hover:bg-[#131b2f]">
                        <div
                            class="w-16 h-16 bg-[#1e293b] rounded-2xl flex items-center justify-center mb-6 shadow-inner">
                            <svg class="w-8 h-8 text-[#0ea5e9]" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                                xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"></path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-4">Machine Learning
                        </h3>
                        <p class="text-slate-400 text-sm leading-relaxed">
                            Implementing predictive models and regression algorithms to extract meaningful patterns from
                            complex datasets.
                        </p>
                    </div>

                    <!-- Service Card 2: UI/UX Design -->
                    <div
                        class="bg-[#111827] border border-[#1e293b] rounded-xl p-8 flex flex-col items-center text-center transition-all duration-300 hover:-translate-y-2 hover:border-[#0ea5e9]/40 hover:bg-[#131b2f]">
                        <div
                            class="w-16 h-16 bg-[#1e293b] rounded-2xl flex items-center justify-center mb-6 shadow-inner">
                            <svg class="w-8 h-8 text-[#0ea5e9]" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                                xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M4 5a1 1 0 011-1h14a1 1 0 011 1v2a1 1 0 01-1 1H5a1 1 0 01-1-1V5zM4 13a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H5a1 1 0 01-1-1v-6zM16 13a1 1 0 011-1h2a1 1 0 011 1v6a1 1 0 01-1 1h-2a1 1 0 01-1-1v-6z">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-4">Python Deep Learning</h3>
                        <p class="text-slate-400 text-sm leading-relaxed">
                            Building end-to-end Neural Networks using PyTorch and TensorFlow for sophisticated feature
                            extraction and modeling.
                        </p>
                    </div>

                    <!-- Service Card 3: State Management -->
                    <div
                        class="bg-[#111827] border border-[#1e293b] rounded-xl p-8 flex flex-col items-center text-center transition-all duration-300 hover:-translate-y-2 hover:border-[#0ea5e9]/40 hover:bg-[#131b2f]">
                        <div
                            class="w-16 h-16 bg-[#1e293b] rounded-2xl flex items-center justify-center mb-6 shadow-inner">
                            <svg class="w-8 h-8 text-[#0ea5e9]" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                                xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z">
                                </path>
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-4">Data Processing</h3>
                        <p class="text-slate-400 text-sm leading-relaxed">
                            Scalable ETL pipelines and data cleaning services to ensure high data quality for training
                            and production environments.
                        </p>
                    </div>



                    <!-- Service Card 7: Machine Learning Models -->
                    <div
                        class="bg-[#111827] border border-[#1e293b] rounded-xl p-8 flex flex-col items-center text-center transition-all duration-300 hover:-translate-y-2 hover:border-[#0ea5e9]/40 hover:bg-[#131b2f]">
                        <div
                            class="w-16 h-16 bg-[#1e293b] rounded-2xl flex items-center justify-center mb-6 shadow-inner">
                            <svg class="w-8 h-8 text-[#0ea5e9]" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                                xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6"></path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-4">Predictive Modeling</h3>
                        <p class="text-slate-400 text-sm leading-relaxed">
                            Build custom Machine Learning models using Python, TensorFlow, and Scikit-Learn for
                            data-driven decisions.
                        </p>
                    </div>

                    <!-- Service Card 8: NLP -->
                    <div
                        class="bg-[#111827] border border-[#1e293b] rounded-xl p-8 flex flex-col items-center text-center transition-all duration-300 hover:-translate-y-2 hover:border-[#0ea5e9]/40 hover:bg-[#131b2f]">
                        <div
                            class="w-16 h-16 bg-[#1e293b] rounded-2xl flex items-center justify-center mb-6 shadow-inner">
                            <svg class="w-8 h-8 text-[#0ea5e9]" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                                xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M8 10h.01M12 10h.01M16 10h.01M9 16H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-5l-5 5v-5z">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-4">Natural Language Processing</h3>
                        <p class="text-slate-400 text-sm leading-relaxed">
                            Develop NLP applications including text classification, sentiment analysis, and intelligent
                            chatbots.
                        </p>
                    </div>

                    <!-- Service Card 9: Computer Vision -->
                    <div
                        class="bg-[#111827] border border-[#1e293b] rounded-xl p-8 flex flex-col items-center text-center transition-all duration-300 hover:-translate-y-2 hover:border-[#0ea5e9]/40 hover:bg-[#131b2f]">
                        <div
                            class="w-16 h-16 bg-[#1e293b] rounded-2xl flex items-center justify-center mb-6 shadow-inner">
                            <svg class="w-8 h-8 text-[#0ea5e9]" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                                xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-4">Computer Vision</h3>
                        <p class="text-slate-400 text-sm leading-relaxed">
                            Implement deep learning solutions for image recognition, object detection, and visual data
                            analysis.
                        </p>
                    </div>

                </div>
            </div>
        </section>
        <!-- Services Section End -->
        <!DOCTYPE html>
        <html lang="en">

        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>ML Expert Portfolio - Projects</title>
            <script src="https://cdn.tailwindcss.com"></script>
            <style>
                @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap');

                body {
                    font-family: 'Inter', sans-serif;
                }
            </style>
        </head>

        <body class="bg-[#0A101E] text-white antialiased">

            <!-- Projects Section -->
            <section class="py-20 px-4 md:px-8 max-w-7xl mx-auto">

                <!-- Header -->
                <h2 class="text-4xl md:text-5xl font-bold text-center mb-4 tracking-tight">
                    Machine Learning <span class="text-[#0EA5E9]">Expertise</span>
                </h2>
                <p class="text-slate-400 text-center max-w-2xl mx-auto mb-16">
                    Showcasing end-to-end AI solutions, from neural network architecture to production-ready
                    deployments.
                </p>

                <!-- Projects Grid -->
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

                    <!-- Card 1: NLP Sentix -->
                    <div
                        class="bg-[#1C2434] rounded-xl overflow-hidden flex flex-col border border-slate-800 hover:border-sky-500/50 transition-all group">
                        <!-- Image Area -->
                        <div class="h-52 w-full bg-slate-900 relative overflow-hidden">
                            <img src="https://images.unsplash.com/photo-1677442136019-21780ecad995?q=80&w=1000&auto=format&fit=crop"
                                alt="NLP Project"
                                class="w-full h-full object-cover opacity-80 group-hover:scale-105 transition-transform duration-500">
                        </div>

                        <!-- Content Area -->
                        <div class="p-6 flex flex-col flex-grow">
                            <span
                                class="bg-sky-500/10 text-[#0EA5E9] text-[11px] uppercase tracking-wider font-bold px-3 py-1 rounded-full w-max mb-4">
                                Natural Language Processing
                            </span>

                            <h3 class="text-xl font-bold mb-3">Sentix AI Engine</h3>
                            <p class="text-slate-400 text-sm mb-6 leading-relaxed">
                                A real-time sentiment analysis API built using BERT transformers. Capable of processing
                                10k+ messages/sec for brand monitoring and automated customer intent detection.
                            </p>

                            <div class="flex-grow"></div>

                            <!-- Buttons -->
                            <div class="flex flex-wrap gap-2">
                                <a href="https://github.com/ml-expert/sentix-nlp" target="_blank"
                                    class="flex items-center gap-1.5 bg-[#0EA5E9] hover:bg-sky-500 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24">
                                        <path
                                            d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
                                    </svg>
                                    Code
                                </a>
                                <a href="https://sentix-demo.ai" target="_blank"
                                    class="flex items-center gap-1.5 border border-slate-600 hover:bg-slate-700 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    Project Proposal
                                </a>
                                <a href="https://huggingface.co/spaces/sentix-ml" target="_blank"
                                    class="flex items-center gap-1.5 border border-slate-600 hover:bg-slate-700 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    Demo
                                </a>
                            </div>
                        </div>
                    </div>

                    <!-- Card 2: ERP Predictive Analytics -->
                    <div
                        class="bg-[#1C2434] rounded-xl overflow-hidden flex flex-col border border-slate-800 hover:border-sky-500/50 transition-all group">
                        <!-- Image Area -->
                        <div class="h-52 w-full bg-slate-900 relative overflow-hidden">
                            <img src="https://images.unsplash.com/photo-1551288049-bbbda536339a?q=80&w=1000&auto=format&fit=crop"
                                alt="Predictive Analytics"
                                class="w-full h-full object-cover opacity-80 group-hover:scale-105 transition-transform duration-500">
                        </div>

                        <!-- Content Area -->
                        <div class="p-6 flex flex-col flex-grow">
                            <span
                                class="bg-sky-500/10 text-[#0EA5E9] text-[11px] uppercase tracking-wider font-bold px-3 py-1 rounded-full w-max mb-4">
                                Predictive Analytics
                            </span>

                            <h3 class="text-xl font-bold mb-3">Dynamics D365 Forecaster</h3>
                            <p class="text-slate-400 text-sm mb-6 leading-relaxed">
                                A forecasting module for Microsoft Dynamics 365. Uses XGBoost and Prophet models to
                                predict payroll fluctuations and resource demands with 94.2% accuracy.
                            </p>

                            <div class="flex-grow"></div>

                            <!-- Buttons -->
                            <div class="flex flex-wrap gap-2">
                                <a href="https://github.com/ml-expert/d365-forecaster" target="_blank"
                                    class="flex items-center gap-1.5 bg-[#0EA5E9] hover:bg-sky-500 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24">
                                        <path
                                            d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
                                    </svg>
                                    GitHub
                                </a>
                                <a href="https://notion.site/project-proposal-d365" target="_blank"
                                    class="flex items-center gap-1.5 border border-slate-600 hover:bg-slate-700 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    Technical Docs
                                </a>
                                <a href="https://azure.microsoft.com/ml-demo" target="_blank"
                                    class="flex items-center gap-1.5 border border-slate-600 hover:bg-slate-700 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    Case Study
                                </a>
                            </div>
                        </div>
                    </div>

                    <!-- Card 3: Reinforcement Learning -->
                    <div
                        class="bg-[#1C2434] rounded-xl overflow-hidden flex flex-col border border-slate-800 hover:border-sky-500/50 transition-all group">
                        <!-- Image Area -->
                        <div class="h-52 w-full bg-slate-900 relative overflow-hidden">
                            <img src="https://images.unsplash.com/photo-1611974789855-9c2a0a7236a3?q=80&w=1000&auto=format&fit=crop"
                                alt="RL Trading"
                                class="w-full h-full object-cover opacity-80 group-hover:scale-105 transition-transform duration-500">
                        </div>

                        <!-- Content Area -->
                        <div class="p-6 flex flex-col flex-grow">
                            <span
                                class="bg-sky-500/10 text-[#0EA5E9] text-[11px] uppercase tracking-wider font-bold px-3 py-1 rounded-full w-max mb-4">
                                Deep Reinforcement Learning
                            </span>

                            <h3 class="text-xl font-bold mb-3">AlphaBot RL Trader</h3>
                            <p class="text-slate-400 text-sm mb-6 leading-relaxed">
                                An autonomous trading agent trained via Deep Q-Learning (DQN). Optimized for
                                high-frequency trading on IBKR, featuring a custom Reward Function for risk management.
                            </p>

                            <div class="flex-grow"></div>

                            <!-- Buttons -->
                            <div class="flex flex-wrap gap-2">
                                <a href="https://github.com/ml-expert/rl-trading-bot" target="_blank"
                                    class="flex items-center gap-1.5 bg-[#0EA5E9] hover:bg-sky-500 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24">
                                        <path
                                            d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
                                    </svg>
                                    Code
                                </a>
                                <a href="https://arxiv.org/abs/2301.12345" target="_blank"
                                    class="flex items-center gap-1.5 border border-slate-600 hover:bg-slate-700 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    Proposal Paper
                                </a>
                                <a href="https://wandb.ai/ml-expert/alphabot" target="_blank"
                                    class="flex items-center gap-1.5 border border-slate-600 hover:bg-slate-700 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    ML Logs
                                </a>
                            </div>
                        </div>
                    </div>
                    <!-- Card 1: NLP Sentix -->
                    <div
                        class="bg-[#1C2434] rounded-xl overflow-hidden flex flex-col border border-slate-800 hover:border-sky-500/50 transition-all group">
                        <!-- Image Area -->
                        <div class="h-52 w-full bg-slate-900 relative overflow-hidden">
                            <img src="https://images.unsplash.com/photo-1677442136019-21780ecad995?q=80&w=1000&auto=format&fit=crop"
                                alt="NLP Project"
                                class="w-full h-full object-cover opacity-80 group-hover:scale-105 transition-transform duration-500">
                        </div>

                        <!-- Content Area -->
                        <div class="p-6 flex flex-col flex-grow">
                            <span
                                class="bg-sky-500/10 text-[#0EA5E9] text-[11px] uppercase tracking-wider font-bold px-3 py-1 rounded-full w-max mb-4">
                                Natural Language Processing
                            </span>

                            <h3 class="text-xl font-bold mb-3">Sentix AI Engine</h3>
                            <p class="text-slate-400 text-sm mb-6 leading-relaxed">
                                A real-time sentiment analysis API built using BERT transformers. Capable of processing
                                10k+ messages/sec for brand monitoring and automated customer intent detection.
                            </p>

                            <div class="flex-grow"></div>

                            <!-- Buttons -->
                            <div class="flex flex-wrap gap-2">
                                <a href="https://github.com/ml-expert/sentix-nlp" target="_blank"
                                    class="flex items-center gap-1.5 bg-[#0EA5E9] hover:bg-sky-500 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24">
                                        <path
                                            d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
                                    </svg>
                                    Code
                                </a>
                                <a href="https://sentix-demo.ai" target="_blank"
                                    class="flex items-center gap-1.5 border border-slate-600 hover:bg-slate-700 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    Project Proposal
                                </a>
                                <a href="https://huggingface.co/spaces/sentix-ml" target="_blank"
                                    class="flex items-center gap-1.5 border border-slate-600 hover:bg-slate-700 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    Demo
                                </a>
                            </div>
                        </div>
                    </div>

                    <!-- Card 2: ERP Predictive Analytics -->
                    <div
                        class="bg-[#1C2434] rounded-xl overflow-hidden flex flex-col border border-slate-800 hover:border-sky-500/50 transition-all group">
                        <!-- Image Area -->
                        <div class="h-52 w-full bg-slate-900 relative overflow-hidden">
                            <img src="https://images.unsplash.com/photo-1551288049-bbbda536339a?q=80&w=1000&auto=format&fit=crop"
                                alt="Predictive Analytics"
                                class="w-full h-full object-cover opacity-80 group-hover:scale-105 transition-transform duration-500">
                        </div>

                        <!-- Content Area -->
                        <div class="p-6 flex flex-col flex-grow">
                            <span
                                class="bg-sky-500/10 text-[#0EA5E9] text-[11px] uppercase tracking-wider font-bold px-3 py-1 rounded-full w-max mb-4">
                                Predictive Analytics
                            </span>

                            <h3 class="text-xl font-bold mb-3">Dynamics D365 Forecaster</h3>
                            <p class="text-slate-400 text-sm mb-6 leading-relaxed">
                                A forecasting module for Microsoft Dynamics 365. Uses XGBoost and Prophet models to
                                predict payroll fluctuations and resource demands with 94.2% accuracy.
                            </p>

                            <div class="flex-grow"></div>

                            <!-- Buttons -->
                            <div class="flex flex-wrap gap-2">
                                <a href="https://github.com/ml-expert/d365-forecaster" target="_blank"
                                    class="flex items-center gap-1.5 bg-[#0EA5E9] hover:bg-sky-500 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24">
                                        <path
                                            d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
                                    </svg>
                                    GitHub
                                </a>
                                <a href="https://notion.site/project-proposal-d365" target="_blank"
                                    class="flex items-center gap-1.5 border border-slate-600 hover:bg-slate-700 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    Technical Docs
                                </a>
                                <a href="https://azure.microsoft.com/ml-demo" target="_blank"
                                    class="flex items-center gap-1.5 border border-slate-600 hover:bg-slate-700 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    Case Study
                                </a>
                            </div>
                        </div>
                    </div>

                    <!-- Card 3: Reinforcement Learning -->
                    <div
                        class="bg-[#1C2434] rounded-xl overflow-hidden flex flex-col border border-slate-800 hover:border-sky-500/50 transition-all group">
                        <!-- Image Area -->
                        <div class="h-52 w-full bg-slate-900 relative overflow-hidden">
                            <img src="https://images.unsplash.com/photo-1611974789855-9c2a0a7236a3?q=80&w=1000&auto=format&fit=crop"
                                alt="RL Trading"
                                class="w-full h-full object-cover opacity-80 group-hover:scale-105 transition-transform duration-500">
                        </div>

                        <!-- Content Area -->
                        <div class="p-6 flex flex-col flex-grow">
                            <span
                                class="bg-sky-500/10 text-[#0EA5E9] text-[11px] uppercase tracking-wider font-bold px-3 py-1 rounded-full w-max mb-4">
                                Deep Reinforcement Learning
                            </span>

                            <h3 class="text-xl font-bold mb-3">AlphaBot RL Trader</h3>
                            <p class="text-slate-400 text-sm mb-6 leading-relaxed">
                                An autonomous trading agent trained via Deep Q-Learning (DQN). Optimized for
                                high-frequency trading on IBKR, featuring a custom Reward Function for risk management.
                            </p>

                            <div class="flex-grow"></div>

                            <!-- Buttons -->
                            <div class="flex flex-wrap gap-2">
                                <a href="https://github.com/ml-expert/rl-trading-bot" target="_blank"
                                    class="flex items-center gap-1.5 bg-[#0EA5E9] hover:bg-sky-500 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24">
                                        <path
                                            d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
                                    </svg>
                                    Code
                                </a>
                                <a href="https://arxiv.org/abs/2301.12345" target="_blank"
                                    class="flex items-center gap-1.5 border border-slate-600 hover:bg-slate-700 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    Proposal Paper
                                </a>
                                <a href="https://wandb.ai/ml-expert/alphabot" target="_blank"
                                    class="flex items-center gap-1.5 border border-slate-600 hover:bg-slate-700 text-white text-[12px] font-medium px-3 py-2 rounded-md transition-colors">
                                    ML Logs
                                </a>
                            </div>
                        </div>
                    </div>

                </div>
            </section>

            <body class="bg-[#020617] text-white antialiased">

                <section class="py-20 px-4 md:px-8 max-w-7xl mx-auto">
                    <!-- Header -->
                    <h2 class="text-4xl md:text-5xl font-bold text-center mb-16">
                        Get In <span class="text-[#0EA5E9]">Touch</span>
                    </h2>

                    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">

                        <!-- Left Side: Form -->
                        <div class="bg-[#0F172A] border border-slate-800 p-8 rounded-xl">
                            <form action="#" class="space-y-6">
                                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                                    <!-- Name -->
                                    <div class="space-y-2">
                                        <label class="text-sm font-medium text-slate-300">Your Name</label>
                                        <input type="text" placeholder="Muhammad Obaid"
                                            class="w-full bg-[#1E293B] border border-slate-700 rounded-lg px-4 py-3 text-slate-200 focus:outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500 transition-all">
                                    </div>
                                    <!-- Email -->
                                    <div class="space-y-2">
                                        <label class="text-sm font-medium text-slate-300">Your Email</label>
                                        <input type="email" placeholder="obaid@example.com"
                                            class="w-full bg-[#1E293B] border border-slate-700 rounded-lg px-4 py-3 text-slate-200 focus:outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500 transition-all">
                                    </div>
                                </div>

                                <!-- Phone Number -->
                                <div class="space-y-2">
                                    <label class="text-sm font-medium text-slate-300">Phone Number</label>
                                    <input type="text" placeholder="+92 329 6132923"
                                        class="w-full bg-[#1E293B] border border-slate-700 rounded-lg px-4 py-3 text-slate-200 focus:outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500 transition-all">
                                </div>

                                <!-- Message -->
                                <div class="space-y-2">
                                    <label class="text-sm font-medium text-slate-300">Your Message</label>
                                    <textarea rows="5" placeholder="Hello Muhammad, I would like to discuss..."
                                        class="w-full bg-[#1E293B] border border-slate-700 rounded-lg px-4 py-3 text-slate-200 focus:outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500 transition-all resize-none"></textarea>
                                </div>

                                <button type="submit"
                                    class="w-full bg-[#0EA5E9] hover:bg-sky-500 text-white font-bold py-4 rounded-lg flex items-center justify-center gap-2 transition-all shadow-lg shadow-sky-500/20">
                                    Send Message
                                    <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                                        <path
                                            d="M10.894 2.553a1 1 0 00-1.788 0l-7 14a1 1 0 001.169 1.409l5-1.429A1 1 0 009 15.571V11a1 1 0 112 0v4.571a1 1 0 00.725.962l5 1.428a1 1 0 001.17-1.408l-7-14z">
                                        </path>
                                    </svg>
                                </button>
                            </form>
                        </div>

                       
                        <div class="bg-[#0F172A] border border-slate-800 p-8 rounded-xl flex flex-col justify-between">
                            <div class="space-y-4">
                              
                                <div
                                    class="flex items-center gap-4 bg-[#1E293B] p-4 rounded-lg border border-slate-700/50">
                                    <div class="text-sky-500">
                                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                                d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z">
                                            </path>
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                                d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path>
                                        </svg>
                                    </div>
                                    <span class="text-slate-300">Pakistan</span>
                                </div>

                                <a href="mailto:abdullahrajpoot2476@gmail.com"
                                    class="flex items-center gap-4 bg-[#1E293B] p-4 rounded-lg border border-slate-700/50 hover:border-sky-500/50 transition-colors group">
                                    <div class="text-sky-500">
                                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                                d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z">
                                            </path>
                                        </svg>
                                    </div>
                                    <span class="text-slate-300 group-hover:text-sky-400">obaidali234@gmail.com</span>
                                </a>

                             
                                <div
                                    class="flex items-center gap-4 bg-[#1E293B] p-4 rounded-lg border border-slate-700/50">
                                    <div class="text-sky-500">
                                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                                d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z">
                                            </path>
                                        </svg>
                                    </div>
                                    <span class="text-slate-300">0328-6793777</span>
                                </div>

                              
                                <a href="#"
                                    class="flex items-center gap-4 bg-[#1E293B] p-4 rounded-lg border border-slate-700/50 hover:border-sky-500/50 transition-colors group">
                                    <div class="text-sky-500">
                                        <svg class="w-6 h-6 fill-current" viewBox="0 0 24 24">
                                            <path
                                                d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12" />
                                        </svg>
                                    </div>
                                    <span class="text-slate-300 group-hover:text-sky-400">GitHub</span>
                                </a>

                              
                                <a href="#"
                                    class="flex items-center gap-4 bg-[#1E293B] p-4 rounded-lg border border-slate-700/50 hover:border-sky-500/50 transition-colors group">
                                    <div class="text-sky-500">
                                        <svg class="w-6 h-6 fill-current" viewBox="0 0 24 24">
                                            <path
                                                d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" />
                                        </svg>
                                    </div>
                                    <span class="text-slate-300 group-hover:text-sky-400">LinkedIn</span>
                                </a>
                            </div>

                          
                            <div class="mt-8">
                                <h4 class="text-lg font-bold mb-2">Available for work</h4>
                                <p class="text-slate-400 text-sm leading-relaxed">
                                    I am currently open to freelance opportunities as well as full-time roles. Please
                                    feel free to connect for collaborations or a friendly conversation!
                                </p>
                            </div>
                        </div>
                    </div>
                </section>
                
                <section class="py-12 bg-[#0A101E]">
                    <div class="max-w-7xl mx-auto px-4 md:px-8">

                       
                        <div
                            class="relative w-full h-[450px] rounded-xl overflow-hidden border border-slate-800 shadow-2xl">

                           
                            <iframe class="absolute inset-0 w-full h-full grayscale-[20%] contrast-[1.1]"
                                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d110543.08581729112!2d71.60676478953153!3d29.381395899999998!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x393b90c37c60310d%3A0x669460020f66e048!2sBahawalpur%2C%20Punjab%2C%20Pakistan!5e0!3m2!1sen!2s!4v1700000000000!5m2!1sen!2s"
                                style="border:0;" allowfullscreen="" loading="lazy"
                                referrerpolicy="no-referrer-when-downgrade">
                            </iframe>

                           
                            <div
                                class="absolute top-4 left-4 bg-white p-4 shadow-lg rounded-sm flex items-center gap-12 z-10 hidden sm:flex">
                                <div>
                                    <h3 class="text-[#202124] text-lg font-semibold leading-tight">Bahawalpur</h3>
                                    <p class="text-[#70757a] text-[13px]">Bahawalpur, Pakistan</p>
                                </div>

                                <div class="flex items-center gap-4">
                                   
                                    <a href="https://maps.google.com" target="_blank"
                                        class="text-[#1a73e8] hover:text-blue-700">
                                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                                d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14">
                                            </path>
                                        </svg>
                                    </a>
                                    
                                    <a href="#"
                                        class="bg-[#1a73e8] p-2 rounded-full text-white hover:bg-blue-700 transition-colors">
                                        <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                                            <path
                                                d="M21.71 11.29l-9-9c-.39-.39-1.02-.39-1.41 0l-9 9c-.39.39-.39 1.02 0 1.41l9 9c.39.39 1.02.39 1.41 0l9-9c.39-.38.39-1.01 0-1.41zM14 14.5V12h-4v3H8v-4c0-.55.45-1 1-1h5V7.5l3.5 3.5-3.5 3.5z">
                                            </path>
                                        </svg>
                                    </a>
                                </div>
                            </div>

                            
                            <div
                                class="absolute bottom-10 left-4 w-12 h-12 rounded-lg border-2 border-white overflow-hidden shadow-md cursor-pointer group z-10">
                                <img src="https://khms1.googleapis.com/kh?v=947&hl=en-US&x=5848&y=3487&z=13"
                                    class="w-full h-full object-cover group-hover:scale-110 transition-transform"
                                    alt="Satellite view">
                            </div>

                           
                            <div class="absolute bottom-10 right-4 flex flex-col gap-2 z-10">
                                <button class="bg-white p-2 shadow-md rounded hover:bg-gray-100 text-gray-600">
                                    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                            d="M4 8V4m0 0h4M4 4l5 5m11-1V4m0 0h-4m4 0l-5 5M4 16v4m0 0h4m-4 0l5-5m11 5l-5-5m5 5v-4m0 4h-4">
                                        </path>
                                    </svg>
                                </button>
                                <div class="flex flex-col bg-white shadow-md rounded overflow-hidden">
                                    <button
                                        class="p-2 hover:bg-gray-100 text-gray-600 border-b border-gray-200 text-xl font-bold">+</button>
                                    <button class="p-2 hover:bg-gray-100 text-gray-600 text-xl font-bold">−</button>
                                </div>
                            </div>

                        </div>
                    </div>
                </section>
                
                <footer class="bg-[#020617] text-white pt-20 pb-10 border-t border-slate-900">
                    <div class="max-w-7xl mx-auto px-4 md:px-8">

                        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-12 mb-16">

                          
                            <div class="space-y-6">
                                <div class="flex items-center gap-3">
                                    <div
                                        class="w-10 h-10 bg-[#0EA5E9] rounded flex items-center justify-center font-bold text-xl shadow-lg shadow-sky-500/20">
                                        <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor"
                                            stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
                                            <path d="M17 11l-5-5-5 5M17 18l-5-5-5 5" />
                                        </svg>
                                    </div>
                                    <h2 class="text-2xl font-bold tracking-tight">Muhammad Obaid</h2>
                                </div>

                                <p class="text-slate-400 leading-relaxed max-w-sm">
                                    Crafting high-performance digital solutions where <span
                                        class="text-white font-medium">design meets engineering</span>. Let's build
                                    something extraordinary together.
                                </p>

                                <div
                                    class="inline-flex items-center gap-2 px-4 py-2 bg-emerald-500/10 border border-emerald-500/20 rounded-full">
                                    <span class="relative flex h-2 w-2">
                                        <span
                                            class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>
                                        <span class="relative inline-flex rounded-full h-2 w-2 bg-emerald-500"></span>
                                    </span>
                                    <span class="text-emerald-500 text-xs font-bold tracking-wider uppercase">Available
                                        for new projects</span>
                                </div>
                            </div>

                          
                            <div class="lg:pl-20">
                                <h3 class="text-xs font-bold uppercase tracking-[0.2em] text-slate-500 mb-8">Navigation
                                </h3>
                                <ul class="space-y-4 text-slate-300">
                                    <li><a href="#home" class="hover:text-[#0EA5E9] transition-colors">Home</a></li>
                                    <li><a href="#about" class="hover:text-[#0EA5E9] transition-colors">About</a></li>
                                    <li><a href="#skills" class="hover:text-[#0EA5E9] transition-colors">Skills</a></li>
                                    <li><a href="#projects" class="hover:text-[#0EA5E9] transition-colors">Projects</a>
                                    </li>
                                    <li><a href="#contact" class="hover:text-[#0EA5E9] transition-colors">Contact</a>
                                    </li>
                                </ul>
                            </div>

                          
                            <div>
                                <h3 class="text-xs font-bold uppercase tracking-[0.2em] text-slate-500 mb-8">Social
                                    Pulse</h3>
                                <div class="flex gap-3 mb-8">
                                   
                                    <a href="https://github.com" target="_blank"
                                        class="w-10 h-10 flex items-center justify-center rounded-lg border border-slate-800 bg-[#0F172A] hover:border-sky-500 hover:text-sky-500 transition-all">
                                        <svg class="w-5 h-5 fill-current" viewBox="0 0 24 24">
                                            <path
                                                d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
                                        </svg>
                                    </a>
                                  
                                    <a href="https://linkedin.com" target="_blank"
                                        class="w-10 h-10 flex items-center justify-center rounded-lg border border-slate-800 bg-[#0F172A] hover:border-sky-500 hover:text-sky-500 transition-all">
                                        <svg class="w-5 h-5 fill-current" viewBox="0 0 24 24">
                                            <path
                                                d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" />
                                        </svg>
                                    </a>
                                    
                                    <a href="https://twitter.com" target="_blank"
                                        class="w-10 h-10 flex items-center justify-center rounded-lg border border-slate-800 bg-[#0F172A] hover:border-sky-500 hover:text-sky-500 transition-all">
                                        <svg class="w-5 h-5 fill-current" viewBox="0 0 24 24">
                                            <path
                                                d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.84 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z" />
                                        </svg>
                                    </a>
                                    <!-- Instagram -->
                                    <a href="https://instagram.com" target="_blank"
                                        class="w-10 h-10 flex items-center justify-center rounded-lg border border-slate-800 bg-[#0F172A] hover:border-sky-500 hover:text-sky-500 transition-all">
                                        <svg class="w-5 h-5 fill-none stroke=" currentColor" stroke-width="2"
                                            viewBox="0 0 24 24">
                                            <rect x="2" y="2" width="20" height="20" rx="5" ry="5"></rect>
                                            <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"></path>
                                            <line x1="17.5" y1="6.5" x2="17.51" y2="6.5"></line>
                                        </svg>
                                    </a>
                                </div>

                                <!-- Quick Chat Box -->
                                <a href="https://wa.me/923256431025" target="_blank"
                                    class="flex items-center gap-4 bg-[#0F172A] border border-slate-800 rounded-xl p-4 hover:border-emerald-500/50 transition-all group">
                                    <div
                                        class="w-12 h-12 bg-emerald-500/10 rounded-full flex items-center justify-center text-emerald-500 group-hover:scale-110 transition-transform">
                                        <svg class="w-6 h-6 fill-current" viewBox="0 0 24 24">
                                            <path
                                                d="M.057 24l1.687-6.163c-1.041-1.804-1.588-3.849-1.587-5.946.003-6.556 5.338-11.891 11.893-11.891 3.181.001 6.167 1.24 8.413 3.488 2.246 2.248 3.484 5.232 3.484 8.412-.003 6.557-5.338 11.892-11.893 11.892-1.912-.001-3.793-.457-5.47-1.32l-6.53 1.714zm5.422-3.891l.389.231c1.514.897 3.256 1.371 5.034 1.372h.001c5.807 0 10.533-4.726 10.536-10.533.001-2.813-1.093-5.459-3.08-7.448-1.987-1.988-4.634-3.082-7.447-3.082-5.812 0-10.538 4.728-10.54 10.535-.001 2.023.579 3.996 1.675 5.717l.253.401-1.01 3.681 3.769-.989z" />
                                        </svg>
                                    </div>
                                    <div>
                                        <p class="text-[10px] uppercase tracking-widest text-slate-500 font-bold">Quick
                                            Chat</p>
                                        <p class="text-slate-200 font-semibold">+92 328 6793777</p>
                                    </div>
                                </a>
                            </div>
                        </div>

                        <!-- Bottom Footer -->
                        <div
                            class="pt-8 border-t border-slate-900 flex flex-col md:flex-row justify-between items-center gap-4 text-slate-500 text-sm">
                            <p>© 2026 <span class="text-slate-300">Muhammad Obaid</span>. Built with passion & Tailwind.
                            </p>
                            <div class="flex gap-6">
                                <a href="#" class="hover:text-white transition-colors">Privacy Policy</a>
                                <a href="#" class="hover:text-white transition-colors">Terms of Service</a>
                            </div>
                        </div>
                    </div>
                </footer>



            </body>

        </html>
