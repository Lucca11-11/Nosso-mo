<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Para o Amor da Minha Vida</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to bottom, #ffe6e6, #fff);
      font-family: 'Courier New', Courier, monospace;
      color: #b30059;
      text-align: center;
    }

    .container {
      padding: 50px 20px;
    }

    h1 {
      font-size: 3em;
      margin-bottom: 10px;
    }

    p {
      font-size: 1.2em;
      max-width: 600px;
      margin: 0 auto 30px;
    }

    button {
      background-color: #ff6699;
      color: white;
      border: none;
      padding: 15px 25px;
      font-size: 1em;
      border-radius: 30px;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background-color: #ff3366;
    }

    .heart {
      font-size: 2em;
      color: red;
      animation: pulse 1s infinite;
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.2); }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="heart">❤️</div>
    <h1>Te Amo Muito!</h1>
    <p>Você é a razão do meu sorriso todos os dias. Este site é só um pedacinho do meu amor por você.</p>
    <button onclick="mostrarMensagem()">Clique para uma surpresa</button>
    <p id="mensagem" style="margin-top: 20px; display: none;"></p>
  </div>

  <script>
    function mostrarMensagem() {
      const mensagem = document.getElementById('mensagem');
      mensagem.innerText = "Você é o meu eterno amor! Sempre ao seu lado!";
      mensagem.style.display = "block";
    }
  </script>
</body>
</html>
