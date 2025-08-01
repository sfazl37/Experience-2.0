<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Experience Evolution</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap');
        
        body {
            font-family: 'Roboto', sans-serif;
            line-height: 1.6;
            color: #3c4043;
            background-color: #f8f9fa;
            margin: 0;
            padding: 0;
        }
        
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Navigation Bar */
        .navbar {
            background-color: #202124;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .nav-menu {
            display: flex;
            justify-content: center;
            list-style-type: none;
            padding: 0;
            margin: 0;
            flex-wrap: wrap;
        }
        
        .nav-item {
            margin: 0 15px;
        }
        
        .nav-link {
            color: white;
            text-decoration: none;
            font-size: 16px;
            transition: color 0.3s;
        }
        
        .nav-link:hover {
            color: #8ab4f8;
        }
        
        /* Home Page */
        .home-page {
            text-align: center;
            padding: 50px 0;
        }
        
        .home-title {
            font-size: 48px;
            font-weight: 300;
            color: #202124;
            margin-bottom: 30px;
        }
        
        .team-container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 30px;
            margin: 50px 0;
        }
        
        .team-member {
            background: white;
            border-radius: 8px;
            padding: 25px;
            width: 250px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .team-member:hover {
            transform: translateY(-5px);
        }
        
        .member-name {
            font-size: 20px;
            font-weight: 500;
            margin: 15px 0 5px;
            color: #202124;
        }
        
        .member-role {
            font-size: 16px;
            color: #5f6368;
            font-style: italic;
        }
        
        .begin-button {
            background-color: #4285f4;
            color: white;
            border: none;
            padding: 15px 30px;
            border-radius: 4px;
            font-size: 18px;
            cursor: pointer;
            transition: background-color 0.3s;
            margin-top: 30px;
        }
        
        .begin-button:hover {
            background-color: #3367d6;
        }
        
        /* Slides */
        .slide {
            background-color: white;
            border-radius: 8px;
            padding: 60px 80px;
            margin-bottom: 30px;
            box-shadow: 0 1px 2px rgba(0,0,0,0.1);
            position: relative;
            min-height: 500px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        
        h1, h2 {
            font-weight: 400;
            text-align: center;
            margin: 0;
            color: #202124;
        }
        
        h1 {
            font-size: 36px;
            margin-bottom: 20px;
            font-weight: 300;
        }
        
        h2 {
            font-size: 28px;
            margin-bottom: 30px;
            position: relative;
        }
        
        h2:after {
            content: "";
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 3px;
            background-color: #4285f4;
        }
        
        ul {
            padding-left: 0;
            list-style-type: none;
            max-width: 700px;
            margin: 0 auto;
        }
        
        li {
            margin-bottom: 15px;
            position: relative;
            padding-left: 30px;
            font-size: 18px;
            line-height: 1.5;
        }
        
        li:before {
            content: "•";
            color: #4285f4;
            font-size: 24px;
            position: absolute;
            left: 0;
            top: -3px;
        }
        
        .footer {
            position: absolute;
            bottom: 20px;
            right: 30px;
            font-size: 12px;
            color: #5f6368;
        }
        
        .visual {
            text-align: center;
            margin: 30px 0;
            color: #5f6368;
            font-style: italic;
        }
        
        .persona {
            background-color: #f1f3f4;
            padding: 20px;
            border-radius: 8px;
            margin: 20px auto;
            max-width: 600px;
            position: relative;
        }
        
        .persona:before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 4px;
            height: 100%;
            background-color: #34a853;
            border-radius: 4px 0 0 4px;
        }
        
        .nav {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
        }
        
        button {
            background-color: #4285f4;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 14px;
            transition: background-color 0.2s;
        }
        
        button:hover {
            background-color: #3367d6;
        }
        
        .hidden {
            display: none;
        }
        
        .slide-number {
            position: absolute;
            top: 20px;
            right: 20px;
            color: #5f6368;
            font-size: 12px;
        }
        
        .title-slide h1 {
            font-size: 42px;
            font-weight: 300;
            margin-bottom: 10px;
        }
        
        .title-slide h2 {
            font-size: 24px;
            font-weight: 300;
            color: #5f6368;
            margin-bottom: 40px;
        }
        
        .title-slide h2:after {
            display: none;
        }
        
        /* Contact Page */
        .contact-page {
            text-align: center;
            padding: 40px;
        }
        
        .contact-title {
            font-size: 32px;
            color: #202124;
            margin-bottom: 30px;
        }
        
        .contact-subtitle {
            font-size: 18px;
            color: #5f6368;
            margin-bottom: 40px;
        }
        
        .contact-list {
            list-style-type: none;
            padding: 0;
            margin: 30px auto;
            max-width: 500px;
        }
        
        .contact-item {
            background: white;
            padding: 20px;
            margin: 15px 0;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            text-align: left;
            position: relative;
            padding-left: 80px;
        }
        
        .contact-icon {
            position: absolute;
            left: 20px;
            top: 50%;
            transform: translateY(-50%);
            font-size: 30px;
            width: 50px;
            height: 50px;
            background: #f1f3f4;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .contact-name {
            font-weight: 500;
            font-size: 18px;
            color: #202124;
            margin-bottom: 5px;
        }
        
        .contact-detail {
            color: #5f6368;
            margin: 5px 0;
        }
        
        /* Emoji Styles */
        .emoji {
            font-size: 1.2em;
            margin-right: 8px;
            vertical-align: middle;
        }
        
        .slide-emoji {
            font-size: 1.5em;
            margin-right: 10px;
            vertical-align: middle;
        }
    </style>
</head>
<body>
    <div class="navbar">
        <ul class="nav-menu">
            <li class="nav-item"><a href="#home" class="nav-link">🏠 Home</a></li>
            <li class="nav-item"><a href="#slide2" class="nav-link">🗨️ Reverse Feedback</a></li>
            <li class="nav-item"><a href="#slide3" class="nav-link">👥 Experience Personas</a></li>
            <li class="nav-item"><a href="#slide4" class="nav-link">🧠 EQ Training</a></li>
            <li class="nav-item"><a href="#slide5" class="nav-link">🎤 Voice of Employee</a></li>
            <li class="nav-item"><a href="#slide6" class="nav-link">🔍 Vertical Audits</a></li>
            <li class="nav-item"><a href="#slide7" class="nav-link">🏆 Micro-Wins Board</a></li>
            <li class="nav-item"><a href="#slide8" class="nav-link">📝 Summary</a></li>
            <li class="nav-item"><a href="#contact" class="nav-link">📞 Contact Us</a></li>
        </ul>
    </div>

    <div class="container">
        <!-- Home Page -->
        <div id="home" class="home-page">
            <h1 class="home-title">🌟 EXPERIENCE EVOLUTION 🌟</h1>
            <p style="font-size: 18px; max-width: 700px; margin: 0 auto 30px;">
                Transforming workplace experiences through innovative approaches and collaborative efforts. 🚀
            </p>
            
            <div class="team-container">
                <div class="team-member">
                    <div style="font-size: 50px;">🦸</div>
                    <div class="member-name">Akhil</div>
                    <div class="member-role">as Tony Stark 🧠</div>
                    <p style="margin-top: 10px; color: #5f6368;">The visionary innovator driving technological solutions 💡</p>
                </div>
                
                <div class="team-member">
                    <div style="font-size: 50px;">🐾</div>
                    <div class="member-name">Pousali</div>
                    <div class="member-role">as Black Panther ✊</div>
                    <p style="margin-top: 10px; color: #5f6368;">The strategic leader with deep cultural understanding 🌍</p>
                </div>
                
                <div class="team-member">
                    <div style="font-size: 50px;">🔥</div>
                    <div class="member-name">Fazal</div>
                    <div class="member-role">as Ghost Rider 💀</div>
                    <p style="margin-top: 10px; color: #5f6368;">The transformative force bringing energy to our initiatives ⚡</p>
                </div>
            </div>
            
            <p style="max-width: 800px; margin: 0 auto; font-size: 16px; line-height: 1.6;">
                Our team combines diverse superpowers to revolutionize workplace experiences. 
                Akhil's technological brilliance as Tony Stark, Pousali's strategic wisdom as Black Panther, 
                and Fazal's transformative energy as Ghost Rider create an unstoppable force for positive change. 💫
            </p>
            
            <button class="begin-button" onclick="showSlide(2)">🚀 To The New Beginning</button>
        </div>

        <!-- Slide 1 Content (on home page) -->
        <div id="slide1-content" style="max-width: 900px; margin: 50px auto; background: white; padding: 40px; border-radius: 8px; box-shadow: 0 2px 10px rgba(0,0,0,0.1);">
            <h2 style="text-align: center; color: #202124; margin-bottom: 30px;">✨ Evolving the Role of Experience Enablers ✨</h2>
            
            <div style="display: flex; flex-wrap: wrap; gap: 30px; justify-content: center;">
                <div style="flex: 1; min-width: 250px;">
                    <h3 style="color: #4285f4; border-bottom: 2px solid #4285f4; padding-bottom: 5px; display: inline-block;">📋 Our Approach</h3>
                    <p>We're redefining workplace experience through innovative, employee-centered strategies that foster engagement, trust, and continuous improvement. 🔄</p>
                </div>
                
                <div style="flex: 1; min-width: 250px;">
                    <h3 style="color: #4285f4; border-bottom: 2px solid #4285f4; padding-bottom: 5px; display: inline-block;">🎯 Key Focus Areas</h3>
                    <ul style="list-style-type: none; padding-left: 0;">
                        <li>• 🔄 Reverse Feedback Mechanisms</li>
                        <li>• 📊 Data-Driven Personas</li>
                        <li>• ❤️ Emotional Intelligence Training</li>
                        <li>• 🗣️ Employee Voice Integration</li>
                    </ul>
                </div>
            </div>
            
            <div style="margin-top: 40px; background: #f1f3f4; padding: 20px; border-radius: 8px;">
                <h3 style="text-align: center; color: #202124;">🤝 Collaborative Framework</h3>
                <p style="text-align: center;">Our methodology combines Pousali's strategic insights, Fazal's transformative processes, and Akhil's technological solutions to create comprehensive experience enhancements. 🌈</p>
            </div>
        </div>

        <!-- Slide 2 -->
        <div id="slide2" class="slide hidden">
            <div class="slide-number">2/8</div>
            <h2><span class="slide-emoji">🗨️</span> Reverse Feedback Connects</h2>
            <ul>
                <li><span class="emoji">💬</span> Employees submit questions via AMA sessions or anonymous tools</li>
                <li><span class="emoji">🔓</span> Builds openness and increases trust within teams</li>
                <li><span class="emoji">📝</span> Log common questions in a shared document for transparency</li>
            </ul>
            <div class="visual">💬 Visual: Speech bubble with question mark icon</div>
            <div class="footer">Author: Pousali ✍️</div>
        </div>

        <!-- Slide 3 -->
        <div id="slide3" class="slide hidden">
            <div class="slide-number">3/8</div>
            <h2><span class="slide-emoji">👥</span> Experience Personas</h2>
            <ul>
                <li><span class="emoji">📊</span> Create data-driven employee personas for targeted solutions</li>
                <li><span class="emoji">❤️</span> Empathy-driven design improves engagement and satisfaction</li>
            </ul>
            <div class="persona">
                <strong><span class="emoji">👤</span> Aman, the New Joiner:</strong> Needs clear onboarding materials and low-pressure support during first 90 days
            </div>
            <div class="visual">👥 Visual: Avatar illustrations representing different personas</div>
            <div class="footer">Author: Pousali ✍️</div>
        </div>

        <!-- Slide 4 -->
        <div id="slide4" class="slide hidden">
            <div class="slide-number">4/8</div>
            <h2><span class="slide-emoji">🧠</span> EQ Training for Enablers</h2>
            <ul>
                <li><span class="emoji">⏱️</span> Monthly 30-minute sessions on emotional intelligence</li>
                <li><span class="emoji">👀</span> Topics include reading body language and identifying burnout</li>
                <li><span class="emoji">👂</span> Improves listening skills and empathetic engagement</li>
            </ul>
            <div class="visual">🧠 Visual: Brain icon with gears</div>
            <div class="footer">Author: Fazal ✍️</div>
        </div>

        <!-- Slide 5 -->
        <div id="slide5" class="slide hidden">
            <div class="slide-number">5/8</div>
            <h2><span class="slide-emoji">🎤</span> Voice of Employee Snippets</h2>
            <ul>
                <li><span class="emoji">🎥</span> 30-60 second video testimonials from employees</li>
                <li><span class="emoji">👔</span> Shared in leadership meetings and company updates</li>
                <li><span class="emoji">💖</span> Adds human element to quantitative data</li>
            </ul>
            <div class="visual">🎥 Visual: Video camera icon</div>
            <div class="footer">Author: Fazal ✍️</div>
        </div>

        <!-- Slide 6 -->
        <div id="slide6" class="slide hidden">
            <div class="slide-number">6/8</div>
            <h2><span class="slide-emoji">🔍</span> Vertical-Based Experience Audits</h2>
            <ul>
                <li><span class="emoji">🏢</span> Facilities: Evaluate workspaces, lighting, and comfort</li>
                <li><span class="emoji">💻</span> Technology: Assess hardware/software usage and support</li>
                <li><span class="emoji">🧘</span> Wellbeing: Review break areas and noise levels</li>
                <li><span class="emoji">🆕</span> Onboarding: Audit new hire experience and resources</li>
            </ul>
            <div class="visual">🔍 Visual: Magnifying glass inspecting a checklist</div>
            <div class="footer">Author: Akhil ✍️</div>
        </div>

        <!-- Slide 7 -->
        <div id="slide7" class="slide hidden">
            <div class="slide-number">7/8</div>
            <h2><span class="slide-emoji">🏆</span> Micro-Wins Board</h2>
            <ul>
                <li><span class="emoji">✅</span> Log small daily improvements and solutions</li>
                <li><span class="emoji">📌</span> Display on physical or digital boards for visibility</li>
                <li><span class="emoji">🎉</span> Celebrate achievements in team huddles</li>
            </ul>
            <div class="visual">📋 Visual: Sticky notes on a bulletin board</div>
            <div class="footer">Author: Akhil ✍️</div>
        </div>

        <!-- Slide 8 -->
        <div id="slide8" class="slide hidden">
            <div class="slide-number">8/8</div>
            <h2><span class="slide-emoji">📝</span> Summary & Next Steps</h2>
            <ul style="text-align: center; list-style-type: none;">
                <li><span class="emoji">1️⃣</span> Implement Reverse Feedback Sessions</li>
                <li><span class="emoji">2️⃣</span> Develop Experience Personas</li>
                <li><span class="emoji">3️⃣</span> Launch EQ Training Program</li>
                <li><span class="emoji">4️⃣</span> Collect Employee Voice Snippets</li>
                <li><span class="emoji">5️⃣</span> Conduct Vertical Audits</li>
                <li><span class="emoji">6️⃣</span> Establish Micro-Wins Board</li>
            </ul>
            <div class="footer">Next Steps: Choose 2-3 initiatives to pilot next quarter 📅</div>
        </div>

        <!-- Contact Page -->
        <div id="contact" class="slide hidden">
            <div class="contact-page">
                <h1 class="contact-title">📞 Contact Us</h1>
                <p class="contact-subtitle">Reach out to our Experience Evolution team members 👋</p>
                
                <ul class="contact-list">
                    <li class="contact-item">
                        <div class="contact-icon">🔥</div>
                        <div class="contact-name">Fazal (Ghost Rider)</div>
                        <div class="contact-detail">📇 Employee ID: F754894</div>
                        <div class="contact-detail">📧 Email: sanaullah.fazal@jll.com</div>
                        <div class="contact-detail">📱 Phone: +91 96939 94430</div>
                    </li>
                    <li class="contact-item">
                        <div class="contact-icon">🐾</div>
                        <div class="contact-name">Pousali (Black Panther)</div>
                        <div class="contact-detail">📇 Employee ID: F747947</div>
                        <div class="contact-detail">📧 Email: pousali.das@jll.com</div>
                        <div class="contact-detail">📱 Phone: +91 98745 689212</div>
                    </li>
                    <li class="contact-item">
                        <div class="contact-icon">🦸</div>
                        <div class="contact-name">Akhil (Tony Stark)</div>
                        <div class="contact-detail">📇 Employee ID: N750530</div>
                        <div class="contact-detail">📧 Email: akhil.pandey@jll.com</div>
                        <div class="contact-detail">📱 Phone: +91 99484 10783</div>
                    </li>
                </ul>
                
                <p style="margin-top: 30px; font-size: 16px; color: #5f6368;">
                    We welcome your feedback and suggestions for improving workplace experiences. 💡<br>
                    Feel free to reach out to any of us directly! ✨
                </p>
            </div>
        </div>

        <div class="nav">
            <button id="prevBtn" onclick="prevSlide()">⬅️ Previous</button>
            <button id="nextBtn" onclick="nextSlide()">Next ➡️</button>
        </div>
    </div>

    <script>
        let currentSlide = 0; // 0 represents home page
        const totalSlides = 8;
        
        // Hide all slides initially
        document.querySelectorAll('.slide').forEach(slide => {
            slide.classList.add('hidden');
        });
        
        function showSlide(n) {
            // Hide home page
            document.getElementById('home').style.display = n === 0 ? 'block' : 'none';
            document.getElementById('slide1-content').style.display = n === 0 ? 'block' : 'none';
            
            // Hide all slides
            document.querySelectorAll('.slide').forEach(slide => {
                slide.classList.add('hidden');
            });
            
            // Show the selected slide if not home page
            if (n > 0 && n <= totalSlides) {
                document.getElementById(`slide${n}`).classList.remove('hidden');
            } else if (n === 'contact') {
                document.getElementById('contact').classList.remove('hidden');
            }
            
            // Update navigation buttons
            updateNavButtons(n);
            
            // Scroll to top
            window.scrollTo(0, 0);
        }
        
        function updateNavButtons(n) {
            const prevBtn = document.getElementById('prevBtn');
            const nextBtn = document.getElementById('nextBtn');
            
            if (n === 0) {
                // Home page
                prevBtn.style.visibility = 'hidden';
                nextBtn.style.visibility = 'visible';
                nextBtn.textContent = '🚀 Begin Presentation';
            } else if (n === 1) {
                // First slide
                prevBtn.style.visibility = 'visible';
                prevBtn.textContent = '🏠 Back to Home';
                nextBtn.style.visibility = 'visible';
                nextBtn.textContent = 'Next ➡️';
            } else if (n === totalSlides) {
                // Last slide
                prevBtn.style.visibility = 'visible';
                nextBtn.style.visibility = 'visible';
                nextBtn.textContent = '📞 Contact Us';
            } else if (n === 'contact') {
                // Contact page
                prevBtn.style.visibility = 'visible';
                nextBtn.style.visibility = 'hidden';
            } else {
                // Middle slides
                prevBtn.style.visibility = 'visible';
                nextBtn.style.visibility = 'visible';
                nextBtn.textContent = 'Next ➡️';
            }
        }
        
        function nextSlide() {
            if (currentSlide === 0) {
                // From home page to first slide
                currentSlide = 1;
            } else if (currentSlide === totalSlides) {
                // From last slide to contact page
                currentSlide = 'contact';
            } else if (currentSlide < totalSlides) {
                currentSlide++;
            }
            showSlide(currentSlide);
        }
        
        function prevSlide() {
            if (currentSlide === 1) {
                // Back to home from first slide
                currentSlide = 0;
            } else if (currentSlide === 'contact') {
                // Back from contact page to last slide
                currentSlide = totalSlides;
            } else if (currentSlide > 1) {
                currentSlide--;
            }
            showSlide(currentSlide);
        }
        
        // Handle navigation through menu links
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                const target = this.getAttribute('href').substring(1);
                
                if (target === 'home') {
                    currentSlide = 0;
                } else if (target === 'contact') {
                    currentSlide = 'contact';
                } else {
                    currentSlide = parseInt(target.replace('slide', ''));
                }
                
                showSlide(currentSlide);
            });
        });
        
        // Initialize
        showSlide(0); // Start with home page
        updateNavButtons(0);
    </script>
</body>
</html>
