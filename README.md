<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Ranush World - Amazing YouTube Content Creator">
    <meta name="keywords" content="Ranush World, YouTube, Videos, Content">
    <meta name="author" content="Ranush World">
    <title>Ranush World - YouTube Channel</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #FF6B6B;
            --secondary: #4ECDC4;
            --dark: #1a1a1a;
            --light: #f5f5f5;
            --text: #333;
            --white: #ffffff;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--white);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* ============ NAVBAR ============ */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: linear-gradient(135deg, var(--dark), #2a2a2a);
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--primary);
            text-decoration: none;
            letter-spacing: 1px;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
            align-items: center;
        }

        nav a {
            color: var(--white);
            text-decoration: none;
            transition: color 0.3s;
            font-weight: 500;
        }

        nav a:hover {
            color: var(--primary);
        }

        .menu-toggle {
            display: none;
            flex-direction: column;
            cursor: pointer;
            gap: 5px;
        }

        .menu-toggle span {
            width: 25px;
            height: 3px;
            background-color: var(--white);
            transition: 0.3s;
        }

        /* ============ HERO SECTION ============ */
        .hero {
            margin-top: 70px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: var(--white);
            padding: 6rem 2rem;
            text-align: center;
            min-height: 80vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -10%;
            width: 500px;
            height: 500px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            animation: slideInUp 0.8s ease;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.95;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2.5rem;
            font-size: 1rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            text-decoration: none;
            transition: all 0.3s;
            font-weight: bold;
            display: inline-block;
            text-align: center;
        }

        .btn-primary {
            background-color: var(--white);
            color: var(--primary);
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.2);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
        }

        .btn-secondary {
            background-color: transparent;
            color: var(--white);
            border: 2px solid var(--white);
        }

        .btn-secondary:hover {
            background-color: var(--white);
            color: var(--primary);
        }

        /* ============ ABOUT SECTION ============ */
        .about {
            padding: 4rem 2rem;
            background-color: var(--light);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--primary);
            position: relative;
            padding-bottom: 1rem;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            border-radius: 2px;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 1rem;
            color: var(--dark);
        }

        .about-text p {
            font-size: 1rem;
            margin-bottom: 1rem;
            color: #666;
            line-height: 1.8;
        }

        .about-image {
            width: 100%;
            height: 350px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 5rem;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
        }

        /* ============ FEATURES SECTION ============ */
        .features {
            padding: 4rem 2rem;
            background-color: var(--white);
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .feature-card {
            background: linear-gradient(135deg, var(--light), var(--white));
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
            transition: all 0.3s;
            border: 2px solid transparent;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
            border-color: var(--primary);
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .feature-card h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: var(--dark);
        }

        .feature-card p {
            color: #666;
            font-size: 0.95rem;
        }

        /* ============ VIDEOS SECTION ============ */
        .videos {
            padding: 4rem 2rem;
            background-color: var(--light);
        }

        .videos-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .video-card {
            background: var(--white);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            transition: all 0.3s;
        }

        .video-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
        }

        .video-thumbnail {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            position: relative;
        }

        .play-btn {
            width: 70px;
            height: 70px;
            background: var(--white);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            transition: all 0.3s;
        }

        .video-card:hover .play-btn {
            transform: scale(1.2);
        }

        .video-info {
            padding: 1.5rem;
        }

        .video-info h3 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            color: var(--dark);
        }

        .video-info p {
            color: #666;
            font-size: 0.95rem;
            margin-bottom: 1rem;
        }

        .video-date {
            color: var(--primary);
            font-size: 0.85rem;
            font-weight: bold;
        }

        /* ============ STATS SECTION ============ */
        .stats {
            padding: 4rem 2rem;
            background: linear-gradient(135deg, var(--dark), #2a2a2a);
            color: var(--white);
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            text-align: center;
        }

        .stat-item h3 {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }

        .stat-item p {
            font-size: 1.1rem;
            opacity: 0.9;
        }

        /* ============ CONTACT SECTION ============ */
        .contact {
            padding: 4rem 2rem;
            background-color: var(--light);
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: var(--dark);
        }

        .contact-item {
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .contact-item-icon {
            font-size: 1.5rem;
            color: var(--primary);
        }

        .contact-item p {
            color: #666;
        }

        .social-icons {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
        }

        .social-icon {
            width: 50px;
            height: 50px;
            background: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 1.5rem;
            text-decoration: none;
            transition: all 0.3s;
        }

        .social-icon:hover {
            background: var(--secondary);
            transform: translateY(-5px);
        }

        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .form-group label {
            margin-bottom: 0.5rem;
            font-weight: bold;
            color: var(--dark);
        }

        .form-group input,
        .form-group textarea {
            padding: 0.8rem;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-family: inherit;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        /* ============ FOOTER ============ */
        footer {
            background: var(--dark);
            color: var(--white);
            padding: 2rem;
            text-align: center;
            border-top: 3px solid var(--primary);
        }

        footer p {
            opacity: 0.8;
        }

        /* ============ ANIMATIONS ============ */
        @keyframes slideInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* ============ RESPONSIVE ============ */
        @media (max-width: 768px) {
            nav ul {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 70px;
                right: 2rem;
                background: var(--dark);
                padding: 1rem;
                border-radius: 10px;
                min-width: 200px;
                gap: 1rem;
            }

            nav ul.active {
                display: flex;
            }

            .menu-toggle {
                display: flex;
            }

            .hero-content h1 {
                font-size: 2rem;
            }

            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
            }

            .about-image {
                height: 250px;
            }

            .cta-buttons {
                flex-direction: column;
            }

            .btn {
                width: 100%;
            }
        }
    </style>
</head>
<body>

    <!-- ============ NAVBAR ============ -->
    <nav>
        <a href="#" class="logo">🎬 Ranush World</a>
        <ul id="navMenu">
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#features">Features</a></li>
            <li><a href="#videos">Videos</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
        <div class="menu-toggle" id="menuToggle">
            <span></span>
            <span></span>
            <span></span>
        </div>
    </nav>

    <!-- ============ HERO SECTION ============ -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Welcome to Ranush World 🌍</h1>
            <p>Creating amazing content that entertains, educates, and inspires millions around the globe!</p>
            <div class="cta-buttons">
                <a href="https://www.youtube.com/@ranushworld" class="btn btn-primary" target="_blank">Subscribe on YouTube</a>
                <a href="#videos" class="btn btn-secondary">Watch Videos</a>
            </div>
        </div>
    </section>

    <!-- ============ ABOUT SECTION ============ -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <div class="about-text">
                    <h3>Hi, I'm Ranush! 👋</h3>
                    <p>Welcome to my YouTube channel! I'm a content creator passionate about creating engaging, entertaining, and educational videos for viewers around the world.</p>
                    <p>From tutorials to vlogs, entertainment to life advice, I create diverse content that resonates with millions of subscribers globally.</p>
                    <p>Join me on this exciting journey and be part of the Ranush World community!</p>
                    <a href="https://www.youtube.com/@ranushworld" class="btn btn-primary" target="_blank" style="margin-top: 1rem;">Subscribe Now</a>
                </div>
                <div class="about-image">🎥</div>
            </div>
        </div>
    </section>

    <!-- ============ FEATURES SECTION ============ -->
    <section class="features" id="features">
        <div class="container">
            <h2 class="section-title">Why Join Ranush World?</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">🎯</div>
                    <h3>Quality Content</h3>
                    <p>High-quality videos with professional production standards</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">💡</div>
                    <h3>Diverse Topics</h3>
                    <p>Entertainment, education, tutorials, and inspiring stories</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🤝</div>
                    <h3>Community</h3>
                    <p>Connect with millions of subscribers in our engaged community</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">⏰</div>
                    <h3>Regular Updates</h3>
                    <p>New videos uploaded regularly to keep you entertained</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🌟</div>
                    <h3>Exclusive Content</h3>
                    <p>Behind-the-scenes and exclusive content for subscribers</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🚀</div>
                    <h3>Growing Community</h3>
                    <p>Join millions who are already part of the Ranush World family</p>
                </div>
            </div>
        </div>
    </section>

    <!-- ============ STATS SECTION ============ -->
    <section class="stats">
        <div class="container">
            <h2 class="section-title" style="color: var(--white); margin-bottom: 3rem;">Our Community</h2>
            <div class="stats-grid">
                <div class="stat-item">
                    <h3>2.5M+</h3>
                    <p>Subscribers</p>
                </div>
                <div class="stat-item">
                    <h3>500+</h3>
                    <p>Videos</p>
                </div>
                <div class="stat-item">
                    <h3>100M+</h3>
                    <p>Views</p>
                </div>
                <div class="stat-item">
                    <h3>50+</h3>
                    <p>Countries</p>
                </div>
            </div>
        </div>
    </section>

    <!-- ============ VIDEOS SECTION ============ -->
    <section class="videos" id="videos">
        <div class="container">
            <h2 class="section-title">Latest Videos</h2>
            <div class="videos-grid">
                <div class="video-card">
                    <div class="video-thumbnail">
                        <div class="play-btn">▶</div>
                    </div>
                    <div class="video-info">
                        <h3>Amazing Vlog Adventure</h3>
                        <p>Join me on an incredible journey around the world!</p>
                        <div class="video-date">Published 2 days ago</div>
                    </div>
                </div>
                <div class="video-card">
                    <div class="video-thumbnail">
                        <div class="play-btn">▶</div>
                    </div>
                    <div class="video-info">
                        <h3>Tutorial: Learn Web Design</h3>
                        <p>Complete guide to becoming a professional web designer</p>
                        <div class="video-date">Published 5 days ago</div>
                    </div>
                </div>
                <div class="video-card">
                    <div class="video-thumbnail">
                        <div class="play-btn">▶</div>
                    </div>
                    <div class="video-info">
                        <h3>Life Lessons & Motivation</h3>
                        <p>Inspiring stories that will change your perspective</p>
                        <div class="video-date">Published 1 week ago</div>
                    </div>
                </div>
            </div>
            <div style="text-align: center; margin-top: 3rem;">
                <a href="https://www.youtube.com/@ranushworld" class="btn btn-primary" target="_blank">View All Videos</a>
            </div>
        </div>
    </section>

    <!-- ============ CONTACT SECTION ============ -->
    <section class="contact" id="contact">
        <div class="container">
            <h2 class="section-title">Get In Touch</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Follow Me</h3>
                    <div class="contact-item">
                        <div class="contact-item-icon">📧</div>
                        <p>Email: ranush@example.com</p>
                    </div>
                    <div class="contact-item">
                        <div class="contact-item-icon">📱</div>
                        <p>Phone: +1 (555) 123-4567</p>
                    </div>
                    <div class="contact-item">
                        <div class="contact-item-icon">📍</div>
                        <p>Location: Worldwide</p>
                    </div>
                    <h3 style="margin-top: 2rem;">Connect With Me</h3>
                    <div class="social-icons">
                        <a href="https://youtube.com/@ranushworld" class="social-icon" target="_blank">▶</a>
                        <a href="https://instagram.com/ranushworld" class="social-icon" target="_blank">📷</a>
                        <a href="https://twitter.com/ranushworld" class="social-icon" target="_blank">𝕏</a>
                        <a href="https://tiktok.com/@ranushworld" class="social-icon" target="_blank">🎵</a>
                    </div>
                </div>
                <form class="contact-form">
                    <div class="form-group">
                        <label for="name">Your Name</label>
                        <input type="text" id="name" placeholder="Enter your name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Your Email</label>
                        <input type="email" id="email" placeholder="Enter your email" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" placeholder="Your message here..." required></textarea>
                    </div>
                    <button type="submit" class="btn btn-primary">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- ============ FOOTER ============ -->
    <footer>
        <p>&copy; 2026 Ranush World. All rights reserved. | Made with ❤️ for you</p>
    </footer>

    <!-- ============ JAVASCRIPT ============ -->
    <script>
        // Mobile Menu Toggle
        const menuToggle = document.getElementById('menuToggle');
        const navMenu = document.getElementById('navMenu');

        menuToggle.addEventListener('click', () => {
            navMenu.classList.toggle('active');
        });

        // Close menu when link clicked
        navMenu.querySelectorAll('a').forEach(link => {
            link.addEventListener('click', () => {
                navMenu.classList.remove('active');
            });
        });

        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                const href = this.getAttribute('href');
                if (href !== '#') {
                    e.preventDefault();
                    const target = document.querySelector(href);
                    if (target) {
                        target.scrollIntoView({
                            behavior: 'smooth',
                            block: 'start'
                        });
                    }
                }
            });
        });

        // Contact form handler
        document.querySelector('.contact-form').addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Thank you for your message! We will get back to you soon.');
            document.querySelector('.contact-form').reset();
        });

        // Add scroll animation
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animation = 'slideInUp 0.8s ease forwards';
                }
            });
        }, observerOptions);

        document.querySelectorAll('.feature-card, .video-card').forEach(el => {
            observer.observe(el);
        });
    </script>

</body>
</html>
