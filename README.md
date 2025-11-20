欢迎付骏怡登舰！
<html lang="en" class="scroll-smooth">
<head>
    <!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-3E9KNYG7D1"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-3E9KNYG7D1');
</script>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title data-lang-key="head.title">Student Science Hub | 理科学习空间</title>
    <!-- 引入 Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- 引入 Inter 字体 -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&family=Noto+Sans+SC:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        /* 全局样式 */
        body {
            font-family: 'Inter', 'Noto Sans SC', sans-serif;
            /* 深空背景：使用径向渐变模拟宇宙光辉 */
            background: radial-gradient(circle at top left, #1a2a44, #0f172a, #000000);
            background-attachment: fixed; /* 背景固定，产生视差感 */
            color: #e2e8f0; /* 浅灰文字 */
            min-height: 100vh;
        }
        
        /* 磨砂玻璃卡片效果 */
        .glass-card {
            background: rgba(30, 41, 59, 0.6); /* 深色半透明 */
            backdrop-filter: blur(12px); /* 毛玻璃模糊 */
            border: 1px solid rgba(255, 255, 255, 0.1); /* 微弱边框 */
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.37);
        }

        /* 导航栏磨砂 */
        .glass-nav {
            background: rgba(15, 23, 42, 0.8);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }
        
        /* 隐藏 section 的基类 */
        .page-section {
            display: none;
            opacity: 0;
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
            transform: translateY(30px) scale(0.98);
        }
        /* 显示当前 active 的 section */
        .page-section.active {
            display: block;
            opacity: 1;
            transform: translateY(0) scale(1);
        }
        
        /* 导航链接激活状态 */
        .nav-link.active {
            @apply text-cyan-400 font-bold;
            text-shadow: 0 0 10px rgba(34, 211, 238, 0.5); /* 霓虹光晕 */
        }

        .nav-link:hover {
            @apply text-cyan-300;
        }
        
        /* 学科卡片悬停效果 */
        .subject-card {
            @apply rounded-xl p-6 flex flex-col items-center text-center transition-all duration-300 ease-in-out glass-card;
        }
        .subject-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 40px rgba(34, 211, 238, 0.15); /* 青色光晕 */
            border-color: rgba(34, 211, 238, 0.3);
        }

        /* AI 结果区的 Markdown 渲染样式 */
        #ai-result-text {
            color: #cbd5e1;
        }
        #ai-result-text strong {
            color: #38bdf8; /* 天蓝色粗体 */
        }
        #ai-result-text p, #ai-result-text ul {
            margin-bottom: 0.5rem;
        }
        #ai-result-text ul {
            list-style: disc;
            margin-left: 1.5rem;
            padding-left: 0;
        }
        #ai-result-text li {
            margin-bottom: 0.25rem;
        }

        /* 子分类列表样式 */
        .sub-topic-list {
            margin-left: 0.75rem;
            margin-top: 0.5rem;
            padding-left: 1rem;
            border-left: 1px solid rgba(255, 255, 255, 0.1);
        }
        .sub-topic-item {
            display: flex;
            align-items: center;
            margin-bottom: 0.5rem;
            font-size: 0.95rem;
            color: #94a3b8;
        }
        .sub-topic-item:hover {
            color: #e2e8f0;
        }
        /* 文件链接预留位样式 */
        .file-link-placeholder {
            margin-left: auto;
            font-size: 0.75rem;
            padding: 2px 8px;
            border-radius: 4px;
            background: rgba(255,255,255,0.05);
            color: #64748b;
            border: 1px dashed #475569;
            transition: all 0.2s;
            text-decoration: none;
        }
        .file-link-placeholder:hover {
            color: #38bdf8;
            border-color: #38bdf8;
            background: rgba(56, 189, 248, 0.1);
        }

        /* 自定义滚动条 */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0f172a; 
        }
        ::-webkit-scrollbar-thumb {
            background: #334155; 
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #475569; 
        }

        /* 资源面板滚动区 */
        .resource-scroll-area {
            max-height: 800px; /* 限制高度以允许滚动 */
            overflow-y: auto;
            padding-right: 10px;
        }
    </style>
    <meta name="google-site-verification" content="nvR5HccczyAA8jNXLNqO3pslMFm8AWp1JCqGeqW3R-k" />
