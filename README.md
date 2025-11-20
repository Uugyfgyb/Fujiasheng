欢迎大家上舰！
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>量子学习空间 | Quantum Learning Hub</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Deep Space Theme */
        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #0f0f3d, #000000);
            color: white;
            padding: 0;
            margin: 0;
            scroll-behavior: smooth;
        }

        /* Glassmorphism effect */
        .glass-card {
            backdrop-filter: blur(10px);
            background: rgba(255, 255, 255, 0.2);
            border-radius: 10px;
            padding: 20px;
            margin: 10px;
        }

        .glass-navbar {
            backdrop-filter: blur(15px);
            background: rgba(0, 0, 0, 0.4);
        }

        .glass-button {
            border: 2px solid #00b0d1;
            color: #00b0d1;
            border-radius: 30px;
            padding: 10px 30px;
            text-align: center;
            font-size: 1.2rem;
        }
    </style>
</head>

<body>
    <!-- Navigation Bar -->
    <nav class="glass-navbar fixed w-full z-10 p-4 flex justify-between items-center">
        <div class="text-2xl font-bold text-white">量子学习空间</div>
        <ul class="flex space-x-4">
            <li><a href="#home" class="text-white">首页</a></li>
            <li><a href="#subjects" class="text-white">学科深度探索</a></li>
            <li><a href="#resources" class="text-white">星际资源库</a></li>
            <li><a href="#ai-query" class="text-white">AI 量子解析</a></li>
        </ul>
    </nav>

    <!-- Home Section -->
    <section id="home" class="pt-16 text-center">
        <h1 class="text-5xl font-bold mb-4">量子学习空间</h1>
        <p class="text-xl">提升你的本科数理化知识，立即进入顶尖网课资源</p>
        <div class="flex justify-center space-x-8 mt-8">
            <div class="glass-card">
                <h2 class="text-2xl">数学</h2>
                <a href="#subjects" class="glass-button">进入数学</a>
            </div>
            <div class="glass-card">
                <h2 class="text-2xl">物理</h2>
                <a href="#subjects" class="glass-button">进入物理</a>
            </div>
            <div class="glass-card">
                <h2 class="text-2xl">化学</h2>
                <a href="#subjects" class="glass-button">进入化学</a>
            </div>
        </div>
    </section>

    <!-- Subjects Section -->
    <section id="subjects" class="py-20">
        <h2 class="text-4xl text-center mb-12">学科深度探索</h2>
        <div class="container mx-auto">
            <div class="flex justify-center space-x-8">
                <div class="glass-card">
                    <h3 class="text-xl">数学</h3>
                    <ul>
                        <li><a href="#calculus" class="glass-button">微积分与分析</a></li>
                        <li><a href="#algebra" class="glass-button">代数与几何</a></li>
                        <li><a href="#applied-math" class="glass-button">应用数学</a></li>
                    </ul>
                </div>
                <div class="glass-card">
                    <h3 class="text-xl">物理</h3>
                    <ul>
                        <li><a href="#quantum-physics" class="glass-button">量子力学</a></li>
                        <li><a href="#relativity" class="glass-button">相对论</a></li>
                        <li><a href="#electromagnetism" class="glass-button">电磁学</a></li>
                    </ul>
                </div>
                <div class="glass-card">
                    <h3 class="text-xl">化学</h3>
                    <ul>
                        <li><a href="#organic-chemistry" class="glass-button">有机化学</a></li>
                        <li><a href="#inorganic-chemistry" class="glass-button">无机化学</a></li>
                        <li><a href="#physical-chemistry" class="glass-button">物理化学</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- AI Query Section -->
    <section id="ai-query" class="py-20 bg-gray-800">
        <h2 class="text-4xl text-center mb-12 text-white">AI 量子解析</h2>
        <div class="text-center">
            <input type="text" id="ai-query-input" class="p-3 rounded" placeholder="输入概念查询...">
            <button onclick="queryAI()" class="glass-button mt-4">查询</button>
            <div id="ai-result" class="mt-6 text-white p-4"></div>
        </div>
    </section>

    <!-- Resources Section -->
    <section id="resources" class="py-20">
        <h2 class="text-4xl text-center mb-12">星际资源库</h2>
        <ul class="container mx-auto text-center">
            <li><a href="https://www.wolframalpha.com" class="text-blue-400">WolframAlpha</a></li>
            <li><a href="https://www.3blue1brown.com" class="text-blue-400">3Blue1Brown</a></li>
            <li><a href="https://phet.colorado.edu" class="text-blue-400">PhET Simulators</a></li>
        </ul>
    </section>

    <script>
        function queryAI() {
            const query = document.getElementById('ai-query-input').value;
            const result = document.getElementById('ai-result');
            if (query) {
                result.innerHTML = `<p>查询结果：关于 "${query}" 的知识点解析。</p>`;
            }
        }
    </script>
</body>

</html>

