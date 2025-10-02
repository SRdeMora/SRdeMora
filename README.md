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
