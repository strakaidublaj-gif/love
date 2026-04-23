<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Matrix</title>
<style>
  body { margin:0; background:black; overflow:hidden; }
  canvas { display:block; }
</style>
</head>
<body>

<canvas id="c"></canvas>

<script>
const canvas = document.getElementById("c");
const ctx = canvas.getContext("2d");

canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

// Matrix karakterleri
const letters = "01ABCDEFGHIJKLMNOPQRSTUVWXYZ";
const fontSize = 16;
const columns = Math.floor(canvas.width / fontSize);

// Her sütunun düşüş pozisyonu
const drops = Array(columns).fill(1);

// 🖕 ASCII mask (1 olan yerler daha parlak)
const mask = [
"000111000",
"000111000",
"000111000",
"000111000",
"000111000",
"001111100",
"001101100",
"001101100",
"001101100",
"011101110",
"111111111"
];

function draw() {
  ctx.fillStyle = "rgba(0,0,0,0.1)";
  ctx.fillRect(0, 0, canvas.width, canvas.height);

  ctx.font = fontSize + "px monospace";

  for (let i = 0; i < drops.length; i++) {
    const text = letters[Math.floor(Math.random() * letters.length)];
    const x = i * fontSize;
    const y = drops[i] * fontSize;

    // Mask içindeyse daha parlak yap
    let bright = false;
    const mx = Math.floor(x / (canvas.width / mask[0].length));
    const my = Math.floor(y / (canvas.height / mask.length));

    if (mask[my] && mask[my][mx] === "1") {
      bright = true;
    }

    ctx.fillStyle = bright ? "#00FF00" : "#0f0";
    ctx.fillText(text, x, y);

    if (y > canvas.height && Math.random() > 0.975) {
      drops[i] = 0;
    }

    drops[i]++;
  }
}

setInterval(draw, 33);
</script>

</body>
</html>
