!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>BOTIGA DE SALUD</title>
  <!-- Fuente Dancing Script de Google Fonts para un estilo más cursivo en la mayor parte del sitio -->
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap" rel="stylesheet">
  <style>
    /* Reseteo de márgenes y paddings */
    * {
      /* Vamos a poner logos de foto para Instagram y Facebook y estrellas a los testimonios */
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    /* Cuerpo con fondo amarillo y letras negras */
    body {
      font-family: 'Dancing Script', cursive;
      background: #FFFF00; /* Amarillo muy potente */
      color: #000; /* Letras negras */
      line-height: 1.6;
      position: relative;
      min-height: 100vh;
      font-size: 1.2rem; /* Tamaño base mayor para textos cursivos */
    }

    /* Cabecera */
    header {
      background-color: rgba(214, 236, 129, 0.8);
      padding: 20px;
      text-align: center;
      position: relative;
    }
    header h1 {
      color: #000;
      font-size: 3.5rem;
      text-transform: uppercase;
      letter-spacing: 1px;
      margin-top: 60px;
    }
    /* Logo en la cabecera */
    .logo {
      width: 80px;
      height: auto;
      position: absolute;
      top: 20px;
      left: 20px;
    }

    /* Barra de navegación */
    nav {
      background: rgba(17, 186, 70, 0.8);
      text-align: center;
      padding: 10px;
    }
    nav a {
      margin: 0 10px;
      text-decoration: none;
      color: #000;
      font-weight: bold;
      font-size: 1.5rem;
    }

    /* Contenedor principal */
    .container {
      max-width: 1200px;
      margin: 20px auto;
      background-color: rgba(255, 255, 255, 0.95);
      padding: 20px;
      border-radius: 5px;
      font-size: 1.3rem; /* Texto principal un poco más grande */
    }

    section {
      margin-bottom: 30px;
    }

    /* Contenedor para imágenes con Flexbox */
    .image-row {
      display: flex;
      gap: 10px;
      justify-content: center;
      flex-wrap: wrap;
      margin-bottom: 20px;
    }

    /* Estilo para las imágenes en forma circular */
    .image-row img {
      width: 300px;
      height: 300px;
      object-fit: cover;
      border: 2px solid #333;
      border-radius: 50%;
    }

    /* Estilo para la descripción de la tienda */
    .store-description {
      color: #000;
      font-size: 1.3rem;
      margin-top: 10px;
    }

    /* Botones */
    .btn {
      display: inline-block;
      background: #076452;
      color: #fff;
      padding: 10px 20px;
      border-radius: 5px;
      text-decoration: none;
      margin: 5px 10px 5px 0;
      transition: background 0.3s;
      font-size: 1.3rem;
    }
    .btn:hover {
      background: #5aae9f;
    }

    /* Sección de Ubicación */
    .ubicacion {
      margin-bottom: 30px;
      text-align: center;
    }
    .ubicacion p {
      font-size: 1.3rem;
      margin-bottom: 10px;
    }

    /* Sección de Testimonios y Placa de Calidad */
    .testimonials {
      background: #F7F7F7;
      padding: 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
      margin-bottom: 20px;
      font-size: 1.3rem;
    }
    .testimonials h2 {
      text-align: center;
      margin-bottom: 15px;
      font-size: 2rem;
    }
    .quality-badge {
      display: block;
      margin: 0 auto 15px auto;
      width: 150px;
      height: auto;
    }
    .testimonial {
      font-style: italic;
      margin-bottom: 10px;
      position: relative;
      padding-left: 120px; /* Espacio para las estrellas */
    }
    /* Estilos para las estrellas */
    .stars {
      position: absolute;
      left: 0;
      top: 0;
      font-size: 1.2rem;
      color: #f4d10b; /* Dorado */
      width: 100px;
      text-align: center;
    }
    .author {
      text-align: right;
      font-weight: bold;
    }

    /* Sección de Contacto: Usamos un estilo clásico con Arial */
    #contacto {
      font-family: Arial, sans-serif;
      font-size: 1rem;
    }
    #contacto a {
      font-family: Arial, sans-serif;
      font-size: 1rem;
    }

    /* Pie de página */
    footer {
      background: rgba(0, 0, 0, 0.8);
      color: #fff;
      text-align: center;
      padding: 10px;
      font-size: 1rem;
    }
    .social-links {
      margin-top: 10px;
    }
    .social-links a {
      position: relative;
      z-index: 1100; /* Asegura que estén sobre otros elementos */
      margin: 0 10px;
      text-decoration: none;
      font-weight: bold;
      font-size: 1rem;
    }
    /* Estilos para los iconos de redes sociales */
    .social-links img {
      vertical-align: middle;
      width: 24px;
      height: 24px;
      margin-right: 5px;
    }

    /* Marca de agua */
    .watermark {
      position: fixed;
      bottom: 10px;
      right: 10px;
      font-size: 0.8rem;
      color: #18df8c;
      opacity: 0.6;
      z-index: 1000;
    }

    /* Responsive */
    @media (max-width: 768px) {
      nav a {
        display: block;
        margin: 5px 0;
      }
      header .logo {
        position: static;
        display: block;
        margin: 0 auto;
      }
      /* Reducir el padding en testimonios para que las estrellas no se superpongan */
      .testimonial {
        padding-left: 60px;
      }
      .stars {
        width: 60px;
        font-size: 1rem;
      }
    }
  </style>
