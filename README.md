<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Birthday Surprise ❤️</title>
  <style>
    body{font-family:Arial,sans-serif;margin:0;background:linear-gradient(135deg,#ffe4e6,#fdf2f8,#f3e8ff);display:flex;justify-content:center;align-items:center;min-height:100vh;padding:20px}
    .card{max-width:900px;width:100%;background:rgba(255,255,255,.85);padding:30px;border-radius:24px;box-shadow:0 10px 30px rgba(0,0,0,.1);text-align:center}
    .grid{display:grid;grid-template-columns:repeat(4,1fr);gap:12px;margin:20px 0}
    .box{background:#fce7f3;padding:16px;border-radius:18px}
    .photos{display:grid;grid-template-columns:repeat(2,1fr);gap:12px}
    .photos img{width:100%;height:260px;object-fit:cover;border-radius:20px}
  </style>
</head>
<body>
  <div class="card">
    <h1>🎂 Happy Birthday Meri Dharm Patni Jii 😚💗</h1>
    <p>Happy Birthday meri pyari Dharm Patni Jii ❤️ Aap meri zindagi ki sabse pyari khushi ho.</p><audio autoplay loop>
  <source src="https://drive.google.com/uc?export=download&id=1FC61Ep6p0MK3YagAFu0vpF-07mwCg7jo" type="audio/mpeg">
</audio>

<div class="grid">
  <div class="box"><div id="days">0</div><small>Days</small></div>
  <div class="box"><div id="hours">0</div><small>Hours</small></div>
  <div class="box"><div id="minutes">0</div><small>Minutes</small></div>
  <div class="box"><div id="seconds">0</div><small>Seconds</small></div>
</div>

<h2>📸 Our Cute Photos</h2>
<div class="photos">
  <img src="https://drive.google.com/uc?export=view&id=1dCllkGufaA-9Uu1SOxgGLtKC2qZEXVjl" />
  <img src="https://drive.google.com/uc?export=view&id=1QU7AeSbRlaugruhEqV0ll5KP3jQcKTGV" />
</div>

  </div><script>
const target = new Date('2026-04-12T00:00:00').getTime();
setInterval(()=>{
 const now = new Date().getTime();
 const diff = target-now;
 document.getElementById('days').innerText = Math.max(0, Math.floor(diff/(1000*60*60*24)));
 document.getElementById('hours').innerText = Math.max(0, Math.floor((diff/(1000*60*60))%24));
 document.getElementById('minutes').innerText = Math.max(0, Math.floor((diff/(1000*60))%60));
 document.getElementById('seconds').innerText = Math.max(0, Math.floor((diff/1000)%60));
},1000);
</script></body>
</html>
