<!DOCTYPE html>
<html lang="es">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Randy De Santis</title>
  <style>
    * { box-sizing: border-box; }
    body { font-family: Arial; margin: 20px; }
    .encabezado { background: #2196f3; color: white; padding: 20px; text-align: center; }
    .encabezado h1 { margin: 0; }
    .menu { background: #333; color: white; padding: 20px; }
    .menu a { color: white; text-decoration: none; padding: 0 8px; }
    .menu a:hover { color: #2196f3; text-decoration: underline; }
    .contenido { display: flex; gap: 10px; margin-top: 10px; }
    .principal { background: #DDEEFF; padding: 30px; width: 70%; }
    .lateral { background: #DDF5DD; padding: 30px; width: 30%; }
    .detalle { background: #DDEEFF; padding: 30px; margin-top: 10px; }
    .detalle a { color: #1565c0; }
    .pie { background: #555; color: white; padding: 15px; text-align: center; margin-top: 10px; }
  </style>
</head>

<body>

  <!-- PÁGINA DE INICIO -->
  <div id="inicio" class="pagina">
    <div class="encabezado">
      <h1>Randy De Santis</h1>
    </div>
    <div class="menu">
      <a href="#biografia" target="_blank" rel="noopener">Biografía</a> |
      <a href="#fotos" target="_blank" rel="noopener">Fotos</a> |
      <a href="#musica" target="_blank" rel="noopener">Música</a> |
      <a href="#video" target="_blank" rel="noopener">Video</a>
    </div>
    <div class="contenido">
      <div class="principal">
        <h2>Bienvenidos</h2>
        <p>Hola, bienvenido a mi página biográfica</p>
      </div>
      <div class="lateral">
        <h2>Proyecto de Desarrollo de Plataformas Web</h2>
        <p>Buenas noches</p>
      </div>
    </div>
  </div>

  <!-- BIOGRAFÍA -->
  <div id="biografia" class="pagina" hidden>
    <div class="encabezado">
      <h1>Biografía</h1>
    </div>
    <div class="detalle">
      <h2>Randy De Santis</h2>
      <p>Hola, me llamo Randy De Santis y tengo 29 años. Soy nacido en Guayaquil pero he vivido en Ventanas prácticamente toda mi vida y actualmente estudio en
        el 3er Semestre de la carrera de Sistemas de Información de la Universidad Técnica de Babahoyo.</p>
      <p><a href="#inicio">← Volver al inicio</a></p>
    </div>
  </div>

  <!-- FOTOS -->
  <div id="fotos" class="pagina" hidden>
    <div class="encabezado">
      <img src="randy.jpeg" alt="Randy" width="300">
      <img src="randy1.jpeg" alt="Randy 1" width="300">
      <p><a href="#inicio">← Volver al inicio</a></p>
    </div>
  </div>

  <!-- MÚSICA -->
  <div id="musica" class="pagina" hidden>
    <div class="encabezado">
      <h1>Música</h1>
    </div>
    <div class="detalle">
      <h2>Discografía y canciones</h2>
      <p>Aquí irá la lista de canciones o álbumes.</p>
      <p><a href="#inicio">← Volver al inicio</a></p>
    </div>
  </div>

  <!-- VIDEO -->
  <div id="video" class="pagina" hidden>
    <div class="encabezado">
      <h1>Video</h1>
    </div>
    <div class="detalle">
      <h2>Videos</h2>
      <p>Aquí irán los videos.</p>
      <p><a href="#inicio">← Volver al inicio</a></p>
    </div>
  </div>

  <!-- PIE (se ve en todas las páginas) -->
  <div class="pie">
    © 2026 Randy De Santis - Todos los derechos reservados
  </div>

  <script>
    // Muestra solo la página que indica la dirección (#biografia, #fotos, etc.)
    function mostrar() {
      var id = location.hash.slice(1) || "inicio";
      var paginas = document.querySelectorAll(".pagina");
      var existe = false;
      paginas.forEach(function (p) {
        p.hidden = (p.id !== id);
        if (p.id === id) existe = true;
      });
      if (!existe) document.getElementById("inicio").hidden = false;
    }
    window.addEventListener("hashchange", mostrar);
    mostrar();
  </script>

</body>

</html>
      </p>
    </div>
  </div>
</body>
</html>
