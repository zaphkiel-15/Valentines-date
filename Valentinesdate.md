# Valentines-date
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Be My Valentine?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #ffe6e6;
            color: #d63384;
            padding: 50px;
        }
        .container {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            display: inline-block;
        }
        h1 {
            font-size: 2.5em;
        }
        p {
            font-size: 1.2em;
        }
        .buttons {
            margin-top: 20px;
        }
        button {
            font-size: 1.2em;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .yes {
            background-color: #ff4d4d;
            color: white;
        }
        .no {
            background-color: #ccc;
            color: black;
        }
        .no:hover {
            position: absolute;
            top: random(10vw);
            left: random(10vw);
        }
    </style>
    <script>
        function sayYes() {
            document.getElementById("question").innerHTML = "Yay! I can't wait!";
            document.getElementById("buttons").style.display = "none";
        }
        function moveNo(btn) {
            btn.style.position = "absolute";
            btn.style.top = Math.random() * window.innerHeight + "px";
            btn.style.left = Math.random() * window.innerWidth + "px";
        }
    </script>
</head>
<body>
    <div class="container">
        <h1 id="question">Will you be my Valentine? ❤️</h1>
        <div class="buttons" id="buttons">
            <button class="yes" onclick="sayYes()">Yes!</button>
            <button class="no" onmouseover="moveNo(this)">No</button>
        </div>
    </div>
</body>
</html>
