
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ivie 🔥 Streak Proposal</title>
<style>
body {
  margin: 0;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, #100016, #ff2b83);
  font-family: Arial, sans-serif;
  text-align: center;
  color: white;
  padding: 18px;
  box-sizing: border-box;
}
.card {
  background: #1c1024;
  border: 2px solid #ff4b9a;
  border-radius: 25px;
  padding: 28px 20px;
  max-width: 390px;
  box-shadow: 0 0 25px #ff2b8370;
}
h1 { color: #ff69ad; }
.fire { font-size: 65px; }
p { line-height: 1.7; font-size: 17px; }
button {
  border: none;
  border-radius: 30px;
  padding: 14px 24px;
  font-size: 17px;
  font-weight: bold;
  margin: 8px;
}
#yes { background: #ff3c91; color: white; }
#no { background: white; color: #222; }
#result { font-size: 22px; color: #ff8fc2; }
</style>
</head>
<body>
<div class="card">
  <div class="fire">🔥🎵🔥</div>
  <h1>Hey Ivie! 💗</h1>
  <p>
    After careful investigation, I have concluded that
    my TikTok life is incomplete without you. 😭😂
    <br><br>
    Will you be my official TikTok streak partner?
    <br>
    Let's keep that fire alive until we reach 1000 days! 🔥
  </p>

  <h2>YOU 🤝 ME = 🔥 FOREVER</h2>

  <button id="yes" onclick="accept()">YESSS! 💖🔥</button>
  <button id="no" onclick="moveNo()">No 🙄</button>

  <p id="result"></p>
</div>

<script>
function accept() {
  document.querySelector(".card").innerHTML = `
    <div class="fire">🔥🥹💖🔥</div>
    <h1>IVIE SAID YESSS!</h1>
    <p>
      Official streak partners unlocked! 😂❤️
      <br><br>
      No skipping days, no abandoning me,
      and absolutely NO letting our fire die! 🔥
      <br><br>
      Our mission: 1000 DAYS! 😌💕
      <br><br>
      Now go to TikTok and let's start this streak!
    </p>
    <h2>IVIE 🔥 STREAK PARTNER</h2>
  `;
}
function moveNo() {
  document.getElementById("result").textContent =
    "Ivie, abeg! 😂 Just press YES! 🔥💗";
}
</script>
</body>
</html>
