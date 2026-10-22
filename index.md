Assignment 6.4 — Positioning Practice1. HTML file — Assignment-6.4.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 6.4 - Positioning Practice</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Sticky Navigation Bar -->
    <nav class="navbar">
        <div class="logo">MyWebsite</div>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Home Section -->
    <section id="home" class="section home">
        <h1>Welcome to My Website</h1>
        <p>Learn CSS positioning with this practical webpage.</p>

        <!-- Card with Absolute Positioned Badge -->
        <div class="card">
            <span class="badge">NEW</span>
            <h2>Featured Course</h2>
            <p>
                Learn HTML and CSS to create beautiful,
                responsive websites.
            </p>
            <button>Explore Course</button>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section about">
        <h1>About Us</h1>
        <p>
            We help students learn web development through
            simple examples and practical projects.
        </p>
    </section>

    <!-- Services Section -->
    <section id="services" class="section services">
        <h1>Our Services</h1>
        <p>We provide web design, frontend development,
           and programming tutorials.</p>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section contact">
        <h1>Contact Us</h1>
        <p>Email: hello@example.com</p>
        <p>Phone: +91 98765 43210</p>
    </section>

    <!-- Fixed Floating Help Button -->
    <a class="floating-btn" href="#contact" aria-label="Contact us">
        Help
    </a>

    <footer>
        <p>Assignment 6.4 | CSS Positioning Practice</p>
    </footer>

</body>
</html>
2. CSS file — style.css

css

/* Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    scroll-padding-top: 80px;
}

body {
    font-family: Arial, sans-serif;
    color: #1e293b;
    background-color: #f8fafc;
}

/* Sticky Navigation */
.navbar {
    position: sticky;
    top: 0;
    z-index: 1000;

    display: flex;
    justify-content: space-between;
    align-items: center;

    padding: 18px 8%;
    background-color: #1e293b;
    color: white;
}

.logo {
    font-size: 24px;
    font-weight: bold;
}

.navbar ul {
    display: flex;
    gap: 25px;
    list-style: none;
}

.navbar a {
    color: white;
    text-decoration: none;
    font-weight: bold;
}

.navbar a:hover {
    color: #38bdf8;
}

/* Common Section Styling */
.section {
    min-height: 100vh;
    padding: 70px 8%;
    text-align: center;
}

.section h1 {
    font-size: 36px;
    margin-bottom: 20px;
}

.section p {
    font-size: 18px;
    line-height: 1.8;
}

/* Home Section */
.home {
    background-color: #e0f2fe;
}

.home h1 {
    color: #075985;
}

/* Featured Card */
.card {
    position: relative;
    z-index: 1;

    width: 300px;
    max-width: 100%;
    margin: 60px auto 0;
    padding: 35px 25px 25px;

    background-color: white;
    border: 2px solid #bae6fd;
    border-radius: 15px;
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
}

.card h2 {
    margin-bottom: 15px;
    color: #0369a1;
}

.card p {
    font-size: 15px;
    margin-bottom: 20px;
}

/* Absolute Positioned Badge */
.badge {
    position: absolute;
    top: -12px;
    right: -10px;
    z-index: 2;

    padding: 8px 14px;
    color: white;
    background-color: #ef4444;
    border-radius: 20px;
    font-size: 12px;
    font-weight: bold;
}

/* Card Button */
.card button {
    padding: 12px 20px;
    border: none;
    border-radius: 6px;
    background-color: #0284c7;
    color: white;
    cursor: pointer;
}

.card button:hover {
    background-color: #0369a1;
}

/* About Section */
.about {
    background-color: #dcfce7;
}

.about h1 {
    color: #166534;
}

/* Services Section */
.services {
    background-color: #f3e8ff;
}

.services h1 {
    color: #7e22ce;
}

/* Contact Section */
.contact {
    background-color: #ffedd5;
}

.contact h1 {
    color: #c2410c;
}

/* Fixed Floating Help Button */
.floating-btn {
    position: fixed;
    right: 25px;
    bottom: 25px;
    z-index: 2000;

    display: inline-block;
    padding: 16px 22px;

    background-color: #2563eb;
    color: white;
    text-decoration: none;
    font-weight: bold;
    border-radius: 50px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.25);
}

.floating-btn:hover {
    background-color: #1d4ed8;
}

/* Footer */
footer {
    padding: 20px;
    text-align: center;
    color: white;
    background-color: #1e293b;
}

/* Responsive Navigation */
@media (max-width: 600px) {
    .navbar {
        flex-direction: column;
        gap: 15px;
        padding: 15px 10px;
    }

    .navbar ul {
        flex-wrap: wrap;
        justify-content: center;
        gap: 15px;
    }

    .section {
        padding: 50px 20px;
    }

    .section h1 {
        font-size: 28px