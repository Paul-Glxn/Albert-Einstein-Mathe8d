<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Mathe & Einstein – erstellt von Paul</title>

<link href="https://fonts.googleapis.com/css2?family=Patrick+Hand&family=Poppins:wght@400;700&display=swap" rel="stylesheet">

<script>
window.MathJax = {
  tex: {inlineMath: [['$','$'],['\\(','\\)']]},
  svg: {fontCache:'global'}
};
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-svg.js" defer></script>

<style>
:root{
  --bg:#0f1724; --card:#0b1220; --muted:#9aa4b2; --accent:#7c3aed; --glass:rgba(255,255,255,0.04);
  --maxw:1100px; --radius:14px; --gap:18px;
}
*{box-sizing:border-box}
body{
  margin:0;
  font-family:'Patrick Hand','Poppins',Arial,sans-serif;
  background:linear-gradient(180deg,#0b1220 0%, #071033 60%);
  color:#f6f8fb;
  padding:24px;
  display:flex;
  justify-content:center;
}
.wrap{width:100%;max-width:var(--maxw);}
header{display:flex;justify-content:space-between;align-items:center;margin-bottom:20px}
.brand{display:flex;gap:14px;align-items:center}
.logo{
  width:64px;height:64px;border-radius:12px;
  background:linear-gradient(135deg,#ff6ec7,#7c3aed);
  display:flex;align-items:center;justify-content:center;
  font-weight:700;font-size:22px;color:white
}
nav{display:flex;gap:10px}

.btn{
  background:var(--glass);
  padding:8px 12px;border-radius:10px;
  border:1px solid rgba(255,255,255,0.05);
  color:white;cursor:pointer;
}
.grid{display:grid;grid-template-columns:2fr 1fr;gap:20px}
@media (max-width:900px){.grid{grid-template-columns:1fr}}

.card{
  background:rgba(255,255,255,0.03);
  padding:18px;border-radius:14px;
  box-shadow:0 6px 20px rgba(0,0,0,0.5);
  transition:.2s;
}
.card:hover{transform:scale(1.02)}
.hero{display:flex;gap:15px;align-items:center}
.hero img{width:140px;height:140px;border-radius:10px}
.eq{background:rgba(255,255,255,0.07);padding:10px;border-radius:8px;font-size:18px}
.timeline{display:flex;flex-direction:column;gap:10px}
.time-item{display:flex;gap:10px}
.year{color:var(--muted);min-width:70px;font-weight:bold}
footer{text-align:center;color:var(--muted);margin-top:20px;font-size:13px}
.gallery img{width:30%;border-radius:8px;margin:5px}
ul{padding-left:18px}
</style>
</head>

<body>
<div class="wrap">

<header>
<div class="brand">
<div class="logo">AE</div>
<div>
<h1>Albert Einstein</h1>
<p style="color:#9aa4b2">Wichtige Infos sowie schlaue Fakten</p>
</div>
</div>
<nav>
<button class="btn" onclick="bio.scrollIntoView()">Bio</button>
<button class="btn" onclick="math.scrollIntoView()">Mathe</button>
<button class="btn" onclick="timeline.scrollIntoView()">Zeit</button>
</nav>
</header>

<main class="grid">

<section>

<div class="card hero">
<img src="https://upload.wikimedia.org/wikipedia/commons/d/d3/Albert_Einstein_Head.jpg">
<div>
<p><b>Geboren:</b> 1879</p>
<p><b>Gestorben:</b> 1955</p>
<p style="color:#9aa4b2;font-size:13px">
Albert Einstein war ein Physiker, der mit Formeln versuchte die Welt besser zu verstehen.
</p>
</div>
</div>

<div id="bio" class="card">
<h2>Kurzbiografie</h2>
<p>
Albert Einstein wurde in Deutschland geboren und lebte später in der Schweiz und in den USA.
Während der Nazizeit musste er fliehen, da er Jude war.
</p>
</div>

<div class="card">
<h2>Fun Facts</h2>
<ul>
<li>🎻 Spielte gern Geige</li>
<li>🧠 Hatte schlechte Noten in Geschichte</li>
<li>👣 Trug selten Socken</li>
<li>📜 Bekam 1921 den Nobelpreis für Physik</li>
<li>🇺🇸 Wurde später US-Amerikaner</li>
</ul>
</div>

<div id="timeline" class="card">
<h2>Zeitleiste</h2>
<div class="timeline">
<div class="time-item"><div class="year">1905</div>Spezielle Relativitätstheorie</div>
<div class="time-item"><div class="year">1915</div>Allgemeine Relativitätstheorie</div>
<div class="time-item"><div class="year">1921</div>Nobelpreis für Physik</div>
<div class="time-item"><div class="year">1933</div>Flucht in die USA</div>
</div>
</div>

<div id="math" class="card">
<h2>Einsteins bekannteste Formel</h2>
<div class="eq">$E = mc^2$</div>
<p>
Das bedeutet: Masse kann in Energie umgewandelt werden. Schon ein kleines Stück Materie enthält extrem viel Energie.
</p>

<p><b>Lichtgeschwindigkeit:</b></p>
<div class="eq">$c = 299\,792\,458 \, m/s$</div>

<h3>Lorentz-Faktor</h3>
<div class="eq">\(\gamma = \frac{1}{\sqrt{1-v^2/c^2}}\)</div>

<p style="font-size:13px;color:#9aa4b2">
Diese Formel zeigt, wie sich Zeit und Masse verändern, wenn sich etwas sehr schnell bewegt.
</p>
</div>



<div class="card">
<h2>Info</h2>
<ul>
<li>Beruf: Physiker</li>
<li>Geburtsland: Deutschland</li>
<li>Lebte in: Schweiz / USA</li>
<li>Fachgebiet: Relativität</li>
</ul>
</div>

<div class="card">
<h2>Zitat</h2>
<p><i>"Phantasie ist wichtiger als Wissen."</i></p>
</div>

</aside>

</main>

<footer>Erstellt von Paul</footer>

</div>
</body>
</html>
