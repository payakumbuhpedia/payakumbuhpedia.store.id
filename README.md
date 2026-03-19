<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PayakumbuhPedia Panel</title>

<style>
*{margin:0;padding:0;box-sizing:border-box}

body{
font-family:'Segoe UI',sans-serif;
background:#0f2027;
color:#fff;
overflow-x:hidden;
animation:fadeIn 1s ease;
}

/* ANIMASI MASUK */
@keyframes fadeIn{
from{opacity:0;transform:translateY(20px)}
to{opacity:1;transform:translateY(0)}
}

/* BACKGROUND GLOW */
.bg{
position:fixed;
width:100%;
height:100%;
background:
radial-gradient(circle at 20% 30%, #00ffd5, transparent),
radial-gradient(circle at 80% 70%, #0077ff, transparent);
opacity:0.08;
animation:move 10s linear infinite;
z-index:-1;
}

@keyframes move{
0%{transform:translate(0,0)}
50%{transform:translate(-10%,-10%)}
100%{transform:translate(0,0)}
}

.container{
max-width:420px;
margin:auto;
padding:16px;
}

/* HEADER */
.header{
text-align:center;
padding:18px 10px;
border-bottom:1px solid rgba(255,255,255,0.08);
}

.brand{
font-size:22px;
font-weight:700;
background:linear-gradient(90deg,#00ffd5,#00aaff);
-webkit-background-clip:text;
color:transparent;
}

.subtitle{
font-size:12px;
opacity:.8;
margin-top:4px;
}

.badge span{
background:#00ff99;
color:#000;
padding:5px 12px;
border-radius:20px;
font-size:11px;
box-shadow:0 0 10px #00ff99;
}

/* STATS */
.stats{
display:flex;
gap:8px;
margin-top:14px;
}

.stat{
flex:1;
background:rgba(255,255,255,0.05);
padding:10px;
border-radius:12px;
text-align:center;
font-size:12px;
backdrop-filter:blur(10px);
}

/* CARD */
.card{
background:rgba(255,255,255,0.05);
padding:14px;
border-radius:16px;
margin-top:14px;
backdrop-filter:blur(12px);
transition:.3s;
}

.card:hover{
transform:scale(1.02);
box-shadow:0 0 25px rgba(0,255,200,0.3);
}

.title{
font-size:14px;
margin-bottom:6px;
}

input,select{
width:100%;
padding:10px;
border:none;
border-radius:10px;
margin-top:8px;
font-size:12px;
outline:none;
}

/* BUTTON PREMIUM */
button{
width:100%;
padding:12px;
margin-top:10px;
border:none;
border-radius:12px;
background:linear-gradient(90deg,#00ffd5,#00aaff);
color:#000;
font-weight:bold;
cursor:pointer;
position:relative;
overflow:hidden;
}

/* SHINE EFFECT */
button::before{
content:'';
position:absolute;
width:100%;
height:100%;
top:0;
left:-100%;
background:linear-gradient(120deg,transparent,rgba(255,255,255,0.6),transparent);
transition:0.5s;
}

button:hover::before{
left:100%;
}

button:active{
transform:scale(.96);
}

footer{
text-align:center;
margin-top:20px;
font-size:11px;
opacity:.6;
}
</style>
</head>

<body>

<div class="bg"></div>

<div class="container">

<div class="header">
<div class="brand">PayakumbuhPedia</div>
<div class="subtitle">SMM Panel Indonesia • Boosting Profesional</div>
<br>
<div class="badge"><span>🟢 Online 24 Jam</span></div>
</div>

<div class="stats">
<div class="stat">👤 10K+ User</div>
<div class="stat">📦 50K+ Order</div>
<div class="stat">⚡ Cepat</div>
</div>

<div class="card">
<div class="title">Buat Order</div>

<select id="layanan">
<option>Followers Instagram Indonesia</option>
<option>Followers TikTok Indonesia</option>
<option>Like Instagram Indonesia</option>
<option>Like TikTok Indonesia</option>
<option>Views Instagram Indonesia</option>
<option>Views TikTok Indonesia</option>
</select>

<input type="text" id="target" placeholder="Username / Link">

<select id="jumlah">
<option>1000</option>
<option>2000</option>
<option>3000</option>
<option>5000</option>
<option>10000</option>
</select>

<button onclick="order()">Kirim Order</button>
</div>

<footer>
© 2026 PayakumbuhPedia • Hak Cipta Dilindungi Undang-Undang
</footer>

</div>

<script>
function order(){
let layanan=document.getElementById('layanan').value;
let target=document.getElementById('target').value;
let jumlah=document.getElementById('jumlah').value;

if(target===''){
alert('Isi data dulu');
return;
}

let pesan =
`Halo Admin PayakumbuhPedia 👋%0A%0A`+
`Saya ingin order:%0A━━━━━━━━━━━━━━━%0A`+
`📌 Layanan : ${layanan}%0A`+
`🎯 Target  : ${target}%0A`+
`📊 Jumlah  : ${jumlah}%0A`+
`━━━━━━━━━━━━━━━%0A`+
`Mohon diproses 🙏%0ATerima kasih ✨`;

window.open(`https://wa.me/6283143490913?text=${pesan}`);
}
</script>

</body>
</html>
