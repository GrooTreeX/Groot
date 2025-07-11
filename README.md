# Groot

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Rakhi, Sis!</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(120deg, #ffdde1, #ee9ca7);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      overflow: hidden;
    }

    h1 {
      font-size: 2em;
      color: #fff;
      margin-bottom: 20px;
      text-shadow: 2px 2px 5px rgba(0,0,0,0.3);
    }

    .tap-btn {
      background: #ff4081;
      color: white;
      border: none;
      padding: 15px 30px;
      font-size: 1.2em;
      border-radius: 30px;
      cursor: pointer;
      transition: 0.3s;
      box-shadow: 0 4px 10px rgba(0,0,0,0.3);
    }

    .tap-btn:hover {
      background: #e91e63;
    }

    .heart-container {
      margin-top: 40px;
      position: relative;
      width: 200px;
      height: 180px;
      display: none;
      animation: pop 0.6s ease forwards;
    }

    .heart {
      position: absolute;
      width: 100px;
      height: 90px;
      background: red;
      left: 50%;
      top: 0;
      transform: translateX(-50%) rotate(-45deg);
      border-radius: 50% 50% 0 0;
    }

    .heart::before,
    .heart::after {
      content: '';
      position: absolute;
      width: 100px;
      height: 90px;
      background: red;
      border-radius: 50%;
    }

    .heart::before {
      top: -45px;
      left: 0;
    }

    .heart::after {
      top: 0;
      left: 45px;
    }

    .message {
      position: absolute;
      width: 100%;
      text-align: center;
      top: 120px;
      font-size: 1.4em;
      font-weight: bold;
      color: #fff;
      opacity: 0;
      animation: fadeInUp 2s ease-in-out forwards;
    }

    @keyframes pop {
      0% {
        transform: scale(0.5);
        opacity: 0;
      }
      100% {
        transform: scale(1);
        opacity: 1;
      }
    }

    @keyframes fadeInUp {
      0% {
        opacity: 0;
        transform: translateY(20px);
      }
      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>
<body>

  <h1>Happy Raksha Bandhan 💖</h1>
  <button class="tap-btn" onclick="showHeart()">Tap Me</button>

  <div class="heart-container" id="heartBox">
    <div class="heart"></div>
    <div class="message">You are my best sister! 💕</div>
  </div>

  <script>
    function showHeart() {
      const heart = document.getElementById('heartBox');
      heart.style.display = 'block';
    }
  </script>

</body>
</html>
