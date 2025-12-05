<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Pinturas Interactivas</title>
<style>
    body {
        font-family: Arial, sans-serif;
        background: #e9eef3;
        margin: 0;
        padding: 30px;
    }
    h1 {
        text-align: center;
        margin-bottom: 40px;
    }

    /* CONTENEDOR */
    .painting-container {
        display: flex;
        justify-content: center;
        gap: 40px;
        flex-wrap: wrap;
    }

    /* TARJETAS */
    .painting {
        width: 320px;
        background: white;
        padding: 15px;
        border-radius: 12px;
        box-shadow: 0 0 15px rgba(0,0,0,0.15);
        transition: transform .3s, box-shadow .3s;
        cursor: pointer;
    }

    .painting:hover {
        transform: scale(1.05);
        box-shadow: 0 0 25px rgba(0,0,0,0.25);
    }

    .painting img {
        width: 100%;
        height: auto;
        border-radius: 10px;
    }

    /* INFO OCULTA */
    .info {
        display: none;
        margin-top: 15px;
        background: #f3f7fa;
        padding: 10px;
        border-radius: 8px;
    }
</style>
</head>

<body>

<h1>Pinturas Interactivas</h1>

<div class="painting-container">

    <!-- LA NOCHE ESTRELLADA -->
    <div class="painting" onclick="toggleInfo(1)">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/ef/The_Starry_Night.jpg/640px-The_Starry_Night.jpg" alt="La noche estrellada">
        <h3>La noche estrellada — Vincent van Gogh (1889)</h3>
        <div class="info" id="info1">
            <p><strong>Técnica:</strong> Óleo sobre lienzo</p>
            <p><strong>Ubicación:</strong> Museo de Arte Moderno (MoMA), Nueva York</p>
            <p>Una de las obras más icónicas de Van Gogh, pintada desde la habitación del hospital psiquiátrico de Saint-Rémy. Presenta un cielo turbulento lleno de energía, considerado una representación emocional más que realista del paisaje nocturno.</p>
        </div>
    </div>

    <!-- EL HIJO DEL HOMBRE -->
    <div class="painting" onclick="toggleInfo(2)">
        <img src="https://upload.wikimedia.org/wikipedia/en/0/0c/Magritte_TheSonOfMan.jpg" alt="El hijo del hombre">
        <h3>El hijo del hombre — René Magritte (1964)</h3>
        <div class="info" id="info2">
            <p><strong>Técnica:</strong> Óleo sobre lienzo</p>
            <p><strong>Ubicación:</strong> Colección privada</p>
            <p>Una de las pinturas más reconocibles del surrealismo. Retrata a un hombre con traje y bombín cuyo rostro está oculto por una manzana verde. Magritte indicó que la obra refleja el conflicto entre lo visible y lo oculto.</p>
        </div>
    </div>

</div>

<script>
function toggleInfo(id) {
    const info = document.getElementById("info" + id);
    info.style.display = info.style.display === "block" ? "none" : "block";
}
</script>

</body>
</html>
