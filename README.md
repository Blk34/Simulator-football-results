# Simulator-football-results
Simulator of football results
<!DOCTYPE html>
<html lang="hr">
<head>
  <meta charset="UTF-8">
  <title>Finale SP 2022</title>
  <style>
    body { font-family: Arial; text-align: center; margin-top: 50px; }
    button { padding: 10px 20px; font-size: 18px; cursor: pointer; }
    #result { margin-top: 20px; font-size: 24px; font-weight: bold; }
  </style>
</head>
<body>
  <h1>Finale SP 2022: Argentina vs Francuska</h1>
  <button id="playBtn">Odigraj utakmicu</button>
  <div id="result"></div>

  <script>
    // Dohvat gumba i rezultata
    const playBtn = document.getElementById('playBtn');
    const resultDiv = document.getElementById('result');

    playBtn.onclick = function() {
      // Šanse
      const rand = Math.random();
      let winner, loser;

      if (rand < 0.6) {
        winner = "Argentina";
        loser = "Francuska";
      } else {
        winner = "Francuska";
        loser = "Argentina";
      }

      // Golovi
      const winnerGoals = Math.floor(Math.random() * 5); // 0-4
      const loserGoals = Math.floor(Math.random() * (winnerGoals + 1));

      // Prikaz rezultata
      const text = winner === "Argentina"
        ? `Argentina ${winnerGoals} - ${loserGoals} Francuska`
        : `Argentina ${loserGoals} - ${winnerGoals} Francuska`;

      resultDiv.innerText = text;
    };
  </script>
</body>
</html>
