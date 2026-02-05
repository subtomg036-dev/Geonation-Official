<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Geonation Store</title>

<link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">

<style>
*{box-sizing:border-box;margin:0;padding:0}

body{
  font-family:'Press Start 2P', cursive;
  background:radial-gradient(circle at top,#103010,#000);
  color:#fff;
  min-height:100vh;
  overflow-x:hidden;
}

/* ANIMATIONS */
@keyframes logoGlow {
  0%{text-shadow:0 0 10px #1faa1f}
  50%{text-shadow:0 0 30px #1faa1f,0 0 60px #1faa1f}
  100%{text-shadow:0 0 10px #1faa1f}
}
@keyframes float {
  0%,100%{transform:translateY(0)}
  50%{transform:translateY(-6px)}
}
@keyframes fadeUp {
  from{opacity:0;transform:translateY(40px)}
  to{opacity:1;transform:translateY(0)}
}

/* HEADER */
header{
  display:flex;
  align-items:center;
  padding:22px 40px;
  gap:25px;
}

.logo{
  font-size:26px;
  color:#1faa1f;
  cursor:pointer;
  animation:logoGlow 2.5s infinite;
}

/* NAV */
.nav-buttons{
  display:flex;
  gap:12px;
}
.nav-buttons button{
  padding:10px 16px;
  border-radius:18px;
  border:none;
  background:#1faa1f;
  font-size:10px;
  cursor:pointer;
  animation:float 3s infinite;
  transition:.3s;
}
.nav-buttons button:hover{
  transform:scale(1.15);
}

/* SOCIALS */
.socials{
  margin-left:auto;
  display:flex;
  gap:12px;
}
.social-btn{
  padding:8px 14px;
  border-radius:18px;
  font-size:9px;
  cursor:pointer;
  animation:float 2.8s infinite;
  transition:.3s;
}
.social-btn:hover{transform:scale(1.15)}
.tiktok{background:#ff0050;color:#000}
.discord{background:#5865F2;color:#000}

/* PAGES */
.page{
  display:none;
  padding:70px 30px;
  text-align:center;
  animation:fadeUp .6s ease;
}
.page.active{display:block}

/* TITLE */
h1{
  font-size:38px;
  margin-bottom:60px;
}

/* STORE GRID */
.store-grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
  gap:35px;
  max-width:1200px;
  margin:auto;
}

/* CARD */
.store-card{
  background:linear-gradient(180deg,#0f1f0f,#000);
  border:2px solid #1faa1f;
  border-radius:26px;
  padding:32px 26px;
  position:relative;
  overflow:hidden;
  transition:.35s;
}
.store-card:hover{
  transform:translateY(-14px) scale(1.06);
  box-shadow:0 0 40px rgba(31,170,31,.8);
}

/* BADGE */
.badge{
  position:absolute;
  top:15px;
  right:15px;
  background:#1faa1f;
  color:#000;
  padding:6px 10px;
  font-size:9px;
  border-radius:12px;
  animation:float 2s infinite;
}

/* ICON */
.store-icon{
  width:56px;
  height:56px;
  margin:auto;
  margin-bottom:20px;
  border-radius:16px;
  background:#1faa1f;
  color:#000;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:20px;
  animation:float 3s infinite;
}

/* TEXT */
.store-title{
  font-size:15px;
  color:#1faa1f;
  margin-bottom:14px;
}
.store-list{
  font-size:10px;
  line-height:2;
  text-align:left;
  margin-bottom:18px;
}
.store-price{
  font-size:12px;
  margin-bottom:8px;
}
.old-price{
  text-decoration:line-through;
  opacity:.5;
  font-size:10px;
}

/* TIMER */
.timer{
  font-size:10px;
  margin-bottom:15px;
  color:#00ff88;
}

/* BUTTON */
.store-btn{
  width:100%;
  padding:14px;
  border-radius:16px;
  border:none;
  background:#1faa1f;
  color:#000;
  font-size:11px;
  cursor:pointer;
}

/* HOME */
.info{
  font-size:12px;
  line-height:2.4;
}
.status{color:#00ff00}
</style>
</head>

<body>

<header>
  <div class="logo" onclick="showPage('home')">Geonation</div>

  <div class="nav-buttons">
    <button onclick="showPage('vip')">VIP Ranks</button>
    <button onclick="showPage('keys')">Buy Keys</button>
  </div>

  <div class="socials">
    <a class="social-btn tiktok" href="https://www.tiktok.com/@mc_itzzmg" target="_blank">TikTok</a>
    <a class="social-btn tiktok" href="https://www.tiktok.com/@mastrasss._" target="_blank">TikTok</a>
    <a class="social-btn discord" href="https://discord.gg/tcvtMVpj" target="_blank">Discord</a>
  </div>
</header>

<section id="home" class="page active">
  <h1>Geonation</h1>
  <div class="info">
    <p>Server IP: 91.197.6.16:22976</p>
    <p>Status: <span class="status">ONLINE</span></p>
  </div>
</section>

<section id="vip" class="page">
  <h1>VIP Ranks</h1>

  <div class="store-grid">
    <div class="store-card">
      <div class="store-icon">★</div>
      <div class="store-title">VIP</div>
      <div class="store-list">
        ✔ Unique Kit<br>
        ✔ /feed<br>
        ✔ Extra homes
      </div>
      <div class="store-price">5 GEL</div>
      <button class="store-btn">ყიდვა</button>
    </div>

    <div class="store-card">
      <div class="badge">-20%</div>
      <div class="store-icon">★★</div>
      <div class="store-title">+VIP</div>
      <div class="store-list">
        ✔ All VIP perks<br>
        ✔ /fly<br>
        ✔ More commands
      </div>
      <div class="old-price">10 GEL</div>
      <div class="store-price" id="vipPrice">8 GEL</div>
      <div class="timer" id="vipTimer"></div>
      <button class="store-btn">ყიდვა</button>
    </div>
  </div>
</section>

<section id="keys" class="page">
  <h1>Buy Keys</h1>
</section>

<script>
function showPage(id){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.getElementById(id).classList.add('active');
}

/* TIMER LOGIC */
const endTime = new Date();
endTime.setMonth(endTime.getMonth() + 1);

const timerEl = document.getElementById("vipTimer");
const priceEl = document.getElementById("vipPrice");

function updateTimer(){
  const now = new Date();
  const diff = endTime - now;

  if(diff <= 0){
    timerEl.textContent = "Offer ended";
    priceEl.textContent = "10 GEL";
    return;
  }

  const days = Math.floor(diff / (1000*60*60*24));
  const hours = Math.floor((diff / (1000*60*60)) % 24);
  const mins = Math.floor((diff / (1000*60)) % 60);

  timerEl.textContent = `Ends in ${days}d ${hours}h ${mins}m`;
}

updateTimer();
setInterval(updateTimer,60000);
</script>

</body>
</html>
