<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>جاري الدخول</title>

<style>
body{
  margin:0;
  height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
  background:#0f0f0f;
  font-family: Arial, sans-serif;
  color:white;
}

.box{
  text-align:center;
}

button{
  margin-top:20px;
  padding:12px 25px;
  border:none;
  border-radius:8px;
  background:#00c2ff;
  font-size:16px;
  font-weight:bold;
  cursor:pointer;
}

button:hover{
  background:#00a3d6;
}
</style>

<script>
let seconds = 3;

function startRedirect(){
  let interval = setInterval(() => {
    seconds--;
    document.getElementById("count").innerText = seconds;

    if(seconds <= 0){
      clearInterval(interval);
      window.location.href = "https://trading-goals-zfih.arcada.app/";
    }
  }, 1000);
}

function manual(){
  window.location.href = "https://trading-goals-zfih.arcada.app/";
}
</script>

</head>

<body onload="startRedirect()">

<div class="box">
  <h2>جاري تحويلك للموقع</h2>
  <p>سيتم التحويل خلال <span id="count">3</span> ثواني</p>

  <button onclick="manual()">دخول الآن</button>
</div>

</body>
</html>