</head>
<body>

    <!-- 导航栏 -->
    <nav class="glass-nav sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <!-- Logo 和 标题 -->
                <div class="flex-shrink-0 flex items-center cursor-pointer" onclick="window.location.hash='home'">
                    <!-- 量子地球 Logo -->
                    <svg class="h-10 w-10" viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <!-- 核心光晕 -->
                        <circle cx="32" cy="32" r="8" fill="#38BDF8" fill-opacity="0.8">
                            <animate attributeName="opacity" values="0.8;0.4;0.8" dur="3s" repeatCount="indefinite" />
                        </circle>
                        <!-- 经纬线 (地球感) -->
                        <path d="M32 4C32 4 16 16 16 32C16 48 32 60 32 60" stroke="#38BDF8" stroke-width="0.5" stroke-opacity="0.3"/>
                        <path d="M32 4C32 4 48 16 48 32C48 48 32 60 32 60" stroke="#38BDF8" stroke-width="0.5" stroke-opacity="0.3"/>
                        <circle cx="32" cy="32" r="28" stroke="#38BDF8" stroke-width="0.5" stroke-opacity="0.3"/>
                        <!-- 轨道环 1 -->
                        <ellipse cx="32" cy="32" rx="28" ry="10" stroke="#A78BFA" stroke-width="2" transform="rotate(45 32 32)">
                             <animateTransform attributeName="transform" type="rotate" from="45 32 32" to="405 32 32" dur="10s" repeatCount="indefinite"/>
                        </ellipse>
                        <!-- 电子粒子 1 -->
                        <circle r="3" fill="#fff">
                            <animateMotion dur="10s" repeatCount="indefinite" path="M12.2 12.2 A 28 10 45 1 1 51.8 51.8 A 28 10 45 1 1 12.2 12.2" />
                        </circle>

                        <!-- 轨道环 2 -->
                        <ellipse cx="32" cy="32" rx="28" ry="10" stroke="#2DD4BF" stroke-width="2" transform="rotate(-45 32 32)">
                             <animateTransform attributeName="transform" type="rotate" from="-45 32 32" to="-405 32 32" dur="12s" repeatCount="indefinite"/>
                        </ellipse>
                    </svg>
                    <span class="font-bold text-xl ml-3 bg-clip-text text-transparent bg-gradient-to-r from-cyan-400 to-purple-400" data-lang-key="nav.title">Quantum Learning Hub</span>
                </div>
                
                <!-- 桌面导航链接 -->
                <div class="hidden sm:ml-6 sm:flex sm:space-x-4">
                    <a href="#home" data-nav-link="home" class="nav-link px-3 py-2 rounded-md text-sm font-medium text-gray-300 transition-all duration-300" data-lang-key="nav.home">首页</a>
                    <a href="#subjects" data-nav-link="subjects" class="nav-link px-3 py-2 rounded-md text-sm font-medium text-gray-300 transition-all duration-300" data-lang-key="nav.subjects">学科探索</a>
                    <a href="#resources" data-nav-link="resources" class="nav-link px-3 py-2 rounded-md text-sm font-medium text-gray-300 transition-all duration-300" data-lang-key="nav.resources">星际资源</a>
                </div>

                <!-- 语言切换按钮 -->
                <div class="flex items-center">
                    <button id="lang-switcher" class="px-4 py-1.5 rounded-full text-sm font-medium border border-cyan-500/50 text-cyan-400 hover:bg-cyan-500/10 transition-all">
                        EN
                    </button>
                    
                    <!-- 移动端菜单按钮 -->
                    <button id="mobile-menu-button" class="sm:hidden ml-3 p-2 rounded-md text-gray-300 hover:text-white">
                        <svg class="w-6 h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
                        </svg>
                    </button>
                </div>
            </div>
        </div>
        
        <!-- 移动端菜单 (默认隐藏) -->
        <div id="mobile-menu" class="sm:hidden hidden glass-nav border-t border-gray-700">
            <div class="px-2 pt-2 pb-3 space-y-1">
                <a href="#home" data-nav-link="home" class="nav-link block px-3 py-2 rounded-md text-base font-medium text-gray-300 hover:text-white hover:bg-gray-800" data-lang-key="nav.home">首页</a>
                <a href="#subjects" data-nav-link="subjects" class="nav-link block px-3 py-2 rounded-md text-base font-medium text-gray-300 hover:text-white hover:bg-gray-800" data-lang-key="nav.subjects">学科探索</a>
                <a href="#resources" data-nav-link="resources" class="nav-link block px-3 py-2 rounded-md text-base font-medium text-gray-300 hover:text-white hover:bg-gray-800" data-lang-key="nav.resources">星际资源</a>
            </div>
        </div>
    </nav>

    <!-- 主内容区 -->
    <main class="max-w-7xl mx-auto p-4 sm:p-6 lg:p-8">

        <!-- 首页 (Home) -->
        <section id="home" class="page-section active">
            <!-- 欢迎横幅 - 宇宙风格 -->
            <div class="relative rounded-3xl shadow-2xl overflow-hidden mb-12 border border-cyan-500/20">
                <!-- 动态背景 -->
                <div class="absolute inset-0 bg-gradient-to-r from-indigo-900 via-purple-900 to-slate-900"></div>
                <!-- 星星装饰 -->
                <div class="absolute inset-0" style="background-image: radial-gradient(white 1px, transparent 1px); background-size: 50px 50px; opacity: 0.1;"></div>
                
                <div class="relative z-10 p-10 sm:p-16 flex flex-col md:flex-row items-center gap-10">
                    <div class="flex-1">
                        <h1 class="text-4xl md:text-6xl font-bold mb-6 text-transparent bg-clip-text bg-gradient-to-r from-cyan-300 via-blue-300 to-purple-300" data-lang-key="home.title">开启你的理科宇宙</h1>
                        <p class="text-xl md:text-2xl text-blue-100 mb-6 leading-relaxed" data-lang-key="home.subtitle">探索数学的逻辑星云，穿越物理的法则虫洞，解构化学的元素矩阵，见证生物的生命奇迹。</p>
                        
                        <!-- 个人简介融合 -->
                        <div class="bg-black/30 p-6 rounded-xl border border-white/10 backdrop-blur-sm">
                            <div class="flex items-center gap-4 mb-2">
                                <div class="w-10 h-10 rounded-full bg-gradient-to-tr from-cyan-500 to-blue-600 flex items-center justify-center text-white font-bold text-lg">Me</div>
                                <h3 class="text-lg font-semibold text-cyan-200" data-lang-key="home.intro_title">舰长简介</h3>
                            </div>
                            <p class="text-gray-300 text-sm leading-relaxed" data-lang-key="home.intro_content">
                                <!-- 内容将由 JS 填充 -->
                            </p>
                        </div>
                    </div>
                    
                    <!-- 右侧装饰性 3D 元素示意 -->
                    <div class="hidden md:block w-64 h-64 relative animate-pulse">
                        <svg class="w-full h-full text-cyan-500/20" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/>
                        </svg>
                    </div>
                </div>
            </div>
            
            <!-- 学科入口 -->
            <h2 class="text-3xl font-bold mb-8 text-center text-white" data-lang-key="home.subjects_title">选择探索象限</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- 数学 -->
                <div class="subject-card group cursor-pointer" onclick="window.location.hash='subjects'; showSubjectTab('math')">
                    <div class="bg-blue-500/20 p-4 rounded-full mb-4 group-hover:bg-blue-500/40 transition-colors">
                        <svg class="w-10 h-10 text-blue-300" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 7h6m0 10v-3m-3 3h.01M9 17h.01M9 14h.01M12 14h.01M15 14h.01M12 17h.01M15 17h.01M9 10h.01M12 10h.01M15 10h.01M3 4a1 1 0 011-1h16a1 1 0 011 1v10a1 1 0 01-1 1H4a1 1 0 01-1-1V4z" /></svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-2 text-white" data-lang-key="subject.math">数学</h3>
                    <p class="text-gray-400 text-sm" data-lang-key="subject.math_desc">逻辑与数字的星图。</p>
                </div>
                <!-- 物理 -->
                <div class="subject-card group cursor-pointer" onclick="window.location.hash='subjects'; showSubjectTab('physics')">
                    <div class="bg-purple-500/20 p-4 rounded-full mb-4 group-hover:bg-purple-500/40 transition-colors">
                        <svg class="w-10 h-10 text-purple-300" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" /></svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-2 text-white" data-lang-key="subject.physics">物理</h3>
                    <p class="text-gray-400 text-sm" data-lang-key="subject.physics_desc">宇宙法则的引擎。</p>
                </div>
                <!-- 化学 -->
                <div class="subject-card group cursor-pointer" onclick="window.location.hash='subjects'; showSubjectTab('chemistry')">
                    <div class="bg-green-500/20 p-4 rounded-full mb-4 group-hover:bg-green-500/40 transition-colors">
                        <svg class="w-10 h-10 text-green-300" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.965l-2.287 2.287-.51.51a2 2 0 01-2.828 0l-2.287-2.287a2 2 0 010-2.828l.51-.51L9.5 7.71a6 6 0 00.965-3.86l-.477-2.387a2 2 0 00-.547-1.022A2 2 0 007.954 0H6.046a2 2 0 00-1.903 1.022 2 2 0 00-.547 1.022l.477 2.387a6 6 0 003.86.965l2.287 2.287.51.51a2 2 0 012.828 0l2.287 2.287a2 2 0 010 2.828l-.51.51-2.287 2.287a6 6 0 00-.965 3.86l.477 2.387a2 2 0 00.547 1.022A2 2 0 0016.046 24h1.908a2 2 0 001.903-1.022 2 2 0 00.547-1.022l-.477-2.387a6 6 0 00-3.86-.965l-2.287-2.287-.51-.51a2 2 0 01-2.828 0l-2.287-2.287a2 2 0 010-2.828l.51-.51 2.287-2.287a6 6 0 003.86-.965l2.387.477a2 2 0 001.022.547A2 2 0 0021.954 16.5H20.046a2 2 0 00-1.903-1.022 2 2 0 00-1.022.547z" /></svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-2 text-white" data-lang-key="subject.chemistry">化学</h3>
                    <p class="text-gray-400 text-sm" data-lang-key="subject.chemistry_desc">物质变化的炼金术。</p>
                </div>
                <!-- 生物 -->
                <div class="subject-card group cursor-pointer" onclick="window.location.hash='subjects'; showSubjectTab('biology')">
                    <div class="bg-rose-500/20 p-4 rounded-full mb-4 group-hover:bg-rose-500/40 transition-colors">
                        <svg class="w-10 h-10 text-rose-300" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" /><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" /></svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-2 text-white" data-lang-key="subject.biology">生物</h3>
                    <p class="text-gray-400 text-sm" data-lang-key="subject.biology_desc">生命螺旋的密码。</p>
                </div>
            </div>
        </section>

        <!-- 学科详情 (Subjects) -->
        <section id="subjects" class="page-section">
            <h2 class="text-3xl font-bold mb-6 text-transparent bg-clip-text bg-gradient-to-r from-cyan-300 to-purple-300" data-lang-key="subjects.title">学科深度探索</h2>
            <p class="text-lg text-gray-300 mb-8" data-lang-key="subjects.desc">点击下方按钮切换频道，深入知识黑洞：</p>
            
            <!-- 学科导航 (Tabs) -->
            <div class="flex flex-wrap gap-3 mb-8">
                <button data-subject-tab="math" class="subject-tab-btn px-6 py-2 rounded-full font-medium border border-blue-500/30 text-blue-300 hover:bg-blue-500/20 transition-all">数学</button>
                <button data-subject-tab="physics" class="subject-tab-btn px-6 py-2 rounded-full font-medium border border-purple-500/30 text-purple-300 hover:bg-purple-500/20 transition-all">物理</button>
                <button data-subject-tab="chemistry" class="subject-tab-btn px-6 py-2 rounded-full font-medium border border-green-500/30 text-green-300 hover:bg-green-500/20 transition-all">化学</button>
                <button data-subject-tab="biology" class="subject-tab-btn px-6 py-2 rounded-full font-medium border border-rose-500/30 text-rose-300 hover:bg-rose-500/20 transition-all">生物</button>
            </div>
            
            <!-- 学科内容容器 (Glassmorphism) -->
            <div class="glass-card p-8 rounded-xl min-h-[300px] relative overflow-hidden">
                <!-- 装饰背景光 -->
                <div class="absolute -top-24 -right-24 w-64 h-64 bg-blue-500/10 rounded-full blur-3xl"></div>

                <!-- 数学内容 -->
                <div id="subject-content-math" class="subject-content active relative z-10">
                    <h3 class="text-2xl font-semibold mb-4 text-blue-300" data-lang-key="subject.math">数学 (Mathematics)</h3>
                    <p class="text-gray-300 mb-6 leading-relaxed" data-lang-key="subjects.math_detail">数学是科学的语言。本板块包含函数、微积分、线性代数、概率论等核心概念的笔记和练习。</p>
                    
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <!-- 微积分 -->
                        <div class="bg-blue-900/20 rounded-lg p-4 border border-blue-500/10">
                            <h4 class="flex items-center text-lg font-semibold mb-3 text-white">
                                <span class="w-2 h-2 bg-blue-400 rounded-full mr-3"></span>
                                <span data-lang-key="subjects.math_t1">微积分 (Calculus)</span>
                            </h4>
                            <ul class="sub-topic-list">
                                <li class="sub-topic-item">
                                    <span data-lang-key="math.t1.s1">极限与连续 (Limits)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="math.t1.s2">导数应用 (Derivatives)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="math.t1.s3">定积分与不定积分 (Integrals)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                            </ul>
                        </div>

                        <!-- 线性代数 -->
                        <div class="bg-blue-900/20 rounded-lg p-4 border border-blue-500/10">
                            <h4 class="flex items-center text-lg font-semibold mb-3 text-white">
                                <span class="w-2 h-2 bg-blue-400 rounded-full mr-3"></span>
                                <span data-lang-key="subjects.math_t2">线性代数 (Linear Algebra)</span>
                            </h4>
                            <ul class="sub-topic-list">
                                <li class="sub-topic-item">
                                    <span data-lang-key="math.t2.s1">矩阵运算 (Matrices)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="math.t2.s2">向量空间 (Vector Spaces)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="math.t2.s3">特征值与特征向量 (Eigenvalues)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                            </ul>
                        </div>

                         <!-- 概率统计 -->
                         <div class="bg-blue-900/20 rounded-lg p-4 border border-blue-500/10">
                            <h4 class="flex items-center text-lg font-semibold mb-3 text-white">
                                <span class="w-2 h-2 bg-blue-400 rounded-full mr-3"></span>
                                <span data-lang-key="subjects.math_t3">概率与统计 (Probability)</span>
                            </h4>
                            <ul class="sub-topic-list">
                                <li class="sub-topic-item">
                                    <span data-lang-key="math.t3.s1">概率分布 (Distributions)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="math.t3.s2">假设检验 (Hypothesis Testing)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="math.t3.s3">回归分析 (Regression)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>

                <!-- 物理内容 -->
                <div id="subject-content-physics" class="subject-content hidden relative z-10">
                    <h3 class="text-2xl font-semibold mb-4 text-purple-300" data-lang-key="subject.physics">物理 (Physics)</h3>
                    <p class="text-gray-300 mb-6 leading-relaxed" data-lang-key="subjects.physics_detail">物理学探索宇宙的基本原理。这里有关于经典力学、电磁学、热力学和现代物理学的学习记录。</p>
                    
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <!-- 牛顿力学 -->
                        <div class="bg-purple-900/20 rounded-lg p-4 border border-purple-500/10">
                            <h4 class="flex items-center text-lg font-semibold mb-3 text-white">
                                <span class="w-2 h-2 bg-purple-400 rounded-full mr-3"></span>
                                <span data-lang-key="subjects.physics_t1">牛顿力学 (Newtonian Mechanics)</span>
                            </h4>
                            <ul class="sub-topic-list">
                                <li class="sub-topic-item">
                                    <span data-lang-key="phy.t1.s1">运动学 (Kinematics)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="phy.t1.s2">牛顿定律 (Newton's Laws)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="phy.t1.s3">能量守恒 (Energy Conservation)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                            </ul>
                        </div>

                        <!-- 电磁学 -->
                        <div class="bg-purple-900/20 rounded-lg p-4 border border-purple-500/10">
                            <h4 class="flex items-center text-lg font-semibold mb-3 text-white">
                                <span class="w-2 h-2 bg-purple-400 rounded-full mr-3"></span>
                                <span data-lang-key="subjects.physics_t2">电磁学 (Electromagnetism)</span>
                            </h4>
                            <ul class="sub-topic-list">
                                <li class="sub-topic-item">
                                    <span data-lang-key="phy.t2.s1">静电场 (Electrostatics)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="phy.t2.s2">磁场与感应 (Magnetism)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="phy.t2.s3">麦克斯韦方程 (Maxwell Eqs)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                            </ul>
                        </div>
                        
                        <!-- 相对论 -->
                        <div class="bg-purple-900/20 rounded-lg p-4 border border-purple-500/10">
                            <h4 class="flex items-center text-lg font-semibold mb-3 text-white">
                                <span class="w-2 h-2 bg-purple-400 rounded-full mr-3"></span>
                                <span data-lang-key="subjects.physics_t3">相对论 (Relativity)</span>
                            </h4>
                            <ul class="sub-topic-list">
                                <li class="sub-topic-item">
                                    <span data-lang-key="phy.t3.s1">狭义相对论 (Special Relativity)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="phy.t3.s2">广义相对论 (General Relativity)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="phy.t3.s3">黑洞物理 (Black Holes)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>

                <!-- 化学内容 -->
                <div id="subject-content-chemistry" class="subject-content hidden relative z-10">
                    <h3 class="text-2xl font-semibold mb-4 text-green-300" data-lang-key="subject.chemistry">化学 (Chemistry)</h3>
                    <p class="text-gray-300 mb-6 leading-relaxed" data-lang-key="subjects.chemistry_detail">化学是研究物质及其变化的中心科学。内容涵盖原子结构、化学键、热化学和有机化学。</p>
                    
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <!-- 有机化学 -->
                        <div class="bg-green-900/20 rounded-lg p-4 border border-green-500/10">
                            <h4 class="flex items-center text-lg font-semibold mb-3 text-white">
                                <span class="w-2 h-2 bg-green-400 rounded-full mr-3"></span>
                                <span data-lang-key="subjects.chem_t1">有机化学 (Organic Chemistry)</span>
                            </h4>
                            <ul class="sub-topic-list">
                                <li class="sub-topic-item">
                                    <span data-lang-key="chem.t1.s1">烃类与官能团 (Hydrocarbons)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="chem.t1.s2">反应机理 (Reaction Mechanisms)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="chem.t1.s3">立体化学 (Stereochemistry)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                            </ul>
                        </div>

                        <!-- 动力学 -->
                        <div class="bg-green-900/20 rounded-lg p-4 border border-green-500/10">
                            <h4 class="flex items-center text-lg font-semibold mb-3 text-white">
                                <span class="w-2 h-2 bg-green-400 rounded-full mr-3"></span>
                                <span data-lang-key="subjects.chem_t2">化学反应动力学 (Kinetics)</span>
                            </h4>
                            <ul class="sub-topic-list">
                                <li class="sub-topic-item">
                                    <span data-lang-key="chem.t2.s1">速率方程 (Rate Laws)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="chem.t2.s2">催化剂作用 (Catalysis)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="chem.t2.s3">化学平衡 (Equilibrium)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                            </ul>
                        </div>
                        
                        <!-- 周期表 -->
                        <div class="bg-green-900/20 rounded-lg p-4 border border-green-500/10">
                            <h4 class="flex items-center text-lg font-semibold mb-3 text-white">
                                <span class="w-2 h-2 bg-green-400 rounded-full mr-3"></span>
                                <span data-lang-key="subjects.chem_t3">元素周期表 (Periodic Table)</span>
                            </h4>
                            <ul class="sub-topic-list">
                                <li class="sub-topic-item">
                                    <span data-lang-key="chem.t3.s1">原子结构 (Atomic Structure)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="chem.t3.s2">周期律 (Periodic Trends)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="chem.t3.s3">过渡金属 (Transition Metals)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>

                <!-- 生物内容 -->
                <div id="subject-content-biology" class="subject-content hidden relative z-10">
                    <h3 class="text-2xl font-semibold mb-4 text-rose-300" data-lang-key="subject.biology">生物 (Biology)</h3>
                    <p class="text-gray-300 mb-6 leading-relaxed" data-lang-key="subjects.biology_detail">生物学探索生命的奇迹。本部分包括细胞生物学、遗传学、进化论和生态学的笔记。</p>
                    
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <!-- 遗传学 -->
                        <div class="bg-rose-900/20 rounded-lg p-4 border border-rose-500/10">
                            <h4 class="flex items-center text-lg font-semibold mb-3 text-white">
                                <span class="w-2 h-2 bg-rose-400 rounded-full mr-3"></span>
                                <span data-lang-key="subjects.bio_t1">遗传学 (Genetics)</span>
                            </h4>
                            <ul class="sub-topic-list">
                                <li class="sub-topic-item">
                                    <span data-lang-key="bio.t1.s1">孟德尔定律 (Mendelian)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="bio.t1.s2">DNA复制 (DNA Replication)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="bio.t1.s3">基因工程 (Gene Engineering)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                            </ul>
                        </div>

                        <!-- 细胞生物学 -->
                        <div class="bg-rose-900/20 rounded-lg p-4 border border-rose-500/10">
                            <h4 class="flex items-center text-lg font-semibold mb-3 text-white">
                                <span class="w-2 h-2 bg-rose-400 rounded-full mr-3"></span>
                                <span data-lang-key="subjects.bio_t2">细胞生物学 (Cell Biology)</span>
                            </h4>
                            <ul class="sub-topic-list">
                                <li class="sub-topic-item">
                                    <span data-lang-key="bio.t2.s1">细胞器功能 (Organelles)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="bio.t2.s2">膜运输 (Membrane Transport)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="bio.t2.s3">信号转导 (Signal Transduction)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                            </ul>
                        </div>
                        
                        <!-- 进化论 -->
                        <div class="bg-rose-900/20 rounded-lg p-4 border border-rose-500/10">
                            <h4 class="flex items-center text-lg font-semibold mb-3 text-white">
                                <span class="w-2 h-2 bg-rose-400 rounded-full mr-3"></span>
                                <span data-lang-key="subjects.bio_t3">进化论 (Evolution)</span>
                            </h4>
                            <ul class="sub-topic-list">
                                <li class="sub-topic-item">
                                    <span data-lang-key="bio.t3.s1">自然选择 (Natural Selection)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="bio.t3.s2">物种形成 (Speciation)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                                <li class="sub-topic-item">
                                    <span data-lang-key="bio.t3.s3">化石证据 (Fossil Records)</span>
                                    <a href="#" class="file-link-placeholder" title="Add File Link">[📄 资料]</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>

            <!-- ✨ AI 概念解析功能 (Dark Theme) ✨ -->
            <div class="mt-12 glass-card p-6 sm:p-8 rounded-xl border border-cyan-500/30">
                <h3 class="text-2xl font-bold mb-4 flex items-center text-white">
                    <span class="text-cyan-400 mr-3 animate-pulse">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M13 10V3L4 14h7v7l9-11h-7z" />
                        </svg>
                    </span>
                    <span data-lang-key="ai.title">AI 量子解析</span>
                </h3>
                <p class="text-gray-400 mb-5" data-lang-key="ai.desc">
                    对某个理科概念感到困惑吗？接入 AI 神经网络获取即时解答！
                </p>
                <div class="flex flex-col sm:flex-row gap-3 mb-4">
                    <input id="ai-prompt" type="text" class="flex-grow p-4 bg-slate-900/80 border border-slate-700 rounded-lg text-white placeholder-gray-500 focus:ring-2 focus:ring-cyan-500 focus:border-transparent outline-none transition-all" data-lang-key="ai.placeholder" placeholder="输入概念 (如：量子纠缠, 熵增定律)">
                    <button id="ai-submit-btn" class="bg-cyan-600 hover:bg-cyan-500 text-white font-bold py-3 px-8 rounded-lg shadow-[0_0_15px_rgba(8,145,178,0.5)] hover:shadow-[0_0_25px_rgba(34,211,238,0.6)] transition-all duration-300 flex items-center justify-center disabled:opacity-50 disabled:cursor-not-allowed">
                        <span class="mr-2">✨</span>
                        <span data-lang-key="ai.button">启动解析</span>
                    </button>
                </div>
                <!-- 结果区 -->
                <div id="ai-result-container" class="mt-4 p-6 bg-slate-900/60 rounded-lg border border-slate-700 min-h-[100px]" style="display: none;">
                    <!-- 加载中 -->
                    <div id="ai-loading" class="text-center py-6" style="display: none;">
                         <svg class="animate-spin h-8 w-8 text-cyan-500 mx-auto" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
                            <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
                            <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
                        </svg>
                        <p class="mt-3 text-cyan-400 tracking-widest text-sm uppercase" data-lang-key="ai.loading">正在建立量子连接...</p>
                    </div>
                    <!-- 结果 -->
                    <div id="ai-result-text" class="text-gray-200 space-y-3 leading-relaxed text-base"></div>
                    <!-- 错误信息 -->
                    <div id="ai-error" class="text-rose-400 font-medium" style="display: none;"></div>
                </div>
            </div>

        </section>

        <!-- 学习资源 (Resources) - 更新为可滚动的面板 -->
        <section id="resources" class="page-section glass-card p-8 rounded-xl">
            <h2 class="text-3xl font-bold mb-6 text-white" data-lang-key="resources.title">星际资源库</h2>
            <p class="text-lg text-gray-300 mb-8" data-lang-key="resources.desc">精选的高质量学习信标，指引你的探索之路。</p>
            
            <!-- 滚动容器 -->
            <div class="resource-scroll-area custom-scrollbar">
                <div id="resource-grid" class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <!-- 资源项将由 JS 动态生成 -->
                </div>
            </div>
        </section>

    </main>

    <!-- 页脚 -->
    <footer class="text-center p-8 mt-12 glass-nav">
        <p class="text-gray-500 text-sm" data-lang-key="footer.text">&copy; 2025 Quantum Learning Hub. All rights reserved.</p>
    </footer>

    <!-- JavaScript 脚本 -->
    <script>
        // 资源数据
        const resourceData = [
            // --- 已有经典 ---
            { title: "Khan Academy", desc: "Comprehensive K-12 science & math.", desc_cn: "全学科覆盖的免费知识宝库。", type: "web", link: "https://www.khanacademy.org/" },
            { title: "3Blue1Brown", desc: "Visualizing math beauty.", desc_cn: "用唯美的可视化动画展示数学之美。", type: "web", link: "https://www.youtube.com/c/3blue1brown" },
            { title: "WolframAlpha", desc: "Computational intelligence.", desc_cn: "强大的计算知识引擎，科学家的外脑。", type: "web", link: "https://www.wolframalpha.com/" },
            { title: "PhET Simulations", desc: "Interactive science sims.", desc_cn: "直观的物理与化学沙盒模拟。", type: "web", link: "https://phet.colorado.edu/" },
            
            // --- 顶级期刊/新闻 ---
            { title: "Nature", desc: "Leading international science journal.", desc_cn: "国际顶级科学期刊。", type: "web", link: "https://www.nature.com/" },
            { title: "Science Magazine", desc: "Breaking science news.", desc_cn: "前沿科学新闻与研究。", type: "web", link: "https://www.science.org/" },
            { title: "Scientific American", desc: "Science for everyone.", desc_cn: "科普界的常青树。", type: "web", link: "https://www.scientificamerican.com/" },
            { title: "NASA", desc: "Space exploration updates.", desc_cn: "宇宙探索的最新前沿。", type: "web", link: "https://www.nasa.gov/" },
            { title: "National Geographic", desc: "Earth & environment.", desc_cn: "地理与环境的视觉盛宴。", type: "web", link: "https://www.nationalgeographic.com/" },
            
            // --- 学习平台/课程 ---
            { title: "MIT OpenCourseWare", desc: "Free MIT course materials.", desc_cn: "麻省理工学院开放课程。", type: "web", link: "https://ocw.mit.edu/" },
            { title: "Coursera", desc: "Degrees from top unis.", desc_cn: "来自顶尖大学的在线课程。", type: "web", link: "https://www.coursera.org/" },
            { title: "edX", desc: "Courses from Harvard & MIT.", desc_cn: "哈佛与MIT联手的课程平台。", type: "web", link: "https://www.edx.org/" },
            { title: "Stanford Online", desc: "Stanford learning.", desc_cn: "斯坦福大学在线资源。", type: "web", link: "https://online.stanford.edu/" },
            { title: "Harvard Online", desc: "Harvard courses.", desc_cn: "哈佛大学在线课程。", type: "web", link: "https://pll.harvard.edu/" },
            
            // --- 核心知识 PDF 下载 (模拟链接) ---
            { title: "Calculus Cheat Sheet", desc: "Derivatives & Integrals.", desc_cn: "微积分速查表 (导数与积分)。", type: "pdf", link: "#" },
            { title: "Physics Constants", desc: "Fundamental constants.", desc_cn: "物理常数表 (光速, 普朗克常数)。", type: "pdf", link: "#" },
            { title: "Periodic Table HD", desc: "High-res printable.", desc_cn: "高清元素周期表。", type: "pdf", link: "#" },
            { title: "Amino Acids Chart", desc: "Structures & properties.", desc_cn: "氨基酸结构与性质表。", type: "pdf", link: "#" },
            { title: "Standard Model", desc: "Fundamental particles.", desc_cn: "粒子物理标准模型图。", type: "pdf", link: "#" },
            { title: "Trig Identities", desc: "Sin, Cos, Tan rules.", desc_cn: "三角函数恒等式大全。", type: "pdf", link: "#" },
            { title: "Organic Reactions", desc: "Reaction map.", desc_cn: "有机化学反应路线图。", type: "pdf", link: "#" },
            { title: "Maxwell's Equations", desc: "Electromagnetism core.", desc_cn: "麦克斯韦方程组详解。", type: "pdf", link: "#" },
            { title: "Metabolic Pathways", desc: "Cellular respiration.", desc_cn: "细胞代谢通路图。", type: "pdf", link: "#" },
            { title: "SI Units", desc: "International system.", desc_cn: "国际单位制换算表。", type: "pdf", link: "#" },

            // --- 实用工具 ---
            { title: "Desmos", desc: "Graphing calculator.", desc_cn: "超好用的在线绘图计算器。", type: "web", link: "https://www.desmos.com/" },
            { title: "GeoGebra", desc: "Dynamic mathematics.", desc_cn: "动态几何与代数工具。", type: "web", link: "https://www.geogebra.org/" },
            { title: "Ptable", desc: "Dynamic periodic table.", desc_cn: "动态交互式元素周期表。", type: "web", link: "https://ptable.com/" },
            { title: "MolView", desc: "Open source molecule viewer.", desc_cn: "开源分子结构查看器。", type: "web", link: "https://molview.org/" },
            { title: "Overleaf", desc: "Online LaTeX editor.", desc_cn: "在线 LaTeX 论文编辑器。", type: "web", link: "https://www.overleaf.com/" },
            
            // --- 学术搜索/数据库 ---
            { title: "arXiv", desc: "Open access e-prints.", desc_cn: "物理与数学预印本库。", type: "web", link: "https://arxiv.org/" },
            { title: "PubMed", desc: "Biomedical literature.", desc_cn: "生物医学文献数据库。", type: "web", link: "https://pubmed.ncbi.nlm.nih.gov/" },
            { title: "Google Scholar", desc: "Scholarly search.", desc_cn: "谷歌学术搜索。", type: "web", link: "https://scholar.google.com/" },
            { title: "MathWorld", desc: "Math encyclopedia.", desc_cn: "Wolfram 数学百科全书。", type: "web", link: "https://mathworld.wolfram.com/" },
            { title: "HyperPhysics", desc: "Physics concepts map.", desc_cn: "物理概念导图百科。", type: "web", link: "http://hyperphysics.phy-astr.gsu.edu/hbase/hframe.html" },
            
            // --- 天文与模拟 ---
            { title: "Stellarium", desc: "Virtual planetarium.", desc_cn: "虚拟天文馆星图。", type: "web", link: "https://stellarium-web.org/" },
            { title: "SpaceX", desc: "Future of space.", desc_cn: "SpaceX 发射与星舰动态。", type: "web", link: "https://www.spacex.com/" },
            { title: "CERN", desc: "Particle physics.", desc_cn: "欧洲核子研究中心。", type: "web", link: "https://home.cern/" },
            { title: "Algodoo", desc: "2D physics sandbox.", desc_cn: "2D 物理沙盒模拟器。", type: "web", link: "http://www.algodoo.com/" },
            { title: "Hubble Site", desc: "Hubble images.", desc_cn: "哈勃望远镜影像库。", type: "web", link: "https://hubblesite.org/" },
            
            // --- 更多 PDF 补充 ---
            { title: "Linear Algebra Map", desc: "Concept connections.", desc_cn: "线性代数概念图谱。", type: "pdf", link: "#" },
            { title: "Genetics Glossary", desc: "Key terms.", desc_cn: "遗传学术语表。", type: "pdf", link: "#" },
            { title: "Thermodynamics", desc: "Laws & formulas.", desc_cn: "热力学定律速查。", type: "pdf", link: "#" },
            { title: "Quantum Intro", desc: "Basic concepts.", desc_cn: "量子力学入门手册。", type: "pdf", link: "#" },
            { title: "Cell Structure", desc: "Diagrams.", desc_cn: "细胞结构精细图解。", type: "pdf", link: "#" },
            { title: "Lab Safety", desc: "Guidelines.", desc_cn: "实验室安全指南。", type: "pdf", link: "#" }
        ];

        // 语言翻译数据
        const translations = {
            en: {
                "head.title": "Quantum Science Hub",
                "nav.title": "Quantum Learning Hub",
                "nav.home": "Bridge",
                "nav.subjects": "Exploration",
                "nav.resources": "Resources",
                "home.title": "Launch Your Science Universe",
                "home.subtitle": "Explore the cosmos of logic, laws, matter, and life.",
                "home.subjects_title": "Choose Your Sector",
                "home.intro_title": "Captain's Log",
                "home.intro_content": "Welcome aboard! I am the pilot of this knowledge starship, Jiasheng Fu Felix. Passionate about decoding the universe's equations—from the infinite mysteries of calculus to the microscopic dance of chemical bonds. No rote memorization here, only the endless pursuit of truth. Let's warp into the unknown!",
                "subject.math": "Mathematics",
                "subject.math_desc": "Star charts of logic & numbers.",
                "subject.physics": "Physics",
                "subject.physics_desc": "Engines of universal laws.",
                "subject.chemistry": "Chemistry",
                "subject.chemistry_desc": "Alchemy of matter.",
                "subject.biology": "Biology",
                "subject.biology_desc": "Code of life spirals.",
                "subjects.title": "Deep Space Exploration",
                "subjects.desc": "Select a frequency channel to dive into the knowledge black hole:",
                "subjects.topics": "Core Sectors:",
                "subjects.math_detail": "Mathematics is the language of the cosmos. Covering calculus, linear algebra, and probability theory.",
                "subjects.math_t1": "Calculus",
                "subjects.math_t2": "Linear Algebra",
                "subjects.math_t3": "Probability & Statistics",
                "subjects.physics_detail": "Uncovering the fundamental principles of reality. From Newtonian mechanics to Relativity.",
                "subjects.physics_t1": "Newtonian Mechanics",
                "subjects.physics_t2": "Electromagnetism",
                "subjects.physics_t3": "Relativity",
                "subjects.chemistry_detail": "The central science of matter and change. Atomic structures and organic synthesis.",
                "subjects.chem_t1": "Organic Chemistry",
                "subjects.chem_t2": "Kinetics",
                "subjects.chem_t3": "Periodic Table",
                "subjects.biology_detail": "Exploring the miracle of life. From DNA helices to ecosystems.",
                "subjects.bio_t1": "Genetics & DNA",
                "subjects.bio_t2": "Cell Biology",
                "subjects.bio_t3": "Evolution",
                "resources.title": "Galactic Library",
                "resources.desc": "High-quality beacons to guide your exploration.",
                "resources.link": "Open Portal",
                "resources.pdf_link": "Download Data",
                "ai.title": "AI Quantum Analysis",
                "ai.desc": "Confused? Connect to the neural network for instant answers.",
                "ai.placeholder": "Enter concept (e.g., Quantum Entanglement)",
                "ai.button": "Analyze",
                "ai.loading": "Establishing Quantum Link...",
                "ai.error": "Signal lost. Please retry.",
                "ai.general_science": "General Science",
                "footer.text": "© 2025 Quantum Learning Hub. All rights reserved.",
                // New Translations for Subtopics
                "math.t1.s1": "Limits & Continuity",
                "math.t1.s2": "Applications of Derivatives",
                "math.t1.s3": "Integrals & Antiderivatives",
                "math.t2.s1": "Matrix Operations",
                "math.t2.s2": "Vector Spaces",
                "math.t2.s3": "Eigenvalues & Eigenvectors",
                "math.t3.s1": "Probability Distributions",
                "math.t3.s2": "Hypothesis Testing",
                "math.t3.s3": "Regression Analysis",
                "phy.t1.s1": "Kinematics",
                "phy.t1.s2": "Newton's Laws",
                "phy.t1.s3": "Energy Conservation",
                "phy.t2.s1": "Electrostatics",
                "phy.t2.s2": "Magnetism & Induction",
                "phy.t2.s3": "Maxwell's Equations",
                "phy.t3.s1": "Special Relativity",
                "phy.t3.s2": "General Relativity",
                "phy.t3.s3": "Black Hole Physics",
                "chem.t1.s1": "Hydrocarbons & Functional Groups",
                "chem.t1.s2": "Reaction Mechanisms",
                "chem.t1.s3": "Stereochemistry",
                "chem.t2.s1": "Rate Laws",
                "chem.t2.s2": "Catalysis",
                "chem.t2.s3": "Chemical Equilibrium",
                "chem.t3.s1": "Atomic Structure",
                "chem.t3.s2": "Periodic Trends",
                "chem.t3.s3": "Transition Metals",
                "bio.t1.s1": "Mendelian Genetics",
                "bio.t1.s2": "DNA Replication",
                "bio.t1.s3": "Genetic Engineering",
                "bio.t2.s1": "Organelle Function",
                "bio.t2.s2": "Membrane Transport",
                "bio.t2.s3": "Signal Transduction",
                "bio.t3.s1": "Natural Selection",
                "bio.t3.s2": "Speciation",
                "bio.t3.s3": "Fossil Records"
            },
            cn: {
                "head.title": "理科量子空间",
                "nav.title": "量子学习空间",
                "nav.home": "舰桥",
                "nav.subjects": "学科探索",
                "nav.resources": "星际资源",
                "home.title": "开启你的理科宇宙",
                "home.subtitle": "探索数学的逻辑星云，穿越物理的法则虫洞，解构化学的元素矩阵，见证生物的生命奇迹。",
                "home.subjects_title": "选择探索象限",
                "home.intro_title": "舰长简介",
                "home.intro_content": "欢迎登舰！我是这艘知识飞船的驾驶员——付嘉圣。我热衷于解开宇宙的方程，无论是微积分的无限奥秘，还是化学键的微观舞蹈。这里没有枯燥的死记硬背，只有对真理的无尽探索。让我们一起向着未知的知识疆域进发！",
                "subject.math": "数学",
                "subject.math_desc": "逻辑与数字的星图。",
                "subject.physics": "物理",
                "subject.physics_desc": "宇宙法则的引擎。",
                "subject.chemistry": "化学",
                "subject.chemistry_desc": "物质变化的炼金术。",
                "subject.biology": "生物",
                "subject.biology_desc": "生命螺旋的密码。",
                "subjects.title": "学科深度探索",
                "subjects.desc": "点击下方按钮切换频道，深入知识黑洞：",
                "subjects.topics": "重点星域：",
                "subjects.math_detail": "数学是科学的语言。本板块包含函数、微积分、线性代数、概率论等核心概念。",
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
                "resources.title": "星际资源库",
                "resources.desc": "精选的高质量学习信标，指引你的探索之路。",
                "resources.link": "开启传送门",
                "resources.pdf_link": "下载数据晶体",
                "ai.title": "AI 量子解析",
                "ai.desc": "对某个理科概念感到困惑吗？接入 AI 神经网络获取即时解答！",
                "ai.placeholder": "输入概念 (如：量子纠缠, 熵增定律)",
                "ai.button": "启动解析",
                "ai.loading": "正在建立量子连接...",
                "ai.error": "信号丢失，请重试。",
                "ai.general_science": "综合理科",
                "footer.text": "© 2025 Quantum Learning Hub. All rights reserved.",
                // Subtopic Translations
                "math.t1.s1": "极限与连续 (Limits)",
                "math.t1.s2": "导数应用 (Derivatives)",
                "math.t1.s3": "定积分与不定积分 (Integrals)",
                "math.t2.s1": "矩阵运算 (Matrices)",
                "math.t2.s2": "向量空间 (Vector Spaces)",
                "math.t2.s3": "特征值与特征向量 (Eigenvalues)",
                "math.t3.s1": "概率分布 (Distributions)",
                "math.t3.s2": "假设检验 (Hypothesis Testing)",
                "math.t3.s3": "回归分析 (Regression)",
                "phy.t1.s1": "运动学 (Kinematics)",
                "phy.t1.s2": "牛顿定律 (Newton's Laws)",
                "phy.t1.s3": "能量守恒 (Energy Conservation)",
                "phy.t2.s1": "静电场 (Electrostatics)",
                "phy.t2.s2": "磁场与感应 (Magnetism)",
                "phy.t2.s3": "麦克斯韦方程 (Maxwell Eqs)",
                "phy.t3.s1": "狭义相对论 (Special Relativity)",
                "phy.t3.s2": "广义相对论 (General Relativity)",
                "phy.t3.s3": "黑洞物理 (Black Holes)",
                "chem.t1.s1": "烃类与官能团 (Hydrocarbons)",
                "chem.t1.s2": "反应机理 (Reaction Mechanisms)",
                "chem.t1.s3": "立体化学 (Stereochemistry)",
                "chem.t2.s1": "速率方程 (Rate Laws)",
                "chem.t2.s2": "催化剂作用 (Catalysis)",
                "chem.t2.s3": "化学平衡 (Equilibrium)",
                "chem.t3.s1": "原子结构 (Atomic Structure)",
                "chem.t3.s2": "周期律 (Periodic Trends)",
                "chem.t3.s3": "过渡金属 (Transition Metals)",
                "bio.t1.s1": "孟德尔定律 (Mendelian)",
                "bio.t1.s2": "DNA复制 (DNA Replication)",
                "bio.t1.s3": "基因工程 (Gene Engineering)",
                "bio.t2.s1": "细胞器功能 (Organelles)",
                "bio.t2.s2": "膜运输 (Membrane Transport)",
                "bio.t2.s3": "信号转导 (Signal Transduction)",
                "bio.t3.s1": "自然选择 (Natural Selection)",
                "bio.t3.s2": "物种形成 (Speciation)",
                "bio.t3.s3": "化石证据 (Fossil Records)"
            }
        };

        let currentLang = 'cn';

        function setLanguage(lang) {
            currentLang = lang;
            document.documentElement.lang = lang;
            
            try { localStorage.setItem('preferredLang', lang); } catch (e) {}

            document.querySelectorAll('[data-lang-key]').forEach(el => {
                const key = el.getAttribute('data-lang-key');
                if (translations[lang] && translations[lang][key]) {
                    el.textContent = translations[lang][key];
                }
            });

            const langSwitcher = document.getElementById('lang-switcher');
            langSwitcher.textContent = lang === 'en' ? 'CN' : 'EN';

            const placeholderKey = 'ai.placeholder';
            const placeholderText = translations[lang] && translations[lang][placeholderKey] ? translations[lang][placeholderKey] : "Enter concept";
            document.getElementById('ai-prompt').setAttribute('placeholder', placeholderText);

             const loadingEl = document.getElementById('ai-loading');
             if (loadingEl.style.display !== 'none') {
                loadingEl.querySelector('p').textContent = translations[lang]['ai.loading'];
             }
             
             // Re-render resources to update language
             renderResources();
        }

        // 渲染资源列表
        function renderResources() {
            const container = document.getElementById('resource-grid');
            container.innerHTML = '';
            
            const linkTextKey = 'resources.link';
            const pdfTextKey = 'resources.pdf_link';
            const linkText = translations[currentLang][linkTextKey];
            const pdfText = translations[currentLang][pdfTextKey];

            resourceData.forEach(item => {
                const title = item.title; // Titles are English in JS data for simplicity, or could be bilingual
                const desc = currentLang === 'cn' && item.desc_cn ? item.desc_cn : item.desc;
                const isPdf = item.type === 'pdf';
                const actionText = isPdf ? pdfText : linkText;
                const actionColor = isPdf ? 'text-emerald-400 hover:text-emerald-300' : 'text-blue-400 hover:text-blue-300';
                const icon = isPdf ? '📄' : '🔗';

                const cardHTML = `
                    <div class="p-4 rounded-lg bg-slate-800/50 border border-slate-700 hover:bg-slate-800 transition-colors">
                        <div class="flex justify-between items-start">
                            <div>
                                <h3 class="text-lg font-semibold text-cyan-300 mb-1">${title}</h3>
                                <p class="text-gray-400 text-xs mb-3">${desc}</p>
                            </div>
                            <span class="text-lg opacity-50">${icon}</span>
                        </div>
                        <a href="${item.link}" target="_blank" class="${actionColor} text-sm flex items-center font-medium">
                            ${actionText}
                        </a>
                    </div>
                `;
                container.insertAdjacentHTML('beforeend', cardHTML);
            });
        }

        function showPage(pageId) {
            document.querySelectorAll('.page-section').forEach(section => {
                section.classList.remove('active');
            });
            
            const targetPage = document.getElementById(pageId);
            if (targetPage) {
                targetPage.classList.add('active');
            }

            document.querySelectorAll('.nav-link').forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('data-nav-link') === pageId) {
                    link.classList.add('active');
                }
            });

            document.getElementById('mobile-menu').classList.add('hidden');
        }

        function showSubjectTab(subjectId) {
            document.querySelectorAll('.subject-content').forEach(content => {
                content.classList.add('hidden');
            });

            const targetContent = document.getElementById(`subject-content-${subjectId}`);
            if (targetContent) {
                targetContent.classList.remove('hidden');
            }

            document.querySelectorAll('.subject-tab-btn').forEach(btn => {
                btn.classList.remove('bg-cyan-500/20', 'text-cyan-300', 'border-cyan-500/50', 'shadow-lg');
                btn.classList.add('border-white/10', 'text-gray-400');
                
                if (btn.getAttribute('data-subject-tab') === subjectId) {
                    // Active State for Dark Mode
                    btn.classList.remove('border-white/10', 'text-gray-400');
                    btn.classList.add('bg-cyan-500/20', 'text-cyan-300', 'border-cyan-500/50', 'shadow-lg');
                }
            });
        }

        function getActiveSubject() {
            const activeBtn = document.querySelector('.subject-tab-btn.bg-cyan-500\\/20'); // Escape slash for selector
            if (activeBtn) {
                const subjectId = activeBtn.getAttribute('data-subject-tab');
                const key = `subject.${subjectId}`;
                if (translations[currentLang] && translations[currentLang][key]) {
                    return translations[currentLang][key];
                }
            }
            return translations[currentLang]['ai.general_science'] || 'science';
        }

        // AI Function (Logic remains mostly same, style updated via HTML classes)
        async function handleAiSubmit() {
            const promptInput = document.getElementById('ai-prompt');
            const submitBtn = document.getElementById('ai-submit-btn');
            const resultContainer = document.getElementById('ai-result-container');
            const loadingEl = document.getElementById('ai-loading');
            const resultTextEl = document.getElementById('ai-result-text');
            const errorEl = document.getElementById('ai-error');

            const userQuery = promptInput.value.trim();
            if (!userQuery) { promptInput.focus(); return; }

            submitBtn.disabled = true;
            resultContainer.style.display = 'block';
            loadingEl.style.display = 'block';
            resultTextEl.innerHTML = '';
            errorEl.style.display = 'none';
            loadingEl.querySelector('p').textContent = translations[currentLang]['ai.loading'];

            try {
                const activeSubject = getActiveSubject();
                const responseLang = currentLang === 'cn' ? '中文' : 'English';
                const systemPrompt = `You are a futuristic science guide. Explain the concept clearly and concisely, suitable for a student exploring the universe of knowledge. Context: ${activeSubject}. Respond in ${responseLang} using Markdown.`;
                
                const apiKey = "AIzaSyArzbmAPfYzLpvxY7yQoT_pXvt88w46HDg"; // Keep empty
                const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`;

                const payload = {
                    contents: [{ parts: [{ text: userQuery }] }],
                    tools: [{ "google_search": {} }],
                    systemInstruction: { parts: [{ text: systemPrompt }] },
                };
                
                const MAX_RETRIES = 3;
                let response = null;
                for (let i = 0; i < MAX_RETRIES; i++) {
                    try {
                        response = await fetch(apiUrl, {
                            method: 'POST',
                            headers: { 'Content-Type': 'application/json' },
                            body: JSON.stringify(payload)
                        });
                        if (response.status !== 429 && response.ok) break;
                        if (response.status === 429 && i < MAX_RETRIES - 1) {
                            await new Promise(r => setTimeout(r, 1000 * Math.pow(2, i)));
                        } else if (!response.ok) throw new Error(response.statusText);
                    } catch (err) { if (i === MAX_RETRIES - 1) throw err; }
                }
                
                if (!response || !response.ok) throw new Error("Connection failed.");

                const result = await response.json();
                const candidate = result.candidates?.[0];

                if (candidate && candidate.content?.parts?.[0]?.text) {
                    const text = candidate.content.parts[0].text;
                    let formattedText = text
                        .replace(/\*\*(.*?)\*\*/g, '<strong>$1</strong>')
                        .replace(/\*(.*?)\*/g, '<em>$1</em>');
                    
                    const lines = formattedText.split('\n');
                    let htmlContent = [];
                    let inList = false;

                    lines.forEach(line => {
                        const trimmedLine = line.trim();
                        const isListItem = trimmedLine.startsWith('- ') || trimmedLine.startsWith('* ');
                        if (isListItem) {
                            if (!inList) { htmlContent.push('<ul>'); inList = true; }
                            htmlContent.push(`<li>${trimmedLine.substring(2).trim()}</li>`);
                        } else {
                            if (inList) { htmlContent.push('</ul>'); inList = false; }
                            if (trimmedLine !== '') htmlContent.push(`<p>${trimmedLine}</p>`);
                        }
                    });
                    if (inList) htmlContent.push('</ul>');
                    
                    resultTextEl.innerHTML = htmlContent.join('');
                } else { throw new Error("No data received."); }

            } catch (error) {
                console.error(error);
                errorEl.textContent = translations[currentLang]['ai.error'];
                errorEl.style.display = 'block';
            } finally {
                submitBtn.disabled = false;
                loadingEl.style.display = 'none';
            }
        }

        document.addEventListener('DOMContentLoaded', () => {
            const langSwitcher = document.getElementById('lang-switcher');
            const mobileMenuButton = document.getElementById('mobile-menu-button');
            const mobileMenu = document.getElementById('mobile-menu');
            const aiPromptInput = document.getElementById('ai-prompt');
            
            langSwitcher.addEventListener('click', () => setLanguage(currentLang === 'en' ? 'cn' : 'en'));
            
            let preferredLang = 'cn';
            try { preferredLang = localStorage.getItem('preferredLang') || 'cn'; } catch (e) {}
            setLanguage(preferredLang);

            mobileMenuButton.addEventListener('click', () => mobileMenu.classList.toggle('hidden'));

            document.querySelectorAll('.nav-link').forEach(link => {
                link.addEventListener('click', (e) => {
                    e.preventDefault();
                    const pageId = link.getAttribute('data-nav-link');
                    window.location.hash = pageId;
                    showPage(pageId);
                });
            });

            document.querySelectorAll('.subject-tab-btn').forEach(btn => {
                btn.addEventListener('click', () => {
                    const subjectId = btn.getAttribute('data-subject-tab');
                    showSubjectTab(subjectId);
                });
            });

            function handleHashChange() {
                const hash = window.location.hash.substring(1) || 'home';
                showPage(hash);
                if (['math', 'physics', 'chemistry', 'biology'].includes(hash)) {
                    showPage('subjects');
                    showSubjectTab(hash);
                }
            }
            window.addEventListener('hashchange', handleHashChange);
            handleHashChange();
            
            // Set default subject tab style
            showSubjectTab('math');

            document.getElementById('ai-submit-btn').addEventListener('click', handleAiSubmit);
            aiPromptInput.addEventListener('keydown', (e) => {
                if (e.key === 'Enter') {
                    e.preventDefault();
                    handleAiSubmit();
                }
            });
            
            // Initial render of resources
            renderResources();
        });
    </script>
</body>
</html>
