<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Raven Lionhart - Professional Resume</title>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;600&family=DM+Sans:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --charcoal: #2A2A2A;
            --warm-gray: #5A5A5A;
            --light-sand: #F8F6F3;
            --accent-gold: #C4A574;
            --accent-navy: #1E3A5F;
            --pure-white: #FFFFFF;
        }

        body {
            font-family: 'DM Sans', sans-serif;
            background: linear-gradient(135deg, #F8F6F3 0%, #EDE9E3 100%);
            color: var(--charcoal);
            line-height: 1.6;
            padding: 3rem 2rem;
            min-height: 100vh;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            background: var(--pure-white);
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.08);
            animation: fadeIn 0.8s ease-out;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Header Section */
        .header {
            position: relative;
            padding: 4rem 4rem 3rem;
            background: linear-gradient(135deg, var(--accent-navy) 0%, #2C5282 100%);
            color: var(--pure-white);
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 300px;
            height: 300px;
            background: radial-gradient(circle, rgba(196, 165, 116, 0.15) 0%, transparent 70%);
            animation: pulse 6s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 0.5; }
            50% { transform: scale(1.2); opacity: 0.8; }
        }

        .header-content {
            position: relative;
            z-index: 1;
        }

        h1 {
            font-family: 'Cormorant Garamond', serif;
            font-size: 3.5rem;
            font-weight: 300;
            margin-bottom: 0.5rem;
            letter-spacing: -0.5px;
            animation: slideInLeft 0.8s ease-out 0.2s both;
        }

        @keyframes slideInLeft {
            from {
                opacity: 0;
                transform: translateX(-30px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .title {
            font-size: 1.25rem;
            font-weight: 500;
            letter-spacing: 2px;
            text-transform: uppercase;
            color: var(--accent-gold);
            margin-bottom: 2rem;
            animation: slideInLeft 0.8s ease-out 0.4s both;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            animation: slideInLeft 0.8s ease-out 0.6s both;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            font-size: 0.95rem;
        }

        .contact-icon {
            width: 24px;
            height: 24px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            flex-shrink: 0;
        }

        /* Main Content */
        .main-content {
            display: grid;
            grid-template-columns: 1fr 350px;
            gap: 0;
        }

        .primary-column {
            padding: 3rem 3rem 3rem 4rem;
        }

        .sidebar {
            background: var(--light-sand);
            padding: 3rem 2.5rem;
            border-left: 3px solid var(--accent-gold);
        }

        /* Section Styling */
        .section {
            margin-bottom: 3rem;
            animation: fadeInUp 0.6s ease-out both;
        }

        .section:nth-child(1) { animation-delay: 0.2s; }
        .section:nth-child(2) { animation-delay: 0.3s; }
        .section:nth-child(3) { animation-delay: 0.4s; }
        .section:nth-child(4) { animation-delay: 0.5s; }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .section-title {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.75rem;
            font-weight: 600;
            color: var(--accent-navy);
            margin-bottom: 1.5rem;
            padding-bottom: 0.75rem;
            border-bottom: 2px solid var(--accent-gold);
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 60px;
            height: 2px;
            background: var(--accent-navy);
        }

        /* Experience & Education Items */
        .experience-item,
        .education-item {
            margin-bottom: 2rem;
            padding-left: 1.5rem;
            border-left: 2px solid var(--accent-gold);
            transition: all 0.3s ease;
        }

        .experience-item:hover,
        .education-item:hover {
            border-left-color: var(--accent-navy);
            padding-left: 2rem;
        }

        .item-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 0.5rem;
            gap: 1rem;
        }

        .item-title {
            font-weight: 700;
            font-size: 1.1rem;
            color: var(--accent-navy);
        }

        .item-date {
            font-size: 0.9rem;
            color: var(--warm-gray);
            white-space: nowrap;
            font-weight: 500;
        }

        .item-company {
            font-weight: 500;
            color: var(--accent-gold);
            margin-bottom: 0.75rem;
        }

        .item-description {
            color: var(--warm-gray);
            font-size: 0.95rem;
            line-height: 1.7;
        }

        .item-description li {
            margin-bottom: 0.5rem;
            padding-left: 0.5rem;
        }

        /* Skills */
        .skills-grid {
            display: grid;
            gap: 1.25rem;
        }

        .skill-category {
            margin-bottom: 1.5rem;
        }

        .skill-category-title {
            font-weight: 700;
            color: var(--accent-navy);
            margin-bottom: 0.75rem;
            font-size: 0.95rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .skill-tag {
            padding: 0.4rem 0.9rem;
            background: var(--pure-white);
            border: 1px solid var(--accent-gold);
            border-radius: 20px;
            font-size: 0.85rem;
            color: var(--charcoal);
            transition: all 0.3s ease;
        }

        .skill-tag:hover {
            background: var(--accent-gold);
            color: var(--pure-white);
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(196, 165, 116, 0.3);
        }

        /* Sidebar Sections */
        .sidebar-section {
            margin-bottom: 2.5rem;
        }

        .sidebar-section-title {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.3rem;
            font-weight: 600;
            color: var(--accent-navy);
            margin-bottom: 1rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid var(--accent-gold);
        }

        .sidebar-list {
            list-style: none;
        }

        .sidebar-list li {
            padding: 0.5rem 0;
            color: var(--warm-gray);
            font-size: 0.95rem;
            display: flex;
            align-items: center;
            gap: 0.75rem;
        }

        .sidebar-list li::before {
            content: '▸';
            color: var(--accent-gold);
            font-weight: bold;
        }

        /* Language & Certifications */
        .language-item,
        .cert-item {
            margin-bottom: 0.75rem;
        }

        .language-name,
        .cert-name {
            font-weight: 600;
            color: var(--accent-navy);
        }

        .language-level,
        .cert-date {
            font-size: 0.85rem;
            color: var(--warm-gray);
        }

        /* Progress Bars */
        .progress-bar {
            height: 6px;
            background: rgba(196, 165, 116, 0.2);
            border-radius: 3px;
            overflow: hidden;
            margin-top: 0.5rem;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--accent-gold), var(--accent-navy));
            border-radius: 3px;
            transition: width 1s ease-out;
        }

        /* Responsive Design */
        @media (max-width: 968px) {
            .main-content {
                grid-template-columns: 1fr;
            }

            .sidebar {
                border-left: none;
                border-top: 3px solid var(--accent-gold);
            }

            h1 {
                font-size: 2.5rem;
            }

            .header {
                padding: 3rem 2rem;
            }

            .primary-column {
                padding: 2rem;
            }

            .sidebar {
                padding: 2rem;
            }
        }

        @media print {
            body {
                background: white;
                padding: 0;
            }

            .container {
                box-shadow: none;
            }

            .section,
            .experience-item,
            .education-item {
                page-break-inside: avoid;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <header class="header">
            <div class="header-content">
                <h1>Raven Lionhart</h1>
                <div class="title">Business Development & Technology</div>
                <div class="contact-grid">
                    <div class="contact-item">
                        <div class="contact-icon">✉</div>
                        <span>darling.lionhart@gmail.com</a></span>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">☎</div>
                        <span>(559) 476-9599</span>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">⚲</div>
                        <span>Montreal, QC</span>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">⧉</div>
                        <span>linkedin.com/in/raven-lionhart/</span>
                    </div>
                </div>
            </div>
        </header>

        <!-- Main Content -->
        <div class="main-content">
            <div class="primary-column">
                <!-- Professional Summary -->
                <section class="section">
                    <h2 class="section-title">Professional Summary</h2>
                    <p class="item-description">
                        Jack of all trades, master of some, always better than a master of none. Business and revenue systems professional with experience designing and implementing B2B sales infrastructure, automation workflows, and conversion-driven digital platforms. Combines consultative selling, CRM architecture, and technical execution to improve pipeline performance, sales efficiency, and revenue visibility. Experienced in full-cycle sales, pre-sales discovery, and international, multilingual client environments.

                </section>

                <!-- Experience -->
                <section class="section">
                    <h2 class="section-title">Professional Experience</h2>
                    
                    <div class="experience-item">
                        <div class="item-header">
                            <div>
                                <div class="item-title">Founder, Developer & Sales Director</div>
                                <div class="item-company">Lionheart Design</div>
                            </div>
                            <div class="item-date">2021 – Present</div>
                        </div>
                        <ul class="item-description">
                            <li>Founded and led a B2B digital solutions firm delivering revenue-focused websites, sales automation, and growth systems for SMB clients across the U.S. and Canada  </li>
                            <li>Designed and developed conversion-optimized websites and interactive web applications using HTML, CSS, JavaScript, and Next.js, supporting client acquisition and brand credibility</li>
                            <li>Increased client conversion rate by 40% through consultative sales approach and needs-based questioning</li>
                            <li>Conducted full sales cycles from prospecting to account management for supporting average deal sizes of  $10K–$30K ACV</li>
                            <li>Built CRM pipelines, automation workflows, and follow-up systems reducing manual sales administration by 60%</li>
                            <li>Delivered SEO and digital growth strategies generating measurable increases in organic traffic, lead quality, and revenue performance</li>
                            <li>Led digital campaigns (Google Ads, SEO, branding) achieving 20–35% average client ROI growth</li>
                            <li>Managed client negotiations, contracts, and after-sale support ensuring 95% client satisfaction</li>
                            <li>Coordinated remote contractors across design, development, and marketing to execute projects efficiently and on schedule</li>
                        </ul>
                    </div>

                    <div class="experience-item">
                        <div class="item-header">
                            <div>
                                <div class="item-title">Senior Operations Representative</div>
                                <div class="item-company">RBC Group Advantage</div>
                            </div>
                            <div class="item-date">2022 – 2024</div>
                        </div>
                        <ul class="item-description">
                            <li>Assisted VIP business clients and resolved 200+ service requests per week, maintaining 98% satisfaction rating</li>
                            <li>Identified recurring service issues, reducing escalations by 25% through proactive communication</li>
                            <li>Supported sales growth initiatives by cross-referencing client needs and recommending RBC solutions</li>
                            <li>Applied risk management, compliance, and cost optimization training to improve team workflow efficiency</li>
                            <li>Recognized for strong communication skills and consultative approach with clients and internal teams</li>
                        </ul>
                    </div>
                </section>

                <!-- Education -->
                <section class="section">
                    <h2 class="section-title">Education</h2>
                    
                    <div class="education-item">
                        <div class="item-header">
                            <div>
                                <div class="item-title">ACS, Project Management</div>
                                <div class="item-company">College Lasalle, Montreal, QC</div>
                            </div>
                            <div class="item-date">In Progress</div>
                        </div>
                    </div>

                    <div class="education-item">
                        <div class="item-header">
                            <div>
                                <div class="item-title">AEC, Entrepreneurship</div>
                                <div class="item-company">Académie Québec, Montreal, QC</div>
                            </div>
                            <div class="item-date"> </div>
                        </div>
                    </div>

                    <div class="education-item">
                        <div class="item-header">
                            <div>
                                <div class="item-title">High School Diploma (Honors, 3.5 GPA)</div>
                                <div class="item-company">San Joaquin Memorial High School, Fresno, CA</div>
                            </div>
                            <div class="item-date"> </div>
                        </div>
                    </div>
                </section>

                <!-- Projects -->
                <section class="section">
                    <h2 class="section-title">Notable Projects</h2>
                     
                    <div class="experience-item">
                        <div class="item-header">
                            <div>
                                <div class="item-title">CRM Automation &Automated Sales System (Lead-to-Close)</div>
                                <div class="item-company">Process Improvement Project</div>
                            </div>
                        </div>
                        <p class="item-description">
                            Built comprehensive automated system managing sales cycle from lead generation through outreach and follow-up, significantly improving conversion efficiency, improving lead routing and pipeline visibility and reduced manual sales administration by 70%.
                        </p>
                    </div>
                    <div class="experience-item">
                        <div class="item-header">
                            <div>
                                <div class="item-title">Web Platforms & Interactive Experiences</div>
                                <div class="item-company">Lionheart Design</div>
                            </div>
                        </div>
                        <p class="item-description">
                            Designed and engineered multiple business websites and interactive platforms, including multilingual web experiences, advanced Next.js and html interfaces with custom animations, SEO-optimized structures, and conversion-focused user flows supporting client acquisition and brand credibility, maintaining a 98% satisfaction rate.
                        </p>
                    </div>
                    
                    <div class="experience-item">
                        <div class="item-header">
                            <div>
                                <div class="item-title">Lead Magnet & Conversion Funnel Development</div>
                                <div class="item-company">B2B Demand Generation Project</div>
                            </div>
                        </div>
                        <p class="item-description">
                           Designed a high-conversion lead magnet and automated funnel integrating landing pages, CRM capture, segmented follow-ups, and qualification logic to improve inbound lead quality and sales readiness.
                        </p>
                    </div>

                    <div class="experience-item">
                        <div class="item-header">
                            <div>
                                <div class="item-title">Invoice Tracking Algorithm</div>
                                <div class="item-company">Process Improvement Technology</div>
                            </div>
                        </div>
                        <p class="item-description">
                          Developed automated algorithm tracking invoices and sending timely payment reminders to clients, improving cash flow management and reducing delayed payments
                        </p>
                    </div>
                    
                    <div class="experience-item">
                        <div class="item-header">
                            <div>
                                <div class="item-title">E-Commerce Platform Launch</div>
                                <div class="item-company">EndlessRunway Fashion</div>
                            </div>
                        </div>
                        <p class="item-description">
                            Developed and launched an e-commerce platform that achieved a complete merchandise sell-out within three weeks through conversion-focused design and optimized user flows.
                        </p>
                    </div>


                    <div class="experience-item">
                        <div class="item-header">
                            <div>
                                <div class="item-title">International Market Expansion Strategy</div>
                                <div class="item-company">Agence Sofi</div>
                            </div>
                        </div>
                        <p class="item-description">
                            Developed international expansion strategy for international recruitment agency including tri-lingual website (English, French, Arabic), ICP localization and sales messaging adaptation to support cross-border client acquisition and international growth.
                        </p>
                    </div>
                    
                    <div class="experience-item">
                        <div class="item-header">
                            <div>
                                <div class="item-title">Video-to-Content Application</div>
                                <div class="item-company">Algorithm & Transcription </div>
                            </div>
                        </div>
                        <p class="item-description">
                            Created application tool converting YouTube videos into detailed blog posts and essays, streamlining content creation workflow.
                        </p>
                    </div>

                    <div class="experience-item">
                        <div class="item-header">
                            <div>
                                <div class="item-title">3D Game Development – Unreal Engine</div>
                                <div class="item-company">Personal Technical Project</div>
                            </div>
                        </div>
                        <p class="item-description">
                            Designed and developed a fully interactive 3D medieval-themed game using Unreal Engine, including custom asset creation, environment design, and gameplay logic. Modeled and textured original assets, implemented character controls, interactions, and game mechanics, and managed the full development pipeline from concept to playable build.
                        </p>
                    </div>

                    
                    
                </section>
            </div>

            <!-- Sidebar -->
            <aside class="sidebar">
                <!-- Skills -->
                <div class="sidebar-section">
                    <h3 class="sidebar-section-title">Core Skills</h3>
                    <div class="skills-grid">
                        <div class="skill-category">
                            <div class="skill-category-title">Business & Sales</div>
                            <div class="skill-tags">
                                <span class="skill-tag">B2B Development</span>
                                <span class="skill-tag">Consultative Selling</span>
                                <span class="skill-tag">Account Management</span>
                                <span class="skill-tag">Negotiation</span>
                                <span class="skill-tag">Client Relations</span>
                            </div>
                        </div>

                        <div class="skill-category">
                            <div class="skill-category-title">Technology</div>
                            <div class="skill-tags">
                                <span class="skill-tag">HTML/CSS</span>
                                <span class="skill-tag">JavaScript</span>
                                <span class="skill-tag">TypeScript</span>
                                <span class="skill-tag">React/Next.js</span>
                                <span class="skill-tag">Three.js</span>
                                <span class="skill-tag">C++/C#</span>
                                <span class="skill-tag">Blender 3D</span>
                            </div>
                        </div>

                        <div class="skill-category">
                            <div class="skill-category-title">Digital Marketing</div>
                            <div class="skill-tags">
                                <span class="skill-tag">SEO Strategy</span>
                                <span class="skill-tag">Google Ads</span>
                                <span class="skill-tag">CRM Systems</span>
                                <span class="skill-tag">Analytics</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Languages -->
                <!-- Languages -->
                <div class="sidebar-section">
                    <h3 class="sidebar-section-title">Languages</h3>
                    <div class="language-item">
                        <div class="language-name">English</div>
                        <div class="progress-bar">
                            <div class="progress-fill" style="width: 100%;"></div>
                        </div>
                    </div>
                    <div class="language-item">
                        <div class="language-name">Arabic</div>
                        <div class="progress-bar">
                            <div class="progress-fill" style="width: 100%;"></div>
                        </div>
                    </div>
                    <div class="language-item">
                        <div class="language-name">French</div>
                        <div class="progress-bar">
                            <div class="progress-fill" style="width: 80%;"></div>
                        </div>
                    </div>
                    <div class="language-item">
                        <div class="language-name">Korean</div>
                        <div class="progress-bar">
                            <div class="progress-fill" style="width: 40%;"></div>
                        </div>
                    </div>
                </div>

                <!-- Tools & Platforms -->
                <div class="sidebar-section">
                    <h3 class="sidebar-section-title">Tools & Platforms</h3>
                    <ul class="sidebar-list">
                        <li>HubSpot, Kixie, GoHighLevel</li>
                        <li>Google Analytics, Search Ads</li>
                        <li>Adobe Creative Suite</li>
                        <li>Blender, Spline (3D)</li>
                        <li>VS Code, Git</li>
                         <li>Unreal Engine, Unity</li>
                    </ul>
                </div>

                <!-- Certifications -->
                <!-- Certifications -->
                <div class="sidebar-section">
                    <h3 class="sidebar-section-title">Certifications</h3>
                    <div class="cert-item">
                        <div class="cert-name">Kennedy-Lugar YES Program</div>
                        <div class="cert-date">U.S. Department of State</div>
                    </div>
                    <div class="cert-item">
                        <div class="cert-name">Certificate of Appreciation</div>
                        <div class="cert-date">U.S. Department of State - Bureau of Educational and Cultural Affairs</div>
                    </div>
                       <div class="cert-item">
                        <div class="cert-name">Certificate of Appreciation BUBW</div>
                        <div class="cert-date">CECF Youth Leadership Conference</div>
                    </div>
                     <div class="cert-item">
                        <div class="cert-name">Discovering Entrepreneurship</div>
                        <div class="cert-date">Cisco Networking Academy</div>
                    </div>
                    <div class="cert-item">
                        <div class="cert-name">International Economics</div>
                        <div class="cert-date">Shanghai University of International Business and Economics</div>
                    </div>
                    <div class="cert-item">
                        <div class="cert-name">CS50x Computer Science 2026</div>
                        <div class="cert-date">Harvard</div>
                    </div>
                    <div class="cert-item">
                        <div class="cert-name">Google Search Ads Certification</div>
                        <div class="cert-date">Google</div>
                    </div>
                     <div class="cert-item">
                        <div class="cert-name">Google MyBusiness Certification</div>
                        <div class="cert-date">Google</div>
                    </div>
                    <div class="cert-item">
                        <div class="cert-name">Google Analytics Certification</div>
                        <div class="cert-date">Google</div>
                    </div>
                    <div class="cert-item">
                        <div class="cert-name">Principle's Honor Roll</div>
                        <div class="cert-date">SJM</div>
                    </div>
                    <div class="cert-item">
                        <div class="cert-name">Web Design</div>
                        <div class="cert-date">Showit</div>
                    </div>
                    
                </div>

                <!-- Additional Courses -->
                <div class="sidebar-section">
                    <h3 class="sidebar-section-title">Additional Courses</h3>
                    
                    <div class="cert-item">
                        <div class="cert-name">Sales Management</div>
                        <div class="cert-date">Alison</div>
                    </div>
                    <div class="cert-item">
                        <div class="cert-name">Business Administration</div>
                        <div class="cert-date">Alison</div>
                    </div>
                    <div class="cert-item">
                        <div class="cert-name">International Business and Trade</div>
                        <div class="cert-date">Alison</div>
                    </div>
                    <div class="cert-item">
                        <div class="cert-name">Navigating International Trade Law</div>
                        <div class="cert-date">Alison</div>
                    </div>
                    <div class="cert-item">
                        <div class="cert-name">Leadership, Economics, Computer Science</div>
                        <div class="cert-date">San Joaquin Memorial</div>
                    </div>
                     <div class="cert-item">
                        <div class="cert-name">RBC Banking Training</div>
                        <div class="cert-date">Multiple courses</div>
                    </div>
                </div>

                <!-- Interests -->
                <div class="sidebar-section">
                    <h3 class="sidebar-section-title">Interests</h3>
                    <ul class="sidebar-list">
                        <li>Web Development</li>
                        <li>International Business</li>
                        <li>Sales and Marketing</li>
                        <li>Product Design</li>
                        <li>3D Design & Modeling</li>
                        <li>Game Development</li>
                        <li>Continuous Learning</li>
                    </ul>
                </div>
                
                <!-- Selected Client Feedback -->
                <div class="sidebar-section">
                    <h3 class="sidebar-section-title">Selected Client Feedback</h3>
            
                    <div class="cert-item">
                        <div class="cert-name">"Raven was amazing with communication and went above and beyond to improve not only my site's SEO but also helped improve the content and formatting of my website. I feel so much more confident with my website now! "</div>
                       
                        <div class="cert-date"> - Anna Spivak, Beauty Oasis MTL</div>
                    </div>

                     <div class="cert-item">
                        <div class="cert-name">"By far the best experience I could ask for.. Raven was very comprehensive, made sure all the details I wanted were there. I recommend everyone to make business with them as my team & i were extremely happy with the result. "</div>
                        <div class="cert-date"> - Ninebill, EndlessRunway</div>
                    </div>
                </div>
            </aside>
        </div>
    </div>

