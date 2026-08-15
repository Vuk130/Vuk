<!DOCTYPE html>
<html lang="sr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>WebStudio | Izrada modernih sajtova</title>

<style>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Arial, sans-serif;
    background: #080c18;
    color: white;
    line-height: 1.6;
}

header {
    position: sticky;
    top: 0;
    z-index: 100;
    padding: 18px 7%;
    background: rgba(8,12,24,0.95);
    border-bottom: 1px solid #252d45;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    font-size: 25px;
    font-weight: bold;
}

.logo span {
    color: #5b8cff;
}

nav a {
    color: white;
    text-decoration: none;
    margin-left: 22px;
}

nav a:hover {
    color: #5b8cff;
}

.hero {
    min-height: 650px;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 80px 20px;
    background: radial-gradient(circle at top, #18254a, #080c18 60%);
}

.hero-content {
    max-width: 850px;
}

.hero h1 {
    font-size: 58px;
    line-height: 1.1;
    margin-bottom: 25px;
}

.hero h1 span {
    color: #5b8cff;
}

.hero p {
    color: #b8c0d4;
    font-size: 20px;
    max-width: 700px;
    margin: auto;
}

.button {
    display: inline-block;
    margin-top: 30px;
    padding: 15px 30px;
    background: #5b8cff;
    color: white;
    text-decoration: none;
    border-radius: 10px;
    font-weight: bold;
    transition: 0.3s;
}

.button:hover {
    transform: translateY(-3px);
    background: #416fd9;
}

.section {
    padding: 85px 7%;
    text-align: center;
}

.section h2 {
    font-size: 38px;
    margin-bottom: 15px;
}

.section-intro {
    color: #aeb7cc;
    max-width: 650px;
    margin: 0 auto 45px;
}

.cards {
    display: flex;
    justify-content: center;
    gap: 25px;
    flex-wrap: wrap;
}

.card {
    background: #131a2d;
    border: 1px solid #29334f;
    border-radius: 18px;
    padding: 32px;
    width: 300px;
    transition: 0.3s;
}

.card:hover {
    transform: translateY(-8px);
    border-color: #5b8cff;
}

.icon {
    font-size: 40px;
    margin-bottom: 15px;
}

.card h3 {
    font-size: 21px;
    margin-bottom: 12px;
}

.card p {
    color: #b8c0d4;
}

.steps {
    max-width: 850px;
    margin: auto;
}

.step {
    display: flex;
    align-items: center;
    gap: 20px;
    text-align: left;
    margin-bottom: 25px;
    background: #131a2d;
    padding: 25px;
    border-radius: 15px;
    border: 1px solid #29334f;
}

.number {
    min-width: 50px;
    height: 50px;
    border-radius: 50%;
    background: #5b8cff;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
}

.step p {
    color: #b8c0d4;
}

.pricing {
    background: #0d1324;
}

.price {
    font-size: 30px;
    color: #5b8cff;
    font-weight: bold;
    margin: 20px 0;
}

.card ul {
    list-style: none;
    text-align: left;
    color: #c1c9da;
}

.card li {
    margin: 9px 0;
}

.portfolio-card {
    width: 330px;
    min-height: 190px;
    background: linear-gradient(135deg, #18254a, #11182c);
    border-radius: 18px;
    padding: 35px 25px;
    border: 1px solid #29334f;
}

.portfolio-card h3 {
    margin-bottom: 12px;
}

.portfolio-card p {
    color: #b8c0d4;
}

.faq {
    max-width: 800px;
    margin: auto;
    text-align: left;
}

.faq-item {
    background: #131a2d;
    border: 1px solid #29334f;
    border-radius: 12px;
    padding: 22px;
    margin-bottom: 15px;
}

.faq-item h3 {
    margin-bottom: 8px;
}

.faq-item p {
    color: #b8c0d4;
}

.contact {
    background: linear-gradient(135deg, #111a34, #0b1020);
}

.contact-box {
    max-width: 700px;
    margin: auto;
}

.contact-box p {
    color: #b8c0d4;
    font-size: 18px;
}

footer {
    text-align: center;
    padding: 30px;
    color: #8993aa;
    border-top: 1px solid #252d45;
}

@media (max-width: 700px) {

    header {
        justify-content: center;
    }

    nav {
        display: none;
    }

    .hero {
        min-height: 570px;
    }

    .hero h1 {
        font-size: 40px;
    }

    .hero p {
        font-size: 17px;
    }

    .section {
        padding: 65px 20px;
    }

    .section h2 {
        font-size: 30px;
    }

    .step {
        align-items: flex-start;
    }
}

</style>
</head>

<body>

<header>

    <div class="logo">
        Web<span>Studio</span>
    </div>

    <nav>
        <a href="#usluge">Usluge</a>
        <a href="#proces">Proces</a>
        <a href="#cene">Cene</a>
        <a href="#portfolio">Primeri</a>
        <a href="#kontakt">Kontakt</a>
    </nav>

</header>


<section class="hero">

    <div class="hero-content">

        <h1>
            Vaš biznis zaslužuje
            <span>moderan sajt.</span>
        </h1>

        <p>
            Izrađujemo moderne, brze i profesionalne web sajtove
            prilagođene vašem biznisu i vašim klijentima.
        </p>

        <a
            class="button"
            href="mailto:vuk.markovic3001@gmail.com?subject=Upit%20za%20izradu%20sajta">
            Zatražite sajt
        </a>

    </div>

</section>


<section class="section" id="usluge">

    <h2>Šta nudimo?</h2>

    <p class="section-intro">
        Sve što je potrebno da vaš biznis izgleda profesionalno
        i bude dostupan vašim klijentima online.
    </p>

    <div class="cards">

        <div class="card">
            <div class="icon">💻</div>
            <h3>Moderan dizajn</h3>
            <p>
                Profesionalan izgled prilagođen vašem brendu.
            </p>
        </div>

        <div class="card">
            <div class="icon">📱</div>
            <h3>Mobilni dizajn</h3>
            <p>
                Sajt koji odlično izgleda na telefonu,
                tabletu i računaru.
            </p>
        </div>

        <div class="card">
            <div class="icon">⚡</div>
            <h3>Brzo učitavanje</h3>
            <p>
                Jednostavan i optimizovan sajt koji se brzo učitava.
            </p>
        </div>

    </div>

</section>


<section class="section" id="proces">

    <h2>Kako funkcioniše?</h2>

    <p class="section-intro">
        Jednostavan proces od dogovora do gotovog sajta.
    </p>

    <div class="steps">

        <div class="step">
            <div class="number">1</div>
            <div>
                <h3>Dogovor</h3>
                <p>
                    Razgovaramo o vašem biznisu, potrebama i izgledu sajta.
                </p>
            </div>
        </div>

        <div class="step">
            <div class="number">2</div>
            <div>
                <h3>Izrada</h3>
                <p>
                    Izrađujemo dizajn i funkcije prema dogovoru.
                </p>
            </div>
        </div>

        <div class="step">
            <div class="number">3</div>
            <div>
                <h3>Objavljivanje</h3>
                <p>
                    Nakon odobrenja, sajt se priprema za objavljivanje.
                </p>
            </div>
        </div>

    </div>

</section>


<section class="section pricing" id="cene">

    <h2>Paketi</h2>

    <p class="section-intro">
        Izaberite paket koji odgovara vašim potrebama.
    </p>

    <div class="cards">

        <div class="card">

            <h3>Starter</h3>

            <p>
                Za male biznise kojima treba jednostavan online nastup.
            </p>

            <div class="price">50 €</div>

            <ul>
                <li>✓ Jedna stranica</li>
                <li>✓ Moderan dizajn</li>
                <li>✓ Mobilna verzija</li>
                <li>✓ Kontakt dugme</li>
            </ul>

            <a
                class="button"
                href="mailto:vuk.markovic3001@gmail.com?subject=Starter%20paket">
                Izaberite paket
            </a>

        </div>


        <div class="card">

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

            <a
                class="button"
                href="mailto:vuk.markovic3001@gmail.com?subject=Business%20paket">
                Izaberite paket
            </a>

        </div>


        <div class="card">

            <h3>Premium</h3>

            <p>
                Za one kojima treba napredniji i detaljniji sajt.
            </p>

            <div class="price">200 €</div>

            <ul>
                <li>✓ Napredniji dizajn</li>
                <li>✓ Više stranica</li>
                <li>✓ Galerija</li>
                <li>✓ Animacije</li>
                <li>✓ Dodatne funkcije</li>
            </ul>

            <a
                class="button"
                href="mailto:vuk.markovic3001@gmail.com?subject=Premium%20paket">
                Izaberite paket
            </a>

        </div>

    </div>

</section>


<section class="section" id="portfolio">

    <h2>Primeri dizajna</h2>

    <p class="section-intro">
        Primeri tipova sajtova koje možemo napraviti.
    </p>

    <div class="cards">

        <div class="portfolio-card">
            <h3>🍕 Restoran</h3>
            <p>
                Meni, galerija, lokacija, radno vreme i kontakt.
            </p>
        </div>

        <div class="portfolio-card">
            <h3>💈 Salon</h3>
            <p>
                Usluge, cenovnik, galerija, informacije i kontakt.
            </p>
        </div>

        <div class="portfolio-card">
            <h3>🏢 Biznis</h3>
            <p>
                Profesionalna prezentacija kompanije i usluga.
            </p>
        </div>

    </div>

</section>


<section class="section">

    <h2>Zašto sajt?</h2>

    <div class="cards">

        <div class="card">
            <div class="icon">🌐</div>
            <h3>Online prisustvo</h3>
            <p>
                Vaši klijenti mogu lako da pronađu informacije o vama.
            </p>
        </div>

        <div class="card">
            <div class="icon">⭐</div>
            <h3>Profesionalni izgled</h3>
            <p>
                Dobar sajt ostavlja profesionalan prvi utisak.
            </p>
        </div>

        <div class="card">
            <div class="icon">📞</div>
            <h3>Lak kontakt</h3>
            <p>
                Klijenti mogu brzo da vas kontaktiraju.
            </p>
        </div>

    </div>

</section>


<section class="section">

    <h2>Česta pitanja</h2>

    <div class="faq">

        <div class="faq-item">
            <h3>Koliko traje izrada?</h3>
            <p>
                Jednostavan sajt može biti završen za oko 3 dana,
                u zavisnosti od zahteva.
            </p>
        </div>

        <div class="faq-item">
            <h3>Da li sajt radi na telefonu?</h3>
            <p>
                Da. Dizajn je prilagođen telefonu, tabletu i računaru.
            </p>
        </div>

        <div class="faq-item">
            <h3>Da li mogu da tražim izmene?</h3>
            <p>
                Da. Izgled i sadržaj se dogovaraju pre završetka sajta.
            </p>
        </div>

        <div class="faq-item">
            <h3>Kako da vas kontaktiram?</h3>
            <p>
                Kliknite na bilo koje kontakt dugme i pošaljite upit emailom.
            </p>
        </div>

    </div>

</section>


<section class="section contact" id="kontakt">

    <div class="contact-box">

        <h2>Zainteresovani za sajt?</h2>

        <p>
            Pošaljite upit i dogovorićemo se oko izgleda,
            sadržaja, cene i vremena izrade.
        </p>

        <a
            class="button"
            href="mailto:vuk.markovic3001@gmail.com?subject=Želim%20da%20napravim%20sajt">
            ✉️ Pošaljite upit
        </a>

    </div>

</section>


<footer>

    © 2026 WebStudio — Izrada web sajtova

</footer>

</body>
</html>
