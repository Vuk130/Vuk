<!DOCTYPE html>
<html lang="sr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>WebStudio — Digital Experiences</title>

<meta name="description" content="WebStudio — premium web dizajn i digitalna iskustva za moderne biznise.">
<meta name="theme-color" content="#050507">

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Space+Grotesk:wght@400;500;600;700&display=swap');

:root{
    --bg:#050507;
    --surface:#0b0b10;
    --surface2:#111117;
    --text:#f7f7f8;
    --muted:#8d8e99;
    --line:rgba(255,255,255,.09);
    --accent:#8b7cff;
    --accent2:#5eead4;
    --white:#fff;
    --max:1240px;
}

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:"DM Sans",sans-serif;
    background:var(--bg);
    color:var(--text);
    overflow-x:hidden;
}

body.light{
    --bg:#f5f5f7;
    --surface:#fff;
    --surface2:#ececf1;
    --text:#101014;
    --muted:#666875;
    --line:rgba(0,0,0,.09);
}

a{
    color:inherit;
    text-decoration:none;
}

button,
input,
textarea,
select{
    font:inherit;
}

button{
    cursor:pointer;
}

.container{
    width:min(var(--max),92%);
    margin:auto;
}

/* PROGRESS */

#progress{
    position:fixed;
    top:0;
    left:0;
    height:3px;
    width:0;
    background:linear-gradient(90deg,var(--accent),var(--accent2));
    z-index:99999;
}

/* HEADER */

header{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    z-index:1000;
    padding:20px 0;
    transition:.35s;
}

header.scrolled{
    background:rgba(5,5,7,.72);
    backdrop-filter:blur(22px);
    border-bottom:1px solid var(--line);
}

