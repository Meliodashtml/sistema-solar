<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Sistema Solar 2.0</title>

<style>
body {
    margin: 0;
    background: black;
    overflow: hidden;
}

/* ESTRELAS */
body::after {
    content: "";
    position: absolute;
    width: 2px;
    height: 2px;
    background: white;
    box-shadow:
        100px 200px white,
        300px 400px white,
        600px 150px white,
        800px 300px white,
        1200px 500px white,
        500px 700px white,
        900px 100px white;
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
    width: 120px;
    height: 120px;
    background: radial-gradient(circle, yellow, orange, red);
    border-radius: 50%;
    transform: translate(-50%, -50%);
    box-shadow: 0 0 60px orange;
}

/* ÓRBITAS */
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

/* PLANETAS */
.mercury { width: 160px; height: 160px; animation-duration: 4s; }
.venus   { width: 240px; height: 240px; animation-duration: 7s; }
.earth   { width: 340px; height: 340px; animation-duration: 10s; }
.mars    { width: 440px; height: 440px; animation-duration: 14s; }
.jupiter { width: 600px; height: 600px; animation-duration: 20s; }

.mercury .planet { background: gray; }
.venus   .planet { background: orange; }
.earth   .planet { background: blue; }
.mars    .planet { background: red; }
.jupiter .planet { background: brown; width: 30px; height: 30px; }

/* LUA */
.moon-orbit {
    position: absolute;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    animation: rotate 3s linear infinite;
}

.moon {
    position: absolute;
    width: 8px;
    height: 8px;
    background: white;
    border-radius: 50%;
    top: 50%;
    left: 0;
    transform: translate(-50%, -50%);
}

/* ANIMAÇÃO */
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
        <div class="planet">
            <div class="moon-orbit">
                <div class="moon"></div>
            </div>
        </div>
    </div>

    <div class="orbit mars">
        <div class="planet"></div>
    </div>

    <div class="orbit jupiter">
        <div class="planet"></div>
    </div>

</div>

</body>
</html>
