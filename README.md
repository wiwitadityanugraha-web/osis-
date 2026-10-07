<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>OSIS SMA Negeri 1 Tanjung</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Playfair+Display:wght@600;700;800&display=swap" rel="stylesheet">

<style>

/* =====================================================
   ROOT
===================================================== */

:root{
    --maroon:#4b0715;
    --maroon-dark:#21030a;
    --maroon-light:#6e1024;

    --gold:#d8ad45;
    --gold-light:#f2d37b;
    --gold-dark:#9b7624;

    --cream:#fff9eb;
    --white:#ffffff;

    --text:#f8f4ea;
    --muted:#c9bec0;

    --glass:rgba(255,255,255,.065);
    --border:rgba(216,173,69,.28);

    --shadow:0 20px 60px rgba(0,0,0,.35);
}


/* =====================================================
   RESET
===================================================== */

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:"Inter",sans-serif;
    color:var(--text);

    background:
        radial-gradient(
            circle at 15% 15%,
            rgba(216,173,69,.10),
            transparent 25%
        ),
        radial-gradient(
            circle at 85% 40%,
            rgba(126,15,39,.35),
            transparent 30%
        ),
        linear-gradient(
            135deg,
            #21030a,
            #4b0715 45%,
            #26030b
        );

    min-height:100vh;
    overflow-x:hidden;
}


/* GOLD GRID BACKGROUND */

body::before{
    content:"";
    position:fixed;
    inset:0;

    background-image:
        linear-gradient(
            rgba(216,173,69,.035) 1px,
            transparent 1px
        ),
        linear-gradient(
            90deg,
            rgba(216,173,69,.035) 1px,
            transparent 1px
        );

    background-size:50px 50px;

    pointer-events:none;
    z-index:-2;
}


/* LIGHT EFFECT */

body::after{
    content:"";
    position:fixed;

    width:450px;
    height:450px;

    border-radius:50%;

    background:rgba(216,173,69,.08);

    filter:blur(130px);

    top:-200px;
    right:-150px;

    pointer-events:none;
    z-index:-1;
}


a{
    text-decoration:none;
    color:inherit;
}

button,
input{
    font-family:inherit;
}


/* =====================================================
   NAVBAR
===================================================== */

.navbar{

    position:fixed;

    top:0;
    left:0;

    width:100%;
    height:78px;

    display:flex;
    align-items:center;
    justify-content:space-between;

    padding:0 7%;

    background:rgba(33,3,10,.82);

    backdrop-filter:blur(20px);

    border-bottom:1px solid rgba(216,173,69,.18);

    z-index:1000;
}


.logo{
    display:flex;
    align-items:center;
    gap:12px;
}


.logo-mark{

    width:45px;
    height:45px;

    display:grid;
    place-items:center;

    border-radius:13px;

    background:
        linear-gradient(
            135deg,
            var(--gold-light),
            var(--gold-dark)
        );

    color:var(--maroon-dark);

    font-family:"Playfair Display";

    font-size:23px;
    font-weight:800;

    box-shadow:
        0 0 25px rgba(216,173,69,.25);
}


.logo-text strong{

    display:block;

    font-size:13px;

    letter-spacing:1px;
}


.logo-text span{

    display:block;

    color:var(--gold-light);

    font-size:9px;

    letter-spacing:2px;

    margin-top:3px;
}


.nav-menu{

    display:flex;

    gap:28px;

    list-style:none;
}


.nav-menu a{

    color:#e9dfe1;

    font-size:12px;

    font-weight:600;

    transition:.3s;

    position:relative;
}


.nav-menu a:hover{
    color:var(--gold-light);
}


.nav-menu a::after{

    content:"";

    position:absolute;

    width:0;
    height:2px;

    background:var(--gold);

    left:50%;
    bottom:-8px;

    transform:translateX(-50%);

    transition:.3s;
}


.nav-menu a:hover::after{
    width:100%;
}


.menu-button{

    display:none;

    background:none;

    border:none;

    color:white;

    font-size:25px;

    cursor:pointer;
}


/* =====================================================
   HERO
===================================================== */

.hero{

    min-height:100vh;

    padding:150px 7% 90px;

    display:grid;

    grid-template-columns:1.1fr .9fr;

    align-items:center;

    gap:70px;
}


.badge{

    display:inline-flex;

    align-items:center;

    gap:8px;

    padding:9px 15px;

    border-radius:50px;

    background:rgba(216,173,69,.08);

    border:1px solid rgba(216,173,69,.35);

    color:var(--gold-light);

    font-size:10px;

    font-weight:700;

    letter-spacing:2px;

    margin-bottom:25px;
}


.badge-dot{

    width:7px;
    height:7px;

    border-radius:50%;

    background:var(--gold);

    box-shadow:0 0 15px var(--gold);

    animation:pulse 1.8s infinite;
}


@keyframes pulse{

    50%{
        opacity:.35;
        transform:scale(.6);
    }

}


.hero h1{

    font-family:"Playfair Display";

    font-size:clamp(45px,6vw,82px);

    line-height:1;

    margin-bottom:25px;

    letter-spacing:-2px;
}


.hero h1 span{

    color:var(--gold-light);

    text-shadow:
        0 0 35px rgba(216,173,69,.15);
}


.hero-description{

    color:var(--muted);

    max-width:650px;

    line-height:1.8;

    font-size:14px;

    margin-bottom:35px;
}


.hero-buttons{

    display:flex;

    flex-wrap:wrap;

    gap:13px;
}


.btn{

    padding:14px 21px;

    border-radius:10px;

    font-size:12px;

    font-weight:700;

    cursor:pointer;

    transition:.3s;

    border:1px solid var(--border);
}


