# Pedido
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Pedido Especial</title>
  <style>
    body {
      background-color: white;
      font-family: 'Arial', sans-serif;
      text-align: center;
      margin: 0;
      padding: 20px;
      height: 100vh;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
    .coracao {
      font-size: 50px;
      color: red;
      margin-bottom: 10px;
    }
    .texto {
      font-size: 20px;
      margin-bottom: 20px;
    }
    .botoes {
      position: relative;
      width: 100%;
      max-width: 300px;
      height: 100px;
    }
    button {
      padding: 8px 16px;
      font-size: 16px;
      margin: 10px;
      cursor: pointer;
    }
    #nao {
      position: absolute;
    }
  </style>
</head>
<body>

  <div class="coracao">❤️</div>
  <div class="texto">Quer namorar comigo?</div>

  <div class="botoes">
    <button onclick="responderSim()">Sim</button>
    <button id="nao" onmouseover="moverBotao()">Não</button>
  </div>

  <script>
    function responderSim() {
      alert("Pronto, agora teve um pedido oficial ❤️");
    }

    function moverBotao() {
      const btn = document.getElementById("nao");
      const largura = document.querySelector(".botoes").clientWidth - 80;
      const altura = document.querySelector(".botoes").clientHeight - 30;

      const novaPosX = Math.random() * largura;
      const novaPosY = Math.random() * altura;

      btn.style.left = novaPosX + "px";
      btn.style.top = novaPosY + "px";
    }
  </script>

</body>
</html>
