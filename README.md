# laxscookies-design.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A Very Important Question</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            background-color: #ffebee;
            font-family: 'Arial', sans-serif;
            overflow: hidden;
            text-align: center;
        }
        h1 { color: #d32f2f; margin-bottom: 20px; }
        .date { font-weight: bold; color: #c2185b; font-size: 1.2rem; }
        .btn-container { position: relative; width: 300px; height: 100px; margin-top: 30px; }
        button {
            padding: 15px 30px;
            font-size: 1.2rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: transform 0.2s;
        }
        #yesBtn { background-color: #4caf50; color: white; position: absolute; left: 0; }
        #noBtn { background-color: #f44336; color: white; position: absolute; right: 0; transition: 0.1s ease; }
        .gif { width: 200px; margin-bottom: 20px; border-radius: 10px; }
    </style>
</head>
<body>

    <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExOHp4Zmt1Y3R4Y3R4Y3R4Y3R4Y3R4Y3R4Y3R4Y3R4Y3R4Y3R4JmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1n/c76IJLufpNUMo/giphy.gif" alt="Cute Cat" class="gif">
    
    <h1>Will you be my Valentine?</h1>
    <p class="date">Save the date: Friday, February 13, 2026</p>

    <div class="btn-container">
        <button id="yesBtn" onclick="celebrate()">YES!</button>
        <button id="noBtn" onmouseover="moveButton()" onclick="moveButton()">NO</button>
    </div>

    <script>
        function moveButton() {
            const noBtn = document.getElementById('noBtn');
            const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
            const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
            
            noBtn.style.position = 'fixed';
            noBtn.style.left = x + 'px';
            noBtn.style.top = y + 'px';
        }

        function celebrate() {
            document.body.innerHTML = `
                <h1 style="color: #d32f2f;">Yay! ❤️</h1>
                <p>I knew you'd say yes! (You didn't really have a choice.)</p>
                <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExOHp4Zmt1Y3R4Y3R4Y3R4Y3R4Y3R4Y3R4Y3R4Y3R4Y3R4JmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1n/l41lTfuxV6mYk5Oxi/giphy.gif" width="300">
                <h2>See you on February 13th!</h2>
            `;
        }
    </script>
</body>
</html>
