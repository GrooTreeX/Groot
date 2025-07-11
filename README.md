

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Best Sister Forever</title>
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      height: 100vh;
      background-color: #006400; /* Dark green */
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      font-family: 'Dancing Script', cursive;
      color: white;
    }

    .heart-popup {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%) scale(0);
      width: 300px;
      height: 300px;
      background: red;
      clip-path: polygon(
        50% 15%, 
        61% 0, 
        75% 0, 
        85% 10%, 
        90% 25%, 
        85% 40%, 
        50% 80%, 
        15% 40%, 
        10% 25%, 
        15% 10%, 
        25% 0, 
        39% 0
      );
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 20px;
      color: white;
      font-size: 24px;
      transition: transform 0.4s ease;
      z-index: 10;
    }

    .heart-popup.show {
      transform: translate(-50%, -50%) scale(1);
    }

    button {
      padding: 12px 24px;
      font-size: 20px;
      border: none;
      background-color: #ffffff;
      color: #006400;
      border-radius: 8px;
      cursor: pointer;
      font-family: 'Dancing Script', cursive;
      transition: transform 0.2s ease;
    }

    button:hover {
      transform: scale(1.05);
    }
  </style>
</head>
<body>

  <div class="heart-popup" id="heart">
    You are my best sister forever
  </div>

  <button onclick="showHeart()">Tap Me 💖</button>

  <script>
    function showHeart() {
      const heart = document.getElementById('heart');
      heart.classList.add('show');
      setTimeout(() => {
        heart.classList.remove('show');
      }, 3000); // Auto-hide after 3 seconds
    }
  </script>

</body>
</html>