.btn-gold{

    color:var(--maroon-dark);

    background:
        linear-gradient(
            135deg,
            var(--gold-light),
            var(--gold)
        );

    box-shadow:
        0 10px 30px rgba(216,173,69,.15);
}


.btn-gold:hover{

    transform:translateY(-4px);

    box-shadow:
        0 15px 40px rgba(216,173,69,.28);
}


.btn-outline{

    background:rgba(255,255,255,.03);

    color:white;
}


.btn-outline:hover{

    background:rgba(216,173,69,.08);

    color:var(--gold-light);

    transform:translateY(-4px);
}


/* =====================================================
   HERO EMBLEM
===================================================== */

.hero-visual{

    display:flex;

    justify-content:center;

    align-items:center;
}


.emblem{

    width:min(410px,80vw);
    height:min(410px,80vw);

    position:relative;

    display:grid;

    place-items:center;

    border-radius:50%;
}


.emblem::before{

    content:"";

    position:absolute;

    inset:0;

    border-radius:50%;

    border:1px solid rgba(216,173,69,.35);

    animation:rotate 18s linear infinite;
}


.emblem::after{

    content:"";

    position:absolute;

    inset:45px;

    border-radius:50%;

    border:1px dashed rgba(255,255,255,.2);

    animation:rotateReverse 13s linear infinite;
}


@keyframes rotate{

    to{
        transform:rotate(360deg);
    }

}


@keyframes rotateReverse{

    to{
        transform:rotate(-360deg);
    }

}


.emblem-center{

    width:220px;
    height:220px;

    border-radius:50%;

    display:grid;
    place-items:center;

    text-align:center;

    background:

        radial-gradient(
            circle at 35% 25%,
            #7d1830,
            #4b0715 55%,
            #21030a
        );

    border:2px solid rgba(216,173,69,.7);

    box-shadow:

        0 0 50px rgba(216,173,69,.13),

        inset 0 0 40px rgba(0,0,0,.45);
}


.emblem-center strong{

    display:block;

    font-family:"Playfair Display";

    font-size:48px;

    color:var(--gold-light);
}


.emblem-center span{

    font-size:9px;

    letter-spacing:3px;

    color:#eee4cc;
}


/* =====================================================
   SECTION
===================================================== */

section{
    padding:100px 7%;
}


.section-heading{

    max-width:800px;

    margin:0 auto 55px;

    text-align:center;
}


.section-label{

    color:var(--gold-light);

    font-size:10px;

    font-weight:800;

    letter-spacing:4px;

    margin-bottom:12px;
}


.section-heading h2{

    font-family:"Playfair Display";

    font-size:clamp(30px,4vw,46px);

    margin-bottom:15px;
}


.section-heading p{

    color:var(--muted);

    font-size:13px;

    line-height:1.8;
}


/* =====================================================
   STATISTICS
===================================================== */

.stats{

    max-width:1100px;

    margin:-20px auto 70px;

    padding:0 7%;

    display:grid;

    grid-template-columns:repeat(4,1fr);

    gap:15px;
}


.stat{

    padding:25px;

    text-align:center;

    border-radius:17px;

    background:rgba(255,255,255,.045);

    border:1px solid rgba(216,173,69,.18);

    backdrop-filter:blur(15px);

    transition:.3s;
}


.stat:hover{

    transform:translateY(-6px);

    border-color:rgba(216,173,69,.5);

    box-shadow:var(--shadow);
}


.stat strong{

    display:block;

    color:var(--gold-light);

    font-family:"Playfair Display";

    font-size:32px;
}


.stat span{

    color:var(--muted);

    font-size:9px;

    letter-spacing:1px;
}


/* =====================================================
   ABOUT
===================================================== */

.about-container{

    max-width:1100px;

    margin:auto;

    display:grid;

    grid-template-columns:1fr 1fr;

    gap:25px;
}


.card{

    padding:32px;

    border-radius:20px;

    background:
        linear-gradient(
            145deg,
            rgba(255,255,255,.07),
            rgba(255,255,255,.025)
        );

    border:1px solid rgba(216,173,69,.2);

    backdrop-filter:blur(20px);

    box-shadow:var(--shadow);

    transition:.35s;
}


.card:hover{

    border-color:rgba(216,173,69,.45);

    transform:translateY(-5px);
}


.card h3{

    font-family:"Playfair Display";

    font-size:20px;

    margin-bottom:18px;

    color:var(--gold-light);
}


.card p,
.card li{

    color:var(--muted);

    line-height:1.8;

    font-size:13px;
}


.card ul{

    padding-left:20px;
}


/* =====================================================
   VISION
===================================================== */

.vision-grid{

    max-width:1100px;

    margin:auto;

    display:grid;

    grid-template-columns:1fr 1fr;

    gap:25px;
}


.vision-box{

    position:relative;

    overflow:hidden;
}


.vision-box::after{

    content:"";

    position:absolute;

    width:180px;
    height:180px;

    right:-70px;
    top:-70px;

    border-radius:50%;

    background:rgba(216,173,69,.07);

    filter:blur(10px);
}


.vision-number{

    color:var(--gold);

    font-family:monospace;

    font-size:11px;

    margin-bottom:15px;
}


/* =====================================================
   STRUCTURE
===================================================== */

.structure-tools{

    max-width:750px;

    margin:0 auto 45px;

    display:flex;

    gap:10px;
}


.search{

    flex:1;

    padding:15px 18px;

    background:rgba(20,2,7,.65);

    border:1px solid rgba(216,173,69,.25);

    border-radius:11px;

    color:white;

    outline:none;

    font-size:12px;
}


.search:focus{

    border-color:var(--gold);

    box-shadow:
        0 0 25px rgba(216,173,69,.08);
}


.print-button{

    padding:0 18px;

    border-radius:11px;

    border:1px solid var(--border);

    background:rgba(216,173,69,.08);

    color:var(--gold-light);

    cursor:pointer;
}


