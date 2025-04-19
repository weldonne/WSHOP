OCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ma Déclaration d'Amour</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background: linear-gradient(45deg, #ff1493, #ff69b4);
            font-family: 'Arial', sans-serif;
            color: white;
            text-align: center;
        }

        .container {
            max-width: 800px;
            padding: 20px;
        }

        h1 {
            font-size: 3em;
            margin-bottom: 30px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .message {
            font-size: 1.5em;
            line-height: 1.6;
            background: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 15px;
            backdrop-filter: blur(5px);
            margin: 20px;
            display: none;
        }

        button {
            padding: 15px 40px;
            font-size: 1.2em;
            background: white;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            transition: transform 0.3s ease;
            margin-top: 20px;
        }

        button:hover {
            transform: scale(1.1);
        }

        .signature {
            margin-top: 40px;
            font-size: 2em;
            font-style: italic;
        }

        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0px); }
        }

        .heart {
            font-size: 4em;
            animation: float 3s ease-in-out infinite;
            margin-bottom: 30px;
        }
    </style>
</head>
<body>
    <div class="heart">❤️</div>
    <div class="container">
        <h1>Mon ❤️ s'adresse à toi...</h1>
        <button onclick="revealMessage()">Clique pour découvrir le message</button>
        <div class="message" id="secretMessage">
            <p>Depuis que tu es entré(e) dans ma vie, chaque instant prend un sens nouveau.<br><br>
            Ton sourire est mon soleil, ta voix ma mélodie préférée.<br><br>
            Je n'ose imaginer un futur sans toi à mes côtés.<br><br>
            Acceptes-tu de partager cette aventure avec moi ?</p>
            <div class="signature">ESTELLE🌹</div>
        </div>
    </div>

    <script>
        function revealMessage() {
            document.getElementById('secretMessage').style.display = 'block';
            document.querySelector('button').style.display = 'none';
            document.querySelector('.heart').innerHTML = '💌';
            
            // Ajout de confettis
            for(let i = 0; i < 50; i++) {
                let confetti = document.createElement('div');
                confetti.innerHTML = ['❤️', '💖', '💕', '🌸', '🎉'][Math.floor(Math.random() * 5)];
                confetti.style.position = 'fixed';
                confetti.style.left = Math.random() * 100 + 'vw';
                confetti.style.animation = `float ${2 + Math.random() * 3}s infinite`;
                document.body.appendChild(confetti);
            }
        }
    </script>
</body>
</html>
