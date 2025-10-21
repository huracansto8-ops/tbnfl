<!DOCTYPE html>
<html>
<head>
  <title>Play Retro Game</title>
  <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
  <style>
    body {
      background-color: #000;
      color: #0f0;
      font-family: 'Press Start 2P', cursive;
      text-align: center;
      margin: 0;
    }
    #startButton {
      background-color: #4CAF50;
      border: none;
      color: white;
      padding: 15px 32px;
      font-size: 16px;
      margin-top: 200px;
      border-radius: 8px;
      cursor: pointer;
      box-shadow: 0 0 10px #000;
    }
  </style>
</head>
<body>
  <div id="game" style="display:none; width:100vw; height:100vh;"></div>
  <button id="startButton">PLAY</button>

  <script>
    const startButton = document.getElementById("startButton");
    const gameDiv = document.getElementById("game");

    startButton.addEventListener("click", () => {
      startButton.style.display = "none";
      gameDiv.style.display = "block";

      // EmulatorJS configuration
      EJS_player = "#game";
      EJS_core = "nes"; // Try "gba", "snes", "n64", etc.
      EJS_gameUrl = "https://cdn.jsdelivr.net/gh/huracansto8-ops/tbnfl@main/TSB%20-%20NCAA%202K25%20Edition%20%5BHARDTYPE%5D.nes"; // Change this URL
      EJS_pathtodata = "https://cdn.jsdelivr.net/gh/a456pur/seraph@main/storage/emulatorjs/data";
      EJS_startOnLoaded = true;

      // Load emulator engine
      const script = document.createElement("script");
      script.src = "https://cdn.jsdelivr.net/gh/a456pur/seraph@main/storage/emulatorjs/data/loader.js";
      document.body.appendChild(script);
    });
  </script>
</body>
</html>