/* ORG CHART */

.organization{

    max-width:1200px;

    margin:auto;
}


.top{

    display:flex;

    justify-content:center;
}


.connector{

    width:2px;

    height:40px;

    margin:auto;

    background:
        linear-gradient(
            var(--gold),
            transparent
        );
}


.executive{

    display:flex;

    justify-content:center;

    gap:15px;

    flex-wrap:wrap;
}


.position{

    width:190px;

    min-height:245px;

    padding:15px;

    text-align:center;

    background:

        linear-gradient(
            145deg,
            rgba(100,15,35,.72),
            rgba(28,2,9,.88)
        );

    border:1px solid rgba(216,173,69,.23);

    border-radius:18px;

    transition:.35s;

    position:relative;
}


.position:hover{

    transform:
        translateY(-7px)
        scale(1.02);

    border-color:rgba(216,173,69,.7);

    box-shadow:
        0 20px 50px rgba(0,0,0,.4);
}


.position.leader{

    width:220px;

    border-color:rgba(216,173,69,.6);

    box-shadow:
        0 0 35px rgba(216,173,69,.08);
}


.photo{

    width:92px;
    height:92px;

    object-fit:cover;

    display:block;

    margin:0 auto 13px;

    border-radius:50%;

    border:2px solid rgba(216,173,69,.55);

    background:
        linear-gradient(
            135deg,
            #71142c,
            #25030b
        );
}


.leader .photo{

    width:105px;
    height:105px;
}


.role{

    color:var(--gold-light);

    font-size:9px;

    font-weight:800;

    letter-spacing:1px;

    line-height:1.4;
}


.person{

    font-size:12px;

    font-weight:700;

    margin-top:8px;
}


.id{

    color:#8f797d;

    font-family:monospace;

    font-size:9px;

    margin-top:8px;
}


.middle-line{

    width:75%;

    height:1px;

    margin:40px auto;

    background:
        linear-gradient(
            90deg,
            transparent,
            rgba(216,173,69,.55),
            transparent
        );
}


.division-title{

    text-align:center;

    font-family:"Playfair Display";

    font-size:20px;

    margin-bottom:30px;
}


.division-title span{

    color:var(--gold-light);
}


/* =====================================================
   SIE GRID
===================================================== */

.sie-grid{

    display:grid;

    grid-template-columns:repeat(2,1fr);

    gap:22px;
}


.sie{

    padding:22px;

    border-radius:20px;

    background:

        linear-gradient(
            145deg,
            rgba(255,255,255,.065),
            rgba(255,255,255,.025)
        );

    border:1px solid rgba(216,173,69,.18);

    backdrop-filter:blur(15px);

    transition:.35s;
}


.sie:hover{

    border-color:rgba(216,173,69,.45);

    transform:translateY(-4px);
}


.sie-header{

    display:flex;

    align-items:center;

    gap:12px;

    margin-bottom:18px;
}


.sie-number{

    width:38px;
    height:38px;

    display:grid;

    place-items:center;

    border-radius:10px;

    background:
        linear-gradient(
            135deg,
            var(--gold-light),
            var(--gold-dark)
        );

    color:var(--maroon-dark);

    font-size:10px;

    font-weight:800;
}


.sie-header h3{

    font-size:13px;

    line-height:1.4;
}


.members{

    display:grid;

    grid-template-columns:repeat(3,1fr);

    gap:10px;
}


.member{

    padding:12px 7px;

    text-align:center;

    border-radius:13px;

    background:rgba(0,0,0,.15);

    border:1px solid rgba(255,255,255,.06);

    transition:.3s;
}


.member:hover{

    background:rgba(216,173,69,.07);

    border-color:rgba(216,173,69,.3);

    transform:translateY(-3px);
}


.member img{

    width:58px;
    height:58px;

    display:block;

    margin:auto;

    object-fit:cover;

    border-radius:50%;

    border:1px solid rgba(216,173,69,.4);

    background:#3b0814;
}


.member p{

    margin-top:8px;

    color:#ddd2d4;

    font-size:9px;

    line-height:1.4;
}


/* =====================================================
   PROGRAM
===================================================== */

.program-grid{

    max-width:1100px;

    margin:auto;

    display:grid;

    grid-template-columns:repeat(3,1fr);

    gap:18px;
}


.program{

    padding:25px;

    border-radius:18px;

    background:rgba(255,255,255,.045);

    border:1px solid rgba(216,173,69,.18);

    transition:.35s;
}


.program:hover{

    transform:translateY(-6px);

    border-color:rgba(216,173,69,.5);
}


.program-icon{

    font-size:27px;

    margin-bottom:16px;
}


.program h3{

    font-family:"Playfair Display";

    color:var(--gold-light);

    font-size:17px;

    margin-bottom:8px;
}


.program p{

    color:var(--muted);

    font-size:11px;

    line-height:1.7;
}


.program-status{

    display:inline-block;

    margin-top:14px;

    padding:5px 8px;

    border-radius:6px;

    background:rgba(216,173,69,.08);

    color:var(--gold-light);

    font-size:8px;

    font-weight:700;

    letter-spacing:1px;
}


/* =====================================================
   ASPIRASI
===================================================== */

.aspiration{

    max-width:1050px;

    margin:auto;

    padding:45px;

    text-align:center;

    border-radius:25px;

    background:

        linear-gradient(
            135deg,
            rgba(110,16,36,.8),
            rgba(45,3,13,.85)
        );

    border:1px solid rgba(216,173,69,.4);

    box-shadow:
        0 20px 70px rgba(0,0,0,.35);
}


.aspiration h2{

    font-family:"Playfair Display";

    font-size:32px;

    margin-bottom:13px;
}


