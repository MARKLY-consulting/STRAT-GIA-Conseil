<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cabinet Conseil & Law Consulting | Expertise Juridique et Stratégique</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&family=Playfair+Display:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #0d3b66;
            --secondary-color: #1a5a8c;
            --accent-color: #f4a261;
            --light-color: #f8f9fa;
            --dark-color: #212529;
            --gray-color: #6c757d;
            --light-gray: #e9ecef;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            line-height: 1.6;
            color: var(--dark-color);
            background-color: #fff;
        }
        
        h1, h2, h3, h4, h5 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
            line-height: 1.3;
            margin-bottom: 1rem;
        }
        
        h1 {
            font-size: 3rem;
            color: var(--light-color);
        }
        
        h2 {
            font-size: 2.5rem;
            color: var(--primary-color);
            position: relative;
            margin-bottom: 2.5rem;
        }
        
        h2:after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 80px;
            height: 4px;
            background-color: var(--accent-color);
        }
        
        h3 {
            font-size: 1.5rem;
            color: var(--secondary-color);
        }
        
        p {
            margin-bottom: 1.2rem;
            color: var(--gray-color);
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--accent-color);
            color: white;
            text-decoration: none;
            border-radius: 4px;
            font-weight: 600;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            background-color: #e76f51;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--accent-color);
            color: var(--accent-color);
        }
        
        .btn-outline:hover {
            background-color: var(--accent-color);
            color: white;
        }
        
        section {
            padding: 80px 0;
        }
        
        /* Header & Navigation */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo-img {
            max-height: 60px;
            width: auto;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--dark-color);
            font-weight: 500;
            transition: color 0.3s ease;
        }
        
        .nav-links a:hover {
            color: var(--accent-color);
        }
        
        .mobile-menu-btn {
            display: none;
            font-size: 1.5rem;
            background: none;
            border: none;
            color: var(--primary-color);
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(13, 59, 102, 0.9), rgba(13, 59, 102, 0.8)), url('https://images.unsplash.com/photo-1589829545856-d10d557cf95f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 160px 0 100px;
            text-align: center;
        }
        
        .hero p {
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.9);
            max-width: 800px;
            margin: 0 auto 30px;
        }
        
        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }
        
        .about-text p {
            margin-bottom: 20px;
        }
        
        .about-image {
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* Services Section */
        .services {
            background-color: var(--light-gray);
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background-color: white;
            padding: 40px 30px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s ease;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
        }
        
        .service-icon {
            font-size: 2.5rem;
            color: var(--accent-color);
            margin-bottom: 20px;
        }
        
        /* Approach Section */
        .approach-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .approach-item {
            text-align: center;
            padding: 30px 20px;
        }
        
        .approach-icon {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 20px;
        }
        
        /* Clients Section */
        .clients {
            background-color: var(--light-gray);
        }
        
        .clients-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .client-card {
            background-color: white;
            padding: 40px 30px;
            border-radius: 8px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        
        .client-icon {
            font-size: 2.5rem;
            color: var(--secondary-color);
            margin-bottom: 20px;
        }
        
        /* Mission Section */
        .mission {
            background-color: var(--primary-color);
            color: white;
            text-align: center;
        }
        
        .mission h2, .mission p {
            color: white;
        }
        
        .mission h2:after {
            left: 50%;
            transform: translateX(-50%);
        }
        
        /* Footer */
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 60px 0 30px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-logo {
            max-height: 70px;
            width: auto;
            margin-bottom: 20px;
        }
        
        .footer-links h3, .footer-contact h3 {
            color: white;
            font-size: 1.3rem;
            margin-bottom: 20px;
        }
        
        .footer-links ul {
