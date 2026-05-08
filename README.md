# Portif-lio-pessoal
Esse portifólio tem como objetivo mostrar o que foi aprendido durante o boot camp.

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Portfólio Profissional</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
        }

        /* ===== HEADER ===== */
        header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #fff;
            padding: 3rem 1rem;
            text-align: center;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) translateX(0px); }
            50% { transform: translateY(-20px) translateX(20px); }
        }

        header h1 {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            position: relative;
            z-index: 1;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
        }

        header p {
            font-size: 1.1rem;
            position: relative;
            z-index: 1;
            opacity: 0.95;
        }

        /* ===== NAVBAR ===== */
        nav {
            background: rgba(255, 255, 255, 0.95);
            padding: 1rem;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(10px);
        }

        nav a {
            color: #667eea;
            margin: 0 20px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1rem;
            transition: all 0.3s ease;
            position: relative;
            padding-bottom: 5px;
        }

        nav a:hover {
            color: #764ba2;
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(90deg, #667eea, #764ba2);
            transition: width 0.3s ease;
        }

        nav a:hover::after {
            width: 100%;
        }

        /* ===== CONTAINER ===== */
        .container {
            width: 90%;
            max-width: 1000px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        /* ===== SECTIONS ===== */
        section {
            background: #fff;
            padding: 2.5rem;
            margin-bottom: 2rem;
            border-radius: 15px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.08);
            animation: slideUp 0.6s ease-out;
            border-left: 5px solid #667eea;
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        h2 {
            color: #667eea;
            font-size: 2rem;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        h2::before {
            content: '';
            display: inline-block;
            width: 5px;
            height: 30px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            border-radius: 3px;
        }

        /* ===== SKILLS SECTION ===== */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            margin-top: 1.5rem;
        }

        .skill-badge {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #fff;
            padding: 1rem;
            border-radius: 10px;
            text-align: center;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.2);
        }

        .skill-badge:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(102, 126, 234, 0.4);
        }

        /* ===== PROJECT CARDS ===== */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 1.5rem;
        }

        .project-card {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            border: none;
            padding: 25px;
            border-radius: 12px;
            transition: all 0.3s ease;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            transition: left 0.5s ease;
        }

        .project-card:hover::before {
            left: 100%;
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 12px 30px rgba(102, 126, 234, 0.3);
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #fff;
        }

        .project-card h3 {
            font-size: 1.4rem;
            margin-bottom: 1rem;
            color: inherit;
        }

        .project-card p {
            font-size: 0.95rem;
            line-height: 1.7;
            color: inherit;
        }

        /* ===== CONTACT SECTION ===== */
        .contact-links {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 1.5rem;
            justify-content: flex-start;
        }

        .contact-link {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 12px 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #fff;
            text-decoration: none;
            border-radius: 25px;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.2);
        }

        .contact-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(102, 126, 234, 0.4);
        }

        /* ===== FOOTER ===== */
        footer {
            text-align: center;
            padding: 2rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #fff;
            margin-top: 3rem;
            box-shadow: 0 -4px 15px rgba(0, 0, 0, 0.1);
        }

        footer p {
            font-size: 0.95rem;
            opacity: 0.9;
        }

        /* ===== RESPONSIVIDADE ===== */
        @media (max-width: 768px) {
            header h1 {
                font-size: 1.8rem;
            }

            header p {
                font-size: 0.95rem;
            }

            nav {
                padding: 0.8rem;
            }

            nav a {
                margin: 0 10px;
                font-size: 0.9rem;
            }

            h2 {
                font-size: 1.5rem;
            }

            section {
                padding: 1.5rem;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .skills-container {
                grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            }

            .container {
                width: 95%;
                padding: 20px 15px;
            }
        }

        @media (max-width: 480px) {
            header h1 {
                font-size: 1.4rem;
            }

            nav a {
                margin: 0 8px;
                font-size: 0.8rem;
            }

            h2 {
                font-size: 1.2rem;
            }

            section {
                padding: 1.2rem;
                border-left: 3px solid #667eea;
            }

            .contact-links {
                flex-direction: column;
                justify-content: center;
            }

            .contact-link {
                width: 100%;
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>🚀 Meu Portfólio Profissional</h1>
        <p>Desenvolvedor em Formação | Criando Soluções Inovadoras</p>
    </header>

    <nav>
        <a href="#sobre">Sobre Mim</a>
        <a href="#skills">Habilidades</a>
        <a href="#projetos">Projetos</a>
        <a href="#contato">Contato</a>
    </nav>

    <div class="container">
        <section id="sobre">
            <h2>📍 Sobre Mim</h2>
            <p>Olá! Sou um desenvolvedor em formação apaixonado por tecnologia e inovação. Durante meu percurso no boot camp, adquiri conhecimentos sólidos em desenvolvimento web, programação de software e práticas modernas de código. Meu objetivo é criar soluções eficientes e escaláveis que façam diferença.</p>
            <p style="margin-top: 1rem;">Sou dedicado ao aprendizado contínuo e tenho grande entusiasmo em colaborar em projetos desafiadores que contribuam para meu crescimento profissional.</p>
        </section>

        <section id="skills">
            <h2>⚡ Habilidades Técnicas</h2>
            <div class="skills-container">
                <div class="skill-badge">HTML5</div>
                <div class="skill-badge">CSS3</div>
                <div class="skill-badge">JavaScript</div>
                <div class="skill-badge">React</div>
                <div class="skill-badge">Git/GitHub</div>
                <div class="skill-badge">Responsive Design</div>
                <div class="skill-badge">APIs REST</div>
                <div class="skill-badge">Node.js</div>
            </div>
        </section>

        <section id="projetos">
            <h2>💼 Meus Projetos</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h3>🎓 Projeto Acadêmico 1</h3>
                    <p>Desenvolvimento de uma aplicação web responsiva utilizando HTML5, CSS3 e JavaScript. Projeto realizado como parte da formação no boot camp, aplicando conceitos de design moderno e UX.</p>
                </div>
                <div class="project-card">
                    <h3>💡 Projeto Pessoal 1</h3>
                    <p>Criação de uma ferramenta de produtividade utilizando React e APIs REST. Desenvolvido para praticar novas tecnologias e aprimorar habilidades em desenvolvimento frontend.</p>
                </div>
                <div class="project-card">
                    <h3>🔧 Projeto Acadêmico 2</h3>
                    <p>Sistema de gerenciamento com Node.js e banco de dados. Projeto com foco em backend, implementando autenticação, validação de dados e boas práticas de segurança.</p>
                </div>
            </div>
        </section>

        <section id="contato">
            <h2>📞 Contato</h2>
            <p>Conecte-se comigo através das minhas redes profissionais e vamos conversar sobre oportunidades de colaboração!</p>
            <div class="contact-links">
                <a href="https://linkedin.com/in/seu-perfil" target="_blank" class="contact-link">💼 LinkedIn</a>
                <a href="https://github.com/victorocean00" target="_blank" class="contact-link">🐙 GitHub</a>
                <a href="mailto:seu-email@example.com" class="contact-link">✉️ Email</a>
            </div>
        </section>
    </div>

    <footer>
        <p>&copy; 2026 - Victor Ocean. Desenvolvido com 💜 para o Desafio PortfolioHUB.</p>
    </footer>
</body>
</html>