.aspiration p{

    color:#d9cdd0;

    font-size:12px;

    line-height:1.8;

    max-width:650px;

    margin:0 auto 25px;
}


/* =====================================================
   GALLERY
===================================================== */

.gallery{

    max-width:1100px;

    margin:auto;

    display:grid;

    grid-template-columns:2fr 1fr 1fr;

    grid-auto-rows:200px;

    gap:13px;
}


.gallery-item{

    overflow:hidden;

    position:relative;

    border-radius:17px;

    border:1px solid rgba(216,173,69,.18);

    background:#30050e;
}


.gallery-item:first-child{

    grid-row:span 2;
}


.gallery-item img{

    width:100%;
    height:100%;

    object-fit:cover;

    opacity:.75;

    transition:.5s;
}


.gallery-item:hover img{

    transform:scale(1.08);

    opacity:1;
}


.gallery-label{

    position:absolute;

    bottom:12px;
    left:12px;

    padding:7px 10px;

    border-radius:7px;

    background:rgba(0,0,0,.65);

    font-size:8px;

    letter-spacing:1px;
}


/* =====================================================
   FOOTER
===================================================== */

footer{

    margin-top:50px;

    padding:50px 7%;

    border-top:1px solid rgba(216,173,69,.18);

    background:rgba(20,2,7,.7);
}


.footer-container{

    max-width:1100px;

    margin:auto;

    display:flex;

    justify-content:space-between;

    align-items:center;

    gap:30px;
}


.footer-brand strong{

    font-family:"Playfair Display";

    font-size:17px;

    color:var(--gold-light);
}


.footer-brand p{

    color:var(--muted);

    font-size:10px;

    margin-top:7px;
}


.footer-code{

    color:#927f83;

    font-family:monospace;

    font-size:9px;

    line-height:1.7;

    text-align:right;
}


/* =====================================================
   BACK TO TOP
===================================================== */

#topButton{

    position:fixed;

    right:25px;
    bottom:25px;

    width:44px;
    height:44px;

    border-radius:12px;

    border:1px solid rgba(216,173,69,.35);

    background:rgba(33,3,10,.9);

    color:var(--gold-light);

    cursor:pointer;

    opacity:0;

    pointer-events:none;

    transition:.3s;

    z-index:900;
}


#topButton.show{

    opacity:1;

    pointer-events:auto;
}


/* =====================================================
   REVEAL ANIMATION
===================================================== */

.reveal{

    opacity:0;

    transform:translateY(30px);

    transition:
        opacity .8s ease,
        transform .8s ease;
}


.reveal.active{

    opacity:1;

    transform:translateY(0);
}


/* =====================================================
   PRINT
===================================================== */

@media print{

    .navbar,
    .hero,
    .stats,
    .structure-tools,
    #topButton,
    footer{

        display:none!important;
    }

    body{

        background:white;

        color:black;
    }

    body::before,
    body::after{

        display:none;
    }

    section{

        padding:20px;
    }

    .position,
    .sie{

        background:white;

        color:black;

        box-shadow:none;

        break-inside:avoid;
    }
}


/* =====================================================
   TABLET
===================================================== */

@media(max-width:950px){

    .hero{

        grid-template-columns:1fr;

        text-align:center;
    }


    .hero-description{

        margin-left:auto;
        margin-right:auto;
    }


    .hero-buttons{

        justify-content:center;
    }


    .hero-visual{

        margin-top:30px;
    }


    .stats{

        grid-template-columns:repeat(2,1fr);
    }


    .program-grid{

        grid-template-columns:repeat(2,1fr);
    }

}


/* =====================================================
   MOBILE
===================================================== */

@media(max-width:700px){

    .navbar{

        padding:0 5%;
    }


    .menu-button{

        display:block;
    }


    .nav-menu{

        position:absolute;

        top:78px;

        left:0;

        width:100%;

        flex-direction:column;

        gap:0;

        padding:10px 6%;

        background:rgba(33,3,10,.97);

        backdrop-filter:blur(20px);

        transform:translateY(-150%);

        transition:.35s;
    }


    .nav-menu.active{

        transform:translateY(0);
    }


    .nav-menu li{

        padding:14px 0;
    }


    section{

        padding:75px 5%;
    }


    .hero{

        padding-left:5%;
        padding-right:5%;
    }


    .about-container,
    .vision-grid,
    .sie-grid{

        grid-template-columns:1fr;
    }


    .members{

        grid-template-columns:repeat(3,1fr);
    }


    .program-grid{

        grid-template-columns:1fr;
    }


    .gallery{

        grid-template-columns:1fr 1fr;

        grid-auto-rows:150px;
    }


    .gallery-item:first-child{

        grid-row:span 1;
    }


    .footer-container{

        flex-direction:column;

        text-align:center;
    }


    .footer-code{

        text-align:center;
    }

}


@media(max-width:450px){

    .stats{

        grid-template-columns:1fr 1fr;

        padding:0 5%;
    }


    .stat{

        padding:18px 8px;
    }


    .stat strong{

        font-size:24px;
    }


    .position{

        width:175px;
    }


    .position.leader{

        width:200px;
    }


    .members{

        gap:5px;
    }


    .member{

        padding:9px 3px;
    }


    .member img{

        width:48px;
        height:48px;
    }

}

</style>
</head>


<body>


<!-- =====================================================
     NAVBAR
===================================================== -->

