<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Mundo de Colores Imperfectos - El Libro</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Nunito+Sans:ital,opsz,wght@0,6..12,200..1000;1,6..12,200..1000&family=Playwrite+EN+Joined:wght@100..400&display=swap" rel="stylesheet">
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        /* --- VARIABLES DE COLOR (Cálido y Análogo) --- */
        :root {
            --bg-calido: #FFF8F5;       /* Fondo suave */
            --principal: #E65F2B;       /* Naranja vibrante */
            --secundario: #F29441;      /* Amarillo cálido / Ámbar */
            --acento: #D9383A;          /* Coral rojizo */
            --texto-oscuro: #2D1A15;    /* Marrón café muy oscuro */
            --blanco: #FFFFFF;
        }

        /* --- ESTILOS GENERALES --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: "Nunito Sans", sans-serif;
            background-color: var(--bg-calido);
            color: var(--texto-oscuro);
            line-height: 1.6;
        }

        h1, h2, h3, .font-titulo {
            font-family: "Playwrite EN Joined", cursive;
            font-weight: 400;
        }

        img {
            max-width: 100%;
            height: auto;
            display: block;
            border-radius: 8px;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        /* --- HERO SECTION (Inspirada en tu maqueta) --- */
        .hero {
            display: grid;
            grid-template-columns: 1fr;
            gap: 40px;
            padding-top: 60px;
            padding-bottom: 60px;
            align-items: center;
        }

        @media (min-width: 768px) {
            .hero {
                grid-template-columns: 1.2fr 1fr;
                gap: 60px;
            }
        }

        .hero-left h1 {
            font-size: 3rem;
            color: var(--texto-oscuro);
            line-height: 1.3;
            margin-bottom: 30px;
        }

        @media (min-width: 768px) {
            .hero-left h1 {
                font-size: 4rem;
            }
        }

        .hero-imagen-wrapper {
            background: linear-gradient(135deg, var(--principal), var(--secundario));
            padding: 15px;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(230, 95, 43, 0.2);
        }

        .hero-right .descripcion {
            font-size: 1.15rem;
            margin-bottom: 35px;
            color: var(--texto-oscuro);
        }

        /* Botonera basada en los bloques negros de tu maqueta */
        .grid-botones {
            display: grid;
            grid-template-columns: 1fr;
            gap: 15px;
            margin-bottom: 40px;
        }

        @media (min-width: 480px) {
            .grid-botones {
                grid-template-columns: 1fr 1fr;
            }
        }

        .btn-interactivo {
            background-color: var(--texto-oscuro);
            color: var(--blanco);
            text-align: center;
            padding: 15px 20px;
            font-size: 1.1rem;
            font-weight: 600;
            text-decoration: none;
            border-radius: 4px;
            transition: all 0.3s ease;
            display: block;
        }

        .btn-interactivo:hover {
            background-color: var(--principal);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(230, 95, 43, 0.3);
        }

        /* --- SECCIÓN SEPARADORA (SINOPSIS) --- */
        .sinopsis-section {
            background-color: var(--principal);
            color: var(--blanco);
            padding: 60px 0;
            text-align: center;
        }

        .sinopsis-section h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .sinopsis-section p {
            max-width: 800px;
            margin: 0 auto;
            font-size: 1.2rem;
            padding: 0 20px;
        }

        /* --- SECCIONES DE CONTENIDO (PROCESO, DISEÑO, GALERÍA) --- */
        .seccion-info {
            padding: 80px 0;
        }

        .seccion-info h2 {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 50px;
            color: var(--acento);
        }

        .grid-3-columnas {
            display: grid;
            grid-template-columns: 1fr;
            gap: 30px;
        }

        @media (min-width: 768px) {
            .grid-3-columnas {
                grid-template-columns: repeat(3, 1fr);
            }
        }

        .tarjeta-proceso {
            background-color: var(--blanco);
            padding: 30px;
            border-radius: 8px;
            border-top: 5px solid var(--secundario);
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .tarjeta-proceso h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--texto-oscuro);
        }

        /* Bloque de Empaque y Diseño de dos columnas alternado */
        .empaque-diseno {
            display: grid;
            grid-template-columns: 1fr;
            gap: 40px;
            align-items: center;
            background-color: #FFEFEA;
            padding: 50px;
            border-radius: 12px;
        }

        @media (min-width: 768px) {
            .empaque-diseno {
                grid-template-columns: 1fr 1.2fr;
            }
        }

        /* Galería de fotos */
        .galeria-fotos {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .galeria-fotos img {
            transition: transform 0.3s ease;
            box-shadow: 0 4px 10px rgba(0,0,0,0.08);
        }

        .galeria-fotos img:hover {
            transform: scale(1.03);
        }

        /* --- FOOTER Y REDES SOCIALES (Inspirado en la maqueta) --- */
        footer {
            border-top: 2px solid var(--texto-oscuro);
            padding: 40px 0;
            text-align: center;
            margin-top: 40px;
        }

        footer p {
            font-weight: 700;
            letter-spacing: 1px;
            margin-bottom: 25px;
            text-transform: uppercase;
            font-size: 0.9rem;
        }

        .redes-sociales {
            display: flex;
            justify-content: center;
            gap: 35px;
            margin-bottom: 30px;
        }

        .redes-sociales a {
            color: var(--texto-oscuro);
            font-size: 1.8rem;
            transition: color 0.3s ease, transform 0.3s ease;
        }

        .redes-sociales a:hover {
            color: var(--principal);
            transform: scale(1.2);
        }

        .creditos {
            font-size: 0.85rem;
            color: #776561;
        }
    </style>
</head>
<body>

    <main class="container hero">
        
        <div class="hero-left">
            <h1>Mi mundo de colores imperfectos</h1>
            <div class="hero-imagen-wrapper">
                <img src="https://images.unsplash.com/photo-1541701494587-cb58502866ab?auto=format&fit=crop&w=800&q=80" alt="Concepto abstracto de colores">
            </div>
        </div>

        <div class="hero-right">
            <p class="descripcion">
                Este libro es un viaje introspectivo a través del arte visual y el feminismo interseccional. Exploramos las narrativas de mujeres y niñas, rompiendo moldes mediante la imperfección y transformando el caos cromático en discursos con un verdadero significado social.
            </p>

            <div class="grid-botones">
                <a href="#sinopsis" class="btn-interactivo">Sinopsis</a>
                <a href="#proceso" class="btn-interactivo">Proceso Creativo</a>
                <a href="#diseno" class="btn-interactivo">Diseño y Empaque</a>
                <a href="#galeria" class="btn-interactivo">Fotografías</a>
                <a href="#comprar" class="btn-interactivo" style="background-color: var(--acento);">Adquirir Libro</a>
                <a href="#contacto" class="btn-interactivo">Saber Más</a>
            </div>
        </div>

    </main>

    <section id="sinopsis" class="sinopsis-section">
        <div class="container">
            <h2>Sinopsis</h2>
            <p>
                "Mi mundo de colores imperfectos" desmantela la idea de la perfección impuesta. A través de páginas llenas de contrastes analógicos e historias crudas pero esperanzadoras, la autora nos sumerge en las texturas de la resiliencia y el activismo de género en el mundo contemporáneo.
            </p>
        </div>
    </section>

    <section id="proceso" class="container seccion-info">
        <h2>Proceso Creativo</h2>
        <div class="grid-3-columnas">
            <div class="tarjeta-proceso">
                <h3>01. Inspiración</h3>
                <p>Recopilación de testimonios reales y discursos sobre feminismo interseccional que encendieron la chispa del proyecto.</p>
            </div>
            <div class="tarjeta-proceso">
                <h3>02. Experimentación</h3>
                <p>Pruebas con pintura macro, texturas e imperfecciones visuales que sirvieron como metáfora para cada capítulo.</p>
            </div>
            <div class="tarjeta-proceso">
                <h3>03. Curaduría</h3>
                <p>Selección minuciosa de textos e imágenes que logran equilibrar el peso político con la belleza estética.</p>
            </div>
        </div>
    </section>

    <section id="diseno" class="container seccion-info">
        <h2>Diseño & Empaque</h2>
        <div class="empaque-diseno">
            <img src="https://images.unsplash.com/photo-1544947950-fa07a98d237f?auto=format&fit=crop&w=600&q=80" alt="Diseño editorial del libro">
            <div>
                <p style="margin-bottom: 15px; font-size: 1.1rem;">
                    Cada ejemplar ha sido diseñado pensando en la experiencia táctil. El empaque utiliza materiales ecológicos y texturizados que transmiten esa sensación de manufactura orgánica e "imperfecta".
                </p>
                <p style="font-size: 1.1rem;">
                    <strong>Detalles del diseño:</strong> Interiores impresos a cinco tintas para preservar la vibración de la paleta cálida y encuadernación expuesta que celebra la estructura del libro al desnudo.
                </p>
            </div>
        </div>
    </section>

    <section id="galeria" class="container seccion-info">
        <h2>Fotografías del Libro</h2>
        <div class="galeria-fotos">
            <img src="https://images.unsplash.com/photo-1512820790803-83ca734da794?auto=format&fit=crop&w=500&q=80" alt="Libro abierto">
            <img src="https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?auto=format&fit=crop&w=500&q=80" alt="Detalle artístico">
            <img src="https://images.unsplash.com/photo-1531988042231-d39a9cc12a9a?auto=format&fit=crop&w=500&q=80" alt="Proceso de empaque">
        </div>
    </section>

    <footer class="container">
        <p>Sigue a la autora en sus redes sociales</p>
        
        <div class="redes-sociales">
            <a href="https://instagram.com" target="_blank" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
            <a href="https://facebook.com" target="_blank" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
            <a href="https://twitter.com" target="_blank" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
            <a href="mailto:autora@email.com" aria-label="Correo"><i class="far fa-envelope"></i></a>
        </div>

        <div class="creditos">
            &copy; 2026 Mi mundo de colores imperfectos. Todos los derechos reservados.
        </div>
    </footer>

</body>
</html>
