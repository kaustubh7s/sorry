<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>I'm Sorry 😔</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to top right, #ffd1dc, #fff0f5);
      overflow: hidden;
      height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
    }

    h1 {
      font-size: 2.8em;
      color: #ff4b5c;
      margin: 0.3em 0;
    }

    p {
      font-size: 1.5em;
      color: #444;
      max-width: 600px;
    }

    .cat {
      font-size: 5em;
      animation: wave 2s infinite alternate;
      margin-top: 1em;
    }

    @keyframes wave {
      0% { transform: rotate(0deg); }
      50% { transform: rotate(15deg); }
      100% { transform: rotate(-15deg); }
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(45deg);
      animation: float 6s linear infinite;
    }

    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      left: -10px;
      top: 0;
    }

    @keyframes float {
      0% {
        bottom: -20px;
        opacity: 0;
      }
      50% {
        opacity: 1;
      }
      100% {
        bottom: 100%;
        opacity: 0;
      }
    }

    .star {
      position: absolute;
      color: #fffacd;
      font-size: 1.2em;
      animation: twinkle 2s infinite ease-in-out alternate;
    }

    @keyframes twinkle {
      0% { opacity: 0.3; transform: scale(1); }
      100% { opacity: 1; transform: scale(1.5); }
    }

    .sorry-button {
      margin-top: 30px;
      padding: 15px 30px;
      background-color: #ffb6c1;
      border: none;
      border-radius: 30px;
      font-size: 1.2em;
      color: #fff;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }

    .sorry-button:hover {
      background-color: #ff4b5c;
    }

    .milk-bottle {
      font-size: 7em;
      display: none;
      margin-top: 30px;
      animation: pop 1s ease-out;
    }

    @keyframes pop {
      0% {
        transform: scale(0);
        opacity: 0;
      }
      100% {
        transform: scale(1);
        opacity: 1;
      }
    }
  </style>
</head>
<body>

  <h1>Mine duduuuuuuuuuuu baby girl 💖</h1>
  <p>I'm really sorry 😔 I never meant to upset you.<br>You mean the world to me — please forgive me 🥺</p>

  <div class="cat">🐱</div>

  <button class="sorry-button" onclick="showMilk()">Touch me if you forgive 🥺</button>

  <div id="milk" class="milk-bottle">🍼</div>

  <!-- Floating hearts -->
  <script>
    for (let i = 0; i < 15; i++) {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (3 + Math.random() * 3) + "s";
      document.body.appendChild(heart);
    }

    // Twinkling stars
    for (let i = 0; i < 30; i++) {
      const star = document.createElement("div");
      star.className = "star";
      star.innerHTML = "★";
      star.style.top = Math.random() * 100 + "vh";
      star.style.left = Math.random() * 100 + "vw";
      star.style.animationDelay = (Math.random() * 2) + "s";
      document.body.appendChild(star);
    }

    // Show milk bottle
    function showMilk() {
      const milk = document.getElementById('milk');
      milk.style.display = 'block';
    }
  </script>
</body>
</html>
