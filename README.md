# My-Love
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <style>
        body {
            background-color: pink;
            text-align: center;
            font-family: 'Arial', sans-serif;
            color: white;
        }
        h1 {
            margin-top: 50px;
            font-size: 2.5em;
        }
        .heart {
            color: red;
            font-size: 50px;
            animation: heartbeat 1s infinite;
        }
        @keyframes heartbeat {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }
        .container {
            max-width: 600px;
            margin: auto;
            background: rgba(255, 182, 193, 0.8);
            padding: 20px;
            border-radius: 20px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
        }
        .buttons {
            margin-top: 30px;
            position: relative;
        }
        button {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
        }
        .yes-btn {
            background-color: red;
            color: white;
        }
        .yes-btn:hover {
            background-color: darkred;
        }
        .no-btn {
            background-color: white;
            color: red;
            border: 2px solid red;
        }
        .no-btn:hover {
            background-color: lightpink;
        }
        .hidden {
            display: none;
            margin-top: 20px;
            font-size: 1.5em;
        }
        img {
            max-width: 100%;
            border-radius: 10px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Will You Be My Valentine? <span class="heart">❤️</span></h1>
        <img src="H&S.jpg" alt="Cute photo of us">
        <p>From the moment we met, you’ve made my heart skip a beat. You bring so much joy and love into my life! 🌸</p>
        <p>So, will you be my Valentine? 💕</p>
        <div class="buttons">
            <button class="yes-btn" onclick="showMessage()">Yes!</button>
            <button class="no-btn" onclick="spawnMoreYesButtons()">No 😢</button>
        </div>
        <div id="message" class="hidden">
            <p>Yay! You just made me the happiest person ever! 💖🥰</p>
            <img src="S&H.jpg" alt="Another cute memory together">
        </div>
    </div>
    <script>
        function showMessage() {
            document.getElementById('message').style.display = 'block';
        }
        
        function spawnMoreYesButtons() {
            let buttonsContainer = document.querySelector('.buttons');
            let newButton = document.createElement('button');
            newButton.classList.add('yes-btn');
            newButton.innerText = 'Yes!';
            newButton.onclick = showMessage;
            buttonsContainer.appendChild(newButton);
        }
    </script>
</body>
</html>
