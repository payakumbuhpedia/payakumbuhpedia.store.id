
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Panel</title><style>
*{margin:0;padding:0;box-sizing:border-box}
body{font-family:'Segoe UI',sans-serif;background:#0f2027;color:#fff}

.container{max-width:420px;margin:auto;padding:16px}

/* HEADER PREMIUM */
.header{
text-align:center;
padding:18px 10px 10px;
border-bottom:1px solid rgba(255,255,255,0.08);
}

.brand{
font-size:20px;
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

.link{
font-size:11px;
color:#00ffd5;
text-decoration:none;
display:inline-block;
margin-top:6px;
}

.badge{
margin-top:10px;
}

.badge span{
background:#00ff99;
color:#000;
padding:4px 10px;
border-radius:20px;
font-size:11px;
}

.stats{
display:flex;
gap:8px;
margin-top:14px;
}

.stat{
flex:1;
background:rgba(255,255,255,0.06);
padding:10px;
border-radius:12px;
text-align:center;
font-size:12px;
}

.card{
background:rgba(255,255,255,0.06);
padding:14px;
border-radius:14px;
margin-top:14px;
backdrop-filter:blur(10px);
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
}

button{
width:100%;
padding:11px;
margin-top:10px;
border:none;
border-radius:12px;
background:linear-gradient(90deg,#00ffd5,#00aaff);
color:#000;
font-weight:bold;
cursor:pointer;
}

button:active{transform:scale(.97)}

</style></head><body><div class="container"><div class="header">
<div class="brand"></div>
<div class="subtitle">SMM Panel Indonesia • Boosting Profesional</div><div class="badge"><span>🟢 Online 24 Jam</span></div>
</div><div class="stats">
<div class="stat">👤 10K+ User</div>
<div class="stat">📦 50K+ Order</div>
<div class="stat">⚡ Cepat</div>
</div><div class="card">
<div class="title">Buat Order</div><select id="layanan">
<option>Followers Instagram Indonesia</option>
<option>Followers TikTok Indonesia</option>
<option>Like Instagram Indonesia</option>
<option>Like TikTok Indonesia</option>
<option>Views Instagram Indonesia</option>
<option>Views TikTok Indonesia</option>
</select><input type="text" id="target" placeholder="Username / Link"><select id="jumlah">
<option>1000</option>
<option>2000</option>
<option>3000</option>
<option>5000</option>
<option>10000</option>
</select><button onclick="order()">Kirim Order</button>

</div></div><footer style="text-align:center;margin-top:20px;font-size:11px;opacity:.6;">
© 2026 PayakumbuhPedia • Hak Cipta Dilindungi Undang-Undang
</footer><script>
function order(){
let layanan=document.getElementById('layanan').value;
let target=document.getElementById('target').value;
let jumlah=document.getElementById('jumlah').value;

if(target===''){alert('Isi data dulu');return}

let pesan = `Halo Admin PayakumbuhPedia 👋%0A%0A`+
`Saya ingin order:%0A━━━━━━━━━━━━━━━%0A`+
`📌 Layanan : ${layanan}%0A`+
`🎯 Target  : ${target}%0A`+
`📊 Jumlah  : ${jumlah}%0A`+
`━━━━━━━━━━━━━━━%0A`+
`Mohon diproses 🙏%0ATerima kasih ✨`;

window.open(`https://wa.me/6283143490913?text=${pesan}`)
}
</script></body>
