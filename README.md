<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Sultan Zaib · README</title>
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0d1117;
            display: flex;
            justify-content: center;
            padding: 2rem 1rem;
            font-family: 'JetBrains Mono', 'Fira Code', monospace;
        }

        .readme-container {
            max-width: 1000px;
            width: 100%;
            background: #0d1117;
            color: #c9d1d9;
            border-radius: 24px;
            padding: 2rem 1.5rem;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.8);
            border: 1px solid #21262d;
        }

        /* ---- scrollbar ---- */
        .readme-container::-webkit-scrollbar {
            width: 6px;
        }
        .readme-container::-webkit-scrollbar-track {
            background: #0d1117;
        }
        .readme-container::-webkit-scrollbar-thumb {
            background: #30363d;
            border-radius: 8px;
        }

        /* ---- headings ---- */
        h1,
        h2,
        h3 {
            font-weight: 600;
            letter-spacing: 0.5px;
        }

        .glow-text {
            text-shadow: 0 0 8px rgba(88, 166, 255, 0.3), 0 0 20px rgba(88, 166, 255, 0.1);
        }

        /* ---- dividers ---- */
        .divider-glow {
            height: 2px;
            background: linear-gradient(90deg, transparent, #58a6ff, #1f6feb, #58a6ff, transparent);
            margin: 1.8rem 0;
            border: none;
            border-radius: 4px;
            opacity: 0.7;
        }

        /* ---- cards ---- */
        .card-dark {
            background: #161b22;
            border-radius: 16px;
            padding: 1.5rem 1.8rem;
            border: 1px solid #21262d;
            box-shadow: 0 8px 24px rgba(0, 0, 0, 0.4);
            transition: 0.2s ease;
        }

        .card-dark:hover {
            border-color: #30363d;
            box-shadow: 0 12px 32px rgba(0, 0, 0, 0.6);
        }

        /* ---- code blocks ---- */
        pre {
            background: #0d1117;
            border-radius: 12px;
            padding: 1.2rem 1.5rem;
            border: 1px solid #21262d;
            overflow-x: auto;
            font-size: 0.85rem;
            line-height: 1.6;
            color: #e6edf3;
            font-family: 'JetBrains Mono', monospace;
        }

        pre .label {
            color: #58a6ff;
        }
        pre .value {
            color: #f0883e;
        }
        pre .comment {
            color: #8b949e;
            font-style: italic;
        }
        pre .keyword {
            color: #ff7b72;
        }
        pre .string {
            color: #a5d6ff;
        }
        pre .number {
            color: #f0883e;
        }

        /* ---- badges ---- */
        .badge-group {
            display: flex;
            flex-wrap: wrap;
            gap: 0.6rem 0.9rem;
            justify-content: center;
            margin: 1.2rem 0;
        }

        .badge-group a {
            text-decoration: none;
            transition: 0.2s ease;
            display: inline-block;
        }

        .badge-group a:hover {
            transform: translateY(-3px) scale(1.02);
            filter: brightness(1.2);
        }

        /* ---- table ---- */
        .tech-table {
            width: 100%;
            border-collapse: collapse;
            font-size: 0.9rem;
        }

        .tech-table td {
            padding: 0.5rem 0.8rem;
            border-bottom: 1px solid #21262d;
        }

        .tech-table tr:last-child td {
            border-bottom: none;
        }

        .tech-table .key {
            color: #8b949e;
            font-weight: 400;
            width: 38%;
        }
        .tech-table .value {
            color: #e6edf3;
            font-weight: 500;
            width: 62%;
        }

        /* ---- responsive ---- */
        @media (max-width: 640px) {
            .readme-container {
                padding: 1rem 0.8rem;
            }
            .card-dark {
                padding: 1rem 1rem;
            }
            pre {
                font-size: 0.7rem;
                padding: 0.8rem 1rem;
            }
        }

        /* ---- animated gradient line ---- */
        .gradient-line {
            height: 2px;
            background: linear-gradient(90deg, #58a6ff, #1f6feb, #58a6ff);
            background-size: 200% 100%;
            animation: shimmer 3s infinite linear;
            border: none;
            border-radius: 4px;
            margin: 1.5rem 0;
        }

        @keyframes shimmer {
            0% {
                background-position: -200% 0;
            }
            100% {
                background-position: 200% 0;
            }
        }

        /* ---- typing wrapper ---- */
        .typing-wrapper {
            display: flex;
            justify-content: center;
            margin: 0.5rem 0;
        }

        .typing-wrapper img {
            max-width: 100%;
            height: auto;
        }

        /* ---- small caps ---- */
        .section-tag {
            font-size: 0.7rem;
            letter-spacing: 2px;
            text-transform: uppercase;
            color: #58a6ff;
            font-weight: 500;
            opacity: 0.8;
        }

        /* ---- flex row ---- */
        .flex-stats {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1.2rem;
            margin: 1.5rem 0;
        }

        .flex-stats img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
        }

        /* ---- snake container ---- */
        .snake-container {
            background: #0d1117;
            border-radius: 16px;
            overflow: hidden;
            border: 1px solid #21262d;
            margin: 1rem 0;
        }

        .snake-container img {
            display: block;
            width: 100%;
            height: auto;
        }

        /* ---- footer wave ---- */
        .footer-wave {
            margin-top: 2rem;
            border-radius: 0 0 16px 16px;
            overflow: hidden;
        }

        .footer-wave img {
            display: block;
            width: 100%;
            height: auto;
        }

        /* ---- activity graph ---- */
        .activity-graph {
            border-radius: 16px;
            overflow: hidden;
            border: 1px solid #21262d;
            background: #0d1117;
        }

        .activity-graph img {
            display: block;
            width: 100%;
            height: auto;
        }

        /* ---- center ---- */
        .text-center {
            text-align: center;
        }

        .mt-1 {
            margin-top: 1rem;
        }
        .mt-2 {
            margin-top: 2rem;
        }
        .mb-1 {
            margin-bottom: 1rem;
        }
        .mb-2 {
            margin-bottom: 2rem;
        }
    </style>
</head>
<body>

    <div class="readme-container">

        <!-- ============================================================ -->
        <!--  TOP : TYPING ANIMATION + BANNER                              -->
        <!-- ============================================================ -->

        <div align="center">

            <!-- main animated roles -->
            <img
            src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=800&size=28&duration=2200&pause=650&color=58A6FF&center=true&vCenter=true&width=900&lines=SULTAN+ZAIB;PYTHON+ENGINEER;DJANGO+ENGINEER;BACKEND+ENGINEER;REST+API+ENGINEER;SOFTWARE+ENGINEER;BUILDING+BACKEND+SYSTEMS"
            alt="Sultan Zaib Animated Roles"
            />

            <br />

            <!-- subtle divider -->
            <img
            src="https://capsule-render.vercel.app/api?type=rect&color=gradient&height=2&section=header"
            width="85%"
            />

            <br /><br />

            <!-- ASCII / banner card -->
            <div class="card-dark" style="display:inline-block; text-align:left; max-width:100%;">
                <pre style="background:transparent; border:none; padding:0.5rem 0; font-size:0.8rem; line-height:1.5;">
                    <span style="color:#58a6ff;">┌──────────────────────────────────────────────────────────────────────────────┐</span>
                    <span style="color:#58a6ff;">│</span>                                                                              <span style="color:#58a6ff;">│</span>
                    <span style="color:#58a6ff;">│</span>   <span style="color:#f0f6fc; font-weight:700;">S U L T A N   Z A I B</span>                                                     <span style="color:#58a6ff;">│</span>
                    <span style="color:#58a6ff;">│</span>   <span style="color:#30363d;">───────────────────────────────────────────────────────────────────────</span>   <span style="color:#58a6ff;">│</span>
                    <span style="color:#58a6ff;">│</span>                                                                              <span style="color:#58a6ff;">│</span>
                    <span style="color:#58a6ff;">│</span>   <span style="color:#58a6ff;">PYTHON</span>  /  <span style="color:#f0883e;">DJANGO</span>  /  <span style="color:#a5d6ff;">REST APIs</span>  /  <span style="color:#3fb950;">DATABASES</span>  /  <span style="color:#f0883e;">BACKEND</span>         <span style="color:#58a6ff;">│</span>
                    <span style="color:#58a6ff;">│</span>                                                                              <span style="color:#58a6ff;">│</span>
                    <span style="color:#58a6ff;">│</span>   <span style="color:#8b949e;">BUILD  →  DEBUG  →  UNDERSTAND  →  IMPROVE  →  SHIP</span>                     <span style="color:#58a6ff;">│</span>
                    <span style="color:#58a6ff;">│</span>                                                                              <span style="color:#58a6ff;">│</span>
                    <span style="color:#58a6ff;">└──────────────────────────────────────────────────────────────────────────────┘</span>
                </pre>
            </div>

            <br />

            <!-- secondary typing : philosophy -->
            <img
            src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=16&duration=2600&pause=900&color=8B949E&center=true&vCenter=true&width=850&lines=Turning+ideas+into+working+software.;Learning+by+building+real+projects.;Understanding+the+problem+before+fixing+the+code."
            alt="Animated Developer Statement"
            />

            <br /><br />

            <!-- social badges -->
            <div class="badge-group">
                <a href="https://github.com/szofficiall">
                    <img src="https://img.shields.io/badge/GITHUB-szofficiall-161B22?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
                </a>
                <a href="https://www.linkedin.com/in/sultan-zaib/">
                    <img src="https://img.shields.io/badge/LINKEDIN-Sultan%20Zaib-161B22?style=for-the-badge&logo=linkedin&logoColor=0A66C2" alt="LinkedIn" />
                </a>
                <a href="mailto:sultan.zaib.dev@gmail.com">
                    <img src="https://img.shields.io/badge/EMAIL-CONTACT-161B22?style=for-the-badge&logo=gmail&logoColor=EA4335" alt="Email" />
                </a>
            </div>

        </div>

        <!-- ============================================================ -->
        <!--  SECTION 01 : IDENTITY                                        -->
        <!-- ============================================================ -->

        <div class="divider-glow"></div>

        <div align="center">
            <span class="section-tag">01 / IDENTITY</span>
            <img
            src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&duration=2400&pause=800&color=58A6FF&center=true&vCenter=true&width=720&lines=WHO+IS+SULTAN+ZAIB%3F;PYTHON+%E2%86%92+DJANGO+%E2%86%92+BACKEND;CODE+WITH+PURPOSE"
            alt="Identity Animation"
            />
        </div>

        <div class="card-dark mt-1">
            <pre style="background:transparent; border:none; padding:0; font-size:0.9rem;">
                <span style="color:#58a6ff; font-weight:600;">SULTAN ZAIB</span>
                <span style="color:#30363d;">────────────────────────────────────────────────────────</span>

                <span style="color:#8b949e;">Role</span>
                <span style="color:#f0f6fc;">Python Engineer → Django Engineer → Backend Engineer</span>

                <span style="color:#8b949e;">Primary Focus</span>
                <span style="color:#f0f6fc;">Python • Django • REST APIs • Databases • Backend Systems</span>

                <span style="color:#8b949e;">Engineering Philosophy</span>
                <span style="color:#f0f6fc;">Understand the problem.</span>
                <span style="color:#f0f6fc;">Build the solution.</span>
                <span style="color:#f0f6fc;">Debug the failure.</span>
                <span style="color:#f0f6fc;">Improve the system.</span>

                <span style="color:#8b949e;">Current Direction</span>
                <span style="color:#f0f6fc;">Backend Engineering → API Development → System Design</span>
            </pre>
            <p style="color:#8b949e; font-size:0.95rem; margin-top:0.5rem;">
                I am a <strong style="color:#58a6ff;">Python/Django-focused</strong> Software Engineer interested in building reliable, database-driven applications, REST APIs and backend systems.
            </p>
            <blockquote style="border-left:3px solid #58a6ff; padding-left:1.2rem; color:#8b949e; margin:0.8rem 0; font-style:italic;">
                I don't just want to fix an error. I want to understand why it happened.
            </blockquote>
        </div>

        <!-- ============================================================ -->
        <!--  SECTION 02 : ENGINEERING MINDSET                             -->
        <!-- ============================================================ -->

        <div class="divider-glow"></div>

        <div align="center">
            <span class="section-tag">02 / ENGINEERING MINDSET</span>
            <img
            src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&duration=2300&pause=700&color=3776AB&center=true&vCenter=true&width=750&lines=LEARN;BUILD;BREAK;DEBUG;UNDERSTAND;IMPROVE;SHIP"
            alt="Engineering Mindset Animation"
            />
        </div>

        <div class="card-dark mt-1">
            <pre style="background:transparent; border:none; padding:0; font-size:0.85rem; line-height:1.7;">
                <span style="color:#8b949e;">                         ┌──────────────┐</span>
                <span style="color:#8b949e;">                         │    LEARN     │</span>
                <span style="color:#8b949e;">                         └──────┬───────┘</span>
                <span style="color:#8b949e;">                                │</span>
                <span style="color:#8b949e;">                                ▼</span>
                <span style="color:#8b949e;">                         ┌──────────────┐</span>
                <span style="color:#8b949e;">                         │    BUILD     │</span>
                <span style="color:#8b949e;">                         └──────┬───────┘</span>
                <span style="color:#8b949e;">                                │</span>
                <span style="color:#8b949e;">                                ▼</span>
                <span style="color:#8b949e;">                         ┌──────────────┐</span>
                <span style="color:#8b949e;">                         │    BREAK     │</span>
                <span style="color:#8b949e;">                         └──────┬───────┘</span>
                <span style="color:#8b949e;">                                │</span>
                <span style="color:#8b949e;">                                ▼</span>
                <span style="color:#8b949e;">                         ┌──────────────┐</span>
                <span style="color:#8b949e;">                         │    DEBUG     │</span>
                <span style="color:#8b949e;">                         └──────┬───────┘</span>
                <span style="color:#8b949e;">                                │</span>
                <span style="color:#8b949e;">                                ▼</span>
                <span style="color:#8b949e;">                         ┌──────────────┐</span>
                <span style="color:#8b949e;">                         │  UNDERSTAND  │</span>
                <span style="color:#8b949e;">                         └──────┬───────┘</span>
                <span style="color:#8b949e;">                                │</span>
                <span style="color:#8b949e;">                                ▼</span>
                <span style="color:#8b949e;">                         ┌──────────────┐</span>
                <span style="color:#8b949e;">                         │   IMPROVE    │</span>
                <span style="color:#8b949e;">                         └──────┬───────┘</span>
                <span style="color:#8b949e;">                                │</span>
                <span style="color:#8b949e;">                                ▼</span>
                <span style="color:#8b949e;">                         ┌──────────────┐</span>
                <span style="color:#8b949e;">                         │     SHIP     │</span>
                <span style="color:#8b949e;">                         └──────┬───────┘</span>
                <span style="color:#8b949e;">                                │</span>
                <span style="color:#8b949e;">                                └──────────────→ REPEAT</span>
            </pre>
        </div>

        <!-- ============================================================ -->
        <!--  SECTION 03 : CORE STACK                                      -->
        <!-- ============================================================ -->

        <div class="divider-glow"></div>

        <div align="center">
            <span class="section-tag">03 / CORE STACK</span>
            <img
            src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&duration=2500&pause=750&color=58A6FF&center=true&vCenter=true&width=800&lines=THE+TOOLS+I+BUILD+WITH;PYTHON+%2B+DJANGO+%2B+REST;DATABASES+%2B+ORM+%2B+APIs;FROM+REQUEST+TO+DATABASE"
            alt="Core Stack Animation"
            />
            <br /><br />
            <img
            src="https://skillicons.dev/icons?i=python,django,fastapi,mysql,sqlite,postgres,git,github,postman&perline=9"
            alt="Core Backend Technologies"
            />
        </div>

        <div class="card-dark mt-1">
            <div style="display:flex; flex-wrap:wrap; gap:1.5rem;">
                <div style="flex:1 1 200px;">
                    <h4 style="color:#58a6ff; margin-bottom:0.5rem;">Backend</h4>
                    <ul style="list-style:none; padding:0; color:#c9d1d9; font-size:0.9rem; line-height:1.8;">
                        <li>Python</li>
                        <li>Django</li>
                        <li>Django REST Framework</li>
                        <li>FastAPI</li>
                        <li>Django ORM</li>
                        <li>REST APIs</li>
                        <li>Authentication</li>
                        <li>CRUD · Middleware · Signals</li>
                    </ul>
                </div>
                <div style="flex:1 1 200px;">
                    <h4 style="color:#58a6ff; margin-bottom:0.5rem;">Databases</h4>
                    <ul style="list-style:none; padding:0; color:#c9d1d9; font-size:0.9rem; line-height:1.8;">
                        <li>MySQL</li>
                        <li>SQLite</li>
                        <li>PostgreSQL</li>
                        <li>Database Design</li>
                        <li>Relationships · Queries</li>
                    </ul>
                </div>
                <div style="flex:1 1 200px;">
                    <h4 style="color:#58a6ff; margin-bottom:0.5rem;">Frontend</h4>
                    <ul style="list-style:none; padding:0; color:#c9d1d9; font-size:0.9rem; line-height:1.8;">
                        <li>HTML · CSS · JS</li>
                        <li>React</li>
                        <li>Bootstrap</li>
                        <li>Tailwind CSS</li>
                    </ul>
                </div>
                <div style="flex:1 1 200px;">
                    <h4 style="color:#58a6ff; margin-bottom:0.5rem;">Dev &amp; Deployment</h4>
                    <ul style="list-style:none; padding:0; color:#c9d1d9; font-size:0.9rem; line-height:1.8;">
                        <li>Git · GitHub</li>
                        <li>Postman · VS Code</li>
                        <li>npm · pip</li>
                        <li>AWS · Vercel · Netlify</li>
                        <li>Gunicorn · Whitenoise</li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- ============================================================ -->
        <!--  SECTION 04 : BACKEND ARCHITECTURE                            -->
        <!-- ============================================================ -->

        <div class="divider-glow"></div>

        <div align="center">
            <span class="section-tag">04 / BACKEND ARCHITECTURE</span>
            <img
            src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&duration=2400&pause=700&color=3776AB&center=true&vCenter=true&width=820&lines=REQUEST+COMES+IN;BUSINESS+LOGIC+DOES+THE+WORK;DATABASE+STORES+THE+STATE;RESPONSE+GOES+BACK"
            alt="Backend Architecture Animation"
            />
        </div>

        <div class="card-dark mt-1">
            <pre style="background:transparent; border:none; padding:0; font-size:0.8rem; line-height:1.6;">
                <span style="color:#8b949e;">                           CLIENT</span>
                <span style="color:#8b949e;">                              │</span>
                <span style="color:#8b949e;">                              │ HTTP</span>
                <span style="color:#8b949e;">                              ▼</span>
                <span style="color:#8b949e;">                     ┌─────────────────┐</span>
                <span style="color:#8b949e;">                     │      URLS       │</span>
                <span style="color:#8b949e;">                     └────────┬────────┘</span>
                <span style="color:#8b949e;">                              │</span>
                <span style="color:#8b949e;">                              ▼</span>
                <span style="color:#8b949e;">                     ┌─────────────────┐</span>
                <span style="color:#8b949e;">                     │      VIEW       │</span>
                <span style="color:#8b949e;">                     └────────┬────────┘</span>
                <span style="color:#8b949e;">                              │</span>
                <span style="color:#8b949e;">                    ┌─────────┴─────────┐</span>
                <span style="color:#8b949e;">                    │                   │</span>
                <span style="color:#8b949e;">                    ▼                   ▼</span>
                <span style="color:#8b949e;">             ┌─────────────┐      ┌─────────────┐</span>
                <span style="color:#8b949e;">             │    FORMS    │      │     API     │</span>
                <span style="color:#8b949e;">             └──────┬──────┘      └──────┬──────┘</span>
                <span style="color:#8b949e;">                    │                    │</span>
                <span style="color:#8b949e;">                    └─────────┬──────────┘</span>
                <span style="color:#8b949e;">                              │</span>
                <span style="color:#8b949e;">                              ▼</span>
                <span style="color:#8b949e;">                     ┌─────────────────┐</span>
                <span style="color:#8b949e;">                     │  BUSINESS LOGIC │</span>
                <span style="color:#8b949e;">                     └────────┬────────┘</span>
                <span style="color:#8b949e;">                              │</span>
                <span style="color:#8b949e;">                              ▼</span>
                <span style="color:#8b949e;">                     ┌─────────────────┐</span>
                <span style="color:#8b949e;">                     │   DJANGO ORM    │</span>
                <span style="color:#8b949e;">                     └────────┬────────┘</span>
                <span style="color:#8b949e;">                              │</span>
                <span style="color:#8b949e;">                              ▼</span>
                <span style="color:#8b949e;">                     ┌─────────────────┐</span>
                <span style="color:#8b949e;">                     │    DATABASE     │</span>
                <span style="color:#8b949e;">                     └─────────────────┘</span>
            </pre>
        </div>

        <!-- ============================================================ -->
        <!--  SECTION 05 : PROJECT LAB                                     -->
        <!-- ============================================================ -->

        <div class="divider-glow"></div>

        <div align="center">
            <span class="section-tag">05 / PROJECT LAB</span>
            <img
            src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&duration=2400&pause=750&color=58A6FF&center=true&vCenter=true&width=850&lines=REAL+PROJECTS;REAL+PROBLEMS;REAL+DJANGO;LEARNING+BY+BUILDING"
            alt="Project Lab Animation"
            />
        </div>

        <div class="card-dark mt-1">
            <div style="display:grid; grid-template-columns:1fr; gap:1.2rem;">
                <!-- 01 -->
                <div style="border-left:3px solid #58a6ff; padding-left:1rem;">
                    <span style="color:#58a6ff; font-weight:600;">01</span> <span style="color:#f0f6fc; font-weight:500;">Django Signals &amp; Admin Blog Manager</span>
                    <div style="font-size:0.8rem; color:#8b949e; margin-top:0.2rem;">pre_save / post_save · Blog Models · Admin Customization · Database Automation</div>
                </div>
                <!-- 02 -->
                <div style="border-left:3px solid #f0883e; padding-left:1rem;">
                    <span style="color:#f0883e; font-weight:600;">02</span> <span style="color:#f0f6fc; font-weight:500;">Django Authentication Starter</span>
                    <div style="font-size:0.8rem; color:#8b949e; margin-top:0.2rem;">Registration · Login / Logout · Protected Views · User Management</div>
                </div>
                <!-- 03 -->
                <div style="border-left:3px solid #a5d6ff; padding-left:1rem;">
                    <span style="color:#a5d6ff; font-weight:600;">03</span> <span style="color:#f0f6fc; font-weight:500;">Django Middleware Made Simple</span>
                    <div style="font-size:0.8rem; color:#8b949e; margin-top:0.2rem;">Custom Middleware · Request/Response Processing · Security · Clickjacking</div>
                </div>
                <!-- 04 -->
                <div style="border-left:3px solid #3fb950; padding-left:1rem;">
                    <span style="color:#3fb950; font-weight:600;">04</span> <span style="color:#f0f6fc; font-weight:500;">Django Blog Post Manager</span>
                    <div style="font-size:0.8rem; color:#8b949e; margin-top:0.2rem;">CRUD · Search · Filtering · Pagination · Django ORM</div>
                </div>
                <!-- 05 -->
                <div style="border-left:3px solid #f0883e; padding-left:1rem;">
                    <span style="color:#f0883e; font-weight:600;">05</span> <span style="color:#f0f6fc; font-weight:500;">Student Management System</span>
                    <div style="font-size:0.8rem; color:#8b949e; margin-top:0.2rem;">Student Records · CRUD · Database Management · Django ORM · Admin</div>
                </div>
                <!-- 06 -->
                <div style="border-left:3px solid #58a6ff; padding-left:1rem;">
                    <span style="color:#58a6ff; font-weight:600;">06</span> <span style="color:#f0f6fc; font-weight:500;">Django Todo Task Manager</span>
                    <div style="font-size:0.8rem; color:#8b949e; margin-top:0.2rem;">Create · Update · Delete · Complete/Incomplete · Search</div>
                </div>
                <!-- 07 -->
                <div style="border-left:3px solid #a5d6ff; padding-left:1rem;">
                    <span style="color:#a5d6ff; font-weight:600;">07</span> <span style="color:#f0f6fc; font-weight:500;">Recipe CRUD Application</span>
                    <div style="font-size:0.8rem; color:#8b949e; margin-top:0.2rem;">Recipe Management · CRUD · Search · Authentication · SQLite</div>
                </div>
            </div>
        </div>

        <!-- ============================================================ -->
        <!--  SECTION 06 : DEVELOPMENT LOOP                                -->
        <!-- ============================================================ -->

        <div class="divider-glow"></div>

        <div align="center">
            <span class="section-tag">06 / DEVELOPMENT LOOP</span>
            <img
            src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&duration=2200&pause=650&color=3776AB&center=true&vCenter=true&width=850&lines=WRITE+THE+CODE;RUN+THE+CODE;READ+THE+ERROR;FIND+THE+CAUSE;FIX+THE+CAUSE;LEARN+FROM+THE+BUG"
            alt="Development Loop Animation"
            />
        </div>

        <div class="card-dark mt-1">
            <pre style="background:transparent; border:none; padding:0; font-size:0.85rem; line-height:1.7;">
                <span style="color:#8b949e;">┌───────────────────────────────────────────────────────────────┐</span>
                <span style="color:#8b949e;">│                                                               │</span>
                <span style="color:#8b949e;">│  <span style="color:#58a6ff;">IDEA</span>                                                        │</span>
                <span style="color:#8b949e;">│   ↓                                                           │</span>
                <span style="color:#8b949e;">│  <span style="color:#f0883e;">DESIGN</span>                                                      │</span>
                <span style="color:#8b949e;">│   ↓                                                           │</span>
                <span style="color:#8b949e;">│  <span style="color:#a5d6ff;">CODE</span>                                                        │</span>
                <span style="color:#8b949e;">│   ↓                                                           │</span>
                <span style="color:#8b949e;">│  <span style="color:#3fb950;">TEST</span>                                                        │</span>
                <span style="color:#8b949e;">│   ↓                                                           │</span>
                <span style="color:#8b949e;">│  <span style="color:#f0883e;">ERROR</span>                                                       │</span>
                <span style="color:#8b949e;">│   ↓                                                           │</span>
                <span style="color:#8b949e;">│  <span style="color:#ff7b72;">DEBUG</span>                                                       │</span>
                <span style="color:#8b949e;">│   ↓                                                           │</span>
                <span style="color:#8b949e;">│  <span style="color:#58a6ff;">UNDERSTAND</span>                                                   │</span>
                <span style="color:#8b949e;">│   ↓                                                           │</span>
                <span style="color:#8b949e;">│  <span style="color:#f0883e;">REFACTOR</span>                                                     │</span>
                <span style="color:#8b949e;">│   ↓                                                           │</span>
                <span style="color:#8b949e;">│  <span style="color:#3fb950;">SHIP</span>                                                         │</span>
                <span style="color:#8b949e;">│                                                               │</span>
                <span style="color:#8b949e;">└───────────────────────────────────────────────────────────────┘</span>
            </pre>
        </div>

        <!-- ============================================================ -->
        <!--  SECTION 07 : WHAT I BUILD                                    -->
        <!-- ============================================================ -->

        <div class="divider-glow"></div>

        <div align="center">
            <span class="section-tag">07 / WHAT I BUILD</span>
            <img
            src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&duration=2400&pause=700&color=58A6FF&center=true&vCenter=true&width=820&lines=WEB+APPLICATIONS;REST+APIs;DATABASE+SYSTEMS;AUTHENTICATION;BACKEND+LOGIC;AUTOMATION"
            alt="What I Build Animation"
            />
        </div>

        <div class="card-dark mt-1">
            <table class="tech-table">
                <tr><td class="key">Web Applications</td><td class="value">Django, Templates, Forms, CRUD</td></tr>
                <tr><td class="key">REST APIs</td><td class="value">DRF, JSON, Authentication, API Design</td></tr>
                <tr><td class="key">Databases</td><td class="value">MySQL, SQLite, PostgreSQL, ORM</td></tr>
                <tr><td class="key">Authentication</td><td class="value">Registration, Login, Permissions</td></tr>
                <tr><td class="key">Backend Logic</td><td class="value">Validation, Business Logic, Security</td></tr>
                <tr><td class="key">Automation</td><td class="value">Signals, Middleware, Admin</td></tr>
                <tr><td class="key">Development</td><td class="value">Git, GitHub, Postman, Testing</td></tr>
            </table>
        </div>

        <!-- ============================================================ -->
        <!--  SECTION 08 : CONTRIBUTION MISSION + SNAKE                    -->
        <!-- ============================================================ -->

        <div class="divider-glow"></div>

        <div align="center">
            <span class="section-tag">08 / CONTRIBUTION MISSION</span>
            <img
            src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&duration=2400&pause=700&color=3776AB&center=true&vCenter=true&width=850&lines=EVERY+COMMIT+IS+PROGRESS;KEEP+BUILDING;KEEP+LEARNING;KEEP+SHIPPING"
            alt="Contribution Mission Animation"
            />
            <br /><br />
            <div class="snake-container">
                <img
                src="https://raw.githubusercontent.com/szofficiall/szofficiall/output/github-snake-dark.svg"
                alt="Sultan Zaib GitHub Contribution Snake"
                />
            </div>
        </div>

        <!-- ============================================================ -->
        <!--  SECTION 09 : ACTIVITY MATRIX                                 -->
        <!-- ============================================================ -->

        <div class="divider-glow"></div>

        <div align="center">
            <span class="section-tag">09 / ACTIVITY MATRIX</span>
            <img
            src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=17&duration=2300&pause=700&color=58A6FF&center=true&vCenter=true&width=750&lines=CODE+ACTIVITY;CONSISTENCY;CONTRIBUTIONS;KEEP+MOVING"
            alt="Activity Matrix Animation"
            />
            <br /><br />
            <div class="activity-graph">
                <img
                src="https://github-readme-activity-graph.vercel.app/graph?username=szofficiall&theme=react-dark&hide_border=true&area=true&custom_title=SULTAN%20ZAIB%20%2F%2F%20ACTIVITY%20MATRIX"
                alt="Sultan Zaib GitHub Activity Graph"
                />
            </div>
        </div>

        <!-- ============================================================ -->
        <!--  SECTION 10 : GITHUB TELEMETRY                                -->
        <!-- ============================================================ -->

        <div class="divider-glow"></div>

        <div align="center">
            <span class="section-tag">10 / GITHUB TELEMETRY</span>
            <img
            src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=17&duration=2400&pause=700&color=3776AB&center=true&vCenter=true&width=780&lines=COMMITS;CONTRIBUTIONS;STREAK;OPEN+SOURCE;CONSISTENCY"
            alt="GitHub Telemetry Animation"
            />
            <br /><br />
            <div class="flex-stats">
                <img
                src="https://github-readme-stats.vercel.app/api?username=szofficiall&show_icons=true&include_all_commits=true&count_private=true&hide_border=true&theme=transparent&title_color=58A6FF&text_color=8B949E&icon_color=58A6FF"
                height="175"
                alt="Sultan Zaib GitHub Stats"
                />
                <img
                src="https://github-readme-streak-stats.herokuapp.com/?user=szofficiall&theme=transparent&hide_border=true&ring=58A6FF&fire=58A6FF&currStreakLabel=58A6FF"
                height="175"
                alt="Sultan Zaib GitHub Streak"
                />
            </div>
        </div>

        <!-- ============================================================ -->
        <!--  SECTION 11 : CURRENTLY LEARNING                              -->
        <!-- ============================================================ -->

        <div class="divider-glow"></div>

        <div align="center">
            <span class="section-tag">11 / CURRENTLY LEARNING</span>
            <img
            src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&duration=2500&pause=750&color=58A6FF&center=true&vCenter=true&width=850&lines=ADVANCED+PYTHON;ADVANCED+DJANGO;REST+API+DESIGN;DATABASE+DESIGN;BACKEND+ARCHITECTURE;SYSTEM+DESIGN;SCALABLE+APPLICATIONS"
            alt="Currently Learning Animation"
            />
        </div>

        <div class="card-dark mt-1">
            <pre style="background:transparent; border:none; padding:0; font-size:0.9rem; line-height:1.7;">
                <span style="color:#58a6ff; font-weight:600;">CURRENT ROADMAP</span>

                <span style="color:#f0883e;">Python</span>
                <span style="color:#8b949e;">   │</span>
                <span style="color:#8b949e;">   ▼</span>
                <span style="color:#58a6ff;">Django</span>
                <span style="color:#8b949e;">   │</span>
                <span style="color:#8b949e;">   ▼</span>
                <span style="color:#a5d6ff;">Django REST Framework</span>
                <span style="color:#8b949e;">   │</span>
                <span style="color:#8b949e;">   ▼</span>
                <span style="color:#f0883e;">REST API Engineering</span>
                <span style="color:#8b949e;">   │</span>
                <span style="color:#8b949e;">   ▼</span>
                <span style="color:#3fb950;">Database Design</span>
                <span style="color:#8b949e;">   │</span>
                <span style="color:#8b949e;">   ▼</span>
                <span style="color:#58a6ff;">Backend Architecture</span>
                <span style="color:#8b949e;">   │</span>
                <span style="color:#8b949e;">   ▼</span>
                <span style="color:#a5d6ff;">System Design</span>
                <span style="color:#8b949e;">   │</span>
                <span style="color:#8b949e;">   ▼</span>
                <span style="color:#f0883e;">Scalable Software Systems</span>
            </pre>
        </div>

        <!-- ============================================================ -->
        <!--  SECTION 12 : ENGINEERING PRINCIPLES                          -->
        <!-- ============================================================ -->

        <div class="divider-glow"></div>

        <div align="center">
            <span class="section-tag">12 / ENGINEERING PRINCIPLES</span>
        </div>

        <div class="card-dark mt-1">
            <pre style="background:transparent; border:none; padding:0; font-size:0.85rem; line-height:1.8;">
                <span style="color:#58a6ff;">01</span>  Understand before optimizing.
                <span style="color:#f0883e;">02</span>  Read the error before searching for the solution.
                <span style="color:#a5d6ff;">03</span>  Build projects instead of only watching tutorials.
                <span style="color:#3fb950;">04</span>  Learn from every bug.
                <span style="color:#f0883e;">05</span>  Keep code readable.
                <span style="color:#58a6ff;">06</span>  Prefer fundamentals over shortcuts.
                <span style="color:#a5d6ff;">07</span>  Improve the system, not only the symptom.
                <span style="color:#3fb950;">08</span>  Ship what you build.
                <span style="color:#f0883e;">09</span>  Keep learning.
                <span style="color:#58a6ff;">10</span>  Keep building.
            </pre>
        </div>

        <!-- ============================================================ -->
        <!--  SECTION 13 : CAREER PIPELINE                                 -->
        <!-- ============================================================ -->

        <div class="divider-glow"></div>

        <div align="center">
            <span class="section-tag">13 / CAREER PIPELINE</span>
            <img
            src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=19&duration=2200&pause=700&color=58A6FF&center=true&vCenter=true&width=850&lines=PYTHON+ENGINEER;DJANGO+ENGINEER;BACKEND+ENGINEER;REST+API+ENGINEER;SOFTWARE+ENGINEER;BACKEND+ARCHITECTURE;SCALABLE+SYSTEMS"
            alt="Career Pipeline Animation"
            />
        </div>

        <div class="card-dark mt-1">
            <pre style="background:transparent; border:none; padding:0; font-size:0.9rem; line-height:1.8;">
                <span style="color:#f0883e;">                 PYTHON ENGINEER</span>
                <span style="color:#8b949e;">                        │</span>
                <span style="color:#8b949e;">                        ▼</span>
                <span style="color:#58a6ff;">                 DJANGO ENGINEER</span>
                <span style="color:#8b949e;">                        │</span>
                <span style="color:#8b949e;">                        ▼</span>
                <span style="color:#a5d6ff;">                 BACKEND ENGINEER</span>
                <span style="color:#8b949e;">                        │</span>
                <span style="color:#8b949e;">                        ▼</span>
                <span style="color:#f0883e;">                REST API ENGINEER</span>
                <span style="color:#8b949e;">                        │</span>
                <span style="color:#8b949e;">                        ▼</span>
                <span style="color:#3fb950;">                SOFTWARE ENGINEER</span>
                <span style="color:#8b949e;">                        │</span>
                <span style="color:#8b949e;">                        ▼</span>
                <span style="color:#58a6ff;">              BACKEND ARCHITECTURE</span>
                <span style="color:#8b949e;">                        │</span>
                <span style="color:#8b949e;">                        ▼</span>
                <span style="color:#a5d6ff;">                 SYSTEM DESIGN</span>
                <span style="color:#8b949e;">                        │</span>
                <span style="color:#8b949e;">                        ▼</span>
                <span style="color:#f0883e;">                SCALABLE SYSTEMS</span>
            </pre>

            <div style="margin-top:1.2rem;">
                <h4 style="color:#58a6ff; font-weight:500; font-size:0.95rem;">Open To</h4>
                <div style="display:flex; flex-wrap:wrap; gap:0.4rem 1rem; color:#c9d1d9; font-size:0.9rem; margin-top:0.3rem;">
                    <span>Backend Development</span>
                    <span>Python Development</span>
                    <span>Django Development</span>
                    <span>REST API Development</span>
                    <span>Junior Backend Engineering</span>
                    <span>Software Engineering</span>
                    <span>Internship Opportunities</span>
                    <span>Freelance Projects</span>
                    <span>Collaborative Engineering</span>
                </div>
            </div>
        </div>

        <!-- ============================================================ -->
        <!--  SECTION 14 : CONNECT                                         -->
        <!-- ============================================================ -->

        <div class="divider-glow"></div>

        <div align="center">
            <span class="section-tag">14 / CONNECT</span>
            <img
            src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=17&duration=2500&pause=800&color=3776AB&center=true&vCenter=true&width=700&lines=LET'S+BUILD+SOMETHING+USEFUL.;OPEN+TO+GOOD+ENGINEERING+CONVERSATIONS."
            alt="Connect Animation"
            />
            <br /><br />
            <div class="badge-group">
                <a href="https://github.com/szofficiall">
                    <img src="https://img.shields.io/badge/GitHub-szofficiall-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
                </a>
                <a href="https://www.linkedin.com/in/sultan-zaib/">
                    <img src="https://img.shields.io/badge/LinkedIn-Sultan%20Zaib-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
                </a>
                <a href="mailto:sultan.zaib.dev@gmail.com">
                    <img src="https://img.shields.io/badge/Email-Contact-3776AB?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
                </a>
            </div>
        </div>

        <!-- ============================================================ -->
        <!--  FOOTER : WAVE + FINAL QUOTE                                  -->
        <!-- ============================================================ -->

        <div class="divider-glow"></div>

        <div align="center">
            <img
            src="https://capsule-render.vercel.app/api?type=rect&color=gradient&height=2&section=footer"
            width="85%"
            />
            <br /><br />

            <pre style="display:inline-block; background:transparent; border:none; padding:0; font-size:0.8rem; line-height:1.6; color:#8b949e;">
                <span style="color:#58a6ff;">╔══════════════════════════════════════════════════════════════════════╗</span>
                <span style="color:#58a6ff;">║                                                                      ║</span>
                <span style="color:#58a6ff;">║                         <span style="color:#f0f6fc; font-weight:600;">S U L T A N   Z A I B</span>                      ║</span>
                <span style="color:#58a6ff;">║                                                                      ║</span>
                <span style="color:#58a6ff;">║              <span style="color:#f0883e;">BUILD IT. UNDERSTAND IT. DEBUG IT.</span>                    ║</span>
                <span style="color:#58a6ff;">║                         <span style="color:#58a6ff;">IMPROVE IT.</span>                                 ║</span>
                <span style="color:#58a6ff;">║                                                                      ║</span>
                <span style="color:#58a6ff;">║        <span style="color:#8b949e;">Built with discipline, curiosity and code by Sultan Zaib.</span>    ║</span>
                <span style="color:#58a6ff;">║                                                                      ║</span>
                <span style="color:#58a6ff;">╚══════════════════════════════════════════════════════════════════════╝</span>
            </pre>

            <br />

            <img
            src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=16&duration=2800&pause=900&color=58A6FF&center=true&vCenter=true&width=850&lines=What+you+seek+is+seeking+you.;Keep+learning.+Keep+building.+Keep+improving.;One+bug.+One+lesson.+One+better+system."
            alt="Final Animated Quote"
            />

            <br /><br />

            <div class="footer-wave">
                <img
                src="https://capsule-render.vercel.app/api?type=waving&color=0:2563eb,50:1e3a8a,100:0f172a&height=120&section=footer&animation=fadeIn"
                width="100%"
                />
            </div>
        </div>

    </div>
    <!-- /readme-container -->

</body>
</html>
