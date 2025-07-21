<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Araña Pavo Real</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      font-family: 'Poppins', sans-serif;
      font-size: 1.1rem;
      line-height: 1.7;
      background-color: #121212;
      color: #eaeaea;
      transition: background-color 0.3s ease, color 0.3s ease;
      padding-top: 200px;
    }
    main > section:first-of-type { margin-top: 7rem; }

    header {
      position: fixed; top: 0; left: 0; width: 100%;
      background: linear-gradient(to bottom, #1a1a1a, #222);
      border-bottom: 1px solid #444;
      box-shadow: 0 4px 12px rgba(0, 204, 153, 0.3);
      padding: 1.5rem 2rem;
      text-align: center; z-index: 1000;
    }
    header h1 {
      font-size: 2.8rem;
      color: #00cca6;
      text-shadow: 0 0 12px rgba(0, 204, 153, 0.8), 0 0 30px rgba(0, 204, 153, 0.5);
      font-weight: 700;
    }
    header p {
      color: #ccc; font-size: 1.3rem; margin-top: 0.4rem;
    }

    #toggle-theme {
      position: fixed; top: 15px; right: 25px;
      background: #00cca6; border-radius: 20px;
      width: 50px; height: 26px; cursor: pointer;
      box-shadow: 0 0 10px rgba(0, 204, 153, 0.7);
      display: flex; align-items: center; padding: 3px;
      border: none; z-index: 1100;
    }
    #toggle-theme .switch {
      background: #eee; width: 20px; height: 20px;
      border-radius: 50%; transition: transform 0.3s ease;
      box-shadow: 0 0 8px rgba(0,0,0,0.3);
    }
    body.light-mode #toggle-theme { background: #eee; }
    body.light-mode #toggle-theme .switch {
      transform: translateX(25px); background: #00cca6;
    }

    body.light-mode {
      background-color: #f4f4f4;
      color: #111;
    }

    main {
      max-width: 960px; margin: auto; padding: 0 2rem;
    }

    section {
      background-color: #181818; border-radius: 8px;
      padding: 2.8rem 3rem; margin-bottom: 2.5rem;
      box-shadow: 0 3px 15px rgba(0, 204, 153, 0.15);
      border-left: 6px solid #00cca6;
    }
    section:nth-child(even) {
      border-left: none; border-right: 6px solid #00cca6;
      background-color: #202020;
    }
    h2 {
      font-size: 2rem; color: #33e0c8;
      margin-bottom: 1.25rem; border-left: 5px solid #66ebdc;
      padding-left: 1rem;
      text-shadow: 0 0 6px rgba(0, 200, 150, 0.4);
    }
    p {
      color: #dcdcdc; margin-bottom: 1.4rem;
    }

    .gallery {
      display: flex; justify-content: center;
      gap: 1.5rem; flex-wrap: wrap;
    }
    .gallery img {
      max-width: 320px; width: 100%;
      border-radius: 10px; border: 1px solid #555;
      cursor: pointer;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    .gallery img:hover {
      transform: scale(1.07);
      box-shadow: 0 0 20px rgba(0, 204, 153, 0.5);
    }

    footer {
      background-color: #1c1c1c;
      text-align: center; padding: 2rem 1rem;
      font-size: 1rem; color: #999;
      border-top: 1px solid #444;
      max-width: 960px; margin: 0 auto 2rem;
      border-radius: 0 0 10px 10px;
    }

    .lightbox {
      position: fixed; top: 0; left: 0;
      width: 100vw; height: 100vh;
      background: rgba(0,0,0,0.85);
      display: none; justify-content: center; align-items: center;
      z-index: 1200;
    }
    .lightbox.active { display: flex; }
    .lightbox img {
      max-width: 90%; max-height: 85vh;
      border-radius: 10px;
      box-shadow: 0 0 25px rgba(0, 200, 150, 0.8);
    }
    .lightbox .close-btn {
      position: fixed; top: 15px; right: 25px;
      font-size: 3rem; color: #00cca6;
      background: transparent; border: none;
      cursor: pointer; font-weight: 700;
    }
    .lightbox .close-btn:hover {
      color: #66ebdc;
    }

    @media (max-width:768px) {
      header h1 { font-size: 2rem; }
      header p { font-size: 1rem; }
      section { padding: 2rem 1.5rem; }
      h2 { font-size: 1.6rem; padding-left: 0.7rem; }
      .gallery img { max-width: 100%; }
      #toggle-theme { width: 42px; height: 22px; top:10px; right:15px; }
      #toggle-theme .switch { width:18px; height:18px; }
      body.light-mode #toggle-theme .switch { transform: translateX(22px); }
    }
  </style>
</head>
<body>

  <header>
    <h1>Araña Pavo Real</h1>
    <p>Pequeña, colorida y sorprendentemente carismática</p>
  </header>

  <button id="toggle-theme" aria-label="Modo claro/oscuro" role="switch" aria-checked="false">
    <div class="switch"></div>
  </button>

  <main>
    <section>
      <h2>¿Qué es la Araña Pavo Real?</h2>
      <p>
        La araña pavo real (<em>Maratus</em>) es una pequeña araña saltarina famosa por los vivos colores y las danzas de cortejo de los machos. Pertenece a la familia <em>Salticidae</em> y se encuentra en Australia.
      </p>
    </section>
    <section>
      <h2>Apariencia y Colores</h2>
      <p>
        Los machos tienen un abdomen expandible y muy colorido, similar a las plumas de un pavo real. Presentan tonalidades metálicas en azul, rojo, verde y naranja. Las hembras, por otro lado, son de aspecto más discreto.
      </p>
    </section>
    <section>
      <h2>Comportamiento y Cortejo</h2>
      <p>
        Durante el cortejo, el macho eleva su abdomen, mueve las patas delanteras y ejecuta una danza vibrante para atraer a la hembra. Si ella no está receptiva, puede rechazarlo o incluso atacarlo.
      </p>
    </section>
    <section>
      <h2>Hábitat y Distribución</h2>
      <p>
        Estas arañas viven en hábitats abiertos y soleados del suroeste australiano. Prefieren áreas con vegetación baja, arena o corteza seca donde pueden camuflarse y moverse con agilidad.
      </p>
    </section>
    <section>
      <h2>Galería</h2>
      <div class="gallery">
        <img src="https://ausemade.com.au/wp-content/uploads/male-dancing-maratus-volans-20131008-woy-woy-10150435166-md.jpg" alt="Araña pavo real mostrando su abdomen colorido" loading="lazy" />
        <img src="https://i.redd.it/maratus-volans-v0-xslol9ct9smd1.jpg?width=1479&format=pjpg&auto=webp&s=1a8d159031463861a201696f8f57f9d8bfec71ec" alt="Maratus volans macho con colores metálicos" loading="lazy" />
        <img src="https://static.nationalgeographic.es/files/styles/image_3200/public/02-peacock-spider-9678_9679_9680.webp?w=1190&h=911" alt="Araña pavo real en postura de cortejo" loading="lazy" />
      </div>
    </section>
  </main>

  <footer>
    <p>© 2025 Sitio educativo sobre la Araña Pavo Real | Información científica y visual</p>
  </footer>

  <div class="lightbox" role="dialog" aria-modal="true">
    <button class="close-btn" aria-label="Cerrar">×</button>
    <img src="" alt="Imagen ampliada" />
  </div>

  <script>
    const toggle = document.getElementById('toggle-theme'), bodyEl = document.body;
    toggle.addEventListener('click', () => {
      bodyEl.classList.toggle('light-mode');
      toggle.setAttribute('aria-checked', bodyEl.classList.contains('light-mode'));
    });

    const lightbox = document.querySelector('.lightbox'),
          imgBox = lightbox.querySelector('img'),
          btnClose = lightbox.querySelector('.close-btn');

    document.querySelectorAll('.gallery img').forEach(img => {
      img.addEventListener('click', () => {
        imgBox.src = img.src;
        imgBox.alt = img.alt;
        lightbox.classList.add('active');
        btnClose.focus();
      });
    });
    btnClose.addEventListener('click', () => lightbox.classList.remove('active'));
    lightbox.addEventListener('click', e => {
      if (e.target === lightbox) lightbox.classList.remove('active');
    });
    document.addEventListener('keydown', e => {
      if (e.key === 'Escape') lightbox.classList.remove('active');
    });
  </script>
</body>
</html>
