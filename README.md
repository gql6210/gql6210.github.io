<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Name | Developer Portfolio</title>
    <!-- 外部资源 -->
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.8/dist/chart.umd.min.js"></script>
    
    <!-- Tailwind 配置 -->
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        primary: '#165DFF',
                        secondary: '#36CFC9',
                        dark: '#1E293B',
                        light: '#F8FAFC'
                    },
                    fontFamily: {
                        inter: ['Inter', 'system-ui', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    
    <!-- 自定义样式 -->
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .text-shadow {
                text-shadow: 0 2px 4px rgba(0,0,0,0.1);
            }
            .card-hover {
                @apply transition-all duration-300 hover:shadow-lg hover:-translate-y-1;
            }
        }
        
        /* 基础样式 */
        body {
            scroll-behavior: smooth;
        }
        
        /* 加载动画 */
        .loader {
            border-top-color: #165DFF;
            animation: spinner 0.6s linear infinite;
        }
        
        @keyframes spinner {
            to {
                transform: rotate(360deg);
            }
        }
    </style>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
</head>

<body class="font-inter bg-light dark:bg-dark text-slate-800 dark:text-slate-200 min-h-screen">
    <!-- 加载遮罩 -->
    <div id="loader" class="fixed inset-0 flex items-center justify-center bg-white dark:bg-dark z-50">
        <div class="loader h-12 w-12 rounded-full border-4 border-slate-200 dark:border-slate-700"></div>
    </div>

    <!-- 导航栏 -->
    <header class="sticky top-0 z-40 bg-white/80 dark:bg-dark/80 backdrop-blur-md border-b border-slate-200 dark:border-slate-700">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <!-- 品牌/名称 -->
                <a href="#hero" class="flex items-center space-x-2">
                    <span class="text-primary text-2xl"><i class="fa fa-code"></i></span>
                    <span class="font-bold text-lg">Your Name</span>
                </a>
                
                <!-- 桌面导航 -->
                <nav class="hidden md:flex space-x-8">
                    <a href="#about" class="text-sm font-medium hover:text-primary transition-colors">About</a>
                    <a href="#skills" class="text-sm font-medium hover:text-primary transition-colors">Skills</a>
                    <a href="#projects" class="text-sm font-medium hover:text-primary transition-colors">Projects</a>
                    <a href="#contact" class="text-sm font-medium hover:text-primary transition-colors">Contact</a>
                </nav>
                
                <!-- 主题切换 -->
                <button id="theme-toggle" class="p-2 rounded-full hover:bg-slate-100 dark:hover:bg-slate-800 transition-colors">
                    <i class="fa fa-moon-o dark:hidden text-slate-600"></i>
                    <i class="fa fa-sun-o hidden dark:block text-slate-300"></i>
                </button>
                
                <!-- 移动端菜单按钮 -->
                <button id="mobile-menu-button" class="md:hidden p-2 rounded-full hover:bg-slate-100 dark:hover:bg-slate-800 transition-colors">
                    <i class="fa fa-bars"></i>
                </button>
            </div>
        </div>
        
        <!-- 移动端导航菜单 -->
        <div id="mobile-menu" class="md:hidden hidden bg-white dark:bg-dark border-b border-slate-200 dark:border-slate-700">
            <div class="container mx-auto px-4 py-3 space-y-2">
                <a href="#about" class="block py-2 text-sm font-medium hover:text-primary transition-colors">About</a>
                <a href="#skills" class="block py-2 text-sm font-medium hover:text-primary transition-colors">Skills</a>
                <a href="#projects" class="block py-2 text-sm font-medium hover:text-primary transition-colors">Projects</a>
                <a href="#contact" class="block py-2 text-sm font-medium hover:text-primary transition-colors">Contact</a>
            </div>
        </div>
    </header>

    <main>
        <!-- 英雄区域 -->
        <section id="hero" class="py-20 md:py-32">
            <div class="container mx-auto px-4 sm:px-6 lg:px-8">
                <div class="flex flex-col md:flex-row items-center gap-10">
                    <div class="md:w-1/2 space-y-6">
                        <h1 class="text-[clamp(2rem,5vw,3.5rem)] font-bold leading-tight text-shadow">
                            Hi, I'm <span class="text-primary">Your Name</span>
                            <br>
                            <span class="text-[clamp(1.5rem,4vw,2.5rem)]">Full Stack Developer</span>
                        </h1>
                        <p class="text-lg text-slate-600 dark:text-slate-400 max-w-lg">
                            I build responsive and performant web applications with modern technologies.
                            Passionate about clean code, user experience, and continuous learning.
                        </p>
                        <div class="flex flex-wrap gap-4">
                            <a href="#projects" class="px-6 py-3 bg-primary text-white rounded-lg font-medium hover:bg-primary/90 transition-colors">
                                View My Work
                            </a>
                            <a href="#contact" class="px-6 py-3 border border-slate-300 dark:border-slate-600 rounded-lg font-medium hover:border-primary hover:text-primary transition-colors">
                                Get In Touch
                            </a>
                        </div>
                        <div class="flex space-x-4 pt-4">
                            <a href="https://github.com/your-username" target="_blank" class="text-slate-600 dark:text-slate-400 hover:text-primary transition-colors">
                                <i class="fa fa-github text-xl"></i>
                            </a>
                            <a href="https://linkedin.com/in/your-username" target="_blank" class="text-slate-600 dark:text-slate-400 hover:text-primary transition-colors">
                                <i class="fa fa-linkedin text-xl"></i>
                            </a>
                            <a href="https://twitter.com/your-username" target="_blank" class="text-slate-600 dark:text-slate-400 hover:text-primary transition-colors">
                                <i class="fa fa-twitter text-xl"></i>
                            </a>
                            <a href="https://dev.to/your-username" target="_blank" class="text-slate-600 dark:text-slate-400 hover:text-primary transition-colors">
                                <i class="fa fa-code text-xl"></i>
                            </a>
                        </div>
                    </div>
                    <div class="md:w-1/2 flex justify-center">
                        <div class="relative">
                            <div class="w-64 h-64 md:w-80 md:h-80 rounded-full bg-primary/10 dark:bg-primary/20 flex items-center justify-center">
                                <img src="https://picsum.photos/seed/dev/400/400" alt="Profile Picture" class="w-56 h-56 md:w-72 md:h-72 rounded-full object-cover border-4 border-white dark:border-slate-800 shadow-lg">
                            </div>
                            <!-- 装饰元素 -->
                            <div class="absolute -bottom-4 -right-4 w-16 h-16 bg-secondary rounded-full flex items-center justify-center text-white">
                                <i class="fa fa-code text-2xl"></i>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 关于我 -->
        <section id="about" class="py-20 bg-slate-50 dark:bg-slate-800/50">
            <div class="container mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold mb-4">About Me</h2>
                    <div class="w-20 h-1 bg-primary mx-auto"></div>
                </div>
                
                <div class="max-w-3xl mx-auto">
                    <p class="text-lg text-slate-700 dark:text-slate-300 mb-6">
                        I'm a passionate developer with over 5 years of experience building web applications. 
                        I specialize in full-stack development with a focus on creating clean, maintainable, 
                        and user-friendly code.
                    </p>
                    <p class="text-lg text-slate-700 dark:text-slate-300 mb-6">
                        My journey in tech started with a curiosity for how websites work, which led me to pursue 
                        a degree in Computer Science. Since then, I've worked with startups and established companies 
                        to build digital products that solve real-world problems.
                    </p>
                    <p class="text-lg text-slate-700 dark:text-slate-300">
                        When I'm not coding, you can find me contributing to open-source projects, 
                        writing technical blog posts, or exploring new technologies. I believe in 
                        continuous learning and strive to stay updated with the latest industry trends.
                    </p>
                    
                    <!-- 个人信息卡片 -->
                    <div class="mt-10 grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div class="bg-white dark:bg-slate-800 rounded-lg p-6 shadow-sm card-hover">
                            <h3 class="font-semibold text-xl mb-4 flex items-center">
                                <i class="fa fa-user text-primary mr-2"></i> Personal Info
                            </h3>
                            <ul class="space-y-3">
                                <li class="flex justify-between">
                                    <span class="text-slate-600 dark:text-slate-400">Name:</span>
                                    <span class="font-medium">Your Full Name</span>
                                </li>
                                <li class="flex justify-between">
                                    <span class="text-slate-600 dark:text-slate-400">Location:</span>
                                    <span class="font-medium">City, Country</span>
                                </li>
                                <li class="flex justify-between">
                                    <span class="text-slate-600 dark:text-slate-400">Email:</span>
                                    <span class="font-medium">your.email@example.com</span>
                                </li>
                                <li class="flex justify-between">
                                    <span class="text-slate-600 dark:text-slate-400">Availability:</span>
                                    <span class="font-medium text-green-500">Open for work</span>
                                </li>
                            </ul>
                        </div>
                        
                        <div class="bg-white dark:bg-slate-800 rounded-lg p-6 shadow-sm card-hover">
                            <h3 class="font-semibold text-xl mb-4 flex items-center">
                                <i class="fa fa-graduation-cap text-primary mr-2"></i> Education & Experience
                            </h3>
                            <ul class="space-y-3">
                                <li class="flex justify-between">
                                    <span class="text-slate-600 dark:text-slate-400">Degree:</span>
                                    <span class="font-medium">BSc in Computer Science</span>
                                </li>
                                <li class="flex justify-between">
                                    <span class="text-slate-600 dark:text-slate-400">Experience:</span>
                                    <span class="font-medium">5+ Years</span>
                                </li>
                                <li class="flex justify-between">
                                    <span class="text-slate-600 dark:text-slate-400">Specialization:</span>
                                    <span class="font-medium">Full Stack Development</span>
                                </li>
                                <li class="flex justify-between">
                                    <span class="text-slate-600 dark:text-slate-400">Languages:</span>
                                    <span class="font-medium">English, Spanish</span>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 技能部分 -->
        <section id="skills" class="py-20">
            <div class="container mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold mb-4">My Skills</h2>
                    <div class="w-20 h-1 bg-primary mx-auto"></div>
                </div>
                
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-10">
                    <!-- 技能图表 -->
                    <div class="bg-white dark:bg-slate-800 rounded-lg p-6 shadow-sm">
                        <h3 class="font-semibold text-xl mb-6">Proficiency</h3>
                        <div class="h-80">
                            <canvas id="skillsChart"></canvas>
                        </div>
                    </div>
                    
                    <!-- 技能列表 -->
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <!-- 前端技能 -->
                        <div class="bg-white dark:bg-slate-800 rounded-lg p-6 shadow-sm card-hover">
                            <h3 class="font-semibold text-xl mb-4 flex items-center">
                                <i class="fa fa-code text-primary mr-2"></i> Frontend
                            </h3>
                            <div class="flex flex-wrap gap-2">
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">HTML5</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">CSS3</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">JavaScript</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">TypeScript</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">React</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">Vue</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">Tailwind CSS</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">Next.js</span>
                            </div>
                        </div>
                        
                        <!-- 后端技能 -->
                        <div class="bg-white dark:bg-slate-800 rounded-lg p-6 shadow-sm card-hover">
                            <h3 class="font-semibold text-xl mb-4 flex items-center">
                                <i class="fa fa-server text-primary mr-2"></i> Backend
                            </h3>
                            <div class="flex flex-wrap gap-2">
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">Node.js</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">Express</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">Python</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">Django</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">MongoDB</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">PostgreSQL</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">REST APIs</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">GraphQL</span>
                            </div>
                        </div>
                        
                        <!-- 工具 & 其他 -->
                        <div class="bg-white dark:bg-slate-800 rounded-lg p-6 shadow-sm card-hover md:col-span-2">
                            <h3 class="font-semibold text-xl mb-4 flex items-center">
                                <i class="fa fa-wrench text-primary mr-2"></i> Tools & Others
                            </h3>
                            <div class="flex flex-wrap gap-2">
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">Git</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">GitHub</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">Docker</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">CI/CD</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">AWS</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">Firebase</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">Figma</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">VS Code</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">Linux</span>
                                <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 rounded-full text-sm">Testing</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 项目展示 -->
        <section id="projects" class="py-20 bg-slate-50 dark:bg-slate-800/50">
            <div class="container mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold mb-4">My Projects</h2>
                    <div class="w-20 h-1 bg-primary mx-auto"></div>
                    <p class="mt-6 text-lg text-slate-600 dark:text-slate-400 max-w-2xl mx-auto">
                        Here are some of the projects I've worked on. Feel free to check them out on GitHub!
                    </p>
                </div>
                
                <!-- 项目网格 -->
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- 项目 1 -->
                    <div class="bg-white dark:bg-slate-800 rounded-lg overflow-hidden shadow-sm card-hover">
                        <img src="https://picsum.photos/seed/project1/600/400" alt="Project 1" class="w-full h-48 object-cover">
                        <div class="p-6">
                            <h3 class="font-bold text-xl mb-2">E-Commerce Platform</h3>
                            <p class="text-slate-600 dark:text-slate-400 mb-4">
                                A full-featured e-commerce platform with shopping cart, payment integration, and admin dashboard.
                            </p>
                            <div class="flex flex-wrap gap-2 mb-4">
                                <span class="px-2 py-1 bg-primary/10 text-primary rounded text-xs">React</span>
                                <span class="px-2 py-1 bg-primary/10 text-primary rounded text-xs">Node.js</span>
                                <span class="px-2 py-1 bg-primary/10 text-primary rounded text-xs">MongoDB</span>
                                <span class="px-2 py-1 bg-primary/10 text-primary rounded text-xs">Stripe</span>
                            </div>
                            <div class="flex space-x-4">
                                <a href="https://github.com/your-username/ecommerce" target="_blank" class="text-primary hover:text-primary/80 flex items-center">
                                    <i class="fa fa-github mr-1"></i> Code
                                </a>
                                <a href="https://ecommerce-demo.com" target="_blank" class="text-primary hover:text-primary/80 flex items-center">
                                    <i class="fa fa-external-link mr-1"></i> Demo
                                </a>
                            </div>
                        </div>
                    </div>
                    
                    <!-- 项目 2 -->
                    <div class="bg-white dark:bg-slate-800 rounded-lg overflow-hidden shadow-sm card-hover">
                        <img src="https://picsum.photos/seed/project2/600/400" alt="Project 2" class="w-full h-48 object-cover">
                        <div class="p-6">
                            <h3 class="font-bold text-xl mb-2">Task Management App</h3>
                            <p class="text-slate-600 dark:text-slate-400 mb-4">
                                A collaborative task management application with real-time updates and team features.
                            </p>
                            <div class="flex flex-wrap gap-2 mb-4">
                                <span class="px-2 py-1 bg-primary/10 text-primary rounded text-xs">Vue.js</span>
                                <span class="px-2 py-1 bg-primary/10 text-primary rounded text-xs">Firebase</span>
                                <span class="px-2 py-1 bg-primary/10 text-primary rounded text-xs">TypeScript</span>
                                <span class="px-2 py-1 bg-primary/10 text-primary rounded text-xs">Tailwind</span>
                            </div>
                            <div class="flex space-x-4">
                                <a href="https://github.com/your-username/task-manager" target="_blank" class="text-primary hover:text-primary/80 flex items-center">
                                    <i class="fa fa-github mr-1"></i> Code
                                </a>
                                <a href="https://task-manager-demo.com" target="_blank" class="text-primary hover:text-primary/80 flex items-center">
                                    <i class="fa fa-external-link mr-1"></i> Demo
                                </a>
                            </div>
                        </div>
                    </div>
                    
                    <!-- 项目 3 -->
                    <div class="bg-white dark:bg-slate-800 rounded-lg overflow-hidden shadow-sm card-hover">
                        <img src="https://picsum.photos/seed/project3/600/400" alt="Project 3" class="w-full h-48 object-cover">
                        <div class="p-6">
                            <h3 class="font-bold text-xl mb-2">Weather Dashboard</h3>
                            <p class="text-slate-600 dark:text-slate-400 mb-4">
                                A responsive weather dashboard with real-time data, forecasts, and location tracking.
                            </p>
                            <div class="flex flex-wrap gap-2 mb-4">
                                <span class="px-2 py-1 bg-primary/10 text-primary rounded text-xs">Next.js</span>
                                <span class="px-2 py-1 bg-primary/10 text-primary rounded text-xs">API Integration</span>
                                <span class="px-2 py-1 bg-primary/10 text-primary rounded text-xs">Chart.js</span>
                                <span class="px-2 py-1 bg-primary/10 text-primary rounded text-xs">PWA</span>
                            </div>
                            <div class="flex space-x-4">
                                <a href="https://github.com/your-username/weather-dashboard" target="_blank" class="text-primary hover:text-primary/80 flex items-center">
                                    <i class="fa fa-github mr-1"></i> Code
                                </a>
                                <a href="https://weather-demo.com" target="_blank" class="text-primary hover:text-primary/80 flex items-center">
                                    <i class="fa fa-external-link mr-1"></i> Demo
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- 查看更多按钮 -->
                <div class="text-center mt-12">
                    <a href="https://github.com/your-username" target="_blank" class="inline-flex items-center px-6 py-3 bg-primary text-white rounded-lg font-medium hover:bg-primary/90 transition-colors">
                        <i class="fa fa-github mr-2"></i> View All Projects
                    </a>
                </div>
            </div>
        </section>

        <!-- 联系部分 -->
        <section id="contact" class="py-20">
            <div class="container mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold mb-4">Get In Touch</h2>
                    <div class="w-20 h-1 bg-primary mx-auto"></div>
                    <p class="mt-6 text-lg text-slate-600 dark:text-slate-400 max-w-2xl mx-auto">
                        Have a project in mind or want to collaborate? Feel free to reach out to me!
                    </p>
                </div>
                
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-10">
                    <!-- 联系信息 -->
                    <div class="space-y-8">
                        <div class="bg-white dark:bg-slate-800 rounded-lg p-6 shadow-sm card-hover">
                            <h3 class="font-semibold text-xl mb-4 flex items-center">
                                <i class="fa fa-envelope text-primary mr-2"></i> Email
                            </h3>
                            <p class="text-slate-600 dark:text-slate-400">
                                <a href="mailto:your.email@example.com" class="hover:text-primary transition-colors">your.email@example.com</a>
                            </p>
                        </div>
                        
                        <div class="bg-white dark:bg-slate-800 rounded-lg p-6 shadow-sm card-hover">
                            <h3 class="font-semibold text-xl mb-4 flex items-center">
                                <i class="fa fa-map-marker text-primary mr-2"></i> Location
                            </h3>
                            <p class="text-slate-600 dark:text-slate-400">
                                City, Country
                            </p>
                        </div>
                        
                        <div class="bg-white dark:bg-slate-800 rounded-lg p-6 shadow-sm card-hover">
                            <h3 class="font-semibold text-xl mb-4 flex items-center">
                                <i class="fa fa-link text-primary mr-2"></i> Connect With Me
                            </h3>
                            <div class="flex flex-wrap gap-4">
                                <a href="https://github.com/your-username" target="_blank" class="inline-flex items-center px-4 py-2 bg-slate-100 dark:bg-slate-700 rounded-lg hover:bg-slate-200 dark:hover:bg-slate-600 transition-colors">
                                    <i class="fa fa-github mr-2"></i> GitHub
                                </a>
                                <a href="https://linkedin.com/in/your-username" target="_blank" class="inline-flex items-center px-4 py-2 bg-slate-100 dark:bg-slate-700 rounded-lg hover:bg-slate-200 dark:hover:bg-slate-600 transition-colors">
                                    <i class="fa fa-linkedin mr-2"></i> LinkedIn
                                </a>
                                <a href="https://twitter.com/your-username" target="_blank" class="inline-flex items-center px-4 py-2 bg-slate-100 dark:bg-slate-700 rounded-lg hover:bg-slate-200 dark:hover:bg-slate-600 transition-colors">
                                    <i class="fa fa-twitter mr-2"></i> Twitter
                                </a>
                            </div>
                        </div>
                    </div>
                    
                    <!-- 联系表单 -->
                    <div class="bg-white dark:bg-slate-800 rounded-lg p-8 shadow-sm">
                        <h3 class="font-semibold text-xl mb-6">Send Me a Message</h3>
                        <form id="contact-form" class="space-y-6">
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                                <div>
                                    <label for="name" class="block text-sm font-medium text-slate-700 dark:text-slate-300 mb-2">Name</label>
                                    <input type="text" id="name" name="name" class="w-full px-4 py-2 border border-slate-300 dark:border-slate-600 rounded-lg bg-white dark:bg-slate-900 text-slate-800 dark:text-slate-200 focus:outline-none focus:ring-2 focus:ring-primary/50" placeholder="Your name" required>
                                </div>
                                <div>
                                    <label for="email" class="block text-sm font-medium text-slate-700 dark:text-slate-300 mb-2">Email</label>
                                    <input type="email" id="email" name="email" class="w-full px-4 py-2 border border-slate-300 dark:border-slate-600 rounded-lg bg-white dark:bg-slate-900 text-slate-800 dark:text-slate-200 focus:outline-none focus:ring-2 focus:ring-primary/50" placeholder="Your email" required>
                                </div>
                            </div>
                            <div>
                                <label for="subject" class="block text-sm font-medium text-slate-700 dark:text-slate-300 mb-2">Subject</label>
                                <input type="text" id="subject" name="subject" class="w-full px-4 py-2 border border-slate-300 dark:border-slate-600 rounded-lg bg-white dark:bg-slate-900 text-slate-800 dark:text-slate-200 focus:outline-none focus:ring-2 focus:ring-primary/50" placeholder="Message subject" required>
                            </div>
                            <div>
                                <label for="message" class="block text-sm font-medium text-slate-700 dark:text-slate-300 mb-2">Message</label>
                                <textarea id="message" name="message" rows="5" class="w-full px-4 py-2 border border-slate-300 dark:border-slate-600 rounded-lg bg-white dark:bg-slate-900 text-slate-800 dark:text-slate-200 focus:outline-none focus:ring-2 focus:ring-primary/50" placeholder="Your message" required></textarea>
                            </div>
                            <button type="submit" class="w-full px-6 py-3 bg-primary text-white rounded-lg font-medium hover:bg-primary/90 transition-colors flex items-center justify-center">
                                <i class="fa fa-paper-plane mr-2"></i> Send Message
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- 页脚 -->
    <footer class="bg-slate-900 text-white py-12">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-6 md:mb-0">
                    <div class="flex items-center space-x-2">
                        <span class="text-primary text-2xl"><i class="fa fa-code"></i></span>
                        <span class="font-bold text-lg">Your Name</span>
                    </div>
                    <p class="mt-2 text-slate-400">Full Stack Developer & Tech Enthusiast</p>
                </div>
                
                <div class="flex space-x-6">
                    <a href="https://github.com/your-username" target="_blank" class="text-slate-400 hover:text-white transition-colors">
                        <i class="fa fa-github text-xl"></i>
                    </a>
                    <a href="https://linkedin.com/in/your-username" target="_blank" class="text-slate-400 hover:text-white transition-colors">
                        <i class="fa fa-linkedin text-xl"></i>
                    </a>
                    <a href="https://twitter.com/your-username" target="_blank" class="text-slate-400 hover:text-white transition-colors">
                        <i class="fa fa-twitter text-xl"></i>
                    </a>
                    <a href="https://dev.to/your-username" target="_blank" class="text-slate-400 hover:text-white transition-colors">
                        <i class="fa fa-code text-xl"></i>
                    </a>
                </div>
            </div>
            
            <div class="border-t border-slate-800 mt-8 pt-8 text-center text-slate-400">
                <p>&copy; 2025 Your Name. All rights reserved.</p>
                <p class="mt-2 text-sm">Built with <i class="fa fa-heart text-red-500"></i> and <i class="fa fa-code text-primary"></i></p>
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        // DOM 加载完成后执行
        document.addEventListener('DOMContentLoaded', function() {
            // 加载动画
            const loader = document.getElementById('loader');
            setTimeout(() => {
                loader.classList.add('opacity-0');
                setTimeout(() => {
                    loader.style.display = 'none';
                }, 500);
            }, 800);
            
            // 主题切换
            const themeToggle = document.getElementById('theme-toggle');
            const html = document.documentElement;
            
            // 检查本地存储的主题偏好
            if (localStorage.getItem('theme') === 'dark' || (!localStorage.getItem('theme') && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
                html.classList.add('dark');
            } else {
                html.classList.remove('dark');
            }
            
            // 切换主题
            themeToggle.addEventListener('click', function() {
                html.classList.toggle('dark');
                if (html.classList.contains('dark')) {
                    localStorage.setItem('theme', 'dark');
                } else {
                    localStorage.setItem('theme', 'light');
                }
                updateChart(); // 更新图表颜色
            });
            
            // 移动端菜单
            const mobileMenuButton = document.getElementById('mobile-menu-button');
            const mobileMenu = document.getElementById('mobile-menu');
            
            mobileMenuButton.addEventListener('click', function() {
                mobileMenu.classList.toggle('hidden');
            });
            
            // 平滑滚动
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    
                    // 关闭移动端菜单
                    mobileMenu.classList.add('hidden');
                    
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);
                    
                    if (targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }
                });
            });
            
            // 技能图表
            let skillsChart;
            function initChart() {
                const ctx = document.getElementById('skillsChart').getContext('2d');
                const isDark = html.classList.contains('dark');
                const textColor = isDark ? '#e2e8f0' : '#1e293b';
                
                skillsChart = new Chart(ctx, {
                    type: 'radar',
                    data: {
                        labels: ['JavaScript', 'React', 'Node.js', 'HTML/CSS', 'Python', 'SQL', 'Git'],
                        datasets: [{
                            label: 'Proficiency',
                            data: [90, 85, 80, 95, 75, 70, 85],
                            backgroundColor: 'rgba(22, 93, 255, 0.2)',
                            borderColor: '#165DFF',
                            pointBackgroundColor: '#165DFF',
                            pointBorderColor: '#fff',
                            pointHoverBackgroundColor: '#fff',
                            pointHoverBorderColor: '#165DFF'
                        }]
                    },
                    options: {
                        scales: {
                            r: {
                                angleLines: {
                                    color: isDark ? 'rgba(255, 255, 255, 0.1)' : 'rgba(0, 0, 0, 0.1)'
                                },
                                grid: {
                                    color: isDark ? 'rgba(255, 255, 255, 0.1)' : 'rgba(0, 0, 0, 0.1)'
                                },
                                pointLabels: {
                                    color: textColor,
                                    font: {
                                        size: 12
                                    }
                                },
                                ticks: {
                                    backdropColor: 'transparent',
                                    color: textColor
                                }
                            }
                        },
                        plugins: {
                            legend: {
                                labels: {
                                    color: textColor
                                }
                            }
                        }
                    }
                });
            }
            
            function updateChart() {
                if (skillsChart) {
                    skillsChart.destroy();
                }
                initChart();
            }
            
            // 初始化图表
            initChart();
            
            // 表单提交处理
            const contactForm = document.getElementById('contact-form');
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                // 这里可以添加表单提交逻辑
                alert('Message sent successfully! (This is a demo - no actual email is sent)');
                contactForm.reset();
            });
            
            // 滚动时导航栏样式变化
            window.addEventListener('scroll', function() {
                const header = document.querySelector('header');
                if (window.scrollY > 50) {
                    header.classList.add('shadow-md');
                } else {
                    header.classList.remove('shadow-md');
                }
            });
        });
    </script>
</body>
</html>
