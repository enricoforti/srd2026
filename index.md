<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stillman Research Day 2026</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');

        :root {
            --bg-color: #f8fafc;
            --text-main: #0f172a;
            --text-muted: #475569;
            --accent: #2563eb;
            --accent-hover: #1d4ed8;
            --surface: #ffffff;
            --border: #e2e8f0;
            --radius: 16px;
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            line-height: 1.6;
            -webkit-font-smoothing: antialiased;
            scroll-behavior: smooth;
        }

        a {
            text-decoration: none;
            color: var(--accent);
            transition: var(--transition);
        }

        a:hover {
            color: var(--accent-hover);
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* Navbar */
        nav {
            background-color: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(12px);
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid var(--border);
            padding: 16px 0;
        }

        .nav-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .nav-logo {
            font-weight: 700;
            font-size: 1.25rem;
            color: var(--text-main);
            letter-spacing: -0.5px;
        }

        .nav-links {
            display: flex;
            gap: 32px;
        }

        .nav-links a {
            color: var(--text-muted);
            font-weight: 500;
            font-size: 0.95rem;
        }

        .nav-links a:hover {
            color: var(--accent);
        }

        /* Buttons */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 14px 32px;
            font-weight: 600;
            border-radius: 50px;
            cursor: pointer;
            transition: var(--transition);
            border: none;
            font-size: 1rem;
            text-align: center;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--accent) 0%, #3b82f6 100%);
            color: #fff;
            box-shadow: 0 4px 14px 0 rgba(37, 99, 235, 0.39);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 24px rgba(37, 99, 235, 0.3);
            color: #fff;
        }

        .btn-secondary {
            background: var(--surface);
            color: var(--text-main);
            border: 1px solid var(--border);
        }

        .btn-secondary:hover {
            border-color: var(--accent);
            color: var(--accent);
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 100px 0 60px;
        }

        .tagline {
            display: inline-block;
            background: #e0e7ff;
            color: var(--accent);
            padding: 6px 16px;
            border-radius: 50px;
            font-size: 0.85rem;
            font-weight: 600;
            letter-spacing: 0.5px;
            text-transform: uppercase;
            margin-bottom: 24px;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 5vw, 4rem);
            font-weight: 800;
            letter-spacing: -1.5px;
            margin-bottom: 24px;
            line-height: 1.1;
        }

        .hero p {
            font-size: 1.25rem;
            color: var(--text-muted);
            max-width: 700px;
            margin: 0 auto 32px;
        }

        .event-meta {
            display: flex;
            justify-content: center;
            gap: 16px;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }

        .meta-item {
            background-color: var(--surface);
            padding: 12px 24px;
            border-radius: 50px;
            border: 1px solid var(--border);
            font-size: 0.95rem;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        /* Typography Formatting */
        .section-header {
            margin-bottom: 40px;
        }

        .section-header h2 {
            font-size: 2rem;
            font-weight: 700;
            letter-spacing: -0.5px;
            margin-bottom: 12px;
        }

        .section-header p {
            color: var(--text-muted);
            font-size: 1.1rem;
        }

        /* Grids & Cards */
        .section-padding {
            padding: 80px 0;
        }

        .grid-2 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 32px;
        }

        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 24px;
        }

        .card {
            background-color: var(--surface);
            padding: 32px;
            border-radius: var(--radius);
            border: 1px solid var(--border);
            transition: var(--transition);
        }

        .card:hover {
            box-shadow: 0 10px 30px -10px rgba(0, 0, 0, 0.05);
            transform: translateY(-4px);
        }

        /* Timeline Schedule */
        .timeline {
            display: flex;
            flex-direction: column;
            gap: 24px;
        }

        .timeline-item {
            background: var(--surface);
            border-radius: var(--radius);
            border: 1px solid var(--border);
            padding: 32px;
            display: flex;
            gap: 32px;
            transition: var(--transition);
        }

        .timeline-item:hover {
            border-color: #cbd5e1;
            box-shadow: 0 4px 20px -10px rgba(0,0,0,0.05);
        }

        .time-badge {
            flex-shrink: 0;
            background: #f1f5f9;
            color: var(--text-main);
            padding: 8px 16px;
            border-radius: 8px;
            font-weight: 600;
            font-size: 0.9rem;
            height: fit-content;
            text-align: center;
        }

        .timeline-content h3 {
            font-size: 1.25rem;
            margin-bottom: 8px;
        }

        .timeline-content p {
            color: var(--text-muted);
            margin-bottom: 16px;
            font-size: 0.95rem;
        }

        .timeline-content ul {
            padding-left: 20px;
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        .timeline-content li {
            margin-bottom: 8px;
        }

        /* People List */
        .people-list {
            list-style: none;
        }

        .people-list li {
            padding: 16px 0;
            border-bottom: 1px solid var(--border);
            display: flex;
            flex-direction: column;
            gap: 4px;
        }

        .people-list li:last-child {
            border-bottom: none;
        }

        .person-name {
            font-weight: 600;
            color: var(--text-main);
        }

        .person-name a {
            color: var(--accent);
            text-decoration: none;
            transition: var(--transition);
        }

        .person-name a:hover {
            color: var(--accent-hover);
            text-decoration: underline;
        }

        .person-role {
            font-size: 0.9rem;
            color: var(--text-muted);
        }

        /* Call to Action */
        .cta-section {
            background: var(--text-main);
            color: #fff;
            text-align: center;
            border-radius: 24px;
            padding: 60px 40px;
            margin: 80px 0;
        }

        .cta-section h2 {
            font-size: 2.5rem;
            margin-bottom: 16px;
        }

        .cta-section p {
            color: #94a3b8;
            margin-bottom: 32px;
            font-size: 1.1rem;
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 40px 0;
            border-top: 1px solid var(--border);
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            .timeline-item {
                flex-direction: column;
                gap: 16px;
            }
            .time-badge {
                width: fit-content;
            }
            .event-meta {
                flex-direction: column;
                align-items: center;
            }
            .meta-item {
                width: 100%;
                justify-content: center;
            }
        }
    </style>
</head>
<body>

    <nav>
        <div class="container nav-content">
            <div class="nav-logo">SRD 2026</div>
            <div class="nav-links">
                <a href="#about">About</a>
                <a href="#schedule">Schedule</a>
                <a href="#people">People</a>
            </div>
            <a href="https://forms.cloud.microsoft/r/VRBahh5Y5F" target="_blank" class="btn btn-primary" style="padding: 8px 20px; font-size: 0.9rem;">Register</a>
        </div>
    </nav>

    <header class="container hero">
        <span class="tagline">Hackathon-Style Event</span>
        <h1>Stillman Research Day 2026</h1>
        <p>An opportunity to share and discuss research, catch up with colleagues, and meet new people to catalyze new publishable projects.</p>
        
        <div class="event-meta">
            <div class="meta-item">
                <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="4" width="18" height="18" rx="2" ry="2"></rect><line x1="16" y1="2" x2="16" y2="6"></line><line x1="8" y1="2" x2="8" y2="6"></line><line x1="3" y1="10" x2="21" y2="10"></line></svg>
                May 5, 2026 &middot; 2:00 PM – 5:30 PM ET
            </div>
            <div class="meta-item">
                <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"></path><circle cx="12" cy="10" r="3"></circle></svg>
                Jubilee Hall, 4th Floor Atrium
            </div>
        </div>

        <div style="display: flex; gap: 16px; justify-content: center;">
            <a href="https://forms.cloud.microsoft/r/VRBahh5Y5F" target="_blank" class="btn btn-primary">Save Your Spot</a>
            <a href="#schedule" class="btn btn-secondary">View Schedule</a>
        </div>
    </header>

    <section id="about" class="container section-padding">
        <div class="section-header text-center" style="text-align: center; max-width: 800px; margin: 0 auto 60px;">
            <h2>Growing Research Seeds</h2>
            <p>An in-person, half-day event designed to catalyze new research by using a flipped format. Faculty members share upfront research "seeds", and participants brainstorm concrete next steps.</p>
        </div>

        <div class="grid-3">
            <div class="card">
                <h3>🔍 A Research Question</h3>
                <p>A research question in search of an empirical strategy.</p>
            </div>
            <div class="card">
                <h3>📐 A Method</h3>
                <p>A specific method looking for research applications.</p>
            </div>
            <div class="card">
                <h3>📊 Some Data</h3>
                <p>A dataset with underexplored potential.</p>
            </div>
        </div>
    </section>

    <section id="schedule" class="container section-padding">
        <div class="section-header">
            <h2>Event Format & Structure</h2>
            <p>Pre-registration by May 1, 2026 is highly recommended to facilitate breakout sessions.</p>
        </div>

        <div class="timeline">
            <div class="timeline-item">
                <div class="time-badge">10 mins</div>
                <div class="timeline-content">
                    <h3>Introduction & Overview</h3>
                    <p>Brief introduction on the hackathon-style format presented by Enrico Forti.</p>
                </div>
            </div>

            <div class="timeline-item">
                <div class="time-badge">80 mins</div>
                <div class="timeline-content">
                    <h3>Part 1 — "Seeding" Macro & Micro Perspectives</h3>
                    <p>Faculty participants share a max 5-minute plenary presentation introducing a specific research "seed".</p>
                    <p style="color: var(--text-muted); font-size: 0.95rem; font-weight: 600; margin-bottom: 8px;">Featured Seed Contributors:</p>
                    <ul style="margin-bottom: 16px; display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 8px;">
                        <li>Jennifer Itzkowitz</li>
                        <li>Shen Zhang</li>
                        <li>Nicolas Dahan</li>
                        <li>Debra Lee Surface</li>
                        <li>Daniel Ladik</li>
                        <li>Ryan Ellis</li>
                        <li>Katri Nousiainen</li>
                        <li>Hector Lozada-Vega</li>
                    </ul>
                    <ul>
                        <li>Organizers review roundtables & worksheet templates</li>
                    </ul>
                </div>
            </div>

            <div class="timeline-item">
                <div class="time-badge">90 mins</div>
                <div class="timeline-content" style="width: 100%;">
                    <h3>Part 2 — Growing the Research Seeds</h3>
                    <p>Groups of participants collaboratively develop research designs. Each breakout table focuses on one “seed” (introduced in Part 1). Each table is led by a faculty participant using a structured worksheet including: (1) problem definition, (2) theoretical anchors, (3) methodological options, (4) potential datasets, and (5) next-step planning. Each roundtable is also assisted by a student volunteer acting as facilitator.</p>
                    
                    <h4 style="margin: 20px 0 10px; font-size: 1rem; color: var(--text-main);">Structure of breakout time:</h4>
                    <ul style="margin-bottom: 20px;">
                        <li><strong>Stage 1 (35 minutes):</strong> Idea generation and theoretical framing</li>
                        <li><strong>Stage 2 (35 minutes):</strong> Methods, data sources, research design sketches</li>
                        <li><strong>Mini break (5 minutes)</strong></li>
                        <li><strong>Stage 3 (20 minutes):</strong> Refining contributions and next steps</li>
                    </ul>

                    <p style="margin-bottom: 24px;">Participants are matched to faculty leads via pre-registration (preferred), but walk-in participants are also welcome. An onboarding pipeline (using QR codes) has been developed for facilitating the integration of both pre-registered and walk-in participants.</p>

                    <h4 style="margin: 24px 0 16px; font-size: 1rem; color: var(--text-main);">Seed Round-tables:</h4>
                    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 16px; margin-bottom: 24px;">
                        
                        <div style="background: #f1f5f9; padding: 16px; border-radius: 12px; border: 1px solid var(--border);">
                            <div style="font-weight: 600; font-size: 0.95rem; margin-bottom: 8px; color: var(--text-main);">Table 1. Title TBC</div>
                            <div style="font-size: 0.85rem; color: var(--text-muted);"><strong>Contributor:</strong> Shen Zhang<br><strong>Facilitator:</strong> TBC</div>
                        </div>

                        <div style="background: #f1f5f9; padding: 16px; border-radius: 12px; border: 1px solid var(--border);">
                            <div style="font-weight: 600; font-size: 0.95rem; margin-bottom: 8px; color: var(--text-main);">Table 2. Title TBC</div>
                            <div style="font-size: 0.85rem; color: var(--text-muted);"><strong>Contributor:</strong> Nicolas Dahan<br><strong>Facilitator:</strong> TBC</div>
                        </div>

                        <div style="background: #f1f5f9; padding: 16px; border-radius: 12px; border: 1px solid var(--border);">
                            <div style="font-weight: 600; font-size: 0.95rem; margin-bottom: 8px; line-height: 1.4; color: var(--text-main);">Table 3. How do firms recover from service failures in B2B relationships?</div>
                            <div style="font-size: 0.85rem; color: var(--text-muted);"><strong>Contributor:</strong> Debra Lee Surface<br><strong>Facilitator:</strong> TBC</div>
                        </div>

                        <div style="background: #f1f5f9; padding: 16px; border-radius: 12px; border: 1px solid var(--border);">
                            <div style="font-weight: 600; font-size: 0.95rem; margin-bottom: 8px; line-height: 1.4; color: var(--text-main);">Table 4. Behavioral Finance in Action: Evidence from Individual Investor Data</div>
                            <div style="font-size: 0.85rem; color: var(--text-muted);"><strong>Contributor:</strong> Jennifer Itzkowitz<br><strong>Facilitator:</strong> TBC</div>
                        </div>

                        <div style="background: #f1f5f9; padding: 16px; border-radius: 12px; border: 1px solid var(--border);">
                            <div style="font-weight: 600; font-size: 0.95rem; margin-bottom: 8px; color: var(--text-main);">Table 5. Title TBC</div>
                            <div style="font-size: 0.85rem; color: var(--text-muted);"><strong>Contributor:</strong> Daniel Ladik<br><strong>Facilitator:</strong> TBC</div>
                        </div>

                        <div style="background: #f1f5f9; padding: 16px; border-radius: 12px; border: 1px solid var(--border);">
                            <div style="font-weight: 600; font-size: 0.95rem; margin-bottom: 8px; line-height: 1.4; color: var(--text-main);">Table 6. Using Mobile Phone Data in Economics and Business Research</div>
                            <div style="font-size: 0.85rem; color: var(--text-muted);"><strong>Contributor:</strong> Ryan Ellis<br><strong>Facilitator:</strong> TBC</div>
                        </div>

                        <div style="background: #f1f5f9; padding: 16px; border-radius: 12px; border: 1px solid var(--border);">
                            <div style="font-weight: 600; font-size: 0.95rem; margin-bottom: 8px; color: var(--text-main);">Table 7. Quantum Roadmap in Law</div>
                            <div style="font-size: 0.85rem; color: var(--text-muted);"><strong>Contributor:</strong> Katri Nousiainen<br><strong>Facilitator:</strong> TBC</div>
                        </div>

                        <div style="background: #f1f5f9; padding: 16px; border-radius: 12px; border: 1px solid var(--border);">
                            <div style="font-weight: 600; font-size: 0.95rem; margin-bottom: 8px; color: var(--text-main);">Table 8. TBC</div>
                            <div style="font-size: 0.85rem; color: var(--text-muted);"><strong>Contributor:</strong> Hector Lozada-Vega<br><strong>Facilitator:</strong> TBC</div>
                        </div>
                    </div>

                    <div style="background: #e0e7ff; padding: 16px; border-radius: 12px; border-left: 4px solid var(--accent); color: var(--text-main); font-size: 0.95rem;">
                        <strong>Table Assignment:</strong> TBD based on pre-registration. Faculty leads may want to document key ideas and outputs to support cross-table synthesis and follow-up collaboration.
                    </div>
                </div>
            </div>

            <div class="timeline-item">
                <div class="time-badge">10 mins</div>
                <div class="timeline-content">
                    <h3>Wrap-Up & Reflections</h3>
                    <p>Final synthesis of the breakout roundtable outputs.</p>
                </div>
            </div>

            <div class="timeline-item">
                <div class="time-badge">90 mins</div>
                <div class="timeline-content">
                    <h3>Networking Reception</h3>
                    <p>Join us at the Jubilee Hall, 4th Floor Atrium and Terrazza to continue the conversation.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="people" class="container section-padding">
        <div class="section-header">
            <h2>People Behind the Event</h2>
        </div>

        <div class="grid-3">
            <div class="card">
                <h3 style="margin-bottom: 24px; border-bottom: 1px solid var(--border); padding-bottom: 12px;">Organizers</h3>
                <ul class="people-list">
                    <li><span class="person-name"><a href="https://www.shu.edu/profiles/fortienr.html" target="_blank">Enrico Forti</a></span><span class="person-role">Assistant Professor of Strategy</span></li>
                    <li><span class="person-name"><a href="https://www.shu.edu/profiles/zhangsh3.html" target="_blank">Shen Zhang</a></span><span class="person-role">Assistant Professor of Finance</span></li>
                    <li><span class="person-name"><a href="https://www.shu.edu/profiles/dahannic.html" target="_blank">Nicolas Dahan</a></span><span class="person-role">Assistant Professor of Management</span></li>
                    <li><span class="person-name"><a href="https://www.shu.edu/profiles/surfacde.html" target="_blank">Debra Lee Surface</a></span><span class="person-role">Assistant Professor of Marketing</span></li>
                </ul>
            </div>

            <div class="card">
                <h3 style="margin-bottom: 24px; border-bottom: 1px solid var(--border); padding-bottom: 12px;">Seed Contributors</h3>
                <ul class="people-list">
                    <li><span class="person-name"><a href="https://www.shu.edu/profiles/jenniferitzkowitz.html" target="_blank">Jennifer Itzkowitz</a></span><span class="person-role">Professor of Finance</span></li>
                    <li><span class="person-name"><a href="https://www.shu.edu/profiles/zhangsh3.html" target="_blank">Shen Zhang</a></span><span class="person-role">Assistant Professor of Finance</span></li>
                    <li><span class="person-name"><a href="https://www.shu.edu/profiles/dahannic.html" target="_blank">Nicolas Dahan</a></span><span class="person-role">Assistant Professor of Management</span></li>
                    <li><span class="person-name"><a href="https://www.shu.edu/profiles/surfacde.html" target="_blank">Debra Lee Surface</a></span><span class="person-role">Assistant Professor of Marketing</span></li>
                    <li><span class="person-name"><a href="https://www.shu.edu/profiles/danielladik.html" target="_blank">Daniel Ladik</a></span><span class="person-role">Associate Professor of Marketing</span></li>
                    <li><span class="person-name"><a href="https://www.shu.edu/profiles/ellisrya.html" target="_blank">Ryan Ellis</a></span><span class="person-role">Assistant Professor of Economics</span></li>
                    <li><span class="person-name"><a href="https://www.shu.edu/profiles/nousiaka.html" target="_blank">Katri Nousiainen</a></span><span class="person-role">Assistant Professor in Economics & Legal Studies</span></li>
                    <li><span class="person-name"><a href="https://www.shu.edu/profiles/hectorlozadavega.html" target="_blank">Hector Lozada-Vega</a></span><span class="person-role">Associate Professor of Marketing</span></li>
                </ul>
            </div>

            <div class="card">
                <h3 style="margin-bottom: 24px; border-bottom: 1px solid var(--border); padding-bottom: 12px;">Facilitators & Support</h3>
                <ul class="people-list">
                    <li><span class="person-name">Grace Iannacone</span><span class="person-role">Student Facilitator</span></li>
                    <li><span class="person-name">Nicole Voltmer</span><span class="person-role">Student Facilitator</span></li>
                    <li><span class="person-name">6x Students</span><span class="person-role">Student Facilitators (TBC)</span></li>
                    <li><span class="person-name">Melody Puliti</span><span class="person-role">Organizational Support</span></li>
                </ul>
            </div>
        </div>
    </section>

    <div class="container">
        <div class="cta-section">
            <h2>Ready to catalyze new research?</h2>
            <p>All are welcome! Students with high potential and curiosity are particularly encouraged to participate.</p>
            <a href="https://forms.cloud.microsoft/r/VRBahh5Y5F" target="_blank" class="btn btn-primary" style="background: #fff; color: var(--text-main); box-shadow: 0 4px 14px 0 rgba(0,0,0,0.1);">Register by May 1, 2026</a>
        </div>
    </div>

    <footer>
        <div class="container">
            <p>&copy; 2026 Stillman School of Business, Seton Hall University. All rights reserved.</p>
        </div>
    </footer>

</body>
</html>
