  
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>...</title>

<style>
body{
  margin:0;
  background:black;
  overflow:hidden;
  font-family:Arial;
  color:white;
}

/* ORTA YAZI */
#main{
  position:absolute;
  top:50%;
  left:50%;
  transform:translate(-50%,-50%);
  text-align:center;
  font-size:35px;
  z-index:2;
}

/* Canvas arkada kalsın */
canvas{
  position:absolute;
  top:0;
  left:0;
  z-index:1;
}
</style>
</head>

<body>

<div id="main">
  Dostluğumuz bu kadar<br>
  <span style="color:red; font-size:45px;">ÜZGÜNÜM</span><br>
  <span style="color:red;">MERT ŞENKAYA</span>
</div>

<canvas id="c"></canvas>

<script>
// CANVAS
const canvas = document.getElementById("c");
const ctx = canvas.getContext("2d");

canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

// Karakterler
const letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789";
const fontSize = 14;
const columns = Math.floor(canvas.width / fontSize);

const drops = Array(columns).fill(1);

// MATRIX EFEKTİ
function draw(){
  ctx.fillStyle = "rgba(0,0,0,0.08)";
  ctx.fillRect(0,0,canvas.width,canvas.height);

  ctx.fillStyle = "#0f0";
  ctx.font = fontSize + "px monospace";

  for(let i=0;i<drops.length;i++){
    const text = letters[Math.floor(Math.random()*letters.length)];

    ctx.fillText(text, i*fontSize, drops[i]*fontSize);

    if(drops[i]*fontSize > canvas.height && Math.random()>0.975){
      drops[i]=0;
    }

    drops[i]++;
  }
}

setInterval(draw, 33);

// EKRAN BOYUTU DEĞİŞİRSE
window.addEventListener("resize", ()=>{
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;
});
</script>

</body>
</html>
