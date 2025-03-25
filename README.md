<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ти мене любиш?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }

        .button-container {
            margin-top: 20px;
        }

        .yes-button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
        }

        .no-button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            position: absolute;
        }

        .message {
            margin-top: 20px;
            font-size: 18px;
            font-weight: bold;
            color: green;
        }
    </style>
</head>
<body>
    <h1>Ти мене любиш?</h1>
    <div class="button-container">
        <button class="yes-button" onclick="showMessage()">Так</button>
        <button class="no-button" onmouseover="moveButton()">Ні</button>
    </div>
    <div class="message" id="message"></div>

    <script>
        function showMessage() {
            document.getElementById('message').textContent = 'Молодець!';
        }

        function moveButton() {
            const button = document.querySelector('.no-button');
            const x = Math.random() * (window.innerWidth - button.offsetWidth);
            const y = Math.random() * (window.innerHeight - button.offsetHeight);
            button.style.left = `${x}px`;
            button.style.top = `${y}px`;
        }
    </script>
</body>
</html>
