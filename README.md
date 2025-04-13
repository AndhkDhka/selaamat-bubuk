<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>I Love You, Sayang 💘</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to right, #ffe6f0, #fff0f5);
      overflow: hidden;
      font-family: 'Comic Sans MS', cursive;
    }

    h1 {
      text-align: center;
      color: #ff4d6d;
      font-size: 3em;
      margin-top: 100px;
      animation: fadeIn 3s ease-in-out;
    }

    .bunga {
      position: absolute;
      width: 30px;
      height: 30px;
      background-image: url('https://cdn-icons-png.flaticon.com/512/616/616408.png');
      background-size: cover;
      animation: jatuh 10s linear infinite;
    }

    @keyframes jatuh {
      0% {
        top: -50px;
        left: calc(100% * var(--random-x));
        transform: rotate(0deg);
      }
      100% {
        top: 100%;
        left: calc(100% * var(--random-x));
        transform: rotate(360deg);
      }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    .love-message {
      text-align: center;
      font-size: 1.5em;
      color: #d6336c;
      margin-top: 20px;
      animation: fadeIn 4s ease-in-out 2s forwards;
      opacity: 0;
    }
  </style>
</head>
<body>
  <h1>I Love You, Bibil 💖</h1>
  <div class="love-message">Selamat tidur mimpi indah malam ini semoga nyenyak bubuk e 🌸</div>

  <script>
    // Bikin bunga jatuh
    function createFlower() {
      const flower = document.createElement("div");
      flower.classList.add("bunga");
      flower.style.setProperty("--random-x", Math.random());
      flower.style.left = Math.random() * 100 + "vw";
      document.body.appendChild(flower);
      
      setTimeout(() => {
        flower.remove();
      }, 10000);
    }

    setInterval(createFlower, 300);
  </script>
</body>
</html>
