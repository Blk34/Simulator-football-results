# Simulator-football-results
Simulator of football results
<!DOCTYPE html>
<html lang="hr">
<head>
  <meta charset="UTF-8">
  <title>Finale SP 2022: Argentina vs Francuska</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 50px;
    }

    #match-info { margin: 20px; }

    button { padding: 10px 20px; font-size: 16px; cursor: pointer; }

    #result { margin-top: 30px; font-size: 24px; font-weight: bold; }
  </style>
</head>
<body>
  <h1>Finale SP 2022: Argentina vs Francuska</h1>
  <div id="match-info">
    <button id="playBtn">Odigraj utakmicu</button>
  </div>
  <div id="result"></div>

  <script>
    document.getElementById('playBtn').addEventListener('click', function() {
      // Postavljanje šansi
      const shanseArgentina = 0.6;
      const shanseFrancuska = 0.4;

      const rand = Math.random();
      let winner;

      if (rand < shanseArgentina) {
        winner = "Argentina";
      } else {
        winner = "Francuska";
      }

      // Generiranje rezultata
      const goalsWinner = Math.floor(Math.random() * 4) + 1; // 1-4 gola
      const goalsLoser = Math.floor(Math.random() * goalsWinner); // 0 do golova pobjednika-1

      const resultText = winner === "Argentina"
        ? `Argentina ${goalsWinner} - ${goalsLoser} Francuska`
        : `Argentina ${goalsLoser} - ${goalsWinner} Francuska`

