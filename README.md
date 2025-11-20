我爱付骏怡
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title data-lang-key="head.title">Student Science Hub | 理科学习空间</title>
    <!-- 引入 Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- 引入 Inter 字体 -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&family=Noto+Sans+SC:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        /* 应用字体 */
        body {
            font-family: 'Inter', 'Noto Sans SC', sans-serif;
            /* 平滑滚动 */
            scroll-behavior: smooth;
        }
        
        /* 隐藏 section 的基类 */
        .page-section {
            display: none;
            /* 渐变过渡效果 */
            opacity: 0;
            transition: opacity 0.5s ease-in-out, transform 0.5s ease-in-out;
            transform: translateY(20px);
        }
        /* 显示当前 active 的 section */
        .page-section.active {
            display: block;
            opacity: 1;
            transform: translateY(0);
        }
        
        /* 导航链接激活状态 */
        .nav-link.active {
            @apply bg-blue-700 text-white;
        }
        
        /* 卡片悬停效果 */
        .subject-card {
            @apply bg-white rounded-xl shadow-lg transition-all duration-300 ease-in-out;
        }
        .subject-card:hover {
            @apply shadow-2xl transform -translate-y-2;
        }

        /* 笔记卡片 */
        .note-card {
             @apply bg-white rounded-lg shadow-md overflow-hidden transition-all duration-300;
        }
        .note-card:hover {
            @apply shadow-xl transform -translate-y-1; /* 增加了上浮效果 */
        }
    </style>
