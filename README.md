<!DOCTYPE html><html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PayakumbuhPedia Ultra</title><style>
*{margin:0;padding:0;box-sizing:border-box}
body{font-family:'Segoe UI',sans-serif;background:linear-gradient(135deg,#0f2027,#203a43,#2c5364);color:#fff}
.wrapper{max-width:420px;margin:auto;padding:15px}
header{text-align:center;padding:20px 10px;animation:fadeIn 1s}
h1{font-size:20px}
p{font-size:12px;opacity:.85}
.verified{color:#00ffd5;font-size:11px}

.badge{margin-top:8px}
.badge span{background:#00ff99;color:#000;padding:4px 8px;border-radius:8px;font-size:11px}

.counter{margin-top:6px;font-size:11px}

.testi{margin-top:10px;font-size:11px;background:rgba(255,255,255,0.05);padding:8px;border-radius:10px}

.best{margin-top:6px}
.best span{background:#ffd700;color:#000;padding:4px 8px;border-radius:8px;font-size:11px}

.nav{display:flex;background:rgba(255,255,255,0.08);border-radius:12px;padding:5px;margin-top:15px}
.nav button{flex:1;background:transparent;border:none;color:#fff;padding:8px;border-radius:10px;font-size:12px}
.nav button.active{background:#00ffd5;color:#000;font-weight:bold}

.card{margin-top:15px;padding:15px;border-radius:14px;background:rgba(255,255,255,0.07);backdrop-filter:blur(10px);animation:slideUp .5s}
input,select{width:100%;padding:9px;border:none;border-radius:9px;margin-top:6px;font-size:12px}

button.order{width:100%;padding:10px;margin-top:10px;border:none;border-radius:10px;background:#00ffd5;color:#000;font-weight:bold;cursor:pointer;position:relative}
button.order:active::after{content:"";position:absolute;width:100%;height:100%;background:rgba(255,255,255,0.3);top:0;left:0;animation:ripple .4s}
button.order:hover{background:#fff;box-shadow:0 0 10px #00ffd5}

footer{margin-top:20px;padding:15px;text-align:center;font-size:11px;opacity:.7;border-top:1px solid rgba(255,255,255,0.1)}
.hidden{display:none}

/* popup notif */
.popup{position:fixed;bottom:20px;left:50%;transform:translateX(-50%);background:#00ffd5;color:#000;padding:8px 12px;border-radius:10px;font-size:11px;display:none;box-shadow:0 5px 15px rgba(0,0,0,0.3)}

/* timer */
.timer{margin-top:8px;font-size:11px;color:#ffcc00}

@keyframes ripple{from{opacity:1}to{opacity:0}}
@keyframes fadeIn{from{opacity:0;transform:translateY(-15px)}to{opacity:1;transform:translateY(0)}}
@keyframes slideUp{from{opacity:0;transform:translateY(20px)}to{opacity:1;transform:translateY(0)}}
</style></head><body>
<div class="wrapper"><header>
<h1>PayakumbuhPedia</h1>
<p>Boosting Sosial Media Profesional</p>
<p class="verified">✔ Terverifikasi @beritapayakumbuh</p>
<p>@payakumbuhpedia.store.id</p><div class="badge"><span>🟢 Online 24 Jam</span></div>
<div class="counter">📊 <span id="counter">0</span>+ Order Berhasil</div>
<div class="timer">⏳ Promo berakhir dalam: <span id="time">05:00</span></div>
<div class="testi">💬 “Followers masuk cepat & aman, recommended!”</div>
<div class="best"><span>🔥 Best Seller</span></div>
</header><div class="nav">
<button class="active" onclick="showTab(1,this)">Followers</button>
<button onclick="showTab(2,this)">Like</button>
<button onclick="showTab(3,this)">Views</button>
</div><div id="tab1" class="card">
<input id="u1" placeholder="Username / Link">
<select id="j1">
<option>1000</option><option>2000</option><option>3000</option><option>4000</option><option>5000</option><option>6000</option><option>7000</option><option>8000</option><option>9000</option><option>10000</option>
</select>
<button class="order" onclick="kirim('Followers','u1','j1')">Order</button>
</div><div id="tab2" class="card hidden">
<input id="u2" placeholder="Link Postingan">
<select id="j2">
<option>1000</option><option>2000</option><option>3000</option><option>4000</option><option>5000</option><option>6000</option><option>7000</option><option>8000</option><option>9000</option><option>10000</option>
</select>
<button class="order" onclick="kirim('Like','u2','j2')">Order</button>
</div><div id="tab3" class="card hidden">
<input id="u3" placeholder="Link Video">
<select id="j3">
<option>1000</option><option>2000</option><option>3000</option><option>4000</option><option>5000</option><option>6000</option><option>7000</option><option>8000</option><option>9000</option><option>10000</option>
</select>
<button class="order" onclick="kirim('Views','u3','j3')">Order</button>
</div><footer>
<div>WhatsApp</div>
<div>083143490913</div>
<div style="margin-top:5px">© 2026 PayakumbuhPedia</div>
</footer></div><div class="popup" id="popup"></div><script>
function showTab(n,btn){
let tabs=["tab1","tab2","tab3"];
tabs.forEach(id=>document.getElementById(id).classList.add("hidden"));
document.getElementById("tab"+n).classList.remove("hidden");

let buttons=document.querySelectorAll(".nav button");
buttons.forEach(b=>b.classList.remove("active"));
btn.classList.add("active");
}

function kirim(service,u,j){
let phone="6283143490913";
let user=document.getElementById(u).value;
let jumlah=document.getElementById(j).value;
if(user===""){alert("Isi data dulu!");return}
let text=`Halo admin PayakumbuhPedia%0A%0ASaya ingin order:%0A- Layanan: ${service}%0A- Target: ${user}%0A- Jumlah: ${jumlah}%0A%0ATerima kasih`;
window.open(`https://wa.me/${phone}?text=${text}`,'_blank');
}

// counter
let count=0,target=10000;
function animCounter(){if(count<target){count+=100;document.getElementById('counter').innerText=count;setTimeout(animCounter,5)}}
animCounter();

// timer
let total=300;
setInterval(()=>{
let m=Math.floor(total/60);
let s=total%60;
document.getElementById('time').innerText=`${m}:${s<10?'0'+s:s}`;
if(total>0) total--;
},1000);

// fake popup notif
let names=["Andi","Rizky","Dina","Fajar","Putri","Budi"];
function showPopup(){
let name=names[Math.floor(Math.random()*names.length)];
let popup=document.getElementById('popup');
popup.innerText=`${name} baru saja order`;
popup.style.display='block';
setTimeout(()=>popup.style.display='none',3000);
}
setInterval(showPopup,6000);
</script></body>
</html>
