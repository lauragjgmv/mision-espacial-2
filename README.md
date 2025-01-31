# mision-espacial-2
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Diseña tu Misión Espacial</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #0a0a23;
            color: white;
        }
        .container {
            width: 80%;
            margin: auto;
            background: #1a1a2e;
            padding: 20px;
            border-radius: 10px;
        }
        select {
            padding: 10px;
            margin: 10px;
            font-size: 16px;
            border-radius: 5px;
        }
        button {
            padding: 12px 20px;
            font-size: 18px;
            border: none;
            background: #007BFF;
            color: white;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background: #0056b3;
        }
        #resultado {
            margin-top: 20px;
            font-size: 18px;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>🚀 Diseña tu Misión Espacial 🌍</h1>
        <p>Selecciona el destino, la nave y la tripulación para tu expedición.</p>

        <label for="destino">🌌 Elige tu destino:</label>
        <select id="destino">
            <option value="Luna">Luna</option>
            <option value="Marte">Marte</option>
            <option value="Órbita Terrestre">Órbita Terrestre</option>
        </select>

        <label for="nave">🚀 Elige tu nave:</label>
        <select id="nave">
            <option value="Módulo Lunar">Módulo Lunar</option>
            <option value="Cohete Tripulado">Cohete Tripulado</option>
            <option value="Módulo Orbital">Módulo Orbital</option>
        </select>

        <label for="tripulacion">👨‍🚀 Elige tu tripulación:</label>
        <select id="tripulacion">
            <option value="Astronautas">Astronautas</option>
            <option value="Científicos">Científicos</option>
            <option value="Robots Autónomos">Robots Autónomos</option>
        </select>

        <br><br>
        <button onclick="validarMision()">🚀 Lanzar Misión</button>

        <p id="resultado"></p>
    </div>

    <script>
        function validarMision() {
            let destino = document.getElementById("destino").value;
            let nave = document.getElementById("nave").value;
            let tripulacion = document.getElementById("tripulacion").value;
            let resultado = document.getElementById("resultado");

            if ((destino === "Luna" && nave === "Módulo Lunar" && tripulacion === "Astronautas") ||
                (destino === "Marte" && nave === "Cohete Tripulado" && tripulacion === "Científicos") ||
                (destino === "Órbita Terrestre" && nave === "Módulo Orbital" && tripulacion === "Robots Autónomos")) {
                resultado.innerHTML = "✅ ¡Misión exitosa! Has seleccionado la combinación correcta.";
                resultado.style.color = "lightgreen";
            } else {
                resultado.innerHTML = "❌ Misión fallida. Revisa que la nave y la tripulación sean adecuadas para el destino.";
                resultado.style.color = "red";
            }
        }
    </script>

</body>
</html>
