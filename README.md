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
      // 60% šanse za Argentinu, 40% za Francusku
      const winner = Math.random() < 0.6 ? "Argentina" : "Francuska";
      const loser = winner === "Argentina" ? "Francuska" : "Argentina";

      // Golovi
      const winnerGoals = Math.floor(Math.random() * 5); // 0-4
      const loserGoals = Math.floor(Math.random() * (winnerGoals + 1)); // 0 do golova pobjednika

      // Prikaz rezultata
      const resultText = winner === "Argentina" 
        ?
