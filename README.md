<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Rakhi Card</title>
  <style>
    body {
      background-color: darkgreen;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      flex-direction: column;
      font-family: 'Segoe UI', sans-serif;
    }

    .btn {
      padding: 15px 30px;
      font-size: 18px;
      background-color: #fff;
      color: darkgreen;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-weight: bold;
      transition: 0.3s;
    }

    .btn:hover {
      background-color: #e0e0e0;
    }

    .heart-container {
      margin-top: 30px;
      display: none;
      flex-direction: column;
      align-items: center;
      animation: popUp 0.6s ease forwards;
    }

    .heart {
      width: 100px;
      height: 90px;
      position: relative;
      background-color: deeppink;
      transform: scale(0);
      animation: heartBeat 0.8s ease forwards;
    }

    .heart::before,
    .heart::after {
      content: "";
      width: 100px;
      height: 90px;
      background-color: deeppink;
      border-radius: 50%;
      position: absolute;
    }

    .heart::before {
      top: -50px;
      left: 0;
    }

    .heart::after {
      left: 50px;
      top: 0;
    }

    .message {
      margin-top: 15px;
      font-size: 24px;
      color: white;
      opacity: 0;
      animation: fadeIn 1s ease forwards 0.8s;
    }

    @keyframes heartBeat {
      to {
        transform: scale(1);
      }
    }

    @keyframes fadeIn {
      to {
        opacity: 1;
      }
    }

    @keyframes popUp {
      0% {
        opacity: 0;
        transform: translateY(50px);
      }
      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>
<body>

  <button class="btn" onclick="showHeart()">Tap</button>

  <div class="heart-container" id="heartContainer">
    <div class="heart"></div>
    <div class="message">You are my best sister</div>
  </div>

  <script>
    function showHeart() {
      document.getElementById("heartContainer").style.display = "flex";
    }
  </script>

</body>
</html>