<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Lectura Inteligente</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
      background: #f9f9f9;
      color: #333;
      line-height: 1.6;
    }
    h1, h2 {
      color: #2c3e50;
    }
    .nivel {
      border: 1px solid #ccc;
      background: #fff;
      border-radius: 10px;
      padding: 15px;
      margin-bottom: 20px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    button {
      background: #3498db;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 5px;
      cursor: pointer;
      margin-top: 10px;
    }
    button:hover {
      background: #2980b9;
    }
    .pregunta {
      margin-top: 10px;
      margin-bottom: 5px;
    }
    .respuesta {
      margin-bottom: 10px;
    }
  </style>
</head>
<body>

  <h1>Lectura Inteligente</h1>
  <p><strong>Descripción:</strong> Lectura Inteligente es una app educativa para mejorar la comprensión lectora, interpretación crítica y habilidades de lógica. Con niveles progresivos y preguntas interactivas, prepara a los jóvenes para situaciones cotidianas y la prueba Saber ICFES.</p>

  <div class="nivel" id="nivel1">
    <h2>Nivel 1 - Comprensión básica</h2>
    <p>Lee el siguiente texto:</p>
    <blockquote>
      "Juan salió temprano a comprar pan, pero al llegar a la tienda se dio cuenta de que no tenía su billetera."
    </blockquote>
    <div class="pregunta">¿Por qué no pudo comprar el pan Juan?</div>
    <input class="respuesta" type="text" id="respuesta1"/>
    <button onclick="verificarRespuesta('respuesta1', 'porque no tenía su billetera')">Verificar</button>
  </div>

  <div class="nivel" id="nivel2">
    <h2>Nivel 2 - Interpretación lógica</h2>
    <p>Texto:</p>
    <blockquote>
      "Ana revisó tres veces su correo, aunque sabía que no recibiría noticias hasta el lunes."
    </blockquote>
    <div class="pregunta">¿Qué nos dice esto sobre el comportamiento de Ana?</div>
    <input class="respuesta" type="text" id="respuesta2"/>
    <button onclick="verificarRespuesta('respuesta2', 'estaba ansiosa')">Verificar</button>
  </div>

  <div class="nivel" id="nivel3">
    <h2>Nivel 3 - Cultura general e historia</h2>
    <div class="pregunta">¿En qué año se firmó la independencia de Colombia?</div>
    <input class="respuesta" type="text" id="respuesta3"/>
    <button onclick="verificarRespuesta('respuesta3', '1810')">Verificar</button>
  </div>

  <div class="nivel" id="nivel4">
    <h2>Nivel 4 - Conceptos básicos</h2>
    <div class="pregunta">¿Qué es un sinónimo?</div>
    <input class="respuesta" type="text" id="respuesta4"/>
    <button onclick="verificarRespuesta('respuesta4', 'palabra con significado similar')">Verificar</button>
  </div>

  <div class="nivel" id="nivel5">
    <h2>Nivel 5 - Situaciones cotidianas</h2>
    <div class="pregunta">Si llegas tarde a clase por tráfico, ¿qué podrías hacer?</div>
    <input class="respuesta" type="text" id="respuesta5"/>
    <button onclick="verificarRespuesta('respuesta5', 'avisar al profesor')">Verificar</button>
  </div>

  <script>
    function verificarRespuesta(inputId, respuestaCorrecta) {
      const respuesta = document.getElementById(inputId).value.trim().toLowerCase();
      if (respuesta.includes(respuestaCorrecta.toLowerCase())) {
        alert("¡Correcto!");
      } else {
        alert("Intenta de nuevo.");
      }
    }
  </script>

</body>
</html>