<nav class="navbar">

    <a href="#home" class="logo">

        <div class="logo-mark">
            O
        </div>

        <div class="logo-text">

            <strong>OSIS SMA NEGERI 1 TANJUNG</strong>

            <span>STUDENT ORGANIZATION</span>

        </div>

    </a>


    <button
        class="menu-button"
        id="menuButton"
    >
        ☰
    </button>


    <ul class="nav-menu" id="navMenu">

        <li>
            <a href="#home">Beranda</a>
        </li>

        <li>
            <a href="#tentang">Tentang</a>
        </li>

        <li>
            <a href="#visi">Visi & Misi</a>
        </li>

        <li>
            <a href="#struktur">Struktur</a>
        </li>

        <li>
            <a href="#program">Program Kerja</a>
        </li>

        <li>
            <a href="#aspirasi">Aspirasi</a>
        </li>

        <li>
            <a href="#galeri">Galeri</a>
        </li>

    </ul>

</nav>



<!-- =====================================================
     HERO
===================================================== -->

<section class="hero" id="home">

    <div class="reveal">

        <div class="badge">

            <span class="badge-dot"></span>

            OSIS • SMA NEGERI 1 TANJUNG

        </div>


        <h1>

            Bersama Untuk
            <span>Berkarya.</span>

        </h1>


        <p class="hero-description">

            Website organisasi siswa yang menjadi pusat
            informasi mengenai kepengurusan, visi dan misi,
            program kerja, aspirasi siswa, serta dokumentasi
            kegiatan OSIS SMA Negeri 1 Tanjung.

        </p>


        <div class="hero-buttons">

            <a
                href="#struktur"
                class="btn btn-gold"
            >
                LIHAT STRUKTUR
            </a>


            <a
                href="#aspirasi"
                class="btn btn-outline"
            >
                KIRIM ASPIRASI
            </a>

        </div>

    </div>



    <div class="hero-visual reveal">

        <div class="emblem">

            <div class="emblem-center">

                <div>

                    <strong>OSIS</strong>

                    <span>
                        SMA NEGERI 1 TANJUNG
                    </span>

                </div>

            </div>

        </div>

    </div>

</section>



<!-- =====================================================
     STATS
===================================================== -->

<div class="stats">

    <div class="stat reveal">

        <strong>36</strong>

        <span>
            POSISI PENGURUS
        </span>

    </div>


    <div class="stat reveal">

        <strong>10</strong>

        <span>
            SEKSI BIDANG
        </span>

    </div>


    <div class="stat reveal">

        <strong>30</strong>

        <span>
            ANGGOTA SIE
        </span>

    </div>


    <div class="stat reveal">

        <strong>∞</strong>

        <span>
            RUANG BERKARYA
        </span>

    </div>

</div>



<!-- =====================================================
     TENTANG
===================================================== -->

<section id="tentang">

    <div class="section-heading reveal">

        <div class="section-label">
            // ABOUT OSIS
        </div>

        <h2>
            Mengenal OSIS
        </h2>

        <p>
            Organisasi siswa sebagai ruang pembelajaran
            kepemimpinan, kreativitas, tanggung jawab,
            kolaborasi, dan pengembangan potensi siswa.
        </p>

    </div>


    <div class="about-container">

        <div class="card reveal">

            <h3>
                Tentang Organisasi
            </h3>

            <p>

                OSIS SMA Negeri 1 Tanjung merupakan wadah
                bagi siswa untuk berpartisipasi dalam berbagai
                kegiatan sekolah serta mengembangkan kemampuan
                kepemimpinan dan organisasi.

                <br><br>

                Melalui kerja sama dan semangat kebersamaan,
                OSIS berupaya menciptakan lingkungan sekolah
                yang aktif, kreatif, disiplin, dan aspiratif.

            </p>

        </div>


        <div class="card reveal">

            <h3>
                Nilai Organisasi
            </h3>

            <ul>

                <li>
                    Integritas dan tanggung jawab
                </li>

                <li>
                    Kolaborasi antar siswa
                </li>

                <li>
                    Kreativitas dan inovasi
                </li>

                <li>
                    Kepedulian terhadap lingkungan
                </li>

                <li>
                    Pengembangan prestasi siswa
                </li>

                <li>
                    Kepemimpinan dan kedisiplinan
                </li>

            </ul>

        </div>

    </div>

</section>



<!-- =====================================================
     VISI MISI
===================================================== -->

<section id="visi">

    <div class="section-heading reveal">

        <div class="section-label">
            // VISION & MISSION
        </div>

        <h2>
            Visi & Misi
        </h2>

        <p>
            Arah dan prinsip yang menjadi dasar dalam
            menjalankan organisasi.
        </p>

    </div>


    <div class="vision-grid">

        <div class="card vision-box reveal">

            <div class="vision-number">
                VISION_01
            </div>

            <h3>
                OSIS Kolaboratif & Berintegritas
            </h3>

            <p>

                Mewujudkan OSIS yang kolaboratif,
                aspiratif, inovatif, dan berintegritas
                sebagai wadah pengembangan potensi siswa.

            </p>

        </div>


        <div class="card vision-box reveal">

            <div class="vision-number">
                MISSION_01
            </div>

            <h3>
                Misi Organisasi
            </h3>

            <ul>

                <li>
                    Meningkatkan kolaborasi siswa dan ekstrakurikuler.
                </li>

                <li>
                    Mendukung peningkatan prestasi siswa.
                </li>

                <li>
                    Mengembangkan kreativitas dan kepemimpinan.
                </li>

                <li>
                    Membangun budaya sekolah yang disiplin dan peduli.
                </li>

            </ul>

        </div>

    </div>

</section>



<!-- =====================================================
     STRUKTUR
===================================================== -->

