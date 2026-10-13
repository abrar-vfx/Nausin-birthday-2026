<!DOCTYPE html><html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Nausin 🎂</title><style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

body {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(135deg, #f6c5ff, #c8f8ff);
  overflow: hidden;
  text-align: center;
}

.box {
  background: white;
  padding: 30px 20px;
  width: 90%;
  max-width: 420px;
  border-radius: 25px;
  box-shadow: 0 10px 30px rgba(0,0,0,.2);
  z-index: 2;
}

h1 {
  color: #ff4f92;
  margin-bottom: 20px;
  font-size: 28px;
}

button {
  padding: 12px 20px;
  margin: 8px;
  border: none;
  border-radius: 25px;
  background: #ff5aa5;
  color: white;
  font-size: 17px;
  cursor: pointer;
}

button:active {
  transform: scale(.95);
}

.hidden {
  display: none;
}

#final {
  display: none;
  position: fixed;
  inset: 0;
  background: linear-gradient(135deg, #ff76b7, #ffd56a, #bda0ff);
  justify-content: center;
  align-items: center;
  flex-direction: column;
  color: white;
  padding: 20px;
  overflow: hidden;
}

.cake {
  font-size: 100px;
  animation: bounce 1.5s infinite;
  z-index: 2;
}

.note {
  font-size: 25px;
  line-height: 1.5;
  padding: 20px;
  z-index: 2;
}

.star {
  position: absolute;
  font-size: 25px;
  animation: fly 5s linear infinite;
}

.confetti {
  position: absolute;
  width: 9px;
  height: 13px;
  animation: fall 4s linear infinite;
}

@keyframes bounce {
  50% { transform: translateY(-15px) rotate(5deg); }
}

@keyframes fly {
  0% { transform: translateY(100vh) rotate(0deg); }
  100% { transform: translateY(-100px) rotate(360deg); }
}

@keyframes fall {
  0% { transform: translateY(-20px) rotate(0deg); }
  100% { transform: translateY(100vh) rotate(720deg); }
}
</style></head><body><div class="box" id="one">
  <h1>Hey NAUSIN!<br>Do u know what's today?</h1>
  <button onclick="yesBtn()">Yes</button>
  <button onclick="nextBtn()">No</button>
  <p id="a" style="margin-top:15px;color:#ff4081;font-size:20px;"></p>
</div><div class="box hidden" id="two">
  <h1>It's ur birthday 🎇🎂</h1>
  <button onclick="endBtn()">Want to end</button>
  <button onclick="giftBtn()">Want the gift</button>
  <p id="b" style="margin-top:15px;color:#ff4081;font-size:20px;"></p>
</div><div id="final">
  <div class="cake">🎁🎂✨</div>
  <div class="note">
    Happy birthday to u and many many returns of the day 💖🎉
  </div>
</div><script>
function yesBtn() {
  document.getElementById("a").innerHTML = "Think again 😏";
}

function nextBtn() {
  document.getElementById("one").classList.add("hidden");
  document.getElementById("two").classList.remove("hidden");
}

function endBtn() {
  document.getElementById("b").innerHTML =
    "Why! First take ur gift 🎁";
}

function giftBtn() {
  document.getElementById("two").classList.add("hidden");
  document.getElementById("final").style.display = "flex";

  for (let i = 0; i < 100; i++) {
    let c = document.createElement("div");
    c.className = "confetti";
    c.style.left = Math.random() * 100 + "vw";
    c.style.backgroundColor =
      `hsl(${Math.random() * 360},100%,60%)`;
    c.style.animationDuration =
      (Math.random() * 3 + 2) + "s";
    c.style.animationDelay = Math.random() * 3 + "s";
    document.getElementById("final").appendChild(c);
  }

  for (let i = 0; i < 30; i++) {
    let s = document.createElement("div");
    s.className = "star";
    s.innerHTML = "⭐";
    s.style.left = Math.random() * 100 + "vw";
    s.style.animationDuration =
      (Math.random() * 5 + 3) + "s";
    s.style.animationDelay = Math.random() * 4 + "s";
    document.getElementById("final").appendChild(s);
  }
}
</script></body>
</html>
