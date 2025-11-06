# Simulator-football-results
Simulator of football results
innerText = text;
<!DOCTYPE html>
<html lang="hr">
<head>
<meta charset="UTF-8">
<title>Simulacija utakmice</title>
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
document.getElementById("playBtn").onclick = function() {
    let winner, loser;
    if (Math.random() < 0.6) {  // 60% Argentina
        winner = "Argentina";
        loser = "Francuska";
    } else {
        winner = "Francuska";
        loser = "Argentina";
    }

    const winnerGoals = Math.floor(Math.random() * 5);
    const loserGoals = Math.floor(Math.random() * (winnerGoals + 1));

    const text = winner === "Argentina"
        ? `Argentina ${winnerGoals} - ${loserGoals} Francuska`
        : `Argentina ${loserGoals} - ${winnerGoals} Francuska`;

    document.getElementById("result").innerText = text;
};
</script>
</body>
</html>
