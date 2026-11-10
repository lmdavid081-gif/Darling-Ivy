
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ivie 🔥 Streak Proposal</title>

<style>
* { box-sizing: border-box; }

body {
  margin: 0;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
  overflow: hidden;
  background: linear-gradient(135deg, #100016, #390b32, #090909);
  font-family: Arial, sans-serif;
  text-align: center;
  color: white;
}

.card {
  position: relative;
  z-index: 2;
  background: rgba(28, 16, 36, 0.94);
  border: 2px solid #ff4b9a;
  border-radius: 25px;
  padding: 28px 20px;
  width: 100%;
  max-width: 390px;
  box-shadow: 0 0 30px #ff2b8370;
  animation: appear 1s ease;
}

h1 { color: #ff69ad; }
.fire { font-size: 55px; }

p {
  line-height: 1.7;
  font-size: 17px;
}

button {
  border: none;
  border-radius: 30px;
  padding: 14px 22px;
  font-size: 16px;
  font-weight: bold;
  margin: 8px 4px;
  cursor: pointer;
}

#yes {
  background: #ff3c91;
  color: white;
  box-shadow: 0 0 18px #ff3c91;
  animation: pulse 1.5s infinite;
}

#no {
  background: white;
  color: #222;
}

#result {
  color: #ff8fc2;
  font-weight: bold;
}

/* FLOATING FIRE 🔥 */
.floating-fire {
  position: fixed;
  bottom: -60px;
  z-index: 1;
  pointer-events: none;
  animation: rise linear forwards;
  filter: drop-shadow(0 0 8px #ff5b18);
}

@keyframes rise {
  0% {
    transform: translateY(0) rotate(0deg) scale(.7);
    opacity: 0;
  }
  15% { opacity: 1; }
  80% { opacity: .9; }
  100% {
    transform: translateY(-115vh) rotate(35deg) scale(1.3);
    opacity: 0;
  }
}

@keyframes pulse {
  50% { transform: scale(1.07); }
}

@keyframes appear {
  from { opacity: 0; transform: scale(.8); }
  to { opacity: 1; transform: scale(1); }
}

.heart {
  position: fixed;
  top: -30px;
  z-index: 1;
  pointer-events: none;
  animation: hearts-fall linear forwards;
}

@keyframes hearts-fall {
  to {
    transform: translateY(110vh) rotate(360deg);
    opacity: 0;
  }
}
</style>
</head>

<body>

<div class="card" id="card">
  <div class="fire">🔥🎵🔥</div>
  <h1>Hey Ivie! 💗</h1>

  <p>
    After careful investigation, I have concluded
    that my TikTok life is incomplete without you. 😭😂
    <br><br>
    Will you be my official TikTok streak partner?
    <br>
    Let's keep that fire alive until we reach 1000 days! 🔥
  </p>

  <h2>YOU 🤝 ME = 🔥 FOREVER</h2>

  <button id="yes" onclick="accept()">
    YESSS! 💖🔥
  </button>

  <button id="no" onclick="moveNo()">
    No 🙄
  </button>

  <p id="result"></p>
</div>

<script>
function createFire() {
  const fire = document.createElement("div");
  fire.className = "floating-fire";
  fire.textContent = Math.random() > 0.25 ? "🔥" : "❤️‍🔥";

  fire.style.left = Math.random() * 100 + "vw";
  fire.style.fontSize = (22 + Math.random() * 25) + "px";
  fire.style.animationDuration = (4 + Math.random() * 5) + "s";

  document.body.appendChild(fire);

  setTimeout(() => fire.remove(), 9500);
}

function createHeart() {
  const heart = document.createElement("div");
  heart.className = "heart";
  heart.textContent = Math.random() > 0.5 ? "💗" : "✨";

  heart.style.left = Math.random() * 100 + "vw";
  heart.style.fontSize = (14 + Math.random() * 18) + "px";
  heart.style.animationDuration = (5 + Math.random() * 5) + "s";

  document.body.appendChild(heart);

  setTimeout(() => heart.remove(), 10500);
}

setInterval(createFire, 350);
setInterval(createHeart, 900);

function accept() {
  document.getElementById("card").innerHTML = `
    <div class="fire">🔥🥹💖🔥</div>
    <h1>IVIE SAID YESSS!</h1>
    <p>
      OFFICIAL STREAK PARTNERS UNLOCKED! 😂❤️
      <br><br>
      No skipping days, no abandoning me,
      and absolutely NO letting our fire die! 🔥
      <br><br>
      Our mission: 1000 DAYS! 😌💕
      <br><br>
      Now go to TikTok and let's keep that streak alive!
    </p>
    <h2>IVIE 🔥 STREAK PARTNER</h2>
    <p>Signed: Your favourite troublemaker 😎💗</p>
  `;

  for (let i = 0; i < 30; i++) {
    setTimeout(createFire, i * 80);
    setTimeout(createHeart, i * 100);
  }
}

function moveNo() {
  document.getElementById("result").textContent =
    "Ivie abeggg! 😂🔥 Just press YES! 💗";
}
</script>

</body>
</html>
