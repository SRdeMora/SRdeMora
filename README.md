<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Perfil de GitHub de Samuel Rodríguez de Mora</title>
    <!-- Importación de fuentes y iconos -->
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&family=Roboto+Mono:wght@400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.15.1/devicon.min.css">

    <style>
        /* --- ESTILOS GENERALES Y VARIABLES DE COLOR --- */
        :root {
            --primary-color: #007bff;      /* Azul principal para enlaces y acentos */
            --secondary-color: #adb5bd;    /* Gris claro para texto secundario y fechas */
            --background-color: #121212;  /* Fondo oscuro profundo */
            --card-background: #1e1e1e;   /* Fondo de tarjetas ligeramente más claro */
            --text-color: #e0e0e0;        /* Color de texto principal */
            --heading-color: #ffffff;     /* Encabezados en blanco puro */
            --border-color: #333333;      /* Borde sutil */
            --accent-color: #00bcd4;      /* Cian para detalles y subtítulos */
            --link-hover-color: #0056b3;  /* Azul más oscuro para hover */
        }

        body {
            font-family: 'Montserrat', sans-serif;
            background-color: var(--background-color);
            color: var(--text-color);
            line-height: 1.7;
            margin: 0;
            padding: 20px;
        }

        .container {
            width: 100%;
            max-width: 1000px;
            margin: auto;
            display: grid;
            grid-template-columns: 1fr;
            gap: 25px;
        }

        @media (min-width: 800px) {
            .container {
                grid-template-columns: 300px 1fr; /* Sidebar fija y contenido principal flexible */
            }
        }

        /* --- ESTILOS DE LA BARRA LATERAL (SIDEBAR) --- */
        .sidebar, .main-content-section {
            background-color: var(--card-background);
            border-radius: 12px;
            padding: 30px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.4);
            border: 1px solid var(--border-color);
        }

        .sidebar {
            text-align: center;
        }

        .profile-pic {
            width: 160px;
            height: 160px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid var(--primary-color);
            margin-bottom: 20px;
            box-shadow: 0 0 20px rgba(0, 123, 255, 0.6);
        }
        
        h1 {
            color: var(--heading-color);
            font-size: 2em;
            margin: 0;
        }

        .subtitle {
            font-family: 'Roboto Mono', monospace;
            color: var(--accent-color);
            font-size: 0.9em;
            margin-top: 5px;
            margin-bottom: 20px;
            font-weight: 600;
        }

        .bio {
            font-size: 0.95em;
            margin-bottom: 25px;
            color: var(--secondary-color);
        }

        .contact-info a {
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text-color);
            text-decoration: none;
            margin-bottom: 12px;
            font-weight: 600;
            transition: color 0.3s ease;
        }

        .contact-info a:hover {
            color: var(--primary-color);
        }

        .contact-info i {
            margin-right: 10px;
            color: var(--primary-color);
            width: 20px;
            text-align: center;
        }

        /* --- ESTILOS DEL CONTENIDO PRINCIPAL --- */
        h2 {
            font-size: 1.8em;
            color: var(--heading-color);
            border-bottom: 3px solid var(--border-color);
            padding-bottom: 12px;
            margin-bottom: 25px;
        }

        h3 {
            font-size: 1.3em;
            color: var(--accent-color);
            margin-bottom: 10px;
        }

        /* Sección de Habilidades Técnicas */
        .skills-category {
            margin-bottom: 20px;
        }

        .skills-category h4 {
            color: var(--heading-color);
            font-weight: 600;
            margin-bottom: 15px;
        }

        .skills-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
        }

        .skill-item {
            display: flex;
            align-items: center;
            background-color: var(--background-color);
            padding: 8px 15px;
            border-radius: 8px;
            font-size: 0.9em;
            font-weight: 600;
            color: var(--text-color);
            border: 1px solid var(--border-color);
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }

        .skill-item:hover {
            transform: translateY(-4px);
            box-shadow: 0 6px 15px rgba(0, 188, 212, 0.2);
            border-color: var(--accent-color);
        }
        
        .skill-item i {
            font-size: 1.5em;
            margin-right: 10px;
            color: var(--accent-color);
        }

        /* Secciones de Experiencia y Educación */
        .timeline-item {
            margin-bottom: 30px;
            padding-left: 25px;
            position: relative;
            border-left: 2px solid var(--border-color);
        }
        
        .timeline-item::before {
            content: '';
            position: absolute;
            left: -9px; /* Centra el círculo en la línea */
            top: 5px;
            width: 16px;
            height: 16px;
            background-color: var(--primary-color);
            border-radius: 50%;
            border: 3px solid var(--card-background);
        }

        .timeline-item h3 {
            margin-bottom: 2px;
        }

        .item-subtitle, .item-date {
            color: var(--secondary-color);
            font-size: 0.95em;
            margin-bottom: 8px;
        }

        .timeline-item ul {
            list-style: none;
            padding-left: 0;
            margin-top: 10px;
        }

        .timeline-item ul li {
            position: relative;
            padding-left: 20px;
            margin-bottom: 8px;
        }

        .timeline-item ul li::before {
            content: '›';
            color: var(--accent-color);
            position: absolute;
            left: 0;
            font-size: 1.4em;
            line-height: 1;
        }

        /* Sección de Estadísticas de GitHub */
        .github-stats {
            text-align: center;
        }
        
        .github-stats img {
            max-width: 100%;
            margin: 10px 0;
            border-radius: 8px;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- ===== BARRA LATERAL (SIDEBAR) ===== -->
        <aside class="sidebar">
            <img src="https://avatars.githubusercontent.com/u/74648784?v=4" alt="Foto de Perfil de Samuel Rodríguez de Mora" class="profile-pic">
            <h1>SAMUEL RODRÍGUEZ DE MORA</h1>
            <p class="subtitle">ESPECIALISTA EN PROCESAMIENTO DEL LENGUAJE NATURAL</p>
            <p class="bio">
                Lingüista Computacional con base en Filología Hispánica, experto en PLN, Machine Learning y modelos Transformer (BERT, GPT). Mi experiencia abarca la ingeniería de prompts, el desarrollo de agentes conversacionales y la creación de automatizaciones con herramientas no-code.
            </p>

            <div class="contact-info">
                <a href="mailto:devai.srm@gmail.com"><i class="fas fa-envelope"></i> devai.srm@gmail.com</a>
                <a href="URL_DE_TU_LINKEDIN" target="_blank" rel="noopener noreferrer"><i class="fab fa-linkedin"></i> LinkedIn</a>
                <a href="URL_DE_TU_PORTFOLIO" target="_blank" rel="noopener noreferrer"><i class="fas fa-globe"></i> Portfolio</a>
                <a href="#"><i class="fas fa-map-marker-alt"></i> Madrid, España</a>
            </div>
        </aside>

        <!-- ===== CONTENIDO PRINCIPAL ===== -->
        <main class="main-content">
            <!-- Sección de Habilidades Técnicas -->
            <section class="main-content-section">
                <h2>Habilidades Técnicas</h2>
                <div class="skills-category">
                    <h4><i class="fas fa-brain"></i> Áreas de PLN / Machine Learning</h4>
                    <div class="skills-grid">
                        <span class="skill-item">Análisis de Sentimiento</span>
                        <span class="skill-item">NER</span>
                        <span class="skill-item">Topic Modeling (LDA)</span>
                        <span class="skill-item">Word Embeddings</span>
                        <span class="skill-item">Modelos Transformer</span>
                        <span class="skill-item">Chatbots y Asistentes</span>
                        <span class="skill-item">Web Scraping</span>
                    </div>
                </div>
                <div class="skills-category">
                    <h4><i class="fas fa-code"></i> Bibliotecas y Frameworks</h4>
                    <div class="skills-grid">
                        <span class="skill-item"><i class="devicon-python-plain"></i> Python</span>
                        <span class="skill-item"><i class="devicon-tensorflow-original"></i> TensorFlow</span>
                        <span class="skill-item"><i class="devicon-keras-plain"></i> Keras</span>
                        <span class="skill-item">🤗 Hugging Face</span>
                        <span class="skill-item">spaCy</span>
                        <span class="skill-item">NLTK</span>
                        <span class="skill-item">Scikit-learn</span>
                        <span class="skill-item">Gensim</span>
                    </div>
                </div>
                <div class="skills-category">
                    <h4><i class="fas fa-tools"></i> Herramientas y Tecnologías</h4>
                    <div class="skills-grid">
                        <span class="skill-item"><i class="devicon-jupyter-plain-wordmark"></i> Jupyter</span>
                        <span class="skill-item"><i class="devicon-git-plain"></i> Git & GitHub</span>
                        <span class="skill-item"><i class="devicon-sqldeveloper-plain"></i> SQL (básico)</span>
                        <span class="skill-item"><i class="fas fa-network-wired"></i> APIs REST</span>
                        <span class="skill-item"><i class="fas fa-cogs"></i> n8n</span>
                    </div>
                </div>
            </section>
            
            <!-- Sección de Experiencia Laboral -->
            <section class="main-content-section">
                <h2>Experiencia Laboral</h2>
                <div class="timeline-item">
                    <h3>Gerente A</h3>
                    <p class="item-subtitle">Mercadona S.A</p>
                    <p class="item-date">2010 - 2024</p>
                    <ul>
                        <li><b>Análisis de Datos y Experiencia Cliente:</b> Utilicé KPIs para la toma de decisiones estratégicas y lideré la resolución de incidencias críticas mediante el análisis de su causa raíz.</li>
                        <li><b>Optimización Logística y de Rutas:</b> Diseñé y optimicé las rutas de reparto, modelando trayectos eficientes con análisis de datos en Excel para maximizar la productividad.</li>
                        <li><b>Gestión de Proyectos:</b> Lideré la implementación de nuevas iniciativas comerciales y operativas, coordinando recursos para asegurar una ejecución exitosa.</li>
                    </ul>
                </div>
                <div class="timeline-item">
                    <h3>Técnico de Mantenimiento de TPVs</h3>
                    <p class="item-subtitle">POAS Mantenimiento</p>
                    <p class="item-date">2006 - 2008</p>
                    <ul>
                        <li><b>Diagnóstico Avanzado y Recuperación:</b> Realicé diagnóstico sistemático de incidencias, especializándome en la recuperación de equipos 'irrecuperables'.</li>
                        <li><b>Formación y Mentoría Técnica:</b> Como referente técnico, formé a nuevas incorporaciones, traduciendo conceptos complejos de electrónica a procedimientos prácticos.</li>
                    </ul>
                </div>
            </section>

            <!-- Sección de Formación -->
            <section class="main-content-section">
                <h2>Formación Académica</h2>
                <div class="timeline-item">
                    <h3>Diplomado en Experto en Procesamiento del Lenguaje Natural</h3>
                    <p class="item-subtitle">Universidad a Distancia de Madrid (UDIMA)</p>
                    <p class="item-date">2024 - 2025</p>
                </div>
                <div class="timeline-item">
                    <h3>Graduado en Lengua y Literatura Españolas</h3>
                    <p class="item-subtitle">Universidad Nacional de Educación a Distancia (UNED)</p>
                    <p class="item-date">2018 - 2023</p>
                </div>
            </section>

            <!-- Sección de Estadísticas de GitHub -->
            <section class="main-content-section github-stats">
                <h2>Estadísticas de GitHub</h2>
                <img src="https://github-readme-stats.vercel.app/api?username=SRdeMora&show_icons=true&theme=transparent&bg_color=1e1e1e&title_color=007bff&text_color=e0e0e0&icon_color=00bcd4" alt="Estadísticas de GitHub de SRdeMora" />
                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=SRdeMora&layout=compact&theme=transparent&bg_color=1e1e1e&title_color=007bff&text_color=e0e0e0" alt="Lenguajes más usados por SRdeMora" />
                <img src="https://github-readme-streak-stats.herokuapp.com/?user=SRdeMora&theme=dark&background=1e1e1e&ring=007bff&fire=00bcd4&currStreakNum=e0e0e0&sideNums=e0e0e0&sideLabels=e0e0e0&currStreakLabel=e0e0e0" alt="Racha de Contribuciones de SRdeMora" />
            </section>
        </main>
    </div>
</body>
</html>
