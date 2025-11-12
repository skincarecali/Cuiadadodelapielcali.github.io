# <!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DermoCare - Dermofarmacia Especializada en Cali</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Raleway:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --color-blanco: #FFFFFF;
            --color-beige: #F5F1E6;
            --color-marron-claro: #D7CEC7;
            --color-marron-oscuro: #8B6B61;
            --color-texto: #4A3F35;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Raleway', sans-serif;
            background-color: var(--color-beige);
            color: var(--color-texto);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            color: var(--color-marron-oscuro);
            margin-bottom: 20px;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        /* Header Styles */
        header {
            background-color: var(--color-blanco);
            box-shadow: 0 2px 15px rgba(0,0,0,0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            animation: slideDown 0.8s ease-out;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo i {
            font-size: 2.5rem;
            color: var(--color-marron-oscuro);
            margin-right: 10px;
            animation: pulse 2s infinite;
        }
        
        .logo h1 {
            font-size: 1.8rem;
            margin: 0;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 25px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: var(--color-texto);
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            position: relative;
        }
        
        nav ul li a:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background-color: var(--color-marron-oscuro);
            transition: width 0.3s ease;
        }
        
        nav ul li a:hover:after {
            width: 100%;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(245, 241, 230, 0.9), rgba(215, 206, 199, 0.7)), 
                        url('https://images.unsplash.com/photo-1607522370275-f14206abe5d3?ixlib=rb-4.0.3&auto=format&fit=crop&w=1950&q=80') center/cover;
            display: flex;
            align-items: center;
            text-align: center;
            margin-top: 80px;
            padding: 0 20px;
            animation: fadeIn 1.5s ease-out;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.8);
            padding: 40px;
            border-radius: 20px;
            backdrop-filter: blur(5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        .hero h2 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            color: var(--color-texto);
            animation: slideInDown 1s ease-out;
        }
        
        .hero p {
            font-size: 1.5rem;
            margin-bottom: 30px;
            animation: slideInUp 1s ease-out;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--color-marron-oscuro);
            color: var(--color-blanco);
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            animation: pulse 2s infinite;
            border: 2px solid var(--color-marron-oscuro);
        }
        
        .btn:hover {
            background-color: transparent;
            color: var(--color-marron-oscuro);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        /* About Section */
        .about {
            padding: 100px 0;
            background-color: var(--color-blanco);
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
            position: relative;
        }
        
        .section-title:after {
            content: '';
            position: absolute;
            width: 80px;
            height: 3px;
            background-color: var(--color-marron-oscuro);
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            animation: float 4s ease-in-out infinite;
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s ease;
        }
        
        .about-image:hover img {
            transform: scale(1.05);
        }
        
        /* Services Section */
        .services {
            padding: 100px 0;
            background-color: var(--color-beige);
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background-color: var(--color-blanco);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            animation: fadeInUp 1s ease-out;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }
        
        .service-img {
            height: 200px;
            overflow: hidden;
        }
        
        .service-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .service-card:hover .service-img img {
            transform: scale(1.1);
        }
        
        .service-content {
            padding: 25px;
        }
        
        .service-content h3 {
            margin-bottom: 15px;
            color: var(--color-marron-oscuro);
        }
        
        /* Products Section */
        .products {
            padding: 100px 0;
            background-color: var(--color-blanco);
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .product-card {
            background-color: var(--color-beige);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            animation: fadeIn 1s ease-out;
        }
        
        .product-card:hover {
            transform: scale(1.03);
        }
        
        .product-img {
            height: 250px;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: var(--color-blanco);
            overflow: hidden;
            position: relative;
        }
        
        .product-img img {
            max-width: 80%;
            max-height: 80%;
            transition: transform 0.5s ease;
        }
        
        .product-card:hover .product-img img {
            transform: scale(1.1);
        }
        
        .product-info {
            padding: 20px;
            text-align: center;
        }
        
        .product-info h3 {
            margin-bottom: 10px;
        }
        
        .price {
            font-weight: 700;
            color: var(--color-marron-oscuro);
            font-size: 1.3rem;
            margin: 10px 0;
        }
        
        .price:before {
            content: '$';
        }
        
        .price:after {
            content: ' COP';
            font-size: 0.9rem;
        }
        
        /* Location Section */
        .location {
            padding: 100px 0;
            background-color: var(--color-beige);
            text-align: center;
        }
        
        .location-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .location-content p {
            margin-bottom: 30px;
            font-size: 1.1rem;
        }
        
        .map {
            height: 400px;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            margin-top: 40px;
            background: url('https://images.unsplash.com/photo-1598005192528-33e5c3a8f29c?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80') center/cover;
            animation: fadeIn 1.5s ease-out;
            position: relative;
        }
        
        .map-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(215, 206, 199, 0.3);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            font-weight: bold;
            text-shadow: 0 2px 4px rgba(0,0,0,0.5);
        }
        
        /* Footer */
        footer {
            background-color: var(--color-texto);
            color: var(--color-beige);
            padding: 50px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            color: var(--color-blanco);
            margin-bottom: 20px;
            position: relative;
        }
        
        .footer-column h3:after {
            content: '';
            position: absolute;
            width: 40px;
            height: 2px;
            background-color: var(--color-marron-claro);
            bottom: -8px;
            left: 0;
        }
        
        .footer-column p, .footer-column li {
            margin-bottom: 10px;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column a {
            color: var(--color-beige);
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .footer-column a:hover {
            color: var(--color-blanco);
            padding-left: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: var(--color-marron-claro);
            color: var(--color-texto);
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background-color: var(--color-blanco);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 0.9rem;
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes slideInDown {
            from { 
                transform: translateY(-50px);
                opacity: 0;
            }
            to { 
                transform: translateY(0);
                opacity: 1;
            }
        }
        
        @keyframes slideInUp {
            from { 
                transform: translateY(50px);
                opacity: 0;
            }
            to { 
                transform: translateY(0);
                opacity: 1;
            }
        }
        
        @keyframes fadeInUp {
            from { 
                transform: translateY(30px);
                opacity: 0;
            }
            to { 
                transform: translateY(0);
                opacity: 1;
            }
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0px); }
        }
        
        @keyframes slideDown {
            from { 
                transform: translateY(-100%);
            }
            to { 
                transform: translateY(0);
            }
        }
        
        .service-card:nth-child(1) { animation-delay: 0.1s; }
        .service-card:nth-child(2) { animation-delay: 0.2s; }
        .service-card:nth-child(3) { animation-delay: 0.3s; }
        
        .product-card:nth-child(1) { animation-delay: 0.1s; }
        .product-card:nth-child(2) { animation-delay: 0.2s; }
        .product-card:nth-child(3) { animation-delay: 0.3s; }
        .product-card:nth-child(4) { animation-delay: 0.4s; }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                padding: 15px;
            }
            
            nav ul {
                margin-top: 15px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            nav ul li {
                margin: 5px 10px;
            }
            
            .hero h2 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .hero-content {
                padding: 20px;
            }
        }
        
        /* Corazón flotante */
        .floating-heart {
            position: fixed;
            bottom: 20px;
            right: 20px;
            font-size: 2rem;
            color: #e91e63;
            animation: floatHeart 3s ease-in-out infinite;
            z-index: 1000;
            pointer-events: none;
        }
        
        @keyframes floatHeart {
            0% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(10deg); }
            100% { transform: translateY(0) rotate(0deg); }
        }
    </style>
