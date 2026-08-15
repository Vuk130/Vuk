<!DOCTYPE html>
<html lang="sr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>WebStudio — Premium Web Design</title>
<meta name="description" content="WebStudio — premium web sajtovi za moderne biznise.">
<meta name="theme-color" content="#08080c">

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Space+Grotesk:wght@400;500;600;700&display=swap');

:root{
 --bg:#07070a;
 --surface:#0d0e13;
 --surface2:#12131a;
 --text:#f5f5f7;
 --muted:#9699a6;
 --line:rgba(255,255,255,.1);
 --accent:#8b7cff;
 --accent2:#5eead4;
 --max:1200px;
}

*{margin:0;padding:0;box-sizing:border-box}
html{scroll-behavior:smooth}
body{
 font-family:"DM Sans",sans-serif;
 background:var(--bg);
 color:var(--text);
 overflow-x:hidden;
}
body.light{
 --bg:#f5f5f7;
 --surface:#fff;
 --surface2:#ededf2;
 --text:#101116;
 --muted:#646774;
 --line:rgba(0,0,0,.1);
}
a{text-decoration:none;color:inherit}
button,input,textarea,select{font:inherit}
button{cursor:pointer}
.container{width:min(var(--max),92%);margin:auto}

#progress{
 position:fixed;
 top:0;left:0;
 width:0;height:3px;
 background:linear-gradient(90deg,var(--accent),var(--accent2));
 z-index:9999;
}

header{
 position:fixed;
 top:0;left:0;
 width:100%;
 z-index:1000;
 padding:18px 0;
 transition:.3s;
}
header.scrolled{
 background:rgba(7,7,10,.75);
 backdrop-filter:blur(20px);
 border-bottom:1px solid var(--line);
}
.nav{
 display:flex;
 justify-content:space-between;
 align-items:center;
}
.logo{
 font-family:"Space Grotesk";
 font-size:25px;
 font-weight:700;
 letter-spacing:-1.5px;
}
.logo i{font-style:normal;color:var(--accent)}
nav{display:flex;gap:30px}
nav a{
 color:var(--muted);
 font-size:13px;
 transition:.25s;
}
nav a:hover{color:var(--text)}
.actions{display:flex;gap:9px;align-items:center}
.circle{
 width:40px;height:40px;
 border-radius:50%;
 border:1px solid var(--line);
 background:var(--surface);
 color:var(--text);
}
.menu{display:none}

