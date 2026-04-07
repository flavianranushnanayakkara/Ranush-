<!DOCTYPE html>
<html>
<head>
    <title>Ranush Nanayakkara</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            text-align: center;
            background: linear-gradient(to right, #4facfe, #00f2fe);
            color: white;
        }
        h1 {
            font-size: 50px;
            margin-top: 50px;
        }
        h2 {
            font-size: 35px;
            margin-top: 40px;
        }
        p {
            font-size: 20px;
            max-width: 600px;
            margin: 10px auto;
        }
        img {
            margin: 10px;
            border-radius: 10px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            border: none;
            background-color: white;
            color: black;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: lightgray;
        }
        .about {
            background-color: rgba(0,0,0,0.3);
            padding: 20px;
            border-radius: 10px;
            display: inline-block;
        }
    </style>
</head>

<body>

    <h1>Ranush Nanayakkara</h1>
    <p>Welcome to my personal website! 😎</p>

    <!-- About Me Section -->
    <h2>About Me</h2>
    <div class="about">
        <p>Hi! I am Ranush Nanayakkara. I love learning new things, creating websites, and exploring technology. I enjoy coding, adding photos, and making my website more interactive. This website is a place where I share a little about myself.</p>
    </div>

    <!-- Photos Section -->
    <h2>My Photos 📸</h2>
    <img src="photo1.jpg" width="200" alt="Photo 1">
    <img src="photo2.jpg" width="200" alt="Photo 2">

    <br><br>

    <!-- Button -->
    <button onclick="showMessage()">Click Me</button>
    <p id="msg"></p>

    <script>
        function showMessage() {
            document.getElementById("msg").innerHTML = "Thanks for visiting my website! 🚀";
        }
    </script>

</body>
</html>
