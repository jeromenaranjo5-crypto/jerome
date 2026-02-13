valentine-card/
│
├── index.html
├── style.css
└── script.js
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Valentine's Day 💖</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="card">
        <h1>Happy Valentine's Day!</h1>
        <p id="message">Click the heart to see your surprise ❤️</p>
        <button id="heartBtn">❤️</button>
    </div>
    <script src="script.js"></script>
</body>
</html>
body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background: pink;
    font-family: 'Arial', sans-serif;
}

.card {
    text-align: center;
    background: white;
    padding: 50px;
    border-radius: 20px;
    box-shadow: 0 0 20px rgba(255, 0, 150, 0.3);
}

button {
    font-size: 2rem;
    background: none;
    border: none;
    cursor: pointer;
    animation: beat 1s infinite;
}

@keyframes beat {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.3); }
}
const button = document.getElementById('heartBtn');
const message = document.getElementById('message');

button.addEventListener('click', () => {
    const surprises = [
        "You are amazing! 💖",
        "Sending you lots of love! 🌹",
        "Roses are red, violets are blue… ❤️",
        "You make the world brighter! ✨",
        "Happy Valentine's Day! 💕"
    ];
    const random = Math.floor(Math.random() * surprises.length);
    message.textContent = surprises[random];
});