.hero{
 min-height:100vh;
 display:flex;
 align-items:center;
 position:relative;
 overflow:hidden;
 padding:140px 0 90px;
}
.hero-grid{
 position:absolute;
 inset:0;
 background-image:
 linear-gradient(rgba(255,255,255,.035) 1px,transparent 1px),
 linear-gradient(90deg,rgba(255,255,255,.035) 1px,transparent 1px);
 background-size:70px 70px;
 mask-image:linear-gradient(to bottom,#000,transparent 85%);
}
.glow{
 position:absolute;
 width:650px;height:650px;
 border-radius:50%;
 background:radial-gradient(circle,rgba(139,124,255,.2),transparent 68%);
 filter:blur(20px);
 top:-250px;left:-220px;
}
.glow2{
 position:absolute;
 width:550px;height:550px;
 border-radius:50%;
 background:radial-gradient(circle,rgba(94,234,212,.1),transparent 68%);
 right:-250px;bottom:-200px;
}
.hero-content{position:relative;z-index:2;max-width:1000px}
.pill{
 display:inline-flex;
 align-items:center;
 gap:9px;
 border:1px solid var(--line);
 background:rgba(255,255,255,.035);
 padding:9px 14px;
 border-radius:100px;
 font-size:12px;
 color:#bbb7ff;
 margin-bottom:25px;
 animation:up .8s both;
}
.live{
 width:7px;height:7px;
 border-radius:50%;
 background:#5eead4;
 box-shadow:0 0 15px #5eead4;
}
.hero h1{
 font-family:"Space Grotesk";
 font-size:clamp(52px,8vw,105px);
 line-height:.93;
 letter-spacing:-6px;
 max-width:1050px;
 animation:up .8s .08s both;
}
.gradient{
 background:linear-gradient(100deg,#fff 10%,#9b8fff 48%,#5eead4 100%);
 -webkit-background-clip:text;
 color:transparent;
}
.hero p{
 max-width:700px;
 color:var(--muted);
 font-size:18px;
 line-height:1.7;
 margin:30px 0;
 animation:up .8s .16s both;
}
.buttons{
 display:flex;
 gap:12px;
 flex-wrap:wrap;
 animation:up .8s .24s both;
}
.btn{
 display:inline-flex;
 align-items:center;
 justify-content:center;
 gap:10px;
 padding:15px 22px;
 border-radius:12px;
 border:1px solid var(--line);
 font-size:13px;
 font-weight:700;
 transition:.3s;
}
.primary{
 background:var(--text);
 color:var(--bg);
 border-color:var(--text);
}
.primary:hover{transform:translateY(-4px);box-shadow:0 20px 50px rgba(139,124,255,.25)}
.secondary{background:rgba(255,255,255,.04)}
.secondary:hover{border-color:var(--accent);transform:translateY(-4px)}
.hero-bottom{
 display:flex;
 gap:45px;
 margin-top:55px;
 animation:up .8s .32s both;
}
.metric strong{font-size:25px;font-family:"Space Grotesk"}
.metric span{display:block;color:var(--muted);font-size:11px;margin-top:3px}

section{padding:120px 0}
.section-top{margin-bottom:55px;max-width:760px}
.kicker{
 color:#a69dff;
 text-transform:uppercase;
 letter-spacing:2px;
 font-size:11px;
 font-weight:700;
 margin-bottom:13px;
}
.section-top h2{
 font-family:"Space Grotesk";
 font-size:clamp(38px,5vw,64px);
 line-height:1;
 letter-spacing:-3.5px;
 margin-bottom:17px;
}
.section-top p{color:var(--muted);line-height:1.7}

.services{
 display:grid;
 grid-template-columns:repeat(3,1fr);
 gap:16px;
}
.card{
 background:linear-gradient(145deg,var(--surface),rgba(255,255,255,.025));
 border:1px solid var(--line);
 border-radius:24px;
 padding:30px;
 transition:.4s;
}
.card:hover{
 transform:translateY(-8px);
 border-color:rgba(139,124,255,.5);
 box-shadow:0 30px 80px rgba(0,0,0,.25);
}
.icon{
 width:52px;height:52px;
 border-radius:15px;
 display:grid;place-items:center;
 background:linear-gradient(135deg,rgba(139,124,255,.18),rgba(94,234,212,.08));
 font-size:23px;
 margin-bottom:25px;
}
.card h3{font-family:"Space Grotesk";font-size:20px;margin-bottom:10px}
.card p{color:var(--muted);font-size:14px;line-height:1.7}

.ticker{
 border-top:1px solid var(--line);
 border-bottom:1px solid var(--line);
 padding:22px 0;
 overflow:hidden;
 white-space:nowrap;
}
.ticker-track{
 display:flex;
 width:max-content;
 gap:40px;
 animation:marquee 25s linear infinite;
}
.ticker span{font-family:"Space Grotesk";font-weight:600;color:var(--muted)}
.ticker b{color:var(--accent)}

.projects{
 display:grid;
 grid-template-columns:repeat(12,1fr);
 gap:17px;
}
.project{
 min-height:420px;
 border-radius:27px;
 border:1px solid var(--line);
 overflow:hidden;
 position:relative;
 background:var(--surface);
 transition:.4s;
}
.project:nth-child(1){grid-column:span 7}
.project:nth-child(2){grid-column:span 5}
.project:nth-child(3){grid-column:span 5}
.project:nth-child(4){grid-column:span 7}
.project:hover{transform:translateY(-8px)}
.project-art{
 position:absolute;
 inset:0;
 display:grid;
 place-items:center;
 font-size:110px;
 opacity:.12;
 background:
 radial-gradient(circle at 50% 30%,rgba(139,124,255,.22),transparent 55%);
}
.project-info{
 position:absolute;
 left:28px;right:28px;bottom:25px;
 z-index:2;
}
.project-tag{font-size:10px;color:#a59cff;font-weight:700;letter-spacing:1.5px}
.project-info h3{
 font-family:"Space Grotesk";
 font-size:30px;
 margin:6px 0;
}
.project-info p{color:var(--muted);font-size:13px}

.process{
 display:grid;
 grid-template-columns:repeat(4,1fr);
 gap:15px;
}
.step{
 padding:28px;
 border:1px solid var(--line);
 background:var(--surface);
 border-radius:22px;
}
.number{color:#777;font-size:11px;margin-bottom:45px}
.step h3{font-family:"Space Grotesk";margin-bottom:9px}
.step p{color:var(--muted);font-size:13px;line-height:1.7}

.pricing{
 display:grid;
 grid-template-columns:repeat(3,1fr);
 gap:17px;
}
.price-card{
 border:1px solid var(--line);
 background:var(--surface);
 border-radius:25px;
 padding:32px;
 position:relative;
}
.price-card.hot{
 border-color:var(--accent);
 box-shadow:0 0 70px rgba(139,124,255,.1);
}
.badge-price{
 position:absolute;
 top:18px;right:18px;
 background:var(--accent);
 padding:6px 9px;
 border-radius:50px;
 font-size:9px;
 font-weight:800;
}
.price{
 font-family:"Space Grotesk";
 font-size:43px;
 font-weight:700;
 margin:20px 0;
}
.price small{font-family:"DM Sans";font-size:12px;color:var(--muted)}
.features{list-style:none;margin:25px 0}
.features li{color:var(--muted);font-size:13px;margin:12px 0}
.features li::first-letter{color:var(--accent2)}

.stats{
 background:var(--surface);
 border-top:1px solid var(--line);
 border-bottom:1px solid var(--line);
}
.stats-grid{
 display:grid;
 grid-template-columns:repeat(4,1fr);
 text-align:center;
 gap:20px;
}
.stats strong{
 font-family:"Space Grotesk";
 font-size:48px;
 letter-spacing:-3px;
}
.stats span{display:block;color:var(--muted);font-size:12px}

.faq{max-width:850px;margin:auto}
details{
 border:1px solid var(--line);
 background:var(--surface);
 border-radius:16px;
 padding:20px 23px;
 margin-bottom:10px;
}
summary{cursor:pointer;font-weight:700;font-size:14px}
details p{color:var(--muted);font-size:13px;line-height:1.7;padding-top:14px}

.cta-box{
 border:1px solid var(--line);
 border-radius:30px;
 text-align:center;
 padding:90px 25px;
 background:
 radial-gradient(circle at 50% 0%,rgba(139,124,255,.25),transparent 50%),
 var(--surface);
}
.cta-box h2{
 font-family:"Space Grotesk";
 font-size:clamp(40px,6vw,70px);
 line-height:1;
 letter-spacing:-4px;
 margin-bottom:18px;
}
.cta-box p{
 max-width:600px;
 color:var(--muted);
 margin:0 auto 30px;
 line-height:1.7;
}

.contact-grid{
 display:grid;
 grid-template-columns:1fr 1fr;
 gap:50px;
 align-items:center;
}
.contact h2{
 font-family:"Space Grotesk";
 font-size:55px;
 line-height:1;
 letter-spacing:-3px;
 margin-bottom:18px;
}
.contact-text{color:var(--muted);line-height:1.7;max-width:520px}
.email{
 display:inline-block;
 color:#a49aff;
 font-weight:700;
 margin-top:25px;
}
.form{
 padding:30px;
 border:1px solid var(--line);
 background:var(--surface);
 border-radius:25px;
}
.field{margin-bottom:14px}
.field label{
 display:block;
 color:var(--muted);
 font-size:10px;
 margin-bottom:7px;
 text-transform:uppercase;
 letter-spacing:1px;
}
.field input,.field textarea,.field select{
 width:100%;
 border:1px solid var(--line);
 background:rgba(255,255,255,.035);
 color:var(--text);
 border-radius:11px;
 padding:14px;
 outline:none;
}
.field textarea{min-height:120px;resize:vertical}
.field input:focus,.field textarea:focus,.field select:focus{border-color:var(--accent)}
.form .btn{width:100%;border:0}

footer{
 border-top:1px solid var(--line);
 padding:35px 0;
}
.footer{
 display:flex;
 justify-content:space-between;
 align-items:center;
 gap:20px;
}
.footer p{color:var(--muted);font-size:11px}

.reveal{
 opacity:0;
 transform:translateY(35px);
 transition:.8s ease;
}
.reveal.show{opacity:1;transform:none}

.cursor{
 position:fixed;
 width:20px;height:20px;
 border:1px solid rgba(255,255,255,.7);
 border-radius:50%;
 pointer-events:none;
 z-index:10000;
 transform:translate(-50%,-50%);
 transition:width .2s,height .2s;
 mix-blend-mode:difference;
}
.cursor.big{width:45px;height:45px}

@keyframes up{
 from{opacity:0;transform:translateY(25px)}
 to{opacity:1;transform:none}
}
@keyframes marquee{
 from{transform:translateX(0)}
 to{transform:translateX(-50%)}
}

@media(max-width:900px){
 nav{display:none}
 .menu{display:block}
 nav.open{
  display:flex;
  position:absolute;
  top:75px;left:4%;right:4%;
  flex-direction:column;
  background:var(--surface);
  border:1px solid var(--line);
  padding:25px;
  border-radius:20px;
 }
 .services,.pricing{grid-template-columns:1fr}
 .process{grid-template-columns:1fr 1fr}
 .stats-grid{grid-template-columns:1fr 1fr}
 .contact-grid{grid-template-columns:1fr}
 .projects{grid-template-columns:1fr}
 .project:nth-child(n){grid-column:span 1}
 .cursor{display:none}
}
@media(max-width:600px){
 section{padding:80px 0}
 .hero h1{letter-spacing:-3px}
 .hero-bottom{gap:22px;flex-wrap:wrap}
 .process{grid-template-columns:1fr}
 .contact h2{font-size:43px}
 .footer{flex-direction:column;text-align:center}
}
</style>
</head>

<body>

<div id="progress"></div>
<div class="cursor" id="cursor"></div>

<header id="header">
<div class="container nav">

<a href="#" class="logo">Web<i>Studio</i></a>

<nav id="nav">
<a href="#usluge">Usluge</a>
<a href="#radovi">Radovi</a>
<a href="#proces">Proces</a>
<a href="#cene">Cene</a>
<a href="#faq">FAQ</a>
<a href="#kontakt">Kontakt</a>
</nav>

<div class="actions">
<button class="circle" id="theme">☼</button>
<button class="circle" id="lang">EN</button>
<button class="circle menu" id="menu">☰</button>
</div>

</div>
</header>


<section class="hero">

<div class="hero-grid"></div>
<div class="glow"></div>
<div class="glow2"></div>

<div class="container hero-content">

<div class="pill">
<span class="live"></span>
Dostupni za nove projekte
</div>

<h1>
Tvoj biznis zaslužuje
<span class="gradient">bolji web.</span>
</h1>

<p>
Kreiramo moderne, brze i profesionalne web sajtove
koji pretvaraju posetioce u potencijalne klijente.
Dizajniran od nule prema tvom biznisu.
</p>

<div class="buttons">
<a class="btn primary" href="#kontakt">Započni projekat →</a>
<a class="btn secondary" href="#radovi">Pogledaj radove</a>
</div>

<div class="hero-bottom">
<div class="metric"><strong>100%</strong><span>Responsive</span></div>
<div class="metric"><strong>24/7</strong><span>Online prisustvo</span></div>
<div class="metric"><strong>∞</strong><span>Mogućnosti</span></div>
</div>

</div>
</section>


<div class="ticker">
<div class="ticker-track">
<span>WEB DESIGN</span><b>✦</b>
<span>BRANDING</span><b>✦</b>
<span>RESPONSIVE</span><b>✦</b>
<span>MODERN UI</span><b>✦</b>
<span>FAST WEBSITES</span><b>✦</b>
<span>WEB DESIGN</span><b>✦</b>
<span>BRANDING</span><b>✦</b>
<span>RESPONSIVE</span><b>✦</b>
<span>MODERN UI</span><b>✦</b>
<span>FAST WEBSITES</span><b>✦</b>
</div>
</div>


<section id="usluge">
<div class="container">

<div class="section-top reveal">
<div class="kicker">Šta radimo</div>
<h2>Sve što treba za ozbiljan online nastup.</h2>
<p>Od prve ideje do gotovog sajta, svaki detalj je napravljen da izgleda profesionalno.</p>
</div>

<div class="services">

<div class="card reveal">
<div class="icon">✦</div>
<h3>Premium dizajn</h3>
<p>Moderan vizuelni sistem, tipografija, boje i raspored koji odgovaraju tvom brendu.</p>
</div>

<div class="card reveal">
<div class="icon">⌁</div>
<h3>Responsive</h3>
<p>Perfektno prilagođeno telefonima, tabletima, laptopovima i velikim ekranima.</p>
</div>

<div class="card reveal">
<div class="icon">⚡</div>
<h3>Brzina</h3>
<p>Lagana i optimizovana struktura za brzo učitavanje i dobro korisničko iskustvo.</p>
</div>

<div class="card reveal">
<div class="icon">▣</div>
<h3>Galerije</h3>
<p>Predstavi proizvode, apartmane, restoran, radove ili usluge kroz atraktivne galerije.</p>
</div>

<div class="card reveal">
<div class="icon">◎</div>
<h3>Kontakt</h3>
<p>Email, telefon, društvene mreže, lokacija i jasni pozivi na akciju.</p>
</div>

<div class="card reveal">
<div class="icon">↗</div>
<h3>SEO osnova</h3>
<p>Semantička struktura i osnovni meta podaci pripremljeni za pretraživače.</p>
</div>

</div>
</div>
</section>


<section id="radovi">
<div class="container">

<div class="section-top reveal">
<div class="kicker">Portfolio</div>
<h2>Jedan studio. Bezbroj mogućnosti.</h2>
<p>Primeri pravaca u kojima možemo napraviti potpuno prilagođen sajt.</p>
</div>

<div class="projects">

<div class="project reveal">
<div class="project-art">🏠</div>
<div class="project-info">
<div class="project-tag">HOSPITALITY</div>
<h3>Premium Apartmani</h3>
<p>Galerija · sobe · sadržaji · lokacija · kontakt</p>
</div>
</div>

<div class="project reveal">
<div class="project-art">🍽️</div>
<div class="project-info">
<div class="project-tag">RESTAURANT</div>
<h3>Fine Dining</h3>
<p>Meni · galerija · rezervacije · lokacija</p>
</div>
</div>

<div class="project reveal">
<div class="project-art">💎</div>
<div class="project-info">
<div class="project-tag">BRAND</div>
<h3>Luxury Brand</h3>
<p>Proizvodi · kolekcije · priča · kontakt</p>
</div>
</div>

<div class="project reveal">
<div class="project-art">🚘</div>
<div class="project-info">
<div class="project-tag">AUTOMOTIVE</div>
<h3>Detailing Studio</h3>
<p>Usluge · paketi · galerija · kontakt</p>
</div>
</div>

</div>
</div>
</section>


<section id="proces">
<div class="container">

<div class="section-top reveal">
<div class="kicker">Proces</div>
<h2>Od prve poruke do gotovog sajta.</h2>
<p>Jednostavan proces bez nepotrebnog komplikovanja.</p>
</div>

<div class="process">

<div class="step reveal">
<div class="number">01 / DISCOVER</div>
<h3>Razgovor</h3>
<p>Upoznajemo tvoj biznis, ciljnu grupu i ono što želiš da postigneš.</p>
</div>

<div class="step reveal">
<div class="number">02 / DESIGN</div>
<h3>Dizajn</h3>
<p>Biramo vizuelni pravac, strukturu, sadržaj i funkcionalnosti.</p>
</div>

<div class="step reveal">
<div class="number">03 / BUILD</div>
<h3>Izrada</h3>
<p>Koncept pretvaramo u brz i potpuno responsive sajt.</p>
</div>

<div class="step reveal">
<div class="number">04 / LAUNCH</div>
<h3>Objava</h3>
<p>Sajt se priprema za objavljivanje i povezivanje sa domenom.</p>
</div>

</div>
</div>
</section>


<section id="cene">
<div class="container">

<div class="section-top reveal">
<div class="kicker">Paketi</div>
<h2>Jednostavne cene. Ozbiljan rezultat.</h2>
<p>Konačna cena zavisi od obima i funkcionalnosti projekta.</p>
</div>

<div class="pricing">

<div class="price-card reveal">
<h3>Starter</h3>
<p>Za jednostavno online prisustvo.</p>
<div class="price">50€</div>

<ul class="features">
<li>✓ Jedna stranica</li>
<li>✓ Responsive dizajn</li>
<li>✓ Kontakt dugme</li>
<li>✓ Osnovna galerija</li>
</ul>

<a class="btn secondary" href="mailto:vuk.markovic3001@gmail.com?subject=Starter%20paket">Zatraži ponudu</a>
</div>


<div class="price-card hot reveal">
<div class="badge-price">POPULARNO</div>
<h3>Business</h3>
<p>Za ozbiljniji biznis i brend.</p>
<div class="price">100€</div>

<ul class="features">
<li>✓ Više sekcija</li>
<li>✓ Premium dizajn</li>
<li>✓ Galerija</li>
<li>✓ Kontakt sistem</li>
<li>✓ Animacije</li>
</ul>

<a class="btn primary" href="mailto:vuk.markovic3001@gmail.com?subject=Business%20paket">Zatraži ponudu</a>
</div>


<div class="price-card reveal">
<h3>Premium</h3>
<p>Za napredniji projekat.</p>
<div class="price">200€</div>

<ul class="features">
<li>✓ Više stranica</li>
<li>✓ Napredni UI</li>
<li>✓ Animacije</li>
<li>✓ Galerija</li>
<li>✓ Dodatne funkcije</li>
</ul>

<a class="btn secondary" href="mailto:vuk.markovic3001@gmail.com?subject=Premium%20paket">Zatraži ponudu</a>
</div>

</div>
</div>
</section>


<section class="stats">
<div class="container">
<div class="stats-grid">

<div><strong>100%</strong><span>responsive</span></div>
<div><strong>24/7</strong><span>online</span></div>
<div><strong>∞</strong><span>mogućnosti</span></div>
<div><strong>1:1</strong><span>prilagođeno</span></div>

</div>
</div>
</section>


<section id="faq">
<div class="container">

<div class="section-top reveal">
<div class="kicker">FAQ</div>
<h2>Česta pitanja.</h2>
<p>Sve što treba da znaš pre početka projekta.</p>
</div>

<div class="faq">

<details class="reveal">
<summary>Koliko traje izrada?</summary>
<p>Jednostavniji projekti mogu biti gotovi za nekoliko dana. Rok zavisi od sadržaja i zahtevnosti projekta.</p>
</details>

<details class="reveal">
<summary>Da li sajt radi na telefonu?</summary>
<p>Da. Dizajn se prilagođava različitim veličinama ekrana.</p>
</details>

<details class="reveal">
<summary>Da li mogu da pošaljem svoje fotografije?</summary>
<p>Da. Fotografije, logo, tekstove i druge materijale možemo koristiti u dizajnu.</p>
</details>

<details class="reveal">
<summary>Da li mogu da imam svoj domen?</summary>
<p>Da. Sajt se može povezati sa sopstvenim domenom kada bude spreman za objavljivanje.</p>
</details>

<details class="reveal">
<summary>Da li možete napraviti sajt na engleskom?</summary>
<p>Da. Sajt može biti na srpskom, engleskom ili kao dvojezična verzija.</p>
</details>

</div>
</div>
</section>


<section>
<div class="container">

<div class="cta-box reveal">
<div class="kicker">LET'S BUILD</div>
<h2>Spreman za svoj<br><span class="gradient">novi sajt?</span></h2>
<p>Pošalji nam informacije o svom biznisu i napravićemo plan za tvoj projekat.</p>

<a class="btn primary" href="#ko
