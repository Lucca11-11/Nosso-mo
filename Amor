<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Nosso Amor</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #ffe6f0;
      text-align: center;
      padding: 0;
      margin: 0;
      overflow-x: hidden;
    }

    h1 {
      font-size: 6vw;
      color: #d63384;
      margin-bottom: 10px;
    }

    #intro {
      transition: opacity 1s ease, transform 1s ease;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    #intro.hidden {
      opacity: 0;
      transform: translateY(-20px);
      pointer-events: none;
    }

    #ursinhos {
      width: 40vw;
      max-width: 200px;
      margin-bottom: 20px;
    }

    #fraseIntro, #timer, #imgCimaTimer {
      opacity: 0;
      transform: translateY(20px);
      transition: opacity 1s ease, transform 1s ease;
    }

    .fade-in {
      opacity: 1 !important;
      transform: translateY(0) !important;
    }

    #fraseIntro {
      font-size: 5vw;
      color: #d63384;
      margin-top: 0;
      margin-bottom: 10px;
    }

    #timer {
      font-size: 5vw;
      color: #333;
    }

    button {
      background-color: #ff4d79;
      color: white;
      border: none;
      padding: 15px 30px;
      font-size: 4.5vw;
      border-radius: 10px;
      cursor: pointer;
    }

    button:hover {
      background-color: #e0436d;
    }

    .heart {
      position: fixed;
      top: -50px;
      color: #ff4d79;
      font-size: 20px;
      animation: fall linear infinite;
      opacity: 0.8;
      z-index: 0;
    }

    @keyframes fall {
      0% {
        transform: translateY(-100px) rotate(0deg);
        opacity: 0;
      }
      10% {
        opacity: 1;
      }
      100% {
        transform: translateY(110vh) rotate(360deg);
        opacity: 0;
      }
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.1); }
      100% { transform: scale(1); }
    }

    #imgCimaTimer {
      width: 30vw;
      max-width: 150px;
      margin-bottom: 20px;
    }

    #imgCimaTimer.fade-in {
      opacity: 1 !important;
      transform: translateY(0) !important;
      animation: pulse 2s infinite;
    }

    #timerContainer {
      display: none;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      text-align: center;
    }
  </style>
</head>
<body>
  <div id="intro">
    <img id="ursinhos" src="Ln.jpg" alt="Ursinhos abraçados" />
    <h1>QUER SABER HÁ QUANTO TEMPO VC ME ATURA?</h1>
    <button id="loveButton">CLICA AQUI</button>
  </div>

  <div id="timerContainer">
    <img id="imgCimaTimer" src="La.png" alt="Coração" />
    <p id="fraseIntro">Estamos juntos há:</p>
    <div id="timer"></div>
  </div>

  <audio id="musica" src="ordinary.mp3"></audio>
  <div id="heart-container"></div>

  <script>
    const dataInicial = new Date("2024-10-08T00:00:00");
    const botao = document.getElementById("loveButton");
    const intro = document.getElementById("intro");
    const timer = document.getElementById("timer");
    const fraseIntro = document.getElementById("fraseIntro");
    const timerContainer = document.getElementById("timerContainer");
    const musica = document.getElementById("musica");
    const heartContainer = document.getElementById("heart-container");
    const imgCimaTimer = document.getElementById("imgCimaTimer");

    function atualizarCronometro() {
      const agora = new Date();
      const diff = agora - dataInicial;
      const dias = Math.floor(diff / (1000 * 60 * 60 * 24));
      const horas = Math.floor((diff / (1000 * 60 * 60)) % 24);
      const minutos = Math.floor((diff / (1000 * 60)) % 60);
      const segundos = Math.floor((diff / 1000) % 60);
      timer.textContent = `${dias} dias, ${horas} horas, ${minutos} minutos e ${segundos} segundos`;
    }

    botao.addEventListener("click", () => {
      intro.classList.add("hidden");

      setTimeout(() => {
        intro.style.display = "none";
        fraseIntro.classList.add("fade-in");
        timer.classList.add("fade-in");
        imgCimaTimer.classList.add("fade-in");
        musica.play();
        atualizarCronometro();
        setInterval(atualizarCronometro, 1000);
        iniciarChuvaDeCoracoes();
        timerContainer.style.display = "flex"; // Mostra e centraliza
      }, 1000);
    });

    function iniciarChuvaDeCoracoes() {
      setInterval(() => {
        const heart = document.createElement("div");
        heart.classList.add("heart");
        heart.innerHTML = "&#10084;";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.fontSize = (Math.random() * 20 + 10) + "px";
        heart.style.animationDuration = (Math.random() * 3 + 3) + "s";
        heartContainer.appendChild(heart);
        setTimeout(() => {
          heart.remove();
        }, 7000);
      }, 300);
    }
  </script>
</body>
</html>
