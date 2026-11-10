<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>CASSIL | Alquiler, compra y venta de inmuebles</title>
<meta name="description" content="CASSIL: alquiler, compra y venta de inmuebles. Te acompañamos desde la búsqueda hasta la firma.">
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Crect x='14' y='20' width='34' height='70' fill='%239b4a9e'/%3E%3Crect x='50' y='8' width='26' height='82' fill='%2300a3e8'/%3E%3C/svg%3E">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Anton&family=Barlow:wght@400;500;600&display=swap" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/@n8n/chat/dist/style.css" rel="stylesheet" />
<style>
:root{
  /* Chatbot n8n con los colores de CASSIL */
  --chat--color-primary:#9b4a9e;
  --chat--color-primary-shade-50:#8a3f8d;
  --chat--color-primary-shade-100:#793580;
  --chat--color-secondary:#00a3e8;
  --chat--color-secondary-shade-50:#0090cf;
  --chat--header--background:#272727;
  --chat--header--color:#ffffff;
  --chat--toggle--background:#9b4a9e;
  --chat--toggle--hover--background:#8a3f8d;
  --chat--toggle--active--background:#793580;
  --chat--toggle--color:#ffffff;
  --chat--window--z-index:70;
  --chat--toggle--z-index:70;
  --purple:#9b4a9e;
  --sky:#00a3e8;
  --yellow:#fff200;
  --ink:#272727;
  --brick:#8b0016;
  --paper:#ffffff;
  --mist:#f3f6fa;
  --line:#dde3ea;
  --text:#272727;
  --muted:#5b6470;
  --card:#ffffff;
  --display:'Anton','Impact','Arial Narrow',sans-serif;
  --body:'Barlow','Segoe UI',Arial,sans-serif;
}
@media (prefers-color-scheme:dark){
  :root:not([data-theme="light"]){
    --paper:#15171b;--mist:#1c1f25;--line:#2c3038;--text:#f1f3f6;--muted:#a3abb7;--card:#1f2229;
  }
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth;scroll-padding-top:80px}
body{font-family:var(--body);color:var(--text);background:var(--paper);line-height:1.6;font-size:17px;overflow-x:hidden}
a{color:inherit}
img,svg{max-width:100%}
:focus-visible{outline:3px solid var(--sky);outline-offset:3px}
.wrap{width:min(1160px,92%);margin-inline:auto}
h1,h2,h3{font-family:var(--display);font-weight:400;letter-spacing:.01em;line-height:1.05}
h2{font-size:clamp(2.2rem,5vw,3.4rem);margin-bottom:.6rem}
.lead{color:var(--muted);max-width:60ch}

/* Scroll progress */
#progress{position:fixed;top:0;left:0;height:4px;width:0;background:linear-gradient(90deg,var(--purple),var(--sky));z-index:100}

