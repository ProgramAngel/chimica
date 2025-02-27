<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>24 a Chimica Organica - Celebrazione Epica!</title>
    <style>
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #1e3c72, #2a5298, #a1c4fd);
            height: 100vh;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #fff;
        }
        .container {
            text-align: center;
            z-index: 1;
        }
        h1 {
            font-size: 4rem;
            text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.3);
            animation: bounce 2s infinite;
        }
        p {
            font-size: 1.5rem;
            margin: 20px 0;
            animation: fadeIn 3s ease-in;
        }
        .chem-icon {
            font-size: 3rem;
            animation: spin 4s linear infinite;
        }
        .confetti {
            position: absolute;
            width: 10px;
            height: 10px;
            background: #fff;
            border-radius: 50%;
            animation: fall 5s linear infinite;
        }
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-30px); }
            60% { transform: translateY(-15px); }
        }
        @keyframes fadeIn {
            0% { opacity: 0; }
            100% { opacity: 1; }
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        @keyframes fall {
            0% { transform: translateY(-100vh) rotate(0deg); opacity: 1; }
            100% { transform: translateY(100vh) rotate(720deg); opacity: 0; }
        }
        .btn {
            padding: 15px 30px;
            font-size: 1.2rem;
            background: #fff;
            color: #2a5298;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .btn:hover {
            transform: scale(1.1);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>24 a Chimica Organica!</h1>
        <p>Ce l’ho fatta, sono un genio delle molecole! 🎉</p>
        <div class="chem-icon">🧪</div>
        <button class="btn" onclick="moreConfetti()">Più coriandoli!</button>
    </div>

    <script>
        function createConfetti() {
            const confetti = document.createElement('div');
            confetti.className = 'confetti';
            confetti.style.left = Math.random() * 100 + 'vw';
            confetti.style.background = `hsl(${Math.random() * 360}, 70%, 50%)`;
            confetti.style.animationDuration = (Math.random() * 3 + 2) + 's';
            document.body.appendChild(confetti);
            setTimeout(() => confetti.remove(), 5000);
        }

        // Genera coriandoli all'avvio
        for (let i = 0; i < 50; i++) {
            setTimeout(createConfetti, i * 100);
        }

        // Più coriandoli al click
        function moreConfetti() {
            for (let i = 0; i < 30; i++) {
                setTimeout(createConfetti, i * 50);
            }
        }
    </script>
</body>
</html>