<section id="struktur">

    <div class="section-heading reveal">

        <div class="section-label">
            // ORGANIZATION STRUCTURE
        </div>

        <h2>
            Struktur Kepengurusan
        </h2>

        <p>
            Struktur organisasi OSIS SMA Negeri 1 Tanjung.
            Setiap kotak dapat diisi foto dan nama pengurus.
        </p>

    </div>


    <div class="structure-tools">

        <input
            class="search"
            id="search"
            type="text"
            placeholder="🔎 Cari nama atau jabatan..."
        >


        <button
            class="print-button"
            onclick="window.print()"
        >
            🖨 Cetak
        </button>

    </div>


    <div class="organization">


        <!-- KETUA -->

        <div class="top">

            <div class="position leader reveal">

                <img
                    class="photo"
                    src="images/ketua.jpg"
                    alt="Ketua OSIS"
                >

                <div class="role">
                    KETUA OSIS
                </div>

                <div class="person">
                    Nama Ketua
                </div>

                <div class="id">
                    OSIS-001
                </div>

            </div>

        </div>


        <div class="connector"></div>


        <!-- WAKIL -->

        <div class="top">

            <div class="position reveal">

                <img
                    class="photo"
                    src="images/wakil.jpg"
                    alt="Wakil Ketua"
                >

                <div class="role">
                    WAKIL KETUA
                </div>

                <div class="person">
                    Nama Wakil
                </div>

                <div class="id">
                    OSIS-002
                </div>

            </div>

        </div>


        <div class="middle-line"></div>


        <!-- SEKRETARIS + BENDAHARA -->

        <div class="executive">


            <div class="position reveal">

                <img
                    class="photo"
                    src="images/sekretaris1.jpg"
                    alt=""
                >

                <div class="role">
                    SEKRETARIS 1
                </div>

                <div class="person">
                    Nama Sekretaris 1
                </div>

                <div class="id">
                    OSIS-003
                </div>

            </div>


            <div class="position reveal">

                <img
                    class="photo"
                    src="images/sekretaris2.jpg"
                    alt=""
                >

                <div class="role">
                    SEKRETARIS 2
                </div>

                <div class="person">
                    Nama Sekretaris 2
                </div>

                <div class="id">
                    OSIS-004
                </div>

            </div>


            <div class="position reveal">

                <img
                    class="photo"
                    src="images/bendahara1.jpg"
                    alt=""
                >

                <div class="role">
                    BENDAHARA 1
                </div>

                <div class="person">
                    Nama Bendahara 1
                </div>

                <div class="id">
                    OSIS-005
                </div>

            </div>


            <div class="position reveal">

                <img
                    class="photo"
                    src="images/bendahara2.jpg"
                    alt=""
                >

                <div class="role">
                    BENDAHARA 2
                </div>

                <div class="person">
                    Nama Bendahara 2
                </div>

                <div class="id">
                    OSIS-006
                </div>

            </div>

        </div>


        <div class="middle-line"></div>


        <div class="division-title">

            SEKSI BIDANG

            <span>
                // 10 DIVISI
            </span>

        </div>



        <!-- =================================================
             SIE 01
        ================================================= -->

        <div class="sie-grid">


            <div class="sie reveal">

                <div class="sie-header">

                    <div class="sie-number">
                        01
                    </div>

                    <h3>
                        Sie Ketaqwaan
                    </h3>

                </div>


                <div class="members">

                    <div class="member">

                        <img src="images/ketaqwaan1.jpg">

                        <p>
                            Nama Anggota 1
                        </p>

                    </div>


                    <div class="member">

                        <img src="images/ketaqwaan2.jpg">

                        <p>
                            Nama Anggota 2
                        </p>

                    </div>


                    <div class="member">

                        <img src="images/ketaqwaan3.jpg">

                        <p>
                            Nama Anggota 3
                        </p>

                    </div>

                </div>

            </div>



            <!-- SIE 02 -->

            <div class="sie reveal">

                <div class="sie-header">

                    <div class="sie-number">
                        02
                    </div>

                    <h3>
                        Sie Budi Pekerti
                    </h3>

                </div>


                <div class="members">

                    <div class="member">
                        <img src="images/budipekerti1.jpg">
                        <p>Nama Anggota 1</p>
                    </div>

                    <div class="member">
                        <img src="images/budipekerti2.jpg">
                        <p>Nama Anggota 2</p>
                    </div>

                    <div class="member">
                        <img src="images/budipekerti3.jpg">
                        <p>Nama Anggota 3</p>
                    </div>

                </div>

            </div>



            <!-- SIE 03 -->

            <div class="sie reveal">

                <div class="sie-header">

                    <div class="sie-number">
                        03
                    </div>

                    <h3>
                        Sie Wawasan Kebangsaan dan Bela Negara
                    </h3>

                </div>


                <div class="members">

                    <div class="member">
                        <img src="images/kebangsaan1.jpg">
                        <p>Nama Anggota 1</p>
                    </div>

                    <div class="member">
                        <img src="images/kebangsaan2.jpg">
                        <p>Nama Anggota 2</p>
                    </div>

                    <div class="member">
                        <img src="images/kebangsaan3.jpg">
                        <p>Nama Anggota 3</p>
                    </div>

                </div>

            </div>



            <!-- SIE 04 -->

            <div class="sie reveal">

                <div class="sie-header">

                    <div class="sie-number">
                        04
                    </div>

                    <h3>
                        Sie Kesenian
                    </h3>

                </div>


                <div class="members">

                    <div class="member">
                        <img src="images/kesenian1.jpg">
                        <p>Nama Anggota 1</p>
                    </div>

                    <div class="member">
                        <img src="images/kesenian2.jpg">
                        <p>Nama Anggota 2</p>
                    </div>

                    <div class="member">
                        <img src="images/kesenian3.jpg">
                        <p>Nama Anggota 3</p>
                    </div>

                </div>

            </div>



            <!-- SIE 05 -->

            <div class="sie reveal">

                <div class="sie-header">

                    <div class="sie-number">
                        05
                    </div>

                    <h3>
                        Sie Demokrasi dan Hak Asasi Manusia
                    </h3>

                </div>


                <div class="members">

                    <div class="member">
                        <img src="images/demokrasi1.jpg">
                        <p>Nama Anggota 1</p>
                    </div>

                    <div class="member">
                        <img src="images/demokrasi2.jpg">
                        <p>Nama Anggota 2</p>
                    </div>

                    <div class="member">
                        <img src="images/demokrasi3.jpg">
                        <p>Nama Anggota 3</p>
                    </div>

                </div>

            </div>



            <!-- SIE 06 -->

            <div class="sie reveal">

                <div class="sie-header">

                    <div class="sie-number">
                        06
                    </div>

                    <h3>
                        Sie Kewirausahaan
                    </h3>

                </div>


                <div class="members">

                    <div class="member">
                        <img src="images/kewirausahaan1.jpg">
                        <p>Nama Anggota 1</p>
                    </div>

                    <div class="member">
                        <img src="images/kewirausahaan2.jpg">
                        <p>Nama Anggota 2</p>
                    </div>

                    <div class="member">
                        <img src="images/kewirausahaan3.jpg">
                        <p>Nama Anggota 3</p>
                    </div>

                </div>

            </div>



            <!-- SIE 07 -->

            <div class="sie reveal">

                <div class="sie-header">

                    <div class="sie-number">
                        07
                    </div>

                    <h3>
                        Sie Jasmani
                    </h3>

                </div>


                <div class="members">

                    <div class="member">
                        <img src="images/jasmani1.jpg">
                        <p>Nama Anggota 1</p>
                    </div>

                    <div class="member">
                        <img src="images/jasmani2.jpg">
                        <p>Nama Anggota 2</p>
                    </div>

                    <div class="member">
                        <img src="images/jasmani3.jpg">
                        <p>Nama Anggota 3</p>
                    </div>

                </div>

            </div>



            <!-- SIE 08 -->

            <div class="sie reveal">

                <div class="sie-header">

                    <div class="sie-number">
                        08
                    </div>

                    <h3>
                        Sie Sastra dan Budaya
                    </h3>

                </div>


                <div class="members">

                    <div class="member">
                        <img src="images/sastrabudaya1.jpg">
                        <p>Nama Anggota 1</p>
                    </div>

                    <div class="member">
                        <img src="images/sastrabudaya2.jpg">
                        <p>Nama Anggota 2</p>
                    </div>

                    <div class="member">
                        <img src="images/sastrabudaya3.jpg">
                        <p>Nama Anggota 3</p>
                    </div>

                </div>

            </div>



            <!-- SIE 09 -->

            <div class="sie reveal">

                <div class="sie-header">

                    <div class="sie-number">
                        09
                    </div>

                    <h3>
                        Sie Teknologi dan Informatika
                    </h3>

                </div>


                <div class="members">

                    <div class="member">
                        <img src="images/teknologi1.jpg">
                        <p>Nama Anggota 1</p>
                    </div>

                    <div class="member">
                        <img src="images/teknologi2.jpg">
                        <p>Nama Anggota 2</p>
                    </div>

                    <div class="member">
                        <img src="images/teknologi3.jpg">
                        <p>Nama Anggota 3</p>
                    </div>

                </div>

            </div>



            <!-- SIE 10 -->

            <div class="sie reveal">

                <div class="sie-header">

                    <div class="sie-number">
                        10
                    </div>

                    <h3>
                        Sie Komunikasi dalam Bahasa Inggris
                    </h3>

                </div>


                <div class="members">

                    <div class="member">
                        <img src="images/english1.jpg">
                        <p>Nama Anggota 1</p>
                    </div>

                    <div class="member">
                        <img src="images/english2.jpg">
                        <p>Nama Anggota 2</p>
                    </div>

                    <div class="member">
                        <img src="images/english3.jpg">
                        <p>Nama Anggota 3</p>
                    </div>

                </div>

            </div>

        </div>

    </div>