</head>
<body>
    <!-- Corazón flotante especial -->
    <div class="floating-heart">❤️</div>

    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <i class="fas fa-spa"></i>
                <h1>DermoCare</h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#nosotros">Nosotros</a></li>
                    <li><a href="#servicios">Servicios</a></li>
                    <li><a href="#productos">Productos</a></li>
                    <li><a href="#ubicacion">Ubicación</a></li>
                    <li><a href="#contacto">Contacto</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <div class="hero-content">
            <h2>Dermofarmacia Especializada en Cali</h2>
            <p>Cuidado experto para tu piel con productos farmacéuticos de alta calidad</p>
            <a href="#servicios" class="btn">Descubre nuestros tratamientos</a>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="nosotros">
        <div class="container">
            <div class="section-title">
                <h2>Sobre la Dermofarmacia</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <p>En DermoCare, ubicada en el corazón de Cali, Colombia, combinamos el conocimiento farmacéutico con la ciencia dermatológica para ofrecerte soluciones personalizadas para el cuidado de tu piel.</p>
                    <p>Nuestro equipo de profesionales altamente capacitados está dedicado a brindarte asesoramiento experto y productos de calidad farmacéutica que se adaptan a las necesidades específicas de tu piel.</p>
                    <p>Entendemos que cada piel es única, por eso desarrollamos tratamientos personalizados que abordan problemas específicos como acné, rosácea, envejecimiento prematuro, sensibilidad y pigmentación irregular.</p>
                    <p>En nuestra farmacia dermatológica, todos los productos son seleccionados rigurosamente por su eficacia comprobada, seguridad y calidad, garantizando resultados visibles y duraderos.</p>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1591348131719-8c1a7b9b5c3d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Dermofarmacia interior">
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="servicios">
        <div class="container">
            <div class="section-title">
                <h2>Nuestros Servicios</h2>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-img">
                        <img src="https://images.unsplash.com/photo-1556228720-195a672e8a03?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Análisis de piel">
                    </div>
                    <div class="service-content">
                        <h3>Análisis de Piel Personalizado</h3>
                        <p>Evaluación profesional de tu tipo de piel y sus necesidades específicas mediante tecnología avanzada.</p>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-img">
                        <img src="https://images.unsplash.com/photo-1576097449790-4ec0b69d0d7b?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Tratamientos personalizados">
                    </div>
                    <div class="service-content">
                        <h3>Tratamientos Personalizados</h3>
                        <p>Diseño de rutinas de cuidado específicas para problemas dermatológicos como acné, rosácea o envejecimiento.</p>
                    </div>
                </div>
                
                <div class="service-card">
                    <d
