<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Webcraft NG | Modern Web Solutions</title>
    <style>
        /* --- RESET & BASIC STYLES --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background-color: #ffffff;
            color: #1a202c;
            line-height: 1.5;
        }

        /* --- UTILITIES & VARIABLES --- */
        .bg-dark { background-color: #050a0e; color: #ffffff; }
        .bg-light { background-color: #f8fafc; }
        .text-green { color: #00a854; }
        
        .btn-green {
            background-color: #00a854;
            color: white;
            padding: 0.75rem 1.75rem;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            transition: background 0.2s ease;
        }
        .btn-green:hover { background-color: #008f47; }

        .btn-white {
            background-color: #ffffff;
            color: #050a0e;
            padding: 0.75rem 1.75rem;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            border: 1px solid #e2e8f0;
            transition: background 0.2s ease;
        }
        .btn-white:hover { background-color: #f1f5f9; }

        .btn-outline {
            border: 1.5px solid #050a0e;
            color: #050a0e;
            padding: 0.6rem 1.5rem;
            border-radius: 50px;
            font-weight: 500;
            text-decoration: none;
            transition: all 0.2s ease;
        }
        .btn-outline:hover {
            background-color: #050a0e;
            color: white;
        }

        /* --- NAVIGATION --- */
        header {
            background: #ffffff;
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid #f1f5f9;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.25rem 2rem;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            letter-spacing: -0.03em;
            color: #050a0e;
            display: flex;
            align-items: center;
        }

        .logo span {
            background: #00a854;
            color: white;
            font-size: 0.75rem;
            padding: 0.2rem 0.4rem;
            border-radius: 4px;
            margin-left: 0.25rem;
            font-weight: 800;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav ul a {
            text-decoration: none;
            color: #4a5568;
            font-weight: 500;
            font-size: 0.95rem;
            transition: color 0.2s;
        }

        nav ul a:hover { color: #00a854; }

        /* --- HERO SECTION --- */
        .hero {
            padding: 6rem 2rem 4rem 2rem;
        }

        .hero-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1.1fr 0.9fr;
            gap: 4rem;
            align-items: center;
        }

        .hero-tag {
            text-transform: uppercase;
            font-size: 0.8rem;
            font-weight: 700;
            letter-spacing: 0.1em;
            margin-bottom: 1rem;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 4.5vw, 3.75rem);
            line-height: 1.15;
            letter-spacing: -0.02em;
            font-weight: 800;
            margin-bottom: 1.5rem;
        }

        .hero p {
            color: #94a3b8;
            font-size: 1.1rem;
            margin-bottom: 2.5rem;
            max-width: 500px;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
            margin-bottom: 3rem;
        }

        /* Mockup Frame Styling */
        .hero-mockup {
            background: #e5dfd3;
            border-radius: 24px;
            padding: 2.5rem 1.5rem 0 1.5rem;
            display: flex;
            justify-content: center;
            overflow: hidden;
            height: 480px;
        }

        .mockup-screen {
            background: #fcfbfa;
            width: 100%;
            border-radius: 12px 12px 0 0;
            border: 8px solid #1a202c;
            border-bottom: none;
            padding: 1.25rem;
            box-shadow: 0 25px 50px -12px rgba(0,0,0,0.5);
            display: flex;
            flex-direction: column;
            color: #2c2622;
        }

        /* Dynamic Uri Essentials Live Elements */
        .uri-mock-nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid #eae5db;
            padding-bottom: 0.75rem;
            margin-bottom: 2rem;
        }
        .uri-mock-logo {
            font-family: "Didot", "Bodoni MT", "Cinzel", serif;
            font-weight: 600;
            font-size: 0.95rem;
            letter-spacing: 0.15em;
            text-transform: uppercase;
        }
        .uri-mock-links {
            display: flex;
            gap: 0.75rem;
            font-size: 0.55rem;
            text-transform: uppercase;
            letter-spacing: 0.05em;
            opacity: 0.6;
        }
        .uri-mock-hero {
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            flex-grow: 1;
            padding-bottom: 2rem;
        }
        .uri-mock-tag {
            font-size: 0.55rem;
            text-transform: uppercase;
            letter-spacing: 0.2em;
            margin-bottom: 0.75rem;
            opacity: 0.7;
        }
        .uri-mock-title {
            font-family: "Didot", "Bodoni MT", "Cinzel", serif;
            font-size: 1.8rem;
            font-weight: 400;
            line-height: 1.2;
            margin-bottom: 1rem;
            letter-spacing: -0.01em;
        }
        .uri-mock-btn {
            font-size: 0.6rem;
            text-transform: uppercase;
            letter-spacing: 0.1em;
            border-bottom: 1px solid #2c2622;
            padding-bottom: 0.25rem;
            text-decoration: none;
            color: #2c2622;
            font-weight: 600;
        }

        /* --- TRUSTED BADGE SECTION --- */
        .trusted-section {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem 4rem 2rem;
        }

        .trusted-wrapper {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .avatar-group {
            display: flex;
        }

        .avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            border: 2px solid #050a0e;
            margin-right: -12px;
            background: #cbd5e1;
            background-size: cover;
        }

        .trusted-text p {
            font-size: 0.9rem;
            font-weight: 600;
        }
        .trusted-text span {
            font-size: 0.8rem;
            color: #64748b;
        }

        /* --- SERVICES SECTION --- */
        .section-header {
            text-align: center;
            padding: 5rem 2rem 3rem 2rem;
        }

        .section-tag {
            text-transform: uppercase;
            font-size: 0.8rem;
            font-weight: 700;
            letter-spacing: 0.1em;
            margin-bottom: 0.75rem;
            display: block;
        }

        .section-header h2 {
            font-size: 2.25rem;
            font-weight: 800;
            letter-spacing: -0.02em;
        }

        .services-grid {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 1.5rem;
            padding: 0 2rem 6rem 2rem;
        }

        .service-card {
            background: #ffffff;
            border: 1px solid #e2e8f0;
            border-radius: 16px;
            padding: 2rem;
            transition: all 0.3s ease;
        }

        .service-card:first-child {
            border-color: #00a854;
            box-shadow: 0 10px 30px rgba(0,168,84,0.05);
        }

        .icon-box {
            width: 45px;
            height: 45px;
            background: #f0fdf4;
            color: #00a854;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1.5rem;
            font-size: 1.25rem;
        }

        .service-card h3 {
            font-size: 1.2rem;
            margin-bottom: 0.75rem;
            font-weight: 700;
        }

        .service-card p {
            color: #64748b;
            font-size: 0.9rem;
            line-height: 1.6;
        }

        /* --- PORTFOLIO SECTION --- */
        .portfolio-grid {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 1.5rem;
            padding: 0 2rem;
        }

        .portfolio-card {
            background: #ffffff;
            border: 1px solid #e2e8f0;
            border-radius: 16px;
            overflow: hidden;
        }

        .portfolio-img {
            height: 220px;
            background: linear-gradient(135deg, #e2e8f0, #cbd5e1);
            position: relative;
            background-size: cover;
            background-position: center;
        }

        .portfolio-info {
            padding: 1.5rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .portfolio-info h3 {
            font-size: 1.1rem;
            font-weight: 700;
            margin-bottom: 0.25rem;
            color: #050a0e;
        }

        .portfolio-info p {
            color: #64748b;
            font-size: 0.85rem;
        }

        .arrow-icon {
            width: 35px;
            height: 35px;
            background: #f0fdf4;
            color: #00a854;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }

        .portfolio-cta {
            text-align: center;
            padding: 3rem 2rem 6rem 2rem;
        }

        /* --- CTA CALLOUT BANNER --- */
        .cta-banner {
            max-width: 1200px;
            margin: 0 auto 6rem auto;
            padding: 0 2rem;
        }

        .cta-box {
            background: #050a0e;
            border-radius: 24px;
            padding: 4rem 3rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 2rem;
        }

        .cta-box h2 {
            color: white;
            font-size: 2rem;
            font-weight: 800;
            margin-bottom: 0.5rem;
        }

        .cta-box p {
            color: #94a3b8;
            font-size: 1rem;
        }

        /* --- FOOTER --- */
        footer {
            border-top: 1px solid #e2e8f0;
            padding-top: 5rem;
        }

        .footer-grid {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1.5fr 1fr 1fr 1.25fr;
            gap: 3rem;
            padding: 0 2rem 4rem 2rem;
        }

        .footer-brand p {
            color: #64748b;
            font-size: 0.95rem;
            margin-top: 1rem;
            margin-bottom: 1.5rem;
            max-width: 280px;
        }

        .social-icons {
            display: flex;
            gap: 0.75rem;
        }

        .social-btn {
            width: 36px;
            height: 36px;
            background: #1a202c;
            border-radius: 50%;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            font-size: 0.9rem;
        }

        .footer-col h4 {
            font-size: 1rem;
            font-weight: 700;
            margin-bottom: 1.5rem;
            color: #ffffff;
        }

        .footer-col ul {
            list-style: none;
        }

        .footer-col ul li {
            margin-bottom: 0.75rem;
        }

        .footer-col ul a {
            color: #64748b;
            text-decoration: none;
            font-size: 0.95rem;
            transition: color 0.2s;
        }

        .footer-col ul a:hover { color: #00a854; }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            color: #64748b;
            font-size: 0.95rem;
            margin-bottom: 0.75rem;
        }

        .footer-bottom {
            border-top: 1px solid rgba(255,255,255,0.05);
            text-align: center;
            padding: 2rem;
            font-size: 0.9rem;
            color: #64748b;
        }

        /* --- SMARTPHONE LAYOUT RESPONSIVENESS --- */
        @media (max-width: 900px) {
            .hero-container {
                grid-template-columns: 1fr;
                gap: 3rem;
                text-align: center;
            }
            .hero p { margin: 0 auto 2.5rem auto; }
            .hero-buttons { justify-content: center; }
            .hero-mockup { height: 380px; }
            
            .cta-box {
                text-align: center;
                justify-content: center;
                padding: 3rem 2rem;
            }

            .footer-grid {
                grid-template-columns: 1fr 1fr;
            }
        }

        @media (max-width: 600px) {
            nav ul, .nav-container .btn-outline {
                display: none;
            }
            .footer-grid {
                grid-template-columns: 1fr;
                gap: 2rem;
            }
        }
    </style>
</head>
<body>

    <!-- 1. NAVIGATION HEADER -->
    <header>
        <div class="nav-container">
            <div class="logo">Webcraft<span>NG</span></div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#portfolio">Portfolio</a></li>
                    <li><a href="#process">Process</a></li>
                    <li><a href="#testimonials">Testimonials</a></li>
                </ul>
            </nav>
            <a href="https://wa.me/2348120807545" target="_blank" class="btn-outline">Let's Talk</a>
        </div>
    </header>

    <!-- 2. HERO SECTION -->
    <section class="bg-dark hero" id="home">
        <div class="hero-container">
            <div class="hero-left">
                <div class="hero-tag text-green">Web Design & Development</div>
                <h1>Websites That<br>Build Brands.<br><span class="text-green">Drive Results.</span></h1>
                <p>We create modern, fast and responsive websites that help Nigerian businesses attract, engage and convert more customers.</p>
                <div class="hero-buttons">
                    <a href="#portfolio" class="btn-green">→ View My Work</a>
                    <a href="https://wa.me/2348120807545" target="_blank" class="btn-white">💬 Chat on WhatsApp</a>
                </div>
            </div>
            <div class="hero-right">
                <!-- Live HTML Rendered Premium Mockup -->
                <div class="hero-mockup">
                    <div class="mockup-screen">
                        <div class="uri-mock-nav">
                            <div class="uri-mock-logo">Uri Essentials</div>
                            <div class="uri-mock-links">
                                <span>Shop</span>
                                <span>Story</span>
                            </div>
                        </div>
                        <div class="uri-mock-hero">
                            <div class="uri-mock-tag">Nourish Your Skin</div>
                            <h2 class="uri-mock-title">Elevate Your Natural Radiance</h2>
                            <a href="#" class="uri-mock-btn" onclick="return false;">Discover Collection</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 3. TRUSTED BADGE STRIP -->
    <section class="bg-dark">
        <div class="trusted-section">
            <div class="trusted-wrapper">
                <div class="avatar-group">
                    <div class="avatar"></div>
                    <div class="avatar"></div>
                    <div class="avatar"></div>
                </div>
                <div class="trusted-text">
                    <p>Trusted by business owners</p>
                    <span>across Nigeria</span>
                </div>
            </div>
        </div>
    </section>

    <!-- 4. SERVICES SECTION -->
    <section class="bg-light" id="services">
        <div class="section-header">
            <span class="section-tag text-green">What I Do</span>
            <h2>Services That Help Your Business Grow</h2>
        </div>
        <div class="services-grid">
            <div class="service-card">
                <div class="icon-box">💻</div>
                <h3>Website Design</h3>
                <p>Beautiful, modern and user-friendly websites that reflect your brand and convert visitors into customers.</p>
            </div>
            <div class="service-card">
                <div class="icon-box">‹›</div>
                <h3>Website Development</h3>
                <p>Fast, responsive and secure websites built with the latest technologies and best practices.</p>
            </div>
            <div class="service-card">
                <div class="icon-box">🛒</div>
                <h3>E-Commerce</h3>
                <p>Online stores that help you sell your products seamlessly and grow your revenue.</p>
            </div>
            <div class="service-card">
                <div class="icon-box">🔍</div>
                <h3>SEO Optimization</h3>
                <p>Improve your visibility on Google and attract more organic traffic to your website.</p>
            </div>
        </div>
    </section>

    <!-- 5. PORTFOLIO SECTION -->
    <section id="portfolio">
        <div class="section-header">
            <span class="section-tag text-green">Featured Projects</span>
            <h2>Some Recent Work</h2>
        </div>
        <div class="portfolio-grid">
            <!-- Project 1: Royal Properties -->
            <div class="portfolio-card">
                <div class="portfolio-img" style="background-image: url('royal.png');"></div>
                <div class="portfolio-info">
                    <div>
                        <h3>Royal Properties</h3>
                        <p class="text-green">Real Estate Brokerage</p>
                    </div>
                    <div class="arrow-icon">↗</div>
                </div>
            </div>
            <!-- Project 2: PrimeCare Clinic -->
            <div class="portfolio-card">
                <div class="portfolio-img" style="background-image: url('primecare.png');"></div>
                <div class="portfolio-info">
                    <div>
                        <h3>PrimeCare Clinic</h3>
                        <p class="text-green">Healthcare Portal</p>
                    </div>
                    <div class="arrow-icon">↗</div>
                </div>
            </div>
            <!-- Project 3: Uri Essentials -->
            <div class="portfolio-card">
                <div class="portfolio-img" style="background-image: url('uri.png');"></div>
                <div class="portfolio-info">
                    <div>
                        <h3>Uri Essentials</h3>
                        <p class="text-green">Skincare E-Commerce</p>
                    </div>
                    <div class="arrow-icon">↗</div>
                </div>
            </div>
            <!-- Project 4: Auron Fly -->
            <div class="portfolio-card">
                <div class="portfolio-img" style="background-image: url('auron.jpg');"></div>
                <div class="portfolio-info">
                    <div>
                        <h3>Auron Fly</h3>
                        <p class="text-green">Private Aviation Brokerage</p>
                    </div>
                    <div class="arrow-icon">↗</div>
                </div>
            </div>
        </div>
        <div class="portfolio-cta">
            <a href="#" class="btn-green">View All Projects</a>
        </div>
    </section>

    <!-- 6. CTA BANNER BLOCK -->
    <section class="cta-banner">
        <div class="cta-box">
            <div>
                <span class="section-tag text-green" style="margin-bottom: 0.25rem;">Let's Work Together</span>
                <h2>Have a Project in Mind?</h2>
                <p>Let's build a website that helps your business stand out and achieve real results.</p>
            </div>
            <a href="https://wa.me/2348120807545" target="_blank" class="btn-green">💬 Chat on WhatsApp</a>
        </div>
    </section>

    <!-- 7. FOOTER SECTION -->
    <footer class="bg-dark">
        <div class="footer-grid">
            <div class="footer-brand">
                <div class="logo" style="color: white;">Webcraft<span style="background: #00a854;">NG</span></div>
                <p>We create modern websites that help Nigerian businesses grow, build trust and attract more customers online.</p>
                <div class="social-icons">
                    <a href="#" class="social-btn">i</a>
                    <a href="#" class="social-btn">l</a>
                    <a href="#" class="social-btn">f</a>
                    <a href="#" class="social-btn">t</a>
                </div>
            </div>
            <div class="footer-col">
                <h4>Quick Links</h4>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#portfolio">Portfolio</a></li>
                    <li><a href="#process">Process</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Services</h4>
                <ul>
                    <li><a href="#">Website Design</a></li>
                    <li><a href="#">Website Development</a></li>
                    <li><a href="#">E-Commerce</a></li>
                    <li><a href="#">SEO Optimization</a></li>
                    <li><a href="#">Website Maintenance</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Contact Us</h4>
                <div class="contact-item">📍 Lagos, Nigeria</div>
                <div class="contact-item">📞 +234 812 080 7545</div>
                <div class="contact-item">✉️ webcraftnglimited@gmail.com</div>
                <div class="contact-item">🕒 Mon - Fri: 9:00am - 6:00pm</div>
            </div>
        </div>
        <div class="footer-bottom">
            &copy; 2026 Webcraft NG. All rights reserved.
        </div>
    </footer>

</body>
</html>
