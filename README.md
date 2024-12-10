<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cartão Animado</title>
  <style>
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: linear-gradient(45deg, #ff9a9e, #fad0c4);
    }

    .card {
      width: 300px;
      height: 400px;
      background: white;
      border-radius: 20px;
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 20px;
      text-align: center;
    }

    .heart {
      width: 100px;
      height: 100px;
      background-color: #ff66b2; /* Tom rosa para a boneca Lili */
      position: relative;
      transform: rotate(-45deg);
      animation: pulse 1s infinite;
    }

    .heart::before,
    .heart::after {
      content: '';
      width: 100px;
      height: 100px;
      background-color: #ff66b2;
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

    @keyframes pulse {
      0%, 100% {
        transform: scale(1) rotate(-45deg);
      }
      50% {
        transform: scale(1.2) rotate(-45deg);
      }
    }

    .message {
      margin-top: 20px;
      font-size: 20px;
      font-weight: bold;
      color: #333;
    }
    
    .angel {
      width: 100px;
      height: 100px;
      background: url('https://static.wikia.nocookie.net/liloandstitch/images/d/d1/Angel.png/revision/latest/scale-to-width-down/350?cb=20200104034334') no-repeat center;
      background-size: contain;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <div class="card">
    <div class="heart"></div>
    <div class="message">Feliz dia! 🌸</div>
    <div class="angel"></div> <!-- Imagem da Angel -->
  </div>
</body>
</html>
