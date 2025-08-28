<!DOCTYPE html>
<html lang="es">   

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>DermoZen - Mi Emprendimiento</title>

  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet" />

  <style> 
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background-color: #f4f7f9;
      color: #333;
    }

    .header {
      background-color: #5bddf0;
      padding: 40px 0;
      text-align: center;
      color: white;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
    }

    .header h1 {
      margin: 0;
      font-size: 2.5em;
    }

    .topnav {
      background-color: #2d3436;
      overflow: hidden;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .topnav a {
      display: inline-block;
      color: #ffffff;
      padding: 14px 20px;
      text-decoration: none;
      font-weight: 600;
      transition: background-color 0.3s ease;
      cursor: pointer;
    }

    .topnav a:hover {
      background-color: #636e72;
      color: #ffeaa7;
    }

    .row {
      display: flex;
      flex-wrap: wrap;
      margin: 20px;
      gap: 20px;
    }

    .row__column {
      flex: 1;
      min-width: 250px;
      background-color: #ffffff;
      border-radius: 12px;
      padding: 20px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }

    .row__column h2 {
      color: #2d3436;
    }

    section {
      padding: 40px 20px;
      background-color: #f9f9f9;
      border-top: 2px solid #e0e0e0;
    }

    section h2 {
      text-align: center;
      color: #5bddf0(53, 149, 208);
      margin-bottom: 15px;
    }

    section p {
      max-width: 800px;
      margin: auto;
      font-size: 1.1em;
      text-align: center;
    }

    .gallery {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: center;
      padding: 40px 20px;
      background-color: #fff;
      border-radius: 12px;
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.05);
    }

    .product {
      background: #fff;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      padding: 20px;
      width: 250px;
      text-align: center;
      transition: transform 0.3s ease;
      cursor: pointer;
    }

    .product:hover {
      transform: scale(1.05);
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
    }

    .product img {
      width: 100%;
      border-radius: 10px;
    }

    .product h3 {
      color: #333;
      margin: 10px 0 5px;
    }

    .product p {
      font-size: 0.95em;
      margin: 5px 0;
    }

    .product .price {
      font-weight: bold;
      color: #636e72;
      font-size: 1.1em;
      margin-top: 8px;
    }

    form.contact-form {
      max-width: 600px;
      margin: 40px auto;
      background: #ffffff;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.1);
    }

    form.contact-form h2 {
      text-align: center;
      margin-bottom: 25px;
      color: #5c95f1;
    }

    form.contact-form label {
      display: block;
      margin-bottom: 8px;
      font-weight: 600;
      color: #333;
    }

    form.contact-form input,
    form.contact-form select,
    form.contact-form textarea {
      width: 100%;
      padding: 10px 12px;
      margin-bottom: 20px;
      border: 2px solid #ddd;
      border-radius: 8px;
      font-size: 1em;
      transition: border-color 0.3s ease;
      font-family: 'Poppins', sans-serif;
    }

    form.contact-form input:focus,
    form.contact-form select:focus,
    form.contact-form textarea:focus {
      border-color: #5c95f1;
      outline: none;
    }

    form.contact-form button {
      background-color: #5c95f1;
      color: white;
      font-weight: 700;
      padding: 14px 0;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      font-size: 1.2em;
      width: 100%;
      transition: background-color 0.3s ease;
    }

    form.contact-form button:hover {
      background-color: #5c95f1;
    }

    .footer {
      background-color: #dfe6e9;
      padding: 20px;
      text-align: center;
      margin-top: 40px;
      font-weight: 600;
      color: #5c95f1;
    }

    audio {
      display: block;
      margin: 20px auto;
      border-radius: 10px;
    }

    a {
      display: inline-block;
      margin: 10px;
      color: #;
      text-decoration: none;
      font-weight: 600;
    }

    a:hover {
      color: #5c95f1;
    }

    /* === Carrusel nuevo === */
    .carousel {
      overflow: hidden;
      width: 100%;
      max-width: 800px;
      margin: 30px auto 50px auto;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      background-color: #fff;
    }

    .carousel-track {
      display: flex;
      width: calc(250px * 10); /* 5 imgs + 5 imgs duplicadas para loop */
      animation: scroll 20s linear infinite;
    }

    .carousel-track img {
      width: 250px;
      height: 150px;
      object-fit: cover;
      margin-right: 10px;
      border-radius: 10px;
      cursor: pointer;
      transition: transform 0.3s ease;
    }

    .carousel-track img:hover {
      transform: scale(1.1);
    }

    @keyframes scroll {
      0% {
        transform: translateX(0);
      }

      100% {
        transform: translateX(-50%);
      }
    }

    /* Video responsivo */
    .video-container {
      position: relative;
      width: 100%;
      max-width: 800px;
      margin: 40px auto;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }

    .video-container iframe {
      width: 100%;
      height: 450px;
      border: none;
    }

    @media (max-width: 600px) {
      .video-container iframe {
        height: 250px;
      }
    }
  </style>
</head>

