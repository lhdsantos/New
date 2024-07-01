<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Resposta Sim ou Não</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
        }
        .container {
            text-align: center;
        }
        .button {
            margin: 20px;
            padding: 10px 20px;
            font-size: 18px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            transition: all 0.3s ease;
        }
        .yes {
            background-color: #4CAF50;
            color: white;
        }
        .no {
            background-color: #f44336;
            color: white;
            position: relative;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Você ama o Henrique?</h1>
        <button class="button yes" onclick="showMessage()">Sim</button>
        <button class="button no" onmouseover="moveButton()">Não</button>
    </div>

    <script>
        function moveButton() {
            const noButton = document.querySelector('.no');
            const container = document.querySelector('.container');
            const containerRect = container.getBoundingClientRect();
            const buttonRect = noButton.getBoundingClientRect();

            const newLeft = Math.random() * (containerRect.width - buttonRect.width);
            const newTop = Math.random() * (containerRect.height - buttonRect.height);

            noButton.style.left = `${newLeft}px`;
            noButton.style.top = `${newTop}px`;
        }

        function showMessage() {
            alert("O aniversário dele está chegando 04/09. Mostre o quanto você ama ele!");
        }
    </script>
</body>
</html>
