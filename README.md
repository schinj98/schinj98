<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sachin Jangid - Software Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0f0f1e 0%, #1a1a2e 50%, #16213e 100%);
            color: #e4e4e7;
            line-height: 1.6;
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .header {
            text-align: center;
            padding: 60px 20px;
            background: linear-gradient(135deg, rgba(99, 102, 241, 0.1) 0%, rgba(139, 92, 246, 0.1) 100%);
            border-radius: 20px;
            border: 1px solid rgba(99, 102, 241, 0.2);
            margin-bottom: 40px;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(99, 102, 241, 0.1) 0%, transparent 70%);
            animation: pulse 4s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 0.5; }
            50% { transform: scale(1.1); opacity: 0.8; }
        }

        .header-content {
            position: relative;
            z-index: 1;
        }

        h1 {
            font-size: 3.5rem;
            font-weight: 700;
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 50%, #d946ef 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 15px;
        }

        .tagline {
            font-size: 1.2rem;
            color: #a1a1aa;
            margin-bottom: 20px;
        }

        .bio {
            font-size: 1rem;
            color: #d4d4d8;
            max-width: 800px;
            margin: 20px auto;
            line-height: 1.8;
        }

        .links {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 25px;
        }

        .link-btn {
            padding: 10px 25px;
            background: rgba(99, 102, 241, 0.1);
            border: 1px solid #6366f1;
            border-radius: 8px;
            color: #6366f1;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .link-btn:hover {
            background: rgba(99, 102, 241, 0.2);
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(99, 102, 241, 0.3);
        }

        .section {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(99, 102, 241, 0.2);
            border-radius: 15px;
            padding: 35px;
            margin-bottom: 30px;
            transition: all 0.3s ease;
        }

        .section:hover {
            border-color: rgba(99, 102, 241, 0.4);
            box-shadow: 0 8px 30px rgba(99, 102, 241, 0.15);
        }

        h2 {
            font-size: 2rem;
            margin-bottom: 25px;
            color: #6366f1;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        h2::before {
            content: '';
            width: 4px;
            height: 30px;
            background: linear-gradient(180deg, #6366f1 0%, #8b5cf6 100%);
            border-radius: 2px;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .tech-item {
            background: rgba(99, 102, 241, 0.05);
            padding: 15px 20px;
            border-radius: 10px;
            border: 1px solid rgba(99, 102, 241, 0.15);
            transition: all 0.3s ease;
        }

        .tech-item:hover {
            background: rgba(99, 102, 241, 0.1);
            border-color: #6366f1;
            transform: translateX(5px);
        }

        .tech-label {
            font-weight: 600;
            color: #8b5cf6;
            margin-bottom: 8px;
            font-size: 0.9rem;
        }

        .tech-values {
            color: #d4d4d8;
            font-size: 0.95rem;
        }

        .experience-card, .project-card {
            background: rgba(139, 92, 246, 0.05);
            padding: 25px;
            border-radius: 12px;
            border-left: 4px solid #8b5cf6;
            margin-bottom: 20px;
            transition: all 0.3s ease;
        }

        .experience-card:hover, .project-card:hover {
            background: rgba(139, 92, 246, 0.1);
            transform: translateX(10px);
        }

        .card-header {
            display: flex;
            justify-content: space-between;
            align-items: start;
            margin-bottom: 15px;
            flex-wrap: wrap;
            gap: 10px;
        }

        .card-title {
            font-size: 1.4rem;
            color: #e4e4e7;
            font-weight: 600;
        }

        .card-meta {
            color: #a1a1aa;
            font-size: 0.9rem;
        }

        .card-tech {
            display: inline-block;
            background: rgba(99, 102, 241, 0.15);
            padding: 5px 12px;
            border-radius: 6px;
            font-size: 0.85rem;
            color: #a5b4fc;
            margin-bottom: 15px;
            border: 1px solid rgba(99, 102, 241, 0.3);
        }

        .card-points {
            list-style: none;
            padding-left: 0;
        }

        .card-points li {
            padding-left: 25px;
            margin-bottom: 10px;
            position: relative;
            color: #d4d4d8;
        }

        .card-points li::before {
            content: '▹';
            position: absolute;
            left: 0;
            color: #6366f1;
            font-weight: bold;
            font-size: 1.2rem;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .stat-card {
            background: linear-gradient(135deg, rgba(99, 102, 241, 0.1) 0%, rgba(139, 92, 246, 0.1) 100%);
            padding: 25px;
            border-radius: 12px;
            border: 1px solid rgba(99, 102, 241, 0.2);
            text-align: center;
            transition: all 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(99, 102, 241, 0.2);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .stat-label {
            color: #a1a1aa;
            font-size: 0.95rem;
            margin-top: 5px;
        }

        .achievement-list {
            list-style: none;
            padding: 0;
        }

        .achievement-list li {
            background: rgba(34, 197, 94, 0.1);
            padding: 15px 20px;
            margin-bottom: 12px;
            border-radius: 10px;
            border-left: 3px solid #22c55e;
            color: #d4d4d8;
            transition: all 0.3s ease;
        }

        .achievement-list li:hover {
            background: rgba(34, 197, 94, 0.15);
            transform: translateX(10px);
        }

        .footer {
            text-align: center;
            padding: 40px 20px;
            color: #71717a;
            font-size: 0.95rem;
            margin-top: 40px;
        }

        .footer-highlight {
            color: #6366f1;
            font-weight: 600;
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }

            .section {
                padding: 25px;
            }

            .tech-grid {
                grid-template-columns: 1fr;
            }

            .card-header {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header class="header">
            <div class="header-content">
                <h1>Sachin Jangid</h1>
                <p class="tagline">Software Developer • Competitive Programmer • Full-Stack Engineer</p>
                <p class="bio">Building scalable systems and solving complex problems through code. Fourth-year B.Tech student with 7.6 CGPA, specializing in high-performance applications and distributed systems.</p>
                <div class="links">
                    <a href="mailto:Sachinreal2003@gmail.com" class="link-btn">Email</a>
                    <a href="#" class="link-btn">LinkedIn</a>
                    <a href="#" class="link-btn">GitHub</a>
                    <a href="#" class="link-btn">LeetCode</a>
                    <a href="#" class="link-btn">CodeChef</a>
                </div>
            </div>
        </header>

        <section class="section">
            <h2>Technical Arsenal</h2>
            <div class="tech-grid">
                <div class="tech-item">
                    <div class="tech-label">Languages</div>
                    <div class="tech-values">Java • Python • JavaScript • SQL • Node.js</div>
                </div>
                <div class="tech-item">
                    <div class="tech-label">Backend</div>
                    <div class="tech-values">Spring Boot • REST APIs • Flask • MySQL</div>
                </div>
                <div class="tech-item">
                    <div class="tech-label">Frontend</div>
                    <div class="tech-values">Next.js • React • Tailwind CSS</div>
                </div>
                <div class="tech-item">
                    <div class="tech-label">DevOps & Tools</div>
                    <div class="tech-values">Docker • AWS EC2 • Git • Maven • JUnit • CI/CD</div>
                </div>
            </div>
        </section>

        <section class="section">
            <h2>Competitive Programming</h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="stat-number">1814</div>
                    <div class="stat-label">LeetCode Rating (Knight)</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">261</div>
                    <div class="stat-label">Rank in Weekly Contest 451</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">750+</div>
                    <div class="stat-label">Problems Solved</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">81.6%</div>
                    <div class="stat-label">TCS ION NQT Score</div>
                </div>
            </div>
        </section>

        <section class="section">
            <h2>Professional Experience</h2>
            <div class="experience-card">
                <div class="card-header">
                    <div>
                        <div class="card-title">Software Developer Intern @ Berrily</div>
                        <div class="card-meta">Mumbai, Maharashtra</div>
                    </div>
                    <div class="card-meta">June 2025 - August 2025</div>
                </div>
                <ul class="card-points">
                    <li>Developed production-grade authentication modules with secure API implementations</li>
                    <li>Optimized MySQL database queries improving performance significantly</li>
                    <li>Built responsive frontends using React and Next.js with Python backend integration</li>
                    <li>Collaborated on real-world problem-solving in an agile development environment</li>
                </ul>
            </div>
        </section>

        <section class="section">
            <h2>Featured Projects</h2>
            
            <div class="project-card">
                <div class="card-header">
                    <div class="card-title">Automated WireGuard VPN Platform</div>
                    <div class="card-meta">Jan 2025 - Mar 2025</div>
                </div>
                <div class="card-tech">Java • Spring Boot • MySQL • JWT • AWS EC2 • JUnit</div>
                <ul class="card-points">
                    <li>Built scalable distributed system on AWS EC2 for automated VPN configuration generation</li>
                    <li>Architected microservice infrastructure handling 100+ concurrent users</li>
                    <li>Achieved sub-200ms response times through optimized AWS EC2 deployment</li>
                    <li>Implemented JWT-based authentication with fault-tolerant design patterns</li>
                    <li>Comprehensive unit testing suite using JUnit ensuring API reliability</li>
                </ul>
            </div>

            <div class="project-card">
                <div class="card-header">
                    <div class="card-title">ArcadeTrack - GCP Analysis Dashboard</div>
                    <div class="card-meta">Feb 2025 - Present</div>
                </div>
                <div class="card-tech">Next.js • Flask • Tailwind CSS • Gunicorn • Vercel</div>
                <ul class="card-points">
                    <li>Built high-performance frontend achieving 100% Lighthouse score on Vercel</li>
                    <li>Engineered Flask API processing 10,000+ profiles with <300ms latency</li>
                    <li>Implemented intelligent localStorage caching reducing API calls by 80%</li>
                    <li>Maintained 99.9% uptime through robust error handling and validation</li>
                </ul>
            </div>
        </section>

        <section class="section">
            <h2>Key Achievements</h2>
            <ul class="achievement-list">
                <li>🏆 LeetCode Knight Badge with Contest Rating of 1814 (June 2025)</li>
                <li>🥈 Secured Rank 261 in LeetCode Weekly Contest 451 among 27,000+ participants</li>
                <li>💻 Solved 750+ problems across multiple coding platforms</li>
                <li>📊 Scored 81.6% in TCS ION NQT examination</li>
            </ul>
        </section>

        <footer class="footer">
            <p>Open to <span class="footer-highlight">Full-Stack Development Roles</span> • <span class="footer-highlight">Software Engineering Internships</span> • <span class="footer-highlight">Collaborative Projects</span></p>
            <p style="margin-top: 15px;">Let's build something amazing together.</p>
        </footer>
    </div>
</body>
</html>
