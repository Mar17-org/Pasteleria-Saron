# Pasteleria-Saron
![image](https://github.com/user-attachments/assets/2f704d59-6ff7-43ce-8dac-6ffc3f236fb3)

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Simulador de Pastel</title>
  <link rel="stylesheet" href="caracteristicas.css" />
</head>
<body>
  <div class="container">
    <h1>Simulador de Presupuesto de Pastel</h1>

    <div class="simulador">
      <form class="formulario">
        <div class="grupo">
          <label for="sabor">Sabor:</label>
          <select id="sabor">
            <option value="">Selecciona</option>
            <option value="Vainilla">Vainilla</option>
            <option value="Chocolate">Chocolate</option>
            <option value="Red Velvet">Red Velvet</option>
          </select>
        </div>

        <div class="grupo">
          <label for="cobertura">Cobertura:</label>
          <select id="cobertura">
            <option value="">Selecciona</option>
            <option value="Crema">Crema</option>
            <option value="Fondant">Fondant</option>
            <option value="Chocolate">Chocolate</option>
          </select>
        </div>

        <div class="grupo">
          <label for="tamano">Tamaño:</label>
          <select id="tamano">
            <option value="">Selecciona</option>
            <option value="Pequeño">Pequeño (6")</option>
            <option value="Mediano">Mediano (8")</option>
            <option value="Grande">Grande (10")</option>
          </select>
        </div>

        <div class="grupo">
          <label for="personalizado">¿Personalizado?</label>
          <select id="personalizado">
            <option value="No">No</option>
            <option value="Sí">Sí</option>
          </select>
        </div>
      </form>

      <div class="preview">
        <div class="pastel" id="pastelPreview">
          <img id="imagenPastel" src="" alt="Vista previa del pastel" />
        </div>
        <div class="descripcion" id="descripcion">
          Selecciona ingredientes para ver tu pastel...
        </div>
        <div class="precio" id="precioFinal">Precio total: $0</div>
      </div>
        
  </div>

  <script>
    const sabor = document.getElementById('sabor');
    const cobertura = document.getElementById('cobertura');
    const tamano = document.getElementById('tamano');
    const personalizado = document.getElementById('personalizado');
    const descripcion = document.getElementById('descripcion');
    const precioFinal = document.getElementById('precioFinal');

    const precios = {
      sabor: {
        "Vainilla": 20,
        "Chocolate": 25,
        "Red Velvet": 30
      },
      cobertura: {
        "Crema": 10,
        "Fondant": 15,
        "Chocolate": 12
      },
      tamano: {
        "Pequeño": 20,
        "Mediano": 35,
        "Grande": 50
      },
      personalizado: {
        "Sí": 15,
        "No": 0
      }
    };

    function actualizarVista() {
      const s = sabor.value;
      const c = cobertura.value;
      const t = tamano.value;
      const p = personalizado.value;

      let total = 0;

      if (s) total += precios.sabor[s];
      if (c) total += precios.cobertura[c];
      if (t) total += precios.tamano[t];
      if (p) total += precios.personalizado[p];

      descripcion.innerHTML = `
        <p><strong>Sabor:</strong> ${s || "No seleccionado"}</p>
        <p><strong>Cobertura:</strong> ${c || "No seleccionada"}</p>
        <p><strong>Tamaño:</strong> ${t || "No seleccionado"}</p>
        <p><strong>Personalizado:</strong> ${p}</p>
      `;

      precioFinal.textContent = `Precio total: $${total}`;
    }

    sabor.addEventListener('change', actualizarVista);
    cobertura.addEventListener('change', actualizarVista);
    tamano.addEventListener('change', actualizarVista);
    personalizado.addEventListener('change', actualizarVista);
    const imagenPastel = document.getElementById('imagenPastel');

function obtenerRutaImagen(sabor, cobertura) {
  if (!sabor || !cobertura) return '';

  // Simulación de rutas de imágenes (debes reemplazar con tus propias imágenes)
  const combinacion = `${sabor}-${cobertura}`.toLowerCase().replace(/\s/g, '-');
  return `imagenes/${combinacion}.jpg`;
}

function actualizarVista() {
  const s = sabor.value;
  const c = cobertura.value;
  const t = tamano.value;
  const p = personalizado.value;

  let total = 0;

  if (s) total += precios.sabor[s];
  if (c) total += precios.cobertura[c];
  if (t) total += precios.tamano[t];
  if (p) total += precios.personalizado[p];

  descripcion.innerHTML = `
    <p><strong>Sabor:</strong> ${s || "No seleccionado"}</p>
    <p><strong>Cobertura:</strong> ${c || "No seleccionada"}</p>
    <p><strong>Tamaño:</strong> ${t || "No seleccionado"}</p>
    <p><strong>Personalizado:</strong> ${p}</p>
  `;

  precioFinal.textContent = `Precio total: $${total}`;

  const rutaImagen = obtenerRutaImagen(s, c);
  if (rutaImagen) {
    imagenPastel.src = rutaImagen;
    imagenPastel.alt = `Pastel de ${s} con ${c}`;
  } else {
    imagenPastel.src = '';
    imagenPastel.alt = '';
  }

descripcion.innerHTML = `
  <p><strong>Sabor:</strong> ${s || "No seleccionado"}</p>
  <p><strong>Cobertura:</strong> ${c || "No seleccionada"}</p>
  <p><strong>Tamaño:</strong> ${t || "No seleccionado"}</p>
  <p><strong>Personalizado:</strong> ${p}</p>
`;
}

 </script>

</body>
</html>
