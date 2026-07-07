<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yogesh Sonawane | Full Stack Developer</title>
    
    <!-- Custom CSS Link -->
    <link rel="stylesheet" href="style.css">

    <!-- Tailwind CSS (via CDN) -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    keyframes: {
                        wave: {
                            '0%, 100%': { transform: 'rotate(0.0deg)' },
                            '10%, 30%': { transform: 'rotate(14.0deg)' },
                            '20%': { transform: 'rotate(-8.0deg)' },
                            '40%': { transform: 'rotate(-4.0deg)' },
                            '50%': { transform: 'rotate(10.0deg)' },
                            '60%': { transform: 'rotate(0.0deg)' },
                        },
                        float: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-15px)' },
                        }
                    },
                    animation: {
                        'wave': 'wave 2.5s infinite transform-origin-[70%_70%]',
                        'float': 'float 5s ease-in-out infinite',
                    }
                }
            }
        }
    </script>

    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- AOS CSS for Scroll Animations -->
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <style>
        /* style.css */

/* Base transition for dark mode toggling */
body { 
    transition: background-color 0.3s ease, color 0.3s ease; 
}

/* Technical Skill Icons Hover Animation */
.tech-icon { 
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1); 
    cursor: pointer; 
}

.tech-icon:hover { 
    transform: scale(1.15) translateY(-5px); 
    filter: drop-shadow(0 10px 8px rgba(147, 51, 234, 0.2)); 
}

/* Social Buttons Hover Animation */
.social-btn {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 3rem;
    height: 3rem;
    background-color: white;
    color: #475569; /* slate-600 */
    border-radius: 9999px;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
    transition: all 0.3s ease;
}

.dark .social-btn {
    background-color: #1e293b; /* slate-800 */
    color: #cbd5e1; /* slate-300 */
}

.social-btn:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
}

/* Custom Scrollbar for a Premium Feel */
::-webkit-scrollbar { 
    width: 8px; 
}

::-webkit-scrollbar-track { 
    background: transparent; 
}

::-webkit-scrollbar-thumb { 
    background: #d8b4fe; 
    border-radius: 4px; 
}

.dark ::-webkit-scrollbar-thumb { 
    background: #6b21a8; 
}
    </style>
