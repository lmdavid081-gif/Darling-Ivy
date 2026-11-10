
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ivie 🔥 TikTok Streak</title>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
  background: #080808;
  color: white;
  font-family: Arial, sans-serif;
  overflow: hidden;
}

.card {
  width: 100%;
  max-width: 390px;
  padding: 32px 22px;
  text-align: center;
  background: #171717;
  border: 1px solid #333;
  border-radius: 25px;
  box-shadow: 0 0 35px #fe2c5530;
  position: relative;
  overflow: hidden;
}

.tiktok {
  font-size: 42px;
  font-weight: 900;
  letter-spacing: -3px;
  text-shadow: -3px 0 #25f4ee, 3px 0 #fe2c55;
}

.flame {
  font-size: 78px;
  margin: 12px 0;
  animation: burn 0.8s infinite alternate;
  filter: drop-shadow(0 0 15px #ff5a00);
}

@keyframes burn {
  from { transform: scale(1) rotate(-4deg); }
  to { transform: scale(1.12) rotate(4deg); }
}

h1 {
  font-size: 29px;
  margin: 8px 0;
}

h1 span {
  color: #ff6333;
}

p {
  color: #c7c7c7;
  line-height: 1.7;
  font-size: 15px;
}

.streak {
  margin: 20px auto;
  padding: 13px;
  background: #242424;
  border-radius: 14px;
  border: 1px solid #444;
  color: #ff8b40;
  font-weight: bold;
  font-size: 17px;
}

.buttons {
  display: flex;
  justify-content: center;
  gap: 12px;
  margin-top: 25px;
  min-height: 55px;
}

button {
  border: none;
  border-radius: 30px;
  padding: 14px 25px;
  font-size: 16px;
  font-weight: bold;
  cursor: pointer;
}

#yes {
  color: white;
  background: linear-gradient(135deg, #fe2c55, #ff6933);
  box-shadow: 0 4px 15px #fe2c5540;
}

#no {
  background: #333;
  color: white;
}

#result {
  display: none;
  margin-top: 20px;
  color: #ff8750;
  font-weight: bold;
  line-height: 1.7;
}

.small {
  font-size: 11px;
  color: #777;
  margin-top: 25px;
}

.particle {
  position: fixed;
  bottom: -30px;
  pointer-events: none;
  animation: rise 3s linear forwards;
  z-index: 10;
}

@keyframes rise {
  to {
    transform: translateY(-110vh) rotate(25deg);
    opacity: 0;
  }
}
</style>
</head>

<body>

<div class="card">
  <div class="tiktok">TikTok</div>

  <div class="flame">🔥</div>

  <h1>Hey, <span>Ivie!</span> ❤️‍🔥</h1>

  <p>
    I have an important question for you.<br>
    Are you ready to be my official TikTok
    streak partner? 👀💕
  </p>

  <div class="streak">
    🔥 0 DAYS — OUR STREAK STARTS HERE!
  </div>

  <p>
    Daily messages, random videos, funny posts
    and absolutely no letting our streak die. 😂❤️
  </p>

  <h3>Will you keep the 🔥 alive with me?</h3>

  <div class="buttons">
    <button id="yes" onclick="accept()">YESSS! 🔥</button>
    <button id="no" onclick="moveNo()">No 🙄</button>
  </div>

  <div id="result">
    YAYYYYY! 😭❤️‍🔥<br>
    Ivie + Me = TikTok streak partners! 🔥<br>
    Now go and send me that first TikTok message. 😂💗
  </div>

  <div class="small">
    MADE WITH ❤️ JUST FOR IVIE
  </div>
</div>

<script>
function accept() {
  document.getElementById("result").style.display = "block";
  document.getElementById("no").style.display = "none";
  document.getElementById("yes").innerText = "STREAK PARTNERS! 🔥";

  for (let i = 0; i < 35; i++) {
    setTimeout(createParticle, i * 70);
  }
}

function moveNo() {
  const btn = document.getElementById("no");

  btn.style.position = "fixed";
  btn.style.left = Math.random() *
    (window.innerWidth - btn.offsetWidth - 20) + "px";
  btn.style.top = Math.random() *
    (window.innerHeight - btn.offsetHeight - 20) + "px";
}

function createParticle() {
  const particle = document.createElement("div");
  particle.className = "particle";

  const emojis = ["🔥", "❤️", "💕", "✨", "💗"];
  particle.textContent = emojis[
    Math.floor(Math.random() * emojis.length)
  ];

  particle.style.left = Math.random() * 100 + "vw";
  particle.style.fontSize = (18 + Math.random() * 22) + "px";

  document.body.appendChild(particle);

  setTimeout(() => particle.remove(), 3000);
}
</script>

</body>
</html>
