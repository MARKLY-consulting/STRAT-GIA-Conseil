<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MARKLY - Conseil & Accompagnement Digital</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* RESET ET BASE */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-blue: #3A56E4;
            --electric-blue: #4A6EFF;
            --violet: #8A2BE2;
            --orange: #FF7A45;
            --neon-green: #00FF9D;
            --dark-bg: #1A1D28;
            --light-bg: #F8F9FA;
            --text-dark: #2A2D3A;
            --text-light: #FFFFFF;
            --gray: #6C757D;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            background-color: var(--light-bg);
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* LOGO MARKLY - Version moderne */
        .logo-container {
            text-align: center;
            padding: 40px 0 20px;
        }

        .markly-logo {
            font-size: 4.5rem;
            font-weight: 900;
            letter-spacing: 2px;
            text-transform: uppercase;
            background: linear-gradient(90deg, var(--primary-blue), var(--violet));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            position: relative;
            display: inline-block;
        }

        .markly-logo::after {
            content: '';
            position: absolute;
            width: 100%;
            height: 5px;
            bottom: -10px;
            left: 0;
            background: linear-gradient(90deg, var(--primary-blue), var(--violet));
            border-radius: 3px;
        }

        /* HERO SECTION */
        .hero {
            background: linear-gradient(rgba(26, 29, 40, 0.9), rgba(26, 29, 40, 0.95)), 
                        url('https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80');
            background-size: cover;
            background-position: center;
            color: var(--text-light);
            padding: 80px 0;
            text-align: center;
            border-radius: 20px;
            margin: 30px auto;
            max-width: 95%;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            background: linear-gradient(90deg, var(--electric-blue), var(--neon-green));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero p {
            font-size: 1.3rem;
            max-width: 800px;
            margin: 0 auto 30px;
            color: rgba(255, 255, 255, 0.85);
        }

        .cta-button {
            display: inline-block;
            background: linear-gradient(90deg, var(--primary-blue), var(--violet));
            color: white;
            padding: 15px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(58, 86, 228, 0.4);
        }

        .cta-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(58, 86, 228, 0.6);
        }

        /* SERVICES SECTION */
        .services {
            padding: 80px 0;
            text-align: center;
        }

        .section-title {
            font-size: 2.5rem;
            margin-bottom: 50px;
            color: var(--text-dark);
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary-blue), var(--violet));
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 2px;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .service-card {
            background: white;
            padding: 40px 25px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            text-align: center;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(58, 86, 228, 0.15);
        }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 20px;
            background: linear-gradient(90deg, var(--primary-blue), var(--violet));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--text-dark);
        }

        .service-card p {
            color: var(--gray);
        }

        /* SERVICE EN DIRECT */
        .direct-service {
            padding: 80px 0;
            background: linear-gradient(135deg, var(--primary-blue), var(--violet));
            color: white;
            text-align: center;
            border-radius: 20px;
            margin: 50px auto;
            max-width: 95%;
        }

        .direct-service h2 {
            font-size: 2.5rem;
            margin-bottom: 30px;
            color: white;
        }

        .direct-service-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            align-items: center;
        }

        .direct-service-text {
            text-align: left;
        }

        .direct-service-text h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--neon-green);
        }

        .direct-service-text ul {
            list-style: none;
            margin: 20px 0;
        }

        .direct-service-text li {
            margin-bottom: 15px;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
        }

        .direct-service-text i {
            color: var(--neon-green);
            margin-right: 10px;
            font-size: 1.2rem;
        }

        .direct-service-image {
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
        }

        .direct-service-image img {
            width: 100%;
            height: auto;
            display: block;
        }

        /* PALETTE DE COULEURS */
        .color-palette {
            padding: 60px 0;
            background-color: #f5f7ff;
            border-radius: 20px;
            margin: 50px auto;
            max-width: 95%;
        }

        .color-grid {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 40px;
        }

        .color-item {
            text-align: center;
        }

        .color-box {
            width: 100px;
            height: 100px;
            border-radius: 10px;
            margin-bottom: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        /* FOOTER */
        footer {
            background-color: var(--dark-bg);
            color: var(--text-light);
            padding: 60px 0 30px;
            margin-top: 80px;
            text-align: center;
        }

        .footer-logo {
            font-size: 2.5rem;
            font-weight: 900;
            background: linear-gradient(90deg, var(--electric-blue), var(--neon-green));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 20px;
        }

        .contact-info {
            margin: 30px 0;
        }

        .contact-item {
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 15px 0;
            font-size: 1.1rem;
        }

        .contact-item i {
            color: var(--neon-green);
            margin-right: 15px;
            font-size: 1.3rem;
        }

        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
        }

        .social-icon {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
            transition: all 0.3s ease;
        }

        .social-icon:hover {
            background: var(--primary-blue);
            transform: translateY(-5px);
        }

        .copyright {
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.6);
            font-size: 0.9rem;
        }

        /* RESPONSIVE */
        @media (max-width: 768px) {
            .markly-logo {
                font-size: 3rem;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .direct-service-content {
                grid-template-columns: 1fr;
            }
            
            .direct-service-text {
                text-align: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- LOGO MARKLY -->
        <div class="logo-container">
            <div class="markly-logo">MARKLY</div>
        </div>

        <!-- HERO SECTION -->
        <section class="hero">
            <h1>Accompagnement Digital Personnalisé</h1>
            <p>Je me déplace directement chez vous pour créer des stratégies digitales sur mesure. Augmentez votre visibilité, engagez votre audience et maximisez votre ROI avec un accompagnement personnalisé.</p>
            <a href="#contact" class="cta-button">Prendre rendez-vous</a>
        </section>

        <!-- SERVICES -->
        <section class="services">
            <h2 class="section-title">Mes Services</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3>SEO & Référencement</h3>
                    <p>Optimisation pour les moteurs de recherche pour améliorer votre visibilité et attirer un trafic qualifié.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-bullhorn"></i>
                    </div>
                    <h3>Publicité Digitale</h3>
                    <p>Campagnes publicitaires ciblées sur les réseaux sociaux et moteurs de recherche pour maximiser votre portée.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-paint-brush"></i>
                    </div>
                    <h3>Création de Contenu</h3>
                    <p>Contenu engageant et stratégique qui captive votre audience et renforce votre image de marque.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-analytics"></i>
                    </div>
                    <h3>Analyse de Données</h3>
                    <p>Suivi, analyse et reporting des performances pour optimiser continuellement vos stratégies digitales.</p>
                </div>
            </div>
        </section>

        <!-- SERVICE EN DIRECT -->
        <section class="direct-service">
            <h2>Service en Direct</h2>
            <div class="direct-service-content">
                <div class="direct-service-text">
                    <h3>Je me déplace chez vous !</h3>
                    <p>Je propose un accompagnement personnalisé en présentiel pour mieux comprendre vos besoins et votre environnement de travail.</p>
                    <ul>
                        <li><i class="fas fa-check-circle"></i> Analyse sur place de votre activité</li>
                        <li><i class="fas fa-check-circle"></i> Formation personnalisée à votre équipe</li>
                        <li><i class="fas fa-check-circle"></i> Stratégie adaptée à votre marché local</li>
                        <li><i class="fas fa-check-circle"></i> Mise en place concrète avec vous</li>
                        <li><i class="fas fa-check-circle"></i> Suivi régulier en présentiel</li>
                    </ul>
                </div>
                <div class="direct-service-image">
                    <img src="https://images.unsplash.com/photo-1556761175-b413da4baf72?ixlib=rb-4.0.3&auto=format&fit=crop&w=1374&q=80" alt="Consultation en entreprise">
                </div>
            </div>
        </section>

        <!-- PALETTE DE COULEURS -->
        <section class="color-palette">
            <h2 class="section-title">Palette de Couleurs</h2>
            <div class="color-grid">
                <div class="color-item">
                    <div class="color-box" style="background-color: #3A56E4;"></div>
                    <p>Bleu Principal<br>#3A56E4</p>
                </div>
                <div class="color-item">
                    <div class="color-box" style="background-color: #8A2BE2;"></div>
                    <p>Violet<br>#8A2BE2</p>
                </div>
                <div class="color-item">
                    <div class="color-box" style="background-color: #FF7A45;"></div>
                    <p>Orange Vif<br>#FF7A45</p>
                </div>
                <div class="color-item">
                    <div class="color-box" style="background-color: #00FF9D;"></div>
                    <p>Vert Néon<br>#00FF9D</p>
                </div>
                <div class="color-item">
                    <div class="color-box" style="background-color: #2A2D3A;"></div>
                    <p>Gris Anthracite<br>#2A2D3A</p>
                </div>
            </div>
        </section>
    </div>

    <!-- FOOTER -->
    <footer id="contact">
        <div class="container">
            <div class="footer-logo">MARKLY</div>
            <p style="color: rgba(255, 255, 255, 0.8); max-width: 600px; margin: 0 auto;">Accompagnement digital personnalisé avec déplacement chez vous pour des résultats concrets.</p>
            
            <div class="contact-info">
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <span>oulkaidkhadija4@gmail.com</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-phone"></i>
                    <span>+33 6 12 34 56 78</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <span>Je me déplace dans toute la région</span>
                </div>
            </div>
            
            <div class="social-icons">
                <a href="#" class="social-icon"><i class="fab fa-facebook-f"></i></a>
                <a href="#" class="social-icon"><i class="fab fa-twitter"></i></a>
                <a href="#" class="social-icon"><i class="fab fa-instagram"></i></a>
                <a href="#" class="social-icon"><i class="fab fa-linkedin-in"></i></a>
                <a href="#" class="social-icon"><i class="fab fa-tiktok"></i></a>
            </div>
            
            <div class="copyright">
                &copy; 2023 MARKLY - Conseil Digital. Tous droits réservés.
            </div>
        </div>
    </footer>
</body>
</html>
