<!DOCTYPE html><html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PayakumbuhPedia Extreme</title><style>
*{margin:0;padding:0;box-sizing:border-box}

body{
font-family:'Segoe UI',sans-serif;
background:#0f2027;
color:#fff;
overflow-x:hidden;
}

/* PARALLAX BACKGROUND */
.bg{
position:fixed;
width:100%;
height:100%;
background:radial-gradient(circle at 30% 30%,#00ffd5,transparent),
radial-gradient(circle at 70% 70%,#0077ff,transparent);
opacity:.08;
animation:move 12s infinite linear;
z-index:-1;
}

@keyframes move{
0%{transform:translate(0,0)}
50%{transform:translate(-10%,-10%)}
100%{transform:translate(0,0)}
}

.wrapper{
max-width:400px;
margin:auto;
padding:15px;
}

/* SPLASH INTRO */
#intro{
position:fixed;
width:100%;
height:100%;
background:#0f2027;
display:flex;
justify-content:center;
align-items:center;
font-size:22px;
font-weight:bold;
z-index:999;
animation:fadeOut 1s ease 2s forwards;
}

@keyframes fadeOut{
to{opacity:0;visibility:hidden}
}

header{
text-align:center;
padding:20px 10px;
animation:fadeIn 1s;
}

h1{
font-size:22px;
background:linear-gradient(90deg,#00ffd5,#0077ff);
-webkit-background-clip:text;
color:transparent;
}

p{font-size:12px;opacity:.85}

.badge span{
background:#00ff99;
color:#000;
padding:5px 10px;
border-radius:20px;
font-size:11px;
}

.counter,.timer{font-size:11px;margin-top:6px}
.timer{color:#ffd54f}

.card{
margin-top:15px;
padding:15px;
border-radius:14px;
background:rgba(255,255,255,0.05);
backdrop-filter:blur(14px);
box-shadow:0 0 20px rgba(0,255,200,0.1);
transition:.3s;
}

.card:hover{
transform:scale(1.02);
box-shadow:0 0 25px rgba(0,255,200,0.4);
}

input,select{
width:100%;
padding:10px;
border:none;
border-radius:10px;
margin-top:8px;
}

button{
width:100%;
padding:11px;
margin-top:10px;
border:none;
border-radius:12px;
background:linear-gradient(90deg,#00ffd5,#0077ff);
color:#000;
font-weight:bold;
cursor:pointer;
transition:.2s;
}

button:active{
transform:scale(0.96);
}

.nav{display:flex;margin-top:15px;background:rgba(255,255,255,0.08);border-radius:12px;padding:5px}
.nav button{flex:1;background:transparent;border:none;color:#fff;padding:8px;border-radius:10px}
.nav button.active{background:#00ffd5;color:#000}

.hidden{display:none}

.popup{
position:fixed;
bottom:20px;
left:50%;
transform:translateX(-50%);
background:#00ffd5;
color:#000;
padding:8px 12px;
border-radius:10px;
font-size:11px;
display:none;
}

</style></head><body><div id="intro">PayakumbuhPedia</div>
<div class="bg"></div><div class="wrapper">
<header>
<h1>PayakumbuhPedia</h1>
<p>Boosting Sosial Media Profesional</p><div class="badge"><span>🟢 Online 24 Jam</span></div>
<div class="counter">📊 <span id="c">0</span>+ Order</div>
<div class="timer">⏳ Promo: <span id="t">05:00</span></div>
</header><div class="nav">
<button class="active" onclick="tab(1,this)">Followers</button>
<button onclick="tab(2,this)">Like</button>
<button onclick="tab(3,this)">Views</button>
</div><div id="tab1" class="card">
<input id="u1" placeholder="Username">
<select id="j1"><option>1000</option><option>5000</option><option>10000</option></select>
<button onclick="go('Followers','u1','j1')">Order</button>
</div><div id="tab2" class="card hidden">
<input id="u2" placeholder="Link">
<select id="j2"><option>1000</option><option>5000</option><option>10000</option></select>
<button onclick="go('Like','u2','j2')">Order</button>
</div><div id="tab3" class="card hidden">
<input id="u3" placeholder="Link">
<select id="j3"><option>1000</option><option>5000</option><option>10000</option></select>
<button onclick="go('Views','u3','j3')">Order</button>
</div></div><div class="popup" id="pop"></div><script>
function tab(n,b){['tab1','tab2','tab3'].forEach(x=>document.getElementById(x).classList.add('hidden'));document.getElementById('tab'+n).classList.remove('hidden');document.querySelectorAll('.nav button').forEach(x=>x.classList.remove('active'));b.classList.add('active');}

function go(s,u,j){let v=document.getElementById(u).value;if(v===''){alert('isi dulu');return}window.open(`https://wa.me/6283143490913?text=${s} ${v}`)}

// counter
let i=0;setInterval(()=>{if(i<10000){i+=100;document.getElementById('c').innerText=i}},20);

// timer
let t=300;setInterval(()=>{let m=Math.floor(t/60),s=t%60;document.getElementById('t').innerText=`${m}:${s<10?'0'+s:s}`;if(t>0)t--},1000);

// popup
let n=["Andi","Rizky","Dina","Putra","Budi","Fajar","Rian","Yoga","Putri","Salsa"];
setInterval(()=>{let name=n[Math.floor(Math.random()*n.length)];let p=document.getElementById('pop');p.innerText=name+" order";p.style.display='block';setTimeout(()=>p.style.display='none',3000)},5000);
</script></body>
</html>