</head>
<body>
  <header>
    <!-- Logo: asegúrate de tener el archivo "logo2.jpg" en la raíz del proyecto -->
    <img src="logo2.jpg" alt="Logo BOTIGA DE SALUD" class="logo">
    <h1>BOTIGA DE SALUD</h1>
  </header>

  <nav>
    <a href="#inicio">Inicio</a>
    <a href="#contacto">Contacto</a>
    <a href="#ubicacion">Ubicación</a>
    <a href="#testimonios">Testimonios</a>
  </nav>

  <div class="container">
    <!-- Sección de inicio con imagen o descripción -->
    <section id="inicio">
      <!-- Contenedor de imágenes para mostrarlas en línea -->
      <div class="image-row">
        <img src="miel.avif" alt="Productos de Herboristería">
        <img src="crema.avif" alt="Crema">
        <img src="miel2.avif" alt="Miel">
      </div>
      <p class="store-description">
        Bienvenido a <strong>BOTIGA DE SALUD</strong>, tu tienda de salud integral. Aquí encontrarás una amplia variedad de productos de herboristería, dietética, cosmética y EcoTienda, seleccionados cuidadosamente para mejorar tu bienestar y el de tu familia. 
        Nos enorgullece ofrecer productos naturales y orgánicos de la mejor calidad, asesoramiento personalizado y un ambiente acogedor. 
        Visítanos y descubre un mundo de bienestar, salud y equilibrio natural.
      </p>
    </section>

    <!-- Sección de Contacto -->
    <section id="contacto">
      <h2>Contacto</h2>
      <p><strong>Correo:</strong>
        <a href="mailto:herboristeriacentrovenecia@yahoo.com">herboristeriacentrovenecia@yahoo.com</a>
      </p>
      <p><strong>Teléfonos:</strong>
        <a href="tel:965154120">965154120</a> | 
        <a href="tel:695333363">695333363</a>
      </p>
      <!-- Botones para enviar correo o llamar -->
      <a href="mailto:herboristeriacentrovenecia@yahoo.com" class="btn">Enviar Correo</a>
      <a href="tel:965154120" class="btn">Llamar</a>
    </section>

    <!-- Sección de Ubicación -->
    <section id="ubicacion" class="ubicacion">
      <h2>Ubicación</h2>
      <p><strong>Dirección:</strong> Avd. Costablanca, 21 Lc.28 C.C. Venecia, 03540 Alicante</p>
      <a href="https://www.google.com/maps?q=Avd.+Costablanca,+21+Lc.28+C.C.+Venecia,+03540+Alicante" target="_blank" class="btn">Ver Ubicación</a>
    </section>

    <!-- Sección de Testimonios y Placa de Calidad -->
    <section id="testimonios">
      <h2>Testimonios y Placa de Calidad</h2>
      <!-- Placa de calidad: asegúrate de tener el archivo "calidad - copia (2).jpg" en la raíz -->
      <img src="calidad - copia (2).jpg" alt="Placa de Calidad" class="quality-badge">
      <!-- Testimonios -->
      <div class="testimonials">
        <p class="testimonial">
          <span class="stars">★★★★★</span>
          "La mejor tienda de productos naturales, me ha ayudado a mejorar mi salud."
        </p>
        <p class="author">- María G.</p>
      </div>
      <div class="testimonials">
        <p class="testimonial">
          <span class="stars">★★★★★</span>
          "Un servicio excepcional y productos de alta calidad. ¡Muy recomendable!"
        </p>
        <p class="author">- Juan P.</p>
      </div>
    </section>
  </div>

  <footer>
    <p>&copy; 2025 BOTIGA DE SALUD. Todos los derechos reservados.</p>
    <!-- Enlaces a redes sociales con iconos: asegúrate de tener "instagram.jpg" y "facebook.jpg" -->
    <div class="social-links">
      <a href="https://instagram.com/botiga_de_salud" target="_blank">
        <img src="instagram.jpg" alt="Instagram">Instagram
      </a>
      <a href="https://facebook.com/BotigaDeSalud" target="_blank">
        <img src="facebook.jpg" alt="Facebook">Facebook
      </a>
    </div>
  </footer>

  <!-- Marca de agua -->
  <div class="watermark">
    Diseño y desarrollo por PixelCraft Studio
  </div>
</body>
</html>

