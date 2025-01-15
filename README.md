<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Spinning Cube</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
        }

        .cube {
            position: relative;
            width: 100px;
            height: 100px;
            transform-style: preserve-3d;
            animation: rotate 5s infinite linear;
        }

        .cube div {
            position: absolute;
            width: 100px;
            height: 100px;
            background: rgba(0, 150, 255, 0.8);
            border: 1px solid #000;
        }

        /* Position the sides of the cube */
        .front { transform: translateZ(50px); }
        .back { transform: rotateY(180deg) translateZ(50px); }
        .right { transform: rotateY(90deg) translateZ(50px); }
        .left { transform: rotateY(-90deg) translateZ(50px); }
        .top { transform: rotateX(90deg) translateZ(50px); }
        .bottom { transform: rotateX(-90deg) translateZ(50px); }

        @keyframes rotate {
            from {
                transform: rotateX(0) rotateY(0);
            }
            to {
                transform: rotateX(360deg) rotateY(360deg);
            }
        }
    </style>
</head>
<body>
    <div class="cube">
        <div class="front"></div>
        <div class="back"></div>
        <div class="right"></div>
        <div class="left"></div>
        <div class="top"></div>
        <div class="bottom"></div>
    </div>
</body>
</html>
