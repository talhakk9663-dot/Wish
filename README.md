
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Birthday Surprise for Zunaira 🎂</title>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  min-height: 100vh;
  padding: 25px 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: Georgia, serif;
  text-align: center;
  background: linear-gradient(135deg,#ffe0ec,#e8d9ff,#fff0f5);
  color: #713c70;
}

.card {
  width: 100%;
  max-width: 430px;
  padding: 30px 22px;
  border: 2px solid white;
  border-radius: 30px;
  background: rgba(255,255,255,.8);
  box-shadow: 0 15px 45px #b77ab044;
  animation: appear 1.2s ease;
}

@keyframes appear {
  from {opacity:0; transform:translateY(35px);}
  to {opacity:1; transform:translateY(0);}
}

h1 {
  color: #d34e91;
  font-size: 34px;
  margin: 15px 0;
}

h2 {
  color: #b65b9b;
  margin: 15px 0;
}

.cake-area {
  margin: 30px 0;
  animation: cakeFloat 2s infinite ease-in-out;
}

.cake {
  font-size: 105px;
  filter: drop-shadow(0 8px 12px #e99abe66);
}

.flames {
  font-size: 22px;
  display: flex;
  justify-content: center;
  gap: 20px;
  margin-bottom: -5px;
  animation: flicker .7s infinite alternate;
}

@keyframes flicker {
  from {opacity:.7;transform:scale(.95);}
  to {opacity:1;transform:scale(1.1);}
}

@keyframes cakeFloat {
  50% {transform:translateY(-7px);}
}

.cake-text {
  color: #d34e91;
  font-style: italic;
  margin-top: 8px;
}

.divider {
  width: 65%;
  height: 2px;
  background: #f2b3d4;
  margin: 25px auto;
}

.message {
  font-size: 16px;
  line-height: 1.9;
  color: #785578;
}

button {
  display: block;
  width: 100%;
  border: none;
  padding: 14px;
  border-radius: 30px;
  background: linear-gradient(45deg,#ed68a6,#a779e8);
  color: white;
  font-size: 15px;
  font-family: Georgia,serif;
  margin-top: 14px;
  cursor: pointer;
}

button:active {
  transform: scale(.96);
}

.special-message {
  display: none;
  padding: 20px;
  margin-top: 20px;
  border-radius: 20px;
  background: #fff0f7;
  color: #bd4d8e;
  line-height: 1.9;
  animation: appear 1s;
}

.footer {
  margin-top: 25px;
  color: #a77b9f;
  font-size: 13px;
}

.heart {
  position: fixed;
  bottom: -30px;
  font-size: 20px;
  pointer-events: none;
  animation: float 7s linear forwards;
}

@keyframes float {
  0% {transform:translateY(0);opacity:0;}
  15% {opacity:1;}
  100% {transform:translateY(-110vh) rotate(360deg);opacity:0;}
}
</style>
</head>

<body>

<div class="card">

  <div style="font-size:42px;">🎀✨</div>

  <h1>Happy Birthday!</h1>
  <h2 style="font-size:30px;">Zunaira 💗</h2>

  <p>Today is all about YOU! 🌷</p>

  <!-- BIRTHDAY CAKE -->

  <div class="cake-area">

    <div class="flames">
      <span>🔥</span>
      <span>🔥</span>
      <span>🔥</span>
    </div>

    <div class="cake">🎂</div>

    <p class="cake-text">
      Make a wish, Zunaira! ✨
    </p>

  </div>

  <div class="divider"></div>

  <h2>💌 A Special Message For You</h2>

  <p class="message">
    Dear Zunaira 🌸,<br><br>

    On your special day, I wish you endless happiness,
    beautiful memories, and a life full of success.
    May every little dream of yours come true.
    Keep smiling and shining always! 💗
  </p>

  <button onclick="showMessage(1)">
    A Little Birthday Wish 💖
  </button>

  <button onclick="showMessage(2)">
    One More Surprise 🎁
  </button>

  <button onclick="showMessage(3)">
    Special Words For You 🌷
  </button>

  <div id="specialMessage" class="special-message">
  </div>

  <div class="footer">
    Made with 💗 just for Zunaira
  </div>

</div>

<script>

function showMessage(number) {

  const messages = {

    1: "Happy Birthday, Zunaira! 💗 May your days be filled with laughter, your heart with peace, and your life with beautiful moments. 🌸",

    2: "A little reminder: You are special, your smile is precious, and you deserve all the happiness this world has to offer. 🎀✨",

    3: "May this new chapter bring wonderful opportunities, unforgettable adventures, success and countless blessings. Keep shining, birthday girl! 🦋💕"

  };

  const box = document.getElementById("specialMessage");

  box.innerHTML = messages[number];
  box.style.display = "block";

}

// FLOATING HEARTS

function createHeart() {

  const heart = document.createElement("div");

  heart.className = "heart";

  heart.innerHTML = ["💗","💕","🌸","✨","🦋"][
    Math.floor(Math.random()*5)
  ];

  heart.style.left = Math.random()*100+"vw";

  heart.style.animationDuration =
    (5+Math.random()*5)+"s";

  document.body.appendChild(heart);

  setTimeout(()=>heart.remove(),10000);

}

setInterval(createHeart,500);

</script>

</body>
</html>
