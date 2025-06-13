# lunarline-game

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Lunarline: Love Game</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #ffe6f0, #f0e6ff);
      margin: 0;
      padding: 20px;
      color: #4a4a4a;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    header {
      text-align: center;
      margin-bottom: 30px;
    }
    .logo {
      font-size: 2rem;
      font-weight: bold;
      color: #d63384;
    }
    .card {
      background: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.1);
      width: 90%;
      max-width: 500px;
      margin-bottom: 20px;
    }
    .btn {
      padding: 10px 15px;
      background-color: #d63384;
      color: white;
      border: none;
      border-radius: 5px;
      margin-top: 10px;
      cursor: pointer;
    }
    .input-box {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
    a {
      color: #007bff;
      text-decoration: none;
    }
    a:hover {
      text-decoration: underline;
    }
    footer {
      margin-top: 20px;
      font-size: 0.85rem;
    }
  </style>
</head>
<body>
  <header>
    <div class="logo">💖 E + L Lunarline 💖</div>
    <p>Where romance meets intellect 🌙</p>
  </header>

  <div class="card" id="gameCard">
    <h3>Debate Prompt</h3>
    <p id="prompt">Click below to receive your first romantic debate prompt.</p>
    <button class="btn" onclick="generatePrompt()">💬 Get Prompt</button>
    <input type="text" id="answerBox" placeholder="Type your response..." class="input-box" />
    <button class="btn" onclick="submitAnswer()">📩 Submit Response</button>
  </div>

  <div class="card">
    <h3>Quick Love Actions</h3>
    <p><a href="tel:+256703315266">📞 Call Elijah</a></p>
    <p><a href="tel:+256705008892">📞 Call Lillian</a></p>
    <p><a href="https://wa.me/256703315266">💬 Chat Elijah</a></p>
    <p><a href="https://wa.me/256705008892">💬 Chat Lillian</a></p>
  </div>

  <footer>
    Made with 🌹 for Senabulya Elijah Kintu & Katungi Lillian — “My Heart’s Lunar Love” & “My Lifeline”
  </footer>

  <script>
    const prompts = [
      "If love is a battlefield, how do we win without hurting each other?",
      "Does feminism strengthen or threaten romantic love?",
      "In your words, what does it mean to be emotionally intelligent in a relationship?",
      "Would you rather be understood or adored — and why?",
      "What principle would you never compromise on in love?"
    ];

    function generatePrompt() {
      const prompt = prompts[Math.floor(Math.random() * prompts.length)];
      document.getElementById("prompt").textContent = prompt;
    }

    function submitAnswer() {
      const answer = document.getElementById("answerBox").value;
      if (answer.trim() === "") {
        alert("Please type a response first.");
        return;
      }
      alert("Your poetic response has been sent! 🌹");
      document.getElementById("answerBox").value = "";
    }
  </script>
</body>
</html>