</head>
<body class="bg-slate-50 text-slate-800 dark:bg-slate-900 dark:text-slate-100 antialiased selection:bg-purple-300 selection:text-purple-900">

    <!-- 1. NAVIGATION BAR -->
    <nav class="fixed w-full top-0 z-50 backdrop-blur-xl bg-white/70 dark:bg-slate-900/80 border-b border-purple-100 dark:border-slate-800 shadow-sm">
        <div class="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center">
            <div class="text-2xl font-bold font-mono text-transparent bg-clip-text bg-gradient-to-r from-purple-600 to-indigo-500" data-aos="fade-right">
                &lt;Yogesh.dev /&gt;
            </div>
            <div class="hidden md:flex items-center space-x-8 font-semibold text-sm tracking-wide">
                <a href="#skills" class="hover:text-purple-600 dark:hover:text-purple-400 transition-colors">SKILLS</a>
                <a href="#experience" class="hover:text-purple-600 dark:hover:text-purple-400 transition-colors">EXPERIENCE</a>
                <a href="#projects" class="hover:text-purple-600 dark:hover:text-purple-400 transition-colors">PROJECTS</a>
                <a href="#education" class="hover:text-purple-600 dark:hover:text-purple-400 transition-colors">EDUCATION</a>
                <a href="#contact" class="hover:text-purple-600 dark:hover:text-purple-400 transition-colors">CONTACT</a>
                <button id="theme-toggle" class="p-2 rounded-full hover:bg-purple-50 dark:hover:bg-slate-800 transition-colors border border-transparent hover:border-purple-200 dark:hover:border-slate-700">
                    <i id="theme-icon" class="fas fa-moon text-purple-600 dark:text-yellow-400 text-lg"></i>
                </button>
            </div>
        </div>
    </nav>

    <main class="max-w-7xl mx-auto px-6 pt-24">
        
        <!-- 2. HERO SECTION -->
        <section class="min-h-[85vh] flex flex-col-reverse lg:flex-row items-center justify-center py-10 gap-16">
            <div class="flex-1 space-y-8" data-aos="fade-up">
                <div class="space-y-2">
                    <h1 class="text-5xl md:text-7xl font-extrabold tracking-tight text-slate-900 dark:text-white">
                        Hi all, I'm Yogesh <span class="inline-block origin-[70%_70%] animate-wave cursor-pointer">👋</span>
                    </h1>
                    <h2 class="text-2xl md:text-3xl font-bold text-slate-600 dark:text-slate-400">
                        I build <span class="text-transparent bg-clip-text bg-gradient-to-r from-purple-600 to-indigo-500">scalable enterprise apps.</span>
                    </h2>
                </div>
                
                <p class="text-lg md:text-xl text-slate-600 dark:text-slate-300 leading-relaxed max-w-2xl">
                    Full Stack Developer with 3+ years of experience building scalable enterprise applications using ASP.NET Core, React.js, and SQL Server. Skilled in developing ASP.NET Core Web Services, Microservices, secure RESTful APIs, and Clean Architecture solutions using CQRS and MediatR.
                </p>
                
                <!-- Social Links Grid -->
                <div class="flex flex-wrap gap-4 pt-2">
                    <a href="https://github.com/YogeshSonawane1311" target="_blank" class="social-btn hover:text-purple-600 dark:hover:text-purple-400">
                        <i class="fab fa-github fa-xl"></i>
                    </a>
                    <a href="https://linkedin.com/in/yogeshss1311" target="_blank" class="social-btn hover:text-blue-600 dark:hover:text-blue-400">
                        <i class="fab fa-linkedin-in fa-xl"></i>
                    </a>
                    <a href="https://leetcode.com/u/YogeshSonawane1311/" target="_blank" class="social-btn hover:text-yellow-600 dark:hover:text-yellow-500">
                        <!-- Custom LeetCode SVG -->
                        <svg viewBox="0 0 24 24" width="20" height="20" fill="currentColor"><path d="M16.102 17.93l-2.697 2.607c-.466.467-1.111.662-1.823.662s-1.357-.195-1.824-.662l-4.332-4.363c-.467-.467-.702-1.15-.702-1.863s.235-1.357.702-1.824l4.319-4.38c.467-.467 1.125-.645 1.837-.645s1.357.195 1.823.662l2.697 2.606c.514.515 1.365.497 1.9-.038.535-.536.553-1.387.039-1.901l-2.609-2.636a5.055 5.055 0 0 0-2.445-1.337l2.467-2.503c.516-.514.498-1.366-.037-1.901-.535-.535-1.387-.552-1.902-.038l-10.1 10.101c-.981.982-1.494 2.337-1.494 3.835 0 1.498.513 2.895 1.494 3.875l4.347 4.361c.981.979 2.337 1.452 3.834 1.452s2.853-.473 3.833-1.452l2.697-2.607c.514-.515.496-1.366-.039-1.901-.534-.535-1.386-.553-1.9-.039zM20.811 13.01H10.666c-.702 0-1.27.604-1.27 1.346s.568 1.346 1.27 1.346h10.145c.701 0 1.27-.604 1.27-1.346s-.569-1.346-1.27-1.346z"/></svg>
                    </a>
                    <a href="mailto:yogeshsonawane1311@gmail.com" class="social-btn hover:text-red-500">
                        <i class="fas fa-envelope fa-xl"></i>
                    </a>
                </div>

                <div class="flex flex-wrap gap-4 pt-6">
                    <a href="#contact" class="px-8 py-3.5 bg-purple-600 hover:bg-purple-700 text-white font-bold rounded-lg shadow-lg hover:shadow-purple-500/40 transition-all flex items-center gap-2">
                        Let's Talk <i class="fas fa-arrow-right"></i>
                    </a>
                    <a href="/resume.pdf" class="px-8 py-3.5 bg-white dark:bg-slate-800 border-2 border-purple-100 dark:border-slate-700 text-purple-600 dark:text-purple-400 font-bold rounded-lg hover:border-purple-600 dark:hover:border-purple-400 transition-all flex items-center gap-2 shadow-sm">
                        <i class="fas fa-download"></i> Resume
                    </a>
                </div>
            </div>

            <div class="flex-1 flex justify-center lg:justify-end animate-float">
                <svg class="w-full max-w-lg drop-shadow-2xl" viewBox="0 0 500 450" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <circle cx="250" cy="225" r="180" class="fill-purple-100 dark:fill-purple-900/20" />
                    <rect x="80" y="120" width="340" height="220" rx="12" class="fill-white dark:fill-slate-800 stroke-purple-200 dark:stroke-slate-700" stroke-width="4"/>
                    <circle cx="110" cy="145" r="6" fill="#ef4444" />
                    <circle cx="130" cy="145" r="6" fill="#eab308" />
                    <circle cx="150" cy="145" r="6" fill="#22c55e" />
                    <rect x="110" y="180" width="180" height="12" rx="6" class="fill-slate-200 dark:fill-slate-700" />
                    <rect x="110" y="210" width="240" height="12" rx="6" class="fill-slate-200 dark:fill-slate-700" />
                    <rect x="110" y="240" width="140" height="12" rx="6" fill="#9333ea" />
                    <!-- Code Blocks -->
                    <path d="M350 200 L370 220 L350 240" stroke="#a855f7" stroke-width="6" stroke-linecap="round" stroke-linejoin="round"/>
                    <path d="M330 240 L310 220 L330 200" stroke="#a855f7" stroke-width="6" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
            </div>
        </section>

        <!-- 3. SKILLS & ARCHITECTURE -->
        <section id="skills" class="py-24 relative">
            <div class="absolute inset-0 bg-purple-50 dark:bg-slate-800/30 -skew-y-3 z-0"></div>
            <div class="relative z-10">
                <div class="text-center mb-16" data-aos="fade-up">
                    <h2 class="text-4xl md:text-5xl font-extrabold mb-4">Technical Expertise</h2>
                    <p class="text-xl text-purple-600 dark:text-purple-400 font-semibold tracking-wide uppercase">
                        Architecting Microservices & Intelligent Systems
                    </p>
                </div>

                <div class="grid lg:grid-cols-12 gap-12 items-center">
                    <!-- Tech Grid -->
                    <div class="lg:col-span-5 grid grid-cols-4 gap-6 text-5xl text-slate-400" data-aos="fade-right">
                        <div class="tech-icon hover:text-[#512BD4] flex flex-col items-center gap-2"><i class="fab fa-microsoft"></i><span class="text-xs font-bold">.NET Core</span></div>
                        <div class="tech-icon hover:text-[#61DAFB] flex flex-col items-center gap-2"><i class="fab fa-react"></i><span class="text-xs font-bold">React</span></div>
                        <div class="tech-icon hover:text-[#3178C6] flex flex-col items-center gap-2"><i class="fab fa-js"></i><span class="text-xs font-bold">TS/JS</span></div>
                        <div class="tech-icon hover:text-[#CC2927] flex flex-col items-center gap-2"><i class="fas fa-database"></i><span class="text-xs font-bold">SQL Server</span></div>
                        <div class="tech-icon hover:text-[#FF9900] flex flex-col items-center gap-2"><i class="fab fa-aws"></i><span class="text-xs font-bold">AWS</span></div>
                        <div class="tech-icon hover:text-[#2496ED] flex flex-col items-center gap-2"><i class="fab fa-docker"></i><span class="text-xs font-bold">Docker</span></div>
                        <div class="tech-icon hover:text-[#3776AB] flex flex-col items-center gap-2"><i class="fab fa-python"></i><span class="text-xs font-bold">Python</span></div>
                        <div class="tech-icon hover:text-[#6e5494] flex flex-col items-center gap-2"><i class="fab fa-git-alt"></i><span class="text-xs font-bold">Git/CI-CD</span></div>
                    </div>

                    <!-- Deeper Skill Descriptions -->
                    <div class="lg:col-span-7 space-y-6 bg-white dark:bg-slate-900 p-8 rounded-2xl shadow-xl border border-slate-100 dark:border-slate-800" data-aos="fade-left">
                        <div class="flex gap-5 items-start">
                            <div class="bg-purple-100 dark:bg-purple-900/40 p-3 rounded-lg text-purple-600 dark:text-purple-400 mt-1">
                                <i class="fas fa-network-wired fa-lg"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-lg">Backend & Microservices</h4>
                                <p class="text-slate-600 dark:text-slate-400 mt-1 text-sm">Building distributed systems using ASP.NET Core Web API, MVC, EF Core, and ADO.NET. Deeply experienced in Clean Architecture, CQRS, MediatR, Repository Pattern, and Dependency Injection.</p>
                            </div>
                        </div>
                        
                        <div class="flex gap-5 items-start">
                            <div class="bg-blue-100 dark:bg-blue-900/40 p-3 rounded-lg text-blue-600 dark:text-blue-400 mt-1">
                                <i class="fas fa-shield-alt fa-lg"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-lg">Security & API Development</h4>
                                <p class="text-slate-600 dark:text-slate-400 mt-1 text-sm">Designing secure RESTful APIs with JWT Authentication, Role-Based Access Control (RBAC), and OpenAPI/Swagger documentation. Integrating external APIs and Firebase Cloud Messaging (FCM).</p>
                            </div>
                        </div>

                        <div class="flex gap-5 items-start">
                            <div class="bg-green-100 dark:bg-green-900/40 p-3 rounded-lg text-green-600 dark:text-green-400 mt-1">
                                <i class="fas fa-robot fa-lg"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-lg">Cloud, DevOps & AI Tooling</h4>
                                <p class="text-slate-600 dark:text-slate-400 mt-1 text-sm">Containerizing with Docker, managing CI/CD via Azure DevOps, and architecting on AWS (Lambda, S3, Cognito). Leveraging AI tools like GitHub Copilot, Codex, and Cursor for rapid development.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 4. PROFESSIONAL EXPERIENCE -->
        <section id="experience" class="py-24">
            <h2 class="text-4xl md:text-5xl font-extrabold text-center mb-16" data-aos="fade-up">Professional Journey</h2>
            
            <div class="max-w-4xl mx-auto relative">
                <!-- Vertical Line -->
                <div class="absolute left-[28px] md:left-[39px] top-4 bottom-4 w-1 bg-gradient-to-b from-purple-600 to-indigo-100 dark:to-slate-800 rounded-full"></div>

                <!-- Role 1 -->
                <div class="relative pl-20 pr-4 py-6" data-aos="fade-up">
                    <div class="absolute left-4 md:left-[27.5px] top-8 w-6 h-6 bg-purple-600 rounded-full border-4 border-white dark:border-slate-900 shadow-md"></div>
                    <div class="bg-white dark:bg-slate-800 p-8 rounded-2xl shadow-md border border-slate-100 dark:border-slate-700 hover:shadow-xl transition-shadow">
                        <div class="flex flex-col md:flex-row md:justify-between md:items-center mb-4 gap-2">
                            <div>
                                <h3 class="text-2xl font-bold">Junior Software Developer</h3>
                                <p class="text-purple-600 dark:text-purple-400 font-bold">PRM Soft Solution Pvt. Ltd. <span class="text-slate-400 font-normal">| Pune, MH</span></p>
                            </div>
                            <span class="inline-block px-4 py-1 bg-purple-100 dark:bg-purple-900/30 text-purple-700 dark:text-purple-300 rounded-full text-sm font-bold whitespace-nowrap">Dec 2024 – Present</span>
                        </div>
                        <ul class="list-none space-y-3 text-slate-700 dark:text-slate-300">
                            <li class="flex items-start gap-3"><i class="fas fa-check-circle text-purple-500 mt-1"></i> <span>Developed and maintained scalable ASP.NET Core Web Services using Microservices Architecture for enterprise business applications.</span></li>
                            <li class="flex items-start gap-3"><i class="fas fa-check-circle text-purple-500 mt-1"></i> <span>Designed and implemented secure RESTful APIs with JWT Authentication and Role-Based Access Control (RBAC) for distributed systems.</span></li>
                            <li class="flex items-start gap-3"><i class="fas fa-check-circle text-purple-500 mt-1"></i> <span>Applied Clean Architecture, CQRS, MediatR, and Dependency Injection to improve code quality, scalability, and maintainability.</span></li>
                            <li class="flex items-start gap-3"><i class="fas fa-check-circle text-purple-500 mt-1"></i> <span>Optimized SQL Server and EF Core queries, reducing API response times by 20–30% and improving application performance.</span></li>
                            <li class="flex items-start gap-3"><i class="fas fa-check-circle text-purple-500 mt-1"></i> <span>Integrated React.js frontends with backend APIs and implemented OpenAI APIs and Firebase Cloud Messaging (FCM) for AI-powered features and real-time notifications.</span></li>
                            <li class="flex items-start gap-3"><i class="fas fa-check-circle text-purple-500 mt-1"></i> <span>Containerized services using Docker and supported deployments through Azure DevOps CI/CD and AWS, improving deployment consistency and release efficiency.</span></li>
                            <li class="flex items-start gap-3"><i class="fas fa-check-circle text-purple-500 mt-1"></i> <span>Collaborated with cross-functional Agile teams to deliver 20+ production features, ensuring timely releases and high-quality software delivery.</span></li>
                        </ul>
                    </div>
                </div>

                <!-- Role 2 -->
                <div class="relative pl-20 pr-4 py-6" data-aos="fade-up">
                    <div class="absolute left-4 md:left-[27.5px] top-8 w-6 h-6 bg-slate-400 dark:bg-slate-600 rounded-full border-4 border-white dark:border-slate-900"></div>
                    <div class="bg-white dark:bg-slate-800 p-8 rounded-2xl shadow-sm border border-slate-100 dark:border-slate-700 hover:shadow-md transition-shadow opacity-90">
                        <div class="flex flex-col md:flex-row md:justify-between md:items-center mb-4 gap-2">
                            <div>
                                <h3 class="text-2xl font-bold">Junior Software Developer</h3>
                                <p class="text-slate-600 dark:text-slate-400 font-bold">Sandeep Venture Pvt Ltd <span class="text-slate-400 font-normal">| Pune, MH</span></p>
                            </div>
                            <span class="inline-block px-4 py-1 bg-slate-100 dark:bg-slate-700 text-slate-600 dark:text-slate-300 rounded-full text-sm font-bold whitespace-nowrap">Jun 2023 – Nov 2024</span>
                        </div>
                        <ul class="list-none space-y-3 text-slate-700 dark:text-slate-300">
                            <li class="flex items-start gap-3"><i class="fas fa-caret-right text-slate-400 mt-1"></i> <span>Developed and maintained a full-stack FinTech billing application using ASP.NET Core and SQL Server to manage invoicing, financial transactions, and client ledger data.</span></li>
                            <li class="flex items-start gap-3"><i class="fas fa-caret-right text-slate-400 mt-1"></i> <span>Developed interactive React.js dashboards with real-time financial visualizations, improving business reporting and decision-making.</span></li>
                            <li class="flex items-start gap-3"><i class="fas fa-caret-right text-slate-400 mt-1"></i> <span>Resolved critical production issues, refactored legacy modules, and optimized SQL Server queries to improve system performance and reliability.</span></li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <!-- 5. FEATURED PROJECTS -->
        <section id="projects" class="py-24">
            <h2 class="text-4xl md:text-5xl font-extrabold text-center mb-16" data-aos="fade-up">Engineering Portfolio</h2>

            <div class="grid md:grid-cols-2 gap-8">
                <!-- Project 1 -->
                <div class="group bg-white dark:bg-slate-800 rounded-2xl shadow-lg border border-slate-100 dark:border-slate-700 overflow-hidden hover:-translate-y-2 transition-all duration-300" data-aos="fade-up">
                    <div class="h-2 bg-gradient-to-r from-purple-600 to-blue-500"></div>
                    <div class="p-8 h-full flex flex-col">
                        <div class="flex justify-between items-start mb-4">
                            <h3 class="text-2xl font-bold group-hover:text-purple-600 dark:group-hover:text-purple-400 transition-colors">Crowdsourcing Platform</h3>
                            <a href="#" class="text-slate-400 hover:text-purple-600 transition-colors"><i class="fab fa-github fa-lg"></i></a>
                        </div>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 text-xs font-bold rounded-md">.NET 8 Web API</span>
                            <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 text-xs font-bold rounded-md">Microservices</span>
                            <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 text-xs font-bold rounded-md">React.js</span>
                            <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 text-xs font-bold rounded-md">Docker</span>
                        </div>
                        <ul class="text-sm text-slate-600 dark:text-slate-300 flex-grow leading-relaxed space-y-2 list-disc list-inside">
                            <li>Developed a full-stack crowdsourcing platform using React.js and ASP.NET Core Web APIs following Microservices and Clean Architecture.</li>
                            <li>Implemented JWT Authentication, Refresh Tokens, RBAC, global exception handling, and user-context middleware.</li>
                            <li>Built RESTful APIs with EF Core and the Repository Pattern, enabling efficient task management.</li>
                            <li>Integrated SHA-256 cryptographic hashing to provide tamper-resistant data validation and integrity.</li>
                        </ul>
                    </div>
                </div>

                <!-- Project 2 -->
                <div class="group bg-white dark:bg-slate-800 rounded-2xl shadow-lg border border-slate-100 dark:border-slate-700 overflow-hidden hover:-translate-y-2 transition-all duration-300" data-aos="fade-up" data-aos-delay="100">
                    <div class="h-2 bg-gradient-to-r from-emerald-500 to-teal-500"></div>
                    <div class="p-8 h-full flex flex-col">
                        <div class="flex justify-between items-start mb-4">
                            <h3 class="text-2xl font-bold group-hover:text-emerald-600 dark:group-hover:text-emerald-400 transition-colors">AI-Based Industrial Robot Fault Detection</h3>
                            <a href="#" class="text-slate-400 hover:text-emerald-600 transition-colors"><i class="fab fa-github fa-lg"></i></a>
                        </div>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 text-xs font-bold rounded-md">Python</span>
                            <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 text-xs font-bold rounded-md">Scikit-learn</span>
                            <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 text-xs font-bold rounded-md">XGBoost</span>
                            <span class="px-3 py-1 bg-slate-100 dark:bg-slate-700 text-xs font-bold rounded-md">Pandas</span>
                        </div>
                        <ul class="text-sm text-slate-600 dark:text-slate-300 flex-grow leading-relaxed space-y-2 list-disc list-inside">
                            <li>Developed a machine learning model to classify industrial robot faults using 50,000+ sensor records.</li>
                            <li>Performed data preprocessing, feature engineering, and exploratory data analysis (EDA) using Pandas, NumPy, Matplotlib, and Seaborn.</li>
                            <li>Trained and evaluated Random Forest, XGBoost, and Logistic Regression models using Scikit-learn.</li>
                            <li>Built an end-to-end ML pipeline for fault prediction and feature importance analysis for predictive maintenance.</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <!-- 6. EDUCATION & PUBLICATIONS -->
        <section id="education" class="py-24">
            <h2 class="text-4xl md:text-5xl font-extrabold text-center mb-16" data-aos="fade-up">Education & Publications</h2>

            <div class="max-w-4xl mx-auto">
                <div class="bg-gradient-to-br from-purple-700 to-indigo-900 text-white p-10 rounded-3xl shadow-2xl relative overflow-hidden flex flex-col justify-center" data-aos="zoom-in">
                    <div class="absolute -right-10 -bottom-10 opacity-10">
                        <i class="fas fa-university text-[250px]"></i>
                    </div>
                    <div class="relative z-10 space-y-6">
                        <span class="uppercase tracking-widest text-purple-200 font-bold text-sm">Formal Degree</span>
                        <h3 class="text-3xl md:text-4xl font-extrabold leading-tight">Bachelor of Engineering in Computer Engineering</h3>
                        <p class="text-xl text-purple-100">Shri Chhatrapati Shivaji Maharaj College of Engineering (SPPU) | Ahilyanagar</p>
                        <p class="font-mono bg-black/20 inline-block px-4 py-1.5 rounded-md font-semibold text-purple-50">Aug 2019 – July 2023</p>
                        
                        <div class="pt-6 border-t border-white/10 space-y-4">
                            <p class="font-medium text-lg flex items-center gap-3"><i class="fas fa-star text-yellow-400"></i> CGPA: 8.55/10</p>
                            <p class="font-medium flex items-start gap-3"><i class="fas fa-book-open text-purple-300 mt-1"></i> 
                                <span>
                                    <strong>IEEE Publication (2023):</strong> 
                                    <a href="https://ieeexplore.ieee.org/abstract/document/10151512" target="_blank" class="underline underline-offset-4 hover:text-purple-300 transition-colors">
                                        "Enriching Trustworthy Trade Decentralized Systems Using Blockchain" <i class="fas fa-external-link-alt text-sm ml-1"></i>
                                    </a>
                                </span>
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 7. CONTACT -->
        <section id="contact" class="py-24 border-t border-slate-200 dark:border-slate-800">
            <div class="bg-purple-600 dark:bg-slate-800 rounded-3xl p-10 md:p-16 shadow-2xl overflow-hidden relative" data-aos="fade-up">
                <!-- Decorative Background Circles -->
                <div class="absolute top-0 right-0 w-64 h-64 bg-white/10 rounded-full blur-3xl -translate-y-1/2 translate-x-1/3"></div>
                <div class="absolute bottom-0 left-0 w-64 h-64 bg-black/10 rounded-full blur-3xl translate-y-1/2 -translate-x-1/3"></div>
                
                <div class="grid md:grid-cols-2 gap-12 items-center relative z-10">
                    <div class="space-y-6 text-white">
                        <h2 class="text-4xl md:text-5xl font-bold">Let's build something great.</h2>
                        <p class="text-lg text-purple-100 max-w-md">
                            Whether you want to discuss a project, enterprise architecture, or just want to say hi, my inbox is always open.
                        </p>
                        
                        <div class="space-y-4 pt-4">
                            <a href="tel:7620157708" class="flex items-center gap-4 group">
                                <div class="p-3 bg-white/10 rounded-lg group-hover:bg-white/20 transition-colors">
                                    <i class="fas fa-phone-alt"></i>
                                </div>
                                <span class="text-lg font-medium">+91 7620157708</span>
                            </a>
                            <a href="mailto:yogeshsonawane1311@gmail.com" class="flex items-center gap-4 group">
                                <div class="p-3 bg-white/10 rounded-lg group-hover:bg-white/20 transition-colors">
                                    <i class="fas fa-envelope"></i>
                                </div>
                                <span class="text-lg font-medium">yogeshsonawane1311@gmail.com</span>
                            </a>
                            <div class="flex items-center gap-4">
                                <div class="p-3 bg-white/10 rounded-lg">
                                    <i class="fas fa-map-marker-alt"></i>
                                </div>
                                <span class="text-lg font-medium">Pune, Maharashtra</span>
                            </div>
                        </div>
                    </div>

                    <div class="flex justify-center md:justify-end">
                        <div class="bg-white dark:bg-slate-900 p-8 rounded-2xl shadow-xl max-w-sm w-full text-center space-y-6">
                            <h3 class="text-2xl font-bold text-slate-800 dark:text-white">Connect Quickly</h3>
                            <div class="flex justify-center gap-4">
                                <a href="https://linkedin.com/in/yogeshss1311" class="w-12 h-12 rounded-full bg-blue-100 text-blue-600 flex items-center justify-center hover:scale-110 transition-transform"><i class="fab fa-linkedin-in fa-lg"></i></a>
                                <a href="https://github.com/YogeshSonawane1311" class="w-12 h-12 rounded-full bg-slate-100 dark:bg-slate-700 text-slate-800 dark:text-white flex items-center justify-center hover:scale-110 transition-transform"><i class="fab fa-github fa-lg"></i></a>
                                <a href="https://leetcode.com/u/YogeshSonawane1311/" class="w-12 h-12 rounded-full bg-yellow-100 text-yellow-600 flex items-center justify-center hover:scale-110 transition-transform"><i class="fas fa-code fa-lg"></i></a>
                            </div>
                            <a href="mailto:yogeshsonawane1311@gmail.com" class="block w-full py-3 bg-purple-600 hover:bg-purple-700 text-white font-bold rounded-lg transition-colors">
                                Send an Email
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <!-- FOOTER -->
    <footer class="text-center py-8">
        <p class="text-slate-500 dark:text-slate-400 font-medium text-sm">
            Designed & Built with <span class="text-red-500 animate-pulse inline-block">❤️</span> by Yogesh Sonawane
        </p>
    </footer>

    <!-- AOS Script for Animations -->
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    
    <!-- Custom JavaScript -->
    <script>
        // Initialize Scroll Animations
        AOS.init({
            duration: 800,
            once: true,
            offset: 50,
        });

        // Dark Mode Toggle Logic
        const themeToggleBtn = document.getElementById('theme-toggle');
        const themeIcon = document.getElementById('theme-icon');
        const html = document.documentElement;

        if (localStorage.getItem('theme') === 'dark' || (!('theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
            html.classList.add('dark');
            themeIcon.classList.replace('fa-moon', 'fa-sun');
        }

        themeToggleBtn.addEventListener('click', () => {
            html.classList.toggle('dark');
            if (html.classList.contains('dark')) {
                localStorage.setItem('theme', 'dark');
                themeIcon.classList.replace('fa-moon', 'fa-sun');
                themeIcon.classList.replace('text-purple-600', 'text-yellow-400');
            } else {
                localStorage.setItem('theme', 'light');
                themeIcon.classList.replace('fa-sun', 'fa-moon');
                themeIcon.classList.replace('text-yellow-400', 'text-purple-600');
            }
        });
    </script>
</body>
</html>
