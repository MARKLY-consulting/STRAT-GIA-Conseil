<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>STRATÉGIA Conseil | Accompagnement Stratégique et Opérationnel</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700;800&family=Playfair+Display:wght@400;500;700;800&display=swap" rel="stylesheet">
    <style>
        /* ===== VARIABLES & RESET ===== */
        :root {
            --primary-blue: #0d3b66;
            --secondary-blue: #1a5a8c;
            --accent-gold: #d4af37;
            --accent-light: #f4a261;
            --dark-bg: #1a1d28;
            --light-bg: #f8f9fa;
            --text-dark: #2a2d3a;
            --text-light: #ffffff;
            --gray-light: #e9ecef;
            --gray-medium: #6c757d;
            --success-green: #28a745;
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            line-height: 1.7;
            color: var(--text-dark);
            background-color: var(--light-bg);
            overflow-x: hidden;
        }

        /* ===== TYPOGRAPHY ===== */
        h1, h2, h3, h4, h5 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
            line-height: 1.3;
            margin-bottom: 1.5rem;
        }

        h1 {
            font-size: 3.5rem;
            font-weight: 800;
        }

        h2 {
            font-size: 2.8rem;
            color: var(--primary-blue);
            position: relative;
            padding-bottom: 1rem;
        }

        h2:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 80px;
            height: 4px;
            background: linear-gradient(to right, var(--accent-gold), var(--accent-light));
            border-radius: 2px;
        }

        h3 {
            font-size: 1.8rem;
            color: var(--secondary-blue);
        }

        p {
            margin-bottom: 1.5rem;
            color: var(--gray-medium);
            font-size: 1.1rem;
        }

        .highlight {
            color: var(--accent-gold);
            font-weight: 600;
        }

        /* ===== LAYOUT ===== */
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        section {
            padding: 100px 0;
        }

        .text-center {
            text-align: center;
        }

        .text-center h2:after {
            left: 50%;
            transform: translateX(-50%);
        }

        /* ===== BUTTONS ===== */
        .btn {
            display: inline-block;
            padding: 15px 35px;
            background: linear-gradient(135deg, var(--primary-blue), var(--secondary-blue));
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1.1rem;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .btn:before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, var(--accent-gold), var(--accent-light));
            transition: all 0.5s ease;
            z-index: -1;
        }

        .btn:hover:before {
            left: 0;
        }

        .btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(13, 59, 102, 0.2);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary-blue);
            color: var(--primary-blue);
        }

        .btn-outline:before {
            background: linear-gradient(135deg, var(--primary-blue), var(--secondary-blue));
        }

        .btn-outline:hover {
            color: white;
        }

        /* ===== HEADER & NAVIGATION ===== */
        header {
            background-color: white;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            transition: var(--transition);
        }

        .header-scrolled {
            padding: 10px 0;
            background-color: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
        }

        .logo-img {
            height: 50px;
            width: auto;
            margin-right: 15px;
        }

        .logo-text {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            font-weight: 800;
            background: linear-gradient(135deg, var(--primary-blue), var(--secondary-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .logo-tagline {
            font-size: 0.9rem;
            color: var(--gray-medium);
            font-weight: 500;
            letter-spacing: 2px;
            margin-top: 5px;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 40px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            font-size: 1rem;
            transition: var(--transition);
            position: relative;
            padding: 5px 0;
        }

        .nav-links a:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(to right, var(--accent-gold), var(--accent-light));
            transition: width 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--primary-blue);
        }

        .nav-links a:hover:after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.8rem;
            color: var(--primary-blue);
            cursor: pointer;
        }

        /* ===== HERO SECTION ===== */
        .hero {
            background: linear-gradient(rgba(13, 59, 102, 0.85), rgba(26, 90, 140, 0.9)), 
                        url('https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&auto=format&fit=crop&w=1600&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            padding: 180px 0 120px;
            text-align: center;
            position: relative;
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 30px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .hero p {
            font-size: 1.3rem;
            max-width: 800px;
            margin: 0 auto 40px;
            color: rgba(255, 255, 255, 0.9);
        }

        .hero-badge {
            display: inline-block;
            background: rgba(212, 175, 55, 0.2);
            border: 1px solid var(--accent-gold);
            color: var(--accent-gold);
            padding: 10px 25px;
            border-radius: 50px;
            font-weight: 600;
            margin-top: 30px;
            backdrop-filter: blur(10px);
        }

        /* ===== ABOUT SECTION ===== */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .about-text h3 {
            margin-bottom: 25px;
        }

        .about-features {
            margin-top: 40px;
        }

        .feature-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 25px;
        }

        .feature-icon {
            flex-shrink: 0;
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--primary-blue), var(--secondary-blue));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            margin-right: 20px;
            box-shadow: var(--shadow);
        }

        .feature-text h4 {
            font-size: 1.3rem;
            margin-bottom: 8px;
            color: var(--text-dark);
        }

        .about-image {
            border-radius: 20px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transform: perspective(1000px) rotateY(-5deg);
            transition: var(--transition);
        }

        .about-image:hover {
            transform: perspective(1000px) rotateY(0deg);
        }

        .about-image img {
            width: 100%;
            height: 500px;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .about-image:hover img {
            transform: scale(1.05);
        }

        /* ===== SERVICES SECTION ===== */
        .services {
            background-color: var(--gray-light);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-top: 60px;
        }

        .service-card {
            background: white;
            padding: 50px 35px;
            border-radius: 15px;
            box-shadow: var(--shadow);
            transition: var(--transition);
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .service-card:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--accent-gold), var(--accent-light));
        }

        .service-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        .service-icon {
            font-size: 3.5rem;
            margin-bottom: 25px;
            background: linear-gradient(135deg, var(--primary-blue), var(--secondary-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* ===== MODALITES SECTION ===== */
        .modalites {
            background: linear-gradient(135deg, var(--primary-blue), var(--secondary-blue));
            color: white;
        }

        .modalites h2, .modalites p, .modalites h3 {
            color: white;
        }

        .modalites h2:after {
            background: linear-gradient(to right, var(--accent-gold), var(--accent-light));
        }

        .modalites-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-top: 60px;
        }

        .modalite-card {
            background: rgba(255, 255, 255, 0.1);
            padding: 40px 30px;
            border-radius: 15px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: var(--transition);
        }

        .modalite-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.15);
        }

        .modalite-icon {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--accent-gold);
        }

        /* ===== CONTACT SECTION ===== */
        .contact {
            background-color: var(--light-bg);
        }

        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            padding: 30px;
            background: white;
            border-radius: 15px;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .contact-item:hover {
            transform: translateY(-10px);
        }

        .contact-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--primary-blue), var(--secondary-blue));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            margin-right: 20px;
            flex-shrink: 0;
        }

        .contact-details h4 {
            font-size: 1.2rem;
            margin-bottom: 8px;
            color: var(--text-dark);
        }

        .contact-details p {
            margin-bottom: 0;
            color: var(--gray-medium);
        }

        /* ===== FOOTER ===== */
        footer {
            background-color: var(--dark-bg);
            color: var(--text-light);
            padding: 80px 0 30px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 50px;
            margin-bottom: 50px;
        }

        .footer-logo {
            font-size: 2.2rem;
            font-weight: 800;
            background: linear-gradient(135deg, var(--accent-gold), var(--accent-light));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 15px;
        }

        .footer-about p {
            color: rgba(255, 255, 255, 0.7);
        }

        .footer-links h3, .footer-contact h3 {
            color: white;
            font-size: 1.3rem;
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-links h3:after, .footer-contact h3:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 2px;
            background: linear-gradient(to right, var(--accent-gold), var(--accent-light));
        }

        .footer-links ul {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 12px;
        }

        .footer-links a {
            color: rgba(255, 255, 255, 0.7);
            text-decoration: none;
            transition: var(--transition);
            display: flex;
            align-items: center;
        }

        .footer-links a:hover {
            color: var(--accent-gold);
            transform: translateX(5px);
        }

        .footer-links i {
            margin-right: 10px;
            color: var(--accent-gold);
        }

        .footer-contact p {
            color: rgba(255, 255, 255, 0.7);
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }

        .footer-contact i {
            margin-right: 15px;
            color: var(--accent-gold);
            font-size: 1.2rem;
            width: 25px;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-link {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
            transition: var(--transition);
        }

        .social-link:hover {
            background: var(--accent-gold);
            transform: translateY(-5px);
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.5);
            font-size: 0.9rem;
        }

        /* ===== RESPONSIVE DESIGN ===== */
        @media (max-width: 992px) {
            h1 {
                font-size: 3rem;
            }
            
            h2 {
                font-size: 2.3rem;
            }
            
            .about-content {
                grid-template-columns: 1fr;
                gap: 40px;
            }
            
            .about-image {
                order: -1;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: fixed;
                top: 80px;
                left: 0;
                width: 100%;
                background: white;
                flex-direction: column;
                padding: 30px;
                box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
                gap: 20px;
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero {
                padding: 150px 0 80px;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            section {
                padding: 70px 0;
            }
            
            .service-card, .modalite-card {
                padding: 35px 25px;
            }
        }

        @media (max-width: 480px) {
            h1 {
                font-size: 2.2rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            .btn {
                padding: 12px 25px;
                font-size: 1rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .feature-item {
                flex-direction: column;
            }
            
            .feature-icon {
                margin-bottom: 15px;
            }
        }

        /* ===== ANIMATIONS ===== */
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .fade-in {
            animation: fadeIn 0.8s ease forwards;
        }
    </style>
</head>
<body>
    <!-- HEADER -->
    <header id="header">
        <div class="container nav-container">
            <a href="#" class="logo">
                <!-- VOTRE LOGO ICI -->
                <img src="https://github.com/user-attachments/assets/0d5ecc40-4652-447a-84d4-13e6f5d3a74b" alt="STRATÉGIA Conseil" class="logo-img">
                <div>
                    <div class="logo-text">STRATÉGIA</div>
                    <div class="logo-tagline">CONSEIL</div>
                </div>
            </a>
            
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>
            
            <ul class="nav-links" id="navLinks">
                <li><a href="#accueil"><i class="fas fa-home"></i> Accueil</a></li>
                <li><a href="#apropos"><i class="fas fa-building"></i> À Propos</a></li>
                <li><a href="#services"><i class="fas fa-briefcase"></i> Services</a></li>
                <li><a href="#modalites"><i class="fas fa-handshake"></i> Modalités</a></li>
                <li><a href="#contact"><i class="fas fa-envelope"></i> Contact</a></li>
            </ul>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section class="hero" id="accueil">
        <div class="container">
            <h1 class="fade-in">GU<span class="highlight">IDING</span> YOUR AMBITION</h1>
            <p class="fade-in">Expert en stratégie et accompagnement opérationnel, je vous guide vers l'excellence. Ensemble, transformons vos ambitions en réalisations tangibles et durables.</p>
            <a href="#contact" class="btn fade-in">Prendre rendez-vous</a>
            <div class="hero-badge fade-in">
                <i class="fas fa-map-marker-alt"></i> Service avec déplacement & meetings à distance
            </div>
        </div>
    </section>

    <!-- ABOUT SECTION -->
    <section id="apropos">
        <div class="container">
            <h2 class="text-center">Notre Approche</h2>
            <div class="about-content">
                <div class="about-text fade-in">
                    <h3>Votre Partenaire en Excellence Stratégique</h3>
                    <p>STRATÉGIA Conseil combine expertise analytique et accompagnement personnalisé pour propulser votre entreprise vers de nouveaux sommets. Nous croyons en une approche sur mesure, adaptée à vos besoins spécifiques.</p>
                    
                    <div class="about-features">
                        <div class="feature-item">
                            <div class="feature-icon">
                                <i class="fas fa-bullseye"></i>
                            </div>
                            <div class="feature-text">
                                <h4>Stratégie Sur Mesure</h4>
                                <p>Des solutions adaptées à votre contexte unique et à vos objectifs spécifiques.</p>
                            </div>
                        </div>
                        
                        <div class="feature-item">
                            <div class="feature-icon">
                                <i class="fas fa-chart-line"></i>
                            </div>
                            <div class="feature-text">
                                <h4>Résultats Tangibles</h4>
                                <p>Une approche orientée résultats avec des indicateurs de performance clairs.</p>
                            </div>
                        </div>
                        
                        <div class="feature-item">
                            <div class="feature-icon">
                                <i class="fas fa-handshake"></i>
                            </div>
                            <div class="feature-text">
                                <h4>Accompagnement Continu</h4>
                                <p>Un suivi régulier et un support constant tout au long du processus.</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="about-image fade-in">
                    <img src="https://images.unsplash.com/photo-1556761175-b413da4baf72?ixlib=rb-4.0.3&auto=format&fit=crop&w=1600&q=80" alt="Consultation stratégique">
                </div>
            </div>
        </div>
    </section>

    <!-- SERVICES SECTION -->
    <section class="services" id="services">
        <div class="container">
            <h2 class="text-center">Nos Services</h2>
            <p class="text-center" style="max-width: 800px; margin: 0 auto 50px;">Des services complets adaptés aux besoins des entreprises modernes, avec un accompagnement personnalisé.</p>
            
            <div class="services-grid">
                <div class="service-card fade-in">
                    <div class="service-icon">
                        <i class="fas fa-chess-king"></i>
                    </div>
                    <h3>Conseil Stratégique</h3>
                    <p>Développement de stratégies sur mesure pour la croissance et l'optimisation de votre entreprise. Analyse approfondie et plan d'action concret.</p>
                </div>
                
                <div class="service-card fade-in">
                    <div class="service-icon">
                        <i class="fas fa-cogs"></i>
                    </div>
                    <h3>Optimisation Opérationnelle</h3>
                    <p>Amélioration de vos processus internes pour augmenter l'efficacité, réduire les coûts et améliorer la qualité de vos services.</p>
                </div>
                
                <div class="service-card fade-in">
                    <div class="service-icon">
                        <i class="fas fa-rocket"></i>
                    </div>
                    <h3>Accompagnement Digital</h3>
                    <p>Transformation digitale de votre entreprise avec des solutions technologiques adaptées à votre secteur d'activité.</p>
                </div>
                
                <div class="service-card fade-in">
                    <div class="service-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3>Formation & Coaching</h3>
                    <p>Formation de vos équipes et coaching des dirigeants pour développer les compétences nécessaires à votre succès.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- MODALITES SECTION -->
    <section class="modalites" id="modalites">
        <div class="container">
            <h2 class="text-center">Modalités d'Intervention</h2>
            <p class="text-center" style="max-width: 800px; margin: 0 auto 50px; color: rgba(255, 255, 255, 0.9);">Une flexibilité totale pour s'adapter à vos contraintes et préférences.</p>
            
            <div class="modalites-grid">
                <div class="modalite-card fade-in">
                    <div class="modalite-icon">
                        <i class="fas fa-car"></i>
                    </div>
                    <h3>Déplacement Chez Vous</h3>
                    <p>Je me déplace directement dans vos locaux pour une analyse sur place et des réunions en face-à-face. Parfait pour une immersion totale dans votre environnement.</p>
                </div>
                
                <div class="modalite-card fade-in">
                    <div class="modalite-icon">
                        <i class="fas fa-video"></i>
                    </div>
                    <h3>Meetings à Distance</h3>
                    <p>Consultations via visioconférence pour une flexibilité maximale. Idéal pour les suivis réguliers ou lorsque le déplacement n'est pas possible.</p>
                </div>
                
                <div class="modalite-card fade-in">
                    <div class="modalite-icon">
                        <i class="fas fa-calendar-alt"></i>
                    </div>
                    <h3>Hybride & Flexible</h3>
                    <p>Combinaison des deux approches selon vos besoins. Certaines étapes en présentiel, d'autres à distance pour optimiser temps et efficacité.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- CONTACT SECTION -->
    <section class="contact" id="contact">
        <div class="container">
            <h2 class="text-center">Contactez-nous</h2>
            <p class="text-center" style="max-width: 800px; margin: 0 auto 50px;">Discutons de vos projets et voyons comment nous pouvons travailler ensemble pour atteindre vos objectifs.</p>
            
            <div class="contact-info">
                <div class="contact-item fade-in">
                    <div class="contact-icon">
                        <i class="fas fa-envelope"></i>
                    </div>
                    <div class="contact-details">
                        <h4>Email</h4>
                        <p>oulkaidkhadija4@gmail.com</p>
                    </div>
                </div>
                
                <div class="contact-item fade-in">
                    <div class="contact-icon">
                        <i class="fas fa-phone"></i>
                    </div>
                    <div class="contact-details">
                        <h4>Téléphone</h4>
                        <p>+33 6 12 34 56 78</p>
                    </div>
                </div>
                
                <div class="contact-item fade-in">
                    <div class="contact-icon">
                        <i class="fas fa-map-marker-alt"></i>
                    </div>
                    <div class="contact-details">
                        <h4>Zone d'Intervention</h4>
                        <p>Déplacement dans toute la région - Meetings à distance disponibles</p>
                    </div>
                </div>
                
                <div class="contact-item fade-in">
                    <div class="contact-icon">
                        <i class="fas fa-clock"></i>
                    </div>
                    <div class="contact-details">
                        <h4>Disponibilité</h4>
                        <p>Lun-Ven: 8h-19h<br>Sur rendez-vous uniquement</p>
                    </div>
                </div>
            </div>
            
            <div class="text-center" style="margin-top: 60px;">
                <a href="mailto:oulkaidkhadija4@gmail.com" class="btn">
                    <i class="fas fa-paper-plane"></i> Envoyer un email
                </a>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-about">
                    <div class="footer-logo">STRATÉGIA</div>
                    <p>Expert en stratégie et accompagnement opérationnel. Nous transformons vos ambitions en réussites tangibles grâce à une approche personnalisée et des résultats mesurables.</p>
                    
                    <div class="social-links">
                        <a href="#" class="social-link"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-facebook-f"></i></a>
                    </div>
                </div>
                
                <div class="footer-links">
                    <h3>Liens Rapides</h3>
                    <ul>
                        <li><a href="#accueil"><i class="fas fa-chevron-right"></i> Accueil</a></li>
                        <li><a href="#apropos"><i class="fas fa-chevron-right"></i> À Propos</a></li>
                        <li><a href="#services"><i class="fas fa-chevron-right"></i> Services</a></li>
                        <li><a href="#modalites"><i class="fas fa-chevron-right"></i> Modalités</a></li>
                        <li><a href="#contact"><i class="fas fa-chevron-right"></i> Contact</a></li>
                    </ul>
                </div>
                
                <div class="footer-contact">
                    <h3>Coordonnées</h3>
                    <p><i class="fas fa-envelope"></i> oulkaidkhadija4@gmail.com</p>
                    <p><i class="fas fa-phone"></i> +33 6 12 34 56 78</p>
                    <p><i class="fas fa-map-marker-alt"></i> Déplacement régional & meetings à distance</p>
                    <p><i class="fas fa-clock"></i> Sur rendez-vous</p>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 STRATÉGIA Conseil. Tous droits réservés.</p>
                <p style="margin-top: 10px;">Site conçu avec <i class="fas fa-heart" style="color: #f4a261;"></i> pour votre réussite</p>
            </div>
        </div>
    </footer>

    <script>
        // Menu Mobile
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const navLinks = document.getElementById('navLinks');
        
        mobileMenuBtn.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            mobileMenuBtn.innerHTML = navLinks.classList.contains('active') 
                ? '<i class="fas fa-times"></i>' 
                : '<i class="fas fa-bars"></i>';
        });
        
        // Fermer le menu en cliquant sur un lien
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
                mobileMenuBtn.innerHTML = '<i class="fas fa-bars"></i>';
            });
        });
        
        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if (window.scrollY > 50) {
                header.classList.add('header-scrolled');
            } else {
                header.classList.remove('header-scrolled');
            }
        });
        
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('fade-in');
                }
            });
        }, observerOptions);
        
        // Observe elements
        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });
        
        // Initialize
        window.dispatchEvent(new Event('scroll'));
    </script>
</body>
</html>
