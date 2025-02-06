<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <style>
        body { 
            text-align: center; 
            font-family: 'Arial', sans-serif; 
            margin-top: 100px;
            background: url('https://source.unsplash.com/1920x1080/?love,hearts') no-repeat center center/cover;
            color: white;
        }
        h1 {
            font-size: 2.5em;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        .button {
            padding: 15px 30px; 
            font-size: 20px; 
            border: none; 
            border-radius: 10px;
            margin: 10px; 
            cursor: pointer;
            transition: 0.3s ease-in-out;
        }
        .yes { background-color: #ff4081; color: white; }
        .yes:hover { background-color: #e91e63; transform: scale(1.1); }
        .no { background-color: #f44336; color: white; position: absolute; }
        
        /* Heart Animation */
        @keyframes heartbeat {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }
        .heart {
            font-size: 50px;
            display: inline-block;
            animation: heartbeat 1s infinite;
        }
    </style>
</head>
<body>
    <h1>Will You Be My Valentine? ❤️</h1>
    <span class="heart">💖</span>
    <br>
    <button class="button yes" onclick="yesClicked()">Yes</button>
    <button class="button no" id="no" onmouseover="moveNo()" onclick="noClicked()">No</button>

    <script>
        function yesClicked() {
            alert("Yay! ❤️ I can't wait!");
            window.location.href = "yes.html";
        }

        function moveNo() {
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 50);
            document.getElementById('no').style.left = `${x}px`;
            document.getElementById('no').style.top = `${y}px`;
        }

        function noClicked() {
            alert("Are you sure? 🥺");
            setTimeout(() => {
                alert("Think again... 😢");
                setTimeout(() => {
                    alert("Just say YES! ❤️");
                }, 1000);
            }, 1000);
        }
    </script>
</body>
</html>
