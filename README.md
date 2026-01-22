<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CivicPulse AI - Team Hacker Slayer</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/3.9.1/chart.min.js"></script>

    <style>
        body { font-family: 'Inter', sans-serif; scroll-behavior: smooth; }
        .glass-panel {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        .ai-scan-line {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: #3B82F6;
            box-shadow: 0 0 10px #3B82F6;
            animation: scan 2s infinite linear;
            display: none;
        }
        @keyframes scan {
            0% { top: 0; opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { top: 100%; opacity: 0; }
        }
        .fade-in { animation: fadeIn 0.5s ease-in; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
        
        /* Custom scrollbar for dashboard lists */
        .scrollbar-hide::-webkit-scrollbar {
            display: none;
        }
        .scrollbar-hide {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800">

    <!-- Navigation -->
    <nav class="fixed w-full z-50 bg-white/90 backdrop-blur-md border-b border-slate-200 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <div class="flex items-center space-x-3">
                    <div class="w-8 h-8 bg-blue-600 rounded-lg flex items-center justify-center text-white font-bold">
                        <i class="fa-solid fa-city"></i>
                    </div>
                    <span class="text-xl font-bold tracking-tight text-slate-900">CivicPulse<span class="text-blue-600">AI</span></span>
                </div>
                <div class="hidden md:flex space-x-8 text-sm font-medium">
                    <a href="#home" class="text-slate-600 hover:text-blue-600 transition">Overview</a>
                    <a href="#differentiators" class="text-slate-600 hover:text-blue-600 transition">Why Us?</a>
                    <a href="#tech-stack" class="text-slate-600 hover:text-blue-600 transition">Google Tech Stack</a>
                    <a href="#future" class="text-slate-600 hover:text-blue-600 transition">Roadmap</a>
                </div>
                <div>
                    <button onclick="scrollToDemo()" class="bg-blue-600 hover:bg-blue-700 text-white px-5 py-2 rounded-full text-sm font-medium transition shadow-md flex items-center gap-2">
                        <i class="fa-solid fa-camera"></i> Live Demo
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="pt-32 pb-20 bg-gradient-to-br from-slate-50 via-blue-50 to-white overflow-hidden relative">
        <div class="absolute top-0 right-0 w-1/3 h-full bg-blue-100/30 skew-x-12 transform origin-top-right"></div>
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <div class="inline-block px-3 py-1 bg-blue-100 text-blue-700 rounded-full text-xs font-semibold tracking-wide mb-4">TEAM HACKER SLAYER</div>
                <h1 class="text-4xl md:text-6xl font-bold text-slate-900 mb-6 leading-tight">
                    Transforming Civic Participation into <br> <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-600 to-indigo-600">Actionable Governance.</span>
                </h1>
                <p class="text-lg text-slate-600 mb-8 leading-relaxed">
                    A computer vision-based infrastructure reporting system. We don't just collect complaints; we verify them with AI, enforce SLA accountability, and ensure resolution with "Proof of Fix" validation.
                </p>
                <div class="flex flex-col sm:flex-row justify-center gap-4">
                    <button onclick="scrollToDemo()" class="bg-slate-900 text-white px-8 py-3.5 rounded-lg font-medium hover:bg-slate-800 transition shadow-lg flex items-center justify-center gap-2">
                        Try the MVP <i class="fa-solid fa-arrow-right"></i>
                    </button>
                    <button onclick="document.getElementById('differentiators').scrollIntoView()" class="bg-white text-slate-700 border border-slate-300 px-8 py-3.5 rounded-lg font-medium hover:bg-slate-50 transition flex items-center justify-center gap-2">
                        See Our Edge
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Key Differentiators Section (From PDF Page 3) -->
    <section id="differentiators" class="py-16 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-slate-900">How We Are Different</h2>
                <p class="text-slate-500 mt-2">Moving beyond simple complaint collection.</p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Diff 1 -->
                <div class="p-6 bg-slate-50 rounded-2xl border border-slate-100 hover:shadow-lg transition">
                    <div class="w-12 h-12 bg-blue-100 text-blue-600 rounded-xl flex items-center justify-center mb-4 text-xl">
                        <i class="fa-solid fa-bolt"></i>
                    </div>
                    <h3 class="font-bold text-lg mb-2">Action-Oriented</h3>
                    <p class="text-slate-600 text-sm">We don't stop at detection. Verified issues are instantly converted into official, SLA-bound maintenance tickets with auto-escalation.</p>
                </div>
                <!-- Diff 2 -->
                <div class="p-6 bg-slate-50 rounded-2xl border border-slate-100 hover:shadow-lg transition">
                    <div class="w-12 h-12 bg-purple-100 text-purple-600 rounded-xl flex items-center justify-center mb-4 text-xl">
                        <i class="fa-solid fa-shield-halved"></i>
                    </div>
                    <h3 class="font-bold text-lg mb-2">Trust & Verification Layer</h3>
                    <p class="text-slate-600 text-sm">Prevents spam and fake reports using AI-based image verification, GPS fencing, timestamp validation, and duplicate detection.</p>
                </div>
                <!-- Diff 3 -->
                <div class="p-6 bg-slate-50 rounded-2xl border border-slate-100 hover:shadow-lg transition">
                    <div class="w-12 h-12 bg-green-100 text-green-600 rounded-xl flex items-center justify-center mb-4 text-xl">
                        <i class="fa-solid fa-rotate-right"></i>
                    </div>
                    <h3 class="font-bold text-lg mb-2">End-to-End Accountability</h3>
                    <p class="text-slate-600 text-sm">A ticket cannot be closed without an "After-Fix" image, which is re-verified by AI to ensure the problem is genuinely solved.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Google Tech Stack Section (From PDF Page 5) -->
    <section id="tech-stack" class="py-20 bg-slate-50 border-y border-slate-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold text-slate-900">Built on Google Cloud</h2>
                <p class="text-slate-500 mt-2">Leveraging the full ecosystem for scalability.</p>
            </div>
            
            <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
                <!-- Stack Item 1 -->
                <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-100 text-center">
                    <i class="fa-solid fa-mobile-screen text-3xl text-blue-600 mb-3"></i>
                    <h4 class="font-bold text-slate-800">Google AppSheet</h4>
                    <p class="text-xs text-slate-500 mt-2">No-code mobile app for citizens & officers.</p>
                </div>
                <!-- Stack Item 2 -->
                <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-100 text-center">
                    <i class="fa-solid fa-eye text-3xl text-red-500 mb-3"></i>
                    <h4 class="font-bold text-slate-800">Cloud Vision AI</h4>
                    <p class="text-xs text-slate-500 mt-2">Fake detection, severity analysis & comparison.</p>
                </div>
                <!-- Stack Item 3 -->
                <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-100 text-center">
                    <i class="fa-solid fa-map-location text-3xl text-green-600 mb-3"></i>
                    <h4 class="font-bold text-slate-800">Maps Platform</h4>
                    <p class="text-xs text-slate-500 mt-2">GPS capture, issue pinning & area visualization.</p>
                </div>
                <!-- Stack Item 4 -->
                <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-100 text-center">
                    <i class="fa-solid fa-chart-line text-3xl text-yellow-500 mb-3"></i>
                    <h4 class="font-bold text-slate-800">Looker Studio</h4>
                    <p class="text-xs text-slate-500 mt-2">Public transparency dashboard & analytics.</p>
                </div>
                 <!-- Stack Item 5 -->
                 <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-100 text-center">
                    <i class="fa-brands fa-google text-3xl text-purple-600 mb-3"></i>
                    <h4 class="font-bold text-slate-800">Google Forms</h4>
                    <p class="text-xs text-slate-500 mt-2">Simplified citizen complaint submission.</p>
                </div>
                 <!-- Stack Item 6 -->
                 <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-100 text-center">
                    <i class="fa-solid fa-database text-3xl text-orange-600 mb-3"></i>
                    <h4 class="font-bold text-slate-800">Firestore</h4>
                    <p class="text-xs text-slate-500 mt-2">Real-time database for ticket tracking.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Main Application Demo Section -->
    <section id="dashboard-demo" class="py-20 bg-white min-h-screen">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-end mb-8">
                <div>
                    <h2 class="text-3xl font-bold text-slate-900">Live MVP Demo</h2>
                    <p class="text-slate-500">Experience the report-to-resolution flow.</p>
                </div>
                
                <!-- Toggle View Buttons -->
                <div class="bg-slate-100 p-1 rounded-lg shadow-inner border border-slate-200 inline-flex mt-4 md:mt-0">
                    <button onclick="switchView('citizen')" id="btn-citizen" class="px-6 py-2 rounded-md text-sm font-medium bg-white text-slate-900 shadow-sm transition">
                        <i class="fa-solid fa-user mr-2"></i> Citizen View
                    </button>
                    <button onclick="switchView('authority')" id="btn-authority" class="px-6 py-2 rounded-md text-sm font-medium text-slate-500 hover:text-slate-900 transition">
                        <i class="fa-solid fa-user-shield mr-2"></i> Official View
                    </button>
                </div>
            </div>

            <!-- VIEW 1: CITIZEN REPORTING APP -->
            <div id="view-citizen" class="fade-in max-w-md mx-auto bg-slate-900 rounded-3xl shadow-2xl overflow-hidden border border-slate-800">
                <div class="bg-slate-800 p-6 text-white text-center relative border-b border-slate-700">
                    <h3 class="font-bold text-lg">Report Issue</h3>
                    <p class="text-slate-400 text-xs mt-1"><i class="fa-solid fa-location-dot mr-1"></i> GPS Locked: 26.8467, 80.9462</p>
                </div>

                <div class="p-6 bg-slate-900">
                    <!-- Upload Area -->
                    <input type="file" id="file-upload" class="hidden" accept="image/*" capture="environment" onchange="handleImageUpload(event)">
                    <div class="mb-6 relative group cursor-pointer" onclick="triggerScan()">
                        <div id="upload-placeholder" class="border-2 border-dashed border-slate-700 rounded-xl bg-slate-800/50 h-64 flex flex-col items-center justify-center text-slate-500 group-hover:border-blue-500 group-hover:text-blue-500 transition">
                            <i class="fa-solid fa-camera text-4xl mb-3"></i>
                            <span class="text-sm font-medium">Take Photo of Issue</span>
                        </div>
                        
                        <!-- Simulated Image Result -->
                        <div id="image-preview" class="hidden h-64 w-full bg-black rounded-xl relative overflow-hidden">
                            <img id="preview-img" src="" alt="Uploaded Issue" class="w-full h-full object-cover opacity-80">
                            <div id="scanner" class="ai-scan-line"></div>
                            
                            <!-- AI Overlay Tags -->
                            <div id="ai-tags" class="absolute bottom-0 left-0 w-full p-4 hidden bg-gradient-to-t from-black/90 to-transparent">
                                <div class="flex gap-2 flex-wrap">
                                    <span class="bg-red-600 text-white text-xs px-2 py-1 rounded font-bold">Severity: HIGH</span>
                                    <span class="bg-blue-600 text-white text-xs px-2 py-1 rounded font-bold">Pothole</span>
                                    <span class="bg-green-600 text-white text-xs px-2 py-1 rounded font-bold"><i class="fa-solid fa-check mr-1"></i>Real Image</span>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Analysis Status -->
                    <div id="analysis-box" class="hidden mb-6 bg-slate-800 p-4 rounded-lg border border-slate-700">
                        <div class="flex items-center justify-between mb-2">
                            <span class="text-xs font-bold text-slate-400 uppercase tracking-wider">Vision AI Analysis</span>
                            <span id="ai-status-text" class="text-xs font-bold text-blue-400 animate-pulse">Processing...</span>
                        </div>
                        <div class="w-full bg-slate-700 rounded-full h-1.5 mb-2">
                            <div id="progress-bar" class="bg-blue-500 h-1.5 rounded-full transition-all duration-[2000ms]" style="width: 0%"></div>
                        </div>
                        <p id="ai-result-text" class="text-xs text-slate-400 mt-2">Verifying metadata & checking duplicates...</p>
                    </div>

                    <!-- Form Inputs (Auto-filled) -->
                    <div id="report-form" class="space-y-4 opacity-50 pointer-events-none transition-opacity duration-500">
                        <div>
                            <label class="block text-xs font-bold text-slate-500 uppercase mb-1">Issue Category</label>
                            <input type="text" value="Road Infrastructure / Pothole" class="w-full bg-slate-800 border border-slate-700 rounded-lg px-3 py-2 text-sm font-medium text-white focus:outline-none" readonly>
                        </div>
                        <button onclick="submitReport()" id="submit-btn" class="w-full bg-blue-600 hover:bg-blue-500 text-white font-bold py-3 rounded-xl shadow-lg shadow-blue-900/50 transition transform active:scale-95">
                            Submit Report
                        </button>
                    </div>

                    <!-- Reset Button -->
                    <button onclick="resetDemo()" id="reset-btn" class="hidden w-full mt-3 border border-slate-700 text-slate-400 font-bold py-3 rounded-xl hover:bg-slate-800 transition">
                        Submit Another
                    </button>
                </div>
            </div>

            <!-- VIEW 2: AUTHORITY DASHBOARD -->
            <div id="view-authority" class="hidden fade-in space-y-6">
                <!-- KPI Cards -->
                <div class="grid grid-cols-1 md:grid-cols-4 gap-4">
                    <div class="bg-white p-5 rounded-xl border border-slate-200 shadow-sm flex items-center justify-between">
                        <div>
                            <p class="text-xs text-slate-500 uppercase font-bold">Total Reports</p>
                            <h3 class="text-2xl font-bold text-slate-800" id="stat-total">1,284</h3>
                        </div>
                        <div class="w-10 h-10 rounded-full bg-blue-50 text-blue-600 flex items-center justify-center"><i class="fa-solid fa-list"></i></div>
                    </div>
                    <div class="bg-white p-5 rounded-xl border border-slate-200 shadow-sm flex items-center justify-between">
                        <div>
                            <p class="text-xs text-slate-500 uppercase font-bold">Pending Fix</p>
                            <h3 class="text-2xl font-bold text-orange-600" id="stat-pending">42</h3>
                        </div>
                        <div class="w-10 h-10 rounded-full bg-orange-50 text-orange-600 flex items-center justify-center"><i class="fa-regular fa-clock"></i></div>
                    </div>
                    <div class="bg-white p-5 rounded-xl border border-slate-200 shadow-sm flex items-center justify-between">
                        <div>
                            <p class="text-xs text-slate-500 uppercase font-bold">SLA Breaches</p>
                            <h3 class="text-2xl font-bold text-red-600">3</h3>
                        </div>
                        <div class="w-10 h-10 rounded-full bg-red-50 text-red-600 flex items-center justify-center"><i class="fa-solid fa-triangle-exclamation"></i></div>
                    </div>
                    <div class="bg-white p-5 rounded-xl border border-slate-200 shadow-sm flex items-center justify-between">
                        <div>
                            <p class="text-xs text-slate-500 uppercase font-bold">Fake Reports</p>
                            <h3 class="text-2xl font-bold text-slate-800">156</h3>
                        </div>
                        <div class="w-10 h-10 rounded-full bg-slate-100 text-slate-600 flex items-center justify-center"><i class="fa-solid fa-ban"></i></div>
                    </div>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
                    <!-- Analytics Chart -->
                    <div class="lg:col-span-2 bg-white rounded-xl border border-slate-200 shadow-sm p-4 h-96 flex flex-col">
                        <div class="flex justify-between items-center mb-4">
                            <h3 class="font-bold text-slate-800">Department Performance</h3>
                            <span class="text-xs bg-slate-100 px-2 py-1 rounded">Last 30 Days</span>
                        </div>
                        <div class="flex-1 relative w-full h-full">
                            <canvas id="performanceChart"></canvas>
                        </div>
                    </div>

                    <!-- Recent Tickets -->
                    <div class="bg-white rounded-xl border border-slate-200 shadow-sm p-4 h-96 flex flex-col">
                        <h3 class="font-bold text-slate-800 mb-4">Live Ticket Feed</h3>
                        <div class="overflow-y-auto flex-1 space-y-3 pr-2 custom-scrollbar" id="ticket-list">
                            <!-- Ticket 1 -->
                            <div class="p-3 border border-slate-100 rounded-lg hover:bg-slate-50 transition cursor-pointer group">
                                <div class="flex justify-between items-start mb-1">
                                    <span class="text-xs font-bold text-red-600 bg-red-50 px-1.5 py-0.5 rounded">High</span>
                                    <span class="text-xs text-slate-400">2m ago</span>
                                </div>
                                <h4 class="text-sm font-semibold text-slate-800">Severe Pothole - Main St.</h4>
                                <div class="flex items-center gap-2 mt-2">
                                    <span class="text-xs bg-slate-100 text-slate-600 px-2 py-1 rounded">Wait: Analysis</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                 <!-- AI Verification Table -->
                 <div class="bg-white rounded-xl border border-slate-200 shadow-sm overflow-hidden">
                    <div class="px-6 py-4 border-b border-slate-100 flex justify-between items-center">
                        <h3 class="font-bold text-slate-800">AI Re-Verification (Before vs After)</h3>
                    </div>
                    <div class="overflow-x-auto">
                        <table class="w-full text-left text-sm text-slate-600">
                            <thead class="bg-slate-50 text-xs uppercase font-semibold text-slate-500">
                                <tr>
                                    <th class="px-6 py-3">Ticket</th>
                                    <th class="px-6 py-3">Type</th>
                                    <th class="px-6 py-3">Before</th>
                                    <th class="px-6 py-3">After (Uploaded)</th>
                                    <th class="px-6 py-3">AI Score</th>
                                    <th class="px-6 py-3">Status</th>
                                </tr>
                            </thead>
                            <tbody class="divide-y divide-slate-100">
                                <tr class="hover:bg-slate-50">
                                    <td class="px-6 py-4 font-mono text-xs">#TKT-8921</td>
                                    <td class="px-6 py-4">Pothole</td>
                                    <td class="px-6 py-4"><div class="w-12 h-12 bg-slate-200 rounded overflow-hidden"><img src="https://images.unsplash.com/photo-1515162816999-a0c47dc192f7?auto=format&fit=crop&q=80&w=100" class="w-full h-full object-cover"></div></td>
                                    <td class="px-6 py-4"><div class="w-12 h-12 bg-slate-200 rounded overflow-hidden"><img src="https://images.unsplash.com/photo-1584463635346-950937a0753f?auto=format&fit=crop&q=80&w=100" class="w-full h-full object-cover"></div></td>
                                    <td class="px-6 py-4"><span class="text-green-600 font-bold">98% Match</span></td>
                                    <td class="px-6 py-4"><span class="bg-green-100 text-green-700 text-xs px-2 py-1 rounded-full">Closed</span></td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Future Roadmap Section (From PDF Page 10) -->
    <section id="future" class="py-20 bg-slate-900 text-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl font-bold">Future Development Roadmap</h2>
                <p class="text-slate-400 mt-2">Where we are taking this project next.</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                <div class="bg-slate-800 p-6 rounded-xl border border-slate-700">
                    <h4 class="font-bold text-blue-400 mb-2">Video Complaints</h4>
                    <p class="text-sm text-slate-300">Support for short video uploads with frame-by-frame AI verification for complex issues.</p>
                </div>
                <div class="bg-slate-800 p-6 rounded-xl border border-slate-700">
                    <h4 class="font-bold text-purple-400 mb-2">Deepfake Detection</h4>
                    <p class="text-sm text-slate-300">Advanced AI capabilities to detect generative AI images and sophisticated forgeries.</p>
                </div>
                <div class="bg-slate-800 p-6 rounded-xl border border-slate-700">
                    <h4 class="font-bold text-green-400 mb-2">Predictive Analytics</h4>
                    <p class="text-sm text-slate-300">Identify accident-prone zones and predict frequent problem areas for preventive action.</p>
                </div>
                <div class="bg-slate-800 p-6 rounded-xl border border-slate-700">
                    <h4 class="font-bold text-yellow-400 mb-2">Citizen Gamification</h4>
                    <p class="text-sm text-slate-300">Reward points and leaderboards for active citizens who submit genuine, helpful reports.</p>
                </div>
                 <div class="bg-slate-800 p-6 rounded-xl border border-slate-700">
                    <h4 class="font-bold text-red-400 mb-2">Multilingual Support</h4>
                    <p class="text-sm text-slate-300">Voice-based complaint submission in regional languages.</p>
                </div>
                 <div class="bg-slate-800 p-6 rounded-xl border border-slate-700">
                    <h4 class="font-bold text-indigo-400 mb-2">Smart Notifications</h4>
                    <p class="text-sm text-slate-300">Real-time status alerts and SLA deadline reminders.</p>
                </div>
                 <div class="bg-slate-800 p-6 rounded-xl border border-slate-700">
                    <h4 class="font-bold text-pink-400 mb-2">NGO Collaboration</h4>
                    <p class="text-sm text-slate-300">Allowing NGOs and CSR projects to adopt local problems for faster execution.</p>
                </div>
                 <div class="bg-slate-800 p-6 rounded-xl border border-slate-700">
                    <h4 class="font-bold text-cyan-400 mb-2">IoT Integration</h4>
                    <p class="text-sm text-slate-300">Integration with traffic sensors for fully automated smart governance.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-slate-950 text-white py-12 border-t border-slate-900">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <h2 class="text-2xl font-bold mb-2">CivicPulse<span class="text-blue-500">AI</span></h2>
            <p class="text-slate-500 text-sm mb-8">A Project by Team <strong>HACKER SLAYER</strong> | Lead: Usman Ahmed</p>
            <div class="flex justify-center space-x-6 text-slate-400">
                <a href="#" class="hover:text-white transition"><i class="fa-brands fa-github text-xl"></i></a>
                <a href="#" class="hover:text-white transition"><i class="fa-brands fa-youtube text-xl"></i></a>
                <a href="#" class="hover:text-white transition"><i class="fa-solid fa-link text-xl"></i></a>
            </div>
            <p class="text-slate-600 text-sm mt-8">&copy; 2024 Team Hacker Slayer. Built for GDG TechSprint.</p>
        </div>
    </footer>

    <!-- Notification Toast -->
    <div id="toast" class="fixed bottom-4 right-4 bg-slate-900 text-white px-6 py-4 rounded-lg shadow-2xl transform translate-y-full transition duration-300 z-50 flex items-center gap-3 border border-slate-700">
        <div class="text-green-400"><i class="fa-solid fa-circle-check"></i></div>
        <div>
            <h4 class="font-bold text-sm">Success</h4>
            <p class="text-xs text-slate-300" id="toast-message">Operation completed.</p>
        </div>
    </div>

    <script>
        // --- Navigation Logic ---
        function scrollToDemo() {
            document.getElementById('dashboard-demo').scrollIntoView({ behavior: 'smooth' });
        }

        function switchView(view) {
            const citizenBtn = document.getElementById('btn-citizen');
            const authBtn = document.getElementById('btn-authority');
            const citizenView = document.getElementById('view-citizen');
            const authView = document.getElementById('view-authority');

            if(view === 'citizen') {
                citizenBtn.className = "px-6 py-2 rounded-md text-sm font-medium bg-white text-slate-900 shadow-sm transition";
                authBtn.className = "px-6 py-2 rounded-md text-sm font-medium text-slate-500 hover:text-slate-900 transition";
                citizenView.classList.remove('hidden');
                authView.classList.add('hidden');
            } else {
                authBtn.className = "px-6 py-2 rounded-md text-sm font-medium bg-slate-800 text-white shadow-sm transition";
                citizenBtn.className = "px-6 py-2 rounded-md text-sm font-medium text-slate-500 hover:text-slate-900 transition";
                authView.classList.remove('hidden');
                citizenView.classList.add('hidden');
                renderChart();
            }
        }

        // --- Demo Simulation Logic ---

        function triggerScan() {
            document.getElementById('file-upload').click();
        }

        function handleImageUpload(event) {
            const file = event.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    document.getElementById('preview-img').src = e.target.result;
                    startSimulation();
                };
                reader.readAsDataURL(file);
            }
            event.target.value = '';
        }

        function startSimulation() {
            const uploadPlaceholder = document.getElementById('upload-placeholder');
            const imagePreview = document.getElementById('image-preview');
            const analysisBox = document.getElementById('analysis-box');
            const scanLine = document.getElementById('scanner');
            const aiTags = document.getElementById('ai-tags');
            const form = document.getElementById('report-form');
            const resetBtn = document.getElementById('reset-btn');

            resetBtn.classList.add('hidden');
            document.getElementById('submit-btn').innerHTML = 'Submit Report';
            document.getElementById('submit-btn').className = "w-full bg-blue-600 hover:bg-blue-500 text-white font-bold py-3 rounded-xl shadow-lg shadow-blue-900/50 transition transform active:scale-95";

            uploadPlaceholder.classList.add('hidden');
            imagePreview.classList.remove('hidden');
            
            scanLine.style.display = 'block';
            analysisBox.classList.remove('hidden');
            
            setTimeout(() => {
                document.getElementById('progress-bar').style.width = "40%";
                document.getElementById('ai-result-text').innerText = "Checking duplicates in Firestore...";
            }, 500);

            setTimeout(() => {
                document.getElementById('progress-bar').style.width = "80%";
                document.getElementById('ai-result-text').innerText = "Verifying geolocation & time...";
            }, 1200);

            setTimeout(() => {
                document.getElementById('progress-bar').style.width = "100%";
                document.getElementById('ai-status-text').innerText = "VERIFIED";
                document.getElementById('ai-status-text').classList.remove('animate-pulse', 'text-blue-400');
                document.getElementById('ai-status-text').classList.add('text-green-400');
                
                scanLine.style.display = 'none';
                aiTags.classList.remove('hidden');
                aiTags.classList.add('fade-in');

                form.classList.remove('opacity-50', 'pointer-events-none');
            }, 2000);
        }

        function submitReport() {
            const btn = document.getElementById('submit-btn');
            btn.innerHTML = '<i class="fa-solid fa-circle-notch fa-spin"></i> Submitting...';
            
            setTimeout(() => {
                showToast("Report Submitted! Ticket #8922 Generated.");
                
                btn.innerHTML = 'Submitted Successfully';
                btn.classList.add('bg-green-600');
                btn.classList.remove('bg-blue-600');
                btn.classList.add('pointer-events-none');

                document.getElementById('reset-btn').classList.remove('hidden');

                updateDashboardStats();
            }, 1500);
        }

        function resetDemo() {
            document.getElementById('upload-placeholder').classList.remove('hidden');
            document.getElementById('image-preview').classList.add('hidden');
            document.getElementById('analysis-box').classList.add('hidden');
            document.getElementById('ai-tags').classList.add('hidden');
            document.getElementById('report-form').classList.add('opacity-50', 'pointer-events-none');
            document.getElementById('reset-btn').classList.add('hidden');
            
            document.getElementById('progress-bar').style.width = "0%";
            document.getElementById('ai-status-text').innerText = "Processing...";
            document.getElementById('ai-status-text').classList.add('animate-pulse', 'text-blue-400');
            document.getElementById('ai-status-text').classList.remove('text-green-400');
            document.getElementById('ai-result-text').innerText = "Verifying metadata & checking duplicates...";
        }

        function updateDashboardStats() {
            const totalEl = document.getElementById('stat-total');
            const pendingEl = document.getElementById('stat-pending');
            const listEl = document.getElementById('ticket-list');

            let total = parseInt(totalEl.innerText.replace(',',''));
            let pending = parseInt(pendingEl.innerText);

            totalEl.innerText = (total + 1).toLocaleString();
            pendingEl.innerText = pending + 1;

            const newTicket = `
                <div class="p-3 border border-slate-100 bg-blue-50 rounded-lg transition cursor-pointer border-l-4 border-l-blue-600 fade-in">
                    <div class="flex justify-between items-start mb-1">
                        <span class="text-xs font-bold text-red-600 bg-white px-1.5 py-0.5 rounded shadow-sm">High</span>
                        <span class="text-xs text-blue-700 font-bold">Just Now</span>
                    </div>
                    <h4 class="text-sm font-semibold text-slate-800">Road Infrastructure / Pothole</h4>
                    <div class="flex items-center gap-2 mt-2">
                        <span class="text-xs bg-white text-slate-600 px-2 py-1 rounded">New Report</span>
                    </div>
                </div>
            `;
            listEl.insertAdjacentHTML('afterbegin', newTicket);
            
            if (window.myChart) {
                window.myChart.data.datasets[0].data[0] += 1;
                window.myChart.update();
            }
        }

        function showToast(msg) {
            const toast = document.getElementById('toast');
            document.getElementById('toast-message').innerText = msg;
            toast.classList.remove('translate-y-full');
            setTimeout(() => {
                toast.classList.add('translate-y-full');
            }, 4000);
        }

        let chartInitialized = false;
        function renderChart() {
            if (chartInitialized) return;
            const ctx = document.getElementById('performanceChart').getContext('2d');
            window.myChart = new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: ['Roads', 'Sanitation', 'Water', 'Electric', 'Parks'],
                    datasets: [{
                        label: 'Open Tickets',
                        data: [12, 19, 3, 5, 2],
                        backgroundColor: '#3B82F6',
                        borderRadius: 4
                    }, {
                        label: 'Resolved (24h)',
                        data: [20, 15, 8, 10, 5],
                        backgroundColor: '#22c55e',
                        borderRadius: 4
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: { position: 'bottom' }
                    },
                    scales: {
                        y: { beginAtZero: true, grid: { color: '#f1f5f9' } },
                        x: { grid: { display: false } }
                    }
                }
            });
            chartInitialized = true;
        }
    </script>
</body>
</html>
