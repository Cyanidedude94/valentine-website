# valentine-website
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <style>
        body { text-align: center; font-family: Arial, sans-serif; margin-top: 100px; }
        .button { padding: 15px 30px; font-size: 20px; margin: 10px; cursor: pointer; }
        #no { position: absolute; }
    </style>
</head>
<body>
    <h1>Dear Baby Bu, Will You Be My Valentine? ❤️</h1>
    <button class="button" onclick="yesClicked()">Yes</button>
    <button class="button" id="no" onmouseover="moveNo()" onclick="noClicked()">No</button>

    <script>
        function yesClicked() {
            alert("Yay! ❤️ I can't wait!");
            window.location.href = "yes.html";
        }

        function moveNo() {
            let x = Math.random() * window.innerWidth;
            let y = Math.random() * window.innerHeight;
            document.getElementById('no').style.left = `${x}px`;
            document.getElementById('no').style.top = `${y}px`;
        }

        function noClicked() {
            alert("Are you sure bubu? 🥺");
            setTimeout(() => {
                alert("Think again ok... 😢");
                setTimeout(() => {
                    alert("Just say YES Oudrey Bu My Manly Wifey! ❤️");
                }, 1000);
            }, 1000);
        }
    </script>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yay! ❤️</title>
</head>
<body style="text-align: center; font-family: Arial, sans-serif; margin-top: 100px;">
    <h1>Yay! Thank you Baby Buuu !!!!! I'm so happy! 🎉❤️</h1>
    <p>Looking forward to our special day!</p>
    <img src="https://source.unsplash.com/300x200/?love,romance" alt="Love">
</body>
</html>
