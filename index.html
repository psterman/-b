<!DOCTYPE html>
<html lang="zh-CN" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CursorHelper 文档 - 提升您的 Cursor 编程效率</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        cursor: {
                            bg: '#0E0E0E',
                            sidebar: '#161616',
                            border: '#2C2C2C',
                            text: '#EAEAEA',
                            muted: '#888888',
                            accent: '#37996B', // Cursor Greenish accent
                            accent_hover: '#2E8059'
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'system-ui', '-apple-system', 'BlinkMacSystemFont', 'Segoe UI', 'Roboto', 'sans-serif'],
                        mono: ['JetBrains Mono', 'Fira Code', 'Consolas', 'monospace'],
                    },
                    animation: {
                        'pulse-slow': 'pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                    }
                }
            }
        }
    </script>
    <style>
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 6px;
            height: 6px;
        }
        ::-webkit-scrollbar-track {
            background: #161616;
        }
        ::-webkit-scrollbar-thumb {
            background: #333;
            border-radius: 3px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #444;
        }
        
        .glass-panel {
            background: rgba(22, 22, 22, 0.8);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }

        .kbd-key {
            display: inline-block;
            padding: 0.1em 0.4em;
            font-size: 0.85em;
            line-height: 1;
            color: #e2e8f0;
            background-color: #2d3748;
            border: 1px solid #4a5568;
            border-radius: 0.25rem;
            box-shadow: 0 1px 1px rgba(0,0,0,0.1);
            font-family: 'JetBrains Mono', monospace;
        }

        /* Demo Animation Styles */
        .demo-window {
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.5);
        }
        
        .code-line {
            transition: background-color 0.3s ease;
        }
        
        .flying-text {
            position: absolute;
            z-index: 50;
            background: #37996B;
            color: white;
            padding: 2px 6px;
            border-radius: 4px;
            font-family: monospace;
            font-size: 12px;
            pointer-events: none;
            box-shadow: 0 4px 6px rgba(0,0,0,0.3);
            white-space: nowrap;
        }

        .queue-item-enter {
            animation: queueEnter 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
        }

        @keyframes queueEnter {
            from { opacity: 0; transform: scale(0.8) translateY(10px); }
            to { opacity: 1; transform: scale(1) translateY(0); }
        }
        
        .cursor-caret {
            display: inline-block;
            width: 2px;
            height: 1.2em;
            background-color: #37996B;
            vertical-align: middle;
            animation: blink 1s step-end infinite;
        }
        
        @keyframes blink {
            50% { opacity: 0; }
        }

        /* Browser Tab Animations */
        .tab-enter {
            animation: tabPop 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
        }
        @keyframes tabPop {
            from { transform: translateY(100%) scale(0.9); opacity: 0; }
            to { transform: translateY(0) scale(1); opacity: 1; }
        }
        .engine-selected {
            background-color: rgba(55, 153, 107, 0.2) !important;
            border-color: #37996B !important;
            color: white !important;
        }
        .engine-check {
            display: inline-block;
            margin-right: 4px;
            color: #37996B;
        }

        /* Screenshot Animations */
        .crosshair-cursor {
            cursor: crosshair;
        }
    </style>
    <!-- Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
