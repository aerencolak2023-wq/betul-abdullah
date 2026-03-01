# betul-abdullah
APO &lt;3 BETÜL
<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<title>Betül ❤️ Abdullah</title>
<!-- Google Fonts: Great Vibes -->
<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap" rel="stylesheet">
<style>
  body {
    margin: 0;
    height: 100vh;
    overflow: hidden;
    font-family: 'Great Vibes', cursive;
    display: flex;
    justify-content: center;
    align-items: center;
    background: linear-gradient(45deg, #ff1a1a, #ff66cc);
    background-size: 400% 400%;
    animation: gradientBG 15s ease infinite;
  }

  @keyframes gradientBG {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
  }

  .container {
    position: relative;
    text-align: center;
    color: white;
  }

  .heart {
    font-size: 150px;
    animation: pulse 1s infinite;
    z-index: 1;
    position: relative;
  }

  @keyframes pulse {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.3); }
  }

  .name-top {
    position: absolute;
    top: -100px;
    left: 50%;
    transform: translateX(-50%);
    font-size: 3em;
    font-weight: normal;
    color: #fff0f5;
    text-shadow: 2px 2px 5px #ff0066;
  }

  .name-bottom {
    position: absolute;
    bottom: -100px;
    left: 50%;
    transform: translateX(-50%);
    font-size: 3em;
    font-weight: normal;
    color: #fff0f5;
    text-shadow: 2px 2px 5px #ff0066;
  }

  .love-message {
    position: absolute;
    bottom: -200px;
    width: 100%;
    text-align: center;
    font-size: 2em;
    color: #ffe6f0;
    opacity: 0;
    transition: opacity 2s;
  }

  .love-message.show {
    opacity: 1;
  }

  .floating-heart {
    position: absolute;
    font-size: 30px;
    color: #ff99cc;
    animation: floatUp linear infinite;
    pointer-events: none;
    text-shadow: 1px 1px 5px #ff3399;
  }

  @keyframes floatUp {
    0% { transform: translateY(0) scale(1); opacity: 1; }
    100% { transform: translateY(-800px) scale(0.5); opacity: 0; }
  }
</style>
</head>
<body>

<div class="container">
  <div class="name-top">Betül</div>
  <div class="heart">❤️</div>
  <div class="name-bottom">Abdullah</div>
  <div class="love-message" id="loveMessage">Seni seviyorum 💖</div>
</div>

<script>
  setTimeout(() => {
    document.getElementById('loveMessage').classList.add('show');
  }, 2000);

  function createFloatingHeart() {
    const heart = document.createElement('div');
    heart.className = 'floating-heart';
    heart.style.left = Math.random() * window.innerWidth + 'px';
    heart.style.fontSize = (25 + Math.random() * 25) + 'px';
    heart.style.animationDuration = (3 + Math.random() * 3) + 's';
    heart.style.color = `hsl(${Math.random()*30+330}, 100%, 80%)`;
    heart.textContent = '❤️';
    document.body.appendChild(heart);

    setTimeout(() => {
      heart.remove();
    }, 6000);
  }

  setInterval(createFloatingHeart, 200);
</script>

</body>
</html>