.nav{
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.logo{
    font-family:"Space Grotesk";
    font-weight:700;
    font-size:25px;
    letter-spacing:-1.5px;
}

.logo span{
    color:var(--accent);
}

nav{
    display:flex;
    gap:28px;
}

nav a{
    color:var(--muted);
    font-size:13px;
    transition:.25s;
}

nav a:hover{
    color:var(--text);
}

.nav-actions{
    display:flex;
    align-items:center;
    gap:8px;
}

.round{
    width:40px;
    height:40px;
    border-radius:50%;
    border:1px solid var(--line);
    background:var(--surface);
    color:var(--text);
}

.menu{
    display:none;
}

/* HERO */

.hero{
    min-height:100vh;
    display:flex;
    align-items:center;
    position:relative;
    overflow:hidden;
    padding:150px 0 90px;
}

.grid{
    position:absolute;
    inset:0;
    background-image:
        linear-gradient(rgba(255,255,255,.035) 1px,transparent 1px),
        linear-gradient(90deg,rgba(255,255,255,.035) 1px,transparent 1px);
    background-size:70px 70px;
    mask-image:linear-gradient(to bottom,#000,transparent 85%);
}

.orb{
    position:absolute;
    border-radius:50%;
    pointer-events:none;
}

.orb1{
    width:650px;
    height:650px;
    left:-260px;
    top:-260px;
    background:radial-gradient(circle,rgba(139,124,255,.23),transparent 68%);
    filter:blur(15px);
}

.orb2{
    width:600px;
    height:600px;
    right:-280px;
    bottom:-300px;
    background:radial-gradient(circle,rgba(94,234,212,.11),transparent 68%);
    filter:blur(20px);
}

.hero-content{
    position:relative;
    z-index:3;
    max-width:1100px;
}

.available{
    display:inline-flex;
    align-items:center;
    gap:9px;
    border:1px solid var(--line);
    background:rgba(255,255,255,.035);
    border-radius:100px;
    padding:9px 14px;
    color:#b9b3ff;
    font-size:11px;
    margin-bottom:26px;
    animation:rise .8s both;
}

.status{
    width:7px;
    height:7px;
    border-radius:50%;
    background:var(--accent2);
    box-shadow:0 0 15px var(--accent2);
}

.hero h1{
    font-family:"Space Grotesk";
    font-size:clamp(55px,9vw,112px);
    line-height:.9;
    letter-spacing:-7px;
    max-width:1100px;
    animation:rise .8s .08s both;
}

.hero h1 em{
    font-style:normal;
    background:linear-gradient(100deg,#fff,#9d91ff,#5eead4);
    -webkit-background-clip:text;
    color:transparent;
}

.hero-copy{
    max-width:700px;
    color:var(--muted);
    font-size:18px;
    line-height:1.75;
    margin:32px 0;
    animation:rise .8s .16s both;
}

.actions{
    display:flex;
    gap:12px;
    flex-wrap:wrap;
    animation:rise .8s .24s both;
}

.btn{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    gap:9px;
    padding:15px 22px;
    border-radius:12px;
    border:1px solid var(--line);
    font-size:13px;
    font-weight:700;
    transition:.35s;
}

.btn-main{
    background:var(--text);
    color:var(--bg);
}

.btn-main:hover{
    transform:translateY(-5px);
    box-shadow:0 25px 60px rgba(139,124,255,.2);
}

.btn-outline{
    background:rgba(255,255,255,.035);
}

.btn-outline:hover{
    border-color:var(--accent);
    transform:translateY(-5px);
}

.hero-meta{
    display:flex;
    gap:42px;
    margin-top:55px;
    animation:rise .8s .32s both;
}

.hero-meta strong{
    display:block;
    font-family:"Space Grotesk";
    font-size:25px;
}

.hero-meta span{
    color:var(--muted);
    font-size:11px;
}

/* FLOATING CARD */

.floating-card{
    position:absolute;
    right:5%;
    bottom:11%;
    width:270px;
    padding:18px;
    border:1px solid var(--line);
    border-radius:20px;
    background:rgba(15,15,22,.65);
    backdrop-filter:blur(20px);
    box-shadow:0 30px 100px rgba(0,0,0,.4);
    transform:rotate(4deg);
    animation:float 5s ease-in-out infinite;
}

.mini-screen{
    height:130px;
    border-radius:13px;
    background:
        radial-gradient(circle at 75% 20%,rgba(94,234,212,.4),transparent 25%),
        linear-gradient(135deg,#292453,#11121b);
    position:relative;
    overflow:hidden;
}

.mini-screen:after{
    content:"";
    position:absolute;
    width:140px;
    height:140px;
    border-radius:50%;
    border:1px solid rgba(255,255,255,.15);
    right:-35px;
    top:-35px;
}

.floating-bottom{
    display:flex;
    justify-content:space-between;
    margin-top:13px;
    font-size:11px;
}

.floating-bottom span{
    color:var(--muted);
}

/* GENERAL */

section{
    padding:125px 0;
}

.section-head{
    max-width:760px;
    margin-bottom:55px;
}

.center{
    text-align:center;
    margin-left:auto;
    margin-right:auto;
}

.kicker{
    color:#a79fff;
    font-size:10px;
    text-transform:uppercase;
    letter-spacing:2px;
    font-weight:700;
    margin-bottom:14px;
}

.section-head h2{
    font-family:"Space Grotesk";
    font-size:clamp(40px,5.5vw,68px);
    line-height:.98;
    letter-spacing:-4px;
    margin-bottom:18px;
}

.section-head p{
    color:var(--muted);
    line-height:1.7;
}

/* SERVICES */

.services{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:16px;
}

.service{
    border:1px solid var(--line);
    border-radius:25px;
    background:linear-gradient(145deg,var(--surface),rgba(255,255,255,.02));
    padding:31px;
    transition:.4s;
}

.service:hover{
    transform:translateY(-9px);
    border-color:rgba(139,124,255,.5);
    box-shadow:0 35px 90px rgba(0,0,0,.28);
}

.service-icon{
    width:54px;
    height:54px;
    border-radius:16px;
    display:grid;
    place-items:center;
    background:linear-gradient(135deg,rgba(139,124,255,.2),rgba(94,234,212,.07));
    font-size:24px;
    margin-bottom:25px;
}

.service h3{
    font-family:"Space Grotesk";
    font-size:20px;
    margin-bottom:10px;
}

.service p{
    color:var(--muted);
    font-size:13px;
    line-height:1.75;
}

/* TICKER */

.ticker{
    overflow:hidden;
    white-space:nowrap;
    border-top:1px solid var(--line);
    border-bottom:1px solid var(--line);
    padding:21px 0;
}

.ticker-track{
    width:max-content;
    display:flex;
    gap:42px;
    animation:marquee 27s linear infinite;
}

.ticker span{
    color:var(--muted);
    font-family:"Space Grotesk";
    font-size:13px;
    font-weight:600;
}

.ticker b{
    color:var(--accent);
}

/* PROJECTS */

.projects{
    display:grid;
    grid-template-columns:repeat(12,1fr);
    gap:17px;
}

.project{
    position:relative;
    min-height:430px;
    border-radius:28px;
    border:1px solid var(--line);
    overflow:hidden;
    background:var(--surface);
    transition:.45s;
}

.project:nth-child(1),
.project:nth-child(4){
    grid-column:span 7;
}

.project:nth-child(2),
.project:nth-child(3){
    grid-column:span 5;
}

.project:hover{
    transform:translateY(-9px) scale(1.01);
}

.project-visual{
    position:absolute;
    inset:0;
    display:grid;
    place-items:center;
    font-size:120px;
    opacity:.14;
    background:
        radial-gradient(circle at 50% 30%,rgba(139,124,255,.28),transparent 55%);
}

.project-ui{
    position:absolute;
    width:68%;
    height:55%;
    top:11%;
    left:16%;
    border:1px solid rgba(255,255,255,.12);
    border-radius:13px;
    background:rgba(255,255,255,.035);
    box-shadow:0 25px 70px rgba(0,0,0,.4);
    transform:perspective(900px) rotateX(8deg);
    padding:12px;
}

.project-ui div{
    height:7px;
    border-radius:10px;
    background:rgba(255,255,255,.1);
    margin-bottom:8px;
}

.project-ui div:nth-child(1){width:35%}
.project-ui div:nth-child(2){width:85%;height:40px}
.project-ui div:nth-child(3){width:70%}
.project-ui div:nth-child(4){width:55%}

.project-info{
    position:absolute;
    left:29px;
    right:29px;
    bottom:26px;
    z-index:2;
}

.project-tag{
    color:#aaa2ff;
    font-size:9px;
    letter-spacing:2px;
    font-weight:700;
}

.project-info h3{
    font-family:"Space Grotesk";
    font-size:30px;
    margin:6px 0;
}

.project-info p{
    color:var(--muted);
    font-size:12px;
}

/* PROCESS */

.process{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:15px;
}

.process-card{
    padding:29px;
    border:1px solid var(--line);
    border-radius:22px;
    background:var(--surface);
    transition:.35s;
}

.process-card:hover{
    transform:translateY(-6px);
}

.process-number{
    color:#666;
    font-size:10px;
    margin-bottom:50px;
}

.process-card h3{
    font-family:"Space Grotesk";
    margin-bottom:9px;
}

.process-card p{
    color:var(--muted);
    font-size:13px;
    line-height:1.7;
}

/* PRICING */

.pricing{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:17px;
}

.price-card{
    position:relative;
    border:1px solid var(--line);
    border-radius:25px;
    background:var(--surface);
    padding:33px;
}

.price-card.featured{
    border-color:var(--accent);
    box-shadow:0 0 90px rgba(139,124,255,.12);
}

.popular{
    position:absolute;
    top:19px;
    right:19px;
    background:var(--accent);
    border-radius:50px;
    padding:6px 10px;
    font-size:8px;
    font-weight:800;
}

.price{
    font-family:"Space Grotesk";
    font-size:44px;
    font-weight:700;
    margin:20px 0;
}

.price-card p{
    color:var(--muted);
    font-size:13px;
}

.features{
    list-style:none;
    margin:25px 0;
}

.features li{
    color:var(--muted);
    font-size:13px;
    margin:12px 0;
}

/* CALCULATOR */

.calculator{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:18px;
    align-items:stretch;
}

.calc-box{
    border:1px solid var(--line);
    border-radius:25px;
    background:var(--surface);
    padding:32px;
}

.calc-option{
    display:flex;
    justify-content:space-between;
    align-items:center;
    border:1px solid var(--line);
    padding:16px;
    border-radius:13px;
    margin-bottom:10px;
}

.calc-option label{
    color:var(--muted);
    font-size:13px;
}

.calc-option input{
    accent-color:var(--accent);
    width:18px;
    height:18px;
}

.total{
    display:flex;
    justify-content:space-between;
    align-items:end;
    margin-top:30px;
}

.total span{
    color:var(--muted);
    font-size:12px;
}

.total strong{
    font-family:"Space Grotesk";
    font-size:48px;
}

/* STATS */

.stats{
    background:var(--surface);
    border-top:1px solid var(--line);
    border-bottom:1px solid var(--line);
}

.stats-grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:20px;
    text-align:center;
}

.stat strong{
    font-family:"Space Grotesk";
    font-size:50px;
    letter-spacing:-3px;
}

.stat span{
    display:block;
    color:var(--muted);
    font-size:11px;
}

/* FAQ */

.faq{
    max-width:850px;
    margin:auto;
}

details{
    background:var(--surface);
    border:1px solid var(--line);
    border-radius:16px;
    padding:21px 24px;
    margin-bottom:10px;
}

summary{
    cursor:pointer;
    font-weight:700;
    font-size:14px;
}

details p{
    color:var(--muted);
    font-size:13px;
    line-height:1.7;
    padding-top:14px;
}

/* CTA */

.cta{
    border:1px solid var(--line);
    border-radius:30px;
    padding:95px 25px;
    text-align:center;
    background:
        radial-gradient(circle at 50% 0%,rgba(139,124,255,.25),transparent 50%),
        var(--surface);
}

.cta h2{
    font-family:"Space Grotesk";
    font-size:clamp(43px,6vw,75px);
    line-height:.95;
    letter-spacing:-4px;
    margin-bottom:20px;
}

.cta p{
    color:var(--muted);
    max-width:600px;
    margin:0 auto 30px;
    line-height:1.7;
}

/* CONTACT */

.contact-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:50px;
    align-items:center;
}

.contact h2{
    font-family:"Space Grotesk";
    font-size:57px;
    line-height:.98;
    letter-spacing:-3.5px;
    margin-bottom:20px;
}

.contact-description{
    color:var(--muted);
    max-width:520px;
    line-height:1.7;
}

.email{
    display:inline-block;
    margin-top:24px;
    color:#aaa1ff;
    font-weight:700;
}

.form{
    border:1px solid var(--line);
    background:var(--surface);
    border-radius:25px;
    padding:30px;
}

.field{
    margin-bottom:14px;
}

.field label{
    display:block;
    color:var(--muted);
    font-size:10px;
    text-transform:uppercase;
    letter-spacing:1px;
    margin-bottom:7px;
}

.field input,
.field textarea,
.field select{
    width:100%;
    padding:14px;
    color:var(--text);
    background:rgba(255,255,255,.03);
    border:1px solid var(--line);
    border-radius:11px;
    outline:none;
}

.field textarea{
    min-height:125px;
    resize:vertical;
}

.field input:focus,
.field textarea:focus,
.field select:focus{
    border-color:var(--accent);
}

.form .btn{
    width:100%;
    border:0;
}

/* FOOTER */

footer{
    border-top:1px solid var(--line);
    padding:35px 0;
}

.footer{
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.footer p{
    color:var(--muted);
    font-size:11px;
}

/* REVEAL */

.reveal{
    opacity:0;
    transform:translateY(35px);
    transition:opacity .8s ease,transform .8s ease;
}

.reveal.visible{
    opacity:1;
    transform:none;
}

/* CURSOR */

.cursor{
    position:fixed;
    width:18px;
    height:18px;
    border:1px solid rgba(255,255,255,.7);
    border-radius:50%;
    pointer-events:none;
    z-index:999999;
    transform:translate(-50%,-50%);
    transition:width .2s,height .2s;
    mix-blend-mode:difference;
}

.cursor.big{
    width:45px;
    height:45px;
}

/* ANIMATIONS */

@keyframes rise{
    from{
        opacity:0;
        transform:translateY(25px);
    }
    to{
        opacity:1;
        transform:none;
    }
}

@keyframes float{
    0%,100%{transform:rotate(4deg) translateY(0)}
    50%{transform:rotate(2deg) translateY(-14px)}
}

@keyframes marquee{
    from{transform:translateX(0)}
    to{transform:translateX(-50%)}
}

/* MOBILE */

@media(max-width:950px){

    nav{
        display:none;
    }

    .menu{
        display:block;
    }

    nav.open{
        display:flex;
        position:absolute;
        top:75px;
        left:4%;
        right:4%;
        flex-direction:column;
        padding:25px;
        background:var(--surface);
        border:1px solid var(--line);
        border-radius:20px;
    }

    .floating-card{
        display:none;
    }

    .services,
    .pricing{
        grid-template-columns:1fr;
    }

    .process{
        grid-template-columns:1fr 1fr;
    }

    .calculator,
    .contact-grid{
        grid-template-columns:1fr;
    }

    .stats-grid{
        grid-template-columns:1fr 1fr;
    }

    .projects{
        grid-template-columns:1fr;
    }

    .project:nth-child(n){
        grid-column:span 1;
    }

    .cursor{
        display:none;
    }
}

@media(max-width:600px){

    section{
        padding:85px 0;
    }

    .hero h1{
        letter-spacing:-4px;
    }

    .hero-meta{
        flex-wrap:wrap;
        gap:22px;
    }

    .process{
        grid-template-columns:1fr;
    }

    .contact h2{
        font-size:43px;
    }

    .footer{
        flex-direction:column;
        gap:14px;
        text-align:center;
    }
}
</style>
</head>

<body>

<div id="progress"></div>
<div class="cursor" id="cursor"></div>

<header id="header">
<div class="container nav">

<a href="#" class="logo">Web<span>Studio</span></a>

<nav id="nav">
<a href="#usluge">Usluge</a>
<a href="#radovi">Radovi</a>
<a href="#proces">Proces</a>
<a href="#cene">Cene</a>
<a href="#faq">FAQ</a>
<a href="#kontakt">Kontakt</a>
</nav>

<div class="nav-actions">
<button class="round" id="theme">☼</button>
<button class="round" id="language">EN</button>
<button class="round menu" id="menu">☰</button>
</div>

</div>
</header>


<section class="hero">

<div class="grid"></div>
<div class="orb orb1"></div>
<div class="orb orb2"></div>

<div class="container hero-content">

<div class="available">
<span class="status"></span>
Otvoreni za nove projekte
</div>

<h1>
Web koji izgleda
<br>
<span><em>skuplje nego što košta.</em></span>
</h1>

<p class="hero-copy">
Pravimo moderne i profesionalne web sajtove za restorane,
apartmane, salone, brendove i male biznise — sa fokusom na
izgled, brzinu i jednostavno iskustvo za korisnika.
</p>

<div class="actions">
<a href="#kontakt" class="btn btn-main">Započni projekat →</a>
<a href="#radovi" class="btn btn-outline">Pogledaj portfolio</a>
</div>

<div class="hero-meta">
<div>
<strong>100%</strong>
<span>Responsive</span>
</div>
<div>
<strong>24/7</strong>
<span>Online prisustvo</span>
</div>
<div>
<strong>1:1</strong>
<span>Prilagođeno biznisu</span>
</div>
</div>

</div>


<div class="floating-card">
<div class="mini-screen"></div>
<div class="floating-bottom">
<strong>Digital Experience</strong>
<span>WebStudio</span>
</div>
</div>

</section>


<div class="ticker">
<div class="ticker-track">
<span>WEB DESIGN</span><b>✦</b>
<span>MODERN UI</span><b>✦</b>
<span>RESPONSIVE</span><b>✦</b>
<span>BRANDING</span><b>✦</b>
<span>FAST WEBSITES</span><b>✦</b>
<span>WEB DESIGN</span><b>✦</b>
<span>MODERN UI</span><b>✦</b>
<span>RESPONSIVE</span><b>✦</b>
<span>BRANDING</span><b>✦</b>
<span>FAST WEBSITES</span><b>✦</b>
</div>
</div>


<section id="usluge">

<div class="container">

<div class="section-head reveal">
<div class="kicker">01 / Usluge</div>
<h2>Ne pravimo samo sajt. Pravimo utisak.</h2>
<p>
Svaki element ima svoju svrhu — od prvog pogleda do trenutka
kada posetilac odluči da vas kontaktira.
</p>
</div>

<div class="services">

<div class="service reveal">
<div class="service-icon">✦</div>
<h3>Premium dizajn</h3>
<p>
Pažljivo odabrana tipografija, boje, spacing i vizuelna hijerarhija
za ozbiljan i moderan izgled.
</p>
</div>

<div class="service reveal">
<div class="service-icon">⌁</div>
<h3>Responsive</h3>
<p>
Sajt se automatski prilagođava telefonu, tabletu, laptopu i velikom ekranu.
</p>
</div>

<div class="service reveal">
<div class="service-icon">⚡</div>
<h3>Brzina</h3>
<p>
Optimizovana struktura bez nepotrebnog opterećenja za bolje korisničko iskustvo.
</p>
</div>

<div class="service reveal">
<div class="service-icon">▣</div>
<h3>Galerija</h3>
<p>
Atraktivno predstavljanje proizvoda, apartmana, hrane, prostora ili radova.
</p>
</div>

<div class="service reveal">
<div class="service-icon">◎</div>
<h3>Kontakt</h3>
<p>
Jasni CTA elementi, 