<body>

  <div class="header">
    <h1>DermoZen - Lo que Mereces en tú vida</h1>
  </div>

  <div class="topnav">
    <a href="#" onclick="irAInicio()">Inicio</a>
    <a href="#mision">Misión</a>
    <a href="#vision">Visión</a>
    <a href="#productos">Productos</a>
    <a href="#pedido">Pedido</a>
    <a href="#registros">Registros</a>
  </div>

  <div class="row" id="inicio">
    <div class="row__column">
      <h2>¿Por qué usar jabones naturales?</h2>
      <p>Porque cuidan tu piel sin químicos agresivos, son biodegradables y amigables con el medio ambiente. Ideales para toda la familia.</p>
    </div>
    <div class="row__column">
      <h2>Beneficios de nuestros jabones</h2>
      <p>Hidratación profunda, suavidad, propiedades antibacterianas y aroma natural. Cada jabón está hecho con dedicación y calidad artesanal.</p>
    </div>
    <div class="row__column">
      <h2>Ingredientes que usamos</h2>
      <p>Aceite de coco, miel, avena, lavanda, aloe vera y otros ingredientes 100% naturales seleccionados cuidadosamente.</p>
    </div>
  </div>

  <section id="mision">
    <h2>Nuestra Misión</h2>
    <p>Ofrecer jabones naturales artesanales de alta calidad que promuevan el cuidado personal y la conciencia ecológica, utilizando ingredientes sostenibles y procesos responsables.</p>
  </section>

  <section id="vision">
    <h2>Nuestra Visión</h2>
    <p>Convertirnos en una marca reconocida a nivel nacional por brindar bienestar, salud y respeto por el medio ambiente a través de nuestros productos naturales.</p>
  </section>

  <!-- Carrusel de imágenes -->
  <section aria-label="Carrusel de productos naturales">
    <div class="carousel" aria-live="polite" aria-atomic="true">
      <div class="carousel-track">
        <img src="images/General 1.webp" alt="Jabón natural 1" />
        <img src="images/General 2.webp" alt="Jabón natural 2" />
        <img src="images/3.jpeg" alt="Jabón natural 3" />
        <img src="images/4.webp" alt="Jabón natural 4" />
        <img src="images/5.jpg" alt="Jabón natural 5" />
        <!-- Duplicado para loop -->
        <img src="images/General 1.webp"Jabón natural 1" />
        <img src="images/General 2.webp" alt="Jabón natural 2" />
        <img src="images/3.jpeg" alt="Jabón natural 3" />
        <img src="images/4.webp" alt="Jabón natural 4" />
        <img src="images/5.jpg" alt="Jabón natural 5" />
      </div>
    </div>
  </section>
  <section id="testimonios">
  <h2>Lo que Dicen Nuestros Clientes</h2>
  <div class="row">
    <div class="row__column">
      <p>"Desde que uso el jabón de avena, mi piel se siente más suave y menos irritada. ¡Recomiendo DermoZen al 100%!"</p>
      <p><strong>- María, Santa Ana</strong></p>
    </div>
    <div class="row__column">
      <p>"Mi favorito es el de miel. Me encanta su aroma y cómo deja mi piel hidratada."</p>
      <p><strong>- José, San Salvador</strong></p>
    </div>
    <div class="row__column">
      <p>"Probé el de aloe vera y me ayudó con la resequedad. ¡Gracias por crear productos naturales y efectivos!"</p>
      <p><strong>- Carmen, Ahuachapán</strong></p>
    </div>
  </div>
</section>

  <!-- Video tutorial -->
  <section id="video">
    <h2>Empresas industriales</h2>
    <div class="video-container">
      <iframe src="https://www.youtube.com/embed/2KXKeyh-Uwc?si=c8oV3bHlrj1iqboy" title="YouTube video player" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
    </div>
    <div style="text-align: center; margin-top: 20px;">
  <a href="https://www.youtube.com/results?search_query=jabones+artesanales" target="_blank" style="background-color: #27ae60; color: white; padding: 12px 25px; border-radius: 8px; text-decoration: none; font-weight: bold; transition: background-color 0.3s ease;">
    Ver más sitios
  </a>
</div>
  </section>
  

  <!-- GALERÍA DE PRODUCTOS -->
  <section id="productos">
    <h2>Nuestros Productos</h2>
    <div class="gallery">
      <div class="product">
        <img src="images/Avena.jpg" alt="Jabón de avena" />
        <h3>Jabón de Avena</h3>
        <p>Exfolia suavemente tu piel y calma la irritación.</p>
        <p class="price">$1.00</p>
      </div>
      <div class="product">
        <img src="images/JabonArroz.webp" alt="Jabón de arroz" />
        <h3>Jabón de Arroz</h3>
        <p>Ideal para limpiar profundamente y suavizar la piel.</p>
        <p class="price">$1.00</p>
      </div>
      <div class="product">
        <img src="images/Savila.webp" alt="Jabón de aloe vera" />
        <h3>Jabón de Aloe Vera</h3>
        <p>Hidratación profunda para pieles sensibles.</p>
        <p class="price">$1.00</p>
      </div>
      <div class="product">
        <img src="images/¿¿Miel.webp" alt="Jabón de miel" />
        <h3>Jabón de Miel</h3>
        <p>Nutre tu piel y tiene propiedades antibacterianas.</p>
        <p class="price">$1.00</p>
      </div>
    </div>
  </section>
