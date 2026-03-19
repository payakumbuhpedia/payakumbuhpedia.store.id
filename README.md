<!DOCTYPE html><html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>PayakumbuhPedia Store</title>
  <style>
    *{box-sizing:border-box}
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
      color: white;
    }header {
  padding: 30px 20px;
  text-align: center;
  animation: fadeIn 1.2s ease;
}

h1 {font-size: 26px;margin:0}
p {font-size: 13px;opacity: .85;margin:6px 0}

.verified {color:#00ffcc;font-size:12px}

.container {padding: 15px}

.card {
  background: rgba(255,255,255,0.08);
  margin: 15px 0;
  padding: 18px;
  border-radius: 16px;
  backdrop-filter: blur(12px);
  animation: slideUp 0.8s ease;
  box-shadow: 0 8px 20px rgba(0,0,0,0.2);
}

h2 {margin:0 0 10px}

select, input {
  width: 100%;
  padding: 10px;
  border-radius: 10px;
  border: none;
  margin-top: 8px;
  outline: none;
}

button {
  width: 100%;
  margin-top: 12px;
  padding: 12px;
  border: none;
  border-radius: 12px;
  background: #00ffcc;
  color: black;
  font-weight: bold;
  cursor: pointer;
  transition: .3s;
}

button:hover {background:white}

footer {
  text-align:center;
  margin: 25px 0;
  font-size: 12px;
  opacity: .7;
}

@keyframes fadeIn {
  from {opacity:0;transform:translateY(-20px)}
  to {opacity:1;transform:translateY(0)}
}

@keyframes slideUp {
  from {opacity:0;transform:translateY(30px)}
  to {opacity:1;transform:translateY(0)}
}

  </style>
</head>
<body><header>
  <h1>PayakumbuhPedia Store</h1>
  <p>Jasa Boosting Followers, Like & Views Profesional</p>
  <p class="verified">✔ Terverifikasi oleh @beritapayakumbuh</p>
  <p>@payakumbuhpedia.store.id</p>
</header><div class="container">  <div class="card">
    <h2>Order Followers</h2>
    <label>Username / Link</label>
    <input type="text" id="user1" placeholder="Masukkan username"><label>Jumlah Followers</label>
<select id="jumlah1">
  <option>1000</option>
  <option>2000</option>
  <option>3000</option>
  <option>4000</option>
  <option>5000</option>
  <option>6000</option>
  <option>7000</option>
  <option>8000</option>
  <option>9000</option>
  <option>10000</option>
</select>

<button onclick="order('Followers', 'user1', 'jumlah1')">Order Sekarang</button>

  </div>  <div class="card">
    <h2>Order Like</h2>
    <label>Link Postingan</label>
    <input type="text" id="user2" placeholder="Masukkan link"><label>Jumlah Like</label>
<select id="jumlah2">
  <option>1000</option>
  <option>2000</option>
  <option>3000</option>
  <option>4000</option>
  <option>5000</option>
  <option>6000</option>
  <option>7000</option>
  <option>8000</option>
  <option>9000</option>
  <option>10000</option>
</select>

<button onclick="order('Like', 'user2', 'jumlah2')">Order Sekarang</button>

  </div>  <div class="card">
    <h2>Order Views</h2>
    <label>Link Video</label>
    <input type="text" id="user3" placeholder="Masukkan link video"><label>Jumlah Views</label>
<select id="jumlah3">
  <option>1000</option>
  <option>2000</option>
  <option>3000</option>
  <option>4000</option>
  <option>5000</option>
  <option>6000</option>
  <option>7000</option>
  <option>8000</option>
  <option>9000</option>
  <option>10000</option>
</select>

<button onclick="order('Views', 'user3', 'jumlah3')">Order Sekarang</button>

  </div></div><footer>
  © 2026 PayakumbuhPedia Store
</footer><script>
function order(service, userId, jumlahId) {
  let phone = "6283143490913";
  let user = document.getElementById(userId).value;
  let jumlah = document.getElementById(jumlahId).value;

  if(user === ""){
    alert("Isi data dulu!");
    return;
  }

  let message = `Halo admin PayakumbuhPedia%0A%0ASaya ingin order layanan:%0A- Service: ${service}%0A- Target: ${user}%0A- Jumlah: ${jumlah}%0A%0ATerima kasih`;

  let url = `https://wa.me/${phone}?text=${message}`;
  window.open(url, '_blank');
}
</script></body>
</html>
