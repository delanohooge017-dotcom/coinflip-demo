# coinflip-demoindex.html
style.css
script.js
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
