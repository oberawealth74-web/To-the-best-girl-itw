<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Be My Valentine ❤️</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      overflow: hidden;
      text-align: center;
    }
    .card {
      background: white;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
      max-width: 420px;
      width: 90%;
      position: relative;
      z-index: 2;
    }
    h1 {
      color: #e63946;
    }
    p {
      font-size: 1.1em;
    }
    button {
      padding: 12px 20px;
      margin: 10px;
      border: none;
      border-radius: 30px;
      font-size: 1em;
      cursor: pointer;
      transition: transform 0.2s;
      position: relative;
    }
    button:hover {
      transform: scale(1.05);
    }
    .yes {
      background-color: #e63946;
      color: white;
    }
    .no {
      background-color: #ccc;
    }
    .heart {
      position: absolute;
      color: #e63946;
      font-size: 20px;
      animation: float 6s linear infinite;
      opacity: 0.7;
    }
    @keyframes float {
      from { transform: translateY(100vh) scale(1); }
      to { transform: translateY(-10vh) scale(1.5); }
    }
    img {
      display: block;
      margin: 15px auto;
      border-radius: 20px;
      max-width: 100%;
    }
    .jumping-puppy {
      animation: jump 1s infinite alternate;
    }
    @keyframes jump {
      from { transform: translateY(0); }
      to { transform: translateY(-30px); }
    }
  </style>
</head>
<body>  <!-- Music controls -->  <audio id="music" autoplay loop controls>
    <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_58c2b7a4f6.mp3?filename=romantic-love-story-112194.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>  <div class="card" id="content">
    <h1>Hey My Love ❤️</h1>
    <p>Leila, I love you so much and you make every day brighter for me. You mean the world to me, and I cherish you more than words can express.</p>
    <!-- Puppy image holding a heart -->
    <img src="https://i.imgur.com/yourPuppyImage.png" alt="Cute Puppy with Heart" style="width:150px;">
    <p>Will you be my Valentine?</p>
    <button class="yes" onclick="sayYes()">Yes 💖</button>
    <button class="no" id="noBtn" onclick="moveNo()">No 🙈</button>
  </div>  <script>
    function sayYes() {
      document.getElementById('content').innerHTML = `
        <h1>Thank You, My Valentine 💕</h1>
        <p>
          Thank you for saying yes, my love ❤️<br><br>
          You mean more to me than words can explain. Your smile, your laugh, your warmth, and your heart fill my world with joy and happiness every single day. I feel so incredibly lucky to have you by my side. Every moment with you feels like a beautiful dream, and I cherish every second we spend together. I promise to always support you, make you smile, and celebrate all the little things that make our love unique. I can’t wait to create countless memories with you and to continue building this beautiful life together.<br><br>
          Every day with you is a new adventure, and my heart grows fonder with every passing moment. I love dreaming about our future together, imagining all the laughter, hugs, and quiet moments we will share. You make me feel complete, and I can’t imagine a life without you. Thank you for being my love, my partner, and my Valentine.<br><br>
          Love always,<br><strong>Wealth</strong> ❤️
        </p>
        <!-- Puppy jumping image -->
        <img src="https://i.imgur.com/yourJumpingPuppy.png" alt="Happy Puppy" class="jumping-puppy" style="width:150px;">
        <img src="https://i.imgur.com/NmY7Xqk.png" alt="Flowers" style="width:150px;">
        <img src="https://i.imgur.com/9hL7Z6c.png" alt="Love Letter" style="width:150px;">
      `;
    }

    function moveNo() {
      const btn = document.getElementById('noBtn');
      const x = Math.random() * 200 - 100;
      const y = Math.random() * 200 - 100;
      btn.style.transform = `translate(${x}px, ${y}px)`;
    }

    function createHearts() {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.innerHTML = '❤️';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.fontSize = Math.random() * 20 + 15 + 'px';
      document.body.appendChild(heart);
      setTimeout(() => { heart.remove(); }, 6000);
    }

    setInterval(createHearts, 300);
  </script></body>
</html>
