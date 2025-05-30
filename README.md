<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Farmacia Nieto - Tu camino hacia el bienestar</title>
    <meta name="description" content="Farmacia especializada en elaboración magistral personalizada. Medicina ortomolecular, dermocosmética, homeopatía y más. Atención personalizada desde 1996.">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: #333;
            background: #fafafa;
        }

        .header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 1rem 5%;
            z-index: 1000;
            border-bottom: 1px solid #86a486;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .header-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            max-width: 1200px;
            margin: 0 auto;
        }

        .logo {
            display: flex;
            align-items: center;
            font-size: 1.5rem;
            font-weight: 800;
            color: #86a486;
            text-decoration: none;
        }

        .logo-icon {
            width: 35px;
            height: 35px;
            background: #86a486;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 10px;
            color: white;
            font-size: 18px;
        }

        .nav {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav a {
            color: #666;
            text-decoration: none;
            font-weight: 500;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            transition: all 0.3s ease;
        }

        .nav a:hover {
            color: #86a486;
            background: rgba(134, 164, 134, 0.1);
        }

        .whatsapp-btn {
            background: #86a486;
            color: white;
            padding: 0.7rem 1.5rem;
            border: none;
            border-radius: 25px;
            font-weight: 600;
            cursor: pointer;
            text-decoration: none;
            transition: all 0.3s ease;
            font-size: 14px;
        }

        .whatsapp-btn:hover {
            background: #2d4a2d;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(134, 164, 134, 0.3);
        }

        .hero {
            background: linear-gradient(135deg, #f8fcf8 0%, #e8f4e8 100%);
            padding: 8rem 5% 4rem;
            text-align: center;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto 3rem;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 5vw, 4rem);
            font-weight: 900;
            color: #2d4a2d;
            margin-bottom: 1rem;
            line-height: 1.2;
        }

        .hero-subtitle {
            font-size: clamp(1.2rem, 3vw, 1.8rem);
            color: #86a486;
            font-weight: 600;
            margin-bottom: 1.5rem;
        }

        .hero-description {
            font-size: 1.1rem;
            color: #666;
            margin-bottom: 2rem;
            line-height: 1.7;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 3rem;
        }

        .btn-primary {
            background: linear-gradient(135deg, #86a486, #9bb49b);
            color: white;
            padding: 1rem 2rem;
            border: none;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(134, 164, 134, 0.3);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(134, 164, 134, 0.4);
        }

        .btn-secondary {
            background: transparent;
            color: #86a486;
            padding: 1rem 2rem;
            border: 2px solid #86a486;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            transition: all 0.3s ease;
        }

        .btn-secondary:hover {
            background: #86a486;
            color: white;
            transform: translateY(-3px);
        }

        .professional-card {
            background: white;
            border-radius: 20px;
            padding: 2.5rem;
            box-shadow: 0 20px 40px rgba(134, 164, 134, 0.15);
            max-width: 600px;
            margin: 0 auto;
            border: 2px solid rgba(134, 164, 134, 0.2);
            position: relative;
            overflow: hidden;
        }

        .professional-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #86a486, #9bb49b, #86a486);
        }

        .card-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            display: block;
        }

        .card-title {
            color: #86a486;
            font-size: 0.9rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 0.5rem;
        }

        .card-name {
            color: #2d4a2d;
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
        }

        .card-role {
            color: #86a486;
            font-size: 1rem;
            font-weight: 500;
            margin-bottom: 1.5rem;
        }

        .stats {
            display: flex;
            justify-content: space-around;
            margin: 1.5rem 0;
            padding: 1.5rem 0;
            border-top: 1px solid rgba(134, 164, 134, 0.2);
            border-bottom: 1px solid rgba(134, 164, 134, 0.2);
            background: rgba(134, 164, 134, 0.05);
            border-radius: 10px;
        }

        .stat {
            text-align: center;
        }

        .stat-number {
            display: block;
            font-size: 1.8rem;
            font-weight: 900;
            color: #86a486;
            line-height: 1;
        }

        .stat-label {
            font-size: 0.7rem;
            color: #666;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-top: 0.5rem;
        }

        .credentials {
            margin-top: 1.5rem;
        }

        .credentials p {
            color: #666;
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

        .section {
            padding: 5rem 5%;
        }

        .section-title {
            text-align: center;
            font-size: clamp(2rem, 4vw, 3rem);
            font-weight: 800;
            color: #2d4a2d;
            margin-bottom: 1rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 4px;
            background: linear-gradient(90deg, #86a486, #9bb49b);
            border-radius: 2px;
        }

        .section-subtitle {
            text-align: center;
            font-size: 1.2rem;
            color: #86a486;
            margin-bottom: 3rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .services {
            background: white;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .service-card {
            background: linear-gradient(135deg, #f8fcf8, #ffffff);
            border-radius: 15px;
            padding: 2rem;
            text-align: center;
            border: 2px solid rgba(134, 164, 134, 0.1);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, #86a486, #9bb49b);
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }

        .service-card:hover::before {
            transform: scaleX(1);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(134, 164, 134, 0.2);
            border-color: #86a486;
        }

        .service-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            display: block;
            transition: transform 0.3s ease;
        }

        .service-card:hover .service-icon {
            transform: scale(1.1) rotate(5deg);
        }

        .service-card h3 {
            color: #2d4a2d;
            font-size: 1.3rem;
            margin-bottom: 1rem;
            font-weight: 600;
        }

        .service-card p {
            color: #666;
            line-height: 1.6;
        }

        .contact {
            background: #2d4a2d;
            color: white;
        }

        .contact-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .contact-info h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .contact-description {
            font-size: 1.1rem;
            opacity: 0.9;
            margin-bottom: 2rem;
            line-height: 1.6;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
            padding: 1.2rem;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            transition: all 0.3s ease;
            cursor: pointer;
            border: 2px solid transparent;
        }

        .contact-item:hover {
            background: rgba(255, 255, 255, 0.15);
            transform: translateX(10px);
            border-color: #9bb49b;
        }

        .contact-item-icon {
            font-size: 1.5rem;
            margin-right: 1rem;
            width: 40px;
            text-align: center;
        }

        .contact-item h4 {
            margin-bottom: 0.3rem;
            font-size: 1.1rem;
        }

        .contact-item p {
            opacity: 0.9;
        }

        .director-info {
            text-align: center;
            background: rgba(255, 255, 255, 0.1);
            padding: 2rem;
            border-radius: 15px;
            backdrop-filter: blur(10px);
        }

        .director-info h3 {
            color: #9bb49b;
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        .director-details {
            font-size: 1.1rem;
            margin-bottom: 2rem;
            line-height: 1.6;
        }

        .director-details strong {
            display: block;
            margin-bottom: 0.5rem;
            color: #9bb49b;
        }

        .footer {
            background: #1a2e1a;
            color: white;
            padding: 3rem 5% 1rem;
            text-align: center;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h4 {
            color: #9bb49b;
            margin-bottom: 1rem;
            font-size: 1.2rem;
        }

        .footer-section p {
            margin-bottom: 0.5rem;
            opacity: 0.9;
            font-size: 0.9rem;
        }

        .footer-bottom {
            border-top: 1px solid rgba(255, 255, 255, 0.2);
            padding-top: 1rem;
            margin-top: 2rem;
            opacity: 0.8;
            font-size: 0.9rem;
        }

        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 60px;
            height: 60px;
            background: #25d366;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            text-decoration: none;
            z-index: 1000;
            box-shadow: 0 5px 20px rgba(37, 211, 102, 0.4);
            transition: all 0.3s ease;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { 
                box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.7); 
            }
            70% { 
                box-shadow: 0 0 0 10px rgba(37, 211, 102, 0); 
            }
            100% { 
                box-shadow: 0 0 0 0 rgba(37, 211, 102, 0); 
            }
        }

        .whatsapp-float:hover {
            transform: scale(1.1);
            box-shadow: 0 8px 25px rgba(37, 211, 102, 0.6);
        }

        .mobile-menu {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: #86a486;
            cursor: pointer;
        }

        @media (max-width: 768px) {
            .nav {
                display: none;
            }

            .mobile-menu {
                display: block;
            }

            .header-content {
                justify-content: space-between;
            }

            .hero {
                padding: 6rem 5% 3rem;
            }

            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }

            .btn-primary,
            .btn-secondary {
                width: 100%;
                max-width: 280px;
                justify-content: center;
            }

            .contact-content {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            .services-grid {
                grid-template-columns: 1fr;
            }

            .stats {
                flex-wrap: wrap;
                gap: 1rem;
            }

            .stat {
                flex: 1;
                min-width: 80px;
            }

            .footer-content {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .whatsapp-float {
                bottom: 20px;
                right: 20px;
                width: 50px;
                height: 50px;
                font-size: 1.2rem;
            }
        }

        @media (max-width: 480px) {
            .professional-card {
                padding: 1.5rem;
                margin: 0 1rem;
            }

            .stats {
                flex-direction: column;
                align-items: center;
                gap: 1rem;
            }

            .stat {
                min-width: 120px;
            }
        }

        html {
            scroll-behavior: smooth;
        }

        .section {
            scroll-margin-top: 80px;
        }
    </style>
</head>
<body>
    <header class="header">
        <div class="header-content">
            <a href="#inicio" class="logo">
                <div class="logo-icon">⚕️</div>
                Farmacia Nieto
            </a>
            <nav class="nav">
                <a href="#inicio">Inicio</a>
                <a href="#servicios">Servicios</a>
                <a href="#contacto">Contacto</a>
            </nav>
            <button class="mobile-menu">☰</button>
            <a href="#contacto" class="whatsapp-btn" onclick="openWhatsApp()">💬 WhatsApp</a>
        </div>
    </header>

    <section id="inicio" class="hero">
        <div class="hero-content">
            <h1>Tu camino hacia el bienestar</h1>
            <p class="hero-subtitle">Elaboración Magistral Personalizada</p>
            <p class="hero-description">
                Bajo la dirección técnica de Patricia Victoria Nieto, farmacéutica con una larga trayectoria, 
                te ofrecemos productos de calidad y una atención de excelencia personalizada para cuidar tu salud.
            </p>
            <div class="hero-buttons">
                <a href="#servicios" class="btn-primary">
                    <span>🔍</span> Conocer Servicios
                </a>
                <a href="#contacto" class="btn-secondary">
                    <span>💬</span> Consultar Ahora
                </a>
            </div>
        </div>

        <div class="professional-card">
            <span class="card-icon">⚕️</span>
            <div class="card-title">Dirección Técnica</div>
            <div class="card-name">Patricia Victoria Nieto</div>
            <div class="card-role">Farmacéutica Profesional</div>
            
            <div class="stats">
                <div class="stat">
                    <span class="stat-number">28+</span>
                    <span class="stat-label">Años</span>
                </div>
                <div class="stat">
                    <span class="stat-number">1000+</span>
                    <span class="stat-label">Pacientes</span>
                </div>
                <div class="stat">
                    <span class="stat-number">8</span>
                    <span class="stat-label">Especialidades</span>
                </div>
            </div>
            
            <div class="credentials">
                <p><span>🎓</span> Matrícula del Colegio de Farmacéuticos</p>
                <p><span>🔬</span> Especialista en Elaboración Magistral</p>
                <p><span>📍</span> Universidad Nacional</p>
                <p><span>⭐</span> Desde 1996 al servicio de la comunidad</p>
            </div>
        </div>
    </section>

    <section id="servicios" class="section services">
        <h2 class="section-title">Nuestros Servicios</h2>
        <p class="section-subtitle">
            Formulaciones personalizadas según las necesidades de cada paciente
        </p>
        
        <div class="services-grid">
            <div class="service-card">
                <span class="service-icon">💊</span>
                <h3>Medicina Ortomolecular</h3>
                <p>Tratamientos personalizados basados en el equilibrio molecular óptimo para restaurar la salud natural del organismo.</p>
            </div>
            
            <div class="service-card">
                <span class="service-icon">✨</span>
                <h3>Dermocosmética</h3>
                <p>Productos especializados para el cuidado de la piel, formulados específicamente para cada tipo y necesidad.</p>
            </div>
            
            <div class="service-card">
                <span class="service-icon">🌿</span>
                <h3>Homeopatía</h3>
                <p>Preparaciones homeopáticas tradicionales elaboradas con los más altos estándares de calidad y pureza.</p>
            </div>
            
            <div class="service-card">
                <span class="service-icon">🔬</span>
                <h3>Alopatía</h3>
                <p>Medicamentos alopáticos preparados magistralmente según prescripción médica con máxima precisión.</p>
            </div>
            
            <div class="service-card">
                <span class="service-icon">🧘‍♀️</span>
                <h3>Fitoterapia</h3>
                <p>Tratamientos naturales a base de plantas medicinales, respaldados por la tradición y la ciencia moderna.</p>
            </div>
            
            <div class="service-card">
                <span class="service-icon">🌸</span>
                <h3>Florales</h3>
                <p>Esencias florales de Bach y otros sistemas para el equilibrio emocional y el bienestar integral.</p>
            </div>
            
            <div class="service-card">
                <span class="service-icon">🦠</span>
                <h3>Probióticos</h3>
                <p>Formulaciones probióticas específicas para restaurar y mantener el equilibrio de la flora intestinal.</p>
            </div>
            
            <div class="service-card">
                <span class="service-icon">🧬</span>
                <h3>Hormonas Bioidénticas</h3>
                <p>Terapias hormonales personalizadas con hormonas bioidénticas para el equilibrio hormonal natural.</p>
            </div>
        </div>
    </section>

    <section id="contacto" class="section contact">
        <div class="contact-content">
            <div class="contact-info">
                <h2>Contactanos</h2>
                <p class="contact-description">
                    Para más asesoramiento y consultas, comunicate con nosotros. 
                    ¡Cuidamos de ti de manera personalizada!
                </p>
                
                <div class="contact-item" onclick="openWhatsApp()">
                    <span class="contact-item-icon">📱</span>
                    <div>
                        <h4>WhatsApp</h4>
                        <p>(+54) 291432-7031</p>
                    </div>
                </div>
                
                <div class="contact-item" onclick="window.open('mailto:farmacia.nieto@hotmail.com')">
                    <span class="contact-item-icon">✉️</span>
                    <div>
                        <h4>Email</h4>
                        <p>farmacia.nieto@hotmail.com</p>
                    </div>
                </div>
                
                <div class="contact-item">
                    <span class="contact-item-icon">📍</span>
                    <div>
                        <h4>Ubicación</h4>
                        <p>Bahía Blanca, Buenos Aires, Argentina</p>
                    </div>
                </div>
                
                <div class="contact-item">
                    <span class="contact-item-icon">⏰</span>
                    <div>
                        <h4>Horarios</h4>
                        <p>Lun-Vie: 8:00-20:00<br>Sáb: 8:00-13:00</p>
                    </div>
                </div>
            </div>
            
            <div class="director-info">
                <h3>¡Estamos aquí para ayudarte!</h3>
                <div class="director-details">
                    <strong>Patricia Victoria Nieto</strong>
                    <strong>Farmacéutica - Directora Técnica</strong>
                    28+ años de experiencia<br>
                    Especialista en Elaboración Magistral<br>
                    Atención personalizada desde 1996
                </div>
                <a href="#" class="btn-primary" onclick="openWhatsApp()">
                    <span>💬</span> Consultar por WhatsApp
                </a>
            </div>
        </div>
    </section>

    <footer class="footer">
        <div class="footer-content">
            <div class="footer-section">
                <h4>Farmacia Nieto</h4>
                <p>Tu camino hacia el bienestar desde 1996.</p>
                <p>Elaboración magistral personalizada con la más alta calidad.</p>
            </div>
            
            <div class="footer-section">
                <h4>Servicios</h4>
                <p>Medicina Ortomolecular</p>
                <p>Dermocosmética</p>
                <p>Homeopatía y Alopatía</p>
                <p>Fitoterapia y Florales</p>
                <p>Probióticos</p>
                <p>Hormonas Bioidénticas</p>
            </div>
            
            <div class="footer-section">
                <h4>Contacto</h4>
                <p>📱 (+54) 291432-7031</p>
                <p>✉️ farmacia.nieto@hotmail.com</p>
                <p>📍 Bahía Blanca, Buenos Aires</p>
                <p>⏰ Lun-Vie: 8:00-20:00 | Sáb: 8:00-13:00</p>
            </div>
            
            <div class="footer-section">
                <h4>Profesional</h4>
                <p>Directora Técnica: Patricia Victoria Nieto</p>
                <p>Matrícula Profesional</p>
                <p>28+ años de experiencia</p>
                <p>Elaboración Magistral</p>
            </div>
        </div>
        
        <div class="footer-bottom">
            <p>&copy; 2024 Farmacia Nieto. Todos los derechos reservados. | Diseñado con ❤️ para tu bienestar</p>
        </div>
    </footer>

    <a href="#" class="whatsapp-float" onclick="openWhatsApp()" aria-label="Contactar por WhatsApp">💬</a>

    <script>
        function openWhatsApp() {
            const message = "Hola, me gustaría obtener información sobre sus servicios farmacéuticos. ¡Gracias!";
            const whatsappURL = `https://wa.me/5492914327031?text=${encodeURIComponent(message)}`;
            window.open(whatsappURL, '_blank');
        }

        // Navegación suave
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ 
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Header scroll effect
        window.addEventListener('scroll', function() {
            const header = document.querySelector('.header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(255, 255, 255, 0.98)';
                header.style.boxShadow = '0 5px 20px rgba(0,0,0,0.1)';
            } else {
                header.style.background = 'rgba(255, 255, 255, 0.95)';
                header.style.boxShadow = '0 2px 10px rgba(0,0,0,0.1)';
            }
        });

        // Animación de contadores al hacer scroll
        function animateCounters() {
            const counters = document.querySelectorAll('.stat-number');
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        const counter = entry.target;
                        const target = parseInt(counter.textContent.replace(/\D/g, ''));
                        const increment = target / 50;
                        let current = 0;
                        
                        const timer = setInterval(() => {
                            current += increment;
                            if (current >= target) {
                                current = target;
                                clearInterval(timer);
                            }
                            const suffix = counter.textContent.includes('+') ? '+' : '';
                            counter.textContent = Math.floor(current) + suffix;
                        }, 40);
                        
                        observer.unobserve(counter);
                    }
                });
            }, { threshold: 0.5 });

            counters.forEach(counter => observer.observe(counter));
        }

        // Animación de tarjetas de servicios
        function animateServiceCards() {
            const cards = document.querySelectorAll('.service-card');
            const observer = new IntersectionObserver((entries) => {
                entries.forEach((entry, index) => {
                    if (entry.isIntersecting) {
                        setTimeout(() => {
                            entry.target.style.opacity = '1';
                            entry.target.style.transform = 'translateY(0)';
                        }, index * 100);
                        observer.unobserve(entry.target);
                    }
                });
            }, { threshold: 0.2 });

            cards.forEach(card => {
                card.style.opacity = '0';
                card.style.transform = 'translateY(30px)';
                card.style.transition = 'all 0.6s ease';
                observer.observe(card);
            });
        }

        // Inicializar animaciones cuando carga la página
        document.addEventListener('DOMContentLoaded', function() {
            animateCounters();
            animateServiceCards();
            
            console.log('🏥 Farmacia Nieto - Sitio web cargado correctamente');
            console.log('📱 WhatsApp: +54 291432-7031');
            console.log('✉️ Email: farmacia.nieto@hotmail.com');
        });

        // Mejorar accesibilidad del teclado
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Enter' || e.key === ' ') {
                if (e.target.classList.contains('contact-item')) {
                    e.target.click();
                }
            }
        });

        // Lazy loading para mejorar rendimiento
        if ('IntersectionObserver' in window) {
            const lazyImages = document.querySelectorAll('img[data-src]');
            const imageObserver = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        const img = entry.target;
                        img.src = img.dataset.src;
                        img.classList.remove('lazy');
                        imageObserver.unobserve(img);
                    }
                });
            });

            lazyImages.forEach(img => imageObserver.observe(img));
        }
    </script>
</body>
</html>
