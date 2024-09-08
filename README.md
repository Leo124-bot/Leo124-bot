<!DOCTYPE html>
<html>
<head>
  <title>Una sorpresa para ti</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #f0f0f0;
    }
    .carta {
      background-color: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
      margin: 20px auto;
      max-width: 400px;
    }
    button {
      background-color: #4CAF50;
      color: white;
      padding: 15px 32px;
      text-align: center;
      text-decoration: none;
      display: inline-block;
      font-size: 16px;
      margin: 4px 2px;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <div class="carta">
    <h1>¡Te llegó una carta!</h1>
    <p>Abre tu corazón y sigue leyendo...</p>
    <button onclick="mostrarSiguienteCarta()">Continuar</button>
  </div>

  <div class="carta" id="carta2" style="display: none;">
    <h2>¿Recuerdas cuando...?</h2>
    <p>...</p>
    <button onclick="mostrarSiguienteCarta()">Continuar</button>
  </div>

  <div class="carta" id="carta3" style="display: none;">
    <h3>Te quiero porque...</h3>
    <p>...</p>
    <button>¡Fin!</button>
  </div>

  <script>
    function mostrarSiguienteCarta() {
      var cartas = document.getElementsByClassName("carta");
      for (var i = 0; i < cartas.length; i++) {
        cartas[i].style.display = "none";
      }
      var siguienteCarta = event.target.parentNode.nextElementSibling;
      siguienteCarta.style.display = "block";
    }
  </script>

</body>
</html>
