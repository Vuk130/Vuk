<!DOCTYPE html>
<html lang="sr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>WebStudio | Moderni web sajtovi</title>
<meta name="description" content="Izrada modernih, brzih i profesionalnih web sajtova za biznise i brendove.">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:Arial,Helvetica,sans-serif;
    background:#070b16;
    color:#fff;
    line-height:1.6;
    overflow-x:hidden;
}

a{
    color:inherit;
    text-decoration:none;
}

.container{
    width:min(1150px,92%);
    margin:auto;
}

header{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    z-index:1000;
    padding:18px 0;
    background:rgba(7,11,22,.82);
    backdrop-filter:blur(15px);
    border-bottom:1px solid rgba(255,255,255,.08);
}

.nav{
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.logo{
    font-size:25px;
    font-weight:800;
    letter-spacing:-1px;
}

.logo span{
    color:#6d8cff;
}

nav{
    display:flex;
    gap:25px;
}

nav a{
    color:#bfc7dc;
    font-size:14px;
    transition:.3s;
}

nav a:hover{
    color:#fff;
}

.hero{
    min-height:100vh;
    display:flex;
    align-items:center;
    position:relative;
    overflow:hidden;
    background:
    radial-gradient(circle at 20% 20%,rgba(82,111,255,.28),transparent 35%),
    radial-gradient(circle at 80% 60%,rgba(130,60,255,.18),transparent 30%),
    #070b16;
}

.hero:before{
    content:"";
    position:absolute;
    width:500px;
    height:500px;
    border:1px solid rgba(255,255,255,.05);
    border-radius:50%;
    right:-180px;
    top:100px;
}

.hero-content{
    max-width:850px;
    padding-top:70px;
    animation:fadeUp 1s ease;
}

.badge{
    display:inline-block;
    padding:8px 14px;
    border:1px solid rgba(109,140,255,.4);
    background:rgba(109,140,255,.08);
    border-radius:50px;
    color:#9db1ff;
    font-size:13px;
    margin-bottom:22px;
}

.hero h1{
    font-size:clamp(44px,7vw,78px);
    line-height:1.02;
    letter-spacing:-3px;
    margin-bottom:25px;
}

.gradient{
    background:linear-gradient(90deg,#6d8cff,#a77bff);
    -webkit-background-clip:text;
    color:transparent;
}

.hero p{
    max-width:690px;
    color:#aeb7cb;
    font-size:19px;
    margin-bottom:32px;
}

.buttons{
    display:flex;
    gap:14px;
    flex-wrap:wrap;
}

.btn{
    padding:15px 23px;
    border-radius:11px;
    font-weight:700;
    transition:.3s;
    display:inline-block;
}

.btn-primary{
    background:#6d8cff;
}

.btn-primary:hover{
    transform:translateY(-3px);
}

.btn-secondary{
    border:1px solid #303a56;
    background:#11182b;
}

.btn-secondary:hover{
    background:#19223b;
}

section{
    padding:100px 0;
}

.section-title{
    text-align:center;
    max-width:700px;
    margin:0 auto 55px;
}

.section-title h2{
    font-size:42px;
    margin-bottom:12px;
}

.section-title p{
    color:#9ea8bd;
}

.grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:22px;
}

.card{
    background:linear-gradient(145deg,#11182a,#0c1220);
    border:1px solid #222d47;
    border-radius:20px;
    padding:30px;
    transition:.35s;
}

.card:hover{
    transform:translateY(-8px);
    border-color:#596fc2;
}

.icon{
    width:54px;
    height:54px;
    display:flex;
    align-items:center;
    justify-content:center;
    border-radius:15px;
    background:#182342;
    font-size:25px;
    margin-bottom:20px;
}

.card h3{
    font-size:21px;
    margin-bottom:10px;
}

.card p{
    color:#9da7bb;
}

.dark{
    background:#0b101d;
}

.pricing .card{
    position:relative;
}

.price{
    font-size:38px;
    font-weight:800;
    margin:18px 0;
    color:#7f9aff;
}

.card ul{
    list-style:none;
    color:#b5bfd2;
    margin:20px 0;
}

.card li{
    margin:10px 0;
}

.featured{
    border:1px solid #6d8cff;
    transform:scale(1.03);
}

.featured:hover{
    transform:scale(1.03) translateY(-8px);
}

.popular{
    position:absolute;
    top:18px;
    right:18px;
    font-size:11px;
    background:#6d8cff;
    padding:5px 9px;
    border-radius:20px;
}

.portfolio{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:22px;
}

.project{
    min-height:240px;
    border-radius:20px;
    padding:30px;
    display:flex;
    flex-direction:column;
    justify-content:flex-end;
    border:1px solid #29334d;
    overflow:hidden;
    position:relative;
    background:linear-gradient(135deg,#172347,#10182b);
}

.project:before{
    content:"";
    position:absolute;
    inset:0;
    background:linear-gradient(transparent,rgba(0,0,0,.65));
}

.project-content{
    position:relative;
    z-index:2;
}

.project h3{
    font-size:24px;
}

.project p{
    color:#b9c2d5;
}

.steps{
    max-width:850px;
    margin:auto;
}

.step{
    display:flex;
    gap:20px;
    padding:25px;
    margin-bottom:18px;
    background:#11182a;
    border:1px solid #222d47;
    border-radius:17px;
}

.step-number{
    min-width:48px;
    height:48px;
    border-radius:50%;
    display:flex;
    justify-content:center;
    align-items:center;
    background:#6d8cff;
    font-weight:800;
}

.step p{
    color:#9da7bb;
}

.faq{
    max-width:850px;
    margin:auto;
}

details{
    background:#11182a;
    border:1px solid #222d47;
    border-radius:14px;
    margin-bottom:14px;
    padding:20px;
}

summary{
    cursor:pointer;
    font-weight:700;
}

details p{
    color:#9da7bb;
    padding-top:14px;
}

.contact{
    background:
    radial-gradient(circle at 50% 0%,rgba(109,140,255,.2),transparent 45%),
    #0b101d;
    text-align:center;
}

.contact-box{
    max-width:750px;
    margin:auto;
}

.contact-box h2{
    font-size:45px;
    margin-bottom:15px;
}

.contact-box p{
    color:#aeb7cb;
    margin-bottom:30px;
}

.email{
    display:inline-block;
    margin-top:20px;
    color:#8da5ff;
    font-weight:700;
}

footer{
    padding:30px 0;
    border-top:1px solid #202a40;
    color:#7f899f;
    text-align:center;
    font-size:14px;
}

@keyframes fadeUp{
    from{
        opacity:0;
        transform:translateY(25px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

@media(max-width:800px){

    nav{
        display:none;
    }

    .grid,
    .portfolio{
        grid-template-columns:1fr;
    }

    .hero h1{
        letter-spacing:-2px;
    }

    .section-title h2{
        font-size:34px;
    }

    .featured{
        transform:none;
    }

    .featured:hover{
        transform:translateY(-8px);
    }

    .contact-box h2{
        font-size:34px;
    }
}
</style>
</head>

<body>

<header>
<div class="container nav">

<div class="logo">
Web<span>Studio</span>
</div>

<nav>
<a href="#usluge">Usluge</a>
<a href="#cene">Cene</a>
<a href="#rad">Primeri</a>
<a href="#proces">Proces</a>
<a href="#faq">FAQ</a>
<a href="#kontakt">Kontakt</a>
</nav>

</div>
</header>


<section class="hero">

<div class="container hero-content">

<div class="badge">
🚀 Moderni web sajtovi za biznise
</div>

<h1>
Vaš biznis.<br>
Vaš <span class="gradient">profesionalni sajt.</span>
</h1>

<p>
Izrađujemo moderne, brze i mobilno prilagođene web sajtove
koji vašem biznisu daju profesionalan online izgled.
</p>

<div class="buttons">

<a class="btn btn-primary"
href="mailto:vuk.markovic3001@gmail.com?subject=Upit%20za%20izradu%20sajta">
Zatražite sajt →
</a>

<a class="btn btn-secondary" href="#rad">
Pogledajte primere
</a>

</div>

</div>

</section>


<section id="usluge">

<div class="container">

<div class="section-title">
<h2>Sve što vašem sajtu treba</h2>
<p>
Od modernog dizajna do jednostavnog kontakta sa vašim klijentima.
</p>
</div>

<div class="grid">

<div class="card">
<div class="icon">🎨</div>
<h3>Moderan dizajn</h3>
<p>
Profesionalan izgled prilagođen vašem brendu, bojama i stilu.
</p>
</div>

<div class="card">
<div class="icon">📱</div>
<h3>100% prilagođen telefonu</h3>
<p>
Sajt izgleda dobro na telefonu, tabletu i računaru.
</p>
</div>

<div class="card">
<div class="icon">⚡</div>
<h3>Brzo učitavanje</h3>
<p>
Optimizovan dizajn bez nepotrebnog opterećenja.
</p>
</div>

<div class="card">
<div class="icon">🖼️</div>
<h3>Galerija</h3>
<p>
Prikažite proizvode, apartmane, restoran, radove ili usluge.
</p>
</div>

<div class="card">
<div class="icon">📍</div>
<h3>Lokacija</h3>
<p>
Jednostavno predstavljanje adrese i lokacije vašeg biznisa.
</p>
</div>

<div class="card">
<div class="icon">✉️</div>
<h3>Kontakt</h3>
<p>
Klijenti vas mogu brzo kontaktirati putem emaila ili telefona.
</p>
</div>

</div>
</div>

</section>


<section class="dark" id="cene">

<div class="container">

<div class="section-title">
<h2>Jednostavni paketi</h2>
<p>
Izaberite paket prema potrebama vašeg biznisa.
</p>
</div>

<div class="grid">

<div class="card">

<h3>Starter</h3>

<p>
Za male biznise kojima treba jednostavno online prisustvo.
</p>

<div class="price">50 €</div>

<ul>
<li>✓ Jedna stranica</li>
<li>✓ Moderan dizajn</li>
<li>✓ Mobilna verzija</li>
<li>✓ Kontakt dugme</li>
</ul>

<a class="btn btn-secondary"
href="mailto:vuk.markovic3001@gmail.com?subject=Starter%20paket">
Izaberite Starter
</a>

</div>


<div class="card featured">

<div class="popular">NAJPOPULARNIJI</div>

<h3>Business</h3>

<p>
Za biznise kojima treba kompletna prezentacija.
</p>

<div class="price">100 €</div>

<ul>
<li>✓ Više sekcija</li>
<li>✓ Galerija</li>
<li>✓ Mobilna verzija</li>
<li>✓ Kontakt</li>
<li>✓ Profesionalni dizajn</li>
</ul>

<a class="btn btn-primary"
href="mailto:vuk.markovic3001@gmail.com?subject=Business%20paket">
Izaberite Business
</a>

</div>


<div class="card">

<h3>Premium</h3>

<p>
Za detaljniji sajt sa naprednijim dizajnom.
</p>

<div class="price">200 €</div>

<ul>
<li>✓ Više stranica</li>
<li>✓ Napredniji dizajn</li>
<li>✓ Galerija</li>
<li>✓ Animacije</li>
<li>✓ Dodatne funkcije</li>
</ul>

<a class="btn btn-secondary"
href="mailto:vuk.markovic3001@gmail.com?subject=Premium%20paket">
Izaberite Premium
</a>

</div>

</div>
</div>

</section>


<section id="rad">

<div class="container">

<div class="section-title">
<h2>Primeri sajtova</h2>
<p>
Jedan dizajn može se prilagoditi različitim vrstama biznisa.
</p>
</div>

<div class="portfolio">

<div class="project">
<div class="project-content">
<h3>🏠 Apartmani</h3>
<p>Galerija, sobe, sadržaji, lokacija i kontakt.</p>
</div>
</div>

<div class="project">
<div class="project-content">
<h3>🍽️ Restoran</h3>
<p>Meni, galerija, radno vreme, lokacija i kontakt.</p>
</div>
</div>

<div class="project">
<div class="project-content">
<h3>👕 Brend</h3>
<p>Predstavljanje proizvoda i profesionalan online nastup.</p>
</div>
</div>

<div class="project">
<div class="project-content">
<h3>💈 Salon</h3>
<p>Usluge, cenovnik, galerija i kontakt.</p>
</div>
</div>

<div class="project">
<div class="project-content">
<h3>🚗 Auto detailing</h3>
<p>Usluge, slike radova, paketi i kontakt.</p>
</div>
</div>

<div class="project">
<div class="project-content">
<h3>💍 Handmade</h3>
<p>Galerija proizvoda, informacije i kontakt.</p>
</div>
</div>

</div>
</div>

</section>


<section class="dark" id="proces">

<div class="container">

<div class="section-title">
<h2>Kako radimo?</h2>
<p>
Jednostavan proces od prve poruke do gotovog sajta.
</p>
</div>

<div class="steps">

<div class="step">
<div class="step-number">1</div>
<div>
<h3>Dogovor</h3>
<p>
Razgovaramo o vašem biznisu, potrebama, sadržaju i izgledu.
</p>
</div>
</div>

<div class="step">
<div class="step-number">2</div>
<div>
<h3>Dizajn</h3>
<p>
Pravimo izgled sajta prilagođen vašem brendu.
</p>
</div>
</div>

<div class="step">
<div class="step-number">3</div>
<div>
<h3>Izrada</h3>
<p>
Sajt se izrađuje i prilagođava telefonu i računaru.
</p>
</div>
</div>

<div class="step">
<div class="step-number">4</div>
<div>
<h3>Objavljivanje</h3>
<p>
Nakon dogovora, sajt se postavlja online.
</p>
</div>
</div>

</div>
</div>

</section>


<section id="faq">

<div class="container">

<div class="section-title">
<h2>Česta pitanja</h2>
<p>
Odgovori na najčešća pitanja klijenata.
</p>
</div>

<div class="faq">

<details>
<summary>Koliko traje izrada sajta?</summary>
<p>
Jednostavniji sajt može biti završen za oko 3 dana,
u zavisnosti od zahteva i količine sadržaja.
</p>
</details>

<details>
<summary>Da li sajt radi na telefonu?</summary>
<p>
Da. Dizajn je prilagođen telefonu, tabletu i računaru.
</p>
</details>

<details>
<summary>Da li mogu da pošaljem svoje slike?</summary>
<p>
Da. Možete poslati fotografije, logo i druge materijale
koje želite da budu na sajtu.
</p>
</details>

<details>
<summary>Da li mogu da tražim izmene?</summary>
<p>
Da. Detalji i izmene se dogovaraju tokom izrade.
</p>
</details>

<details>
<summary>Da li mogu da imam svoj domen?</summary>
<p>
Da. Sajt se može povezati sa vašim sopstvenim domenom.
</p>
</details>

<details>
<summary>Kako da počnemo?</summary>
<p>
Pošaljite upit putem kontakt dugmeta i dogovorićemo detalje.
</p>
</details>

</div>
</div>

</section>


<section class="contact" id="kontakt">

<div class="container contact-box">

<h2>Spremni za novi sajt?</h2>

<p>
Pošaljite nam email i napišite nekoliko informacija
o vašem biznisu. Javićemo vam se i dogovoriti sve detalje.
</p>

<a class="btn btn-primary"
href="mailto:vuk.markovic3001@gmail.com?subject=Zainteresovan%20sam%20za%20izradu%20sajta&body=Zdravo,%0A%0AZainteresovan/a%20sam%20za%20izradu%20sajta.%0A%0ANaziv%20biznisa:%0ATip%20biznisa:%0AŠta%20želim%20na%20sajtu:%0A%0AHvala!">
✉️ Zatražite sajt
</a>

<br>

<a class="email"
href="mailto:vuk.markovic3001@gmail.com">
vuk.markovic3001@gmail.com
</a>

</div>

</section>


<footer>
<div class="container">
© 2026 WebStudio · Izrada modernih web sajtova
</div>
</footer>

</body>
</html>
