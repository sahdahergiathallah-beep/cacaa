```
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>For You 🖤</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600&family=Poppins:wght@300;400;500&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    min-height: 100vh;
    overflow: hidden;
    background: #050505;
    color: white;
    font-family: 'Poppins', sans-serif;
}

/* BACKGROUND */

.background {
    position: fixed;
    inset: 0;
    background:
        radial-gradient(
            circle at center,
            #350d15 0%,
            #120608 35%,
            #050505 75%
        );
    z-index: -2;
}

.glow {
    position: fixed;
    width: 250px;
    height: 250px;
    border-radius: 50%;
    background: #7b1428;
    filter: blur(120px);
    opacity: .2;
    z-index: -1;
}

.glow1 {
    top: -100px;
    left: -100px;
}

.glow2 {
    bottom: -120px;
    right: -100px;
}

/* STARS */

.star {
    position: fixed;
    width: 2px;
    height: 2px;
    background: white;
    border-radius: 50%;
    opacity: .4;
    animation: moveStar linear infinite;
}

@keyframes moveStar {

    from {
        transform: translateY(100vh);
        opacity: 0;
    }

    20% {
        opacity: .5;
    }

    to {
        transform: translateY(-10vh);
        opacity: 0;
    }

}

/* CONTAINER */

.container {
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 25px;
}

.page {
    display: none;
    width: 100%;
    max-width: 700px;
    text-align: center;
    animation: fadeIn .8s ease;
}

.page.active {
    display: block;
}

@keyframes fadeIn {

    from {
        opacity: 0;
        transform: translateY(25px);
        filter: blur(5px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
        filter: blur(0);
    }

}

/* TEXT */

.small-title {
    font-size: 11px;
    letter-spacing: 5px;
    text-transform: uppercase;
    color: #9f9294;
    margin-bottom: 25px;
}

h1,
h2 {
    font-family: 'Cormorant Garamond', serif;
}

h1 {
    font-size: clamp(60px, 15vw, 110px);
    font-weight: 500;
}

h2 {
    font-size: clamp(38px, 9vw, 65px);
    line-height: 1.05;
    font-weight: 500;
    margin-bottom: 25px;
}

.text {
    color: #b9b0b1;
    font-size: 14px;
    line-height: 2;
    max-width: 550px;
    margin: auto;
}

.message {
    font-family: 'Cormorant Garamond', serif;
    font-size: 25px;
    line-height: 1.55;
    color: #ded7d8;
}

.message p {
    margin-bottom: 14px;
}

.red {
    color: #b94156;
}

/* BUTTON */

button {
    border: 1px solid #512832;
    background: rgba(30, 8, 12, .75);
    color: white;
    padding: 14px 27px;
    border-radius: 50px;
    margin: 8px;
    cursor: pointer;
    font-family: 'Poppins', sans-serif;
    font-size: 13px;
    letter-spacing: 1px;
    transition: .3s;
}

button:hover {
    transform: translateY(-3px);
    border-color: #b94156;
    box-shadow: 0 0 30px rgba(185,65,86,.3);
}

.primary {
    background: #72172a;
    border-color: #a63247;
}

/* HEART */

.big-heart {
    font-size: 55px;
    color: #a82f45;
    animation: heartbeat 1.5s infinite;
    margin-bottom: 20px;
}

@keyframes heartbeat {

    50% {
        transform: scale(1.2);
    }

}

/* YES SCREEN */

#yesPage h2 {
    margin-bottom: 15px;
}

/* MOBILE */

@media(max-width: 500px) {

    .message {
        font-size: 21px;
    }

    .text {
        font-size: 13px;
    }

    button {
        padding: 13px 20px;
    }

}
</style>
</head>

<body>

<div class="background"></div>

<div class="glow glow1"></div>
<div class="glow glow2"></div>

<div id="stars"></div>


<div class="container">

<!-- ================= PAGE 1 ================= -->

<section class="page active" id="page1">

    <div class="small-title">
        A little message for
    </div>

    <h1>
        Kamu.
    </h1>

    <p class="text" style="margin-top:25px;">
        Ada sesuatu yang ingin aku sampaikan.
        Sesuatu yang sebenarnya sudah lama aku simpan.
    </p>

    <button
        class="primary"
        onclick="nextPage(2)"
        style="margin-top:35px;"
    >
        Buka Pesannya →
    </button>

</section>


<!-- ================= PAGE 2 ================= -->

<section class="page" id="page2">

    <div class="small-title">
        Honestly...
    </div>

    <div class="message">

        <p>
            Aku awalnya nggak pernah menyangka
            kalau seseorang seperti kamu bisa
            menjadi begitu berarti buat aku.
        </p>

        <p>
            Tapi semakin sering kita ngobrol,
            semakin aku nyaman sama kamu.
        </p>

        <p>
            Sampai akhirnya aku sadar...
        </p>

    </div>

    <h2
        class="red"
        style="font-size:35px;margin-top:25px;"
    >
        Aku suka sama kamu.
    </h2>

    <button
        class="primary"
        onclick="nextPage(3)"
    >
        Lanjut →
    </button>

</section>


<!-- ================= PAGE 3 ================= -->

<section class="page" id="page3">

    <div class="small-title">
        One question
    </div>

    <h2>
        Maukah kamu<br>
        jadi seseorang<br>
        yang spesial buat aku?
    </h2>

    <p class="text">
        Aku nggak ingin memaksa.
        Aku cuma ingin jujur tentang apa
        yang aku rasakan.
    </p>

    <div style="margin-top:30px;">

        <button
            class="primary"
            onclick="sayYes()"
        >
            Iya ❤️
        </button>

        <button
            id="noButton"
            onclick="sayNo()"
        >
            Belum tahu
        </button>

    </div>

</section>


<!-- ================= PAGE 4 ================= -->

<section class="page" id="page4">

    <div class="small-title">
        It's okay
    </div>

    <h2>
        Aku mengerti.
    </h2>

    <div class="message">

        <p>
            Kamu nggak perlu menjawab sekarang.
        </p>

        <p>
            Ambil waktu yang kamu butuhkan.
            Yang penting kamu tahu bahwa
            perasaan ini tulus.
        </p>

        <p class="red">
            Aku tetap menghargai kamu. 🖤
        </p>

    </div>

    <button onclick="nextPage(3)">
        ← Kembali
    </button>

</section>


<!-- ================= PAGE 5 ================= -->

<section class="page" id="yesPage">

    <div class="big-heart">
        ♥
    </div>

    <div class="small-title">
        Thank you
    </div>

    <h2>
        Jadi... kita?
    </h2>

    <div class="message">

        <p>
            Terima kasih sudah memilih aku. ❤️
        </p>

        <p>
            Aku nggak janji semuanya akan selalu
            sempurna, tapi aku akan berusaha
            menjaga apa yang kita mulai.
        </p>

    </div>

    <button
        class="primary"
        onclick="nextPage(6)"
    >
        Lanjut →
    </button>

</section>


<!-- ================= PAGE 6 ================= -->

<section class="page" id="page6">

    <div class="small-title">
        The end
    </div>

    <h2>
        For you. 🖤
    </h2>

    <p class="text">
        Terima kasih sudah membaca sampai akhir.
        Apa pun yang terjadi setelah ini,
        aku senang akhirnya bisa jujur.
    </p>

    <p
        class="red"
        style="
        font-family:'Cormorant Garamond';
        font-size:25px;
        margin-top:25px;
        "
    >
        — seseorang yang menyukaimu
    </p>

    <button
        onclick="nextPage(1)"
        style="margin-top:30px;"
    >
        Ulangi ↻
    </button>

</section>

</div>


<script>

/* =========================
   NAVIGASI
========================= */

function nextPage(number) {

    document
        .querySelectorAll('.page')
        .forEach(page => {

            page.classList.remove('active');

        });

    if(number === 5) {

        document
            .getElementById('yesPage')
            .classList.add('active');

    } else {

        document
            .getElementById('page' + number)
            .classList.add('active');

    }

}


/* =========================
   JAWABAN IYA
========================= */

function sayYes() {

    nextPage(5);

    createHearts();

}


/* =========================
   JAWABAN BELUM TAHU
========================= */

function sayNo() {

    nextPage(4);

}


/* =========================
   ANIMASI HATI
========================= */

function createHearts() {

    for(let i = 0; i < 50; i++) {

        const heart =
            document.createElement('div');

        heart.innerHTML =
            Math.random() > .3
            ? '♥'
            : '✦';

        heart.style.position =
            'fixed';

        heart.style.left =
            '50%';

        heart.style.top =
            '50%';

        heart.style.color =
            '#b94156';

        heart.style.fontSize =
            (10 + Math.random() * 22) + 'px';

        heart.style.zIndex = '10';

        heart.style.pointerEvents =
            'none';

        document.body.appendChild(heart);


        const x =
            (Math.random() - .5) * 600;

        const y =
            (Math.random() - .5) * 600;


        heart.animate(

            [
                {
                    transform:
                    'translate(-50%,-50%) scale(.3)',
                    opacity: 1
                },

                {
                    transform:
                    `translate(${x}px,${y}px) scale(1)`,
                    opacity: 0
                }

            ],

            {
                duration:
                    1300 + Math.random() * 1000,

                easing:
                    'cubic-bezier(.2,.8,.3,1)'
            }

        );


        setTimeout(() => {

            heart.remove();

        }, 2500);

    }

}


/* =========================
   BINTANG / PARTICLES
========================= */

const stars =
    document.getElementById('stars');


for(let i = 0; i < 35; i++) {

    const star =
        document.createElement('div');

    star.className = 'star';

    star.style.left =
        Math.random() * 100 + 'vw';

    star.style.animationDuration =
        (6 + Math.random() * 12) + 's';

    star.style.animationDelay =
        (-Math.random() * 15) + 's';

    stars.appendChild(star);

}

</script>

</body>
</html>

```