</section>



<!-- =====================================================
     PROGRAM KERJA
===================================================== -->

<section id="program">

    <div class="section-heading reveal">

        <div class="section-label">
            // WORK PROGRAM
        </div>

        <h2>
            Program Kerja
        </h2>

        <p>
            Ruang untuk menampilkan program kerja yang
            telah dilaksanakan maupun sedang berjalan.
        </p>

    </div>


    <div class="program-grid">


        <div class="program reveal">

            <div class="program-icon">
                🎨
            </div>

            <h3>
                Pengembangan Kesenian
            </h3>

            <p>
                Mendukung kegiatan dan perkembangan
                ekstrakurikuler seni seperti Atari dan Band.
            </p>

            <span class="program-status">
                TERLAKSANA
            </span>

        </div>


        <div class="program reveal">

            <div class="program-icon">
                🏆
            </div>

            <h3>
                Student Achievement
            </h3>

            <p>
                Mendukung siswa dalam mengembangkan prestasi
                akademik dan nonakademik.
            </p>

            <span class="program-status">
                TERLAKSANA
            </span>

        </div>


        <div class="program reveal">

            <div class="program-icon">
                🇮🇩
            </div>

            <h3>
                Bela Negara
            </h3>

            <p>
                Kegiatan yang menumbuhkan kedisiplinan,
                nasionalisme, dan rasa tanggung jawab.
            </p>

            <span class="program-status">
                TERLAKSANA
            </span>

        </div>


        <div class="program reveal">

            <div class="program-icon">
                🌱
            </div>

            <h3>
                Green School
            </h3>

            <p>
                Mendorong kepedulian siswa terhadap kebersihan
                dan lingkungan sekolah.
            </p>

            <span class="program-status">
                TERLAKSANA
            </span>

        </div>


        <div class="program reveal">

            <div class="program-icon">
                💡
            </div>

            <h3>
                Student Aspiration
            </h3>

            <p>
                Membuka ruang komunikasi agar siswa dapat
                menyampaikan ide dan aspirasi.
            </p>

            <span class="program-status">
                TERBUKA
            </span>

        </div>


        <div class="program reveal">

            <div class="program-icon">
                🤝
            </div>

            <h3>
                OSIS Collaboration
            </h3>

            <p>
                Kolaborasi OSIS dengan berbagai organisasi
                dan ekstrakurikuler sekolah.
            </p>

            <span class="program-status">
                BERJALAN
            </span>

        </div>

    </div>

