# coinflip-demoindex.html
style.css body {
  background: #111;
  color: white;
  text-align: center;
  font-family: Arial;
}

button {
  padding: 10px 20px;
  margin: 10px;
  font-size: 16px;
}

script.jslet balance = 1000;

function flip(choice) {
  const bet = Number(document.getElementById("bet").value);
  if (bet <= 0 || bet > balance) {
    alert("Ongeldige inzet");
    return;
  }

  const result = Math.random() < 0.5 ? "heads" : "tails";

  if (choice === result) {
    balance += bet;
    document.getElementById("result").innerText =
      `🎉 Gewonnen! Het was ${result}`;
  } else {
    balance -= bet;
    document.getElementById("result").innerText =
      `❌ Verloren! Het was ${result}`;
  }

  document.getElementById("balance").innerText = balance;
}

<!DOCTYPE html>
<html lang="nl">
<head>
  <meta charset="UTF-8">
  <title>Coinflip Demo</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

<h1>🪙 Coinflip</h1>
<p>Balans: <span id="balance">1000</span></p>

<input id="bet" type="number" value="10">
<br><br>

<button onclick="flip('heads')">Kop</button>
<button onclick="flip('tails')">Munt</button>

<p id="result"></p>

<script src="script.js"></script>
</body>
</html>
