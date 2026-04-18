<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Birthday 🎂</title>

<style>
body {
    margin: 0;
    background: linear-gradient(45deg, #ff9a9e, #fad0c4);
    font-family: Arial;
    text-align: center;
    overflow: hidden;
}

h1 {
    margin-top: 80px;
    font-size: 45px;
    color: white;
    animation: glow 2s infinite alternate;
}

@keyframes glow {
    from { text-shadow: 0 0 10px white; }
    to { text-shadow: 0 0 25px yellow; }
}

#text {
    font-size: 22px;
    color: white;
    margin-top: 20px;
}

button {
    margin-top: 30px;
    padding: 12px 25px;
    border: none;
    border-radius: 20px;
    background: #ff4081;
    color: white;
    font-size: 18px;
    cursor: pointer;
}

button:hover {
    background: #e91e63;
}

/* floating hearts */
.heart {
    position: absolute;
    color: red;
    animation: float 5s linear infinite;
}

@keyframes float {
    0% { transform: translateY(0); opacity:1; }
    100% { transform: translateY(-800px); opacity:0; }
}
</style>
</head>

<body>

<h1>🎉 Happy Birthday Musfira 🎉</h1>

<div id="text"></div>

<button onclick="surprise()">Click Me 🎁</button>

<script>
// typing effect
let msg = "💖 You are special, amazing and beautiful. Stay happy always 🌸✨";
let i = 0;

function typing() {
    if (i < msg.length) {
        document.getElementById("text").innerHTML += msg.charAt(i);
        i++;
        setTimeout(typing, 40);
    }
}
typing();

// floating hearts
function createHeart() {
    let heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = Math.random() * 20 + 20 + "px";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 5000);
}
setInterval(createHeart, 300);

// surprise button
function surprise() {
    alert("🎂 Happiest Birthday Musfira 💖✨\nStay blessed always!");
}
</script>

</body>
</html>
