<!DOCTYPE html>
<html lang="sr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>WebStudio - Izrada sajtova</title>

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
    background: #0b1020;
    color: white;
    line-height: 1.6;
}

header {
    padding: 20px 7%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid #252d45;
    background: #0b1020;
}

.logo {
    font-size: 25px;
    font-weight: bold;
}

nav a {
    color: white;
    text-decoration: none;
    margin-left: 20px;
}

nav a:hover {
    color: #5b8cff;
}

.hero {
    text-align: center;
    padding: 100px 20px;
}

.hero h1 {
    font-size: 52px;
    margin-bottom: 20px;
}

.hero h1 span {
    color: #5b8cff;
}

.hero p {
    max-width: 650px;
    margin: auto;
    color: #b8c0d4;
    font-size: 19px;
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
}

.button:hover {
    background: #416fd9;
}

.section {
    padding: 70px 7%;
    text-align: center;
}

.section h2 {
    font-size: 35px;
    margin-bottom: 40px;
}

.cards {
    display: flex;
    justify-content: center;
    gap: 25px;
    flex-wrap: wrap;
}

.card {
    background: #151c32;
    border: 1px solid #29334f;
    border-radius: 18px;
    width: 290px;
    padding: 30px;
    transition: 0.3s;
}

.card:hover {
    transform: translateY(-7px);
}

.card h3 {
    font-size: 21px;
    margin-bottom: 12px;
}

.card p {
    color: #b8c0d4;
}

.price {
    margin-top: 18px;
    font-size: 25px;
    color: #5b8cff;
    font-weight: bold;
}

.contact {
    background: #11182c;
}

.contact p {
    color: #b8c0d4;
}

footer {
    text-align: center;
    padding: 25px;
    color: #8f98ad;
    border-top: 1px solid #252d45;
}

@media (max-width: 650px) {

    header {
        justify-content: center;
    }

    nav {
        display: none;
    }

    .hero {
        padding: 75px 20px;
    }

    .hero h1 {
        font-size: 38px;
    }

    .section {
        padding: 55px 20px;
    }
}
</style>
</head>

<body>

<header>

    <div class="logo">
        WebStudio
    </div>

    <nav>
        <a href="#usluge">Usluge</a>
        <a href="#cene">Cene</a>
        <a href="#kontakt">Kontakt</a>
    </nav>

</header>

<section class="hero">

    <h1>
        Moderan sajt za <span>vaš biznis.</span>
    </h1>

    <p>
        Izrađujemo moderne, brze i profesionalne web sajtove
        za restorane, salone, prodavnice i male biznise.
    </p>

    <a href="#kontakt" class="button">
        Zatražite sajt
    </a>

</section>

<section class="section" id="usluge">

    <h2>Naše usluge</h2>

    <div class="cards">

        <div class="card">
            <h3>💻 Izrada sajta</h3>
            <p>
                Moderan sajt prilagođen vašem poslu,
                brendu i potrebama.
            </p>
        </div>

        <div class="card">
            <h3>📱 Mobilni dizajn</h3>
            <p>
                Sajt koji izgleda odlično na telefonu,
                tabletu i računaru.
            </p>
        </div>

        <div class="card">
            <h3>⚡ Brz sajt</h3>
            <p>
                Jednostavan i brz sajt koji se brzo učitava.
            </p>
        </div>

    </div>

</section>

<section class="section" id="cene">

    <h2>Paketi</h2>

    <div class="cards">

        <div class="card">
            <h3>Starter</h3>
            <p>
                Jednostavan sajt za mali biznis.
            </p>
            <div class="price">
                od 50 €
            </div>
        </div>

        <div class="card">
            <h3>Business</h3>
            <p>
                Kompletan sajt sa više sekcija
                i profesionalnim dizajnom.
            </p>
            <div class="price">
                od 100 €
            </div>
        </div>

        <div class="card">
            <h3>Premium</h3>
            <p>
                Napredniji dizajn i dodatne funkcije
                po dogovoru.
            </p>
            <div class="price">
                od 200 €
            </div>
        </div>

    </div>

</section>

<section class="section contact" id="kontakt">

    <h2>Želite svoj sajt?</h2>

    <p>
        Kontaktirajte nas i napravite prvi korak
        ka boljem online prisustvu.
    </p>

    <a href="mailto:vuk.markovic3001@gmail.com?subject=Želim%20da%20napravim%20sajt" class="button">
    Zatražite sajt
</a>


</section>

<footer>

    © 2026 WebStudio - Izrada web sajtova

</footer>

</body>
</html>
