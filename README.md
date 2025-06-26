<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abi Olawuyi | Elite Salesforce Consultant</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #00A1E0;
            --secondary: #032D60;
            --accent: #FF5D2D;
            --light: #F3F6F9;
            --dark: #181818;
            --success: #2E844A;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        /* Particle Background */
        #particles-js {
            position: fixed;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: linear-gradient(135deg, var(--secondary) 0%, var(--primary) 100%);
        }
        
        /* Navigation */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            padding: 1.5rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
            background-color: rgba(255, 255, 255, 0.9);
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
        }
        
        header.scrolled {
            padding: 1rem 5%;
            background-color: rgba(255, 255, 255, 0.98);
        }
        
        .logo {
            display: flex;
            align-items: center;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
        }
        
        .logo i {
            margin-right: 0.5rem;
            color: var(--primary);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 2.5rem;
        }
        
        .nav-links a {
            color: var(--dark);
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: color 0.3s ease;
            position: relative;
        }
        
        .nav-links a:hover {
            color: var(--primary);
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--primary);
            bottom: -5px;
            left: 0;
            transition: width 0.3s ease;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .hamburger {
            display: none;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            padding: 0 10%;
            position: relative;
            color: white;
            text-align: left;
        }
        
        .hero-content {
            max-width: 800px;
            z-index: 1;
        }
        
        .hero h1 {
            font-size: 4rem;
            font-weight: 800;
            margin-bottom: 1.5rem;
            line-height: 1.2;
            background: linear-gradient(to right, white, #c2e9fb);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .hero h2 {
            font-size: 1.8rem;
            font-weight: 500;
            margin-bottom: 2rem;
            opacity: 0.9;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 3rem;
            max-width: 600px;
            opacity: 0.85;
        }
        
        .cta-buttons {
            display: flex;
            gap: 1.5rem;
        }
        
        .btn {
            display: inline-block;
            padding: 0.8rem 2rem;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            font-size: 1.1rem;
            border: 2px solid transparent;
        }
        
        .btn-primary {
            background-color: var(--accent);
            color: white;
        }
        
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(255, 93, 45, 0.3);
        }
        
        .btn-outline {
            border-color: white;
            color: white;
        }
        
        .btn-outline:hover {
            background-color: white;
            color: var(--primary);
            transform: translateY(-3px);
        }
        
        /* About Section */
        .section {
            padding: 8rem 10%;
            background-color: white;
            position: relative;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 5rem;
            position: relative;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--secondary);
            margin-bottom: 1.5rem;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            background: var(--primary);
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 2px;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 5rem;
        }
        
        .about-img {
            flex: 1;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
        }
        
        .about-img img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s ease;
        }
        
        .about-img:hover img {
            transform: scale(1.05);
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h3 {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            color: var(--secondary);
        }
        
        .about-text p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
            color: #555;
        }
        
        .skills {
            margin-top: 2rem;
        }
        
        .skill-category {
            margin-bottom: 2rem;
        }
        
        .skill-category h4 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            color: var(--secondary);
        }
        
        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
        }
        
        .skill-tag {
            background-color: var(--light);
            color: var(--secondary);
            padding: 0.5rem 1.2rem;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 600;
            display: flex;
            align-items: center;
            transition: all 0.3s ease;
        }
        
        .skill-tag:hover {
            background-color: var(--primary);
            color: white;
            transform: translateY(-2px);
        }
        
        .skill-tag i {
            margin-right: 0.5rem;
        }
        
        /* Services Section */
        .services {
            background-color: var(--light);
        }
        
        .services-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2.5rem;
            margin-top: 3rem;
        }
        
        .service-card {
            background-color: white;
            border-radius: 15px;
            padding: 2.5rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }
        
        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--primary), var(--accent));
            transition: all 0.3s ease;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
        }
        
        .service-card:hover::before {
            height: 10px;
        }
        
        .service-icon {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }
        
        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--secondary);
        }
        
        .service-card p {
            color: #666;
            margin-bottom: 1.5rem;
        }
        
        .service-link {
            display: inline-flex;
            align-items: center;
            color: var(--primary);
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .service-link i {
            margin-left: 0.5rem;
            transition: transform 0.3s ease;
        }
        
        .service-link:hover {
            color: var(--accent);
        }
        
        .service-link:hover i {
            transform: translateX(5px);
        }
        
        /* Portfolio Section */
        .portfolio {
            position: relative;
        }
        
        .portfolio-filters {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1rem;
            margin-bottom: 3rem;
        }
        
        .filter-btn {
            padding: 0.6rem 1.5rem;
            border-radius: 50px;
            background-color: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .filter-btn.active, .filter-btn:hover {
            background-color: var(--primary);
            color: white;
        }
        
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2rem;
        }
        
        .portfolio-item {
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            position: relative;
            transition: all 0.3s ease;
        }
        
        .portfolio-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
        }
        
        .portfolio-img {
            position: relative;
            overflow: hidden;
            height: 250px;
        }
        
        .portfolio-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .portfolio-item:hover .portfolio-img img {
            transform: scale(1.1);
        }
        
        .portfolio-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to top, rgba(3, 45, 96, 0.9), transparent);
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            padding: 2rem;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .portfolio-item:hover .portfolio-overlay {
            opacity: 1;
        }
        
        .portfolio-overlay h3 {
            color: white;
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }
        
        .portfolio-overlay p {
            color: rgba(255, 255, 255, 0.8);
            margin-bottom: 1rem;
        }
        
        .portfolio-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }
        
        .portfolio-tag {
            background-color: rgba(255, 255, 255, 0.2);
            color: white;
            padding: 0.3rem 0.8rem;
            border-radius: 50px;
            font-size: 0.8rem;
        }
        
        .portfolio-links {
            display: flex;
            gap: 1rem;
        }
        
        .portfolio-link {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: var(--primary);
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .portfolio-link:hover {
            background-color: var(--accent);
            transform: translateY(-3px);
        }
        
        /* Testimonials Section */
        .testimonials {
            background-color: var(--light);
        }
        
        .testimonial-slider {
            max-width: 1000px;
            margin: 0 auto;
            position: relative;
        }
        
        .testimonial-card {
            background-color: white;
            border-radius: 15px;
            padding: 3rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            margin: 2rem;
            position: relative;
        }
        
        .testimonial-card::before {
            content: '\201C';
            position: absolute;
            top: 1rem;
            left: 2rem;
            font-size: 5rem;
            color: rgba(0, 161, 224, 0.1);
            font-family: Georgia, serif;
            line-height: 1;
        }
        
        .testimonial-content {
            margin-bottom: 2rem;
            font-size: 1.1rem;
            font-style: italic;
            color: #555;
            position: relative;
            z-index: 1;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .author-img {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 1rem;
        }
        
        .author-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .author-info h4 {
            font-size: 1.2rem;
            color: var(--secondary);
            margin-bottom: 0.3rem;
        }
        
        .author-info p {
            color: #777;
            font-size: 0.9rem;
        }
        
        .testimonial-rating {
            color: var(--accent);
            margin-top: 0.5rem;
        }
        
        /* Contact Section */
        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 5rem;
            margin-top: 3rem;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }
        
        .contact-card {
            display: flex;
            align-items: flex-start;
            gap: 1.5rem;
        }
        
        .contact-icon {
            width: 60px;
            height: 60px;
            background-color: var(--light);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: var(--primary);
            flex-shrink: 0;
        }
        
        .contact-details h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: var(--secondary);
        }
        
        .contact-details p, .contact-details a {
            color: #666;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .contact-details a:hover {
            color: var(--primary);
        }
        
        .contact-form {
            background-color: white;
            padding: 2.5rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--secondary);
        }
        
        .form-control {
            width: 100%;
            padding: 0.8rem 1.2rem;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            transition: all 0.3s ease;
        }
        
        .form-control:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(0, 161, 224, 0.2);
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        .submit-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 0.8rem 2.5rem;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .submit-btn:hover {
            background-color: var(--secondary);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        /* Footer */
        footer {
            background-color: var(--secondary);
            color: white;
            padding: 5rem 10% 2rem;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            margin-bottom: 3rem;
        }
        
        .footer-col h3 {
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            position: relative;
            display: inline-block;
        }
        
        .footer-col h3::after {
            content: '';
            position: absolute;
            width: 50%;
            height: 3px;
            background-color: var(--primary);
            bottom: -8px;
            left: 0;
        }
        
        .footer-col p {
            margin-bottom: 1.5rem;
            opacity: 0.8;
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
        }
        
        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.1);
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .social-link:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 0.8rem;
        }
        
        .footer-links a {
            color: rgba(255, 255, 255, 0.8);
            text-decoration: none;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
        }
        
        .footer-links a:hover {
            color: var(--primary);
            padding-left: 5px;
        }
        
        .footer-links a i {
            margin-right: 0.5rem;
        }
        
        .footer-newsletter input {
            width: 100%;
            padding: 0.8rem 1.2rem;
            border: none;
            border-radius: 50px;
            margin-bottom: 1rem;
            font-size: 1rem;
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .footer-bottom p {
            opacity: 0.7;
            font-size: 0.9rem;
        }
        
        /* Back to Top Button */
        .back-to-top {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            width: 50px;
            height: 50px;
            background-color: var(--primary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            font-size: 1.2rem;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
            z-index: 999;
        }
        
        .back-to-top.active {
            opacity: 1;
            visibility: visible;
        }
        
        .back-to-top:hover {
            background-color: var(--accent);
            transform: translateY(-5px);
        }
        
        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .animate {
            animation: fadeInUp 0.8s ease forwards;
        }
        
        .delay-1 {
            animation-delay: 0.2s;
        }
        
        .delay-2 {
            animation-delay: 0.4s;
        }
        
        .delay-3 {
            animation-delay: 0.6s;
        }
        
        /* Responsive Styles */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 3.5rem;
            }
            
            .about-content {
                flex-direction: column;
                gap: 3rem;
            }
            
            .contact-container {
                grid-template-columns: 1fr;
                gap: 3rem;
            }
        }
        
        @media (max-width: 768px) {
            .nav-links {
                position: fixed;
                top: 80px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background-color: white;
                flex-direction: column;
                align-items: center;
                justify-content: center;
                transition: all 0.5s ease;
                padding: 2rem;
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .nav-links li {
                margin: 1.5rem 0;
            }
            
            .hamburger {
                display: block;
                font-size: 1.8rem;
                color: var(--dark);
            }
            
            .hero {
                padding: 0 5%;
                text-align: center;
            }
            
            .hero-content {
                margin: 0 auto;
                text-align: center;
            }
            
            .hero h1 {
                font-size: 2.8rem;
            }
            
            .hero h2 {
                font-size: 1.5rem;
            }
            
            .cta-buttons {
                justify-content: center;
            }
            
            .section {
                padding: 5rem 5%;
            }
            
            .portfolio-grid {
                grid-template-columns: 1fr;
            }
        }
        
        @media (max-width: 576px) {
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .hero h2 {
                font-size: 1.2rem;
            }
            
            .btn {
                padding: 0.6rem 1.5rem;
                font-size: 1rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .testimonial-card {
                padding: 2rem 1.5rem;
                margin: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Particle Background -->
    <div id="particles-js"></div>
    
    <!-- Header -->
    <header id="header">
        <a href="#" class="logo"><i class="fas fa-cloud"></i> Abi Olawuyi</a>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#portfolio">Portfolio</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
        <div class="hamburger">
            <i class="fas fa-bars"></i>
        </div>
    </header>
    
    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1 class="animate">Transforming Businesses with <span style="color: var(--accent);">Salesforce</span> Excellence</h1>
            <h2 class="animate delay-1">Certified Salesforce Consultant | FSL Expert | Solution Architect</h2>
            <p class="animate delay-2">I help organizations maximize their Salesforce investment through strategic implementation, customization, and automation that drives efficiency, growth, and user adoption.</p>
            <div class="cta-buttons animate delay-3">
                <a href="#portfolio" class="btn btn-primary">View My Work</a>
                <a href="#contact" class="btn btn-outline">Get In Touch</a>
            </div>
        </div>
    </section>
    
    <!-- About Section -->
    <section class="section" id="about">
        <div class="section-title">
            <h2>About Me</h2>
        </div>
        <div class="about-content">
            <div class="about-img">
                <img src="https://images.unsplash.com/photo-1571171637578-41bc2dd41cd2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Abi Olawuyi">
            </div>
            <div class="about-text">
                <h3>Salesforce Consultant with 8+ Years of Transformation Success</h3>
                <p>I'm Abi Olawuyi, a passionate Salesforce professional dedicated to helping businesses leverage the full power of the Salesforce platform. With extensive experience across multiple industries, I bridge the gap between business needs and technical solutions.</p>
                <p>My approach combines deep technical expertise with strategic business acumen to deliver solutions that not only meet requirements but drive measurable ROI. I specialize in complex implementations, process automation, and creating intuitive user experiences that drive adoption.</p>
                
                <div class="skills">
                    <div class="skill-category">
                        <h4>Core Competencies</h4>
                        <div class="skill-tags">
                            <span class="skill-tag"><i class="fas fa-cog"></i> Configuration</span>
                            <span class="skill-tag"><i class="fas fa-magic"></i> Customization</span>
                            <span class="skill-tag"><i class="fas fa-tools"></i> FSL Implementation</span>
                            <span class="skill-tag"><i class="fas fa-robot"></i> Process Automation</span>
                            <span class="skill-tag"><i class="fas fa-project-diagram"></i> Integration</span>
                            <span class="skill-tag"><i class="fas fa-chart-line"></i> Business Analysis</span>
                        </div>
                    </div>
                    
                    <div class="skill-category">
                        <h4>Certifications</h4>
                        <div class="skill-tags">
                            <span class="skill-tag"><i class="fas fa-certificate"></i> Salesforce Certified Administrator</span>
                            <span class="skill-tag"><i class="fas fa-certificate"></i> Salesforce Platform App Builder</span>
                            <span class="skill-tag"><i class="fas fa-certificate"></i> Field Service Lightning Consultant</span>
                            <span class="skill-tag"><i class="fas fa-certificate"></i> Salesforce CPQ Specialist</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Services Section -->
    <section class="section services" id="services">
        <div class="section-title">
            <h2>My Services</h2>
        </div>
        <div class="services-container">
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-sliders-h"></i>
                </div>
                <h3>Salesforce Configuration</h3>
                <p>Tailoring Salesforce to your business processes without code using declarative tools like Flows, Process Builder, and Lightning App Builder.</p>
                <a href="#" class="service-link">Learn More <i class="fas fa-arrow-right"></i></a>
            </div>
            
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-code"></i>
                </div>
                <h3>Custom Development</h3>
                <p>Building custom solutions with Apex, Lightning Web Components, and Visualforce when out-of-the-box features aren't enough.</p>
                <a href="#" class="service-link">Learn More <i class="fas fa-arrow-right"></i></a>
            </div>
            
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-truck"></i>
                </div>
                <h3>Field Service Implementation</h3>
                <p>End-to-end FSL implementations that optimize scheduling, mobile workforce management, and customer service operations.</p>
                <a href="#" class="service-link">Learn More <i class="fas fa-arrow-right"></i></a>
            </div>
            
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-random"></i>
                </div>
                <h3>Process Automation</h3>
                <p>Streamlining business processes with Flow, Process Builder, Approval Processes, and complex workflow automation.</p>
                <a href="#" class="service-link">Learn More <i class="fas fa-arrow-right"></i></a>
            </div>
            
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-plug"></i>
                </div>
                <h3>System Integration</h3>
                <p>Connecting Salesforce with ERP, marketing, billing and other systems using APIs, middleware, and integration patterns.</p>
                <a href="#" class="service-link">Learn More <i class="fas fa-arrow-right"></i></a>
            </div>
            
            <div class="service-card">
                <div class="service-icon">
                    <i class="fas fa-chalkboard-teacher"></i>
                </div>
                <h3>User Training & Adoption</h3>
                <p>Comprehensive training programs and change management strategies to ensure successful Salesforce adoption.</p>
                <a href="#" class="service-link">Learn More <i class="fas fa-arrow-right"></i></a>
            </div>
        </div>
    </section>
    
    <!-- Portfolio Section -->
    <section class="section portfolio" id="portfolio">
        <div class="section-title">
            <h2>Portfolio Projects</h2>
        </div>
        <div class="portfolio-filters">
            <button class="filter-btn active" data-filter="all">All</button>
            <button class="filter-btn" data-filter="fsl">Field Service</button>
            <button class="filter-btn" data-filter="automation">Automation</button>
            <button class="filter-btn" data-filter="integration">Integration</button>
            <button class="filter-btn" data-filter="custom">Custom Solutions</button>
        </div>
        <div class="portfolio-grid">
            <!-- Project 1 -->
            <div class="portfolio-item" data-category="fsl">
                <div class="portfolio-img">
                    <img src="https://images.unsplash.com/photo-1581092918056-0c4c3acd3789?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Field Service Implementation">
                    <div class="portfolio-overlay">
                        <div class="portfolio-tags">
                            <span class="portfolio-tag">Field Service</span>
                            <span class="portfolio-tag">Scheduling</span>
                            <span class="portfolio-tag">Mobile</span>
                        </div>
                        <h3>Global HVAC Service Transformation</h3>
                        <p>Implemented FSL for a multinational HVAC company, reducing service resolution time by 40% and increasing first-time fix rate to 92%.</p>
                        <div class="portfolio-links">
                            <a href="#" class="portfolio-link" title="View Details"><i class="fas fa-eye"></i></a>
                            <a href="#" class="portfolio-link" title="Case Study"><i class="fas fa-file-alt"></i></a>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Project 2 -->
            <div class="portfolio-item" data-category="automation">
                <div class="portfolio-img">
                    <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Process Automation">
                    <div class="portfolio-overlay">
                        <div class="portfolio-tags">
                            <span class="portfolio-tag">Flow</span>
                            <span class="portfolio-tag">Automation</span>
                            <span class="portfolio-tag">Efficiency</span>
                        </div>
                        <h3>Insurance Claims Automation</h3>
                        <p>Automated 85% of manual claims processing for a mid-sized insurer, reducing processing time from 5 days to 4 hours.</p>
                        <div class="portfolio-links">
                            <a href="#" class="portfolio-link" title="View Details"><i class="fas fa-eye"></i></a>
                            <a href="#" class="portfolio-link" title="Case Study"><i class="fas fa-file-alt"></i></a>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Project 3 -->
            <div class="portfolio-item" data-category="integration">
                <div class="portfolio-img">
                    <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="System Integration">
                    <div class="portfolio-overlay">
                        <div class="portfolio-tags">
                            <span class="portfolio-tag">MuleSoft</span>
                            <span class="portfolio-tag">ERP</span>
                            <span class="portfolio-tag">Real-time</span>
                        </div>
                        <h3>Manufacturing ERP Integration</h3>
                        <p>Integrated Salesforce with SAP ERP for a manufacturing client, enabling real-time inventory visibility and reducing order errors by 75%.</p>
                        <div class="portfolio-links">
                            <a href="#" class="portfolio-link" title="View Details"><i class="fas fa-eye"></i></a>
                            <a href="#" class="portfolio-link" title="Case Study"><i class="fas fa-file-alt"></i></a>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Project 4 -->
            <div class="portfolio-item" data-category="custom">
                <div class="portfolio-img">
                    <img src="https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Custom Solution">
                    <div class="portfolio-overlay">
                        <div class="portfolio-tags">
                            <span class="portfolio-tag">LWC</span>
                            <span class="portfolio-tag">Apex</span>
                            <span class="portfolio-tag">Custom</span>
                        </div>
                        <h3>Healthcare Provider Portal</h3>
                        <p>Built a custom patient management portal for healthcare providers with complex referral tracking and compliance requirements.</p>
                        <div class="portfolio-links">
                            <a href="#" class="portfolio-link" title="View Details"><i class="fas fa-eye"></i></a>
                            <a href="#" class="portfolio-link" title="Case Study"><i class="fas fa-file-alt"></i></a>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Project 5 -->
            <div class="portfolio-item" data-category="fsl,automation">
                <div class="portfolio-img">
                    <img src="https://images.unsplash.com/photo-1573164713988-8665fc963095?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1469&q=80" alt="Field Service Automation">
                    <div class="portfolio-overlay">
                        <div class="portfolio-tags">
                            <span class="portfolio-tag">FSL</span>
                            <span class="portfolio-tag">IoT</span>
                            <span class="portfolio-tag">Predictive</span>
                        </div>
                        <h3>IoT-Enabled Predictive Maintenance</h3>
                        <p>Combined FSL with IoT data to create predictive maintenance schedules for industrial equipment, reducing downtime by 60%.</p>
                        <div class="portfolio-links">
                            <a href="#" class="portfolio-link" title="View Details"><i class="fas fa-eye"></i></a>
                            <a href="#" class="portfolio-link" title="Case Study"><i class="fas fa-file-alt"></i></a>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Project 6 -->
            <div class="portfolio-item" data-category="integration,custom">
                <div class="portfolio-img">
                    <img src="https://images.unsplash.com/photo-1563986768609-322da13575f3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Custom Integration">
                    <div class="portfolio-overlay">
                        <div class="portfolio-tags">
                            <span class="portfolio-tag">API</span>
                            <span class="portfolio-tag">Custom</span>
                            <span class="portfolio-tag">E-commerce</span>
                        </div>
                        <h3>E-commerce Order Management</h3>
                        <p>Developed a custom order management system integrating Salesforce with Shopify and warehouse management systems.</p>
                        <div class="portfolio-links">
                            <a href="#" class="portfolio-link" title="View Details"><i class="fas fa-eye"></i></a>
                            <a href="#" class="portfolio-link" title="Case Study"><i class="fas fa-file-alt"></i></a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Testimonials Section -->
    <section class="section testimonials">
        <div class="section-title">
            <h2>Client Testimonials</h2>
        </div>
        <div class="testimonial-slider">
            <div class="testimonial-card">
                <div class="testimonial-content">
                    <p>Abi transformed our field service operations with his FSL implementation. His deep understanding of both the technical and business aspects resulted in a solution that reduced our service costs by 35% while improving customer satisfaction scores. His post-implementation support and training ensured our team was fully prepared to leverage the new system.</p>
                </div>
                <div class="testimonial-author">
                    <div class="author-img">
                        <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Client">
                    </div>
                    <div class="author-info">
                        <h4>Michael Johnson</h4>
                        <p>COO, Global Service Solutions</p>
                        <div class="testimonial-rating">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Contact Section -->
    <section class="section" id="contact">
        <div class="section-title">
            <h2>Get In Touch</h2>
        </div>
        <div class="contact-container">
            <div class="contact-info">
                <div class="contact-card">
                    <div class="contact-icon">
                        <i class="fas fa-envelope"></i>
                    </div>
                    <div class="contact-details">
                        <h3>Email</h3>
                        <a href="mailto:abi@example.com">abi@example.com</a>
                    </div>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">
                        <i class="fas fa-phone-alt"></i>
                    </div>
                    <div class="contact-details">
                        <h3>Phone</h3>
                        <a href="tel:+1234567890">+1 (234) 567-890</a>
                    </div>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">
                        <i class="fas fa-map-marker-alt"></i>
                    </div>
                    <div class="contact-details">
                        <h3>Location</h3>
                        <p>San Francisco, CA</p>
                    </div>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">
                        <i class="fab fa-linkedin-in"></i>
                    </div>
                    <div class="contact-details">
                        <h3>LinkedIn</h3>
                        <a href="https://linkedin.com/in/abiolawuyi" target="_blank">linkedin.com/in/abiolawuyi</a>
                    </div>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">
                        <i class="fab fa-trailhead"></i>
                    </div>
                    <div class="contact-details">
                        <h3>Trailhead</h3>
                        <a href="https://trailblazer.me/id/abiolawuyi" target="_blank">trailblazer.me/id/abiolawuyi</a>
                    </div>
                </div>
            </div>
            
            <div class="contact-form">
                <form>
                    <div class="form-group">
                        <label for="name">Your Name</label>
                        <input type="text" id="name" class="form-control" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="email">Email Address</label>
                        <input type="email" id="email" class="form-control" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="subject">Subject</label>
                        <input type="text" id="subject" class="form-control" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" class="form-control" required></textarea>
                    </div>
                    
                    <button type="submit" class="submit-btn">Send Message</button>
                </form>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-col">
                <h3>Abi Olawuyi</h3>
                <p>Transforming businesses through innovative Salesforce solutions that drive efficiency, growth, and user adoption.</p>
                <div class="social-links">
                    <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                    <a href="#" class="social-link"><i class="fab fa-linkedin-in"></i></a>
                    <a href="#" class="social-link"><i class="fab fa-github"></i></a>
                    <a href="#" class="social-link"><i class="fab fa-trailhead"></i></a>
                </div>
            </div>
            
            <div class="footer-col">
                <h3>Quick Links</h3>
                <ul class="footer-links">
                    <li><a href="#home"><i class="fas fa-chevron-right"></i> Home</a></li>
                    <li><a href="#about"><i class="fas fa-chevron-right"></i> About</a></li>
                    <li><a href="#services"><i class="fas fa-chevron-right"></i> Services</a></li>
                    <li><a href="#portfolio"><i class="fas fa-chevron-right"></i> Portfolio</a></li>
                    <li><a href="#contact"><i class="fas fa-chevron-right"></i> Contact</a></li>
                </ul>
            </div>
            
            <div class="footer-col">
                <h3>Services</h3>
                <ul class="footer-links">
                    <li><a href="#"><i class="fas fa-chevron-right"></i> Salesforce Configuration</a></li>
                    <li><a href="#"><i class="fas fa-chevron-right"></i> Custom Development</a></li>
                    <li><a href="#"><i class="fas fa-chevron-right"></i> FSL Implementation</a></li>
                    <li><a href="#"><i class="fas fa-chevron-right"></i> Process Automation</a></li>
                    <li><a href="#"><i class="fas fa-chevron-right"></i> System Integration</a></li>
                </ul>
            </div>
            
            <div class="footer-col">
                <h3>Newsletter</h3>
                <p>Subscribe to my newsletter for Salesforce tips, industry insights, and project updates.</p>
                <form class="footer-newsletter">
                    <input type="email" placeholder="Your Email Address">
                    <button type="submit" class="btn btn-primary">Subscribe</button>
                </form>
            </div>
        </div>
        
        <div class="footer-bottom">
            <p>&copy; 2023 Abi Olawuyi. All Rights Reserved.</p>
        </div>
    </footer>
    
    <!-- Back to Top Button -->
    <a href="#" class="back-to-top"><i class="fas fa-arrow-up"></i></a>
    
    <!-- Scripts -->
    <script src="https://cdn.jsdelivr.net/particles.js/2.0.0/particles.min.js"></script>
    <script>
        // Mobile Navigation
        const hamburger = document.querySelector('.hamburger');
        const navLinks = document.querySelector('.nav-links');
        
        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            hamburger.innerHTML = navLinks.classList.contains('active') ? 
                '<i class="fas fa-times"></i>' : '<i class="fas fa-bars"></i>';
        });
        
        // Close mobile menu when clicking a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
                hamburger.innerHTML = '<i class="fas fa-bars"></i>';
            });
        });
        
        // Sticky Header
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            header.classList.toggle('scrolled', window.scrollY > 50);
        });
        
        // Back to Top Button
        const backToTopBtn = document.querySelector('.back-to-top');
        
        window.addEventListener('scroll', () => {
            backToTopBtn.classList.toggle('active', window.scrollY > 300);
        });
        
        // Smooth Scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetElement.offsetTop - 80,
                    behavior: 'smooth'
                });
            });
        });
        
        // Portfolio Filtering
        const filterBtns = document.querySelectorAll('.filter-btn');
        const portfolioItems = document.querySelectorAll('.portfolio-item');
        
        filterBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                // Remove active class from all buttons
                filterBtns.forEach(btn => btn.classList.remove('active'));
                // Add active class to clicked button
                btn.classList.add('active');
                
                const filter = btn.getAttribute('data-filter');
                
                portfolioItems.forEach(item => {
                    if (filter === 'all' || item.getAttribute('data-category').includes(filter)) {
                        item.style.display = 'block';
                    } else {
                        item.style.display = 'none';
                    }
                });
            });
        });
        
        // Initialize Particles.js
        particlesJS("particles-js", {
            "particles": {
                "number": {
                    "value": 80,
                    "density": {
                        "enable": true,
                        "value_area": 800
                    }
                },
                "color": {
                    "value": "#ffffff"
                },
                "shape": {
                    "type": "circle",
                    "stroke": {
                        "width": 0,
                        "color": "#000000"
                    },
                    "polygon": {
                        "nb_sides": 5
                    }
                },
                "opacity": {
                    "value": 0.5,
                    "random": false,
                    "anim": {
                        "enable": false,
                        "speed": 1,
                        "opacity_min": 0.1,
                        "sync": false
                    }
                },
                "size": {
                    "value": 3,
                    "random": true,
                    "anim": {
                        "enable": false,
                        "speed": 40,
                        "size_min": 0.1,
                        "sync": false
                    }
                },
                "line_linked": {
                    "enable": true,
                    "distance": 150,
                    "color": "#ffffff",
                    "opacity": 0.4,
                    "width": 1
                },
                "move": {
                    "enable": true,
                    "speed": 2,
                    "direction": "none",
                    "random": false,
                    "straight": false,
                    "out_mode": "out",
                    "bounce": false,
                    "attract": {
                        "enable": false,
                        "rotateX": 600,
                        "rotateY": 1200
                    }
                }
            },
            "interactivity": {
                "detect_on": "canvas",
                "events": {
                    "onhover": {
                        "enable": true,
                        "mode": "grab"
                    },
                    "onclick": {
                        "enable": true,
                        "mode": "push"
                    },
                    "resize": true
                },
                "modes": {
                    "grab": {
                        "distance": 140,
                        "line_linked": {
                            "opacity": 1
                        }
                    },
                    "bubble": {
                        "distance": 400,
                        "size": 40,
                        "duration": 2,
                        "opacity": 8,
                        "speed": 3
                    },
                    "repulse": {
                        "distance": 200,
                        "duration": 0.4
                    },
                    "push": {
                        "particles_nb": 4
                    },
                    "remove": {
                        "particles_nb": 2
                    }
                }
            },
            "retina_detect": true
        });
        
        // Animation on Scroll
        const animateElements = document.querySelectorAll('.animate');
        
        const animateOnScroll = () => {
            animateElements.forEach(element => {
                const elementPosition = element.getBoundingClientRect().top;
                const windowHeight = window.innerHeight;
                
                if (elementPosition < windowHeight - 100) {
                    element.style.opacity = '1';
                    element.style.transform = 'translateY(0)';
                }
            });
        };
        
        // Initial check
        animateOnScroll();
        
        // Check on scroll
        window.addEventListener('scroll', animateOnScroll);
    </script>
</body>
</html>