</head>
<body class="bg-gray-100 text-gray-800">

    <!-- 导航栏 -->
    <nav class="bg-white shadow-md sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <!-- Logo 和 标题 -->
                <div class="flex-shrink-0 flex items-center">
                    <svg class="h-8 w-8 text-blue-600" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.75 17.25l.038-.038A7.5 7.5 0 0112 15c1.528 0 3.004.463 4.212 1.288l.038.038m-8.4 0H4.5a2.25 2.25 0 01-2.25-2.25V6.75A2.25 2.25 0 014.5 4.5h15A2.25 2.25 0 0121.75 6.75v8.25a2.25 2.25 0 01-2.25 2.25h-5.25m-8.4 0s-1.125 .625-2.625 1.125" />
                    </svg>
                    <span class="font-bold text-xl ml-2 text-blue-700" data-lang-key="nav.title">理科学习空间</span>
                </div>
                
                <!-- 桌面导航链接 -->
                <div class="hidden sm:ml-6 sm:flex sm:space-x-2">
                    <a href="#home" data-nav-link="home" class="nav-link px-3 py-2 rounded-md text-sm font-medium text-gray-700 hover:bg-gray-200 transition-all duration-300" data-lang-key="nav.home">首页</a>
                    <a href="#about" data-nav-link="about" class="nav-link px-3 py-2 rounded-md text-sm font-medium text-gray-700 hover:bg-gray-200 transition-all duration-300" data-lang-key="nav.about">关于我</a>
                    <a href="#subjects" data-nav-link="subjects" class="nav-link px-3 py-2 rounded-md text-sm font-medium text-gray-700 hover:bg-gray-200 transition-all duration-300" data-lang-key="nav.subjects">学科</a>
                    <a href="#notes" data-nav-link="notes" class="nav-link px-3 py-2 rounded-md text-sm font-medium text-gray-700 hover:bg-gray-200 transition-all duration-300" data-lang-key="nav.notes">学习笔记</a>
                    <a href="#resources" data-nav-link="resources" class="nav-link px-3 py-2 rounded-md text-sm font-medium text-gray-700 hover:bg-gray-200 transition-all duration-300" data-lang-key="nav.resources">学习资源</a>
                </div>

                <!-- 语言切换按钮 -->
                <div class="flex items-center">
                    <button id="lang-switcher" class="px-3 py-2 rounded-md text-sm font-medium bg-blue-600 text-white hover:bg-blue-700 transition-all">
                        English
                    </button>
                    
                    <!-- 移动端菜单按钮 -->
                    <button id="mobile-menu-button" class="sm:hidden ml-3 p-2 rounded-md text-gray-700 hover:bg-gray-200">
                        <svg class="w-6 h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
                        </svg>
                    </button>
                </div>
            </div>
        </div>
        
        <!-- 移动端菜单 (默认隐藏) -->
        <div id="mobile-menu" class="sm:hidden hidden bg-white shadow-lg">
            <div class="px-2 pt-2 pb-3 space-y-1">
                <a href="#home" data-nav-link="home" class="nav-link block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:bg-gray-200 transition-all duration-300" data-lang-key="nav.home">首页</a>
                <a href="#about" data-nav-link="about" class="nav-link block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:bg-gray-200 transition-all duration-300" data-lang-key="nav.about">关于我</a>
                <a href="#subjects" data-nav-link="subjects" class="nav-link block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:bg-gray-200 transition-all duration-300" data-lang-key="nav.subjects">学科</a>
                <a href="#notes" data-nav-link="notes" class="nav-link block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:bg-gray-200 transition-all duration-300" data-lang-key="nav.notes">学习笔记</a>
                <a href="#resources" data-nav-link="resources" class="nav-link block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:bg-gray-200 transition-all duration-300" data-lang-key="nav.resources">学习资源</a>
            </div>
        </div>
    </nav>

    <!-- 主内容区 -->
    <main class="max-w-7xl mx-auto p-4 sm:p-6 lg:p-8">

        <!-- 首页 (Home) -->
        <section id="home" class="page-section active">
            <!-- 欢迎横幅 -->
            <div class="relative bg-gradient-to-r from-pink-600 to-indigo-700 text-blue p-10 sm:p-16 rounded-2xl shadow-xl overflow-hidden mb-12">
                <div class="relative z-10">
                    <h1 class="text-4xl md:text-5xl font-bold mb-4" data-lang-key="home.title">欢迎来到我的自由理科空间</h1>
                    <p class="text-xl md:text-2xl" data-lang-key="home.subtitle">探索、学习、分享：我的数学、物理、化学与生物之旅。</p>
                </div>
                <!-- 装饰性 SVG -->
                <svg class="absolute z-0 top-0 left-0 w-64 h-64 opacity-20 -translate-x-12 -translate-y-12 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1.5a4.5 4.5 0 014.5-4.5h3a4.5 4.5 0 014.5 4.5V21zm4-12a2 2 0 100-4 2 2 0 000 4z"></path></svg>
                <svg class="absolute z-0 bottom-0 right-0 w-72 h-72 opacity-20 translate-x-16 translate-y-16 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M14 10l-2 1m0 0l-2-1m2 1v2.5M20 7l-2 1m2-1l-2-1m2 1v2.5M14 4l-2-1-2 1M4 7l2 1M4 7l2-1M4 7v2.5M12 21.25l-2-1l-2 1v-2.5l2 1 2-1V21.25zM12 11.25l-2-1-2 1v-2.5l2 1 2-1V11.25zM20 11.25l-2-1-2 1v-2.5l2 1 2-1V11.25zM4 11.25l-2-1-2 1v-2.5l2 1 2-1V11.25z"></path></svg>
            </div>
            
            <!-- 学科概览 -->
            <h2 class="text-3xl font-bold mb-6 text-gray-900" data-lang-key="home.subjects_title">学科概览</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- 数学卡片 -->
                <div class="subject-card p-6 flex flex-col items-center text-center">
                    <div class="bg-blue-100 text-blue-700 p-4 rounded-full mb-4">
                        <svg class="w-10 h-10" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 7h6m0 10v-3m-3 3h.01M9 17h.01M9 14h.01M12 14h.01M15 14h.01M12 17h.01M15 17h.01M9 10h.01M12 10h.01M15 10h.01M3 4a1 1 0 011-1h16a1 1 0 011 1v10a1 1 0 01-1 1H4a1 1 0 01-1-1V4z" /></svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-2" data-lang-key="subject.math">数学</h3>
                    <p class="text-gray-600" data-lang-key="subject.math_desc">从微积分到线性代数，探索数字与逻辑的世界。</p>
                </div>
                <!-- 物理卡片 -->
                <div class="subject-card p-6 flex flex-col items-center text-center">
                    <div class="bg-red-100 text-red-700 p-4 rounded-full mb-4">
                        <svg class="w-10 h-10" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" /></svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-2" data-lang-key="subject.physics">物理</h3>
                    <p class="text-gray-600" data-lang-key="subject.physics_desc">理解宇宙的法则，从经典力学到量子物理。</p>
                </div>
                <!-- 化学卡片 -->
                <div class="subject-card p-6 flex flex-col items-center text-center">
                    <div class="bg-green-100 text-green-700 p-4 rounded-full mb-4">
                        <svg class="w-10 h-10" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.965l-2.287 2.287-.51.51a2 2 0 01-2.828 0l-2.287-2.287a2 2 0 010-2.828l.51-.51L9.5 7.71a6 6 0 00.965-3.86l-.477-2.387a2 2 0 00-.547-1.022A2 2 0 007.954 0H6.046a2 2 0 00-1.903 1.022 2 2 0 00-.547 1.022l.477 2.387a6 6 0 003.86.965l2.287 2.287.51.51a2 2 0 012.828 0l2.287 2.287a2 2 0 010 2.828l-.51.51-2.287 2.287a6 6 0 00-.965 3.86l.477 2.387a2 2 0 00.547 1.022A2 2 0 0016.046 24h1.908a2 2 0 001.903-1.022 2 2 0 00.547-1.022l-.477-2.387a6 6 0 00-3.86-.965l-2.287-2.287-.51-.51a2 2 0 01-2.828 0l-2.287-2.287a2 2 0 010-2.828l.51-.51 2.287-2.287a6 6 0 003.86-.965l2.387.477a2 2 0 001.022.547A2 2 0 0021.954 16.5H20.046a2 2 0 00-1.903-1.022 2 2 0 00-1.022.547z" /></svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-2" data-lang-key="subject.chemistry">化学</h3>
                    <p class="text-gray-600" data-lang-key="subject.chemistry_desc">探究物质的构成、性质和变化。</p>
                </div>
                <!-- 生物卡片 -->
                <div class="subject-card p-6 flex flex-col items-center text-center">
                    <div class="bg-yellow-100 text-yellow-700 p-4 rounded-full mb-4">
                        <svg class="w-10 h-10" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" /><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" /></svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-2" data-lang-key="subject.biology">生物</h3>
                    <p class="text-gray-600" data-lang-key="subject.biology_desc">从微观细胞到宏观生态，理解生命的奥秘。</p>
                </div>
            </div>
        </section>

        <!-- 关于我 (About) -->
        <section id="about" class="page-section bg-white p-8 rounded-xl shadow-lg">
            <h2 class="text-3xl font-bold mb-6 text-gray-900" data-lang-key="about.title">关于我</h2>
            <div class="flex flex-col md:flex-row items-center gap-8">
                <img src="https://placehold.co/200x200/E2E8F0/3B82F6?text=Me" alt="[个人头像]" class="w-48 h-48 rounded-full shadow-md object-cover flex-shrink-0">
                <div class="text-lg text-gray-700 space-y-4">
                    <p data-lang-key="about.p1">你好！我是一名热衷于理科学习的学生。我对解开复杂的数学难题、理解宇宙的物理规律、探索物质的奥秘充满热情。</p>
                    <p data-lang-key="about.p2">创建这个网站的目的是为了系统地整理我的学习笔记、分享有用的资源，并记录我在理科学习道路上的成长与思考。我相信，分享是最好的学习方式。</p>
                    <p data-lang-key="about.p3">希望这个网站也能对你有所启发！</p>
                </div>
            </div>
        </section>

        <!-- 学科 (Subjects) -->
        <section id="subjects" class="page-section">
            <h2 class="text-3xl font-bold mb-6 text-gray-900" data-lang-key="subjects.title">学科详情</h2>
            <p class="text-lg text-gray-700 mb-8" data-lang-key="subjects.desc">在这里，我将深入探讨每个学科。选择一个学科开始探索：</p>
            
            <!-- 学科导航 (Tabs) - 简单实现 -->
            <div class="flex flex-wrap gap-2 mb-8">
                <button data-subject-tab="math" class="subject-tab-btn px-4 py-2 rounded-md font-medium bg-blue-600 text-white transition-all duration-300 shadow-md" data-lang-key="subject.math">数学</button>
                <button data-subject-tab="physics" class="subject-tab-btn px-4 py-2 rounded-md font-medium bg-white text-gray-700 hover:bg-gray-200 transition-all duration-300 shadow-sm hover:shadow-md" data-lang-key="subject.physics">物理</button>
                <button data-subject-tab="chemistry" class="subject-tab-btn px-4 py-2 rounded-md font-medium bg-white text-gray-700 hover:bg-gray-200 transition-all duration-300 shadow-sm hover:shadow-md" data-lang-key="subject.chemistry">化学</button>
                <button data-subject-tab="biology" class="subject-tab-btn px-4 py-2 rounded-md font-medium bg-white text-gray-700 hover:bg-gray-200 transition-all duration-300 shadow-sm hover:shadow-md" data-lang-key="subject.biology">生物</button>
            </div>
            
            <!-- 学科内容容器 -->
            <div class="bg-white p-8 rounded-xl shadow-lg min-h-[300px]">
                <!-- 数学内容 -->
                <div id="subject-content-math" class="subject-content active">
                    <h3 class="text-2xl font-semibold mb-4" data-lang-key="subject.math">数学 (Mathematics)</h3>
                    <p class="text-gray-700 mb-4" data-lang-key="subjects.math_detail">数学是科学的语言。本板块包含函数、微积分、线性代数、概率论等核心概念的笔记和练习。</p>
                    <h4 class="text-xl font-semibold mt-6 mb-3" data-lang-key="subjects.topics">重点主题：</h4>
                    <ul class="list-disc list-inside text-gray-700 space-y-1">
                        <li data-lang-key="subjects.math_t1">微积分 (Calculus)</li>
                        <li data-lang-key="subjects.math_t2">线性代数 (Linear Algebra)</li>
                        <li data-lang-key="subjects.math_t3">概率与统计 (Probability & Statistics)</li>
                    </ul>
                </div>
                <!-- 物理内容 -->
                <div id="subject-content-physics" class="subject-content hidden">
                    <h3 class="text-2xl font-semibold mb-4" data-lang-key="subject.physics">物理 (Physics)</h3>
                    <p class="text-gray-700 mb-4" data-lang-key="subjects.physics_detail">物理学探索宇宙的基本原理。这里有关于经典力学、电磁学、热力学和现代物理学的学习记录。</p>
                    <h4 class="text-xl font-semibold mt-6 mb-3" data-lang-key="subjects.topics">重点主题：</h4>
                    <ul class="list-disc list-inside text-gray-700 space-y-1">
                        <li data-lang-key="subjects.physics_t1">群论香香 (Group Theory)</li>
                        <a 
  href="https://raw.githubusercontent.com/Uugyfgyb/Fujiasheng/4669e85de00f6b1317c6ecc1adda6f95951d064d/GT.pdf"
  download="GT文件.pdf"