</section>



<!-- =====================================================
     ASPIRASI
===================================================== -->

<section id="aspirasi">

    <div class="aspiration reveal">

        <div class="section-label">
            // STUDENT VOICE
        </div>

        <h2>
            Sampaikan Aspirasi
        </h2>

        <p>

            Punya ide untuk program kerja OSIS?
            Ingin memberikan masukan mengenai kegiatan
            yang sudah terlaksana?

            Sampaikan aspirasi kamu melalui formulir
            berikut agar dapat menjadi bahan evaluasi
            dan pengembangan program kerja OSIS.

        </p>


        <!--
            GANTI LINK DI BAWAH INI DENGAN
            LINK GOOGLE FORM ASPIRASI OSIS KAMU
        -->

        <a
            href="https://forms.google.com/"
            target="_blank"
            class="btn btn-gold"
        >

            💬 BUKA FORM ASPIRASI →

        </a>

    </div>

</section>



<!-- =====================================================
     GALERI
===================================================== -->

<section id="galeri">

    <div class="section-heading reveal">

        <div class="section-label">
            // DOCUMENTATION
        </div>

        <h2>
            Galeri Kegiatan
        </h2>

        <p>
            Dokumentasi kegiatan OSIS SMA Negeri 1 Tanjung.
        </p>

    </div>


    <div class="gallery">


        <div class="gallery-item reveal">

            <img
                src="images/kegiatan1.jpg"
                alt="Kegiatan OSIS"
            >

            <div class="gallery-label">
                OSIS ACTIVITY
            </div>

        </div>


        <div class="gallery-item reveal">

            <img
                src="images/kegiatan2.jpg"
                alt="Kegiatan sekolah"
            >

            <div class="gallery-label">
                EVENT
            </div>

        </div>


        <div class="gallery-item reveal">

            <img
                src="images/kegiatan3.jpg"
                alt="Dokumentasi kegiatan"
            >

            <div class="gallery-label">
                COLLABORATION
            </div>

        </div>


        <div class="gallery-item reveal">

            <img
                src="images/kegiatan4.jpg"
                alt="Kegiatan siswa"
            >

            <div class="gallery-label">
                STUDENT
            </div>

        </div>


        <div class="gallery-item reveal">

            <img
                src="images/kegiatan5.jpg"
                alt="Dokumentasi OSIS"
            >

            <div class="gallery-label">
                MOMENT
            </div>

        </div>
        <div class="gallery-item reveal">

            <img
                src="images/kegiatan5.jpg"
                alt="Dokumentasi OSIS"
            >

            <div class="gallery-label">
                MOMENT
            </div>

        </div>

    </div>

</section>



<!-- =====================================================
     FOOTER
===================================================== -->

<footer>

    <div class="footer-container">

        <div class="footer-brand">

            <strong>
                OSIS SMA NEGERI 1 TANJUNG
            </strong>

            <p>
                Bersama • Berkarya • Berintegritas
            </p>

            <p>
                © 2026 OSIS SMA Negeri 1 Tanjung
            </p>

        </div>


        <div class="footer-code">

            SYSTEM_STATUS : ONLINE<br>

            ORGANIZATION : OSIS<br>

            DIVISIONS : 10<br>

            STRUCTURE : ACTIVE

        </div>

    </div>

</footer>



<button id="topButton">
    ↑
</button>



<script>

/* =====================================================
   MOBILE MENU
===================================================== */

const menuButton =
    document.getElementById("menuButton");

const navMenu =
    document.getElementById("navMenu");


menuButton.addEventListener("click", () => {

    navMenu.classList.toggle("active");

    menuButton.textContent =
        navMenu.classList.contains("active")
            ? "✕"
            : "☰";

});


document.querySelectorAll(".nav-menu a")
.forEach(link => {

    link.addEventListener("click", () => {

        navMenu.classList.remove("active");

        menuButton.textContent="☰";

    });

});



/* =====================================================
   SCROLL REVEAL
===================================================== */

const observer =
    new IntersectionObserver(

        entries => {

            entries.forEach(entry => {

                if(entry.isIntersecting){

                    entry.target.classList.add("active");

                }

            });

        },

        {
            threshold:.12
        }

    );


document.querySelectorAll(".reveal")
.forEach(element => {

    observer.observe(element);

});



/* =====================================================
   BACK TO TOP
===================================================== */

const topButton =
    document.getElementById("topButton");


window.addEventListener("scroll", () => {

    if(window.scrollY > 500){

        topButton.classList.add("show");

    }else{

        topButton.classList.remove("show");

    }

});


topButton.addEventListener("click", () => {

    window.scrollTo({

        top:0,

        behavior:"smooth"

    });

});



/* =====================================================
   SEARCH PENGURUS
===================================================== */

const search =
    document.getElementById("search");


search.addEventListener("input", () => {

    const query =
        search.value
        .toLowerCase()
        .trim();


    document
    .querySelectorAll(".position, .sie")
    .forEach(card => {

        const text =
            card.textContent
            .toLowerCase();


        if(
            query === "" ||
            text.includes(query)
        ){

            card.style.display="";

        }else{

            card.style.display="none";

        }

    });

});



/* =====================================================
   IMAGE FALLBACK
===================================================== */

document
.querySelectorAll("img")
.forEach(img => {

    img.addEventListener("error", function(){

        this.style.opacity=".18";

    });

});

</script>

</body>
</html>
