# -ucjasmolak
festiwaL tańca2026
<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Festiwal Tańca 2026</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Segoe UI',sans-serif;
}

body{
    background:linear-gradient(-45deg,#ff4fd8,#6a5cff,#00d4ff,#00ff95);
    background-size:400% 400%;
    animation:bg 12s ease infinite;
    color:white;
    min-height:100vh;
}

@keyframes bg{
    0%{background-position:0% 50%;}
    50%{background-position:100% 50%;}
    100%{background-position:0% 50%;}
}

header{
    text-align:center;
    padding:60px 20px;
}

h1{
    font-size:4rem;
    text-shadow:0 0 20px rgba(255,255,255,.5);
}

.subtitle{
    font-size:1.4rem;
    margin-top:10px;
}

.countdown{
    display:flex;
    justify-content:center;
    gap:20px;
    flex-wrap:wrap;
    margin:40px auto;
}

.box{
    background:rgba(255,255,255,.15);
    backdrop-filter:blur(10px);
    padding:20px;
    border-radius:20px;
    min-width:120px;
    text-align:center;
}

.box span{
    font-size:2.5rem;
    font-weight:bold;
    display:block;
}

.section{
    max-width:1000px;
    margin:auto;
    padding:30px;
}

.card{
    background:rgba(255,255,255,.12);
    backdrop-filter:blur(12px);
    border-radius:25px;
    padding:30px;
    text-align:center;
    box-shadow:0 10px 30px rgba(0,0,0,.2);
}

.card h2{
    margin-bottom:15px;
}

.card p{
    line-height:1.8;
}

.btn{
    display:inline-block;
    margin-top:25px;
    padding:15px 35px;
    border-radius:50px;
    background:#fff;
    color:#333;
    text-decoration:none;
    font-weight:bold;
    transition:.3s;
}

.btn:hover{
    transform:scale(1.08);
}

.schedule{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
    gap:20px;
    margin-top:30px;
}

.event{
    background:rgba(255,255,255,.15);
    padding:20px;
    border-radius:20px;
    text-align:center;
}

footer{
    text-align:center;
    padding:40px;
}

.dance{
    font-size:4rem;
    animation:bounce 1.5s infinite;
    text-align:center;
    margin-bottom:20px;
}

@keyframes bounce{
    50%{transform:translateY(-15px);}
}
</style>
</head>
<body>

<header>
    <h1>💃 FESTIWAL TAŃCA 2026 🕺</h1>
    <p class="subtitle">Najbardziej roztańczone wydarzenie roku!</p>
</header>

<div class="dance">🎉💃🎶🕺🎉</div>

<div class="countdown">
    <div class="box">
        <span id="days">0</span>
        Dni
    </div>

    <div class="box">
        <span id="hours">0</span>
        Godzin
    </div>

    <div class="box">
        <span id="minutes">0</span>
        Minut
    </div>

    <div class="box">
        <span id="seconds">0</span>
        Sekund
    </div>
</div>

<section class="section">
    <div class="card">
        <h2>O Festiwalu</h2>

        <p>
            Przygotuj się na niezapomniane emocje!
            Pokazy taneczne, konkursy, warsztaty,
            muzyka i świetna zabawa przez cały dzień.
            Spotkaj tancerzy z całego kraju i przeżyj
            wyjątkowe chwile na parkiecie.
        </p>

        <a class="btn"
           href="https://www.youtube.com/results?search_query=Baby+Justin+Bieber"
           target="_blank">
            ▶ Posłuchaj „Baby”
        </a>
    </div>

    <div class="schedule">
        <div class="event">
            <h3>🎵 10:00</h3>
            <p>Otwarcie Festiwalu</p>
        </div>

        <div class="event">
            <h3>💃 12:00</h3>
            <p>Pokazy Taneczne</p>
        </div>

        <div class="event">
            <h3>🏆 15:00</h3>
            <p>Konkurs Tańca</p>
        </div>

        <div class="event">
            <h3>🎉 19:00</h3>
            <p>Wielki Finał</p>
        </div>
    </div>
</section>

<footer>
    ✨ Do zobaczenia na parkiecie! ✨
</footer>

<script>
const festivalDate = new Date("August 1, 2026 10:00:00").getTime();

setInterval(() => {
    const now = new Date().getTime();
    const distance = festivalDate - now;

    const days = Math.floor(distance / (1000 * 60 * 60 * 24));
    const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    const seconds = Math.floor((distance % (1000 * 60)) / 1000);

    document.getElementById("days").innerHTML = days;
    document.getElementById("hours").innerHTML = hours;
    document.getElementById("minutes").innerHTML = minutes;
    document.getElementById("seconds").innerHTML = seconds;
}, 1000);
</script>

</body>
</html>
