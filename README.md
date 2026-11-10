
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ivie 💗 Streak Partner?</title>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  font-family: "Trebuchet MS", sans-serif;
  background: linear-gradient(135deg, #ffe0ec, #f8a5c2, #ffc8dd);
  color: #702344;
}

.heart {
  position: fixed;
  bottom: -40px;
  pointer-events: none;
  animation: floatUp linear infinite;
  opacity: 0.6;
  z-index: 0;
}

@keyframes floatUp {
  to {
    transform: translateY(-115vh) rotate(360deg);
    opacity: 0;
  }
}

.card {
  position: relative;
  z-index: 2;
  width: 90%;
  max-width: 420px;
  padding: 30px 22px;
  text-align: center;
  border-radius: 28px;
  background: rgba(255,255,255,0.92);
  box-shadow: 0 15px 45px #a83d6650;
}

.emoji {
  font-size: 65px;
  animation: bounce 1.5s infinite;
}

@keyframes bounce {
  50% { transform: translateY(-8px); }
}

h1 {
  font-size: 30px;
  margin: 12px 0;
}

p {
  font-size: 16px;
  line-height: 1.7;
}

.buttons {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 14px;
  margin-top: 28px;
  min-height: 55px;
}

button {
  border: none;
  padding: 13px 23px;
  border-radius: 30px;
  font-size: 16px;
  font-weight: bold;
  cursor: pointer;
  touch-action: manipulation;
}

#yes {
  color: white;
  background: #ed4b86;
  box-shadow: 0 5px 12px #ed4b8650;
}

#no {
  background: #f3e8ed;
  color: #702344;
  position: fixed;
  z-index: 5;
}

#result {
  display: none;
}

.small {
  font-size: 12px;
  opacity: 0.7;
}
</style>
</head>

<body>

<div class="card">
  <div class="emoji">💌</div>

  <h1>Hey, Ivie! 💗</h1>

  <p>
    I have an extremely important question to ask you.
    Please take a deep breath and prepare yourself. 😭😂
  </p>

  <p>
    Will you do me the honour of becoming
    <b>my official streak partner?</b> 🔥📱
  </p>

  <p>
    Daily snaps, random pictures, unserious updates
    and absolutely no letting our streak die. 😌❤️
  </p>

  <h3>So, Ivie... deal? 🥹</h3>

  <div class="buttons" id="buttons">
    <button id="yes" onclick="sayYes()">YESSS! 💖</button>
    <button id="no">NO 😭</button>
  </div>

  <div id="result">
    <div class="emoji">🥳💗🔥</div>
    <h1>IT'S OFFICIAL!!</h1>
    <p>
      IVIE SAID YESSS! 😭❤️
      <br>
      Our streak era begins NOW.
      No excuses, no disappearing,
      and no letting that fire die! 🔥
    </p>
    <p>Best streak partners loading... 💌</p>
  </div>

  <p class="small">Made with questionable levels of effort 😂💕</p>
</div>

<script>
const noBtn = document.getElementById("no");

function moveNo() {
  const maxX = Math.max(0, window.innerWidth - noBtn.offsetWidth - 12);
  const maxY = Math.max(0, window.innerHeight - noBtn.offsetHeight - 12);

  noBtn.style.left = (Math.random() * maxX) + "px";
  noBtn.style.top = (Math.random() * maxY) + "px";
}

noBtn.addEventListener("mouseenter", moveNo);
noBtn.addEventListener("touchstart", function(e) {
  e.preventDefault();
  moveNo();
}, { passive: false });

noBtn.addEventListener("click", moveNo);

function sayYes() {
  document.getElementById("buttons").style.display = "none";
  noBtn.style.display = "none";
  document.getElementById("result").style.display = "block";

  for (let i = 0; i < 35; i++) {
    const heart = document.createElement("div");
    heart.textContent = ["💖", "💕", "🔥", "💗", "✨"][
      Math.floor(Math.random() * 5)
    ];
    heart.style.position = "fixed";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.top = Math.random() * 100 + "vh";
    heart.style.fontSize = "25px";
    heart.style.zIndex = "10";
    heart.style.pointerEvents = "none";
    document.body.appendChild(heart);

    heart.animate([
      { transform: "translateY(0) scale(0.5)", opacity: 1 },
      { transform: "translateY(-180px) scale(1.5)", opacity: 0 }
    ], {
      duration: 1800 + Math.random() * 1500,
      easing: "ease-out"
    }).onfinish = () => heart.remove();
  }
}

// Create floating background hearts
for (let i = 0; i < 22; i++) {
  const heart = document.createElement("div");
  heart.className = "heart";
  heart.textContent = Math.random() > 0.5 ? "💗" : "💕";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.animationDuration = (5 + Math.random() * 8) + "s";
  heart.style.animationDelay = (Math.random() * 8) + "s";
  heart.style.fontSize = (16 + Math.random() * 22) + "px";
  document.body.appendChild(heart);
}

// Put the No button somewhere visible at first
moveNo();
</script>

</body>
</html>
