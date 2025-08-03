<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hadia Yasir - Developer Profile</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #FFF0F5 0%, #FFE4E1 50%, #FFEFD5 100%);
            min-height: 100vh;
            color: #8B4B8C;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .header {
            text-align: center;
            padding: 40px 0;
            background: linear-gradient(45deg, #FF69B4, #FFB6C1, #FFC0CB);
            border-radius: 20px;
            margin-bottom: 30px;
            box-shadow: 0 10px 30px rgba(255, 105, 180, 0.3);
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
            background: repeating-linear-gradient(
                45deg,
                transparent,
                transparent 10px,
                rgba(255, 255, 255, 0.1) 10px,
                rgba(255, 255, 255, 0.1) 20px
            );
            animation: sparkle 20s linear infinite;
        }
        
        @keyframes sparkle {
            0% { transform: translateX(-50%) translateY(-50%) rotate(0deg); }
            100% { transform: translateX(-50%) translateY(-50%) rotate(360deg); }
        }
        
        .header h1 {
            font-size: 3em;
            color: white;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
            margin-bottom: 10px;
            position: relative;
            z-index: 2;
        }
        
        .header h3 {
            font-size: 1.3em;
            color: #FFF0F5;
            font-weight: 400;
            position: relative;
            z-index: 2;
        }
        
        .typing-animation {
            background: rgba(255, 255, 255, 0.2);
            padding: 15px;
            border-radius: 15px;
            margin: 20px 0;
            position: relative;
            z-index: 2;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
            position: relative;
            z-index: 2;
        }
        
        .social-links a {
            background: rgba(255, 255, 255, 0.9);
            color: #FF69B4;
            padding: 12px 24px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(255, 105, 180, 0.3);
        }
        
        .social-links a:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(255, 105, 180, 0.4);
            background: white;
        }
        
        .section {
            background: rgba(255, 255, 255, 0.8);
            margin: 30px 0;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(255, 182, 193, 0.2);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 182, 193, 0.3);
        }
        
        .section h2 {
            color: #FF69B4;
            font-size: 2.2em;
            margin-bottom: 20px;
            text-align: center;
            text-shadow: 1px 1px 2px rgba(255, 105, 180, 0.3);
        }
        
        .cute-border {
            border: 3px dashed #FFB6C1;
            padding: 20px;
            border-radius: 15px;
            background: rgba(255, 240, 245, 0.5);
            margin: 20px 0;
        }
        
        .highlights-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }
        
        .highlight-item {
            background: linear-gradient(135deg, #FFE4E1, #FFF0F5);
            padding: 15px;
            border-radius: 12px;
            border-left: 4px solid #FF69B4;
            transition: transform 0.3s ease;
        }
        
        .highlight-item:hover {
            transform: translateX(5px);
            box-shadow: 0 5px 15px rgba(255, 105, 180, 0.2);
        }
        
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 10px;
            margin: 20px 0;
        }
        
        .tech-badge {
            background: #FF69B4;
            color: white;
            padding: 8px 12px;
            border-radius: 20px;
            text-align: center;
            font-size: 0.9em;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        .tech-badge:hover {
            background: #C71585;
            transform: translateY(-2px);
        }
        
        .github-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.9);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(255, 182, 193, 0.2);
            border: 2px solid #FFB6C1;
        }
        
        .footer {
            text-align: center;
            padding: 40px;
            background: linear-gradient(45deg, #FF69B4, #FFB6C1);
            border-radius: 20px;
            margin-top: 40px;
            color: white;
        }
        
        .cute-divider {
            text-align: center;
            font-size: 2em;
            margin: 30px 0;
            color: #FF69B4;
        }
        
        .floating-hearts {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }
        
        .heart {
            position: absolute;
            color: #FFB6C1;
            font-size: 20px;
            animation: float 6s ease-in-out infinite;
            opacity: 0.3;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(100vh) rotate(0deg); opacity: 0; }
            10% { opacity: 0.3; }
            90% { opacity: 0.3; }
            50% { transform: translateY(-100px) rotate(180deg); opacity: 0.6; }
        }
        
        .welcome-box {
            background: linear-gradient(135deg, #FFE4E1, #FFF0F5);
            border: 3px solid #FFB6C1;
            border-radius: 15px;
            padding: 20px;
            margin: 20px 0;
            text-align: center;
            font-family: 'Courier New', monospace;
            color: #C71585;
            font-weight: bold;
        }
        
        .goal-box {
            background: linear-gradient(45deg, #FFE4E1, #FFF0F5);
            border: 2px solid #FFB6C1;
            border-radius: 15px;
            padding: 20px;
            margin: 20px 0;
            text-align: center;
            font-style: italic;
            color: #C71585;
        }
        
        @media (max-width: 768px) {
            .header h1 { font-size: 2em; }
            .header h3 { font-size: 1em; }
            .social-links { flex-direction: column; align-items: center; }
            .highlights-grid { grid-template-columns: 1fr; }
            .tech-grid { grid-template-columns: repeat(auto-fit, minmax(100px, 1fr)); }
            .github-stats { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <div class="floating-hearts">
        <div class="heart" style="left: 10%; animation-delay: 0s;">♡</div>
        <div class="heart" style="left: 20%; animation-delay: 1s;">♡</div>
        <div class="heart" style="left: 30%; animation-delay: 2s;">♡</div>
        <div class="heart" style="left: 40%; animation-delay: 3s;">♡</div>
        <div class="heart" style="left: 50%; animation-delay: 4s;">♡</div>
        <div class="heart" style="left: 60%; animation-delay: 5s;">♡</div>
        <div class="heart" style="left: 70%; animation-delay: 1.5s;">♡</div>
        <div class="heart" style="left: 80%; animation-delay: 2.5s;">♡</div>
        <div class="heart" style="left: 90%; animation-delay: 3.5s;">♡</div>
    </div>

    <div class="container">
        <header class="header">
            <h1>Hadia Yasir</h1>
            <h3>Computer Science Student | Creative Coder | Web Developer | Tech Explorer</h3>
            
            <div class="typing-animation">
                <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=18&duration=2400&pause=900&color=FFFFFF&center=true&vCenter=true&width=560&lines=Creative+Coding;Web+Development;Arduino+Projects;UI/UX+Design;Building+Amazing+Things!" alt="Typing SVG" />
            </div>
            
            <div class="social-links">
                <a href="https://instagram.com/hadia.malik.k">Instagram</a>
                <a href="https://tiktok.com/@haviar.a">TikTok</a>
                <a href="mailto:hadiya.ymalik@gmail.com">Email</a>
            </div>
        </header>

        <div class="welcome-box">
            ╭─────────────────────────────────────────────╮<br>
            │    Welcome to my creative coding world!     │<br>
            ╰─────────────────────────────────────────────╯
        </div>

        <section class="section">
            <h2>About Me</h2>
            <div class="cute-border">
                <p>Hi, I'm <strong>Hadia</strong> — a Computer Science student passionate about building smart, simple, and impactful tech.</p>
                <p>I love turning ideas into real projects — whether it's coding with C++, creating Arduino-based systems, or designing clean user interfaces.</p>
                <p>I'm especially curious about how tech can solve real-world problems in creative ways.</p>
                <p>I actively contribute to student-led tech communities and love mentoring others while learning from real-world projects.</p>
            </div>
            
            <div class="goal-box">
                My goal is to keep learning, keep building, and contribute to meaningful projects that make tech more human.
            </div>
        </section>

        <div class="cute-divider">~  ♡  ~  ♡  ~</div>

        <section class="section">
            <h2>Highlights</h2>
            <div class="highlights-grid">
                <div class="highlight-item">
                    <strong>Core Team Member:</strong> IEEE Namal Student Branch
                </div>
                <div class="highlight-item">
                    <strong>Founding Member & Designer:</strong> Namal Open Source Society (OSS)
                </div>
                <div class="highlight-item">
                    <strong>Lead Developer:</strong> Multiple academic and portfolio-level Web Development Projects
                </div>
                <div class="highlight-item">
                    <strong>Tech Stack:</strong> React, TailwindCSS, and Firebase based tools with AI integration
                </div>
                <div class="highlight-item">
                    <strong>UI/UX Designer:</strong> Strong eye for user experience
                </div>
                <div class="highlight-item">
                    <strong>Community Leader:</strong> Presenter and Volunteer at university tech events and workshops
                </div>
            </div>
        </section>

        <div class="cute-divider">~  ♡  ~  ♡  ~</div>

        <section class="section">
            <h2>Tech Stack</h2>
            <div class="tech-grid">
                <div class="tech-badge">Arduino</div>
                <div class="tech-badge">C++</div>
                <div class="tech-badge">CSS3</div>
                <div class="tech-badge">Figma</div>
                <div class="tech-badge">Firebase</div>
                <div class="tech-badge">HTML5</div>
                <div class="tech-badge">Illustrator</div>
                <div class="tech-badge">Java</div>
                <div class="tech-badge">JavaScript</div>
                <div class="tech-badge">Node.js</div>
                <div class="tech-badge">OpenCV</div>
                <div class="tech-badge">Pandas</div>
                <div class="tech-badge">Photoshop</div>
                <div class="tech-badge">Python</div>
                <div class="tech-badge">Qt</div>
                <div class="tech-badge">React</div>
                <div class="tech-badge">React Native</div>
                <div class="tech-badge">Scikit-learn</div>
                <div class="tech-badge">TailwindCSS</div>
                <div class="tech-badge">TensorFlow</div>
                <div class="tech-badge">TypeScript</div>
            </div>
        </section>

        <div class="cute-divider">~  ♡  ~  ♡  ~</div>

        <section class="section">
            <h2>GitHub Stats</h2>
            <div class="github-stats">
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api?username=Hadia-codes&theme=buefy&hide_border=false&include_all_commits=false&count_private=false&bg_color=FFF0F5&title_color=FF69B4&text_color=C71585&icon_color=FFB6C1" alt="GitHub Stats" style="max-width: 100%; border-radius: 10px;">
                </div>
                <div class="stat-card">
                    <img src="https://nirzak-streak-stats.vercel.app/?user=Hadia-codes&theme=buefy&hide_border=false&background=FFF0F5&ring=FF69B4&fire=FF69B4&currStreakLabel=C71585" alt="GitHub Streak" style="max-width: 100%; border-radius: 10px;">
                </div>
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Hadia-codes&theme=buefy&hide_border=false&include_all_commits=false&count_private=false&layout=compact&bg_color=FFF0F5&title_color=FF69B4&text_color=C71585" alt="Top Languages" style="max-width: 100%; border-radius: 10px;">
                </div>
                <div class="stat-card">
                    <img src="https://github-profile-trophy.vercel.app/?username=Hadia-codes&theme=buefy&no-frame=false&no-bg=true&margin-w=4" alt="GitHub Trophies" style="max-width: 100%; border-radius: 10px;">
                </div>
            </div>
            
            <div class="stat-card" style="margin-top: 20px;">
                <h3 style="color: #FF69B4; margin-bottom: 15px;">Top Contributed Repositories</h3>
                <img src="https://github-contributor-stats.vercel.app/api?username=Hadia-codes&limit=5&theme=buefy&combine_all_yearly_contributions=true" alt="Top Contributed Repo" style="max-width: 100%; border-radius: 10px;">
            </div>
        </section>

        <footer class="footer">
            <div class="welcome-box" style="background: rgba(255, 255, 255, 0.2); border-color: white; color: white;">
                Thank you for visiting my profile! Let's create something amazing together!
            </div>
            
            <div style="margin: 20px 0;">
                <img src="https://visitcount.itsvg.in/api?id=Hadia-codes&icon=0&color=FF69B4" alt="Profile Views" style="margin: 5px;">
            </div>
            
            <h3>Let's Connect and Build the Future Together!</h3>
        </footer>
    </div>

    <script>
        // Add some interactive sparkle effects
        document.addEventListener('mousemove', function(e) {
            if (Math.random() > 0.9) {
                createSparkle(e.clientX, e.clientY);
            }
        });

        function createSparkle(x, y) {
            const sparkle = document.createElement('div');
            sparkle.style.position = 'fixed';
            sparkle.style.left = x + 'px';
            sparkle.style.top = y + 'px';
            sparkle.style.color = '#FF69B4';
            sparkle.style.fontSize = '12px';
            sparkle.style.pointerEvents = 'none';
            sparkle.style.zIndex = '1000';
            sparkle.innerHTML = '♡';
            
            document.body.appendChild(sparkle);
            
            setTimeout(() => {
                sparkle.style.transform = 'translateY(-50px)';
                sparkle.style.opacity = '0';
                sparkle.style.transition = 'all 1s ease-out';
            }, 10);
            
            setTimeout(() => {
                document.body.removeChild(sparkle);
            }, 1100);
        }

        // Add scroll animations
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => {
                const rect = section.getBoundingClientRect();
                if (rect.top < window.innerHeight && rect.bottom > 0) {
                    section.style.transform = 'translateY(0)';
                    section.style.opacity = '1';
                }
            });
        });

        // Initialize sections with animation
        document.querySelectorAll('.section').forEach(section => {
            section.style.transform = 'translateY(50px)';
            section.style.opacity = '0';
            section.style.transition = 'all 0.6s ease-out';
        });
    </script>
</body>
</html>