>
  点击下载 GT.pdf 文件
</a>
                         <a 
  href="https://raw.githubusercontent.com/Uugyfgyb/Fujiasheng/1d5a1b1d1f8d14f1ad3306841aea536b76cb6f92/group-theory-chap7.pdf"
  download="群论第7章.pdf"
>
  点击下载 群论 (group-theory) 第七章 PDF
</a>

                        <li data-lang-key="subjects.physics_t2">电磁学 (Electromagnetism)</li>
                        
                        <li data-lang-key="subjects.physics_t3">相对论 (Relativity)</li>
                    </ul>
                </div>
                <!-- 化学内容 -->
                <div id="subject-content-chemistry" class="subject-content hidden">
                    <h3 class="text-2xl font-semibold mb-4" data-lang-key="subject.chemistry">化学 (Chemistry)</h3>
                    <p class="text-gray-700 mb-4" data-lang-key="subjects.chemistry_detail">化学是研究物质及其变化的中心科学。内容涵盖原子结构、化学键、热化学和有机化学。</p>
                    <h4 class="text-xl font-semibold mt-6 mb-3" data-lang-key="subjects.topics">重点主题：</h4>
                    <ul class="list-disc list-inside text-gray-700 space-y-1">
                        <li data-lang-key="subjects.chem_t1">有机化学 (Organic Chemistry)</li>
                        <li data-lang-key="subjects.chem_t2">化学反应动力学 (Kinetics)</li>
                        <li data-lang-key="subjects.chem_t3">元素周期表 (Periodic Table)</li>
                    </ul>
                </div>
                <!-- 生物内容 -->
                <div id="subject-content-biology" class="subject-content hidden">
                    <h3 class="text-2xl font-semibold mb-4" data-lang-key="subject.biology">生物 (Biology)</h3>
                    <p class="text-gray-700 mb-4" data-lang-key="subjects.biology_detail">生物学探索生命的奇迹。本部分包括细胞生物学、遗传学、进化论和生态学的笔记。</p>
                    <h4 class="text-xl font-semibold mt-6 mb-3" data-lang-key="subjects.topics">重点主题：</h4>
                    <ul class="list-disc list-inside text-gray-700 space-y-1">
                        <li data-lang-key="subjects.bio_t1">遗传学与 DNA (Genetics & DNA)</li>
                        <li data-lang-key="subjects.bio_t2">细胞生物学 (Cell Biology)</li>
                        <li data-lang-key="subjects.bio_t3">进化论 (Evolution)</li>
                    </ul>
                </div>
            </div>

            <!-- ✨ 新增的 AI 概念解析功能 ✨ -->
            <div class="mt-12 bg-white p-6 sm:p-8 rounded-xl shadow-lg border border-gray-200">
                <h3 class="text-2xl font-bold mb-4 flex items-center text-gray-900">
                    <span class="text-yellow-500 mr-2">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707m12.728 0l-.707-.707M12 21v-1" />
                        </svg>
                    </span>
                    <span data-lang-key="ai.title">AI 概念解析</span>
                </h3>
                <p class="text-gray-700 mb-5" data-lang-key="ai.desc">
                    对某个理科概念感到困惑吗？问问 AI 吧！
                </p>
                <div class="flex flex-col sm:flex-row gap-2 mb-4">
                    <input id="ai-prompt" type="text" class="flex-grow p-3 border border-gray-300 rounded-lg shadow-sm focus:ring-2 focus:ring-blue-500 outline-none" data-lang-key="ai.placeholder" placeholder="输入一个理科概念 (如：牛顿第二定律)">
                    <button id="ai-submit-btn" class="bg-gradient-to-r from-blue-600 to-indigo-700 text-white font-bold py-3 px-5 rounded-lg shadow-md hover:shadow-lg transition-all duration-300 flex items-center justify-center disabled:opacity-50 disabled:cursor-not-allowed">
                        <span class="mr-2">✨</span>
                        <span data-lang-key="ai.button">提问</span>
                    </button>
                </div>
                <!-- 结果区 -->
                <div id="ai-result-container" class="mt-4 p-5 bg-gray-50 rounded-lg border border-gray-200 min-h-[100px]" style="display: none;">
                    <!-- 加载中 -->
                    <div id="ai-loading" class="text-center py-4" style="display: none;">
                        <svg class="animate-spin h-6 w-6 text-blue-600 mx-auto" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
                            <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
                            <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
                        </svg>
                        <p class="mt-2 text-gray-600" data-lang-key="ai.loading">正在思考中...</p>
                    </div>
                    <!-- 结果 -->
                    <div id="ai-result-text" class="text-gray-800 space-y-3 leading-relaxed"></div>
                    <!-- 错误信息 -->
                    <div id="ai-error" class="text-red-600 font-medium" style="display: none;"></div>
                </div>
            </div>

        </section>

        <!-- 学习笔记 (Notes) -->
        <section id="notes" class="page-section">
            <h2 class="text-3xl font-bold mb-6 text-gray-900" data-lang-key="notes.title">学习笔记</h2>
            <p class="text-lg text-gray-700 mb-8" data-lang-key="notes.desc">这是我最近的学习记录和项目总结。</p>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <!-- 笔记卡片 1 -->
                <div class="note-card">
                    <img src="https://placehold.co/400x200/3B82F6/FFFFFF?text=Calculus" alt="[微积分笔记]" class="w-full h-40 object-cover">
                    <div class="p-6">
                        <span class="text-sm text-blue-600 font-medium" data-lang-key="subject.math">数学</span>
                        <h3 class="text-xl font-semibold my-2" data-lang-key="notes.note1_title">微积分核心：导数与积分</h3>
                        <p class="text-gray-600" data-lang-key="notes.note1_desc">一篇关于导数几何意义和积分应用的总结笔记。</p>
                    </div>
                </div>
                <!-- 笔记卡片 2 -->
                <div class="note-card">
                    <img src="https://placehold.co/400x200/10B981/FFFFFF?text=Chemistry" alt="[化学实验]" class="w-full h-40 object-cover">
                    <div class="p-6">
                        <span class="text-sm text-green-600 font-medium" data-lang-key="subject.chemistry">化学</span>
                        <h3 class="text-xl font-semibold my-2" data-lang-key="notes.note2_title">有机化学反应机制</h3>
                        <p class="text-gray-600" data-lang-key="notes.note2_desc">整理 SN1, SN2, E1, E2 反应的区别和实例。</p>
                    </div>
                </div>
                <!-- 笔记卡片 3 -->
                <div class="note-card">
                    <img src="https://placehold.co/400x200/EF4444/FFFFFF?text=Physics" alt="[物理项目]" class="w-full h-40 object-cover">
                    <div class="p-6">
                        <span class="text-sm text-red-600 font-medium" data-lang-key="subject.physics">物理</span>
                        <h3 class="text-xl font-semibold my-2" data-lang-key="notes.note3_title">项目：搭建一个简易电磁炮</h3>
                        <p class="text-gray-600" data-lang-key="notes.note3_desc">记录一次物理课外项目，关于线圈、电容和楞次定律的应用。</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- 学习资源 (Resources) -->
        <section id="resources" class="page-section bg-white p-8 rounded-xl shadow-lg">
            <h2 class="text-3xl font-bold mb-6 text-gray-900" data-lang-key="resources.title">学习资源</h2>
            <p class="text-lg text-gray-700 mb-8" data-lang-key="resources.desc">一些我发现非常有帮助的网站、工具和频道。</p>
            
            <div class="space-y-6">
                <!-- 资源 1 -->
                <div>
                    <h3 class="text-xl font-semibold text-blue-700" data-lang-key="resources.r1_title">可汗学院 (Khan Academy)</h3>
                    <p class="text-gray-600" data-lang-key="resources.r1_desc">非常棒的免费学习平台，涵盖了从基础数学到高等物理的各种课程。</p>
                    <a href="https://www.khanacademy.org/" target="_blank" class="text-blue-500 hover:underline font-medium transition-colors duration-300 hover:text-blue-700" data-lang-key="resources.link">访问网站 &rarr;</a>
                </div>
                <!-- 资源 2 -->
                <div>
                    <h3 class="text-xl font-semibold text-blue-700" data-lang-key="resources.r2_title">3Blue1Brown</h3>
                    <p class="text-gray-600" data-lang-key="resources.r2_desc">一个专注于数学可视化的 YouTube 频道，能让你直观地理解复杂的数学概念。</p>
                    <a href="https://www.youtube.com/c/3blue1brown" target="_blank" class="text-blue-500 hover:underline font-medium transition-colors duration-300 hover:text-blue-700" data-lang-key="resources.link">访问网站 &rarr;</a>
                </div>
                <!-- 资源 3 -->
                <div>
                    <h3 class="text-xl font-semibold text-blue-700" data-lang-key="resources.r3_title">WolframAlpha</h3>
                    <p class="text-gray-600" data-lang-key="resources.r3_desc">强大的计算知识引擎，是解决数学和科学计算问题的利器。</p>
                    <a href="https://www.wolframalpha.com/" target="_blank" class="text-blue-500 hover:underline font-medium transition-colors duration-300 hover:text-blue-700" data-lang-key="resources.link">访问网站 &rarr;</a>
                </div>
                <!-- 资源 4 (新增) -->
                <div>
                    <h3 class="text-xl font-semibold text-blue-700" data-lang-key="resources.r4_title">PhET 互动模拟 (PhET Simulations)</h3>
                    <p class="text-gray-600" data-lang-key="resources.r4_desc">科罗拉多大学出品的免费互动数学和科学模拟，非常直观。</p>
                    <a href="https://phet.colorado.edu/" target="_blank" class="text-blue-500 hover:underline font-medium transition-colors duration-300 hover:text-blue-700" data-lang-key="resources.link">访问网站 &rarr;</a>
                </div>
                <!-- 资源 5 (新增) -->
                <div>
                    <h3 class="text-xl font-semibold text-blue-700" data-lang-key="resources.r5_title">Crash Course (速成课程)</h3>
                    <p class="text-gray-600" data-lang-key="resources.r5_desc">YouTube 上的一个王牌科普频道，用生动的动画快速讲解各种学科知识。</p>
                    <a href="https://www.youtube.com/user/crashcourse" target="_blank" class="text-blue-500 hover:underline font-medium transition-colors duration-300 hover:text-blue-700" data-lang-key="resources.link">访问网站 &rarr;</a>
                </div>
                <!-- 资源 6 (新增) -->
                <div>
                    <h3 class="text-xl font-semibold text-blue-700" data-lang-key="resources.r6_title">MIT OpenCourseWare</h3>
                    <p class="text-gray-600" data-lang-key="resources.r6_desc">麻省理工学院的开放课程，提供了大量的大学级别理科课程资料。</p>
                    <a href="https://ocw.mit.edu/" target="_blank" class="text-blue-500 hover:underline font-medium transition-colors duration-300 hover:text-blue-700" data-lang-key="resources.link">访问网站 &rarr;</a>
                </div>
            </div>
        </section>

    </main>

    <!-- 页脚 -->
    <footer class="text-center p-6 mt-12 bg-gray-200">
        <p class="text-gray-600" data-lang-key="footer.text">&copy; 2025 [你的名字]. 保留所有权利。</p>
    </footer>

    <!-- JavaScript 脚本 -->
    <script>
        // 语言翻译数据
        const translations = {
            en: {
                "head.title": "Student Science Hub",
                "nav.title": "Science Hub",
                "nav.home": "Home",
                "nav.about": "About Me",
                "nav.subjects": "Subjects",
                "nav.notes": "Notes",
                "nav.resources": "Resources",
                "home.title": "Welcome to My Science Hub",
                "home.subtitle": "Explore, learn, and share: My journey through Math, Physics, Chemistry, and Biology.",
                "home.subjects_title": "Subjects Overview",
                "subject.math": "Mathematics",
                "subject.math_desc": "From calculus to linear algebra, exploring the world of numbers and logic.",
                "subject.physics": "Physics",
                "subject.physics_desc": "Understanding the laws of the universe, from classical mechanics to quantum physics.",
                "subject.chemistry": "Chemistry",
                "subject.chemistry_desc": "Investigating the composition, properties, and changes of matter.",
                "subject.biology": "Biology",
                "subject.biology_desc": "Understanding the mysteries of life, from micro-cells to macro-ecology.",
                "about.title": "About Me",
                "about.p1": "Hello! I am a student passionate about science. I am enthusiastic about solving complex math problems, understanding the physical laws of the universe, exploring chemical reactions, and studying the wonders of life.",
                "about.p2": "I created this website to systematically organize my study notes, share useful resources, and document my growth and thoughts on the path of science learning. I believe sharing is the best way to learn.",
                "about.p3": "My goal is [Write your goal here, e.g., to study at XYZ University or win an award in a science competition]. I hope this website can inspire you too!",
                "subjects.title": "Subject Details",
                "subjects.desc": "Here, I dive deeper into each subject. Choose one to start exploring:",
                "subjects.topics": "Key Topics:",
                "subjects.math_detail": "Mathematics is the language of science. This section contains notes and exercises on core concepts like functions, calculus, linear algebra, and probability.",
                "subjects.math_t1": "Calculus",
                "subjects.math_t2": "Linear Algebra",
                "subjects.math_t3": "Probability & Statistics",
                "subjects.physics_detail": "Physics explores the fundamental principles of the universe. Here are study records on classical mechanics, electromagnetism, thermodynamics, and modern physics.",
                "subjects.physics_t1": "Newtonian Mechanics",
                "subjects.physics_t2": "Electromagnetism",
                "subjects.physics_t3": "Relativity",
                "subjects.chemistry_detail": "Chemistry is the central science studying matter and its changes. Content covers atomic structure, chemical bonds, thermochemistry, and organic chemistry.",
                "subjects.chem_t1": "Organic Chemistry",
                "subjects.chem_t2": "Kinetics",
                "subjects.chem_t3": "Periodic Table",
                "subjects.biology_detail": "Biology explores the wonders of life. This section includes notes on cell biology, genetics, evolution, and ecology.",
                "subjects.bio_t1": "Genetics & DNA",
                "subjects.bio_t2": "Cell Biology",
                "subjects.bio_t3": "Evolution",
                "notes.title": "Study Notes",
                "notes.desc": "Here are my recent study logs and project summaries.",
                "notes.note1_title": "Calculus Core: Derivatives & Integrals",
                "notes.note1_desc": "A summary note on the geometric meaning of derivatives and the application of integrals.",
                "notes.note2_title": "Organic Chemistry Reaction Mechanisms",
                "notes.note2_desc": "Organizing the differences and examples of SN1, SN2, E1, and E2 reactions.",
                "notes.note3_title": "Project: Building a Simple Coilgun",
                "notes.note3_desc": "Documenting an extracurricular physics project on the application of coils, capacitors, and Lenz's Law.",
                "resources.title": "Learning Resources",
                "resources.desc": "Some websites, tools, and channels I've found incredibly helpful.",
                "resources.r1_title": "Khan Academy",
                "resources.r1_desc": "A fantastic free learning platform covering everything from basic math to advanced physics.",
                "resources.link": "Visit Website &rarr;",
                "resources.r2_title": "3Blue1Brown",
                "resources.r2_desc": "A YouTube channel focused on math visualization that helps you intuitively understand complex concepts.",
                "resources.r3_title": "WolframAlpha",
                "resources.r3_desc": "A powerful computational knowledge engine, a great tool for solving math and science problems.",
                "resources.r4_title": "PhET Interactive Simulations",
                "resources.r4_desc": "Free interactive math and science simulations from the University of Colorado Boulder. Very intuitive.",
                "resources.r5_title": "Crash Course",
                "resources.r5_desc": "A premier educational YouTube channel that explains various subjects with engaging animations.",
                "resources.r6_title": "MIT OpenCourseWare",
                "resources.r6_desc": "MIT's open-access course materials, offering a vast amount of university-level science resources.",
                "footer.text": "© 2025 [Jiasheng Fu]. All rights reserved.",
                "ai.title": "AI Concept Explainer",
                "ai.desc": "Confused about a science concept? Ask the AI!",
                "ai.placeholder": "Enter a science concept (e.g., Newton's Second Law)",
                "ai.button": "Ask",
                "ai.loading": "Thinking...",
                "ai.error": "An error occurred. Please try again later.",
                "ai.general_science": "General Science"
            },
            cn: {
                "head.title": "理科学习空间",
                "nav.title": "理科学习空间",
                "nav.home": "首页",
                "nav.about": "关于我",
                "nav.subjects": "学科",
                "nav.notes": "学习笔记",
                "nav.resources": "学习资源",
                "home.title": "欢迎来到我的理科空间",
                "home.subtitle": "探索、学习、分享：我的数学、物理、化学与生物之旅。",
                "home.subjects_title": "学科概览",
                "subject.math": "数学",
                "subject.math_desc": "从微积分到线性代数，探索数字与逻辑的世界。",
                "subject.physics": "物理",
                "subject.physics_desc": "理解宇宙的法则，从经典力学到量子物理。",
                "subject.chemistry": "化学",
                "subject.chemistry_desc": "探究物质的构成、性质和变化。",
                "subject.biology": "生物",
                "subject.biology_desc": "从微观细胞到宏观生态，理解生命的奥秘。",
                "about.title": "关于我",
                "about.p1": "你好！我是一名热衷于理科学习的学生。我对解开复杂的数学难题、理解宇宙的物理规律、探索物质的化学反应以及研究奇妙的生命现象充满热情。",
                "about.p2": "创建这个网站的目的是为了系统地整理我的学习笔记、分享有用的资源，并记录我在理科学习道路上的成长与思考。我相信，分享是最好的学习方式。",
                "subjects.title": "学科详情",
                "subjects.desc": "在这里，我将深入探讨每个学科。选择一个学科开始探索：",
                "subjects.topics": "重点主题：",
                "subjects.math_detail": "数学是科学的语言。本板块包含函数、微积分、线性代数、概率论等核心概念的笔记和练习。",
                "subjects.math_t1": "微积分 (Calculus)",
                "subjects.math_t2": "线性代数 (Linear Algebra)",
                "subjects.math_t3": "概率与统计 (Probability & Statistics)",
                "subjects.physics_detail": "物理学探索宇宙的基本原理。这里有关于经典力学、电磁学、热力学和现代物理学的学习记录。",
                "subjects.physics_t1": "牛顿力学 (Newtonian Mechanics)",
                "subjects.physics_t2": "电磁学 (Electromagnetism)",
                "subjects.physics_t3": "相对论 (Relativity)",
                "subjects.chemistry_detail": "化学是研究物质及其变化的中心科学。内容涵盖原子结构、化学键、热化学和有机化学。",
                "subjects.chem_t1": "有机化学 (Organic Chemistry)",
                "subjects.chem_t2": "化学反应动力学 (Kinetics)",
                "subjects.chem_t3": "元素周期表 (Periodic Table)",
                "subjects.biology_detail": "生物学探索生命的奇迹。本部分包括细胞生物学、遗传学、进化论和生态学的笔记。",
                "subjects.bio_t1": "遗传学与 DNA (Genetics & DNA)",
                "subjects.bio_t2": "细胞生物学 (Cell Biology)",
                "subjects.bio_t3": "进化论 (Evolution)",
                "notes.title": "学习笔记",
                "notes.desc": "这是我最近的学习记录和项目总结。",
                "notes.note1_title": "微积分核心：导数与积分",
                "notes.note1_desc": "一篇关于导数几何意义和积分应用的总结笔记。",
                "notes.note2_title": "有机化学反应机制",
                "notes.note2_desc": "整理 SN1, SN2, E1, E2 反应的区别和实例。",
                "notes.note3_title": "项目：搭建一个简易电磁炮",
                "notes.note3_desc": "记录一次物理课外项目，关于线圈、电容和楞次定律的应用。",
                "resources.title": "学习资源",
                "resources.desc": "一些我发现非常有帮助的网站、工具和频道。",
                "resources.r1_title": "可汗学院 (Khan Academy)",
                "resources.r1_desc": "非常棒的免费学习平台，涵盖了从基础数学到高等物理的各种课程。",
                "resources.link": "访问网站 ",
                "resources.r2_title": "3Blue1Brown",
                "resources.r2_desc": "一个专注于数学可视化的 YouTube 频道，能让你直观地理解复杂的数学概念。",
                "resources.r3_title": "WolframAlpha",
                "resources.r3_desc": "强大的计算知识引擎，是解决数学和科学计算问题的利器。",
                "resources.r4_title": "PhET 互动模拟 (PhET Simulations)",
                "resources.r4_desc": "科罗拉多大学出品的免费互动数学和科学模拟，非常直观。",
                "resources.r5_title": "Crash Course (速成课程)",
                "resources.r5_desc": "YouTube 上的一个王牌科普频道，用生动的动画快速讲解各种学科知识。",
                "resources.r6_title": "MIT OpenCourseWare",
                "resources.r6_desc": "麻省理工学院的开放课程，提供了大量的大学级别理科课程资料。",
                "footer.text": "© 2025 [Jiasheng Fu]. 保留所有权利。",
                "ai.title": "AI 概念解析",
                "ai.desc": "对某个理科概念感到困惑吗？问问 AI 吧！",
                "ai.placeholder": "输入一个理科概念 (如：牛顿第二定律)",
                "ai.button": "提问",
                "ai.loading": "正在思考中...",
                "ai.error": "抱歉，发生了一个错误，请稍后再试。",
                "ai.general_science": "综合理科"
            }
        };

        let currentLang = 'cn'; // 默认语言为中文

        // 语言切换函数
        function setLanguage(lang) {
            currentLang = lang;
            document.documentElement.lang = lang; // 更新 html 标签的 lang 属性
            
            // 存储用户偏好
            try {
                localStorage.setItem('preferredLang', lang);
            } catch (e) {
                console.warn("无法访问 localStorage:", e);
            }

            // 更新所有带 data-lang-key 属性的元素
            document.querySelectorAll('[data-lang-key]').forEach(el => {
                const key = el.getAttribute('data-lang-key');
                if (translations[lang] && translations[lang][key]) {
                    el.textContent = translations[lang][key];
                }
            });

            // 更新语言切换按钮的文本
            const langSwitcher = document.getElementById('lang-switcher');
            if (lang === 'en') {
                langSwitcher.textContent = '中文';
            } else {
                langSwitcher.textContent = 'English';
            }

            // 更新输入框的 placeholder
            const placeholderKey = 'ai.placeholder';
            const placeholderText = translations[lang] && translations[lang][placeholderKey] ? translations[lang][placeholderKey] : "Enter a science concept";
            document.getElementById('ai-prompt').setAttribute('placeholder', placeholderText);

            // 更新加载文本
             const loadingEl = document.getElementById('ai-loading');
             if (loadingEl.style.display !== 'none') {
                loadingEl.querySelector('p').textContent = translations[lang]['ai.loading'];
             }
        }

        // 页面导航函数
        function showPage(pageId) {
            // 隐藏所有页面
            document.querySelectorAll('.page-section').forEach(section => {
                section.classList.remove('active');
            });
            
            // 显示目标页面
            const targetPage = document.getElementById(pageId);
            if (targetPage) {
                targetPage.classList.add('active');
            }

            // 更新导航链接的激活状态
            document.querySelectorAll('.nav-link').forEach(link => {
                link.classList.remove('active', 'bg-blue-700', 'text-white');
                if (link.getAttribute('data-nav-link') === pageId) {
                    link.classList.add('active', 'bg-blue-700', 'text-white');
                }
            });

            // 关闭移动端菜单（如果打开）
            document.getElementById('mobile-menu').classList.add('hidden');
        }

        // 学科内 Tab 切换函数
        function showSubjectTab(subjectId) {
            // 隐藏所有学科内容
            document.querySelectorAll('.subject-content').forEach(content => {
                content.classList.add('hidden');
            });

            // 显示目标学科内容
            const targetContent = document.getElementById(`subject-content-${subjectId}`);
            if (targetContent) {
                targetContent.classList.remove('hidden');
            }

            // 更新 Tab 按钮样式
            document.querySelectorAll('.subject-tab-btn').forEach(btn => {
                // Inactive state
                btn.classList.remove('bg-blue-600', 'text-white', 'shadow-md');
                btn.classList.add('bg-white', 'text-gray-700', 'hover:bg-gray-200', 'shadow-sm', 'hover:shadow-md');
                
                if (btn.getAttribute('data-subject-tab') === subjectId) {
                    // Active state
                    btn.classList.add('bg-blue-600', 'text-white', 'shadow-md');
                    btn.classList.remove('bg-white', 'text-gray-700', 'hover:bg-gray-200', 'shadow-sm', 'hover:shadow-md');
                }
            });
        }

        // ✨ [新增] 获取当前激活的学科名称（用于 AI 上下文）
        function getActiveSubject() {
            const activeBtn = document.querySelector('.subject-tab-btn.bg-blue-600');
            if (activeBtn) {
                const subjectId = activeBtn.getAttribute('data-subject-tab');
                const key = `subject.${subjectId}`;
                if (translations[currentLang] && translations[currentLang][key]) {
                    return translations[currentLang][key]; // 返回 "数学", "Physics" 等
                }
            }
            return translations[currentLang]['ai.general_science'] || 'science'; // 降级处理
        }

        // ✨ [新增] 处理 AI 提问
        async function handleAiSubmit() {
            const promptInput = document.getElementById('ai-prompt');
            const submitBtn = document.getElementById('ai-submit-btn');
            const resultContainer = document.getElementById('ai-result-container');
            const loadingEl = document.getElementById('ai-loading');
            const resultTextEl = document.getElementById('ai-result-text');
            const errorEl = document.getElementById('ai-error');

            const userQuery = promptInput.value.trim();
            if (!userQuery) {
                return; // 如果输入为空则不执行
            }

            // 1. 设置加载状态
            submitBtn.disabled = true;
            resultContainer.style.display = 'block';
            loadingEl.style.display = 'block';
            resultTextEl.innerHTML = '';
            errorEl.style.display = 'none';
            // 更新加载文本的语言
            loadingEl.querySelector('p').textContent = translations[currentLang]['ai.loading'];


            try {
                // 2. 准备 API 请求
                const activeSubject = getActiveSubject(); // 获取当前学科上下文
                const responseLang = currentLang === 'cn' ? '中文' : 'English';
                const systemPrompt = `You are a helpful science tutor. Explain the following concept clearly and concisely, as if to a high school or early college student. The user is currently studying ${activeSubject}. Respond in ${responseLang}.`;
                
                const apiKey = ""; // API 密钥保持为空
                const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`;

                const payload = {
                    contents: [{ parts: [{ text: userQuery }] }],
                    systemInstruction: {
                        parts: [{ text: systemPrompt }]
                    },
                };
                
                // 3. 发送请求，带指数退避 (Exponential Backoff)
                const MAX_RETRIES = 5;
                let response = null;
                for (let i = 0; i < MAX_RETRIES; i++) {
                    try {
                        response = await fetch(apiUrl, {
                            method: 'POST',
                            headers: { 'Content-Type': 'application/json' },
                            body: JSON.stringify(payload)
                        });

                        if (response.status !== 429 && response.ok) {
                            break; // 成功或非限流错误，退出重试
                        }
                        
                        if (response.status === 429 && i < MAX_RETRIES - 1) {
                            const delay = Math.pow(2, i) * 1000 + Math.random() * 1000;
                            await new Promise(resolve => setTimeout(resolve, delay));
                        } else {
                            throw new Error(`API Error: ${response.status} ${response.statusText}`);
                        }
                    } catch (err) {
                        if (i === MAX_RETRIES - 1) throw err;
                        const delay = Math.pow(2, i) * 1000 + Math.random() * 1000;
                        await new Promise(resolve => setTimeout(resolve, delay));
                    }
                }
                
                if (!response || !response.ok) {
                     throw new Error("Failed to fetch response after multiple retries.");
                }

                const result = await response.json();

                // 4. 处理并显示结果
                if (result.candidates && result.candidates[0].content?.parts?.[0]?.text) {
                    const text = result.candidates[0].content.parts[0].text;
                    // 使用 Markdown 格式化（例如将 **粗体** 转换为 <strong> 标签）
                    let formattedText = text
                        .replace(/\*\*(.*?)\*\*/g, '<strong>$1</strong>')
                        .replace(/\*(.*?)\*/g, '<em>$1</em>');
                    
                    // 将换行符转换为段落或换行
                    formattedText = formattedText.split('\n').map(line => {
                        if (line.trim().startsWith('- ') || line.trim().startsWith('* ')) {
                            return `<li>${line.substring(2).trim()}</li>`;
                        }
                        return line.trim() === '' ? '' : `<p>${line.trim()}</p>`;
                    }).join('');

                    // 处理列表（如果需要）
                    if (formattedText.includes('<li>')) {
                        formattedText = `<ul>${formattedText}</ul>`;
                    }


                    resultTextEl.innerHTML = formattedText; 
                } else {
                    throw new Error("Invalid response structure from API.");
                }

            } catch (error) {
                console.error("Error calling Gemini API:", error);
                errorEl.textContent = translations[currentLang]['ai.error'];
                errorEl.style.display = 'block';
                resultTextEl.innerHTML = ''; // 清空可能存在的部分结果
            } finally {
                // 5. 移除加载状态
                submitBtn.disabled = false;
                loadingEl.style.display = 'none';
            }
        }


        // DOM 加载完成后执行
        document.addEventListener('DOMContentLoaded', () => {
            const langSwitcher = document.getElementById('lang-switcher');
            const mobileMenuButton = document.getElementById('mobile-menu-button');
            const mobileMenu = document.getElementById('mobile-menu');
            const aiPromptInput = document.getElementById('ai-prompt');
            
            // 1. 设置语言切换
            langSwitcher.addEventListener('click', () => {
                setLanguage(currentLang === 'en' ? 'cn' : 'en');
            });

            // 2. 检查本地存储的语言偏好
            let preferredLang = 'cn';
            try {
                preferredLang = localStorage.getItem('preferredLang') || 'cn';
            } catch (e) {
                console.warn("无法访问 localStorage:", e);
            }
            setLanguage(preferredLang);

            // 3. 移动端菜单切换
            mobileMenuButton.addEventListener('click', () => {
                mobileMenu.classList.toggle('hidden');
            });

            // 4. 设置页面导航
            document.querySelectorAll('.nav-link').forEach(link => {
                link.addEventListener('click', (e) => {
                    e.preventDefault();
                    const pageId = link.getAttribute('data-nav-link');
                    // 更新 URL hash
                    window.location.hash = pageId;
                    showPage(pageId);
                });
            });

            // 5. 设置学科内 Tab 导航
            document.querySelectorAll('.subject-tab-btn').forEach(btn => {
                btn.addEventListener('click', (e) => {
                    const subjectId = btn.getAttribute('data-subject-tab');
                    showSubjectTab(subjectId);
                });
            });

            // 6. 监听 URL hash 变化以实现页面导航（例如刷新或后退）
            function handleHashChange() {
                const hash = window.location.hash.substring(1) || 'home';
                showPage(hash);
                
                // 如果 hash 是某个学科，也需要切换到 "学科" 主页面
                const subjectPages = ['math', 'physics', 'chemistry', 'biology'];
                if (subjectPages.includes(hash)) {
                    showPage('subjects');
                    showSubjectTab(hash);
                }
            }

            window.addEventListener('hashchange', handleHashChange);
            
            // 7. 页面初始加载时处理
            handleHashChange();

            // 8. ✨ [新增] 为 AI 提交按钮添加事件监听
            document.getElementById('ai-submit-btn').addEventListener('click', handleAiSubmit);

            // 9. 允许在输入框中按 Enter 提交
             aiPromptInput.addEventListener('keydown', (e) => {
                if (e.key === 'Enter') {
                    e.preventDefault(); // 阻止默认的换行行为
                    handleAiSubmit();
                }
            });
        });

    </script>
</body>
</html>
