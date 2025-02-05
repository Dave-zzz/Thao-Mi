# Thao-Mi
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentinstags-Anfrage</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #ffcccb;
            margin: 0;
            padding: 0;
            overflow: hidden;
        }
        h1 {
            text-align: center;
            color: #ff3366;
            font-size: 3em;
            margin-top: 20%;
        }
        p {
            text-align: center;
            font-size: 1.5em;
            color: #ff6699;
            margin-top: 20px;
        }
        .heart {
            position: absolute;
            width: 30px;
            height: 30px;
            background-color: #ff3366;
            clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
            animation: heartAnimation 5s infinite;
        }
        @keyframes heartAnimation {
            0% {
                top: 100%;
                left: 0;
                transform: scale(1) rotate(0);
            }
            50% {
                top: 10%;
                left: 50%;
                transform: scale(1.2) rotate(45deg);
            }
            100% {
                top: 100%;
                left: 100%;
                transform: scale(1) rotate(0);
            }
        }
        .heart:nth-child(odd) {
            animation-duration: 6s;
        }
        .heart:nth-child(even) {
            animation-duration: 7s;
        }
    </style>
</head>
<body>
    <h1>Liebst du mich, Thao Mi?</h1>
    <p>Würdest du mit mir ein Date am Valentinstag verbringen?</p>
    
    <!-- Herzen hinzufügen -->
    <div class="heart" style="animation-delay: 0s;"></div>
    <div class="heart" style="animation-delay: 1s;"></div>
    <div class="heart" style="animation-delay: 2s;"></div>
    <div class="heart" style="animation-delay: 3s;"></div>
    <div class="heart" style="animation-delay: 4s;"></div>

    <script>
        // Zufällige Positionierung der Herzen
        const hearts = document.querySelectorAll('.heart');
        hearts.forEach(heart => {
            heart.style.left = `${Math.random() * 100}%`;
            heart.style.animationDuration = `${Math.random() * (7 - 5) + 5}s`;
        });
    </script>
</body>
</html>
