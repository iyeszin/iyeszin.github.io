---
layout: page
title: CV & Skills
image: assets/images/pic02.JPG
nav-menu: true
---

<style>
    /* Scope everything to .cv-wrapper to protect your existing site design */
    .cv-wrapper {
        --cv-primary: #2c3e50;
        --cv-accent: #2980b9;
        --cv-bg: #fff;
        --cv-text: #333;
        font-family: 'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
        color: var(--cv-text);
        line-height: 1.6;
        width: 100%;
        box-sizing: border-box;
    }

    .cv-container {
        display: grid;
        grid-template-columns: 300px 1fr; /* Sidebar | Main Content */
        gap: 30px;
        margin-top: 20px;
        max-width: 1200px; /* Prevent it from getting too wide on large screens */
        margin-left: auto;
        margin-right: auto;
    }

    /* HEADER SECTION */
    .cv-header-card {
        grid-column: 1 / -1;
        background: var(--cv-bg);
        padding: 30px;
        border-radius: 8px;
        box-shadow: 0 2px 8px rgba(0,0,0,0.08);
        display: flex;
        align-items: center;
        justify-content: space-between;
        flex-wrap: wrap;
        gap: 20px;
    }

    .cv-title h1 {
        margin: 0 0 5px 0 !important;
        color: var(--cv-primary);
        font-size: 2.2rem;
        line-height: 1.2;
    }

    .cv-title h2 {
        margin: 0 !important;
        font-size: 1.1rem;
        color: var(--cv-accent);
        font-weight: 400;
        border: none;
    }

    .cv-btn {
        background-color: var(--cv-accent);
        color: white !important;
        padding: 10px 20px;
        text-decoration: none;
        border-radius: 5px;
        font-weight: 600;
        transition: background 0.3s;
        display: inline-block;
        border-bottom: none !important;
    }

    .cv-btn:hover {
        background-color: #1c5980;
    }

    /* SIDEBAR */
    .cv-sidebar {
        background: var(--cv-bg);
        padding: 25px;
        border-radius: 8px;
        box-shadow: 0 2px 8px rgba(0,0,0,0.08);
        height: fit-content;
    }

    .cv-section h3 {
        border-bottom: 2px solid #eee;
        padding-bottom: 10px;
        margin-bottom: 15px !important;
        color: var(--cv-primary);
        font-size: 1.1rem;
        text-transform: uppercase;
        letter-spacing: 1px;
    }

    .cv-sidebar p, .cv-sidebar a {
        font-size: 0.95rem;
        margin-bottom: 8px;
        color: var(--cv-text);
    }
    
    .cv-sidebar a {
        color: var(--cv-accent);
        text-decoration: none;
        border-bottom: none !important;
    }

    /* PILL TAGS */
    .cv-tags {
        display: flex;
        flex-wrap: wrap;
        gap: 8px;
        margin-bottom: 20px;
    }

    .cv-tag {
        background: #eef2f5;
        color: #4a5568;
        padding: 5px 10px;
        border-radius: 15px;
        font-size: 0.85rem;
        font-weight: 500;
    }

    /* ENIC-NARIC BOX */
    .cv-notice-box {
        background: #e3f2fd;
        padding: 10px;
        border-radius: 4px;
        border-left: 3px solid #2980b9;
        margin-top: 5px;
        margin-bottom: 15px;
    }

    .cv-notice-box p {
        font-size: 0.8rem;
        margin: 0;
        color: #0c5460;
        line-height: 1.3;
    }

    /* MAIN CONTENT */
    .cv-main {
        background: var(--cv-bg);
        padding: 30px;
        border-radius: 8px;
        box-shadow: 0 2px 8px rgba(0,0,0,0.08);
    }

    .cv-main h2.section-title {
        color: var(--cv-primary);
        font-size: 1.5rem;
        margin-bottom: 25px !important;
        border-left: 5px solid var(--cv-accent);
        padding-left: 15px;
        border-bottom: none;
    }

    .cv-job {
        margin-bottom: 30px;
        border-bottom: 1px solid #eee;
        padding-bottom: 20px;
    }

    .cv-job:last-child {
        border-bottom: none;
    }

    .cv-job-header {
        display: flex;
        justify-content: space-between;
        align-items: baseline;
        flex-wrap: wrap;
        margin-bottom: 10px;
    }

    .cv-job h3 {
        margin: 0 !important;
        color: #2d3748;
        font-size: 1.2rem;
    }

    .cv-company {
        color: var(--cv-accent);
        font-weight: 600;
        display: block;
        margin-top: 4px;
    }

    .cv-date {
        color: #718096;
        font-size: 0.9rem;
        font-weight: 500;
    }

    /* PROJECT LINK BUTTON */
    .cv-project-btn {
        display: inline-flex;
        align-items: center;
        margin-top: 8px;
        margin-bottom: 12px;
        padding: 6px 14px;
        background-color: #f0f7fb;
        color: var(--cv-accent) !important;
        border: 1px solid var(--cv-accent);
        border-radius: 20px;
        font-size: 0.85rem;
        font-weight: 600;
        text-decoration: none;
        transition: all 0.2s ease;
        border-bottom: 1px solid var(--cv-accent) !important;
    }

    .cv-project-btn:hover {
        background-color: var(--cv-accent);
        color: white !important;
        text-decoration: none;
    }
    
    .cv-project-icon {
        margin-right: 6px;
    }

    .cv-main ul {
        padding-left: 20px;
        margin-top: 10px;
    }

    .cv-main li {
        margin-bottom: 8px;
        color: #4a5568;
    }

    /* RESPONSIVE */
    @media (max-width: 768px) {
        .cv-container {
            grid-template-columns: 1fr;
        }
        .cv-header-card {
            flex-direction: column;
            text-align: center;
            align-items: center;
        }
    }
