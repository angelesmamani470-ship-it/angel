# angel
hola mundo
<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Día de regalar Hot Wheels — Mensajes en ramo</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;500;700&display=swap" rel="stylesheet">
  <style>
    :root{--bg1:#07133a;--bg2:#06203b;--accent:#ffd400;--blue:#0b5bd7}
    *{box-sizing:border-box}
    body{margin:0;min-height:100vh;display:flex;align-items:center;justify-content:center;font-family:Montserrat,system-ui,Arial;background:linear-gradient(180deg,var(--bg1),var(--bg2));color:#fff;padding:28px}

    .stage{width:min(980px,96%);display:flex;gap:24px;align-items:center;justify-content:center}

    /* Ramo visual */
    .bouquet{width:420px;background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);border-radius:18px;padding:18px;border:1px solid rgba(255,255,255,0.04);box-shadow:0 8px 30px rgba(2,6,23,0.6);display:flex;flex-direction:column;align-items:center}
    .wrap{position:relative;width:320px;height:420px}

    /* envoltura con efecto de papel doblado */
    .wrap .paper{position:absolute;left:50%;transform:translateX(-50%);bottom:0;width:320px;height:420px;border-radius:18px;overflow:hidden;}
    .paper::before{content:"";position:absolute;inset:0;background:linear-gradient(135deg,#09306b,#0b2a5b);opacity:0.95}
    .paper::after{content:"";position:absolute;left:-40px;top:30px;width:420px;height:420px;background:radial-gradient(circle at 30% 20%, rgba(255,255,255,0.03), transparent 15%) ;transform:rotate(-12deg)}

    /* tarjeta Hot Wheels (imagen) */
    .card-slot{position:absolute;left:50%;transform:translateX(-50%);top:18px;width:180px;}
    .card-slot img{width:100%;height:auto;border-radius:6px;box-shadow:0 12px 30px rgba(2,6,23,0.6)}

    /* rosa azul (SVG) */
    .rose{position:absolute;left:50%;transform:translateX(-50%);bottom:110px;width:220px;height:220px}

    /* moño */
    .bow{position:absolute;left:50%;transform:translateX(-50%);bottom:28px}

    /* Texto y controles */
    .panel{width:520px;padding:18px;border-radius:14px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));box-shadow:0 8px 30px rgba(2,6,23,0.6);border:1px solid rgba(255,255,255,0.04)}
    h1{margin:6px 0 12px 0;font-size:26px}
    p.lead{margin:0 0 18px 0;opacity:0.9}

    .rotator{height:260px;border-radius:12px;padding:18px;background:rgba(255,255,255,0.02);position:relative;overflow:hidden}
    .phrases{position:relative;height:100%}
    .phrase{position:absolute;left:12px;right:12px;opacity:0;transform:translateY(18px) scale(0.98);transition:all 600ms cubic-bezier(.2,.9,.3,1);font-size:20px;line-height:1.3}
    .phrase.show{opacity:1;transform:translateY(0) scale(1)}

    .controls{display:flex;gap:10px;margin-top:12px}
    button{background:transparent;border:1px solid rgba(255,255,255,0.06);padding:10px 14px;border-radius:10px;color:var(--accent);cursor:pointer}
    button.secondary{color:#fff;border-color:rgba(255,255,255,0.04)}

    /* Responsive */
    @media (max-width:900px){.stage{flex-direction:column}.panel{width:100%}.bouquet{width:100%;order:2}}
  </style>
</head>
<body>
  <div class="stage" role="main">

    <div class="bouquet" aria-label="Ramo de Hot Wheels">
      <div class="wrap" aria-hidden="true">
        <div class="paper"></div>

        <div class="card-slot">
          <!-- Referencia de la imagen que subiste -->
          <img src="/mnt/data/fbc7e987-ad0d-4b0c-b3aa-c499c55090ff.png" alt="Hot Wheels en empaque"/>
        </div>

        <!-- rosa azul (SVG simple) -->
        <svg class="rose" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <radialGradient id="gR" cx="30%" cy="30%" r="80%">
              <stop offset="0%" stop-color="#3aa0ff" />
              <stop offset="100%" stop-color="#0b3fa6" />
            </radialGradient>
          </defs>
          <g transform="translate(100,100)">
            <circle r="48" fill="url(#gR)" opacity="0.98" />
            <!-- pétalos estilizados -->
            <g fill="#0b3fa6" opacity="0.95">
              <path d="M0,-52 C20,-52 36,-36 36,-20 C36,-4 20,8 0,12 C-20,8 -36,-4 -36,-20 C-36,-36 -20,-52 0,-52 Z" transform="rotate(10)"/>
              <path d="M0,-52 C20,-52 36,-36 36,-20 C36,-4 20,8 0,12 C-20,8 -36,-4 -36,-20 C-36,-36 -20,-52 0,-52 Z" transform="rotate(50)"/>
              <path d="M0,-52 C20,-52 36,-36 36,-20 C36,-4 20,8 0,12 C-20,8 -36,-4 -36,-20 C-36,-36 -20,-52 0,-52 Z" transform="rotate(90)"/>
              <path d="M0,-52 C20,-52 36,-36 36,-20 C36,-4 20,8 0,12 C-20,8 -36,-4 -36,-20 C-36,-36 -20,-52 0,-52 Z" transform="rotate(130)"/>
            </g>
          </g>
        </svg>

        <!-- moño amarillo -->
        <svg class="bow" viewBox="0 0 240 120" xmlns="http://www.w3.org/2000/svg">
          <g transform="translate(120,60)">
            <path d="M0,0 C40,-40 80,-60 110,-18 C80,-20 46,12 0,16 C-46,12 -80,-20 -110,-18 C-80,-60 -40,-40 0,0 Z" fill="#ffd400" opacity="0.98"/>
            <rect x="-18" y="0" width="36" height="32" rx="6" fill="#ffbf00" />
            <path d="M-140,16 L-36,16" stroke="#ffd400" stroke-width="12" stroke-linecap="round"/>
            <path d="M140,16 L36,16" stroke="#ffd400" stroke-width="12" stroke-linecap="round"/>
          </g>
        </svg>

      </div>
    </div>

    <div class="panel">
      <h1>Un ramo diferente: detalles que quedan</h1>
      <p class="lead">Basado en la referencia: envoltura azul, rosa azul y moño amarillo. Aquí tienes varias frases bonitas pensadas para acompañar un detalle así (sin usar la palabra que pediste).</p>

      <div class="rotator" aria-live="polite">
        <div class="phrases" id="phrases">
          <div class="phrase">Eres la chispa que convierte lo cotidiano en aventura.</div>
          <div class="phrase">Cada kilómetro recorrido deja una historia para recordar.</div>
          <div class="phrase">Gracias por sumarte a las locuras y hacerlas más divertidas.</div>
          <div class="phrase">Tu risa acelera los mejores planes.</div>
          <div class="phrase">Las buenas ideas siempre viajan más rápido cuando estás cerca.</div>
          <div class="phrase">A tu lado, cualquier camino se siente como una pista de diversión.</div>
          <div class="phrase">Un gesto pequeño, un recuerdo que sigue rodando.</div>
          <div class="phrase">Por las risas, las complicidades y las anécdotas que aún faltan.</div>
          <div class="phrase">Que esta miniatura guarde grandes momentos junto a ti.</div>
        </div>
      </div>

      <div class="controls">
        <button id="prev" class="secondary" aria-label="Frase anterior">◀ Anterior</button>
        <button id="pause">Pausar</button>
        <button id="next" class="secondary" aria-label="Siguiente frase">Siguiente ▶</button>
      </div>

    </div>
  </div>

  <script>
    // Rotador de frases
    const phrases = Array.from(document.querySelectorAll('.phrase'));
    let idx = 0;let timer = null;let paused = false;
    function show(i){phrases.forEach((p,pi)=> p.classList.toggle('show', pi===i));}
    function next(){ idx = (idx+1) % phrases.length; show(idx); }
    function prev(){ idx = (idx-1+phrases.length) % phrases.length; show(idx); }
    document.getElementById('next').addEventListener('click', ()=>{ next(); resetTimer(); });
    document.getElementById('prev').addEventListener('click', ()=>{ prev(); resetTimer(); });
    document.getElementById('pause').addEventListener('click', (e)=>{ paused = !paused; e.target.textContent = paused? 'Reanudar' : 'Pausar'; if(!paused) startTimer(); else stopTimer(); });
    function startTimer(){ stopTimer(); timer = setInterval(next, 3800); }
    function stopTimer(){ if(timer) clearInterval(timer); timer = null; }
    function resetTimer(){ if(!paused) startTimer(); }
    show(idx); startTimer();

    // accesibilidad: cambiar frase con teclado
    window.addEventListener('keydown', (e)=>{ if(e.key === 'ArrowRight') { next(); resetTimer(); } if(e.key === 'ArrowLeft') { prev(); resetTimer(); } if(e.key === ' ') { e.preventDefault(); document.getElementById('pause').click(); } });
  </script>
</body>
</html>
