<!doctype html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Mathe & Einstein — Eine interaktive Mini-Website</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Patrick+Hand&family=Poppins:wght@400;700&display=swap" rel="stylesheet">
  <!-- MathJax für schöne Formeln -->
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
    html,body{margin:0; font-family:'Patrick Hand', 'Poppins', system-ui, -apple-system, 'Segoe UI', Roboto, Helvetica, Arial; background:linear-gradient(180deg,#0b1220 0%, #071033 60%); color:#f6f8fb; -webkit-font-smoothing:antialiased; padding:24px 12px; display:flex; justify-content:center;
      display:flex; justify-content:center;
    }
    .wrap{width:100%; max-width:var(--maxw);}
    header{display:flex;justify-content:space-between;align-items:center;gap:16px;margin-bottom:22px}
    .brand{display:flex;gap:14px;align-items:center}
    .logo{width:64px;height:64px;border-radius:12px;background:linear-gradient(135deg,#ff6ec7,#7c3aed);display:flex;align-items:center;justify-content:center;font-weight:700;color:white;font-size:22px;box-shadow:0 6px 20px rgba(124,58,237,0.25)}
    h1{font-size:22px;margin:0}
    p.lead{margin:0;color:var(--muted)}

    nav{display:flex;gap:10px}
    .btn{background:var(--glass);padding:8px 12px;border-radius:10px;border:1px solid rgba(255,255,255,0.03);cursor:pointer;font-weight:600}

    .grid{display:grid;grid-template-columns:2fr 1fr;gap:var(--gap)}
    @media (max-width:900px){.grid{grid-template-columns:1fr}}

    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:18px;border-radius:var(--radius);box-shadow:0 6px 30px rgba(2,6,23,0.6);border:1px solid rgba(255,255,255,0.03)}
    .hero{display:flex;gap:16px;align-items:center}
    .hero img{width:150px;height:150px;border-radius:12px;object-fit:cover;border:1px solid rgba(255,255,255,0.04)}
    .facts{display:flex;flex-direction:column;gap:8px}

    .section{margin-top:16px}
    .section h2{margin:0 0 10px 0}

    .eq{font-size:20px;padding:12px;background:linear-gradient(90deg, rgba(255,255,255,0.01), rgba(255,255,255,0.02));border-radius:8px}

    .timeline{display:flex;flex-direction:column;gap:10px}
    .time-item{display:flex;gap:12px;align-items:flex-start}
    .time-item .year{min-width:72px;color:var(--muted);font-weight:700}

    .list{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:12px;margin-top:10px}
    .small{font-size:13px;color:var(--muted)}

    footer{margin-top:20px;text-align:center;color:var(--muted);font-size:13px}

    /* dark mode toggle */
    .toggle{display:inline-flex;align-items:center;gap:8px}
    .switch{width:44px;height:26px;background:rgba(255,255,255,0.07);border-radius:999px;padding:3px;display:inline-flex;align-items:center;cursor:pointer}
    .knob{width:20px;height:20px;border-radius:50%;background:white;transition:transform .25s}
    .switch.off .knob{transform:translateX(0)}
    .switch.on .knob{transform:translateX(18px)}

    /* small code block */
    pre{background:#071023;padding:12px;border-radius:8px;overflow:auto;font-size:13px}

    .cta{display:flex;gap:10px;margin-top:12px}
    .cta .primary{background:linear-gradient(90deg,var(--accent),#5b21b6);padding:10px 14px;border-radius:10px;color:white;border:none}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="brand">
        <div class="logo">AE</div>
        <div>
          <h1>Albert Einstein — Mathe & Ideen ✨</h1>
          <p class="lead">Coole Erklärungen, einfache Beispiele und kleine Aufgaben — so dass Mathe Spaß macht! 🤓</p>
        </div>
      </div>
      <nav>
        <button class="btn" onclick="document.getElementById('bio').scrollIntoView({behavior:'smooth'})">Biografie</button>
        <button class="btn" onclick="document.getElementById('math').scrollIntoView({behavior:'smooth'})">Mathe</button>
        <button class="btn" onclick="document.getElementById('timeline').scrollIntoView({behavior:'smooth'})">Timeline</button>
      </nav>
    </header>

    <main class="grid">
      <section>
        <div class="card hero">
          <img src="https://upload.wikimedia.org/wikipedia/commons/d/d3/Albert_Einstein_Head.jpg" alt="Albert Einstein">
          <div>
            <div class="facts">
              <div><strong>Geboren:</strong> 14. März 1879</div>
              <div><strong>Gestorben:</strong> 18. April 1955</div>
              <div class="small">Theoretischer Physiker; prägende Figur der modernen Physik. Auf dieser Seite: Ein Schwerpunkt auf den mathematischen Ideen hinter seinen Theorien.</div>
            </div>
            <div class="cta">
              <button class="primary" onclick="document.getElementById('math').scrollIntoView({behavior:'smooth'})">Zum Mathe-Teil 🚀</button>
              <button class="btn" onclick="alert('Mehr Inhalte folgen — du kannst mir sagen, was du möchtest!')">Anpassen</button>
            </div>
          </div>
        </div>

        <div id="bio" class="card section">
          <h2>Kurzbiografie</h2>
          <p class="small">Albert Einstein gilt als einer der einflussreichsten Wissenschaftler aller Zeiten. Seine besondere Stärke lag darin, komplizierte Naturgesetze in einfache mathematische Ideen zu übersetzen. Statt auf reines Auswendiglernen setzte er auf Vorstellungsvermögen, logisches Denken und saubere Mathematik.</p>

          <p class="small">Schon als Jugendlicher beschäftigte er sich intensiv mit Geometrie und Algebra. Später verband er diese Grundlagen mit physikalischen Fragen – besonders zu Raum, Zeit und Bewegung.</p>

          <div class="timeline"" id="timeline">
            <div class="time-item"><div class="year">1905</div><div><strong>Annus Mirabilis</strong> — vier grundlegende Arbeiten, u. a. zur speziellen Relativität und zum photoelektrischen Effekt.</div></div>
            <div class="time-item"><div class="year">1915</div><div><strong>Allgemeine Relativitätstheorie</strong> — Gravitation als Geometrie der Raumzeit.</div></div>
            <div class="time-item"><div class="year">1921</div><div><strong>Nobelpreis</strong> für den photoelektrischen Effekt (nicht für Relativitätstheorie).</div></div>
          </div>
        </div>

        <div id="math" class="card section">
          <h2>Mathematische Highlights</h2>
          <p class="small">Hier sind zentrale Gleichungen und Konzepte — kurz erklärt mit LaTeX-Formeln (MathJax wird automatisch gerendert).</p>

          <h3>Energie — Masse</h3>
          <div class="eq">$E = mc^2$</div>
          <p class="small">Diese berühmte Gleichung zeigt, dass Masse und Energie zwei Formen derselben Größe sind. Selbst eine winzige Menge Masse kann in extrem viel Energie umgewandelt werden.</p>

          <h3>Speziellen Relativität (Lorentz-Transformation)</h3>
          <pre>\( t' = \gamma \left(t - \dfrac{v x}{c^2}\right), \quad x' = \gamma (x - v t), \quad \gamma = \dfrac{1}{\sqrt{1-v^2/c^2}} \)</pre>

          <p class="small">Die Lorentz-Transformationen erklären, warum Zeit und Strecke für bewegte Beobachter unterschiedlich gemessen werden. Je schneller man sich bewegt, desto stärker treten diese Effekte auf.</p>

          <h3>Allgemeine Relativität — Einsteins Feldgleichungen (kompakt)</h3>
          <pre>\( G_{\mu\nu} + \Lambda g_{\mu\nu} = \tfrac{8\pi G}{c^4} T_{\mu\nu} \)</pre>
          <p class="small">Diese Gleichung beschreibt, wie Materie und Energie die Raumzeit krümmen. Die Krümmung bestimmt wiederum, wie sich Körper bewegen – das ist Einsteins Erklärung für Gravitation.</p>

          <h3>Lineare Algebra & Tensorkalkül</h3>
          <p class="small">Einsteins Theorien benötigen Tensoren (z. B. Metrik $g_{\mu\nu}$, Energie-Impuls-Tensor $T_{\mu\nu}$). Lineare Algebra, Differentialgeometrie und Analysis sind hier die Werkzeuge.</p>

          <div style="margin-top:10px">
            <label for="speedRange">Relativistische Zeitdilatation — Geschwindigkeit einstellen:</label>
            <input id="speedRange" type="range" min="0" max="99.99" step="0.01" value="50" oninput="updateTau()">
            <div id="tau" class="small" style="margin-top:8px"></div>
          </div>
        </div>

        <div class="card section">
          <h2>Warum ist Einsteins Mathematik so wichtig?</h2>
          <div class="list">
            <div class="card small"><strong>Geometrie der Raumzeit</strong><div class="small">Riemannsche Geometrie, Metrik, Geodäten.</div></div>
            <div class="card small"><strong>Feldgleichungen lösen</strong><div class="small">Symmetrien (z. B. Schwarzschild-Lösung), Näherungsverfahren.</div></div>
            <div class="card small"><strong>Quanten vs. Relativität</strong><div class="small">Einsteins Berührungen mit Quanten (Photoeffekt) und seine späteren Einwände gegen die Kopenhagener Deutung.</div></div>
          </div>
        </div>

      </section>

      <aside>
        <div class="card">
          <h2>Schnelle Fakten</h2>
          <ul class="small">
            <li>Sprachkenntnisse: Deutsch (Muttersprache), Englisch.</li>
            <li>Beruf: Patentamt (Bern) — dort intensive Gedankenexperimente.</li>
            <li>Lieblingsfragen: Symmetrie, Erhaltungssätze, einfache Modelle.</li>
          </ul>
        </div>

        <div class="card section">
          <h2>Zitate</h2>
          <blockquote style="margin:0;font-style:italic;color:var(--muted)">"Phantasie ist wichtiger als Wissen, denn Wissen ist begrenzt." — Albert Einstein</blockquote>
        </div>

        <div class="card section">
          <h2>Download</h2>
          <p class="small">Kopiere diesen Code in eine Datei <code>index.html</code> und öffne sie im Browser, um die Seite lokal zu sehen.</p>
          <button class="btn" onclick="copyCode()">HTML in Zwischenablage kopieren</button>
        </div>

        <div class="card section">
          <h2>Design-Tools</h2>
          <p class="small">Wenn du möchtest, kann ich eine Druckversion (PDF), eine mehrsprachige Variante oder zusätzliche Seiten (z. B. interaktive Aufgaben) anlegen.</p>
        </div>
      </aside>
    </main>

    <footer>
      <div class="small">Schulprojekt-Vorlage — Text neu formuliert & designorientiert. Gestalte sie weiter nach deinem Stil.</div>
    </footer>
  </div>

  <script>
    // Dark/light (nur visuelle Farbverschiebung) — einfache Toggle
    const switchEl = (() => {
      const sw = document.createElement('div');
      sw.className = 'toggle';
      sw.innerHTML = `<div class='switch on' id='darkSwitch'><div class='knob'></div></div>`;
      document.querySelector('header').appendChild(sw);
      const s = document.getElementById('darkSwitch');
      s.addEventListener('click', ()=>{
        s.classList.toggle('on'); s.classList.toggle('off');
        if(s.classList.contains('off')){
          document.documentElement.style.setProperty('--bg','#f7fafc');
          document.body.style.background = 'linear-gradient(180deg,#ffffff 0%, #f3f6fb 60%)';
          document.body.style.color = '#0b1220';
        } else {
          document.documentElement.style.removeProperty('--bg');
          document.body.style.background = 'linear-gradient(180deg,#071124 0%, #061226 60%)';
          document.body.style.color = '#e6eef6';
        }
      });
      return s;
    })();

    // Zeitdilatation: tau = t * sqrt(1 - v^2/c^2)
    function updateTau(){
      const vPercent = parseFloat(document.getElementById('speedRange').value);
      const v = vPercent/100 * 299792458; // m/s (not needed numerically but keeps units intuitive)
      const c = 299792458;
      const gamma = 1/Math.sqrt(1 - Math.pow(v/c,2));
      const t = 1; // 1s im Ruhesystem
      const tau = t/ gamma; // wie viel kürzer die Zeit wird
      document.getElementById('tau').textContent = `Bei v = ${vPercent}% von c: Zeitdilatation → eine Sekunde entspricht ≈ ${tau.toFixed(6)} s (Eigenzeit). Lorentz-Faktor γ = ${gamma.toFixed(4)}`;
    }
    updateTau();

    function copyCode(){
      const code = `<!doctype html>\n` + document.documentElement.outerHTML; /* irredundant placeholder: user will copy manually */
      navigator.clipboard.writeText(code).then(()=>alert('HTML wurde in die Zwischenablage kopiert.')).catch(()=>alert('Kopieren fehlgeschlagen — öffne die Entwicklertools und kopiere manuell.'));
    }
  </script>
</body>
</html>
