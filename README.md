# Simulator-football-results
Simulator of football results
<!DOCTYPE html>
<html lang="hr">
<head>
  <meta charset="UTF-8">
  <title>Finale SP 2022: Argentina vs Francuska</title>
  <style>
    body { font-family: Arial, sans-serif; text-align: center; margin-top: 50px; }
    button { font-size: 18px; padding: 10px 20px; cursor: pointer; }
    #result { margin-top: 30px; font-size: 24px; font-weight: bold; }
  </style>
</head>
<body>
  <h1>Finale SP 2022</h1>
  <h2>Argentina vs Francuska</h2>
  <button onclick="playMatch()">Odigraj utakmicu</button>
  <div id="result"></div>

  <script>
    function playMatch() {
      const argentinaChance = 0.6; // 60%
      const francuskaChance = 0.4; // 40%
      
      let winner, loser;
      if (Math.random() < argentinaChance) {
        winner = "Argentina";
        loser = "Francuska";
      } else {
        winner = "Francuska";
        loser = "Argentina";
      }

      const goalsWinner = Math.floor(Math.random() * 5); // 0-4 gola
      const goalsLoser = Math.floor(Math.random() * (goalsWinner + 1)); // 0 do golova pobjednika

      let resultText = "";
      if (winner === "Argentina") {
        resultText = `Argentina ${goalsWinner} - ${goalsLoser} Francuska`;
      } else {
        resultText = `Argentina ${goalsLoser} - ${goalsWinner} Francuska`;
      }

      document.getElementById("result").innerText = resultText;
    }
  </script>
</body>
</html>
