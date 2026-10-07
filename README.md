<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Jake M. — Best Boss Ever</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
      min-height: 100vh;
      color: white;
      text-align: center;
      overflow-x: hidden;
      background: linear-gradient(135deg, #08001f, #24005c, #001f4d);
      background-size: 400% 400%;
      animation: backgroundMove 10s ease infinite;
    }

    @keyframes backgroundMove {
      0% {
        background-position: 0% 50%;
      }

      50% {
        background-position: 100% 50%;
      }

      100% {
        background-position: 0% 50%;
      }
    }

    .container {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 30px;
    }

    .trophy {
      font-size: 100px;
      animation: bounce 1.5s infinite;
      filter: drop-shadow(0 0 20px gold);
    }

    @keyframes bounce {
      0%, 100% {
        transform: translateY(0) rotate(-3deg);
      }

      50% {
        transform: translateY(-18px) rotate(3deg);
      }
    }

    h1 {
      font-size: clamp(45px, 10vw, 90px);
      color: #ffd700;
      text-shadow:
        0 0 10px #ffd700,
        0 0 30px #ff9d00,
        0 0 60px #ff6600;
      margin: 10px 0;
    }

    .subtitle {
      font-size: clamp(22px, 5vw, 40px);
      font-weight: bold;
      margin-bottom: 30px;
    }

    .card {
      max-width: 700px;
      width: 100%;
      padding: 35px;
      border-radius: 25px;
      background: rgba(255, 255, 255, 0.12);
      border: 2px solid rgba(255, 215, 0, 0.6);
      box-shadow: 0 0 40px rgba(255, 215, 0, 0.25);
      backdrop-filter: blur(10px);
    }

    .card h2 {
      color: #ffd700;
      font-size: 32px;
      margin-bottom: 25px;
    }

    .reasons {
      display: grid;
      gap: 15px;
      margin-bottom: 30px;
    }

    .reason {
      padding: 15px;
      border-radius: 15px;
      background: rgba(0, 0, 0, 0.25);
      font-size: 20px;
      transition: transform 0.3s, background 0.3s;
    }

    .reason:hover {
      transform: scale(1.05);
      background: rgba(255, 215, 0, 0.2);
    }

    button {
      border: none;
      padding: 16px 30px;
      border-radius: 50px;
      background: linear-gradient(90deg, #ffd700, #ff8c00);
      color: #241000;
      font-size: 20px;
      font-weight: bold;
      cursor: pointer;
      box-shadow: 0 0 25px rgba(255, 215, 0, 0.6);
      transition: transform 0.2s;
    }

    button:hover {
      transform: scale(1.08);
    }

    #message {
      margin-top: 25px;
      min-height: 30px;
      font-size: 24px;
      font-weight: bold;
      color: #ffd700;
    }

    .footer {
      margin-top: 35px;
      opacity: 0.7;
      font-size: 14px;
    }

    .confetti {
      position: fixed;
      top: -20px;
      font-size: 25px;
      animation: fall linear forwards;
      pointer-events: none;
    }

    @keyframes fall {
      to {
        transform: translateY(110vh) rotate(720deg);
      }
    }
  </style>
</head>

<body>

  <div class="container">

    <div class="trophy">🏆</div>

    <h1>JAKE M.</h1>

    <div class="subtitle">
      THE BEST BOSS EVER!
    </div>

    <div class="card">

      <h2>⭐ Official Boss Rating ⭐</h2>

      <div class="reasons">

        <div class="reason">
          👑 Great leader
        </div>

        <div class="reason">
          💪 Always has our back
        </div>

        <div class="reason">
          🔥 Maximum boss energy
        </div>

        <div class="reason">
          😎 Somehow makes being a boss look easy
        </div>

        <div class="reason">
          🏆 Absolutely deserves the #1 spot
        </div>

      </div>

      <button onclick="celebrate()">
        🎉 PROVE JAKE IS THE BEST 🎉
      </button>

      <div id="message"></div>

    </div>

    <div class="footer">
      © Official Jake M. Best Boss Committee
    </div>

  </div>

  <script>
    function celebrate() {
      document.getElementById("message").textContent =
        "🚨 SCIENTIFICALLY CONFIRMED: JAKE M. IS THE BEST BOSS! 🚨";

      const emojis = ["🎉", "⭐", "🏆", "🔥", "👑", "😎"];

      for (let i = 0; i < 60; i++) {
        const confetti = document.createElement("div");

        confetti.className = "confetti";

        confetti.textContent =
          emojis[Math.floor(Math.random() * emojis.length)];

        confetti.style.left =
          Math.random() * 100 + "vw";

        confetti.style.animationDuration =
          (Math.random() * 3 + 2) + "s";

        document.body.appendChild(confetti);

        setTimeout(() => {
          confetti.remove();
        }, 5000);
      }
    }
  </script>

</body>
</html>