</head>
<body class="bg-cursor-bg text-cursor-text font-sans antialiased selection:bg-cursor-accent selection:text-white">

    <!-- Header -->
    <header class="fixed top-0 w-full z-50 border-b border-cursor-border glass-panel">
        <div class="max-w-7xl mx-auto px-4 h-14 flex items-center justify-between">
            <div class="flex items-center gap-2 font-bold text-xl tracking-tight">
                <i data-lucide="terminal" class="w-6 h-6 text-cursor-accent"></i>
                <span>CursorHelper</span>
            </div>
            <div class="flex items-center gap-6 text-sm font-medium">
                <a href="#download" class="text-cursor-muted hover:text-white transition-colors">版本 v2.1</a>
                <a href="https://github.com/your-repo" target="_blank" class="text-cursor-muted hover:text-white transition-colors flex items-center gap-1">
                    <i data-lucide="github" class="w-4 h-4"></i> GitHub
                </a>
            </div>
        </div>
    </header>

    <div class="flex max-w-7xl mx-auto pt-14 min-h-screen">
        
        <!-- Sidebar Navigation -->
        <aside class="w-64 hidden lg:block fixed h-[calc(100vh-3.5rem)] overflow-y-auto border-r border-cursor-border bg-cursor-bg py-8">
            <nav class="space-y-1 px-4 text-sm">
                <div class="pb-4">
                    <h3 class="font-semibold text-white mb-2 px-2">入门</h3>
                    <a href="#intro" class="block px-2 py-1.5 text-cursor-accent bg-cursor-accent/10 rounded-md">简介</a>
                    <a href="#quick-start" class="block px-2 py-1.5 text-cursor-muted hover:text-white transition-colors">快速开始</a>
                </div>
                
                <div class="pb-4">
                    <h3 class="font-semibold text-white mb-2 px-2">核心概念</h3>
                    <a href="#concept-capslock" class="block px-2 py-1.5 text-cursor-muted hover:text-white transition-colors">CapsLock+ 机制</a>
                    <a href="#concept-panel" class="block px-2 py-1.5 text-cursor-muted hover:text-white transition-colors">快捷面板</a>
                </div>

                <div class="pb-4">
                    <h3 class="font-semibold text-white mb-2 px-2">功能详解</h3>
                    <a href="#feat-ai" class="block px-2 py-1.5 text-cursor-muted hover:text-white transition-colors">AI 辅助 (E/R/O)</a>
                    <a href="#feat-clipboard" class="block px-2 py-1.5 text-cursor-muted hover:text-white transition-colors">连续复制 & 粘贴</a>
                    <a href="#feat-search" class="block px-2 py-1.5 text-cursor-muted hover:text-white transition-colors">多引擎聚合搜索</a>
                    <a href="#feat-utils" class="block px-2 py-1.5 text-cursor-muted hover:text-white transition-colors">实用工具 (截图/分割)</a>
                </div>

                <div class="pb-4">
                    <h3 class="font-semibold text-white mb-2 px-2">高级</h3>
                    <a href="#interface-settings" class="block px-2 py-1.5 text-cursor-muted hover:text-white transition-colors">配置与规则</a>
                    <a href="#troubleshooting" class="block px-2 py-1.5 text-cursor-muted hover:text-white transition-colors">常见问题</a>
                </div>
            </nav>
        </aside>

        <!-- Main Content -->
        <main class="flex-1 lg:pl-72 py-10 px-6 lg:px-12 max-w-4xl">
            
            <!-- Hero Section -->
            <section id="intro" class="mb-16">
                <h1 class="text-4xl font-bold mb-4 tracking-tight">CursorHelper 文档</h1>
                <p class="text-lg text-cursor-muted leading-relaxed mb-6">
                    专为 Cursor 编辑器打造的 AutoHotkey 效率增强脚本。通过 <kbd class="kbd-key">CapsLock</kbd> 键赋予您全新的交互方式，集成代码解释、重构、连续复制、多引擎搜索等强大功能。
                </p>
                <div class="flex gap-4">
                    <a href="#download" class="bg-white text-black px-5 py-2.5 rounded-full font-medium hover:bg-gray-200 transition-colors">下载脚本</a>
                    <a href="#quick-start" class="border border-cursor-border text-white px-5 py-2.5 rounded-full font-medium hover:bg-cursor-sidebar transition-colors">查看教程</a>
                </div>
            </section>

            <!-- Quick Start -->
            <section id="quick-start" class="mb-16 scroll-mt-20">
                <h2 class="text-2xl font-semibold mb-6 flex items-center gap-2">
                    <i data-lucide="zap" class="text-cursor-accent"></i> 快速开始
                </h2>
                
                <div class="space-y-6">
                    <div class="bg-cursor-sidebar border border-cursor-border rounded-lg p-6">
                        <h3 class="font-medium text-lg mb-2">1. 安装环境</h3>
                        <p class="text-cursor-muted text-sm mb-2">确保您已安装 AutoHotkey v2 版本。</p>
                        <div class="bg-black rounded p-3 font-mono text-xs text-gray-400">
                            下载地址: https://www.autohotkey.com/
                        </div>
                    </div>

                    <div class="bg-cursor-sidebar border border-cursor-border rounded-lg p-6">
                        <h3 class="font-medium text-lg mb-2">2. 运行脚本</h3>
                        <p class="text-cursor-muted text-sm mb-2">
                            右键点击 <code class="text-cursor-accent">CursorHelper.ahk</code>，选择“Run Script”。
                            <br><span class="text-yellow-500 text-xs">*脚本会自动尝试获取管理员权限以确保功能正常。</span>
                        </p>
                    </div>

                    <div class="bg-cursor-sidebar border border-cursor-border rounded-lg p-6">
                        <h3 class="font-medium text-lg mb-2">3. 基础操作</h3>
                        <ul class="list-disc list-inside text-cursor-muted text-sm space-y-1">
                            <li><strong>长按 CapsLock (0.5秒)：</strong> 弹出快捷操作面板。</li>
                            <li><strong>短按 CapsLock：</strong> 切换大小写（原功能不变）。</li>
                            <li><strong>在面板中按键：</strong> 触发对应功能（如 E 解释，C 复制）。</li>
                        </ul>
                    </div>
                </div>
            </section>

            <!-- Concepts -->
            <section id="concept-capslock" class="mb-16 scroll-mt-20">
                <h2 class="text-2xl font-semibold mb-6">CapsLock+ 核心机制</h2>
                <p class="text-cursor-muted mb-4">
                    CursorHelper 不会废弃您的 CapsLock 键，而是将其增强为一个<strong>功能修饰键 (Hyper Key)</strong>。
                </p>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div class="border border-cursor-border rounded-xl p-6 bg-gradient-to-br from-cursor-sidebar to-cursor-bg">
                        <div class="text-cursor-accent font-mono mb-2">短按 Click</div>
                        <h3 class="text-lg font-medium mb-2">切换大小写</h3>
                        <p class="text-sm text-cursor-muted">像往常一样快速点击 CapsLock，即可切换大小写状态。不影响日常打字。</p>
                    </div>
                    <div class="border border-cursor-border rounded-xl p-6 bg-gradient-to-br from-cursor-sidebar to-cursor-bg">
                        <div class="text-blue-400 font-mono mb-2">长按 Hold (>0.5s)</div>
                        <h3 class="text-lg font-medium mb-2">唤起快捷面板</h3>
                        <p class="text-sm text-cursor-muted">长按不放，屏幕中央弹出半透明快捷操作面板 (HUD)，此时按下对应字母键即可触发功能。</p>
                    </div>
                </div>
            </section>

            <!-- Quick Panel Map -->
            <section id="concept-panel" class="mb-16 scroll-mt-20">
                <h2 class="text-2xl font-semibold mb-6">快捷键映射</h2>
                <div class="overflow-x-auto">
                    <table class="w-full text-sm text-left text-cursor-muted">
                        <thead class="text-xs text-white uppercase bg-cursor-sidebar">
                            <tr>
                                <th scope="col" class="px-6 py-3 rounded-l-lg">快捷键 (面板打开时)</th>
                                <th scope="col" class="px-6 py-3">功能名称</th>
                                <th scope="col" class="px-6 py-3 rounded-r-lg">描述</th>
                            </tr>
                        </thead>
                        <tbody class="divide-y divide-cursor-border">
                            <tr class="bg-cursor-bg">
                                <td class="px-6 py-4 font-mono text-white">E</td>
                                <td class="px-6 py-4">解释代码 (Explain)</td>
                                <td class="px-6 py-4">AI 解释选中代码的核心逻辑。</td>
                            </tr>
                            <tr class="bg-cursor-sidebar/50">
                                <td class="px-6 py-4 font-mono text-white">R</td>
                                <td class="px-6 py-4">重构代码 (Refactor)</td>
                                <td class="px-6 py-4">AI 遵循规范重构代码，添加注释。</td>
                            </tr>
                            <tr class="bg-cursor-bg">
                                <td class="px-6 py-4 font-mono text-white">O</td>
                                <td class="px-6 py-4">优化代码 (Optimize)</td>
                                <td class="px-6 py-4">AI 分析性能瓶颈并给出优化方案。</td>
                            </tr>
                            <tr class="bg-cursor-sidebar/50">
                                <td class="px-6 py-4 font-mono text-white">C</td>
                                <td class="px-6 py-4">连续复制</td>
                                <td class="px-6 py-4">多次选中不同位置文本，连续按 <kbd class="kbd-key">C</kbd> 存入历史。</td>
                            </tr>
                            <tr class="bg-cursor-bg">
                                <td class="px-6 py-4 font-mono text-white">V</td>
                                <td class="px-6 py-4">合并粘贴</td>
                                <td class="px-6 py-4">将连续复制的内容合并后一次性粘贴。</td>
                            </tr>
                            <tr class="bg-cursor-sidebar/50">
                                <td class="px-6 py-4 font-mono text-white">X</td>
                                <td class="px-6 py-4">剪贴板管理</td>
                                <td class="px-6 py-4">打开可视化剪贴板历史管理器。</td>
                            </tr>
                            <tr class="bg-cursor-bg">
                                <td class="px-6 py-4 font-mono text-white">F</td>
                                <td class="px-6 py-4">聚合搜索</td>
                                <td class="px-6 py-4">输入关键词，同时打开多个搜索引擎 (DeepSeek/Google/Baidu)。</td>
                            </tr>
                            <tr class="bg-cursor-sidebar/50">
                                <td class="px-6 py-4 font-mono text-white">P</td>
                                <td class="px-6 py-4">区域截图</td>
                                <td class="px-6 py-4">截图并提供“粘贴到 Cursor”悬浮按钮。</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </section>

            <!-- Feature Details -->
            <section id="feat-ai" class="mb-16 scroll-mt-20">
                <h2 class="text-2xl font-semibold mb-6 flex items-center gap-2">
                    <i data-lucide="brain-circuit" class="text-blue-400"></i> AI 辅助编程
                </h2>
                <p class="text-cursor-muted mb-4">
                    无需手动打字提问，CursorHelper 预设了高效的 Prompt 模板。只需选中代码，唤起面板，一键直达。
                </p>
                <div class="bg-cursor-sidebar rounded-lg p-6 border border-cursor-border">
                    <h4 class="font-medium text-white mb-2">工作流程：</h4>
                    <ol class="list-decimal list-inside text-cursor-muted space-y-2 text-sm">
                        <li>在 Cursor 编辑器中选中一段代码。</li>
                        <li>长按 <kbd class="kbd-key">CapsLock</kbd> 直到面板出现。</li>
                        <li>按 <kbd class="kbd-key">E</kbd> (解释)、<kbd class="kbd-key">R</kbd> (重构) 或 <kbd class="kbd-key">O</kbd> (优化)。</li>
                        <li>脚本会自动：复制选中代码 -> 聚焦 Chat 面板 -> 填入预设 Prompt -> 发送。</li>
                    </ol>
                    <div class="mt-4 p-4 bg-black/50 rounded border border-cursor-border text-xs font-mono text-gray-400">
                        // 示例：解释代码的默认 Prompt<br>
                        "解释这段代码的核心逻辑、输入输出、关键函数作用，用新手能懂的语言，标注易错点..."
                    </div>
                </div>
            </section>

            <section id="feat-clipboard" class="mb-16 scroll-mt-20">
                <h2 class="text-2xl font-semibold mb-6 flex items-center gap-2">
                    <i data-lucide="clipboard-list" class="text-yellow-400"></i> 智能剪贴板
                </h2>
                
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
                    <div>
                        <h3 class="text-lg font-medium text-white mb-2">连续复制 (Queue Copy)</h3>
                        <p class="text-sm text-cursor-muted mb-4">
                            需要从多个文件中复制代码片段？无需来回切换窗口。
                            选中A -> <kbd class="kbd-key">CapsLock</kbd>+<kbd class="kbd-key">C</kbd>，选中B -> <kbd class="kbd-key">CapsLock</kbd>+<kbd class="kbd-key">C</kbd>...
                            所有内容会被存入临时队列。
                        </p>
                    </div>
                    <div>
                        <h3 class="text-lg font-medium text-white mb-2">合并粘贴</h3>
                        <p class="text-sm text-cursor-muted mb-4">
                            回到目标位置，按 <kbd class="kbd-key">CapsLock</kbd>+<kbd class="kbd-key">V</kbd>。
                            队列中的所有片段将按顺序合并，一次性粘贴。
                        </p>
                    </div>
                </div>

                <!-- 动作演示区域 -->
                <div class="mt-4 border border-cursor-border rounded-xl bg-cursor-sidebar/50 p-6 overflow-hidden relative shadow-lg">
                    <div class="flex justify-between items-center mb-4">
                        <h4 class="text-white font-medium flex items-center gap-2">
                            <i data-lucide="monitor-play" class="w-4 h-4 text-cursor-accent"></i>
                            动作演示：批量提取函数名
                        </h4>
                        <div class="text-xs text-cursor-muted font-mono bg-black/30 px-2 py-1 rounded">Interactive Demo</div>
                    </div>
                    
                    <!-- 动画舞台 -->
                    <div id="demo-stage" class="relative h-[280px] bg-cursor-bg border border-cursor-border rounded-lg flex items-start justify-between p-6 overflow-hidden">
                        
                        <!-- 左侧：源文件 -->
                        <div class="w-[45%] h-full flex flex-col relative z-10">
                            <div class="text-xs text-cursor-muted mb-2 font-medium">📄 utils.py (源文件)</div>
                            <div class="demo-window flex-1 bg-[#1E1E1E] rounded-md border border-cursor-border p-3 font-mono text-xs text-gray-400 leading-6 shadow-inner relative">
                                <div id="line-1" class="code-line px-1 rounded">def <span class="text-blue-300">calculate_sum</span>(a, b):</div>
                                <div class="pl-4 text-gray-600">return a + b</div>
                                <div id="line-2" class="code-line px-1 rounded mt-2">def <span class="text-blue-300">calculate_avg</span>(a, b):</div>
                                <div class="pl-4 text-gray-600">return (a + b) / 2</div>
                                <div id="line-3" class="code-line px-1 rounded mt-2">def <span class="text-blue-300">format_output</span>(res):</div>
                                <div class="pl-4 text-gray-600">print(f"Res: {res}")</div>
                                
                                <!-- 模拟光标选区 -->
                                <div id="selection-highlight" class="absolute bg-blue-500/30 border border-blue-500/50 rounded pointer-events-none opacity-0 transition-all duration-200"></div>
                            </div>
                        </div>

                        <!-- 中间：剪贴板队列可视化 -->
                        <div class="w-[10%] h-full flex flex-col items-center justify-center relative z-0">
                            <div class="absolute inset-y-0 w-[1px] border-l border-dashed border-cursor-border"></div>
                            <div id="clipboard-queue" class="relative w-full h-40 flex flex-col-reverse items-center gap-2">
                                <!-- 队列项会动态插入到这里 -->
                            </div>
                            <div class="mt-2 text-[10px] text-cursor-muted uppercase tracking-wider">Queue</div>
                        </div>

                        <!-- 右侧：目标文件 -->
                        <div class="w-[45%] h-full flex flex-col relative z-10">
                            <div class="text-xs text-cursor-muted mb-2 font-medium">📄 main.py (目标文件)</div>
                            <div class="demo-window flex-1 bg-[#1E1E1E] rounded-md border border-cursor-border p-3 font-mono text-xs text-gray-300 shadow-inner relative">
                                <div class="text-gray-500"># 导入需要的函数</div>
                                <div>from utils import <span id="target-content"></span><span class="cursor-caret"></span></div>
                            </div>
                        </div>

                    </div>

                    <!-- 状态栏/解说字幕 -->
                    <div class="mt-4 flex items-center justify-center h-8">
                        <div id="demo-caption" class="px-4 py-1.5 rounded-full bg-black/50 border border-cursor-border text-xs text-cursor-accent font-mono transition-all duration-300">
                            正在初始化演示...
                        </div>
                    </div>
                </div>

                <!-- 优点列表 -->
                <div class="mt-6 grid grid-cols-1 sm:grid-cols-3 gap-4">
                    <div class="bg-cursor-sidebar/30 p-4 rounded-lg border border-cursor-border/50">
                        <div class="text-cursor-accent mb-2"><i data-lucide="zap" class="w-5 h-5"></i></div>
                        <h5 class="text-white text-sm font-semibold mb-1">减少切换</h5>
                        <p class="text-xs text-cursor-muted">无需在源文件和目标文件之间频繁 Alt+Tab 切换窗口。</p>
                    </div>
                    <div class="bg-cursor-sidebar/30 p-4 rounded-lg border border-cursor-border/50">
                        <div class="text-cursor-accent mb-2"><i data-lucide="layers" class="w-5 h-5"></i></div>
                        <h5 class="text-white text-sm font-semibold mb-1">保持心流</h5>
                        <p class="text-xs text-cursor-muted">一次性收集所需素材，保持阅读代码的连贯性，不被打断。</p>
                    </div>
                    <div class="bg-cursor-sidebar/30 p-4 rounded-lg border border-cursor-border/50">
                        <div class="text-cursor-accent mb-2"><i data-lucide="database" class="w-5 h-5"></i></div>
                        <h5 class="text-white text-sm font-semibold mb-1">自动合并</h5>
                        <p class="text-xs text-cursor-muted">粘贴时自动用空格或换行符连接，智能处理格式。</p>
                    </div>
                </div>
            </section>

            <section id="feat-search" class="mb-16 scroll-mt-20">
                <h2 class="text-2xl font-semibold mb-6 flex items-center gap-2">
                    <i data-lucide="globe" class="text-blue-400"></i> 多引擎聚合搜索
                </h2>
                
                <div class="space-y-4 mb-8">
                    <div class="flex gap-4 items-start">
                        <div class="w-10 h-10 rounded bg-blue-900/30 flex items-center justify-center flex-shrink-0 text-blue-400 font-bold">F</div>
                        <div>
                            <h3 class="font-medium text-white">聚合搜索</h3>
                            <p class="text-sm text-cursor-muted">
                                编程遇到问题？一键呼出搜索框，输入关键词，<strong>同时在多个搜索引擎</strong>中查找结果。告别逐个打开网页的低效。
                            </p>
                            <p class="text-sm text-cursor-muted mt-2">
                                支持引擎：DeepSeek, Google, GitHub, StackOverflow, Baidu 等。
                            </p>
                        </div>
                    </div>
                </div>

                <!-- 搜索动作演示 -->
                <div class="mt-6 border border-cursor-border rounded-xl bg-cursor-sidebar/50 p-6 overflow-hidden relative shadow-lg">
                    <div class="flex justify-between items-center mb-4">
                        <h4 class="text-white font-medium flex items-center gap-2">
                            <i data-lucide="monitor-play" class="w-4 h-4 text-cursor-accent"></i>
                            动作演示：多引擎并发搜索
                        </h4>
                        <div class="text-xs text-cursor-muted font-mono bg-black/30 px-2 py-1 rounded">Interactive Demo</div>
                    </div>

                    <!-- 搜索演示舞台 -->
                    <div id="search-demo-stage" class="relative h-[300px] bg-cursor-bg border border-cursor-border rounded-lg flex items-center justify-center overflow-hidden p-4">
                        
                        <!-- 搜索面板 (模拟) -->
                        <div id="search-panel" class="absolute z-20 w-80 bg-[#1E1E1E] border border-cursor-border rounded-lg shadow-2xl p-4 transform transition-all duration-500 opacity-0 scale-90 origin-center">
                            <div class="flex items-center justify-between mb-3">
                                <span class="text-xs font-bold text-white flex items-center gap-2"><i data-lucide="search" class="w-3 h-3 text-blue-400"></i> 聚合搜索</span>
                            </div>
                            <div class="bg-black/30 rounded p-2 mb-3 border border-cursor-border/50 h-10 flex items-center">
                                <span id="search-input-text" class="text-sm text-gray-300 font-mono"></span><span class="cursor-caret"></span>
                            </div>
                            <div class="grid grid-cols-2 gap-2 mb-3">
                                <div id="engine-deepseek" class="text-xs border border-cursor-border rounded px-2 py-1.5 text-gray-400 bg-cursor-bg transition-colors duration-300 flex items-center gap-1 cursor-pointer">DeepSeek</div>
                                <div id="engine-google" class="text-xs border border-cursor-border rounded px-2 py-1.5 text-gray-400 bg-cursor-bg transition-colors duration-300 flex items-center gap-1 cursor-pointer">Google</div>
                                <div id="engine-github" class="text-xs border border-cursor-border rounded px-2 py-1.5 text-gray-400 bg-cursor-bg transition-colors duration-300 flex items-center gap-1 cursor-pointer">GitHub</div>
                                <div id="engine-baidu" class="text-xs border border-cursor-border rounded px-2 py-1.5 text-gray-400 bg-cursor-bg transition-colors duration-300 flex items-center gap-1 cursor-pointer">Baidu</div>
                            </div>
                            <div class="flex justify-end">
                                <div id="search-btn" class="bg-cursor-accent text-white text-xs px-3 py-1.5 rounded opacity-50 transition-opacity">搜索</div>
                            </div>
                        </div>

                        <!-- 浏览器窗口 (模拟) -->
                        <div id="browser-window" class="absolute z-10 inset-x-10 bottom-0 top-10 bg-[#2D2D2D] rounded-t-lg shadow-2xl transform translate-y-full transition-transform duration-500 flex flex-col">
                            <!-- 浏览器标题栏 -->
                            <div class="h-8 bg-[#202020] rounded-t-lg flex items-center px-2 gap-2 border-b border-black">
                                <div class="flex gap-1.5">
                                    <div class="w-2.5 h-2.5 rounded-full bg-red-500"></div>
                                    <div class="w-2.5 h-2.5 rounded-full bg-yellow-500"></div>
                                    <div class="w-2.5 h-2.5 rounded-full bg-green-500"></div>
                                </div>
                                <!-- Tabs Container -->
                                <div id="browser-tabs" class="flex gap-1 ml-4 overflow-hidden items-end h-full pt-1">
                                    <!-- Tabs will be injected here -->
                                </div>
                            </div>
                            <!-- 浏览器内容区 -->
                            <div class="flex-1 bg-white relative overflow-hidden">
                                <div id="browser-content" class="absolute inset-0 p-4 font-sans text-gray-800">
                                    <div class="animate-pulse space-y-3">
                                        <div class="h-4 bg-gray-200 rounded w-1/3"></div>
                                        <div class="h-4 bg-gray-200 rounded w-2/3"></div>
                                        <div class="h-4 bg-gray-200 rounded w-1/2"></div>
                                    </div>
                                </div>
                                <!-- Loading Spinner overlay -->
                                <div id="browser-loading" class="absolute inset-0 bg-white/80 flex items-center justify-center opacity-0 transition-opacity pointer-events-none">
                                    <i data-lucide="loader-2" class="w-8 h-8 text-blue-500 animate-spin"></i>
                                </div>
                            </div>
                        </div>

                    </div>

                    <!-- 状态栏/解说字幕 -->
                    <div class="mt-4 flex items-center justify-center h-8">
                        <div id="search-demo-caption" class="px-4 py-1.5 rounded-full bg-black/50 border border-cursor-border text-xs text-cursor-accent font-mono transition-all duration-300">
                            等待开始...
                        </div>
                    </div>
                </div>
            </section>

            <section id="feat-utils" class="mb-16 scroll-mt-20">
                <h2 class="text-2xl font-semibold mb-6">其他实用工具</h2>
                <ul class="space-y-4">
                    <li class="bg-cursor-sidebar p-4 rounded-lg border border-cursor-border">
                        <div class="flex justify-between items-center mb-2">
                            <span class="font-bold text-white">代码分割 (S)</span>
                            <span class="text-xs bg-gray-700 text-gray-300 px-2 py-1 rounded">Batch</span>
                        </div>
                        <p class="text-sm text-cursor-muted">在代码中插入特定的分割标记。结合 <strong>批量操作 (B)</strong>，可以一次性让 AI 处理多个分散的代码块。</p>
                    </li>
                    <li class="bg-cursor-sidebar p-4 rounded-lg border border-cursor-border">
                        <div class="flex justify-between items-center mb-2">
                            <span class="font-bold text-white">截图粘贴 (P)</span>
                            <span class="text-xs bg-gray-700 text-gray-300 px-2 py-1 rounded">Image</span>
                        </div>
                        <p class="text-sm text-cursor-muted">调用系统截图工具。截图完成后，屏幕会出现悬浮按钮，点击即可将图片粘贴到 Cursor 对话框中（解决部分场景下直接粘贴失效的问题）。</p>
                    </li>
                </ul>

                <!-- 截图动作演示 -->
                <div class="mt-6 border border-cursor-border rounded-xl bg-cursor-sidebar/50 p-6 overflow-hidden relative shadow-lg">
                    <div class="flex justify-between items-center mb-4">
                        <h4 class="text-white font-medium flex items-center gap-2">
                            <i data-lucide="monitor-play" class="w-4 h-4 text-cursor-accent"></i>
                            动作演示：截图自动粘贴
                        </h4>
                        <div class="text-xs text-cursor-muted font-mono bg-black/30 px-2 py-1 rounded">Interactive Demo</div>
                    </div>

                    <!-- 截图演示舞台 -->
                    <div id="screenshot-demo-stage" class="relative h-[280px] bg-cursor-bg border border-cursor-border rounded-lg overflow-hidden flex flex-col">
                        
                        <!-- 屏幕内容 -->
                        <div class="flex-1 p-4 grid grid-cols-2 gap-4 opacity-50 transition-opacity duration-300" id="screenshot-bg">
                            <div class="bg-[#2D2D2D] rounded h-20 w-full animate-pulse"></div>
                            <div class="bg-[#2D2D2D] rounded h-20 w-full animate-pulse delay-100"></div>
                            <div class="bg-[#2D2D2D] rounded h-40 w-full col-span-2 animate-pulse delay-200"></div>
                        </div>

                        <!-- 遮罩层 (Snipping Overlay) -->
                        <div id="screenshot-overlay" class="absolute inset-0 bg-black/60 opacity-0 pointer-events-none transition-opacity duration-300">
                            <!-- 选区 -->
                            <div id="screenshot-selection" class="absolute border-2 border-white bg-transparent shadow-[0_0_0_9999px_rgba(0,0,0,0.5)] opacity-0 transition-all duration-700 ease-out"></div>
                        </div>

                        <!-- 悬浮按钮 -->
                        <div id="screenshot-float-btn" class="absolute left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2 bg-cursor-accent text-white px-4 py-2 rounded-lg shadow-xl flex items-center gap-2 transform scale-0 transition-transform duration-300 z-50 cursor-pointer">
                            <i data-lucide="clipboard" class="w-4 h-4"></i> 粘贴截图
                        </div>

                        <!-- Cursor 对话框 (模拟) -->
                        <div id="cursor-chat-window" class="absolute inset-x-0 bottom-0 h-40 bg-[#1E1E1E] border-t border-cursor-border transform translate-y-full transition-transform duration-500 z-40 flex flex-col">
                            <div class="h-8 bg-[#252526] flex items-center px-4 text-xs text-gray-400 border-b border-black">Cursor Chat</div>
                            <div class="flex-1 p-4 flex flex-col gap-2">
                                <div class="flex items-start gap-2">
                                    <div class="w-6 h-6 rounded-full bg-blue-500/20 text-blue-400 flex items-center justify-center text-xs">U</div>
                                    <div class="flex-1 bg-[#2D2D2D] rounded p-2">
                                        <div id="pasted-image-placeholder" class="w-32 h-20 bg-gray-700 rounded flex items-center justify-center text-xs text-gray-400 opacity-0 transition-opacity duration-500">
                                            <i data-lucide="image" class="w-6 h-6 mb-1"></i>
                                            Image.png
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                    </div>

                    <!-- 状态栏/解说字幕 -->
                    <div class="mt-4 flex items-center justify-center h-8">
                        <div id="screenshot-demo-caption" class="px-4 py-1.5 rounded-full bg-black/50 border border-cursor-border text-xs text-cursor-accent font-mono transition-all duration-300">
                            等待开始...
                        </div>
                    </div>
                </div>
            </section>

            <!-- Settings -->
            <section id="interface-settings" class="mb-16 scroll-mt-20">
                <h2 class="text-2xl font-semibold mb-6">配置与个性化 (Q)</h2>
                <p class="text-cursor-muted mb-4">按 <kbd class="kbd-key">CapsLock</kbd>+<kbd class="kbd-key">Q</kbd> 打开设置面板。</p>
                <div class="bg-cursor-sidebar p-6 rounded-lg border border-cursor-border space-y-4">
                    <div>
                        <h4 class="text-white font-medium">主要设置项：</h4>
                        <ul class="list-disc list-inside text-sm text-cursor-muted mt-2 space-y-1">
                            <li><strong>Cursor 路径：</strong> 设置 Cursor.exe 的绝对路径（用于自动启动）。</li>
                            <li><strong>AI 响应时间：</strong> 调整脚本等待 AI 窗口响应的毫秒数。</li>
                            <li><strong>提示词模板：</strong> 修改解释、重构、优化的默认 Prompt。</li>
                            <li><strong>外观：</strong> 切换面板的深色/浅色主题，调整位置。</li>
                        </ul>
                    </div>
                    <div class="border-t border-cursor-border pt-4">
                        <h4 class="text-white font-medium mb-2">Cursor 规则 (.cursorrules)</h4>
                        <p class="text-sm text-cursor-muted">
                            设置面板中内置了常用的 Cursor Rules。您可以选择特定的技术栈（如 Python, Web, iOS），一键复制规则内容并粘贴到项目的 <code>.cursorrules</code> 文件中，让 AI 更懂你的项目规范。
                        </p>
                    </div>
                </div>
            </section>

            <!-- Troubleshooting -->
            <section id="troubleshooting" class="mb-16 scroll-mt-20">
                <h2 class="text-2xl font-semibold mb-6">常见问题 & 故障排查</h2>
                <div class="space-y-4">
                    <details class="group bg-cursor-sidebar rounded-lg border border-cursor-border">
                        <summary class="flex justify-between items-center font-medium cursor-pointer list-none p-4">
                            <span>提示 "Cursor 未运行" 但我已经打开了</span>
                            <span class="transition group-open:rotate-180">
                                <i data-lucide="chevron-down" class="w-4 h-4"></i>
                            </span>
                        </summary>
                        <div class="text-cursor-muted text-sm px-4 pb-4 border-t border-cursor-border pt-4">
                            请检查设置面板中的 <strong>Cursor 路径</strong> 是否正确。通常路径为 <code>C:\Users\用户名\AppData\Local\Cursor\Cursor.exe</code>。如果没有正确识别，请点击“浏览”手动指定。
                        </div>
                    </details>

                    <details class="group bg-cursor-sidebar rounded-lg border border-cursor-border">
                        <summary class="flex justify-between items-center font-medium cursor-pointer list-none p-4">
                            <span>快捷键无反应或被杀毒软件拦截</span>
                            <span class="transition group-open:rotate-180">
                                <i data-lucide="chevron-down" class="w-4 h-4"></i>
                            </span>
                        </summary>
                        <div class="text-cursor-muted text-sm px-4 pb-4 border-t border-cursor-border pt-4">
                            脚本需要监听键盘底层钩子。请务必<strong>以管理员身份运行</strong>脚本。如果不生效，请尝试重新加载脚本或检查 Windows Defender/360 是否拦截了按键监听。
                        </div>
                    </details>

                    <details class="group bg-cursor-sidebar rounded-lg border border-cursor-border">
                        <summary class="flex justify-between items-center font-medium cursor-pointer list-none p-4">
                            <span>剪贴板历史记录不保存</span>
                            <span class="transition group-open:rotate-180">
                                <i data-lucide="chevron-down" class="w-4 h-4"></i>
                            </span>
                        </summary>
                        <div class="text-cursor-muted text-sm px-4 pb-4 border-t border-cursor-border pt-4">
                            请确保脚本目录下的 <code>sqlite3.dll</code> 文件存在。脚本使用 SQLite 数据库存储历史记录。如果丢失该文件，将回退到内存存储，重启后数据会丢失。
                        </div>
                    </details>
                </div>
            </section>

            <!-- Download Placeholder -->
            <section id="download" class="py-10 border-t border-cursor-border text-center">
                <h2 class="text-2xl font-bold mb-4">准备好提升效率了吗？</h2>
                <p class="text-cursor-muted mb-6">下载 CursorHelper，让 AI 编程快人一步。</p>
                <button class="bg-white text-black px-8 py-3 rounded-full font-bold hover:scale-105 transition-transform">
                    下载最新版 v2.0
                </button>
                <p class="text-xs text-cursor-muted mt-4">仅支持 Windows 10/11 系统</p>
            </section>

        </main>
    </div>

    <script>
        lucide.createIcons();
        
        // Simple active state for sidebar
        const sections = document.querySelectorAll('section');
        const navLinks = document.querySelectorAll('aside nav a');

        window.addEventListener('scroll', () => {
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                if (scrollY >= sectionTop - 100) {
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('text-white', 'bg-white/5');
                link.classList.add('text-cursor-muted');
                if (link.getAttribute('href').includes(current)) {
                    link.classList.add('text-white', 'bg-white/5');
                    link.classList.remove('text-cursor-muted');
                }
            });
        });

        function wait(ms) {
            return new Promise(resolve => setTimeout(resolve, ms));
        }

        /* ==================== CLIPBOARD DEMO ==================== */
        const demoData = [
            { text: 'calculate_sum', top: 12, left: 35, width: 100 },
            { text: 'calculate_avg', top: 60, left: 35, width: 100 },
            { text: 'format_output', top: 108, left: 35, width: 100 }
        ];

        const clipboardDemo = {
            caption: document.getElementById('demo-caption'),
            selection: document.getElementById('selection-highlight'),
            queue: document.getElementById('clipboard-queue'),
            target: document.getElementById('target-content'),
            stage: document.getElementById('demo-stage'),
            isAnimating: true
        };

        async function runClipboardDemo() {
            if(!clipboardDemo.isAnimating) return;

            // Reset
            clipboardDemo.queue.innerHTML = '';
            clipboardDemo.target.innerHTML = '';
            clipboardDemo.selection.style.opacity = '0';
            clipboardDemo.target.parentElement.classList.remove('animate-pulse');

            // Step 1-3: Copy items
            for (let i = 0; i < demoData.length; i++) {
                const item = demoData[i];
                
                // 1. Select
                clipboardDemo.caption.textContent = `1. 选中 ${item.text}...`;
                clipboardDemo.caption.className = "px-4 py-1.5 rounded-full bg-blue-500/20 border border-blue-500/50 text-xs text-blue-300 font-mono transition-all duration-300";
                
                clipboardDemo.selection.style.top = item.top + 'px';
                clipboardDemo.selection.style.left = item.left + 'px';
                clipboardDemo.selection.style.width = item.width + 'px';
                clipboardDemo.selection.style.height = '18px';
                clipboardDemo.selection.style.opacity = '1';
                await wait(800);

                // 2. Press Key
                clipboardDemo.caption.textContent = `2. 按 CapsLock + C 复制`;
                clipboardDemo.caption.className = "px-4 py-1.5 rounded-full bg-cursor-accent/20 border border-cursor-accent/50 text-xs text-cursor-accent font-mono transition-all duration-300 scale-105";
                await wait(600);

                // 3. Fly Animation
                createFlyingElement(item.text, item.top + 20, item.left + 20); 
                
                // Add to queue visual
                const queueItem = document.createElement('div');
                queueItem.className = 'bg-cursor-sidebar border border-cursor-border text-xs px-2 py-1 rounded text-cursor-muted w-24 text-center opacity-0 transform translate-y-4 transition-all duration-300';
                queueItem.textContent = item.text;
                clipboardDemo.queue.appendChild(queueItem);
                
                setTimeout(() => {
                    queueItem.classList.remove('opacity-0', 'translate-y-4');
                    queueItem.classList.add('border-cursor-accent', 'text-white');
                }, 400);

                await wait(1000);
            }

            // Step 4: Paste
            clipboardDemo.selection.style.opacity = '0';
            clipboardDemo.caption.textContent = `3. 切换到目标位置，按 CapsLock + V`;
            clipboardDemo.caption.className = "px-4 py-1.5 rounded-full bg-purple-500/20 border border-purple-500/50 text-xs text-purple-300 font-mono transition-all duration-300";
            await wait(1000);

            // Step 5: Merge Result
            clipboardDemo.caption.textContent = `4. 自动合并粘贴完成！`;
            clipboardDemo.caption.className = "px-4 py-1.5 rounded-full bg-green-500/20 border border-green-500/50 text-xs text-green-300 font-mono transition-all duration-300";
            
            const queueItems = clipboardDemo.queue.children;
            for(let item of queueItems) {
                item.style.transform = 'translateX(100px) scale(0.5)';
                item.style.opacity = '0';
            }

            const resultText = demoData.map(d => d.text).join(', ');
            clipboardDemo.target.textContent = resultText;
            clipboardDemo.target.classList.add('text-cursor-accent');
            
            await wait(3000);
            
            runClipboardDemo();
        }

        function createFlyingElement(text, top, left) {
            const el = document.createElement('div');
            el.className = 'flying-text';
            el.textContent = text;
            el.style.top = top + 'px'; 
            el.style.left = '40px'; 
            
            clipboardDemo.stage.appendChild(el);

            const keyframes = [
                { transform: `translate(0, 0) scale(1)`, opacity: 1 },
                { transform: `translate(200px, 0) scale(0.5)`, opacity: 0 } 
            ];

            const anim = el.animate(keyframes, {
                duration: 600,
                easing: 'cubic-bezier(0.4, 0, 0.2, 1)'
            });

            anim.onfinish = () => el.remove();
        }

        /* ==================== SEARCH DEMO (REPLACED VOICE) ==================== */
        const searchDemo = {
            panel: document.getElementById('search-panel'),
            input: document.getElementById('search-input-text'),
            searchBtn: document.getElementById('search-btn'),
            browser: document.getElementById('browser-window'),
            tabsContainer: document.getElementById('browser-tabs'),
            caption: document.getElementById('search-demo-caption'),
            stage: document.getElementById('search-demo-stage'),
            engines: {
                deepseek: document.getElementById('engine-deepseek'),
                google: document.getElementById('engine-google'),
                github: document.getElementById('engine-github'),
                baidu: document.getElementById('engine-baidu')
            },
            isAnimating: true
        };

        async function runSearchDemo() {
            if(!searchDemo.isAnimating) return;

            // --- Reset State ---
            searchDemo.panel.classList.remove('opacity-100', 'scale-100');
            searchDemo.panel.classList.add('opacity-0', 'scale-90');
            searchDemo.browser.classList.remove('translate-y-0');
            searchDemo.browser.classList.add('translate-y-full');
            searchDemo.input.textContent = '';
            searchDemo.searchBtn.classList.add('opacity-50');
            searchDemo.tabsContainer.innerHTML = '';
            
            Object.values(searchDemo.engines).forEach(el => {
                el.classList.remove('engine-selected');
                el.innerHTML = el.id.split('-')[1].charAt(0).toUpperCase() + el.id.split('-')[1].slice(1);
            });

            await wait(1000);

            // --- Step 1: CapsLock+F ---
            searchDemo.caption.textContent = '1. 按下 CapsLock + F 唤起搜索面板';
            searchDemo.caption.className = "px-4 py-1.5 rounded-full bg-blue-500/20 border border-blue-500/50 text-xs text-blue-300 font-mono transition-all duration-300";
            
            searchDemo.panel.classList.remove('opacity-0', 'scale-90');
            searchDemo.panel.classList.add('opacity-100', 'scale-100');
            
            await wait(800);

            // --- Step 2: Typing ---
            searchDemo.caption.textContent = '2. 输入: "Python Asyncio 教程"';
            searchDemo.caption.className = "px-4 py-1.5 rounded-full bg-cursor-accent/20 border border-cursor-accent/50 text-xs text-cursor-accent font-mono transition-all duration-300";
            
            const phrase = "Python Asyncio 教程";
            for(let i=0; i<phrase.length; i++) {
                searchDemo.input.textContent += phrase[i];
                await wait(80); // Typing speed
            }
            await wait(500);

            // --- Step 3: Select Engines ---
            searchDemo.caption.textContent = '3. 选择多个搜索引擎';
            searchDemo.caption.className = "px-4 py-1.5 rounded-full bg-yellow-500/20 border border-yellow-500/50 text-xs text-yellow-300 font-mono transition-all duration-300";

            const enginesToSelect = ['deepseek', 'google', 'github'];
            for (let engine of enginesToSelect) {
                const el = searchDemo.engines[engine];
                el.classList.add('engine-selected');
                // Add fake checkmark
                el.innerHTML = `<span class="engine-check">✓</span>${engine.charAt(0).toUpperCase() + engine.slice(1)}`;
                await wait(400);
            }
            
            searchDemo.searchBtn.classList.remove('opacity-50'); // Enable button visually
            await wait(500);

            // --- Step 4: Click Search ---
            searchDemo.caption.textContent = '4. 点击搜索，并发打开结果';
            searchDemo.caption.className = "px-4 py-1.5 rounded-full bg-purple-500/20 border border-purple-500/50 text-xs text-purple-300 font-mono transition-all duration-300";
            
            searchDemo.searchBtn.style.transform = 'scale(0.95)';
            setTimeout(() => searchDemo.searchBtn.style.transform = 'scale(1)', 100);
            
            await wait(300);
            searchDemo.panel.classList.add('opacity-0', 'scale-90'); // Hide panel
            await wait(200);

            // --- Step 5: Browser & Tabs ---
            searchDemo.browser.classList.remove('translate-y-full');
            searchDemo.browser.classList.add('translate-y-0');
            
            await wait(400);

            const tabs = [
                { name: 'DeepSeek', color: 'bg-blue-500' },
                { name: 'Google', color: 'bg-red-500' },
                { name: 'GitHub', color: 'bg-gray-200 text-black' }
            ];

            for (let tab of tabs) {
                const tabEl = document.createElement('div');
                tabEl.className = `h-6 px-3 rounded-t-md text-[10px] flex items-center gap-2 bg-[#3C3C3C] text-gray-300 border-r border-black/20 tab-enter`;
                tabEl.innerHTML = `<div class="w-2 h-2 rounded-full ${tab.color}"></div>${tab.name}`;
                searchDemo.tabsContainer.appendChild(tabEl);
                await wait(200);
            }

            // Simulate content loading
            const loader = document.getElementById('browser-loading');
            loader.classList.remove('opacity-0');
            await wait(800);
            loader.classList.add('opacity-0');

            await wait(2500);
            runSearchDemo();
        }

        /* ==================== SCREENSHOT DEMO ==================== */
        const screenshotDemo = {
            bg: document.getElementById('screenshot-bg'),
            overlay: document.getElementById('screenshot-overlay'),
            selection: document.getElementById('screenshot-selection'),
            floatBtn: document.getElementById('screenshot-float-btn'),
            chatWindow: document.getElementById('cursor-chat-window'),
            pastedImage: document.getElementById('pasted-image-placeholder'),
            caption: document.getElementById('screenshot-demo-caption'),
            stage: document.getElementById('screenshot-demo-stage'),
            isAnimating: true
        };

        async function runScreenshotDemo() {
            if(!screenshotDemo.isAnimating) return;

            // Reset
            screenshotDemo.overlay.classList.add('opacity-0');
            screenshotDemo.overlay.classList.remove('opacity-100');
            screenshotDemo.selection.style.width = '0';
            screenshotDemo.selection.style.height = '0';
            screenshotDemo.selection.style.opacity = '0';
            screenshotDemo.floatBtn.classList.add('scale-0');
            screenshotDemo.floatBtn.classList.remove('scale-100');
            screenshotDemo.chatWindow.classList.add('translate-y-full');
            screenshotDemo.chatWindow.classList.remove('translate-y-0');
            screenshotDemo.pastedImage.classList.add('opacity-0');
            
            await wait(1000);

            // 1. CapsLock+P
            screenshotDemo.caption.textContent = '1. 按下 CapsLock + P 启动截图';
            screenshotDemo.caption.className = "px-4 py-1.5 rounded-full bg-blue-500/20 border border-blue-500/50 text-xs text-blue-300 font-mono transition-all duration-300";
            
            await wait(800);
            
            // Show Overlay
            screenshotDemo.overlay.classList.remove('opacity-0');
            screenshotDemo.overlay.classList.add('opacity-100');
            screenshotDemo.bg.classList.add('crosshair-cursor'); // Add crosshair
            
            await wait(500);

            // 2. Select Area
            screenshotDemo.caption.textContent = '2. 框选截图区域';
            screenshotDemo.caption.className = "px-4 py-1.5 rounded-full bg-yellow-500/20 border border-yellow-500/50 text-xs text-yellow-300 font-mono transition-all duration-300";
            
            screenshotDemo.selection.style.opacity = '1';
            screenshotDemo.selection.style.left = '20%';
            screenshotDemo.selection.style.top = '20%';
            // Simulate dragging
            screenshotDemo.selection.style.width = '60%';
            screenshotDemo.selection.style.height = '50%';
            
            await wait(1000);

            // 3. Float Button Appears
            screenshotDemo.overlay.classList.add('opacity-0'); // Hide overlay
            screenshotDemo.overlay.classList.remove('opacity-100');
            screenshotDemo.bg.classList.remove('crosshair-cursor');
            
            await wait(200);
            screenshotDemo.caption.textContent = '3. 悬浮按钮自动出现';
            screenshotDemo.caption.className = "px-4 py-1.5 rounded-full bg-cursor-accent/20 border border-cursor-accent/50 text-xs text-cursor-accent font-mono transition-all duration-300";
            
            screenshotDemo.floatBtn.classList.remove('scale-0');
            screenshotDemo.floatBtn.classList.add('scale-100');
            
            await wait(1000);

            // 4. Click Paste
            screenshotDemo.caption.textContent = '4. 点击粘贴，自动发送到 Cursor';
            screenshotDemo.caption.className = "px-4 py-1.5 rounded-full bg-purple-500/20 border border-purple-500/50 text-xs text-purple-300 font-mono transition-all duration-300";
            
            screenshotDemo.floatBtn.style.transform = 'translate(-50%, -50%) scale(0.9)'; // Click effect
            await wait(150);
            screenshotDemo.floatBtn.style.transform = 'translate(-50%, -50%) scale(0)'; // Hide button
            
            await wait(300);
            
            // Show Chat Window
            screenshotDemo.chatWindow.classList.remove('translate-y-full');
            screenshotDemo.chatWindow.classList.add('translate-y-0');
            
            await wait(500);
            // Show pasted image
            screenshotDemo.pastedImage.classList.remove('opacity-0');
            
            await wait(3000);
            runScreenshotDemo();
        }


        // Observers
        const cbObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    clipboardDemo.isAnimating = true;
                    runClipboardDemo();
                    cbObserver.unobserve(entry.target);
                }
            });
        });

        const searchObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    searchDemo.isAnimating = true;
                    runSearchDemo();
                    searchObserver.unobserve(entry.target);
                }
            });
        });

        const screenshotObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    screenshotDemo.isAnimating = true;
                    runScreenshotDemo();
                    screenshotObserver.unobserve(entry.target);
                }
            });
        });
        
        setTimeout(() => {
            if(clipboardDemo.stage) cbObserver.observe(clipboardDemo.stage);
            if(searchDemo.stage) searchObserver.observe(searchDemo.stage);
            if(screenshotDemo.stage) screenshotObserver.observe(screenshotDemo.stage);
        }, 1000);

    </script>
</body>
</html>