</style>

<div class="cv-wrapper">

    <div class="cv-container">
        <div class="cv-header-card">
            <div class="cv-title">
                <h1>Iye Szin ANG</h1>
                <h2>Technical Project Coordinator | AI Product Owner | Data Analyst</h2>
            </div>
            <div>
                <a href="https://iyeszin.github.io/CV_IyeSzinAng.pdf" class="cv-btn" target="_blank">Download PDF Resume</a>
            </div>
        </div>
    </div>

    <div class="cv-container">
        
        <div class="cv-sidebar">
            <div class="cv-section">
                <h3>Contact</h3>
                <p>📍 Leoben, Austria (Open to Relocation) </p>
                <p>📧 <a href="mailto:iyeszin@gmail.com">iyeszin@gmail.com</a> </p>
                <p>🔗 <a href="https://www.linkedin.com/in/iyeszin/">LinkedIn Profile</a></p>
                <p>📂 <a href="projects.html">View Portfolio</a></p>
            </div>

            <div class="cv-section">
                <h3>Data & AI Stack</h3>
                <div class="cv-tags">
                    <span class="cv-tag">Python</span>
                    <span class="cv-tag">SQL</span>
                    <span class="cv-tag">Tableau</span>
                    <span class="cv-tag">Pandas / NumPy</span>
                    <span class="cv-tag">SciPy</span>
                    <span class="cv-tag">TensorFlow</span>
                    <span class="cv-tag">PyTorch</span>
                    <span class="cv-tag">Scikit-learn</span>
                </div>
            </div>

            <div class="cv-section">
                <h3>Product & Mgmt</h3>
                <div class="cv-tags">
                    <span class="cv-tag">Agile / Scrum</span>
                    <span class="cv-tag">Requirements</span>
                    <span class="cv-tag">Stakeholder Mgmt</span>
                    <span class="cv-tag">R&D Mgmt</span>
                    <span class="cv-tag">Risk Mitigation</span>
                    <span class="cv-tag">Jira / Trello</span>
                </div>
            </div>

            <div class="cv-section">
                <h3>Education</h3>
                <p><strong>M.Sc. Photonics & Intelligent Vision</strong><br>
                <span style="font-size: 0.85rem; color: #666;">Erasmus Mundus (2021-2023) </span></p>
                
                <div class="cv-notice-box">
                    <p><strong>🇦🇹 Recognized in Austria as:</strong><br>
                    Masterstudium aus Mikroelektronik und Photonik<br>
                    <i>(Schwerpunkt: Sicherheits- und Zuverlässigkeitstechnik)</i></p>
                </div>

                <p><strong>B.S. Computer Science</strong><br>
                <span style="font-size: 0.85rem; color: #666;">Universiti Malaysia Sabah (2014-2018) </span></p>
                
                <div class="cv-notice-box">
                    <p><strong>🇦🇹 Recognized in Austria as:</strong><br>
                    Fachhochschul-Bachelorstudiengang aus Software Engineering</p>
                </div>
            </div>

            <div class="cv-section">
                <h3>Certifications</h3>
                <p style="font-size: 0.9rem; margin-bottom: 10px;"><strong>AI Ethics & Risk Mitigation</strong><br>2025 </p>
                <p style="font-size: 0.9rem; margin-bottom: 10px;"><strong>Nordic Probabilistic AI School</strong><br>2024 </p>
                <p style="font-size: 0.9rem;"><strong>Google Cloud Big Data & ML</strong><br>2020 </p>
            </div>

            <div class="cv-section">
                <h3>Languages</h3>
                <p><strong>English:</strong> Fluent (C1/C2) </p>
                <p><strong>Mandarin:</strong> Fluent (C1/C2) </p>
                <p><strong>Malay:</strong> Native </p>
                <p><strong>German:</strong> A2/B1 (Active Learner) </p>
            </div>
        </div>

        <div class="cv-main">
            <h2 class="section-title">Professional Summary</h2>
            <p style="margin-bottom: 30px;">
                Technical professional with strong expertise in Data Science, Machine Learning, and Software Development. I combine a primary focus on technical execution with the ability to manage stakeholder requirements and project documentation. Seeking a hands-on technical role (e.g., Data Analyst, Solution Engineer) or Product Owner role in an international environment.
            </p>

            <h2 class="section-title">Work Experience</h2>

            <div class="cv-job">
                <div class="cv-job-header">
                    <div>
                        <h3>Technical Project Coordinator</h3>
                        <span class="cv-company">Montanuniversität Leoben, Austria</span>
                    </div>
                    <span class="cv-date">Nov 2023 - Mar 2025 </span>
                </div>

                <a href="https://iyeszin.github.io/bridging_gap.html" class="cv-project-btn" target="_blank">
                    <span class="cv-project-icon">📊</span> View Project Dashboard
                </a>

                <ul>
                    <li>Served as the primary technical point of contact, coordinating the development of an ML classification system and bridging the gap between geological specialists and technology teams.</li>
                    <li>Implemented an AI solution addressing <strong>59% of Austria's total waste volume</strong>, successfully bringing together 3 research units and industrial partners.</li>
                    <li>Researched AI classification challenges for geological materials and identified key differences in multi-context classification requirements.</li>
                    <li>Created knowledge exchange frameworks to overcome communication barriers between technical and non-technical stakeholders.</li>
                </ul>
            </div>

            <div class="cv-job">
                <div class="cv-job-header">
                    <div>
                        <h3>Research Intern</h3>
                        <span class="cv-company">Chair of Cyber-Physical-Systems, Austria</span>
                    </div>
                    <span class="cv-date">Feb 2023 - Sept 2023 </span>
                </div>

                <a href="https://iyeszin.github.io/projects/sign-language-robot/" class="cv-project-btn" target="_blank">
                    <span class="cv-project-icon">🤖</span> View Project: Sign Language Robot
                </a>

                <ul>
                    <li>Developed and implemented a deep learning-based sign language recognition system achieving an <strong>87% accuracy rate</strong>.</li>
                    <li><strong>Hardware Integration:</strong> Developed a robotic hand interface to translate text into physical gestures, ensuring system accuracy through rigorous testing.</li>
                    <li>Created comprehensive technical reports and user manuals, adapting writing styles for audiences ranging from technical specialists to end-users.</li>
                </ul>
            </div>

            <div class="cv-job">
                <div class="cv-job-header">
                    <div>
                        <h3>Research Intern</h3>
                        <span class="cv-company">Color Imaging Lab, University of Granada, Spain</span>
                    </div>
                    <span class="cv-date">June 2022 - Sept 2022 </span>
                </div>

                <a href="https://iyeszin.github.io/projects/color-vision/" class="cv-project-btn" target="_blank">
                    <span class="cv-project-icon">📱</span> View Project: Color Vision Aid
                </a>

                <ul>
                    <li>Developed a cross-platform mobile application using <strong>React Native, Flask, and JavaScript</strong>.</li>
                    <li>Designed features to help color-blind individuals perceive colors more accurately and <strong>simulate color blindness</strong> for users with normal vision.</li>
                    <li>Conducted a 3-month design sprint for accessibility technology, moving from user research to implementation and testing.</li>
                </ul>
            </div>

            <div class="cv-job">
                <div class="cv-job-header">
                    <div>
                        <h3>Business Intelligence Consultant</h3>
                        <span class="cv-company">SturnGroup, Malaysia</span>
                    </div>
                    <span class="cv-date">Feb 2020 - Aug 2021</span>
                </div>
                <ul>
                    <li>Managed end-to-end implementation of a Change Data Capture system, using MS Project and Gantt charts to ensure on-time delivery.</li>
                    <li>Established test metrics that <strong>reduced projected disaster recovery time from 8 hours to 30 minutes</strong>.</li>
                    <li>Developed VBA automation tools to streamline data processing workflows and coordinate BI report development.</li>
                </ul>
            </div>
            
            <div class="cv-job">
                <div class="cv-job-header">
                    <div>
                        <h3>Software Developer</h3>
                        <span class="cv-company">Merimen Online, Malaysia</span>
                    </div>
                    <span class="cv-date">Dec 2018 - Jan 2020 </span>
                </div>
                <ul>
                    <li>Full-stack developer (JavaScript, jQuery, HTML, ColdFusion) for an SE Asian motor insurance processing system.</li>
                    <li>Consistently completed <strong>95% of assigned sprint tickets</strong> within deadlines.</li>
                    <li>Resolved software bugs to improve application stability and reduce claim handling errors.</li>
                </ul>
            </div>

             <div class="cv-job">
                <div class="cv-job-header">
                    <div>
                        <h3>Software Intern</h3>
                        <span class="cv-company">Meta Technology (Asia Office), Malaysia</span>
                    </div>
                    <span class="cv-date">Feb 2017 - Aug 2017</span>
                </div>
                <ul>
                    <li>Produced clean, efficient code based on specifications and performed system troubleshooting.</li>
                    <li>Worked on Odoo ERP/CRM tasks, including form implementation, Kanban revisions, and Qweb report creation.</li>
                </ul>
            </div>

        </div>
    </div>
</div>