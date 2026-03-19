<!DOCTYPE html><html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SMM Panel - PayakumbuhPedia</title><style>
*{margin:0;padding:0;box-sizing:border-box}
body{font-family:'Segoe UI',sans-serif;background:#0f2027;color:#fff}

.container{max-width:420px;margin:auto;padding:15px}

.header{
text-align:center;
padding:20px 10px;
}

.header h1{
font-size:20px;
color:#00ffd5;
}

.badge{
margin-top:8px;
font-size:11px;
}

.badge span{
background:#00ff99;
color:#000;
padding:4px 10px;
border-radius:20px;
}

.card{
background:#1c2b36;
padding:15px;
border-radius:12px;
margin-top:15px;
}

input,select{
width:100%;
padding:10px;
border:none;
border-radius:8px;
margin-top:8px;
}

button{
width:100%;
padding:10px;
margin-top:10px;
border:none;
border-radius:10px;
background:#00ffd5;
color:#000;
font-weight:bold;
}

.stats{
display:flex;
justify-content:space-between;
margin-top:15px;
}

.stat{
flex:1;
margin:5px;
padding:10px;
background:#1c2b36;
border-radius:10px;
text-align:center;
font-size:12px;
}

</style></head><body><div class="container"><div class="header">
<h1>PayakumbuhPedia Panel</h1>
<p style="font-size:12px">SMM Panel Indonesia</p><div class="badge">
<span>🟢 Online 24 Jam</span>
</div>
</div><div class="stats">
<div class="stat">👤 10K+ User</div>
<div class="stat">📦 50K+ Order</div>
<div class="stat">⚡ Fast</div>
</div><div class="card">
<h3 style="font-size:14px">Buat Order</h3><select id="layanan">
<option>Followers Instagram</option>
<option>Like Instagram</option>
<option>Views TikTok</option>
</select><input type="text" id="target" placeholder="Username / Link"><select id="jumlah">
<option>1000</option>
<option>5000</option>
<option>10000</option>
</select><button onclick="order()">Kirim Order</button>

</div><div class="card">
<h3 style="font-size:14px">Status Order</h3>
<input type="text" placeholder="Masukkan ID Order">
<button>Cek Status</button>
</div></div><script>
function order(){
let layanan=document.getElementById('layanan').value;
let target=document.getElementById('target').value;
let jumlah=document.getElementById('jumlah').value;

if(target===''){alert('Harap isi data terlebih dahulu');return}

let pesan = `Halo Admin PayakumbuhPedia 👋%0A%0A`+
`Saya ingin melakukan pemesanan dengan detail berikut:%0A`+
`━━━━━━━━━━━━━━━%0A`+
`📌 Layanan : ${layanan}%0A`+
`🎯 Target  : ${target}%0A`+
`📊 Jumlah  : ${jumlah}%0A`+
`━━━━━━━━━━━━━━━%0A%0A`+
`Mohon diproses ya kak 🙏%0A`+
`Terima kasih ✨`;

window.open(`https://wa.me/6283143490913?text=${pesan}`)
}

window.open(`https://wa.me/6283143490913?text=Order ${l} ${t} ${j}`)
}
</script></body>
</html>
