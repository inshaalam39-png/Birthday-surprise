<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Birthday Surprise</title>

<style>
body{
  margin:0;
  background:black;
  color:white;
  font-family: Arial, sans-serif;
  text-align:center;
}

.page{
  display:none;
  height:100vh;
  justify-content:center;
  align-items:center;
  flex-direction:column;
}

.show{ display:flex; }

button{
  padding:15px 25px;
  font-size:18px;
  border:none;
  border-radius:10px;
  cursor:pointer;
}

.balloon{
  width:60px;
  height:80px;
  border-radius:50%;
  margin:10px;
  animation: float 3s infinite;
}

@keyframes float{
  0%{transform:translateY(0);}
  50%{transform:translateY(-30px);}
  100%{transform:translateY(0);}
}

.cake, .gift{
  font-size:80px;
  cursor:pointer;
}

.letter{
  background:#f5deb3;
  color:black;
  padding:20px;
  width:80%;
  border-radius:10px;
}
</style>
</head>

<body>

<!-- PG 1 -->
<div id="pg1" class="page show">
  <h1>Press You 💖</h1>
  <button onclick="next(2)">Start</button>
</div>

<!-- PG 2 -->
<div id="pg2" class="page">
  <div style="display:flex;">
    <div class="balloon" style="background:red;"></div>
    <div class="balloon" style="background:blue;"></div>
  </div>
  <p>I always want to stay with you.</p>
  <button onclick="next(3)">Next</button>
</div>

<!-- PG 3 -->
<div id="pg3" class="page">
  <p>I want to support you in every situation.</p>
  <p>Your happiness matters to me.</p>
  <p>How was your day?</p>
  <div class="cake" onclick="next(4)">🎂</div>
  <small>Tap the cake</small>
</div>

<!-- PG 4 -->
<div id="pg4" class="page">
  <h2>Cake Cut 🎉</h2>
  <div class="gift" onclick="next(5)">🎁</div>
  <small>Tap the gift</small>
</div>

<!-- PG 5 -->
<div id="pg5" class="page">
  <div class="letter">
    <h2>Happy Birthday 🎂</h2>
    <p>Stay healthy and happy.</p>
    <p>May all your dreams come true.</p>
    <p>Always keep smiling 🌸</p>
  </div>
  <button onclick="next(6)">Final Surprise</button>
</div>

<!-- PG 6 -->
<div id="pg6" class="page">
  <h1>🎈🎈🎈</h1>
  <div style="display:flex; flex-wrap:wrap; justify-content:center;">
    <div class="balloon" style="background:pink;"></div>
    <div class="balloon" style="background:yellow;"></div>
    <div class="balloon" style="background:purple;"></div>
    <div class="balloon" style="background:orange;"></div>
    <div class="balloon" style="background:green;"></div>
    <div class="balloon" style="background:red;"></div>
    <div class="balloon" style="background:blue;"></div>
    <div class="balloon" style="background:cyan;"></div>
  </div>
  <h2>Once Again Happy Birthday 💖</h2>
</div>

<script>
function next(n){
  for(let i=1;i<=6;i++){
    document.getElementById("pg"+i).classList.remove("show");
  }
  document.getElementById("pg"+n).classList.add("show");
}
</script>

</body>
</html>
