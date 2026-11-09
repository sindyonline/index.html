<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <script type="module" src="https://pyscript.net/releases/2026.7.3/core.js"></script>
</head>
<body>
  <h1>🍪 Glückskeks-Orakel 🍪</h1>
  <p>Tippe auf den Keks!</p>
  <button id="keks">🥠</button>
  <p id="spruch"></p>

<script type="mpy">
from pyscript import when, document
import random

sprueche = [
    "Heute passiert dir etwas Schönes ✨",
    "Du bist netter, als du denkst 💖",
    "Ein Lächeln von dir macht jemandem den Tag 😊",
    "Gönn dir heute einen Keks 🍪",
    "Sei nett - immer, zu jedem! 🐢",
]

@when("click", "#keks")
def oeffne_keks(event):
    nummer = random.randint(0, len(sprueche) - 1)
    document.querySelector("#spruch").innerText = sprueche[nummer]
</script>
</body>
</html>
