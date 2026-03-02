# sistema-solar
solar.html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Sistema Solar</title>

<style>
body {
    margin: 0;
    background: black;
    overflow: hidden;
}

.solar-system {
    position: relative;
    width: 100vw;
    height: 100vh;
}

.sun {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 100px;
    height: 100px;
    background: radial-gradient(circle, yellow, orange, red);
    border-radius: 50%;
    transform: translate(-50%, -50%);
}

.orbit {
    position: absolute;
    top: 50%;
    left: 50%;
    border: 1px solid rgba(255,255,255,0.2);
    border-radius: 50%;
    transform: translate(-50%, -50%);
    animation: rotate linear infinite;
}

.planet {
    position: absolute;
    top: 50%;
    left: 0;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    transform: translate(-50%, -50%);
}

.mercury { width: 150px; height: 150px; animation-duration: 4s; }
.venus   { width: 220px; height: 220px; animation-duration: 7s; }
.earth   { width: 300px; height: 300px; animation-duration: 10s; }
.mars    { width: 380px; height: 380px; animation-duration: 14s; }

.mercury .planet { background: gray; }
.venus   .planet { background: orange; }
.earth   .planet { background: blue; }
.mars    .planet { background: red; }

@keyframes rotate {
    from { transform: translate(-50%, -50%) rotate(0deg); }
    to   { transform: translate(-50%, -50%) rotate(360deg); }
}
</style>
</head>

<body>

<div class="solar-system">

    <div class="sun"></div>

    <div class="orbit mercury">
        <div class="planet"></div>
    </div>

    <div class="orbit venus">
        <div class="planet"></div>
    </div>

    <div class="orbit earth">
        <div class="planet"></div>
    </div>

    <div class="orbit mars">
        <div class="planet"></div>
    </div>

</div>

</body>
</html>
