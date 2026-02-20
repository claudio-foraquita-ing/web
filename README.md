<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ID CLAUDIO FORAQUITA</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600&display=swap" rel="stylesheet">
    <style>
        body { background-color: #0d0f12; color: #d1d5db; font-family: sans-serif; display: flex; justify-content: center; padding-top: 20px; margin: 0; }
        .container { text-align: center; width: 340px; }
        #clock { font-family: 'Orbitron', sans-serif; font-size: 3.2rem; color: #ffffff; margin-bottom: 15px; line-height: 1.2; }
        .photo-container { width: 220px; height: 280px; margin: 0 auto 20px; border: 1px solid #374151; border-radius: 8px; position: relative; overflow: hidden; background: #1a1c20; }
        .photo-container img { width: 100%; height: 100%; object-fit: cover; }
        .scanner-line { position: absolute; width: 100%; height: 2px; background: #ffffff; box-shadow: 0 0 15px #ffffff; animation: scan 3.5s infinite ease-in-out; z-index: 10; }
        .name { font-weight: bold; font-size: 1.2rem; color: #ffffff; text-transform: uppercase; margin-top: 10px; }
        @keyframes scan { 0%, 100% {top: 0;} 50% {top: 100%;} }
    </style>
</head>
<body>
<div class="container">
    <div id="clock">00:00</div>
    <div class="photo-container">
        <div class="scanner-line"></div>
        <img src="Claudio_Foraquita.png" alt="ID PHOTO">
    </div>
    <div class="name">CLAUDIO FORAQUITA</div>
    <div style="font-size: 0.95rem; margin-top: 5px;">REG. CIP: 114389</div>
    <div style="font-weight: bold; color: #9ca3af; margin-top: 5px;">INGENIERO ELECTRÓNICO</div>
    <div style="margin-top: 50px; font-size: 0.8rem; color: #4b5563; border-top: 1px solid #1f2937; padding-top: 10px;">
        19/02/2026<br>ILO, PERÚ - 22°C DESPEJADO ☀️
    </div>
</div>
<script>
    function update() {
        const n = new Date();
        const h = n.getHours();
        const m = n.getMinutes().toString().padStart(2, '0');
        const p = h >= 12 ? 'PM' : 'AM';
        const h12 = (h % 12 || 12).toString().padStart(2, '0');
        document.getElementById('clock').innerHTML = h12 + ":" + m + "<br><span style='font-size:1.2rem'>" + p + "</span>";
    }
    setInterval(update, 1000); update();
</script>
</body>
</html>