/* Nav */
header.nav{position:fixed;inset:0 0 auto 0;z-index:50;transition:background .3s,box-shadow .3s,padding .3s;padding:18px 0}
header.nav.solid{background:var(--paper);box-shadow:0 2px 18px rgba(0,0,0,.12);padding:8px 0}
.nav .wrap{display:flex;align-items:center;justify-content:space-between;gap:20px}
.brand{display:flex;align-items:center;gap:10px;text-decoration:none}
.brand svg{height:44px;width:auto}
.brand span{font-family:var(--display);font-size:1.7rem;color:var(--ink);letter-spacing:.03em;
  -webkit-text-stroke:1.5px var(--yellow);paint-order:stroke fill;text-shadow:0 0 0 var(--yellow)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]) .brand span{color:#fff;-webkit-text-stroke:0}}
.menu{display:flex;gap:28px;list-style:none;align-items:center}
.menu a{text-decoration:none;font-weight:600;position:relative;padding:4px 0}
.menu a:not(.btn)::after{content:"";position:absolute;left:0;bottom:-2px;height:3px;width:0;background:var(--sky);transition:width .25s}
.menu a:not(.btn):hover::after,.menu a.active::after{width:100%}
.burger{display:none;background:none;border:0;cursor:pointer;width:44px;height:44px;position:relative}
.burger i,.burger i::before,.burger i::after{position:absolute;left:10px;width:24px;height:3px;background:var(--text);content:"";transition:transform .3s,top .3s,opacity .3s}
.burger i{top:20px}.burger i::before{top:-8px;left:0}.burger i::after{top:8px;left:0}
.burger[aria-expanded="true"] i{background:transparent}
.burger[aria-expanded="true"] i::before{top:0;transform:rotate(45deg)}
.burger[aria-expanded="true"] i::after{top:0;transform:rotate(-45deg)}

.btn{display:inline-flex;align-items:center;gap:10px;font-family:var(--body);font-weight:600;font-size:1rem;
  padding:14px 26px;border-radius:6px;text-decoration:none;border:2px solid transparent;cursor:pointer;
  transition:transform .2s,box-shadow .2s,background .2s}
.btn:hover{transform:translateY(-3px);box-shadow:0 8px 20px rgba(0,0,0,.2)}
.btn-main{background:var(--ink);color:#fff;border-color:var(--yellow)}
.btn-wa{background:#1fa855;color:#fff}
.btn-line{background:transparent;color:var(--text);border-color:var(--text)}
.btn svg{width:20px;height:20px;fill:currentColor}

/* Hero */
.hero{position:relative;min-height:100vh;display:flex;align-items:center;padding:120px 0 80px;
  background:linear-gradient(180deg,var(--paper) 0%,var(--mist) 100%);overflow:hidden}
.hero .wrap{display:grid;grid-template-columns:1.1fr .9fr;gap:30px;align-items:center;position:relative;z-index:2}
.hero h1{font-size:clamp(4.5rem,15vw,10.5rem);color:var(--ink);letter-spacing:.02em;
  -webkit-text-stroke:3px var(--yellow);paint-order:stroke fill;line-height:.95;
  filter:drop-shadow(4px 5px 0 rgba(0,0,0,.12))}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]) .hero h1{color:#fff;-webkit-text-stroke:0;filter:none}}
.hero h1 .ch{display:inline-block;opacity:0;transform:translateY(60px) rotate(6deg);animation:drop .7s cubic-bezier(.2,.9,.3,1.3) forwards}
@keyframes drop{to{opacity:1;transform:none}}
.hero p.tag{font-size:clamp(1.15rem,2.4vw,1.5rem);margin:18px 0 6px;font-weight:500}
.typed{color:var(--purple);font-weight:600;border-right:3px solid var(--sky);padding-right:4px;white-space:nowrap}
.hero .actions{display:flex;flex-wrap:wrap;gap:14px;margin-top:30px}

.skyline{position:relative;height:min(62vh,520px);display:flex;align-items:flex-end;justify-content:center;gap:14px}
.tower{position:relative;display:grid;gap:7px;padding:14px 12px;transform-origin:bottom;
  transform:scaleY(0);animation:rise 1.1s cubic-bezier(.2,.8,.2,1) forwards}
.tower.t1{background:var(--purple);width:150px;height:78%;grid-template-columns:repeat(6,1fr);animation-delay:.2s}
.tower.t2{background:var(--sky);width:128px;height:96%;grid-template-columns:1fr;border-top-left-radius:60px 20px;animation-delay:.45s}
@keyframes rise{to{transform:scaleY(1)}}
.tower .w{background:#fff;border-radius:2px;min-height:9px;transition:background .6s,box-shadow .6s}
.tower.t1 .w{aspect-ratio:1/1.2}
.tower.t2 .w{height:9px;min-height:0}
.tower .w.on{background:var(--yellow);box-shadow:0 0 10px var(--yellow)}
.house{position:absolute;left:-30px;bottom:0;width:150px;z-index:3;transform:translateY(40px);opacity:0;animation:pop .6s .9s forwards}
@keyframes pop{to{transform:none;opacity:1}}
.ground{position:absolute;left:-40px;right:-40px;bottom:-4px;height:6px;background:var(--ink)}

/* Sections */
section{padding:96px 0}
.alt{background:var(--mist)}
.head{margin-bottom:46px}

/* Services */
.tabs{display:flex;gap:10px;flex-wrap:wrap;margin-bottom:26px}
.tab{font-family:var(--body);font-weight:600;font-size:1rem;padding:11px 22px;border-radius:999px;border:2px solid var(--line);
  background:var(--card);color:var(--text);cursor:pointer;transition:all .2s}
.tab:hover{border-color:var(--sky)}
.tab[aria-selected="true"]{background:var(--ink);color:#fff;border-color:var(--yellow)}
.panel{display:none;grid-template-columns:1fr 1fr;gap:40px;align-items:center;animation:fade .45s}
.panel.show{display:grid}
@keyframes fade{from{opacity:0;transform:translateX(24px)}to{opacity:1;transform:none}}
.panel h3{font-size:2.2rem;margin-bottom:12px}
.panel ul{list-style:none;margin:18px 0 26px}
.panel li{padding:8px 0 8px 34px;position:relative;border-bottom:1px solid var(--line)}
.panel li::before{content:"";position:absolute;left:0;top:14px;width:18px;height:18px;border-radius:50%;background:var(--sky);
  box-shadow:inset 0 0 0 5px var(--card),0 0 0 2px var(--sky)}
.panel .art{aspect-ratio:4/3;border-radius:14px;display:grid;place-items:center;position:relative;overflow:hidden}
.art.a1{background:var(--purple)}.art.a2{background:var(--sky)}.art.a3{background:var(--ink)}
.art svg{width:58%;height:auto}

/* Cards */
.grid3{display:grid;grid-template-columns:repeat(3,1fr);gap:24px}
.card{background:var(--card);border:1px solid var(--line);border-radius:12px;padding:30px;transform-style:preserve-3d;transition:transform .15s ease-out,box-shadow .3s}
.card:hover{box-shadow:0 18px 36px rgba(0,0,0,.14)}
.card h3{font-size:1.7rem;margin:14px 0 8px}
.card .ico{width:54px;height:54px;border-radius:12px;display:grid;place-items:center;background:var(--sky)}
.card:nth-child(2) .ico{background:var(--purple)}
.card:nth-child(3) .ico{background:var(--brick)}
.card .ico svg{width:30px;height:30px;fill:none;stroke:#fff;stroke-width:2;stroke-linecap:round;stroke-linejoin:round}
.card p{color:var(--muted)}

/* Stats */
.stats{background:var(--ink);color:#fff;padding:64px 0}
.stats .wrap{display:grid;grid-template-columns:repeat(4,1fr);gap:20px;text-align:center}
.stats strong{display:block;font-family:var(--display);font-weight:400;font-size:clamp(2.6rem,6vw,4.2rem);color:var(--yellow);line-height:1}
.stats span{color:#c9cfd8}

/* Steps */
.steps{display:grid;grid-template-columns:repeat(4,1fr);gap:22px;counter-reset:s}
.step{position:relative;padding:26px 22px;border-left:4px solid var(--sky);background:var(--card);border-radius:0 12px 12px 0}
.step::before{counter-increment:s;content:counter(s);font-family:var(--display);font-size:2.6rem;color:var(--purple);display:block;line-height:1}
.step h3{font-size:1.4rem;margin:8px 0 4px}
.step p{color:var(--muted);font-size:.97rem}

/* Contact */
.contact{display:grid;grid-template-columns:.9fr 1.1fr;gap:50px}
.info p{margin:10px 0}
.info .btn{margin-top:18px}
form{background:var(--card);border:1px solid var(--line);border-radius:14px;padding:32px;display:grid;gap:16px;box-shadow:0 14px 34px rgba(0,0,0,.08)}
.row{display:grid;grid-template-columns:1fr 1fr;gap:16px}
label{font-weight:600;font-size:.95rem;display:block;margin-bottom:5px}
input,select,textarea{width:100%;font:inherit;color:var(--text);background:var(--paper);border:2px solid var(--line);border-radius:8px;padding:12px 14px;transition:border-color .2s,box-shadow .2s}
input:focus,select:focus,textarea:focus{outline:none;border-color:var(--sky);box-shadow:0 0 0 4px rgba(0,163,232,.2)}
textarea{min-height:130px;resize:vertical}
.hp{position:absolute;left:-9999px}
#msg{min-height:1.5em;font-weight:600}
#msg.ok{color:#168a47}#msg.err{color:var(--brick)}
form .btn[disabled]{opacity:.6;pointer-events:none}

footer{background:var(--ink);color:#c9cfd8;padding:34px 0;text-align:center;font-size:.95rem}
footer b{font-family:var(--display);font-weight:400;font-size:1.3rem;color:#fff;letter-spacing:.04em}

/* Floating WhatsApp */
.fab{position:fixed;left:20px;bottom:20px;z-index:60;width:62px;height:62px;border-radius:50%;background:#1fa855;display:grid;place-items:center;
  box-shadow:0 8px 22px rgba(0,0,0,.3);text-decoration:none;transition:transform .2s}
.fab:hover{transform:scale(1.1)}
.fab svg{width:34px;height:34px;fill:#fff}
.fab::before{content:"";position:absolute;inset:0;border-radius:50%;border:3px solid #1fa855;animation:ring 2s infinite}
@keyframes ring{from{transform:scale(1);opacity:.8}to{transform:scale(1.7);opacity:0}}

/* Reveal */
.rv{opacity:0;transform:translateY(34px);transition:opacity .7s,transform .7s}
.rv.in{opacity:1;transform:none}

@media (max-width:900px){
  .hero .wrap,.panel.show,.contact{grid-template-columns:1fr}
  .grid3,.steps{grid-template-columns:1fr 1fr}
  .stats .wrap{grid-template-columns:1fr 1fr}
  .skyline{height:360px;margin-top:20px}
  .burger{display:block}
  .menu{position:fixed;inset:0 0 auto 0;top:0;flex-direction:column;background:var(--paper);padding:90px 0 30px;gap:20px;
    transform:translateY(-110%);transition:transform .35s;box-shadow:0 10px 30px rgba(0,0,0,.2);z-index:-1}
  .menu.open{transform:none}
  .burger{z-index:2}
}
@media (max-width:560px){
  .grid3,.steps,.row{grid-template-columns:1fr}
  .tower.t1{width:110px}.tower.t2{width:92px}.house{width:110px;left:-14px}
}
@media (prefers-reduced-motion:reduce){
  *{animation-duration:.01ms!important;animation-delay:0s!important;transition-duration:.01ms!important}
  .rv{opacity:1;transform:none}
  .tower{transform:none}.house{opacity:1;transform:none}.hero h1 .ch{opacity:1;transform:none}
}
</style>
</head>
<body>
<div id="progress"></div>

<header class="nav" id="nav">
  <div class="wrap">
    <a href="#inicio" class="brand" aria-label="CASSIL, inicio">
      <svg viewBox="0 0 60 60" aria-hidden="true">
        <rect x="4" y="12" width="22" height="44" fill="#9b4a9e"/>
        <path d="M28 6 q8 2 12 6 h4 v44 H28z" fill="#00a3e8"/>
        <path d="M2 56 L16 40 L30 56z" fill="#8b0016"/><rect x="6" y="46" width="20" height="10" fill="#c8c8c8"/>
        <rect x="14" y="48" width="5" height="8" fill="#8b0016"/>
      </svg>
      <span>CASSIL</span>
    </a>
    <button class="burger" id="burger" aria-label="Abrir menú" aria-expanded="false" aria-controls="menu"><i></i></button>
    <ul class="menu" id="menu">
      <li><a href="#servicios">Servicios</a></li>
      <li><a href="#nosotros">Por qué CASSIL</a></li>
      <li><a href="#proceso">Cómo trabajamos</a></li>
      <li><a class="btn btn-wa" href="https://wa.me/51996351230?text=Hola%20CASSIL%2C%20quiero%20informaci%C3%B3n%20sobre%20inmuebles" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24"><path d="M12 2a10 10 0 0 0-8.6 15.1L2 22l5-1.3A10 10 0 1 0 12 2zm5.2 14c-.2.6-1.3 1.2-1.8 1.2-.5.1-1 .2-3.3-.7-2.8-1.2-4.6-4-4.7-4.2-.1-.2-1.1-1.5-1.1-2.8s.7-2 1-2.3c.2-.3.5-.3.7-.3h.5c.2 0 .4 0 .6.5l.8 1.9c.1.2.1.4 0 .5l-.4.6c-.1.2-.3.3-.1.6.2.3.8 1.300 1.700 2.100 1.200 1 2.100 1.300 2.400 1.500.3.1.4.1.6-.1l.8-1c.2-.3.4-.2.6-.1l1.800.9c.3.1.5.2.5.3.1.2.1.8-.1 1.400z"/></svg>
        WhatsApp</a></li>
    </ul>
  </div>
</header>

<main>
<!-- HERO -->
<section class="hero" id="inicio">
  <div class="wrap">
    <div>
      <h1 id="title" aria-label="CASSIL">CASSIL</h1>
      <p class="tag">Inmuebles para <span class="typed" id="typed"></span></p>
      <p class="lead">Alquiler, compra y venta con asesoría cercana desde la primera visita hasta la firma.</p>
      <div class="actions">
        <a class="btn btn-wa" href="https://wa.me/51996351230?text=Hola%20CASSIL%2C%20quiero%20informaci%C3%B3n%20sobre%20inmuebles" target="_blank" rel="noopener">
          <svg viewBox="0 0 24 24"><path d="M12 2a10 10 0 0 0-8.6 15.1L2 22l5-1.3A10 10 0 1 0 12 2zm5.2 14c-.2.6-1.3 1.2-1.8 1.2-.5.1-1 .2-3.3-.7-2.8-1.2-4.6-4-4.7-4.2-.1-.2-1.1-1.5-1.1-2.8s.7-2 1-2.3c.2-.3.5-.3.7-.3h.5c.2 0 .4 0 .6.5l.8 1.9c.1.2.1.4 0 .5l-.4.6c-.1.2-.3.3-.1.6.2.3.8 1.3 1.7 2.1 1.200 1 2.100 1.300 2.400 1.500.3.1.4.1.6-.1l.8-1c.2-.3.4-.2.6-.1l1.800.9c.3.1.5.2.5.3.1.2.1.8-.1 1.400z"/></svg>
          Escríbenos por WhatsApp</a>
        <a class="btn btn-line" href="#contacto">Enviar consulta</a>
      </div>
    </div>
    <div class="skyline" id="skyline" aria-hidden="true">
      <div class="tower t1" id="t1"></div>
      <div class="tower t2" id="t2"></div>
      <svg class="house" viewBox="0 0 150 130">
        <rect x="104" y="14" width="20" height="30" fill="#8b0016" stroke="#272727" stroke-width="3"/>
        <path d="M4 66 L72 10 L146 66 L136 74 L72 24 L14 74z" fill="#8b0016" stroke="#272727" stroke-width="3"/>
        <rect x="20" y="62" width="104" height="62" fill="#c8c8c8" stroke="#272727" stroke-width="2"/>
        <rect x="62" y="40" width="22" height="26" fill="#9fdcf0" stroke="#272727" stroke-width="3"/>
        <rect x="28" y="84" width="20" height="24" fill="#9fdcf0" stroke="#272727" stroke-width="3"/>
        <rect x="96" y="84" width="20" height="24" fill="#9fdcf0" stroke="#272727" stroke-width="3"/>
        <rect x="58" y="80" width="30" height="44" fill="#8b0016" stroke="#272727" stroke-width="2"/>
        <line x1="73" y1="80" x2="73" y2="124" stroke="#272727" stroke-width="2"/>
        <ellipse cx="12" cy="104" rx="9" ry="20" fill="#6aa621"/><ellipse cx="136" cy="108" rx="8" ry="16" fill="#2f7d3b"/>
      </svg>
      <div class="ground"></div>
    </div>
  </div>
</section>

<!-- SERVICIOS -->
<section id="servicios">
  <div class="wrap">
    <div class="head rv">
      <h2>Tres formas de mudarte con confianza</h2>
      <p class="lead">Elige lo que necesitas hoy. Nuestro equipo te guía en cada trámite.</p>
    </div>
    <div class="tabs rv" role="tablist" aria-label="Servicios">
      <button class="tab" role="tab" aria-selected="true" data-p="p1" id="tab1">Alquiler</button>
      <button class="tab" role="tab" aria-selected="false" data-p="p2" id="tab2">Compra</button>
      <button class="tab" role="tab" aria-selected="false" data-p="p3" id="tab3">Venta</button>
    </div>

    <div class="panel show" id="p1" role="tabpanel" aria-labelledby="tab1">
      <div>
        <h3>Alquila el lugar que se ajusta a ti</h3>
        <p class="lead">Departamentos, casas y locales verificados, con contrato claro y visitas coordinadas a tu horario.</p>
        <ul><li>Inmuebles revisados antes de publicarse</li><li>Contratos transparentes, sin letra chica</li><li>Acompañamiento durante toda la estadía</li></ul>
        <a class="btn btn-main" href="#contacto" data-interes="Alquiler">Quiero alquilar</a>
      </div>
      <div class="art a1"><svg viewBox="0 0 150 130" fill="none" stroke="#fff" stroke-width="5" stroke-linejoin="round"><path d="M10 64 L75 12 L140 64"/><rect x="26" y="60" width="98" height="62"/><circle cx="75" cy="86" r="10"/><path d="M85 86 h26 M101 86 v10"/></svg></div>
    </div>

    <div class="panel" id="p2" role="tabpanel" aria-labelledby="tab2">
      <div>
        <h3>Compra con asesoría de principio a fin</h3>
        <p class="lead">Te ayudamos a comparar opciones, revisar documentos y negociar el precio justo.</p>
        <ul><li>Búsqueda según tu presupuesto y zona</li><li>Revisión legal de la documentación</li><li>Apoyo para el proceso de financiamiento</li></ul>
        <a class="btn btn-main" href="#contacto" data-interes="Compra">Quiero comprar</a>
      </div>
      <div class="art a2"><svg viewBox="0 0 150 130" fill="none" stroke="#fff" stroke-width="5" stroke-linejoin="round"><rect x="20" y="20" width="46" height="102"/><rect x="72" y="8" width="40" height="114"/><path d="M30 40h26M30 58h26M30 76h26M82 30h20M82 48h20M82 66h20M82 84h20"/></svg></div>
    </div>

    <div class="panel" id="p3" role="tabpanel" aria-labelledby="tab3">
      <div>
        <h3>Vende tu inmueble al mejor precio</h3>
        <p class="lead">Valoramos tu propiedad, la promocionamos y filtramos a los interesados por ti.</p>
        <ul><li>Tasación basada en el mercado de tu zona</li><li>Difusión en redes y portales</li><li>Gestión de visitas y cierre de la venta</li></ul>
        <a class="btn btn-main" href="#contacto" data-interes="Venta">Quiero vender</a>
      </div>
      <div class="art a3"><svg viewBox="0 0 150 130" fill="none" stroke="#fff200" stroke-width="5" stroke-linejoin="round" stroke-linecap="round"><path d="M14 112 V70 M14 112 h122"/><path d="M26 96 L56 68 L82 84 L130 30"/><path d="M106 30 h24 v24"/></svg></div>
    </div>
  </div>
</section>

<!-- STATS -->
<div class="stats">
  <div class="wrap">
    <div><strong data-n="350" data-s="+">0</strong><span>inmuebles gestionados</span></div>
    <div><strong data-n="280" data-s="+">0</strong><span>familias atendidas</span></div>
    <div><strong data-n="10" data-s="+">0</strong><span>años de experiencia</span></div>
    <div><strong data-n="98" data-s="%">0</strong><span>clientes satisfechos</span></div>
  </div>
</div>

<!-- NOSOTROS -->
<section class="alt" id="nosotros">
  <div class="wrap">
    <div class="head rv">
      <h2>Por qué elegir CASSIL</h2>
      <p class="lead">Una inmobiliaria pensada para que cada decisión sea clara y segura.</p>
    </div>
    <div class="grid3">
      <article class="card rv"><div class="ico"><svg viewBox="0 0 24 24"><path d="M12 3l8 3v6c0 5-3.500 8-8 9-4.500-1-8-4-8-9V6z"/><path d="M9 12l2 2 4-4"/></svg></div><h3>Seguridad legal</h3><p>Revisamos títulos y contratos para que tu inversión esté protegida.</p></article>
      <article class="card rv"><div class="ico"><svg viewBox="0 0 24 24"><circle cx="9" cy="8" r="3.500"/><path d="M2 20c0-4 3-6 7-6s7 2 7 6"/><path d="M16 4a3.500 3.500 0 0 1 0 7M19 20c0-2.500-1-4.300-3-5.300"/></svg></div><h3>Trato cercano</h3><p>Un asesor responde tus dudas por WhatsApp y te acompaña en cada visita.</p></article>
      <article class="card rv"><div class="ico"><svg viewBox="0 0 24 24"><path d="M12 21s-7-6.200-7-11a7 7 0 0 1 14 0c0 4.800-7 11-7 11z"/><circle cx="12" cy="10" r="2.500"/></svg></div><h3>Conocemos tu zona</h3><p>Te mostramos opciones con precios reales y buena ubicación.</p></article>
    </div>
  </div>
</section>

<!-- PROCESO -->
<section id="proceso">
  <div class="wrap">
    <div class="head rv">
      <h2>Así trabajamos contigo</h2>
      <p class="lead">Cuatro pasos desde tu primer mensaje hasta las llaves en tu mano.</p>
    </div>
    <div class="steps">
      <div class="step rv"><h3>Cuéntanos qué buscas</h3><p>Escríbenos por WhatsApp o el formulario.</p></div>
      <div class="step rv"><h3>Recibe opciones</h3><p>Te enviamos inmuebles que encajan contigo.</p></div>
      <div class="step rv"><h3>Visita y compara</h3><p>Coordinamos las visitas en tu horario.</p></div>
      <div class="step rv"><h3>Firma tranquilo</h3><p>Nos encargamos de los documentos.</p></div>
    </div>
  </div>
</section>

<!-- CONTACTO -->
<section class="alt" id="contacto">
  <div class="wrap contact">
    <div class="info rv">
      <h2>Hablemos de tu próximo inmueble</h2>
      <p class="lead">Completa el formulario y te respondemos al correo, o escríbenos directo por WhatsApp para una respuesta más rápida.</p>
      <p><b>WhatsApp:</b> <a href="https://wa.me/51996351230" target="_blank" rel="noopener">996 351 230</a></p>
      <p><b>Correo:</b> <a href="mailto:cassilpremier@gmail.com">cassilpremier@gmail.com</a></p>
      <a class="btn btn-wa" href="https://wa.me/51996351230?text=Hola%20CASSIL%2C%20quiero%20informaci%C3%B3n%20sobre%20inmuebles" target="_blank" rel="noopener">Abrir chat de WhatsApp</a>
    </div>

    <form id="form" class="rv" action="https://formsubmit.co/cassilpremier@gmail.com" method="POST">
      <input type="hidden" name="_subject" value="Nueva consulta desde la web de CASSIL">
      <input type="hidden" name="_template" value="table">
      <input type="hidden" name="_captcha" value="false">
      <input class="hp" type="text" name="_honey" tabindex="-1" autocomplete="off" aria-hidden="true">
      <div class="row">
        <div><label for="nombre">Nombre completo</label><input id="nombre" name="Nombre" required autocomplete="name"></div>
        <div><label for="telefono">Teléfono</label><input id="telefono" name="Telefono" type="tel" required autocomplete="tel"></div>
      </div>
      <div class="row">
        <div><label for="email">Tu correo</label><input id="email" name="email" type="email" required autocomplete="email"></div>
        <div><label for="interes">Me interesa</label>
          <select id="interes" name="Servicio"><option>Alquiler</option><option>Compra</option><option>Venta</option></select></div>
      </div>
      <div><label for="mensaje">Mensaje</label><textarea id="mensaje" name="Mensaje" required placeholder="Zona, presupuesto, número de dormitorios..."></textarea></div>
      <button class="btn btn-main" type="submit" id="send">Enviar consulta</button>
      <p id="msg" role="status" aria-live="polite"></p>
    </form>
  </div>
</section>
</main>

<footer>
  <div class="wrap"><b>CASSIL</b><br>Alquiler, compra y venta de inmuebles &copy; <span id="year"></span></div>
</footer>

<a class="fab" href="https://wa.me/51996351230?text=Hola%20CASSIL%2C%20quiero%20informaci%C3%B3n%20sobre%20inmuebles" target="_blank" rel="noopener" aria-label="Escribir por WhatsApp">
  <svg viewBox="0 0 24 24"><path d="M12 2a10 10 0 0 0-8.6 15.1L2 22l5-1.3A10 10 0 1 0 12 2zm5.2 14c-.2.6-1.3 1.2-1.8 1.2-.5.1-1 .2-3.3-.7-2.8-1.2-4.6-4-4.7-4.2-.1-.2-1.1-1.5-1.1-2.8s.7-2 1-2.3c.2-.3.5-.3.7-.3h.5c.2 0 .4 0 .6.5l.8 1.9c.1.2.1.4 0 .5l-.4.6c-.1.2-.3.3-.1.6.2.3.8 1.3 1.7 2.1 1.200 1 2.100 1.300 2.400 1.500.3.1.4.1.6-.1l.8-1c.2-.3.4-.2.6-.1l1.800.9c.3.1.5.2.5.3.1.2.1.8-.1 1.400z"/></svg>
</a>

<script>
(function(){
  var $=function(s,c){return (c||document).querySelector(s)}, $$=function(s,c){return Array.prototype.slice.call((c||document).querySelectorAll(s))};
  var reduce=window.matchMedia('(prefers-reduced-motion: reduce)').matches;

  /* Año */
  $('#year').textContent=new Date().getFullYear();

  /* Letras del título que caen una a una */
  var title=$('#title'), txt=title.textContent; title.textContent='';
  txt.split('').forEach(function(c,i){
    var s=document.createElement('span'); s.className='ch'; s.setAttribute('aria-hidden','true');
    s.style.animationDelay=(0.1+i*0.09)+'s'; s.textContent=c; title.appendChild(s);
  });

  /* Ventanas de los edificios (se encienden al azar) */
  function windows(el,count){
    for(var i=0;i<count;i++){var w=document.createElement('div');w.className='w';el.appendChild(w);}
  }
  var t1=$('#t1'), t2=$('#t2'); windows(t1,60); windows(t2,28);
  var all=$$('.w');
  function flicker(){
    for(var i=0;i<4;i++){
      var w=all[Math.floor(Math.random()*all.length)]; w.classList.toggle('on');
    }
  }
  for(var k=0;k<10;k++) all[Math.floor(Math.random()*all.length)].classList.add('on');
  if(!reduce) setInterval(flicker,700);

  /* Efecto de escritura */
  var words=['alquilar','comprar','vender','empezar de nuevo'], wi=0, ci=0, del=false, typed=$('#typed');
  function type(){
    var w=words[wi];
    typed.textContent=w.slice(0,ci);
    if(!del && ci<w.length){ci++;setTimeout(type,100);}
    else if(!del){del=true;setTimeout(type,1400);}
    else if(ci>0){ci--;setTimeout(type,45);}
    else{del=false;wi=(wi+1)%words.length;setTimeout(type,300);}
  }
  if(reduce){typed.textContent=words[0];}else{type();}

  /* Barra de progreso, menú sólido y enlace activo */
  var nav=$('#nav'), bar=$('#progress'), links=$$('.menu a[href^="#"]:not(.btn)');
  var secs=links.map(function(a){return $(a.getAttribute('href'));});
  function onScroll(){
    var y=window.scrollY, h=document.documentElement.scrollHeight-window.innerHeight;
    bar.style.width=(y/h*100)+'%';
    nav.classList.toggle('solid',y>40);
    var cur=-1; secs.forEach(function(s,i){if(s&&s.getBoundingClientRect().top<140)cur=i;});
    links.forEach(function(a,i){a.classList.toggle('active',i===cur);});
    if(!reduce){var sk=$('#skyline'); if(sk&&y<window.innerHeight) sk.style.transform='translateY('+(y*0.12)+'px)';}
  }
  window.addEventListener('scroll',onScroll,{passive:true}); onScroll();

  /* Menú móvil */
  var burger=$('#burger'), menu=$('#menu');
  burger.addEventListener('click',function(){
    var open=menu.classList.toggle('open'); burger.setAttribute('aria-expanded',open);
  });
  $$('.menu a').forEach(function(a){a.addEventListener('click',function(){menu.classList.remove('open');burger.setAttribute('aria-expanded','false');});});

  /* Revelado al hacer scroll */
  var io=new IntersectionObserver(function(es){
    es.forEach(function(e){if(e.isIntersecting){e.target.classList.add('in');io.unobserve(e.target);}});
  },{threshold:.15});
  $$('.rv').forEach(function(el,i){el.style.transitionDelay=((i%4)*0.08)+'s';io.observe(el);});

  /* Contadores */
  var cio=new IntersectionObserver(function(es){
    es.forEach(function(e){
      if(!e.isIntersecting)return; cio.unobserve(e.target);
      var el=e.target, n=+el.dataset.n, s=el.dataset.s||'', t0=null;
      if(reduce){el.textContent=n+s;return;}
      function step(t){t0=t0||t;var p=Math.min((t-t0)/1600,1);el.textContent=Math.floor((1-Math.pow(1-p,3))*n)+s;if(p<1)requestAnimationFrame(step);}
      requestAnimationFrame(step);
    });
  },{threshold:.6});
  $$('[data-n]').forEach(function(el){cio.observe(el);});

  /* Pestañas de servicios */
  var tabs=$$('.tab');
  function showTab(id){
    tabs.forEach(function(t){t.setAttribute('aria-selected',t.dataset.p===id);});
    $$('.panel').forEach(function(p){p.classList.toggle('show',p.id===id);});
  }
  tabs.forEach(function(t,i){
    t.addEventListener('click',function(){showTab(t.dataset.p);});
    t.addEventListener('keydown',function(e){
      if(e.key==='ArrowRight'||e.key==='ArrowLeft'){
        var n=tabs[(i+(e.key==='ArrowRight'?1:tabs.length-1))%tabs.length]; n.focus(); showTab(n.dataset.p);
      }
    });
  });
  $$('[data-interes]').forEach(function(a){a.addEventListener('click',function(){$('#interes').value=a.dataset.interes;});});

  /* Inclinación 3D en tarjetas */
  if(!reduce && window.matchMedia('(hover:hover)').matches){
    $$('.card').forEach(function(c){
      c.addEventListener('mousemove',function(e){
        var r=c.getBoundingClientRect(), x=(e.clientX-r.left)/r.width-.5, y=(e.clientY-r.top)/r.height-.5;
        c.style.transform='perspective(700px) rotateY('+(x*10)+'deg) rotateX('+(-y*10)+'deg) translateY(-4px)';
      });
      c.addEventListener('mouseleave',function(){c.style.transform='';});
    });
  }

  /* Formulario: envía al correo cassilpremier@gmail.com */
  var form=$('#form'), msg=$('#msg'), send=$('#send');
  form.addEventListener('submit',function(e){
    e.preventDefault();
    msg.className=''; msg.textContent='Enviando...'; send.disabled=true;
    fetch('https://formsubmit.co/ajax/cassilpremier@gmail.com',{
      method:'POST',headers:{'Accept':'application/json'},body:new FormData(form)
    }).then(function(r){return r.json();}).then(function(d){
      if(d.success==='true'||d.success===true){
        msg.className='ok'; msg.textContent='Consulta enviada. Te responderemos pronto.'; form.reset();
      }else{throw new Error('fail');}
    }).catch(function(){
      msg.className='err'; msg.textContent='No pudimos enviar el formulario. Escríbenos por WhatsApp al 996 351 230.';
    }).then(function(){send.disabled=false;});
  });
})();
</script>

<!-- Chatbot n8n -->
<script type="module">
  import { createChat } from 'https://cdn.jsdelivr.net/npm/@n8n/chat/dist/chat.bundle.es.js';

  createChat({
    webhookUrl: 'https://jraffo.app.n8n.cloud/webhook/8f419458-97b0-4f83-9c4a-961d4be0bb01/chat',
    mode: 'window',
    loadPreviousSession: false,
    showWelcomeScreen: false,
    defaultLanguage: 'en',
    initialMessages: [
      '¡Hola! Bienvenido.',
      '¿Buscas alquilar, comprar o vender un inmueble? Cuéntame y te ayudo.'
    ],
    i18n: {
      en: {
        title: 'Asesor inmobiliario',
        subtitle: 'Alquiler, compra y venta de inmuebles',
        footer: '',
        getStarted: 'Nueva conversación',
        inputPlaceholder: 'Escribe tu consulta...'
      }
    }
  });
</script>
</body>
</html>
