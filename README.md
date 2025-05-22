<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Estradas Melhores - Pinhão/PR</title>
    <style>
        /* CSS Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        /* Variáveis de cor */
        :root {
            --primary: #1a472a; /* Verde mais escuro para representar o Paraná */
            --secondary: #27ae60; /* Verde claro */
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
        }

        /* Estilos gerais */
        body {
            line-height: 1.6;
            color: #333;
            background-color: var(--light);
        }

        header {
            background-color: var(--primary);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: white;
            text-decoration: none;
        }

        .logo span {
            color: var(--secondary);
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--secondary);
        }

        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1583854470000-8e7ef1a9d8b8?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 80vh;
            display: flex;
            align-items: center;
            text-align: center;
            color: white;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }

        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 5px;
            text-decoration: none;
            transition: background-color 0.3s;
            font-weight: bold;
        }

        .btn:hover {
            background-color: #219653;
        }

        .btn-accent {
            background-color: var(--accent);
        }

        .btn-accent:hover {
            background-color: #c0392b;
        }

        section {
            padding: 5rem 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            font-size: 2.5rem;
            color: var(--dark);
        }

        .benefits {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .benefit-card {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }

        .benefit-card:hover {
            transform: translateY(-10px);
        }

        .benefit-card h3 {
            color: var(--secondary);
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        .benefit-icon {
            font-size: 3rem;
            color: var(--secondary);
            margin-bottom: 1.5rem;
        }

        .projects {
            background-color: var(--primary);
            color: white;
        }

        .projects .section-title {
            color: white;
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background-color: white;
            color: var(--dark);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .project-img {
            height: 200px;
            overflow: hidden;
        }

        .project-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .project-card:hover .project-img img {
            transform: scale(1.1);
        }

        .project-info {
            padding: 1.5rem;
        }

        .project-info h3 {
            margin-bottom: 0.5rem;
            color: var(--secondary);
        }

        .stats {
            background-color: var(--secondary);
            color: white;
            text-align: center;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
        }

        .stat-item h3 {
            font-size: 3rem;
            margin-bottom: 0.5rem;
        }

        .contact {
            background-color: white;
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background-color: var(--light);
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: bold;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }

        .form-group textarea {
            min-height: 150px;
        }

        footer {
            background-color: var(--dark);
            color: white;
            padding: 3rem 0;
            text-align: center;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            list-style: none;
            margin: 1.5rem 0;
        }

        .footer-links li {
            margin: 0 1rem;
        }

        .footer-links a {
            color: white;
            text-decoration: none;
        }

        .footer-links a:hover {
            color: var(--secondary);
        }

        .social-icons {
            margin: 1.5rem 0;
        }

        .social-icons a {
            color: white;
            font-size: 1.5rem;
            margin: 0 0.5rem;
            transition: color 0.3s;
        }

        .social-icons a:hover {
            color: var(--secondary);
        }

        .local-info {
            text-align: center;
            margin-bottom: 3rem;
        }

        .local-info img {
            max-width: 150px;
            margin-bottom: 1rem;
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero h1 {
                font-size: 2.2rem;
            }

            .hero p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <nav>
                <a href="#" class="logo">Pinhão<span>Estradas</span></a>
                <ul class="nav-links">
                    <li><a href="#inicio">Início</a></li>
                    <li><a href="#beneficios">Benefícios</a></li>
                    <li><a href="#projetos">Projetos</a></li>
                    <li><a href="#contato">Contato</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero" id="inicio">
        <div class="hero-content">
            <h1>Melhorando as Estradas de Pinhão/PR</h1>
            <p>Investimentos em infraestrutura viária para impulsionar o desenvolvimento de nossa região.</p>
            <a href="#projetos" class="btn">Nossos Projetos</a>
            <a href="#contato" class="btn btn-accent">Fale Conosco</a>
        </div>
    </section>

    <section id="beneficios">
        <div class="container">
            <div class="local-info">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/93/Bandeira_do_munic%C3%ADpio_de_Pinh%C3%A3o_%28PR%29.svg/1200px-Bandeira_do_munic%C3%ADpio_de_Pinh%C3%A3o_%28PR%29.svg.png" alt="Bandeira de Pinhão/PR" style="max-width: 150px;">
                <h2>Pinhão - Capital da Erva-Mate</h2>
                <p>Município paranaense com forte vocação agrícola e necessidade de infraestrutura viária de qualidade.</p>
            </div>
            
            <h2 class="section-title">Benefícios para Pinhão</h2>
            <div class="benefits">
                <div class="benefit-card">
                    <div class="benefit-icon">🚜</div>
                    <h3>Escoamento Agrícola</h3>
                    <p>Melhorias nas estradas rurais para facilitar o transporte da produção agrícola, especialmente da erva-mate.</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">🏘️</div>
                    <h3>Desenvolvimento Urbano</h3>
                    <p>Pavimentação de vias urbanas e construção de calçadas para melhorar a mobilidade dos cidadãos.</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">🚌</div>
                    <h3>Transporte Coletivo</h3>
                    <p>Melhoria nas condições das estradas para o transporte escolar e coletivo na região.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="projects" id="projetos">
        <div class="container">
            <h2 class="section-title">Projetos em Andamento</h2>
            <div class="project-grid">
                <div class="project-card">
                    <div class="project-img">
                        <img src="https://images.unsplash.com/photo-1513828583688-c52646db42da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Estrada Rural">
                    </div>
                    <div class="project-info">
                        <h3>Pavimentação PR-488</h3>
                        <p>Asfaltamento de 15km da PR-488, ligando Pinhão aos distritos rurais e facilitando o escoamento agrícola.</p>
                        <a href="#" class="btn">Saiba Mais</a>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-img">
                        <img src="https://images.unsplash.com/photo-1477959858617-67f85cf4f1df?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Estrada Urbana">
                    </div>
                    <div class="project-info">
                        <h3>Recapeamento Urbano</h3>
                        <p>Recuperação de 8km de vias urbanas no centro de Pinhão, com drenagem adequada e sinalização moderna.</p>
                        <a href="#" class="btn">Saiba Mais</a>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-img">
                        <img src="https://images.unsplash.com/photo-1493238792000-8113da705763?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Ponte">
                    </div>
                    <div class="project-info">
                        <h3>Reconstrução de Pontes</h3>
                        <p>Substituição de 3 pontes em estradas rurais que apresentavam risco à população.</p>
                        <a href="#" class="btn">Saiba Mais</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="stats">
        <div class="container">
            <div class="stats-grid">
                <div class="stat-item">
                    <h3>42km</h3>
                    <p>De estradas recuperadas</p>
                </div>
                <div class="stat-item">
                    <h3>3</h3>
                    <p>Pontes reconstruídas</p>
                </div>
                <div class="stat-item">
                    <h3>12</h3>
                    <p>Comunidades beneficiadas</p>
                </div>
                <div class="stat-item">
                    <h3>85%</h3>
                    <p>Redução de reclamações</p>
                </div>
            </div>
        </div>
    </section>

    <section class="contact" id="contato">
        <div class="container">
            <h2 class="section-title">Secretaria de Obras de Pinhão</h2>
            <div class="contact-form">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="name">Nome</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="subject">Assunto</label>
                        <input type="text" id="subject" name="subject" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Mensagem</label>
                        <textarea id="message" name="message" required></textarea>
                    </div>
                    <button type="submit" class="btn">Enviar Mensagem</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <a href="#" class="logo">Pinhão<span>Estradas</span></a>
            <ul class="footer-links">
                <li><a href="#inicio">Início</a></li>
                <li><a href="#beneficios">Benefícios</a></li>
                <li><a href="#projetos">Projetos</a></li>
                <li><a href="#contato">Contato</a></li>
                <li><a href="#">Prefeitura Municipal</a></li>
            </ul>
            <div class="social-icons">
                <a href="#"><span>📱</span></a>
                <a href="#"><span>📘</span></a>
                <a href="#"><span>📸</span></a>
            </div>
            <p>Secretaria Municipal de Obras e Infraestrutura</p>
            <p>Pinhão - Paraná</p>
            <p>&copy; 2023 Todos os direitos reservados</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form values
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const subject = document.getElementById('subject').value;
            const message = document.getElementById('message').value;
            
            // Here you would typically send the data to a server
            console.log('Form submitted:', { name, email, subject, message });
            
            // Show success message
            alert('Obrigado por sua mensagem, ' + name + '! A Secretaria de Obras entrará em contato em breve.');
            
            // Reset form
            this.reset();
        });

        // Animation on scroll
        window.addEventListener('scroll', function() {
            const cards = document.querySelectorAll('.benefit-card, .project-card');
            const windowHeight = window.innerHeight;
            
            cards.forEach(card => {
                const cardPosition = card.getBoundingClientRect().top;
                if (cardPosition < windowHeight - 100) {
                    card.style.opacity = '1';
                    card.style.transform = 'translateY(0)';
                }
            });
        });

        // Initialize animations
        document.addEventListener('DOMContentLoaded', function() {
            const cards = document.querySelectorAll('.benefit-card, .project-card');
            cards.forEach(card => {
                card.style.opacity = '0';
                card.style.transform = 'translateY(20px)';
                card.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
            });
        });
    </script>
</body>
</html><!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Estradas Melhores - Pinhão/PR</title>
    <style>
        /* CSS Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        /* Variáveis de cor */
        :root {
            --primary: #1a472a; /* Verde mais escuro para representar o Paraná */
            --secondary: #27ae60; /* Verde claro */
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
        }

        /* Estilos gerais */
        body {
            line-height: 1.6;
            color: #333;
            background-color: var(--light);
        }

        header {
            background-color: var(--primary);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: white;
            text-decoration: none;
        }

        .logo span {
            color: var(--secondary);
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--secondary);
        }

        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1583854470000-8e7ef1a9d8b8?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 80vh;
            display: flex;
            align-items: center;
            text-align: center;
            color: white;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }

        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 5px;
            text-decoration: none;
            transition: background-color 0.3s;
            font-weight: bold;
        }

        .btn:hover {
            background-color: #219653;
        }

        .btn-accent {
            background-color: var(--accent);
        }

        .btn-accent:hover {
            background-color: #c0392b;
        }

        section {
            padding: 5rem 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            font-size: 2.5rem;
            color: var(--dark);
        }

        .benefits {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .benefit-card {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }

        .benefit-card:hover {
            transform: translateY(-10px);
        }

        .benefit-card h3 {
            color: var(--secondary);
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        .benefit-icon {
            font-size: 3rem;
            color: var(--secondary);
            margin-bottom: 1.5rem;
        }

        .projects {
            background-color: var(--primary);
            color: white;
        }

        .projects .section-title {
            color: white;
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background-color: white;
            color: var(--dark);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .project-img {
            height: 200px;
            overflow: hidden;
        }

        .project-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .project-card:hover .project-img img {
            transform: scale(1.1);
        }

        .project-info {
            padding: 1.5rem;
        }

        .project-info h3 {
            margin-bottom: 0.5rem;
            color: var(--secondary);
        }

        .stats {
            background-color: var(--secondary);
            color: white;
            text-align: center;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
        }

        .stat-item h3 {
            font-size: 3rem;
            margin-bottom: 0.5rem;
        }

        .contact {
            background-color: white;
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background-color: var(--light);
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: bold;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }

        .form-group textarea {
            min-height: 150px;
        }

        footer {
            background-color: var(--dark);
            color: white;
            padding: 3rem 0;
            text-align: center;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            list-style: none;
            margin: 1.5rem 0;
        }

        .footer-links li {
            margin: 0 1rem;
        }

        .footer-links a {
            color: white;
            text-decoration: none;
        }

        .footer-links a:hover {
            color: var(--secondary);
        }

        .social-icons {
            margin: 1.5rem 0;
        }

        .social-icons a {
            color: white;
            font-size: 1.5rem;
            margin: 0 0.5rem;
            transition: color 0.3s;
        }

        .social-icons a:hover {
            color: var(--secondary);
        }

        .local-info {
            text-align: center;
            margin-bottom: 3rem;
        }

        .local-info img {
            max-width: 150px;
            margin-bottom: 1rem;
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero h1 {
                font-size: 2.2rem;
            }

            .hero p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <nav>
                <a href="#" class="logo">Pinhão<span>Estradas</span></a>
                <ul class="nav-links">
                    <li><a href="#inicio">Início</a></li>
                    <li><a href="#beneficios">Benefícios</a></li>
                    <li><a href="#projetos">Projetos</a></li>
                    <li><a href="#contato">Contato</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero" id="inicio">
        <div class="hero-content">
            <h1>Melhorando as Estradas de Pinhão/PR</h1>
            <p>Investimentos em infraestrutura viária para impulsionar o desenvolvimento de nossa região.</p>
            <a href="#projetos" class="btn">Nossos Projetos</a>
            <a href="#contato" class="btn btn-accent">Fale Conosco</a>
        </div>
    </section>

    <section id="beneficios">
        <div class="container">
            <div class="local-info">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/93/Bandeira_do_munic%C3%ADpio_de_Pinh%C3%A3o_%28PR%29.svg/1200px-Bandeira_do_munic%C3%ADpio_de_Pinh%C3%A3o_%28PR%29.svg.png" alt="Bandeira de Pinhão/PR" style="max-width: 150px;">
                <h2>Pinhão - Capital da Erva-Mate</h2>
                <p>Município paranaense com forte vocação agrícola e necessidade de infraestrutura viária de qualidade.</p>
            </div>
            
            <h2 class="section-title">Benefícios para Pinhão</h2>
            <div class="benefits">
                <div class="benefit-card">
                    <div class="benefit-icon">🚜</div>
                    <h3>Escoamento Agrícola</h3>
                    <p>Melhorias nas estradas rurais para facilitar o transporte da produção agrícola, especialmente da erva-mate.</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">🏘️</div>
                    <h3>Desenvolvimento Urbano</h3>
                    <p>Pavimentação de vias urbanas e construção de calçadas para melhorar a mobilidade dos cidadãos.</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">🚌</div>
                    <h3>Transporte Coletivo</h3>
                    <p>Melhoria nas condições das estradas para o transporte escolar e coletivo na região.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="projects" id="projetos">
        <div class="container">
            <h2 class="section-title">Projetos em Andamento</h2>
            <div class="project-grid">
                <div class="project-card">
                    <div class="project-img">
                        <img src="https://images.unsplash.com/photo-1513828583688-c52646db42da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Estrada Rural">
                    </div>
                    <div class="project-info">
                        <h3>Pavimentação PR-488</h3>
                        <p>Asfaltamento de 15km da PR-488, ligando Pinhão aos distritos rurais e facilitando o escoamento agrícola.</p>
                        <a href="#" class="btn">Saiba Mais</a>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-img">
                        <img src="https://images.unsplash.com/photo-1477959858617-67f85cf4f1df?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Estrada Urbana">
                    </div>
                    <div class="project-info">
                        <h3>Recapeamento Urbano</h3>
                        <p>Recuperação de 8km de vias urbanas no centro de Pinhão, com drenagem adequada e sinalização moderna.</p>
                        <a href="#" class="btn">Saiba Mais</a>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-img">
                        <img src="https://images.unsplash.com/photo-1493238792000-8113da705763?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Ponte">
                    </div>
                    <div class="project-info">
                        <h3>Reconstrução de Pontes</h3>
                        <p>Substituição de 3 pontes em estradas rurais que apresentavam risco à população.</p>
                        <a href="#" class="btn">Saiba Mais</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="stats">
        <div class="container">
            <div class="stats-grid">
                <div class="stat-item">
                    <h3>42km</h3>
                    <p>De estradas recuperadas</p>
                </div>
                <div class="stat-item">
                    <h3>3</h3>
                    <p>Pontes reconstruídas</p>
                </div>
                <div class="stat-item">
                    <h3>12</h3>
                    <p>Comunidades beneficiadas</p>
                </div>
                <div class="stat-item">
                    <h3>85%</h3>
                    <p>Redução de reclamações</p>
                </div>
            </div>
        </div>
    </section>

    <section class="contact" id="contato">
        <div class="container">
            <h2 class="section-title">Secretaria de Obras de Pinhão</h2>
            <div class="contact-form">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="name">Nome</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="subject">Assunto</label>
                        <input type="text" id="subject" name="subject" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Mensagem</label>
                        <textarea id="message" name="message" required></textarea>
                    </div>
                    <button type="submit" class="btn">Enviar Mensagem</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <a href="#" class="logo">Pinhão<span>Estradas</span></a>
            <ul class="footer-links">
                <li><a href="#inicio">Início</a></li>
                <li><a href="#beneficios">Benefícios</a></li>
                <li><a href="#projetos">Projetos</a></li>
                <li><a href="#contato">Contato</a></li>
                <li><a href="#">Prefeitura Municipal</a></li>
            </ul>
            <div class="social-icons">
                <a href="#"><span>📱</span></a>
                <a href="#"><span>📘</span></a>
                <a href="#"><span>📸</span></a>
            </div>
            <p>Secretaria Municipal de Obras e Infraestrutura</p>
            <p>Pinhão - Paraná</p>
            <p>&copy; 2023 Todos os direitos reservados</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form values
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const subject = document.getElementById('subject').value;
            const message = document.getElementById('message').value;
            
            // Here you would typically send the data to a server
            console.log('Form submitted:', { name, email, subject, message });
            
            // Show success message
            alert('Obrigado por sua mensagem, ' + name + '! A Secretaria de Obras entrará em contato em breve.');
            
            // Reset form
            this.reset();
        });

        // Animation on scroll
        window.addEventListener('scroll', function() {
            const cards = document.querySelectorAll('.benefit-card, .project-card');
            const windowHeight = window.innerHeight;
            
            cards.forEach(card => {
                const cardPosition = card.getBoundingClientRect().top;
                if (cardPosition < windowHeight - 100) {
                    card.style.opacity = '1';
                    card.style.transform = 'translateY(0)';
                }
            });
        });

        // Initialize animations
        document.addEventListener('DOMContentLoaded', function() {
            const cards = document.querySelectorAll('.benefit-card, .project-card');
            cards.forEach(card => {
                card.style.opacity = '0';
                card.style.transform = 'translateY(20px)';
                card.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
            });
        });
    </script>
</body>
</html>

