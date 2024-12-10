<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pedido Especial</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: linear-gradient(45deg, #ff9a9e, #fad0c4);
      margin: 0;
    }

    .card {
      width: 350px;
      height: 300px;
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

    .message {
      font-size: 20px;
      font-weight: bold;
      color: #333;
      margin-bottom: 20px;
    }

    .buttons {
      display: flex;
      gap: 10px;
    }

    .buttons button {
      padding: 10px 20px;
      font-size: 16px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: background 0.3s;
    }

    .yes {
      background-color: #66b3ff;
    }

    .no {
      background-color: #ff6666;
      animation: moveButton 2s infinite; /* Animação para o botão 'Não' */
    }

    .yes:hover {
      background-color: #4d99cc;
    }

    .no:hover {
      background-color: #cc4d4d;
    }

    @keyframes moveButton {
      0% { transform: translateX(0); }
      25% { transform: translateX(15px); }
      50% { transform: translateX(0); }
      75% { transform: translateX(-15px); }
      100% { transform: translateX(0); }
    }

    .response {
      margin-top: 20px;
      font-size: 18px;
      color: #333;
      font-weight: bold;
      display: none;
    }
    
    /* Desabilitar interação com o botão 'Não' */
    .no:disabled {
      pointer-events: none;
      opacity: 0.5;
    }
  </style>
</head>
<body>

  <div class="card">
    <div class="message">Quer jantar comigo?</div>
    <div class="buttons">
      <button class="yes" onclick="showResponse('yes')">Sim</button>
      <button class="no" id="noButton" onclick="showResponse('no')" disabled>Não</button>
    </div>
    <div class="response" id="responseMessage"></div>
  </div>

  <script>
    function showResponse(answer) {
      const responseMessage = document.getElementById('responseMessage');
      const noButton = document.getElementById('noButton');
      
      if (answer === 'yes') {
        responseMessage.textContent = 'Beleza, te pego às 22:00!';
        responseMessage.style.color = '#66b3ff';
      } else {
        responseMessage.textContent = 'Sem problemas!';
        responseMessage.style.color = '#ff6666';
      }
      responseMessage.style.display = 'block';
      
      // Desabilitar o botão "Não" ao clicar
      noButton.disabled = true;
    }
  </script>

</body>
</html>
