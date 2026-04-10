<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Birthday Meli Pyali Biwi Jii ❤️</title>

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:sans-serif;}
body{
  background: linear-gradient(to bottom,#ff758c,#ff7eb3);
  color:white;text-align:center;overflow-x:hidden;
}
section{
  height:100vh;display:flex;flex-direction:column;
  justify-content:center;align-items:center;padding:20px;
}
h1{font-size:45px;}
.gallery img{
  width:200px;margin:10px;border-radius:15px;
}

/* floating hearts */
.heart{
  position:absolute;animation:float 5s linear infinite;
}
@keyframes float{
  0%{transform:translateY(100vh);}
  100%{transform:translateY(-10vh);}
}

/* cake */
.cake{position:relative;width:200px;height:150px;margin-top:20px;}
.layer{
  width:200px;height:100px;background:#ff4b5c;
  border-radius:10px;position:absolute;bottom:0;
}
.candles{
  display:flex;justify-content:space-around;
  position:absolute;width:100%;top:-30px;
}
.flame{
  width:10px;height:30px;background:orange;
  border-radius:50%;animation:flicker 0.3s infinite;
}
@keyframes flicker{
  0%{transform:scale(1);}
  50%{transform:scale(1.2);}
  100%{transform:scale(1);}
}

/* wish text */
#wishText{
  margin-top:20px;
  font-size:22px;
  opacity:0.8;
}
</style>
</head>

<body>

<audio autoplay loop>
  <source src="HAPPY BIRTHDAY TO YOU PIANO INSTRUMENTAL BEST HAPPY BITHDAY MUSIC 2021 - Happy Birthday Music.mp3" type="audio/mpeg">
</audio>

<section>
  <h1>🎂 Happy Birthday</h1>
  <h1>Meli Pyali Biwi Jii ❤️</h1>
  <p>Scroll karo mela bacchaa 😘</p>
</section>

<section>
  <h1>💖 From Someone Who Loves You</h1>
</section>

<section>
  <h1>📸 Memories</h1>
  <div class="gallery">
    <img src="IMG_20260312_225123.jpg">
    <img src="IMG_20260312_225139.jpg">
    <img src="Screenshot_20260312_200303.jpg">
  </div>
</section>

<section>
  <h1>💌 Message</h1>
  <p>
Meri pyari jaan, aap meri zindagi ki sabse khoobsurat gift ho Mela Bacchaaa ❤️ <br><br>
Aapki muskaan meri duniya ko roshan kar deti hai meli pyali biwi jii ✨ <br><br>
Jab bhi aap paas hoti ho, har problem chhoti lagti hai Mela Bacchaaa 🥰 <br><br>
Aap meri life ka sabse important hissa ho Mela Bacchaaa 💖 <br><br>
Main har din bhagwan ka shukriya karta hoon aapko meri zindagi me bhejne ke liye Mela Bacchaaa 🙏 <br><br>
Aapke bina sab kuch adhoora lagta hai meli ardhangini jii 😘 <br><br>
Main hamesha aapko khush rakhne ki koshish karta rahunga Mela Bacchaaa 💕 <br><br>
Aap meri strength bhi ho aur meri weakness bhi ho Mela Bacchaaa 💫 <br><br>
Har pal bas aapke saath bitana chahta hoon Mela Bacchaaa 💑 <br><br>
Happy Birthday meri jaan, aap hamesha aise hi muskuraati raho Mela Bacchaaa 🎂❤️  
  </p>
</section>

<section>
  <h1>🎂 Make a Wish 🎂</h1>

  <div class="cake">
    <div class="candles">
      <div class="flame" id="f1"></div>
      <div class="flame" id="f2"></div>
      <div class="flame" id="f3"></div>
    </div>
    <div class="layer"></div>
  </div>

  <p id="wishText">✨ Make a wish ✨</p>
</section>

<script>
// hearts
setInterval(()=>{
  let heart=document.createElement("div");
  heart.innerHTML="❤️";
  heart.classList.add("heart");
  heart.style.left=Math.random()*100+"vw";
  document.body.appendChild(heart);
  setTimeout(()=>heart.remove(),5000);
},500);

// clap detect
navigator.mediaDevices.getUserMedia({audio:true})
.then(stream=>{
  const ctx=new AudioContext();
  const mic=ctx.createMediaStreamSource(stream);
  const analyser=ctx.createAnalyser();
  mic.connect(analyser);
  analyser.fftSize=256;

  const data=new Uint8Array(analyser.frequencyBinCount);

  function detect(){
    analyser.getByteFrequencyData(data);
    let vol=data.reduce((a,b)=>a+b)/data.length;

    if(vol>60){
      blow();
    }
    requestAnimationFrame(detect);
  }
  detect();
})
.catch(()=>alert("Mic allow karo 😘"));

function blow(){
  document.getElementById("f1").style.display="none";
  document.getElementById("f2").style.display="none";
  document.getElementById("f3").style.display="none";

  document.getElementById("wishText").innerHTML="🎉 Wish Complete 💖";

  confetti();
}

// confetti
function confetti(){
  for(let i=0;i<50;i++){
    let c=document.createElement("div");
    c.style.position="absolute";
    c.style.width="10px";
    c.style.height="10px";
    c.style.background="white";
    c.style.top=Math.random()*100+"vh";
    c.style.left=Math.random()*100+"vw";
    document.body.appendChild(c);
    setTimeout(()=>c.remove(),2000);
  }
}
</script>

</body>
</html>