<section id="video">
  <h2>Empresas Industriales</h2>
  <div class="video-container">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/wTdHmbRw-W8?si=EsnrmnW-JfsWkfeq" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
  </div>
</section>
<section id="precios">
  <h2 style="text-align: center; color: #5c95f1;">Paquetes Promocionales</h2>

  <style>
    .promo-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 40px;
      margin: 40px auto;
      max-width: 1200px;
    }

    .promo-card {
      background: #f7f7f7;
      border-radius: 20px;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
      overflow: hidden;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      width: 300px;
      text-align: center;
    }

    .promo-card:hover {
      transform: scale(1.05);
      box-shadow: 0 12px 25px rgba(0, 0, 0, 0.2);
    }

    .promo-img {
      height: 220px;
      overflow: hidden;
    }

    .promo-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.4s ease;
    }

    .promo-card:hover .promo-img img {
      transform: scale(1.1);
    }

    .promo-card h3 {
      margin-top: 15px;
      font-size: 1.4em;
      color: #333;
    }

    .promo-card p {
      padding: 0 20px;
      color: #666;
    }

    .price {
      font-weight: bold;
      color: #2b8f5c;
      font-size: 1.2em;
      margin-bottom: 20px;
    }
  </style>

  <div class="promo-container">
    <div class="promo-card">
      <div class="promo-img">
        <img src="images/Solicitud de beca/Combo 3.jpeg" alt="Combo Básico">
      </div>
      <h3>Combo Básico</h3>
      <p>3 jabones surtidos para el cuidado diario.</p>
      <p class="price">$2.50</p>
    </div>

    <div class="promo-card">
      <div class="promo-img">
        <img src="images/Solicitud de beca/Combo 2.jpeg" alt="Combo Familiar">
      </div>
      <h3>Combo Familiar</h3>
      <p>6 jabones a tu elección. Ideal para la familia.</p>
      <p class="price">$5.00</p>
    </div>

    <div class="promo-card">
      <div class="promo-img">
        <img src="images/Solicitud de beca/Combo1.jpeg" alt="Paquete Mayorista">
      </div>
      <h3>Paquete Mayorista</h3>
      <p>12 jabones con descuento para revender o regalar.</p>
      <p class="price">$9.00</p>
    </div>
  </div>
</section>
<!-- FORMULARIO DE PEDIDO / CONTACTO -->
<section id="pedido">
  <form class="contact-form" onsubmit="return enviarFormulario(event)">
    <h2>Haz tu Pedido o Contáctanos</h2>

    <label for="nombre">Nombre completo:</label>
    <input type="text" id="nombre" name="nombre" required placeholder="Tu nombre completo" />

    <label for="correo">Correo electrónico:</label>
    <input type="email" id="correo" name="correo" required placeholder="ejemplo@correo.com" />

    <label for="telefono">Teléfono (opcional):</label>
    <input type="tel" id="telefono" name="telefono" placeholder="Tu número de teléfono" />

    <label for="tipoJabon">Tipo de jabón:</label>
    <select id="tipoJabon" name="tipoJabon" required>
      <option value="">-- Selecciona un jabón --</option>
      <option value="Avena">Jabón de Avena</option>
      <option value="Arroz">Jabón de Arroz</option>
      <option value="Aloe Vera">Jabón de Savila</option>
      <option value="Miel">Jabón de Miel</option>
    </select>

    <label for="cantidad">Cantidad:</label>
    <input type="number" id="cantidad" name="cantidad" min="1" required placeholder="Cantidad de jabones" />

    <label for="direccion">Dirección de envío:</label>
    <textarea id="direccion" name="direccion" rows="3" placeholder="Escribe tu dirección completa"></textarea>

    <button type="submit">Enviar pedido</button>
  </form>
</section>
<!-- Reproductores de audio estilizados -->
<style>
  .audio-container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    background-color: #5c95f1;
    padding: 30px;
    border-radius: 15px;
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
    margin: 40px auto;
    max-width: 800px;
  }

  .audio-box {
    background-color: #5c95f1;
    padding: 15px;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    flex: 1 1 300px;  }

  .audio-box audio {
    width: 100%;
    outline: none;
  }
</style>

<div class="audio-container">
  <div class="audio-box">
    <audio controls>
      <source src="images/traimory-mega-horn-angry-siren-f-cinematic-trailer-sound-effects-193408.mp3" type="audio/mp3">
      Tu navegador no soporta audio HTML5.
    </audio>
  </div>
  <div class="audio-box">
    <audio controls>
      <source src="images/Audio de WhatsApp 2025-07-02 a las 16.32.19_d7e95bcf.waptt.opus" type="audio/mp3">
      Tu navegador no soporta audio HTML5.
    </audio>
  </div>
</div>


