<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Mathe & Einstein – erstellt von Paul</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Patrick+Hand&family=Poppins:wght@400;700&display=swap" rel="stylesheet">

  <!-- MathJax für Formeln -->
  <script>
    window.MathJax = {
      tex: {inlineMath: [['$','$'], ['\\(','\\)']]},
      svg: { fontCache: 'global' }
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
      padding:24px 12px;
      display:flex;
      justify-content:center;
    }
    .wrap{width:100%;max-width:var(--maxw);}
    header{display:flex;justify-content:space-between;align-items:center;gap:16px;margin-bottom:22px}
    .brand{display:flex;gap:14px;align-items:center}
    .logo{width:64px;height:64px;border-radius:12px;background:linear-gradient(135deg,#ff6ec7,#7c3aed);display:flex;align-items:center;justify-content:center;font-weight:700;color:white;font-size:22px}
    h1{font-size:22px;margin:0}
    .lead{margin:0;color:var(--muted)}

    nav{display:flex;gap:10px}
    .btn{background:var(--glass);padding:8px 12px;border-radius:10px;border:1px solid rgba(255,255,255,0.05);cursor:pointer;font-weight:600;color:white}

    .grid{display:grid;grid-template-columns:2fr 1fr;gap:var(--gap)}
    @media (max-width:900px){.grid{grid-template-columns:1fr}}

    .card{background:rgba(255,255,255,0.03);padding:18px;border-radius:var(--radius);box-shadow:0 6px 20px rgba(0,0,0,0.4)}
    .hero{display:flex;gap:16px;align-items:center}
    .hero img{width:140px;height:140px;border-radius:10px;object-fit:cover}

    .section{margin-top:16px}
    .eq{font-size:20px;padding:10px;background:rgba(255,255,255,0.06);border-radius:8px}

    .timeline{display:flex;flex-direction:column;gap:10px}
    .time-item{display:flex;gap:10px}
    .year{color:var(--muted);min-width:70px;font-weight:bold}

    footer{margin-top:20px;text-align:center;color:var(--muted);font-size:13px}
  </style>
</head>

<body>
<div class="wrap">

<header>
  <div class="brand">
    <div class="logo">AE</div>
    <div>
      <h1>Albert Einstein</h1>
      <p class="lead">Wichtige Infos Sowie schlaue fakten</p>
    </div>
  </div>

  <nav>
    <button class="btn" onclick="bio.scrollIntoView({behavior:'smooth'})">Bio</button>
    <button class="btn" onclick="math.scrollIntoView({behavior:'smooth'})">Mathe</button>
    <button class="btn" onclick="timeline.scrollIntoView({behavior:'smooth'})">Zeit</button>
  </nav>
</header>

<main class="grid">

<section>

<div class="card hero">
  <img src="https://upload.wikimedia.org/wikipedia/commons/d/d3/Albert_Einstein_Head.jpg" alt="Einstein">
  <div>
    <p><strong>Geboren:</strong> 1879</p>
    <p><strong>Gestorben:</strong> 1955</p>
    <p style="font-size:13px;color:var(--muted)">
      Albert Einstein war ein Physiker, der mit Formeln versuchte die Welt besser zu verstehen.
    </p>
  </div>
</div>

<div id="bio" class="card section">
  <h2>Kurzbiografie</h2>
  <p style="font-size:14px">
    Albert Einstein war einer der bekanntesten Wissenschaftler. Schon in der Schule interessierte
    er sich sehr für Mathematik und Physik, auch wenn er am Anfang kein Musterschüler war.
  </p>
</div>

<div id="timeline" class="card section">
  <h2>Zeitleiste</h2>
  <div class="timeline">
    <div class="time-item"><div class="year">1905</div>Wichtige Arbeiten zur Relativität</div>
    <div class="time-item"><div class="year">1915</div>Allgemeine Relativitätstheorie</div>
    <div class="time-item"><div class="year">1921</div>Nobelpreis</div>
  </div>
</div>

<div id="math" class="card section">
  <h2>Einsteins bekannteste Formel</h2>
  <div class="eq">$E = mc^2$</div>
  <p style="font-size:13px">
    Diese Formel bedeutet: Energie und Masse gehören zusammen.
  </p>

  <h3>Lorentz-Faktor</h3>
  <pre>\(\gamma = \frac{1}{\sqrt{1-v^2/c^2}}\)</pre>
</div>

</section>

<aside>

<div class="card">
  <h2>Info</h2>
  <ul style="font-size:13px">
    <li>Beruf: Physiker</li>
    <li>Land: Deutschland</li>
    <li>Arbeitsort: Schweiz / USA</li>
  </ul>
</div>

<div class="card section">
  <h2>Zitat</h2>
  <p style="font-style:italic;font-size:13px">
    "Phantasie ist wichtiger als Wissen."
  </p>
</div>

</aside>

</main>

<footer>
  Erstellt von Paul
</footer>

</div>
</body>
</html>
