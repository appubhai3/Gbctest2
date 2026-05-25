<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GBC Ministries | Welcome Home</title>
    <!-- Google Fonts & FontAwesome for Icons -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --bg-main: #0b0c10;
            --bg-card: #1f2833;
            --gold: #d4af37;
            --gold-glow: rgba(212, 175, 55, 0.4);
            --red: #8b0000;
            --red-glow: rgba(139, 0, 0, 0.6);
            --text-light: #c5a059;
            --text-white: #ffffff;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-main);
            color: var(--text-white);
            line-height: 1.6;
        }

        /* Navbar */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(11, 12, 16, 0.95);
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
            z-index: 1000;
            backdrop-filter: blur(10px);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 20px;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--gold);
            text-shadow: 0 0 10px var(--gold-glow);
            text-decoration: none;
        }

        nav a {
            color: var(--text-white);
            text-decoration: none;
            margin-left: 20px;
            font-size: 0.95rem;
            transition: 0.3s;
        }

        nav a:hover {
            color: var(--gold);
            text-shadow: 0 0 8px var(--gold-glow);
        }

        /* Hero Section */
        .hero {
            height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
            background: radial-gradient(circle at center, rgba(139, 0, 0, 0.2) 0%, rgba(11, 12, 16, 1) 70%);
            border-bottom: 2px solid var(--red);
            box-shadow: 0 10px 30px var(--red-glow);
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 10px;
            letter-spacing: 2px;
        }

        .hero h1 span {
            color: var(--gold);
            text-shadow: 0 0 15px var(--gold-glow);
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 600px;
            margin-bottom: 30px;
            color: #ccc;
        }

        .btn-live {
            background: linear-gradient(45deg, var(--red), #b22222);
            color: white;
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 30px;
            font-weight: 600;
            box-shadow: 0 0 15px var(--red-glow);
            transition: 0.3s;
        }

        .btn-live:hover {
            transform: scale(1.05);
            box-shadow: 0 0 25px var(--red-glow);
        }

        /* Section Global Settings */
        section {
            padding: 80px 20px max(80px, 6%);
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.2rem;
            margin-bottom: 50px;
            position: relative;
            color: var(--gold);
            text-shadow: 0 0 10px var(--gold-glow);
        }

        /* Grid Layouts */
        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        /* Cards Style */
        .card {
            background-color: var(--bg-card);
            border: 1px solid rgba(212, 175, 55, 0.1);
            border-radius: 12px;
            padding: 30px;
            text-align: center;
            transition: 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: var(--red);
            box-shadow: 0 5px 20px var(--red-glow);
        }

        .card i {
            font-size: 2.5rem;
            color: var(--gold);
            margin-bottom: 20px;
        }

        .card h3 {
            margin-bottom: 12px;
            font-size: 1.4rem;
        }

        /* Streams / Video Embed Placeholders */
        .media-placeholder {
            background: #111;
            aspect-ratio: 16/9;
            border-radius: 12px;
            border: 1px solid rgba(212, 175, 55, 0.2);
            display: flex;
            justify-content: center;
            align-items: center;
            color: #888;
            position: relative;
            overflow: hidden;
        }

        .media-placeholder:hover {
            border-color: var(--red);
            box-shadow: 0 0 20px var(--red-glow);
        }

        /* Forms styling */
        .form-container {
            max-width: 600px;
            margin: 0 auto;
            background: var(--bg-card);
            padding: 40px;
            border-radius: 15px;
            border: 1px solid rgba(212, 175, 55, 0.1);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: var(--gold);
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 12px;
            background: #0b0c10;
            border: 1px solid #45f3ff33;
            border: 1px solid rgba(212, 175, 55, 0.2);
            color: white;
            border-radius: 6px;
            outline: none;
        }

        .form-group input:focus, .form-group textarea:focus {
            border-color: var(--red);
            box-shadow: 0 0 10px var(--red-glow);
        }

        .btn-submit {
            background: var(--gold);
            color: var(--bg-main);
            border: none;
            width: 100%;
            padding: 14px;
            font-size: 1rem;
            font-weight: bold;
            border-radius: 6px;
            cursor: pointer;
            transition: 0.3s;
        }

        .btn-submit:hover {
            background: white;
            box-shadow: 0 0 15px var(--gold-glow);
        }

        /* Gallery Layout */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 15px;
        }

        .gallery-item {
            aspect-ratio: 1;
            background: #151b24;
            border-radius: 8px;
            overflow: hidden;
            border: 1px solid rgba(212, 175, 55, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* Footer */
        footer {
            background: #050508;
            text-align: center;
            padding: 40px 20px;
            border-top: 1px solid rgba(212, 175, 55, 0.1);
            font-size: 0.9rem;
            color: #777;
        }

        /* Mobile Responsive Design Menu Hidden Logic simplified for pure CSS */
        @media (max-width: 768px) {
            nav {
                display: none; /* Can be expanded with a JS hamburger toggler later */
            }
            .hero h1 {
                font-size: 2.2rem;
            }
        }
    </style>
</head>
<body>

    <!-- Header Navigation -->
    <header>
        <div class="nav-container">
            <a href="#" class="logo">GBC MINISTRIES</a>
            <nav>
                <a href="#services">Services</a>
                <a href="#ministries">Ministries</a>
                <a href="#live">Live Stream</a>
                <a href="#testimonies">Testimonies</a>
                <a href="#gallery">Gallery</a>
                <a href="#prayer">Prayer Request</a>
                <a href="#contact">Contact</a>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h1>WELCOME TO <span>GBC MINISTRIES</span></h1>
        <p>Experiencing God's Grace, Sharing Christ's Love, and Walking in the Spirit together.</p>
        <a href="#live" class="btn-live"><i class="fa-solid fa-play"></i> Watch Live Stream</a>
    </section>

    <!-- Services Section -->
    <section id="services">
        <h2 class="section-title">Sunday Services</h2>
        <div class="grid-3">
            <div class="card">
                <i class="fa-solid fa-cross"></i>
                <h3>Morning Service</h3>
                <p>Join us for our main traditional & contemporary worship experience.</p>
                <p style="color: var(--gold); margin-top: 10px;"><strong>09:00 AM</strong></p>
            </div>
            <div class="card">
                <i class="fa-solid fa-clock"></i>
                <h3>Evening Fellowship</h3>
                <p>An intimate time of deeper study, prayer, and community gathering.</p>
                <p style="color: var(--gold); margin-top: 10px;"><strong>06:30 PM</strong></p>
            </div>
        </div>
    </section>

    <!-- Ministries Section -->
    <section id="ministries" style="background: rgba(255,255,255,0.01);">
        <h2 class="section-title">Our Ministries</h2>
        <div class="grid-3">
            <div class="card">
                <i class="fa-solid fa-book-bible"></i>
                <h3>Sunday School</h3>
                <p>Interactive biblical teaching and foundational growth environments for all ages.</p>
            </div>
            <div class="card">
                <i class="fa-solid fa-child"></i>
                <h3>Children Ministries</h3>
                <p>A fun, energetic, and safe environment where kids discover God's incredible love.</p>
            </div>
            <div class="card">
                <i class="fa-solid fa-fire"></i>
                <h3>Youth Fellowship</h3>
                <p>Empowering the next generation to lead passionate, Christ-centered lifestyles.</p>
            </div>
        </div>
    </section>

    <!-- Live Stream Section -->
    <section id="live">
        <h2 class="section-title">YouTube / YouCam Live</h2>
        <div class="media-placeholder">
            <!-- Tip: You can replace this div with a real YouTube Embed iframe later -->
            <div style="text-align: center; padding: 20px;">
                <i class="fa-brands fa-youtube" style="font-size: 4rem; color: #ff0000; margin-bottom: 10px;"></i>
                <p>Live Broadcast Screen Container</p>
                <p style="font-size: 0.8rem; color: #555;">(Will automatically switch when dynamic link or embed code is attached)</p>
            </div>
        </div>
    </section>

    <!-- Testimonies Section -->
    <section id="testimonies" style="background: rgba(255,255,255,0.01);">
        <h2 class="section-title">Testimonies</h2>
        <div class="grid-3">
            <div class="card" style="text-align: left;">
                <p style="font-style: italic; color: #bbb;">"Finding a home at GBC completely shifted my faith journey. The youth community instantly supported me."</p>
                <h4 style="margin-top:15px; color: var(--gold);">- Joshua K.</h4>
            </div>
            <div class="card" style="text-align: left;">
                <p style="font-style: italic; color: #bbb;">"The Sunday School programs have been an absolute blessing for my kids. They love coming every single week."</p>
                <h4 style="margin-top:15px; color: var(--gold);">- Sarah M.</h4>
            </div>
        </div>
    </section>

    <!-- Photo & Video Gallery Section -->
    <section id="gallery">
        <h2 class="section-title">Photo & Video Gallery</h2>
        <div class="gallery-grid">
            <div class="gallery-item"><i class="fa-regular fa-image" style="color: #444; font-size: 2rem;"></i></div>
            <div class="gallery-item"><i class="fa-regular fa-image" style="color: #444; font-size: 2rem;"></i></div>
            <div class="gallery-item"><i class="fa-regular fa-image" style="color: #444; font-size: 2rem;"></i></div>
            <div class="gallery-item"><i class="fa-regular fa-image" style="color: #444; font-size: 2rem;"></i></div>
        </div>
    </section>

    <!-- Prayer Request Form -->
    <section id="prayer" style="background: rgba(255,255,255,0.01);">
        <h2 class="section-title">Prayer Request</h2>
        <div class="form-container">
            <form action="#" method="POST">
                <div class="form-group">
                    <label for="prayer-name">Your Name</label>
                    <input type="text" id="prayer-name" placeholder="Optional">
                </div>
                <div class="form-group">
                    <label for="prayer-msg">How can we pray for you?</label>
                    <textarea id="prayer-msg" rows="5" required placeholder="Type your prayer request here..."></textarea>
                </div>
                <button type="submit" class="btn-submit">Submit Request</button>
            </form>
        </div>
    </section>

    <!-- Contact Page/Section -->
    <section id="contact">
        <h2 class="section-title">Contact Us</h2>
        <div class="form-container">
            <form action="#" method="POST">
                <div class="form-group">
                    <label for="contact-name">Full Name</label>
                    <input type="text" id="contact-name" required>
                </div>
                <div class="form-group">
                    <label for="contact-email">Email Address</label>
                    <input type="email" id="contact-email" required>
                </div>
                <div class="form-group">
                    <label for="contact-msg">Message</label>
                    <textarea id="contact-msg" rows="4" required></textarea>
                </div>
                <button type="submit" class="btn-submit" style="background: linear-gradient(45deg, var(--red), #b22222); color:white;">Send Message</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 GBC Ministries. All Rights Reserved.</p>
        <p style="margin-top: 5px; font-size: 0.8rem;">Designed cleanly & professionally with dark gold/red glow accents.</p>
    </footer>

</body>
</html>
