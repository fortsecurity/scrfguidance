<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8"> 
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SCRF Methodology Guidance</title>
    
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com/"></script>
    
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

        /* Global Black Theme */
        html, body {
            background-color: #000000 !important;
            color: #e2e8f0; /* slate-200 */
            font-family: 'Inter', sans-serif;
            scroll-behavior: smooth;
            margin: 0;
        }

        /* Fade Animation for Data Injection */
        .fade-in {
            animation: fadeIn 0.5s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* Card Styling for Black Theme */
        .card-dark {
            background-color: #0a0a0a; /* Very dark gray, almost black */
            border: 1px solid #262626; /* neutral-800 */
        }
        
        .card-inner {
            background-color: #171717; /* neutral-900 */
            border: 1px solid #262626;
        }

        /* Form Elements */
        select {
            background-color: #000000 !important;
            border-color: #404040 !important;
            color: white !important;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #000;
        }
        ::-webkit-scrollbar-thumb {
            background: #333;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #555;
        }
    </style>
</head>
<body class="bg-black text-slate-200">

    <!-- Main Container -->
    <div class="max-w-6xl mx-auto px-4 py-8 mb-20">
        
        <!-- Header Section -->
        <header class="mb-10 border-b border-blue-900/50 pb-8 flex flex-col md:flex-row justify-between items-start md:items-center gap-6">
            <div>
                <h1 class="text-4xl md:text-5xl font-bold text-white mb-2 tracking-tight">
                    SCRF Methodology
                </h1>
                <p class="text-lg md:text-xl text-blue-400 font-medium">
                    A Practical Guide for Cyber Champions
                </p>
            </div>
            <!-- Sector Selector -->
            <div class="w-full md:w-auto card-dark p-5 rounded-xl shadow-2xl">
                <label for="sectorSelect" class="block text-sm font-bold text-blue-400 uppercase tracking-wide mb-2">
                    Select Your Critical Sector:
                </label>
                <select id="sectorSelect" class="text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5">
                    <option value="Oil & Gas">Oil & Gas</option>
                    <option value="Government">Government</option>
                    <option value="Defense">Defense</option>
                    <option value="Energy">Energy</option>
                    <option value="Banking" selected="">Banking</option>
                    <option value="Trade & Investments">Trade & Investments</option>
                    <option value="Telecommunications">Telecommunications</option>
                    <option value="National IT Infrastructure">National IT Infrastructure</option>
                    <option value="Healthcare">Healthcare</option>
                    <option value="Food Supply">Food Supply</option>
                </select>
            </div>
        </header>

        <!-- Introduction -->
        <div class="mb-16 card-dark rounded-xl shadow-2xl p-8 border-l-4 border-blue-600">
            <h2 class="text-3xl font-bold text-white mb-4">Welcome, <span id="sector-name-intro" class="text-blue-400">Banking</span> Cyber Champion</h2>
            <p class="text-lg text-gray-400 mb-4 leading-relaxed">
                This guidance is your playbook for implementing the Sector Cyber Resilience Framework (SCRF). Your role is to lead the <span id="sector-name-body" class="font-semibold text-blue-200">Banking</span> sector, coordinating with Critical Service Operators (CSOs) to build a unified, proactive, and resilient defense.
            </p>
            <p class="text-lg text-gray-400 mb-6 leading-relaxed">
                The SCRF is a continuous four-phase cycle. Your mission is to guide your CSOs through each phase to generate awareness, define risk, plan controls, and execute assurance. 
            </p>
            <p class="text-lg text-yellow-200 italic bg-yellow-900/20 p-4 rounded-lg border border-yellow-600/30">
                Remember, where you are also responsible for Critical Services, you must adopt the dual role of Champion and CSO.
            </p>
        </div>

        <!-- SCRF Visual -->
        <div class="mb-20">
            <h2 class="text-3xl font-bold text-white text-center mb-10">The SCRF Continuous Cycle</h2>
            <div class="flex justify-center items-center p-8 card-inner rounded-xl border border-gray-800">
                <svg class="w-full max-w-md" viewBox="0 0 350 220" xmlns="http://www.w3.org/2000/svg">
                    <defs>
                        <marker id="arrow" markerWidth="10" markerHeight="7" refX="8" refY="3.5" orient="auto" fill="#0ea5e9">
                            <polygon points="0 0, 10 3.5, 0 7"></polygon>
                        </marker>
                    </defs>
                    <g>
                        <rect x="10" y="10" width="150" height="80" rx="8" fill="#000" stroke="#3b82f6" stroke-width="1.5"></rect>
                        <text x="85" y="40" text-anchor="middle" font-size="12" font-weight="bold" fill="#60a5fa">1. Generate SA</text>
                        <text x="85" y="60" text-anchor="middle" font-size="10" fill="#94a3b8">(Identify Mission & Assets)</text>
                    </g>
                    <g>
                        <rect x="190" y="10" width="150" height="80" rx="8" fill="#000" stroke="#3b82f6" stroke-width="1.5"></rect>
                        <text x="265" y="40" text-anchor="middle" font-size="12" font-weight="bold" fill="#60a5fa">2. Define Risk</text>
                        <text x="265" y="60" text-anchor="middle" font-size="10" fill="#94a3b8">(Impact & Likelihood)</text>
                    </g>
                    <g>
                        <rect x="10" y="130" width="150" height="80" rx="8" fill="#000" stroke="#3b82f6" stroke-width="1.5"></rect>
                        <text x="85" y="160" text-anchor="middle" font-size="12" font-weight="bold" fill="#60a5fa">4. Execute Assurance</text>
                        <text x="85" y="180" text-anchor="middle" font-size="10" fill="#94a3b8">(Observe, Measure, Act)</text>
                    </g>
                    <g>
                        <rect x="190" y="130" width="150" height="80" rx="8" fill="#000" stroke="#3b82f6" stroke-width="1.5"></rect>
                        <text x="265" y="160" text-anchor="middle" font-size="12" font-weight="bold" fill="#60a5fa">3. Plan Controls</text>
                        <text x="265" y="180" text-anchor="middle" font-size="10" fill="#94a3b8">(Baseline & Adjust)</text>
                    </g>
                    <path d="M 160, 50 L 180, 50" stroke="#0ea5e9" stroke-width="2" fill="none" marker-end="url(#arrow)"></path>
                    <path d="M 265, 90 L 265, 120" stroke="#0ea5e9" stroke-width="2" fill="none" marker-end="url(#arrow)"></path>
                    <path d="M 180, 170 L 160, 170" stroke="#0ea5e9" stroke-width="2" fill="none" marker-end="url(#arrow)"></path>
                    <path d="M 85, 120 L 85, 90" stroke="#0ea5e9" stroke-width="2" fill="none" marker-end="url(#arrow)"></path>
                </svg>
            </div>
        </div>

        <!-- Role Definitions -->
        <section class="mb-20">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- Cyber Champion Role -->
                <div class="card-dark rounded-xl shadow-2xl p-8 border-t-4 border-blue-500">
                    <h3 class="text-2xl font-semibold text-white mb-4 flex items-center">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7 mr-3 text-blue-400" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M11.049 2.927c.3-.921 1.603-.921 1.902 0l1.519 4.674a1 1 0 00.95.69h4.915c.969 0 1.371 1.24.588 1.81l-3.976 2.888a1 1 0 00-.363 1.118l1.518 4.674c.3.922-.755 1.688-1.538 1.118l-3.976-2.888a1 1 0 00-1.175 0l-3.976 2.888c-.783.57-1.838-.196-1.538-1.118l1.518-4.674a1 1 0 00-.363-1.118L2.05 10.1c-.783-.57-.38-1.81.588-1.81h4.914a1 1 0 00.95-.69L9.53 2.927z"></path>
                        </svg>
                        Sector Role: Cyber Champion
                    </h3>
                    <p class="text-gray-400 mb-4">You are the sector leader, liaison, and expert. Your main responsibilities are to:</p>
                    <ul class="list-disc list-inside space-y-2 text-blue-300">
                        <li>Set cybersecurity regulation, policy, compliance, and standards for your entire Critical Sector.</li>
                        <li>Act as the sector expert and liaison for the government (NCSC) on all cybersecurity matters.</li>
                        <li>Lead engagement with CSOs to drive the implementation of this framework.</li>
                        <li>Hold the authority to make decisions on cybersecurity matters that impact the sector and nation.</li>
                    </ul>
                </div>
                <!-- CSO Role -->
                <div class="card-dark rounded-xl shadow-2xl p-8 border-t-4 border-green-500">
                    <h3 class="text-2xl font-semibold text-white mb-4 flex items-center">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7 mr-3 text-green-400" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                          <path stroke-linecap="round" stroke-linejoin="round" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"></path>
                          <path stroke-linecap="round" stroke-linejoin="round" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
                        </svg>
                        Service Leader: CSO
                    </h3>
                    <p class="text-gray-400 mb-4">CSOs are the organizations on the front line. Their main responsibilities are to:</p>
                    <ul class="list-disc list-inside space-y-2 text-green-300">
                        <li>Operate the nation's Critical Services.</li>
                        <li>Work with you to identify and assure their "crown jewel" Critical Assets.</li>
                        <li>Perform the hands-on implementation of the SCRF activities on their systems.</li>
                        <li>Report their findings, risks, and progress to you as the Sector Cyber Champion.</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Main Phases -->
        <div class="space-y-12">

            <!-- Phase 1 -->
            <section>
                <h2 class="text-3xl font-bold text-white mb-6 flex items-center">
                    <span class="bg-cyan-900/50 text-cyan-400 px-4 py-2 rounded-lg mr-4 text-2xl font-mono">01</span>
                    Phase 1: Generate Situational Awareness
                </h2>
                
                <div class="space-y-6 ml-4 md:ml-12">
                    <!-- Activity 1.1 -->
                    <div class="card-dark rounded-xl p-6 md:p-8 shadow-lg">
                        <h3 class="text-xl md:text-2xl font-semibold text-white mb-4">Activity 1.1: Identify Sector Mission (Cyber Champion)</h3>
                        <div class="mb-6">
                            <h4 class="font-bold text-blue-400 mb-2 uppercase text-sm tracking-wide">Required Actions:</h4>
                            <ul class="list-disc list-inside text-gray-400 space-y-1">
                                <li>Review and align with published National Cybersecurity Strategic Goals.</li>
                                <li>Workshop with key stakeholders to draft and formally approve a Sector-specific Mission Statement.</li>
                                <li>Develop and document a Sectoral Cybersecurity Strategy that includes specific, measurable goals.</li>
                            </ul>
                        </div>
                        <div class="card-inner p-4 rounded-lg border-l-4 border-blue-400">
                            <h5 class="text-xs font-bold text-blue-400 uppercase mb-2">Sector Examples</h5>
                            <div id="ex-1.1" class="text-gray-300 italic ml-4 fade-in">Loading...</div>
                        </div>
                    </div>

                    <!-- Activity 1.2 -->
                    <div class="card-dark rounded-xl p-6 md:p-8 shadow-lg">
                        <h3 class="text-xl md:text-2xl font-semibold text-white mb-4">Activity 1.2: Define Services &amp; Assets (CSO)</h3>
                        <div class="mb-6">
                            <h4 class="font-bold text-green-400 mb-2 uppercase text-sm tracking-wide">Required Actions:</h4>
                            <ul class="list-disc list-inside text-gray-400 space-y-1">
                                <li>Conduct Business Capability Mapping to model the core functions related to Critical Services.</li>
                                <li>Deconstruct functions into a catalog of supporting Critical Services.</li>
                                <li>Implement a discovery process to create a comprehensive inventory of all critical IT, OT, and data assets.</li>
                            </ul>
                        </div>
                        <div class="card-inner p-4 rounded-lg border-l-4 border-green-400">
                            <h5 class="text-xs font-bold text-green-400 uppercase mb-2">Sector Examples</h5>
                            <div id="ex-1.2" class="text-gray-300 italic ml-4 fade-in">Loading...</div>
                        </div>
                    </div>

                    <!-- Activity 1.3 -->
                    <div class="card-dark rounded-xl p-6 md:p-8 shadow-lg">
                        <h3 class="text-xl md:text-2xl font-semibold text-white mb-4">Activity 1.3: Understand Vulnerabilities (Shared)</h3>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                            <div>
                                <h4 class="font-bold text-blue-400 mb-2 text-sm uppercase">Champion Actions:</h4>
                                <ul class="list-disc list-inside text-gray-400 space-y-1">
                                    <li>Establish a sector-wide vulnerability reporting program that can integrate with the Sector Cyber Champion.</li>
                                </ul>
                            </div>
                            <div>
                                <h4 class="font-bold text-green-400 mb-2 text-sm uppercase">CSO Actions:</h4>
                                <ul class="list-disc list-inside text-gray-400 space-y-1">
                                    <li>Maintain External Attack Surface Management, specifically for internet facing Critical Services.</li>
                                </ul>
                            </div>
                        </div>
                        <div class="card-inner p-4 rounded-lg border-l-4 border-green-400">
                            <h5 class="text-xs font-bold text-green-400 uppercase mb-2">Sector Examples</h5>
                            <div id="ex-1.3" class="text-gray-300 italic ml-4 fade-in">Loading...</div>
                        </div>
                    </div>

                    <!-- Activity 1.4 -->
                    <div class="card-dark rounded-xl p-6 md:p-8 shadow-lg">
                        <h3 class="text-xl md:text-2xl font-semibold text-white mb-4">Activity 1.4: Understand Threat Landscape (Shared)</h3>
                         <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                            <div>
                                <h4 class="font-bold text-blue-400 mb-2 text-sm uppercase">Champion Actions:</h4>
                                <ul class="list-disc list-inside text-gray-400 space-y-1">
                                    <li>Produce and consume regular threat intelligence reports that analyze adversary capability and intent.</li>
                                </ul>
                            </div>
                            <div>
                                <h4 class="font-bold text-green-400 mb-2 text-sm uppercase">CSO Actions:</h4>
                                <ul class="list-disc list-inside text-gray-400 space-y-1">
                                    <li>Produce and consume regular threat intelligence reports (Organisational reporting).</li>
                                </ul>
                            </div>
                        </div>
                        <div class="card-inner p-4 rounded-lg border-l-4 border-green-400">
                            <h5 class="text-xs font-bold text-green-400 uppercase mb-2">Sector Examples</h5>
                            <div id="ex-1.4" class="text-gray-300 italic ml-4 fade-in">Loading...</div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Phase 2 -->
            <section>
                <h2 class="text-3xl font-bold text-white mb-6 flex items-center">
                    <span class="bg-red-900/50 text-red-400 px-4 py-2 rounded-lg mr-4 text-2xl font-mono">02</span>
                    Phase 2: Define Mission Risk
                </h2>
                
                <div class="space-y-6 ml-4 md:ml-12">
                    <!-- Activity 2.1 -->
                    <div class="card-dark rounded-xl p-6 md:p-8 shadow-lg">
                        <h3 class="text-xl md:text-2xl font-semibold text-white mb-4">Activity 2.1: Determine Threat Intent &amp; Likelihood (CSO)</h3>
                        <div class="mb-6">
                            <h4 class="font-bold text-green-400 mb-2 uppercase text-sm tracking-wide">Required Actions:</h4>
                            <ul class="list-disc list-inside text-gray-400 space-y-1">
                                <li>Develop and maintain sector-specific threat models for Critical Services, mapping known adversary behaviors.</li>
                                <li>Map the Vulnerabilities present to Controls that mitigate them. This gives you Net Vulnerabilities.</li>
                            </ul>
                        </div>
                        <div class="card-inner p-4 rounded-lg border-l-4 border-green-400">
                            <h5 class="text-xs font-bold text-green-400 uppercase mb-2">Sector Examples</h5>
                            <div id="ex-2.1" class="text-gray-300 italic ml-4 fade-in">Loading...</div>
                        </div>
                    </div>

                    <!-- Activity 2.2 -->
                    <div class="card-dark rounded-xl p-6 md:p-8 shadow-lg">
                        <h3 class="text-xl md:text-2xl font-semibold text-white mb-4">Activity 2.2: Determine Impact (CSO)</h3>
                        <div class="mb-6">
                            <h4 class="font-bold text-green-400 mb-2 uppercase text-sm tracking-wide">Required Actions:</h4>
                            <ul class="list-disc list-inside text-gray-400 space-y-1">
                                <li>Identify your Critical Services’ ‘Crown Jewels’ assets.</li>
                                <li>Conduct a formal Business Impact Analysis (BIA) covering all Critical Services.</li>
                                <li>Interview business owners to define and document Maximum Tolerable Downtime (MTD).</li>
                                <li>From the BIA and MTD, derive and set official RTOs and RPOs.</li>
                            </ul>
                        </div>
                        <div class="card-inner p-4 rounded-lg border-l-4 border-green-400">
                            <h5 class="text-xs font-bold text-green-400 uppercase mb-2">Sector Examples</h5>
                            <div id="ex-2.2" class="text-gray-300 italic ml-4 fade-in">Loading...</div>
                        </div>
                    </div>

                    <!-- Activity 2.3 -->
                    <div class="card-dark rounded-xl p-6 md:p-8 shadow-lg">
                        <h3 class="text-xl md:text-2xl font-semibold text-white mb-4">Activity 2.3: Calculate Risk (Shared)</h3>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                            <div>
                                <h4 class="font-bold text-blue-400 mb-2 text-sm uppercase">Champion Actions:</h4>
                                <ul class="list-disc list-inside text-gray-400 space-y-1">
                                    <li>Develop a standardised risk assessment procedure.</li>
                                    <li>Create and maintain a Sectoral Cyber Risk Register.</li>
                                </ul>
                            </div>
                            <div>
                                <h4 class="font-bold text-green-400 mb-2 text-sm uppercase">CSO Actions:</h4>
                                <ul class="list-disc list-inside text-gray-400 space-y-1">
                                    <li>Implement a risk assessment procedure.</li>
                                    <li>Create and maintain an Organizational Cyber Risk Register.</li>
                                </ul>
                            </div>
                        </div>
                        <div class="card-inner p-4 rounded-lg border-l-4 border-blue-400">
                            <h5 class="text-xs font-bold text-blue-400 uppercase mb-2">Sector Examples</h5>
                            <div id="ex-2.3" class="text-gray-300 italic ml-4 fade-in">Loading...</div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Phase 3 -->
            <section>
                <h2 class="text-3xl font-bold text-white mb-6 flex items-center">
                    <span class="bg-yellow-900/50 text-yellow-400 px-4 py-2 rounded-lg mr-4 text-2xl font-mono">03</span>
                    Phase 3: Plan Additional Controls
                </h2>
                
                <div class="space-y-6 ml-4 md:ml-12">
                    <!-- Activity 3.1 -->
                    <div class="card-dark rounded-xl p-6 md:p-8 shadow-lg">
                        <h3 class="text-xl md:text-2xl font-semibold text-white mb-4">Activity 3.1: Baseline &amp; Adjust Controls (Shared)</h3>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                            <div>
                                <h4 class="font-bold text-blue-400 mb-2 text-sm uppercase">Champion Actions:</h4>
                                <ul class="list-disc list-inside text-gray-400 space-y-1">
                                    <li>Utilise the minimum security requirements in Appendix C to establish a minimum critical security and resilience baseline.</li>
                                </ul>
                            </div>
                            <div>
                                <h4 class="font-bold text-green-400 mb-2 text-sm uppercase">CSO Actions:</h4>
                                <ul class="list-disc list-inside text-gray-400 space-y-1">
                                    <li>Perform a gap analysis of existing controls using Appendix C requirements.</li>
                                    <li>Prioritize and implement/adjust controls to reduce risk to an acceptable level.</li>
                                </ul>
                            </div>
                        </div>
                        <div class="card-inner p-4 rounded-lg border-l-4 border-blue-400">
                            <h5 class="text-xs font-bold text-blue-400 uppercase mb-2">Sector Examples</h5>
                            <div id="ex-3.1" class="text-gray-300 italic ml-4 fade-in">Loading...</div>
                        </div>
                    </div>

                    <!-- Minimum Security Controls Matrix -->
                    <div class="card-dark rounded-xl p-6 md:p-8 shadow-lg border border-gray-800">
                        <h3 class="text-xl md:text-2xl font-semibold text-white mb-6">Minimum Security Controls Matrix</h3>
                        <div class="overflow-x-auto">
                            <table class="w-full text-left text-gray-300 border-collapse text-sm">
                                <thead>
                                    <tr class="bg-gray-900 text-white border-b border-gray-700">
                                        <th class="p-4 font-semibold w-1/4">Requirement</th>
                                        <th class="p-4 font-semibold w-1/4">Outcome</th>
                                        <th class="p-4 font-semibold w-1/3">Commonly Enhanced Controls</th>
                                        <th class="p-4 font-semibold text-center w-1/12">TRI*</th>
                                    </tr>
                                </thead>
                                <tbody class="divide-y divide-gray-800">
                                    <!-- 1. Secure Acquisition -->
                                    <tr class="hover:bg-white/5 transition-colors">
                                        <td class="p-4 align-top font-semibold text-blue-400">1. Secure Acquisition, Development & Maintenance</td>
                                        <td class="p-4 align-top">Security must be an integral part of the entire lifecycle of critical networks and systems, from procurement and development to patching and decommissioning.</td>
                                        <td class="p-4 align-top text-gray-400">
                                            <ul class="list-disc list-inside">
                                                <li>Formal vulnerability management program (scanning, patching SLAs)</li>
                                                <li>Secure Software Development Lifecycle (SSDLC)</li>
                                                <li>Documented change management process</li>
                                                <li>Cyber-physical: Preventative Maintenance Levels tracked via threat-based budgeting</li>
                                            </ul>
                                        </td>
                                        <td class="p-4 align-top text-center font-bold text-red-500 text-lg">10</td>
                                    </tr>
                                    <!-- 2. MFA -->
                                    <tr class="hover:bg-white/5 transition-colors">
                                        <td class="p-4 align-top font-semibold text-blue-400">2. Multi-Factor Authentication & Secure Comms</td>
                                        <td class="p-4 align-top">Authentication of users must be strongly verified before granting access to critical systems, and secure communications are pivotal.</td>
                                        <td class="p-4 align-top text-gray-400">
                                            <ul class="list-disc list-inside">
                                                <li>Phishing-resistant MFA enforced on all remote access/admin accounts</li>
                                                <li>End-to-end encrypted communication tools</li>
                                                <li>Secure configuration of email systems (DMARC, DKIM, SPF)</li>
                                                <li>Cyber-physical: Test Internet Denial/Communications Resilience with backup channels</li>
                                            </ul>
                                        </td>
                                        <td class="p-4 align-top text-center font-bold text-red-500 text-lg">9</td>
                                    </tr>
                                    <!-- 3. Controlled Access -->
                                    <tr class="hover:bg-white/5 transition-colors">
                                        <td class="p-4 align-top font-semibold text-blue-400">3. Controlled Access Linked to Critical Asset Management</td>
                                        <td class="p-4 align-top">Identity of users must be strictly controlled based on the principle of least privilege and Just-In-Time (JIT) access. This relies on knowing what is critical.</td>
                                        <td class="p-4 align-top text-gray-400">
                                            <ul class="list-disc list-inside">
                                                <li>Identity and Access Management (IAM/PAM)</li>
                                                <li>Comprehensive critical asset inventory mapped to identity</li>
                                                <li>Secure employee onboarding/offboarding</li>
                                                <li>Cyber-physical: Asset inventory covers OT, ICS, and OT supply chain</li>
                                            </ul>
                                        </td>
                                        <td class="p-4 align-top text-center font-bold text-red-400 text-lg">8</td>
                                    </tr>
                                    <!-- 4. Incident Handling -->
                                    <tr class="hover:bg-white/5 transition-colors">
                                        <td class="p-4 align-top font-semibold text-blue-400">4. Incident Handling</td>
                                        <td class="p-4 align-top">The organization must have a defined, resourced, and tested plan to effectively manage security incidents from detection to resolution.</td>
                                        <td class="p-4 align-top text-gray-400">
                                            <ul class="list-disc list-inside">
                                                <li>Tested Incident Response Plan (IRP) with playbooks</li>
                                                <li>Designated Cyber Security Incident Response Team (CSIRT)</li>
                                                <li>Regular tabletop exercises and simulation drills</li>
                                                <li>Cyber-physical: Testing fail-over to manual operations</li>
                                            </ul>
                                        </td>
                                        <td class="p-4 align-top text-center font-bold text-red-400 text-lg">7</td>
                                    </tr>
                                    <!-- 5. Supply Chain Security -->
                                    <tr class="hover:bg-white/5 transition-colors">
                                        <td class="p-4 align-top font-semibold text-blue-400">5. Supply Chain Security</td>
                                        <td class="p-4 align-top">Cyber risk originating from direct suppliers and critical service providers must be systematically identified, assessed, and managed.</td>
                                        <td class="p-4 align-top text-gray-400">
                                            <ul class="list-disc list-inside">
                                                <li>Formal Third-Party Risk Management (TPRM) procedure</li>
                                                <li>Mandatory security clauses and right-to-audit in contracts</li>
                                                <li>Cyber-physical: Demonstrable modularity to reduce cascading failures</li>
                                            </ul>
                                        </td>
                                        <td class="p-4 align-top text-center font-bold text-orange-400 text-lg">6</td>
                                    </tr>
                                    <!-- 6. Security Monitoring -->
                                    <tr class="hover:bg-white/5 transition-colors">
                                        <td class="p-4 align-top font-semibold text-blue-400">6. Security Monitoring & Validation Measures</td>
                                        <td class="p-4 align-top">Continuously measure, test, and track the effectiveness of security controls to ensure they are working as intended.</td>
                                        <td class="p-4 align-top text-gray-400">
                                            <ul class="list-disc list-inside">
                                                <li>Dedicated logging and monitoring solution (EDR/SIEM)</li>
                                                <li>Security metrics program with KPIs/KRIs</li>
                                                <li>Regular independent penetration testing and threat hunting</li>
                                                <li>Cyber-physical: OT/ICS Stress-Testing (red teaming/chaos engineering)</li>
                                            </ul>
                                        </td>
                                        <td class="p-4 align-top text-center font-bold text-orange-400 text-lg">5</td>
                                    </tr>
                                    <!-- 7. HPU -->
                                    <tr class="hover:bg-white/5 transition-colors">
                                        <td class="p-4 align-top font-semibold text-blue-400">7. High Privileged Users (HPUs) Cyber Hygiene & Training</td>
                                        <td class="p-4 align-top">Individuals with privileged access must possess baseline knowledge of relevant cyber threats and security domains.</td>
                                        <td class="p-4 align-top text-gray-400">
                                            <ul class="list-disc list-inside">
                                                <li>Mandatory threat assessments and training for HPUs</li>
                                                <li>Regular, realistic phishing simulation campaigns</li>
                                                <li>Guidance on secure data handling</li>
                                                <li>Cyber-physical: Training for manual operations "muscle-memory"</li>
                                            </ul>
                                        </td>
                                        <td class="p-4 align-top text-center font-bold text-yellow-400 text-lg">4</td>
                                    </tr>
                                    <!-- 8. Core Policies -->
                                    <tr class="hover:bg-white/5 transition-colors">
                                        <td class="p-4 align-top font-semibold text-blue-400">8. Core Cyber Policies and Procedures</td>
                                        <td class="p-4 align-top">The organization must have a formal, documented, and leadership-approved information security policy and risk assessment process.</td>
                                        <td class="p-4 align-top text-gray-400">
                                            <ul class="list-disc list-inside">
                                                <li>Board-approved Information Security Policy</li>
                                                <li>Documented Critical Service risk assessment methodology</li>
                                                <li>Live cyber risk register tracked by management</li>
                                                <li>Cyber-physical: Assessment of cascading/interdependency risks</li>
                                            </ul>
                                        </td>
                                        <td class="p-4 align-top text-center font-bold text-yellow-400 text-lg">3</td>
                                    </tr>
                                    <!-- 9. Cryptography -->
                                    <tr class="hover:bg-white/5 transition-colors">
                                        <td class="p-4 align-top font-semibold text-blue-400">9. Cryptography & Encryption</td>
                                        <td class="p-4 align-top">Sensitive data must be rendered unreadable and unusable to unauthorized parties (at-rest and in-transit).</td>
                                        <td class="p-4 align-top text-gray-400">
                                            <ul class="list-disc list-inside">
                                                <li>Formal policy defining approved cryptographic standards</li>
                                                <li>Full-disk encryption (e.g., BitLocker, FileVault)</li>
                                                <li>Use of TLS 1.2 or higher for external transfers</li>
                                            </ul>
                                        </td>
                                        <td class="p-4 align-top text-center font-bold text-green-400 text-lg">2</td>
                                    </tr>
                                    <!-- 10. Business Continuity -->
                                    <tr class="hover:bg-white/5 transition-colors">
                                        <td class="p-4 align-top font-semibold text-blue-400">10. Business Continuity & Crisis Management</td>
                                        <td class="p-4 align-top">Critical services must be resilient and able to be restored in a timely manner following a significant cyber disruption.</td>
                                        <td class="p-4 align-top text-gray-400">
                                            <ul class="list-disc list-inside">
                                                <li>Comprehensive Business Impact Analysis (BIA)</li>
                                                <li>Tested Business Continuity & Disaster Recovery Plan (DRP)</li>
                                                <li>Robust data backup and restoration procedures (3-2-1 rule)</li>
                                                <li>Cyber-physical: Hard-Start Recovery Time scenario planning</li>
                                            </ul>
                                        </td>
                                        <td class="p-4 align-top text-center font-bold text-green-400 text-lg">1</td>
                                    </tr>
                                </tbody>
                            </table>
                            <p class="mt-4 text-xs text-gray-500 italic">*TRI = Threat Reduction Indicator (1-10 impact scale)</p>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Phase 4 -->
            <section>
                <h2 class="text-3xl font-bold text-white mb-6 flex items-center">
                    <span class="bg-green-900/50 text-green-400 px-4 py-2 rounded-lg mr-4 text-2xl font-mono">04</span>
                    Phase 4: Execute Mission Assurance
                </h2>
                
                <div class="space-y-6 ml-4 md:ml-12">
                    <!-- Activity 4.1 -->
                    <div class="card-dark rounded-xl p-6 md:p-8 shadow-lg">
                        <h3 class="text-xl md:text-2xl font-semibold text-white mb-4">Activity 4.1: Observe (Cyber Champion)</h3>
                        <div class="mb-6">
                            <h4 class="font-bold text-blue-400 mb-2 uppercase text-sm tracking-wide">Required Actions:</h4>
                            <ul class="list-disc list-inside text-gray-400 space-y-1">
                                <li>Establish a 24/7/365 Security Operations Center (SOC) or monitoring function.</li>
                                <li>Configure EDR / SIEM / SOAR for sector-wide continuous monitoring.</li>
                                <li>Integrate threat intelligence feeds into the monitoring function.</li>
                            </ul>
                        </div>
                        <div class="card-inner p-4 rounded-lg border-l-4 border-blue-400">
                            <h5 class="text-xs font-bold text-blue-400 uppercase mb-2">Sector Examples</h5>
                            <div id="ex-4.1" class="text-gray-300 italic ml-4 fade-in">Loading...</div>
                        </div>
                    </div>

                    <!-- Activity 4.2 -->
                    <div class="card-dark rounded-xl p-6 md:p-8 shadow-lg">
                        <h3 class="text-xl md:text-2xl font-semibold text-white mb-4">Activity 4.2: Measure (Shared)</h3>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                            <div>
                                <h4 class="font-bold text-orange-400 mb-2 text-sm uppercase">NCSC Actions:</h4>
                                <ul class="list-disc list-inside text-gray-400 space-y-1">
                                    <li>Conduct periodic national cyber risk reviews.</li>
                                </ul>
                            </div>
                            <div>
                                <h4 class="font-bold text-blue-400 mb-2 text-sm uppercase">Champion Actions:</h4>
                                <ul class="list-disc list-inside text-gray-400 space-y-1">
                                    <li>Implement GRC process to formalize risk measurement.</li>
                                    <li>Hold regular risk reviews to reassess risk scores.</li>
                                </ul>
                            </div>
                        </div>
                        <div class="card-inner p-4 rounded-lg border-l-4 border-blue-400">
                            <h5 class="text-xs font-bold text-blue-400 uppercase mb-2">Sector Examples</h5>
                            <div id="ex-4.2" class="text-gray-300 italic ml-4 fade-in">Loading...</div>
                        </div>
                    </div>

                    <!-- Activity 4.3 -->
                    <div class="card-dark rounded-xl p-6 md:p-8 shadow-lg">
                        <h3 class="text-xl md:text-2xl font-semibold text-white mb-4">Activity 4.3: Act (Shared)</h3>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                            <div>
                                <h4 class="font-bold text-orange-400 mb-2 text-sm uppercase">NCSC Actions:</h4>
                                <ul class="list-disc list-inside text-gray-400 space-y-1">
                                    <li>Maintain the national change log for cyber risks.</li>
                                </ul>
                            </div>
                            <div>
                                <h4 class="font-bold text-blue-400 mb-2 text-sm uppercase">Champion Actions:</h4>
                                <ul class="list-disc list-inside text-gray-400 space-y-1">
                                    <li>Map control enhancements linked to risk changes.</li>
                                    <li>Maintain a documented change log.</li>
                                </ul>
                            </div>
                        </div>
                        <div class="card-inner p-4 rounded-lg border-l-4 border-blue-400">
                            <h5 class="text-xs font-bold text-blue-400 uppercase mb-2">Sector Examples</h5>
                            <div id="ex-4.3" class="text-gray-300 italic ml-4 fade-in">Loading...</div>
                        </div>
                    </div>

                    <!-- Activity 4.4 -->
                    <div class="card-dark rounded-xl p-6 md:p-8 shadow-lg">
                        <h3 class="text-xl md:text-2xl font-semibold text-white mb-4">Activity 4.4: Report (Shared)</h3>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                            <div>
                                <h4 class="font-bold text-orange-400 mb-2 text-sm uppercase">NCSC Actions:</h4>
                                <ul class="list-disc list-inside text-gray-400 space-y-1">
                                    <li>National-level reporting of risk posture.</li>
                                </ul>
                            </div>
                            <div>
                                <h4 class="font-bold text-blue-400 mb-2 text-sm uppercase">Champion Actions:</h4>
                                <ul class="list-disc list-inside text-gray-400 space-y-1">
                                    <li>Create automated dashboards for near real-time risk reporting.</li>
                                    <li>Produce regular critical cyber resilience executive reports.</li>
                                    <li>Establish a cyber risk data feed.</li>
                                </ul>
                            </div>
                        </div>
                        <div class="card-inner p-4 rounded-lg border-l-4 border-blue-400">
                            <h5 class="text-xs font-bold text-blue-400 uppercase mb-2">Sector Examples</h5>
                            <div id="ex-4.4" class="text-gray-300 italic ml-4 fade-in">Loading...</div>
                        </div>
                    </div>
                </div>
            </section>
        </div>

        <!-- Summary & Timeline Widget -->
        <section class="mt-20 mb-20 card-dark rounded-xl shadow-2xl p-8 border-t-4 border-indigo-500">
            <h2 class="text-3xl font-bold text-white mb-4">Leading the Charge</h2>
            <p class="text-lg text-gray-400 mb-8">
                Thank you, Cyber Champion, for taking on this critical mission. Your leadership in implementing the SCRF will directly enhance the resilience of our nation's most vital services.
            </p>

            <h3 class="text-2xl font-semibold text-white mb-6 text-center">Scaling Cyber Resilience</h3>
            
            <div class="relative pt-4 pb-4 overflow-x-auto">
                <svg class="w-full min-w-[700px]" viewBox="0 0 800 250" xmlns="http://www.w3.org/2000/svg">
                    <style>
                        .year-label { font-size: 14px; fill: #6b7280; text-anchor: middle; font-weight: 600; }
                        .bar-label { font-size: 14px; font-weight: bold; fill: white; alignment-baseline: middle; }
                        .grid-line { stroke: #333; stroke-width: 1; stroke-dasharray: 4; }
                    </style>

                    <!-- Grid Lines -->
                    <line x1="50" y1="20" x2="50" y2="220" class="grid-line"></line>
                    <line x1="190" y1="20" x2="190" y2="220" class="grid-line"></line>
                    <line x1="330" y1="20" x2="330" y2="220" class="grid-line"></line>
                    <line x1="470" y1="20" x2="470" y2="220" class="grid-line"></line>
                    <line x1="610" y1="20" x2="610" y2="220" class="grid-line"></line>
                    <line x1="750" y1="20" x2="750" y2="220" class="grid-line"></line>

                    <!-- Year Labels -->
                    <text x="50" y="240" class="year-label">2025</text>
                    <text x="190" y="240" class="year-label">2026</text>
                    <text x="330" y="240" class="year-label">2027</text>
                    <text x="470" y="240" class="year-label">2028</text>
                    <text x="610" y="240" class="year-label">2029</text>
                    <text x="750" y="240" class="year-label">2030</text>

                    <!-- Phase Bars -->
                    <rect x="190" y="40" width="140" height="40" rx="8" fill="#0ea5e9" fill-opacity="0.8" stroke="#38bdf8" stroke-width="1"></rect>
                    <text x="260" y="65" class="bar-label" text-anchor="middle">Phases 1 &amp; 2</text>

                    <rect x="330" y="100" width="280" height="40" rx="8" fill="#eab308" fill-opacity="0.8" stroke="#facc15" stroke-width="1"></rect>
                    <text x="470" y="125" class="bar-label" text-anchor="middle">Phase 3: Controls</text>

                    <rect x="190" y="160" width="560" height="40" rx="8" fill="#22c55e" fill-opacity="0.8" stroke="#4ade80" stroke-width="1"></rect>
                    <text x="470" y="185" class="bar-label" text-anchor="middle">Phase 4: Assurance</text>
                </svg>
            </div>
        </section>

        <!-- Footer -->
        <footer class="text-center mt-16 pt-6 border-t border-gray-800">
            <p class="text-sm text-gray-500">Sector Cyber Resilience Framework (SCRF) | National Cyber Security Center</p>
        </footer>

    </div>

    <!-- Data Injection Script -->
    <script>
        const sectorData = {
            "Oil & Gas": {
                "1.1": [
                    "Host a workshop with refinery directors to draft a mission: 'To ensure the safe, continuous extraction, refining, and transport of national hydrocarbon resources.'",
                    "Define strategic goals for securing offshore platforms from remote cyber-physical interference by 2026."
                ],
                "1.2": [
                    "Run a discovery scan to map 'Crown Jewel' OT assets (e.g., DCS controllers, pipeline SCADA sensors) for the 'Crude Transport' service.",
                    "Deconstruct the 'Refining' function into supporting services like 'Catalytic Cracking Control' and 'Safety Instrument Systems (SIS)'."
                ],
                "1.3": [
                    "Schedule passive vulnerability scans on refinery control networks to avoid disrupting sensitive PLCs.",
                    "Monitor for unauthorized cellular modems (shadow IT) connected to remote wellhead controllers."
                ],
                "1.4": [
                    "Subscribe to feeds monitoring for hacktivist groups targeting environmental infrastructure.",
                    "Analyze TTPs of state actors known for targeting energy sector safety systems (e.g., Xenotime/TRISIS)."
                ],
                "2.1": [
                    "Develop a threat model for 'Pipeline Pressure Control' systems against sabotage aiming to cause physical ruptures.",
                    "Model insider threats for offshore rig personnel with access to critical safety overrides."
                ],
                "2.2": [
                    "Conduct a BIA for the 'Refinery Emergency Shutdown' system; MTD is practically zero due to immediate physical safety risks.",
                    "Determine RTO for main pipeline SCADA control is less than 15 minutes to prevent massive product backlogs."
                ],
                "2.3": [
                    "Risk Register: 'Ransomware on pipeline HMI. Impact: Critical (supply halt). Likelihood: Medium. Risk Score: 90/100.'",
                    "Risk Register: 'Insider sabotage of refinery SIS. Impact: Catastrophic (loss of life/explosion). Likelihood: Low. Risk Score: 95/100.'"
                ],
                "3.1": [
                    "Champion mandates IEC 62443 standards for all OT environments.",
                    "CSO gap analysis reveals missing segmentation; create a project to install industrial DMZs between IT and OT networks."
                ],
                "4.1": [
                    "Aggregate alerts from offshore rig SOCs and onshore refinery SIEMs to detect lateral movement across the corporate-to-industrial boundary.",
                    "Monitor for anomalous commands sent to pipeline valve controllers during non-standard hours."
                ],
                "4.2": [
                    "Host a semi-annual 'Petrochemical Risk Review' to reassess OT risk scores based on new geopolitical tensions affecting physical asset targeting.",
                    "Re-evaluate risk scores after a major upgrade to a Distributed Control System (DCS)."
                ],
                "4.3": [
                    "A new PLC vulnerability is disclosed. Champion hosts an emergency sector call and shares vendor-specific mitigation guidance.",
                    "Update change log to reflect emergency 'virtual patching' via firewall rules while waiting for a certified vendor patch."
                ],
                "4.4": [
                    "Create a quarterly 'Energy Independence Resilience Report' for the NCSC, showing a 20% improvement in OT network segmentation.",
                    "Provide real-time dashboard to ministry leadership showing current operational status of all major export terminals."
                ]
            },
            "Government": {
                "1.1": [
                    "Workshop with ministry directors for a mission: 'To protect the confidentiality, integrity, and availability of all citizen data and critical national security services.'",
                    "Develop a strategy to migrate 80% of non-classified citizen services to a secure government cloud by 2027."
                ],
                "1.2": [
                    "Run a discovery scan to build an inventory of 'Crown Jewel' assets for the 'National ID Database' service.",
                    "Map dependencies between the 'Tax Collection' service and external banking API gateways."
                ],
                "1.3": [
                    "Run continuous scans on public-facing e-government portal servers, immediately reporting all SQL injection and XSS vulnerabilities.",
                    "Perform weekly automated penetration tests on new citizen-facing mobile applications before release."
                ],
                "1.4": [
                    "Subscribe to national CTI feeds and configure SIEM to detect IOCs related to state-sponsored APTs known for espionage.",
                    "Analyze disinformation campaigns that might accompany cyberattacks on election infrastructure."
                ],
                "2.1": [
                    "Create a threat model for the 'Citizen Tax Portal', mapping TTPs from actors aiming for mass PII data exfiltration.",
                    "Model threats to the 'E-Voting' system specifically focusing on data integrity attacks that could undermine public trust."
                ],
                "2.2": [
                    "Perform BIA on the 'National Health Registry', determining MTD is 2 hours to avoid impacting emergency care admissions.",
                    "Set RPO for the 'National Land Registry' to 0 seconds (synchronous replication) to prevent loss of property ownership data."
                ],
                "2.3": [
                    "Risk Register: 'DDoS on primary e-voting gateway during election week. Impact: High (public trust). Likelihood: High. Risk Score: 95/100.'",
                    "Risk Register: 'Leak of full citizen biometric database. Impact: Catastrophic (national security). Likelihood: Low. Risk Score: 90/100.'"
                ],
                "3.1": [
                    "Champion mandates FIDO2-based MFA for all government employees accessing citizen data.",
                    "CSO gap analysis shows 'Partially Met' for MFA; launch initiative to roll out hardware tokens to all administrators."
                ],
                "4.1": [
                    "Aggregate alerts from all ministry CSOs into a 'Government CERT' dashboard to identify widespread malware outbreaks targeting common administrative software.",
                    "Deploy honeytokens in standard government document templates to detect unauthorized exfiltration."
                ],
                "4.2": [
                    "Host monthly 'Inter-Ministry Cyber Governance' meetings to review risks to shared services like the government cloud platform.",
                    "Reassess risk scores following any major geopolitical event that increases the likelihood of state-sponsored targeting."
                ],
                "4.3": [
                    "A zero-day hits a widely used government CMS. Mandate an emergency patching window across all agencies within 48 hours.",
                    "Coordinate a unified public response to dispel rumors during a disruptive cyberattack on government services."
                ],
                "4.4": [
                    "Produce a 'National Digital Trust' dashboard for Sector Ministers, showing real-time uptime and attack deflection metrics for key citizen services.",
                    "Submit classified monthly reports on attempts by foreign actors to access sensitive government networks."
                ]
            },
            "Defense": {
                "1.1": [
                    "Establish mission: 'To guarantee the confidentiality of classified intelligence and the availability of command-and-control (C2) logistics systems.'",
                    "Define strategic goal to achieve full quantum-resistant encryption on all top-secret communications by 2030."
                ],
                "1.2": [
                    "Map 'Crown Jewel' assets supporting the 'Secure Tactical Comms' service, including specialized encryption hardware and satellite uplinks.",
                    "Inventory all embedded systems within major weapon platforms (aircraft, naval vessels) for cyber-physical dependencies."
                ],
                "1.3": [
                    "Implement strict, isolated vulnerability scanning within classified air-gapped networks, ensuring data diodes are not bypassed.",
                    "Conduct rigorous supply chain analysis on microelectronics used in critical missile defense systems."
                ],
                "1.4": [
                    "Consume highly classified intelligence briefings on near-peer adversary cyber capabilities targeting weapon system supply chains.",
                    "Analyze adversary doctrine regarding the use of cyber effects to soften targets prior to kinetic engagement."
                ],
                "2.1": [
                    "Threat model 'Logistics ERP' against advanced persistent threats (APTs) aiming to pre-position malware for wartime sabotage.",
                    "Model the threat of GPS spoofing against autonomous drone fleet navigation systems."
                ],
                "2.2": [
                    "BIA for 'Early Warning Radar' determines MTD is seconds; systems must have active-active high availability across dispersed sites.",
                    "Determine RTO for 'Field Medical Record' systems is 1 hour to support combat casualty care."
                ],
                "2.3": [
                    "Risk Register: 'Supply chain compromise of drone firmware. Impact: Critical (mission failure). Likelihood: Medium. Risk Score: 92/100.'",
                    "Risk Register: 'Adversary lateral movement from unclassified to classified networks. Impact: Critical (intelligence loss). Likelihood: Low. Risk Score: 88/100.'"
                ],
                "3.1": [
                    "Champion mandates strict Zero Trust Architecture (ZTA) and Cross-Domain Solutions (CDS) standards.",
                    "CSO gap analysis reveals over-reliance on perimeter defense; initiate project for identity-based micro-segmentation."
                ],
                "4.1": [
                    "Operate a 24/7 Joint Cyber Defense SOC that correlates network anomalies with geopolitical threat levels to adjust defensive postures dynamically.",
                    "Deploy specialized sensors to monitor RF spectrum for jamming or Command Link intrusion attempts."
                ],
                "4.2": [
                    "Conduct quarterly 'Cyber Readiness Reviews' with military leadership, adjusting risk appetites based on current DEFCON levels.",
                    "Re-measure risks immediately after any new adversary cyber capability is revealed in intelligence reports."
                ],
                "4.3": [
                    "Intelligence indicates imminent targeting of a specific defense contractor. Immediately deploy hunt teams to their networks to sweep for indicators of compromise.",
                    "Disconnect compromised non-essential logistics systems during active conflict to prevent lateral movement to C2 systems."
                ],
                "4.4": [
                    "Submit classified 'Cyber Force Posture' reports to National Security leadership, detailing the combat readiness of critical digital systems.",
                    "Report on the cyber-resilience of the Defense Industrial Base (DIB) partners."
                ]
            },
            "Energy": {
                "1.1": [
                    "Draft mission: 'To guarantee the continuous, secure operation and control of the national power grid and water desalination plants.'",
                    "Set goal to ensure 100% of critical substation communications are encrypted and authenticated by next year."
                ],
                "1.2": [
                    "Use OT-specific discovery tools to map 'Crown Jewels' like substation RTUs and Grid Control Center SCADA servers.",
                    "Deconstruct 'Power Generation' into services like 'Turbine Control', 'Voltage Regulation', and 'Environmental Monitoring'."
                ],
                "1.3": [
                    "Perform non-intrusive vulnerability assessments on live grid control systems during scheduled maintenance windows only.",
                    "Scan for exposed DNP3 or Modbus ports on internet-facing cellular gateways used for remote metering."
                ],
                "1.4": [
                    "Analyze threat intel for malware specifically designed to interact with electrical grid protocols (e.g., IEC 61850, CrashOverride malware).",
                    "Track groups known for targeting energy sector aiming for coercive political leverage."
                ],
                "2.1": [
                    "Threat model the 'Distributed Energy Resource Management System' (DERMS) against attacks aiming to destabilize grid frequency via botnets of solar inverters.",
                    "Model physical access threats to remote, unmanned substations."
                ],
                "2.2": [
                    "BIA for 'National Load Dispatch Centre' determines MTD is under 5 minutes to prevent cascading national blackouts.",
                    "Determine RTO for restoring a hacked smart meter network is 24 hours before billing data is irretrievably lost."
                ],
                "2.3": [
                    "Risk Register: 'Insider threat gaining remote access to switchgear. Impact: Critical (physical damage/blackout). Likelihood: Low. Risk Score: 75/100.'",
                    "Risk Register: 'Coordinated attack on desalination plant PLCs. Impact: Critical (national water shortage). Likelihood: Medium. Risk Score: 90/100.'"
                ],
                "3.1": [
                    "Champion mandates NERC-CIP equivalent standards for all high-impact bulk electric systems.",
                    "CSO gap analysis shows weak controls on legacy smart meters; launch program to upgrade firmware signing infrastructure."
                ],
                "4.1": [
                    "Establish a sector-wide view of grid control network traffic to spot coordinated probing activities across multiple utility providers.",
                    "Monitor energy usage patterns for anomalies that might indicate manipulation of demand-response systems."
                ],
                "4.2": [
                    "Review risks regarding renewable energy integration, assessing how new IoT-enabled solar farms increase the sector attack surface.",
                    "Hold annual 'Black Start' tabletop exercises to measure the realistic recovery time from a total grid cyber-outage."
                ],
                "4.3": [
                    "Upon detecting a novel ICS malware strain, immediately island critical generation segments and revert to manual grid management procedures.",
                    "Coordinate fuel resupply priorities for backup generators during a prolonged cyber-induced outage."
                ],
                "4.4": [
                    "Report to regulators on 'Grid Blackstart Resilience', detailing capabilities to recover from a catastrophic cyber-induced power failure.",
                    "Provide public-facing dashboards showing current grid stability without revealing sensitive operational details."
                ]
            },
            "Banking": {
                "1.1": [
                    "Draft mission: 'To ensure 99.999% integrity and availability for all national digital payment gateways and core banking ledgers.'",
                    "Strategy: Achieve real-time fraud detection on 100% of domestic transactions by 2026."
                ],
                "1.2": [
                    "Run a scan to create a 'Crown Jewels' inventory for the 'SWIFT Payment Interface', listing specific HSMs, gateway servers, and databases.",
                    "Identify all third-party APIs with read/write access to customer account data."
                ],
                "1.3": [
                    "Perform continuous authenticated scanning and daily penetration testing on internet-facing mobile banking API endpoints.",
                    "Conduct regular audits of open-source libraries used in proprietary trading platforms for known vulnerabilities."
                ],
                "1.4": [
                    "Subscribe to FS-ISAC feeds to track financially motivated threat groups (e.g., FIN7, Lazarus) and their evolving ransomware TTPs.",
                    "Monitor dark web forums for specialized banking trojans targeting domestic bank customers."
                ],
                "2.1": [
                    "Threat model 'High-Value Wire Transfer' systems against business logic abuse and sophisticated insider collusion scenarios.",
                    "Model attacks against automated loan approval AI models (adversarial machine learning)."
                ],
                "2.2": [
                    "BIA for 'Real-Time Gross Settlement (RTGS)' system determines MTD is 2 hours; beyond this, national liquidity markets freeze.",
                    "Determine RPO for 'Core Ledger' is zero; data loss is unacceptable under any circumstances."
                ],
                "2.3": [
                    "Risk Register: 'Compromise of third-party ATM software update mechanism. Impact: High. Likelihood: Medium. Risk Score: 85/100.'",
                    "Risk Register: 'Data integrity attack on core ledger backups. Impact: Catastrophic (bank collapse). Likelihood: Very Low. Risk Score: 80/100.'"
                ],
                "3.1": [
                    "Champion mandates PCI-DSS 4.0 compliance plus bespoke controls for national payment switches.",
                    "CSO gap analysis shows weak API security; implement strict OAuth2.0 and rate limiting on all open banking interfaces."
                ],
                "4.1": [
                    "Aggregate anonymized transaction fraud alerts from all major banks to identify sector-wide 'cash-out' schemes in real-time.",
                    "Deploy User Behavior Analytics (UBA) to detect compromised insider accounts accessing dormant high-value accounts."
                ],
                "4.2": [
                    "Monthly 'Financial Stability Risk Committee' reviews aggregated systemic risks, such as concentration risk in a shared cloud provider.",
                    "Reassess risk scores based on economic indicators that might increase the likelihood of desperate cyber-criminal activity."
                ],
                "4.3": [
                    "A major bank suffers a DDoS. Champion coordinates traffic scrubbing at the national ISP level to protect the wider financial ecosystem.",
                    "Activate the 'Sector Shelter Protocol', isolating a compromised bank from the national payment switch to prevent contagion."
                ],
                "4.4": [
                    "Provide 'Consumer Confidence' reports to the Central Bank, detailing metrics on successful fraud prevention and uptime of digital payment rails.",
                    "Report on the aggregated cyber insurance exposure of the entire banking sector."
                ]
            },
            "Trade & Investments": {
                "1.1": [
                    "Establish mission: 'To maintain the integrity, fairness, and continuous operation of national stock exchanges and trade logistics platforms.'",
                    "Goal: Ensure trade matching engines have <1ms latency variance even under active DDoS attack conditions."
                ],
                "1.2": [
                    "Inventory assets supporting 'High-Frequency Trading Engines', focusing on ultra-low latency network switches and matching engine servers.",
                    "Map the complete data lineage for 'Regulatory Trade Reporting' systems to ensure accuracy."
                ],
                "1.3": [
                    "Scan for time-drift vulnerabilities in trading servers, as compromised clocks can destroy non-repudiation in trade execution.",
                    "Test resilience of algorithmic trading APIs against fuzzed inputs designed to cause crashes or erratic trades."
                ],
                "1.4": [
                    "Monitor for threats aiming to manipulate market data feeds (ticker plants) to trigger automated algorithmic sell-offs.",
                    "Track 'pump and dump' schemes organized on social media that leverage cyber-intrusions to maximize profit."
                ],
                "2.1": [
                    "Threat model 'Central Securities Depository' against attacks aiming to corrupt ownership records, which would cause irreversible economic chaos.",
                    "Model insider threats from developers with access to trading algorithm source code."
                ],
                "2.2": [
                    "BIA for the 'National Stock Exchange' determines MTD is 0 minutes during trading hours; any outage damages global investor confidence.",
                    "RTO for post-trade clearing and settlement systems is set to 4 hours to ensure end-of-day completion."
                ],
                "2.3": [
                    "Risk Register: 'Integrity attack on market data feed. Impact: Critical (market crash). Likelihood: Low. Risk Score: 80/100.'",
                    "Risk Register: 'Ransomware on trade clearing house. Impact: Critical (settlement failure). Likelihood: Medium. Risk Score: 90/100.'"
                ],
                "3.1": [
                    "Champion mandates strict controls on algorithmic trading bot testing and validation.",
                    "CSO gap analysis reveals weak pre-production testing; enforce mandatory sandbox testing for all new trading algorithms."
                ],
                "4.1": [
                    "Monitor trade volume anomalies in real-time that might indicate a cyber-induced 'flash crash' rather than normal market behavior.",
                    "Oversee a 'Market Integrity SOC' that specifically looks for correlations between cyber events and unusual stock price movements."
                ],
                "4.2": [
                    "Quarterly reviews with major brokerages to assess risks related to shared dependencies on specific clearing house technologies.",
                    "Reassess risks when new complex financial instruments (e.g., crypto-derivatives) are introduced to the exchange."
                ],
                "4.3": [
                    "Detect data corruption in trade logs. Immediately halt trading (trip circuit breakers) and activate immutable backup restoration procedures.",
                    "Issue a sector-wide ban on a specific compromised third-party trading software until it is re-certified."
                ],
                "4.4": [
                    "Report to Financial Regulators on 'Market Infrastructure Integrity', proving that trade data remains uncompromised by cyber actors.",
                    "Publish transparency reports for international investors detailing the cybersecurity robustness of the national exchange."
                ]
            },
            "Telecommunications": {
                "1.1": [
                    "Draft mission: 'To provide resilient, continuous voice and data connectivity for citizens, emergency services, and national defense.'",
                    "Goal: Maintain 99.99% availability of cellular networks during national crisis scenarios."
                ],
                "1.2": [
                    "Map 'Crown Jewels' for the 'National Backbone Core', including core BGP routers, HLR/HSS databases for mobile subscriber data, and undersea cable landing stations.",
                    "Identify all physical cell towers that provide sole coverage to critical military or government facilities."
                ],
                "1.3": [
                    "Continuously scan for vulnerabilities in 5G network slices and virtualized network functions (VNFs) that could allow tenant cross-over.",
                    "Audit physical security controls at remote, unstaffed landing stations and repeater sites."
                ],
                "1.4": [
                    "Track threats targeting SS7/Diameter protocols used for tracking user location or intercepting SMS 2FA codes.",
                    "Monitor for APTs attempting to implant firmware backdoors in core routing equipment."
                ],
                "2.1": [
                    "Threat model 'Lawful Intercept' interfaces against unauthorized access by foreign intelligence aiming to spy on domestic officials.",
                    "Model threats to the Over-The-Air (OTA) update mechanism for SIM cards."
                ],
                "2.2": [
                    "BIA for '999/Emergency Services Routing' determines MTD is zero; calls must always connect, requiring extreme redundancy.",
                    "Determine RTO for a major undersea cable cut is 24 hours (rerouting capacity), but RPO for billing data can be 24 hours."
                ],
                "2.3": [
                    "Risk Register: 'BGP Hijacking of national prefixes. Impact: High (data interception). Likelihood: Medium. Risk Score: 88/100.'",
                    "Risk Register: 'State-sponsored compromise of HLR/HSS. Impact: Critical (national outage). Likelihood: Low. Risk Score: 92/100.'"
                ],
                "3.1": [
                    "Champion mandates RPKI for BGP route validation across all domestic carriers.",
                    "CSO gap analysis shows legacy equipment lacking RPKI support; plan phased hardware refresh for core routers."
                ],
                "4.1": [
                    "Establish a sector SOC monitoring national internet traffic flows to rapidly identify and scrub massive DDoS attacks before they saturate international links.",
                    "Monitor for unauthorized IMSI catchers (Stingrays) operating near sensitive government locations."
                ],
                "4.2": [
                    "Review risks associated with high-risk vendors in the 5G supply chain during bi-annual 'Infrastructure Security' meetings.",
                    "Reassess resilience scores based on periodic 'Chaos Engineering' tests on the national backbone."
                ],
                "4.3": [
                    "A major fiber cut is identified as sabotage. Coordinate immediate traffic rerouting via satellite and terrestrial redundancy.",
                    "Blacklist compromised international peers that are repeatedly sourcing malicious route advertisements."
                ],
                "4.4": [
                    "Produce 'National Connectivity Health' reports showing latency, packet loss, and successful deflection of nation-state level intercept attempts.",
                    "Report to national security council on the physical and cyber security of undersea cable infrastructure."
                ]
            },
            "National IT Infrastructure": {
                "1.1": [
                    "Draft mission: 'To ensure the resilience and trust of foundational digital services, including national cloud, digital identity, and root DNS.'",
                    "Strategy: Establish absolute digital sovereignty over all citizen identity data by 2026."
                ],
                "1.2": [
                    "Inventory assets for the 'National Root CA', including offline root keys, issuing CAs, and associated Hardware Security Modules (HSMs).",
                    "Map the entire dependency tree of the 'Government Cloud' platform, including underlying hypervisors and storage arrays."
                ],
                "1.3": [
                    "Perform rigorous code review and fuzz testing on the APIs used by all other sectors to validate digital Citizen IDs.",
                    "Scan for misconfigurations in the national DNSSEC deployment that could lead to widespread validation failures."
                ],
                "1.4": [
                    "Monitor for APTs specifically targeting Managed Service Providers (MSPs) and cloud infrastructure to gain broad access to downstream government tenants.",
                    "Analyze threats against cryptographic standards, preparing for post-quantum decryption capabilities."
                ],
                "2.1": [
                    "Threat model 'Government Cloud Hypervisors' against container escape vulnerabilities that could compromise multiple tenant ministries.",
                    "Model insider attacks against the physical ceremony processes for Root CA key generation."
                ],
                "2.2": [
                    "BIA for 'Top-Level Domain (.gov) DNS' determines MTD is 15 minutes; loss breaks all government digital presence.",
                    "RTO for National Identity authentication services is <5 minutes to avoid halting all public sector digital activity."
                ],
                "2.3": [
                    "Risk Register: 'Compromise of National Identity root key. Impact: Catastrophic (total loss of digital trust). Likelihood: Very Low. Risk Score: 95/100.'",
                    "Risk Register: 'Cloud provider administrative account compromise. Impact: Critical (multi-tenant breach). Likelihood: Low. Risk Score: 90/100.'"
                ],
                "3.1": [
                    "Champion mandates multi-person integrity controls (M-of-N) for all root administrative actions.",
                    "CSO gap analysis reveals single-admin access to some backup systems; implement quorum authorization immediately."
                ],
                "4.1": [
                    "Monitor authentication logs across the national ID ecosystem to detect credential stuffing or impossible travel anomalies at a population scale.",
                    "Deploy integrity monitoring on all core DNS zone files to detect unauthorized changes instantly."
                ],
                "4.2": [
                    "Convene 'Digital Trust Architecture' reviews to assess cryptographic agility risks (e.g., post-quantum readiness of national PKI).",
                    "Review systemic risk posed by concentration of all government services in a single cloud region."
                ],
                "4.3": [
                    "Detect a rogue certificate issued by a compromised intermediate CA. Immediately revoke it via OCSP and trigger automated trust-store updates nationwide.",
                    "Isolate a compromised segment of the government cloud while migrating critical tenants to a disaster recovery region."
                ],
                "4.4": [
                    "Report on 'Sovereign Cloud Integrity', detailing assurance levels of data residency and immunity from foreign legal jurisdiction data requests.",
                    "Publish public transparency reports on government data access requests to maintain citizen trust."
                ]
            },
            "Healthcare": {
                "1.1": [
                    "Draft mission: 'To protect patient safety and privacy by ensuring the availability of life-critical medical systems and integrity of health records.'",
                    "Goal: Ensure zero patient mortality due to cyber-induced failure of connected medical devices."
                ],
                "1.2": [
                    "Inventory 'Crown Jewels' including Electronic Health Record (EHR) databases and network-connected life-support devices (IoMT) in ICUs.",
                    "Map the data flow of Laboratory Information Systems (LIS) which are critical for timely diagnoses."
                ],
                "1.3": [
                    "Scan for unpatched legacy operating systems often found on MRI machines and other expensive, long-lifecycle medical equipment.",
                    "Audit access controls for telemedicine platforms to prevent unauthorized joining of patient consultations."
                ],
                "1.4": [
                    "Track ransomware groups known to target hospitals (e.g., Conti, Ryuk), understanding their tactics for disabling backups to force payment.",
                    "Monitor for theft of medical research data by state actors, especially during pandemics."
                ],
                "2.1": [
                    "Threat model 'Picture Archiving and Communication Systems' (PACS) against attacks that could alter medical images, leading to misdiagnosis.",
                    "Model attacks on automated medication dispensing cabinets that could lead to incorrect dosing."
                ],
                "2.2": [
                    "BIA for 'Emergency Department Admission Systems' determines MTD is 1 hour before patient care is significantly compromised (revert to paper).",
                    "RPO for active patient vitals monitoring history must be <5 minutes."
                ],
                "2.3": [
                    "Risk Register: 'Ransomware locking ventilator control network. Impact: Critical (loss of life). Likelihood: Low. Risk Score: 98/100.'",
                    "Risk Register: 'Mass leak of patient psychological records. Impact: High (privacy/trust). Likelihood: Medium. Risk Score: 85/100.'"
                ],
                "3.1": [
                    "Champion mandates strict network segmentation for all IoMT (Internet of Medical Things) devices.",
                    "CSO gap analysis shows poor segregation; launch project to NAC (Network Access Control) all medical devices into isolated VLANs."
                ],
                "4.1": [
                    "Monitor hospital networks for unusual outbound traffic from medical devices, which might indicate they have been compromised into a botnet.",
                    "Track access patterns to VIP patient records to detect insider snooping."
                ],
                "4.2": [
                    "Quarterly 'Clinical Cyber Risk' reviews with Chief Medical Officers to translate digital risks into patient safety terminology.",
                    "Reassess risks when integrating new hospital wings or after mergers with other healthcare providers."
                ],
                "4.3": [
                    "During a ransomware outbreak, coordinate the sector-wide diversion of ambulances from impacted hospitals to unaffected ones.",
                    "Activate 'Code Dark' protocols to physically disconnect critical diagnostic equipment during an active attack."
                ],
                "4.4": [
                    "Report to the Ministry of Health on 'Digital Patient Safety', tracking metrics on medical device patching levels and resilience to outages.",
                    "Provide assurance reports on the anonymization effectiveness of health data shared for research purposes."
                ]
            },
            "Food Supply": {
                "1.1": [
                    "Draft mission: 'To ensure the continuous, safe production and distribution of food and water to prevent national shortages and panic.'",
                    "Goal: Guarantee 30 days of resilient food supply distribution even under total national internet outage conditions."
                ],
                "1.2": [
                    "Map assets for 'Just-in-Time Distribution Centers', including automated warehouse robots and inventory management ERPs.",
                    "Inventory OT systems in large-scale industrial bakeries and dairy processing plants."
                ],
                "1.3": [
                    "Scan OT systems in food processing plants, looking for exposed PLCs controlling temperature (cold chain) or ingredient mixing ratios.",
                    "Vulnerability check on GPS systems used for automated agriculture (precision farming) equipment."
                ],
                "1.4": [
                    "Monitor for cyber-criminal activity targeting logistics aggregators, where a single attack could halt nationwide supermarket deliveries.",
                    "Analyze threats of 'agro-terrorism' where cyberattacks are used to spoil massive quantities of food."
                ],
                "2.1": [
                    "Threat model 'Cold Chain Monitoring IoT' against attacks that could spoof temperature data, causing massive spoilage of perishable goods.",
                    "Model attacks on ingredients labeling systems that could hide allergen information, risking public health."
                ],
                "2.2": [
                    "BIA for 'Centralized Order Processing' determines MTD is 4 hours; delays beyond this cause empty shelves within 24 hours due to lean supply chains.",
                    "RTO for automated warehouse control systems is 2 hours to avoid massive backlog of perishable goods."
                ],
                "2.3": [
                    "Risk Register: 'Manipulation of allergen data in production PLCs. Impact: Critical (public health/recalls). Likelihood: Low. Risk Score: 85/100.'",
                    "Risk Register: 'Ransomware on major food logistics hub. Impact: High (national shortages). Likelihood: Medium. Risk Score: 88/100.'"
                ],
                "3.1": [
                    "Champion mandates offline, tested backups for 'National Food Reserves' inventory data.",
                    "CSO gap analysis shows over-reliance on cloud-synced backups vulnerable to ransomware; implement immutable on-prem storage."
                ],
                "4.1": [
                    "Aggregate data from major logistics providers to spot sector-wide disruptions in transport management systems simultaneously.",
                    "Monitor for unusual changes in reported inventory levels that don't match physical intake/outtake data."
                ],
                "4.2": [
                    "Review risks related to concentration of supply, such as reliance on a single digital platform for grain import/export management.",
                    "Reassess risks seasonally, as impacts of disruption are higher during harvest or major holidays."
                ],
                "4.3": [
                    "A major dairy processor is hit by ransomware. Activate national contingency plans to reroute raw milk to alternative facilities.",
                    "Issue public advisories if a cyberattack might have compromised food safety data (e.g., sterilization times)."
                ],
                "4.4": [
                    "Report to government on 'National Food Security Resilience', detailing the ability of the sector to switch to manual logistics in a crisis.",
                    "Provide assurance on the integrity of the national seed bank digital records."
                ]
            }
        };

        const sectorSelect = document.getElementById('sectorSelect');
        const sectorNameIntro = document.getElementById('sector-name-intro');
        const sectorNameBody = document.getElementById('sector-name-body');

        function updateContent() {
            const selectedSector = sectorSelect.value;
            const data = sectorData[selectedSector];

            // Update Sector Names
            sectorNameIntro.textContent = selectedSector;
            sectorNameBody.textContent = selectedSector;

            // Update all examples with a fade effect and bullet list
            for (const [key, valueArray] of Object.entries(data)) {
                const el = document.getElementById(`ex-${key}`);
                if (el) {
                    // Reset animation and content
                    el.classList.remove('fade-in');
                    void el.offsetWidth; // Trigger reflow
                    el.classList.add('fade-in');
                    el.innerHTML = ''; // Clear previous content

                    // Create unordered list for multiple examples
                    const ul = document.createElement('ul');
                    ul.className = 'list-disc list-outside ml-4 space-y-2';

                    valueArray.forEach(exampleText => {
                        const li = document.createElement('li');
                        li.textContent = exampleText;
                        ul.appendChild(li);[scrfguidance.html](https://github.com/user-attachments/files/25018144/scrfguidance.html)

                    });

                    el.appendChild(ul);
                }
            }
        }

        // Initial load
        updateContent();

        // Event listener
        sectorSelect.addEventListener('change', updateContent);
    </script>
</body>
</html>
