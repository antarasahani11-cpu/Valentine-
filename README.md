<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>My Forever Valentine 💝</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
body {
  margin: 0;
  font-family: 'Comic Sans MS', cursive;
  background: linear-gradient(135deg, #ffd6e8, #e8d6ff);
  text-align: center;
  overflow-x: hidden;
}
section {
  min-height: 100vh;
  display: none;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 20px;
}
section.active {
  display: flex;
}
h1 {
  color: #ff3f81;
  font-size: 2.5em;
}
button {
  padding: 15px 30px;
  margin: 10px;
  font-size: 1.1em;
  border: none;
  border-radius: 30px;
  cursor: pointer;
  transition: transform 0.2s;
}
button:hover {
  transform: scale(1.1);
}
.yes {
  background: #ff4f9a;
  color: white;
}
.no {
  background: #ccc;
}
.popup {
  margin-top: 15px;
  color: #ff3f81;
}
.teddy {
  font-size: 60px;
  animation: jump 1s infinite;
}
@keyframes jump {
  0%,100% {transform: translateY(0);}
  50% {transform: translateY(-15px);}
}
.gallery img {
  width: 200px;
  height: 200px;
  object-fit: cover;
  border-radius: 20px;
  margin: 10px;
  box-shadow: 0 5px 15px rgba(0,0,0,0.2);
}
.hearts {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
}
</style>
</head>

<body>

<!-- PAGE 1 -->
<section id="page1" class="active">
  <h1>Do you love me? 💕</h1>
  <button class="yes" onclick="goTo('page2')">YES 💖</button>
  <button class="no" onclick="thinkAgain('p1msg')">NO 🙄</button>
  <div class="popup" id="p1msg"></div>
</section>

<!-- PAGE 2 -->
<section id="page2">
  <h1>Will you marry me? 🥹💍</h1>
  <button class="yes" onclick="goTo('page3')">YES 💍💖</button>
  <button class="no" onclick="thinkAgain('p2msg')">NO 😬</button>
  <div class="popup" id="p2msg"></div>
</section>

<!-- PAGE 3 -->
<section id="page3">
  <h1>ANUU has created a Valentine gift for you 💝</h1>
  <button class="yes" onclick="goTo('page4')">OPEN 🎁💖</button>
</section>

<!-- PAGE 4 -->
<section id="page4">
  <h1>HAPPY VALENTINE’S DAY<br>MY FOREVER ❤️♾️</h1>
  
  <div class="gallery">
    <!-- REPLACE image1.jpg etc with your own image links -->
    <img src="Snapchat-1616974652.jpg">
    <img src="Snapchat-876477308.jpg">
    <img src="Snapchat-419832368.jpg">
    <img src="Snapchat-1977597412.jpg">
  </div>

  <div class="teddy">🧸</div>
  <p>❤️ 💖 🥰 😍 💋</p>
  <p><b>Forever yours, ANUU 💗</b></p>
</section>

<script>
function goTo(id) {
  document.querySelectorAll('section').forEach(s => s.classList.remove('active'));
  document.getElementById(id).classList.add('active');
}

function thinkAgain(msgId) {
  document.getElementById(msgId).innerHTML = "Think again 😌💭";
}
</script>

</body>
</html>
