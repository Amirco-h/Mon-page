<!DOCTYPE html>
<html lang="French">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!--<link rel="stylesheet" href="style.css"> -->
  <link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel="stylesheet"> 
  <title> AmirPersonalpageweb</title>
</head> 
<!--hedear design-->

<style>
  @import url('https://fonts.googleapis.com/css2?family=Fira+Sans:ital,wght@1,900&family=Poppins:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
*{ 
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    text-decoration: none;
    border: none;
    outline: none;
    scroll-behavior:smooth;
    font-family: 'Poppins', sans-serif;
}
:root {
    --bg-color: #081b29;
    --second-bg-color:#112e42;
    --text-color: #ededed;
    --main-color: #00abf0;
}
html {
    font-size: 62.5%;
    overflow: auto;
}

body {
    background: var(--bg-color);
    color: var(--text-color);
}
.header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    padding: 2rem 9%;
    background:transparent;
    display: flex;
    justify-content: space-between;
    align-items: center;
    z-index: 100;
    transition: .3s;
}
.header .sticky {
    background:var(--bg-color);
}
.logo{
    position: relative;
    font-size: 2.5rem;
    color: var(--text-color);
    text-decoration: none;
    font-weight: 600;
}
.navbar {
    position: relative;
}
.navbar a {
    font-size: 1.7rem;
    color: var(--text-color);
    font-weight: 500;
    margin-left: 3.5rem;
    transition: .3s;
}
.navbar a:hover,
.navbar a.acvtive {
    color: var(--main-color);
}
#menu-icon {
    position: relative;
    font-size: 3.6rem;
    color: var(--text-color);
    cursor: pointer;
    display: none;
}
section {
    min-height: 100vh;
    padding: 10rem 9% 2rem;
}
.home {
    display: flex;
    align-items: center;
    padding: 0 9%;
    background: url('image/image1.png');
    background-size: cover;
    background-position: center;
}
.home-content{
    max-width: 60rem;
    z-index: 99;
}

.home-content h1 {
    position: relative;
    display: inline-block;
    font-size: 5.6rem;
    font-weight: 700;
    line-height: 1.3;
}
.home-content h1 span {
    color: var(--text-color);
}
.home-content .text-animate {
    position: relative;
    width: 32.8rem;
}
.home-content .text-animate h3 {
    font-size: 3.2rem;
    font-weight: 700;
    color: transparent;
    -webkit-text-stroke: .7px var(--main-color); 
    background-image: linear-gradient(var(--main-color), var(--main-color));
    background-repeat: no-repeat; 
    -webkit-background-clip: text;
    -o-background-clip: text;
    -moz-background-clip: text;
    -ms-background-clip: text;
    background-clip: text;
    background-position: -33rem 0;
    animation: homeBText 6s linear infinite;
    animation-delay: 2s;

}
.home-content .text-animate h3::before {
    content:'';
    position: absolute;
    top: 0;
    left: 0;
    width: 0;
    height: 100%;
    border-right: 2px solid var(--main-color);
    z-index: -1;
    animation: homeCursorText 6s linear infinite;
    animation-delay: 2s;
}
.home-content p {
    position: relative;
    font-size: 1.6rem;
    margin: 2rem 0 4rem;
    
}
.btn-box {
    position: relative;
    display: flex;
    justify-content: space-between;
    width: 34.5rem;
    height: 5rem;
}
.btn-box .btn {
    position: relative;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    width: 15rem;
    height: 100%;
    background: var(--main-color);
    border: .2rem solid var(--main-color);
    border-radius: .8rem;
    font-size: 1.8rem;
    font-weight: 600;
    letter-spacing: .1rem;
    color: var(--bg-color);
    z-index: 1;
    overflow: hidden;
    transition: .5s;
}
.btn-box .btn:hover{
    color: var(--main-color);
}
.btn-box .btn:nth-child(2) {
    background: transparent;
    color: var(--main-color);
}
.btn-box .btn:nth-child(2)::before{
    background: var(--main-color);
}
.btn-box .btn:nth-child(2):hover{
    color: var(--bg-color);
}
.btn-box .btn::before{
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 0;
    height: 100%;
    background: var(--bg-color);
    z-index: -1;
    transition: .5s;
}
.btn-box .btn:hover:before{
    width: 100%;
}
.home-sci {
    position: absolute;
    bottom: 4rem;
    width: 170px;
    display: flex;
    justify-content: space-between;
}
.home-sci a {
    position: relative;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    width: 40px;
    height: 40px;
    background: transparent;
    border: .2rem solid var(--main-color);
    border-radius: 50%;
    font-size: 30px;
    color: var(--main-color);
    z-index: 1;
    overflow: hidden;
    transition: .5s;
}
.home-sci a :hover{
    color: var(--bg-color);
    
}
.home-sci a::before{
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    height: 0;
    width: 0;
    height: 100%;
    background: var(--main-color);
    z-index: -1;
    transition: .5s;
}
.home-sci a:hover::before{
    width: 100%;
}
.home-imgHover {
    position: absolute;
    top: 0;
    right: 0;
    width: 45%;
    height: 100%;
    background: transparent;
    transition: .3s;
}
.home-imgHover:hover {
    background: none;
    opacity: none;
}

.about {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    gap: 2rem;
    background: var(--second-bg-color);
    padding-bottom: 6rem;
}
.heading {
    position: relative;
    font-size: 5rem;
    margin-bottom: 3rem;
    text-align: center;
}
span {
    color: var(--main-color);
}
.about-img {
    position: relative;
    width: 25rem;
    height: 25rem;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    
}
.about-img img {
    width: 90%;
    border-radius: 50%;
    border: .2rem solid var(--main-color);
}

.about-img .circle-spin  {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) rotate(0);
    width: 100%;
    height: 100%;
    border-radius: 50%;
    border-top: .2rem solid var(--second-bg-color);
    border-bottom: .2rem solid var(--second-bg-color);
    border-left: .2rem solid var(--main-color);
    border-right: .2rem solid var(--main-color);
    animation: aboutSpinner 5s linear infinite;
}
.about-img .circle-spin1  {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) rotate(0);
    width: 110%;
    height: 110%;
    border-radius: 50%;
    border-top: .2rem solid var(--second-bg-color);
    border-bottom: .2rem solid var(--second-bg-color);
    border-left: .2rem solid var(--main-color);
    border-right: .2rem solid var(--main-color);
    animation: aboutSpinne 8s linear infinite;
}
.about-img .circle-spin2  {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) rotate(0);
    width: 120%;
    height: 120%;
    border-radius: 50%;
    border-top: .2rem solid var(--second-bg-color);
    border-bottom: .2rem solid var(--second-bg-color);
    border-left: .2rem solid var(--main-color);
    border-right: .2rem solid var(--main-color);
    animation: aboutSpinner 3s linear infinite;
}
.about-content {
    text-align: center;
}
.about-content h3 {
    font-size: 2.6rem;
}
.about-content p {
    font-size: 1.6rem;
    margin: 2rem 0 3rem;
}
.btn-box.btns {
    display: inline-block;
    width: 15rem;
}
.btn-box.btns a::before {
    background: var(--second-bg-color);
}
.education {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    min-height: auto;
    padding-bottom: 5rem;
    background: var(--second-bg-color);
}
.education .education-row {

    display: flex;
    flex-wrap: wrap;
    gap: 5rem;

}
.education-row .education-column {
    flex: 1 1 40rem;
}

.education-column .title {
    font-size: 2.5rem;
    margin: 0 0 1.5rem 2rem;
}

.education-column .education-box {
    border-left: .2rem solid var(--main-color);
}

.education-box .education-content {
    position: relative;
    padding: 2rem;
}

.education-box .education-content::before {
    content: '';
    position: absolute;
    top: 0;
    left: -1.1rem;
    width: 2rem;
    height: 2rem;
    background: var(--main-color);
    border-radius: 50%;
}


.education-content .content {
    position: relative;
    padding: 1.5rem;
    border: .2rem solid var(--main-color);
    border-radius: .6rem;
    margin-bottom: 2rem;
    overflow: hidden;
    
}

.education-content .content::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 0;
    height: 100%;
    background: var(--second-bg-color);
    z-index: -1;
    transition: .5s;
}
.education-content .content:hover::before {
    width: 100%;
}

.education-content .content .year {
    font-size: 1.5rem;
    color: var(--main-color);
    padding-bottom: .5rem;
}

.education-content .content i {
    padding-right: .5rem;
}

.education-content .content h3 {
    font-size: 2rem;
}

.education-content .content p {
    font-size: 1.6rem;
    padding-top: .5rem;
}
.skills {
    min-height: auto;
    padding-bottom: 7rem;
    background: var(--second-bg-color);
}

.skills .skills-row {
    display: flex;
    flex-wrap: wrap;
    gap: 5rem;
}

.skills-row .skills-column {
    flex: 1 1 40rem;
}

.skills-column .title {

   font-size: 2.5rem;
   margin: 0 0 1.5rem;
}

.skills-box .skills-content {
    position: relative;
    border: .2rem solid var(--main-color);
    border-radius: .6rem; 
    padding: .5rem 1.5rem;
    overflow: hidden;
    z-index: 1;
}

.skills-box .skills-content::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 0;
    height: 100%;
    background: var(--bg-color);
    z-index: -1;
    transition: .5s;
}
.skills-box .skills-content:hover::before {
    width: 100%;
}
.skills-content .progress {
    padding: 1rem 0;
}
.skills-content .progress h3 {
    font-size: 1.7rem;
    display: flex;
    justify-content: space-between;
}

.skills-content .progress h3 span {
    color: var(--text-color);
}
.skills-content .progress .bar {
    height: 2.5rem;
    border-radius: .6rem;
    border: .2rem solid var(--main-color);
    padding: .5rem;
    margin: 1rem 0;
}
.skills-content .progress .bar span {
    display: block;
    height: 100%;
    border-radius: .3rem;
    background: var(--main-color);
}
.skills-column:nth-child(1) .skills-content .progress:nth-child(1) .bar span {
    width: 84%;
}
.skills-column:nth-child(1) .skills-content .progress:nth-child(2) .bar span {
    width: 57%;
}

.skills-column:nth-child(1) .skills-content .progress:nth-child(3) .bar span {
    width: 30%;
}

.skills-column:nth-child(1) .skills-content .progress:nth-child(4) .bar span {
    width: 50%;
}

.skills-column:nth-child(2) .skills-content .progress:nth-child(1) .bar span {
    width: 45%;
}
.skills-column:nth-child(2) .skills-content .progress:nth-child(2) .bar span {
    width: 50%;
}

.skills-column:nth-child(2) .skills-content .progress:nth-child(3) .bar span {
    width: 65%;
}

.skills-column:nth-child(2) .skills-content .progress:nth-child(4) .bar span {
    width: 70%;
}

/* contact design*/

.contact {
    min-height: auto;
    padding-bottom: 7rem;
}
.contact form {
    max-width: 70rem;
    margin: 0 auto;
    text-align: center;
}
.contact form .input-box {
    position: relative;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}
.contact form .input-field {
    position: relative;
    width: 49%;
    margin: .8rem 0;
}

.contact form .input-box .input-field input,
.contact form .textarea-field textarea {
    width: 100%;
    height: 100%;
    padding: 1.5rem; 
    font-size: 1.6rem;
    color: var(--text-color); 
    background: transparent; 
    border-radius: .6rem;
    border: .2rem solid var(--main-color);

}


.contact form .input-box .input-field input::placeholder,
.contact form .textarea-field textarea::placeholder {
    color: var(--text-color);
}

.contact form .focus {
    position: absolute;
    top: 0; 
    left: 0;
    width: 0;
    height: 100%;
    background: var(--second-bg-color);
    border-radius: .6rem;
    z-index: -1;
    transition: .4s;
}
.contact form .input-box .input-field input:focus~.focus, 
.contact form .input-box .input-field input:valid~.focus,
.contact form .textarea-field textarea:focus~.focus, 
.contact form .textarea-field textarea:invalid~.focus {
    width: 100%;
}

.contact form .textarea-field {
    position: relative;
    margin: .8rem 0 2.7rem;
    display: flex;
}
.contact form .textarea-field textarea {
    resize: none;
}

.contact form .btn-box.btns .btn {
    cursor: pointer;
}

/*footer design*/

.footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    padding: 2rem 9%;
    background: var(--second-bg-color);
}

.footer-text p {
    font-size: 1.6rem;
}
.footer-iconTop {
    position: relative;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    padding: .8rem;
    background: var(--main-color);
    border: .2rem solid var(--main-color);
    border-radius: .6rem;
    z-index: 1;
    overflow: hidden;
}

.footer-iconTop a::before {
    content:'';
    position: absolute;
    top: 0; 
    left: 0;
    width: 0;
    height: 100%;
    background: var(--second-bg-color);
    z-index:-1;
    transition: .4s;

}
.footer-iconTop a:hover::before {
    width: 100%;
}


.footer-iconTop a i {
    font: 2.rem;
    color: var(--bg-color);
    transition: .4s;
}
/* animation reload and scroll*/
.animate {
    position: absolute;
    top: 0;
    right: 0;
    width: 100%;
    height: 100%;
    background: var(--bg-color);
    z-index: 98;
}

.animate.home-img {
    width: 50%;
}
.logo .animate,
.navbar .animate,
#menu-icon .animate,
.home.show-animate .animate {
    animation: showRight 1s ease forwards;
    animation-delay: calc(.3s * var(--i));
}

.animate .scroll {
    animation:  1s ease;
    animation-delay: calc(.3s / var(--i));
    
}

.about .show-animate .animate .scroll {
    transition-delay: calc(.3s * var(--i));
    width: 0;
}

.footer-iconTop a:hover i {
    color: var(--main-color);
}
/* breack point*/
@media (max-width: 1200px) {
    html{
        font-size: 55%;
    }
}
@media (max-width: 991px) {
    .header {
        padding: 2rem 4%;

    }
    section {
        padding: 10rem 4% 2rem;
    }
    .home {
        padding: 0 4%;

    }
    .footer {
        padding: 2rem 4%;
    }

}
@media (max-width: 768px) {
    .header {
        background: var(--bg-color);
    }
    #menu-icon {
        display: block;
    }
    .navbar {
        position: absolute;
        top: 100%;
        left: -100%;
        width: 100%;
        padding: 1rem 4%;
        background: var(--main-color);
        box-shadow: 0 .5rem 1rem rgba(0, 0, 0, .2);
        z-index: 1;
        transition: .25s ease;
        transition-delay: .25s;
    }
    .navbar.active {
        left: 0;
        transition-delay: 0s;
          
    }
    .navbar .active-nav {
        position: absolute;
        top: 0;
        left: -100%;
        width: 100%;
        height: 100%;
        background: var(--bg-color);
        border-top: .1rem solid rgba(0, 0, 0, .2);
        z-index: -1;
        transition: .25s ease; 
        transition-delay: 0s;
    }
    .navbar.active .active-nav {
        left: 0;
        transition-delay: .25s;
    }
    .navbar a {
        display: block;
        font-size: 2rem;
        margin: 3rem 0;
        transform: translateX(-20rem);
        transition: .25s ease;
        transition-delay: 0s;
        
    }
    .navbar.active a {
        transform: translateX(0); 
        transition-delay: .25s;
    }
   

    .home-imgHover {
        pointer-events: none;
        background: var(--bg-color);
        opacity: .6;
    }

}

@media (max-width: 520px) {
    html{
        font-size: 50%;
    }
    .home-content h1 {
        display: flex;
        flex-direction: column;
    }
    .home-sci {
        width: 160px;
    }

    .home-sci a {
        width: 38px;
        height: 38px;
    }

}

@media (max-width: 462px) {
    .home-content h1 {
    font-size: 5.2rem;
    }
    .education {
        padding: 10rem 4% 5rem 5%;
    }
    .contact form .input-box .input-field{
        width: 100%;

    }
    .footer {
        flex-direction: column-reverse;
    }
    .footer p {
        margin-top: 2rem;
        text-align: center;
    }
}
@media (max-width: 371px) {
    .home {
        justify-content: center;
    }
    .home-content{
        display: flex;
        align-items: center;
        flex-direction: column;
        text-align: center;
    }
    .home-content h1 {
        font-size: 5rem;
    }
}
@keyframes homeBText {
    0%, 
    10%, 
    100% {
        background-position: -33rem 0;
    }

    65%, 
    85%  {
        background-position: 0 0;
    }
}
@keyframes homeCursorText {
    0%,
    10%,
    100% {
        width: 0;
    }

    65%,
    78%,
    85% {
        width: 100%;
        opacity: 1;
    }

    75%,
    85% {
        opacity: 0;
    }
    
}

@keyframes aboutSpinner {
    100% {
        transform: translate(-50%, -50%) rotate(360deg);
    }

}
@keyframes aboutSpinne {
    100% {
        transform: translate(-50%, -50%) rotate(-360deg);
    }

}


@keyframes showRight {
    100% { 
        
        width: 0;
    }
}







</style>
<body>

  <header class="header">
    <a href="#" class="logo">Amir.<span class="animate" style="--i:1;"></span></a>
     <div class="bx bx-menu" id="menu-icon"> <span class="animate" style="--i:2;"></span></div>
  
    <nav class="navbar">
      <a href="#home" class="acvtive">Home</a>
      <a href="#about" >About</a>
      <a href="#education" >Education</a>
      <a href="#skills" >Skills</a>
      <a href="#contact" >Contact</a>
      
      <span class="active-nav"></span>
      <span class="animate" style="--i:2;"></span>
    </nav>
  </header>
  <!-- home section  design-->
  <section class="home show-animate" id="home">
    <div class="home-content">
      <h1>Salut,c'est <span>Amir hissein</span><span class="animate" style="--i:2;"></span></h1>
      <div class="text-animate">
        <h3> Swift &UI ios App Developer</h3>
        <span class="animate" style="--i:3;"></span>
      </div>
      <p>Through this page, I would like to present my little experience on web development and many others.  <span class="animate" style="--i:4;"></span></p>
       
      <div class="btn-box">
        <a href="#" class="btn">Hire Me</a>
        <a href="#" class="btn">Let's Talk</a>
        <span class="animate" style="--i:5;"></span>
      </div>
    </div>
    <div class="home-sci">
      <a href="https://www.facebook.com/amir.hisseinabakar"><i class="bx bxl-facebook"></i></a>
      <a href="https://twitter.com/Amir_officiel97"><i class="bx bxl-twitter"></i></a>
      <a href="https://www.linkedin.com/in/amir-hissein-abakar-b739a9251/?lipi=urn%3Ali%3Apage%3Ad_flagship3_feed%3B3j1g3v33Suy%2FEMKJ6kx0kw%3D%3D"><i class="bx bxl-linkedin"></i></a>
      <a href="https://www.instagram.com/amir_officiel_____97dk/"><i class="bx bxl-instagram-alt"></i></a>
      <span class="animate" style="--i:6;"></span>
    </div>
    <div class="home-imgHover"></div>
    <span class="animate home-img" style="--i:7;"></span>
  </section>
  
  <!-- about section  design-->

  <section class="about" id="about">
    <h2 class="heading"> About <span> Me </h2>
    <div class="about-img">
      <img src="image/image2.jpg" alt="">
      <span class="circle-spin"></span>
      <span class="circle-spin1"></span>
      <span class="circle-spin2"></span>
    </div>

    <div class="about-content">
      <h3>Mobile App Developer </h3>
      <p>Hi, my name is Amir Hissein Abakar; Computer engineering student at the University of Tekirdağ Namik kemal....</p>
      <div class="btn-box btns">
        <a href="#education" class="btn">Read more</a>
      </div>
    </div>
  </section>
    <!-- education section  design-->
  <section class="education" id="education">
    <h2 class="heading"> My <span>Journey</span></h2>

    <div class="education-row">
      <div class="education-column">
        <h3 class="title">Education</h3>

        <div class="education-box">

          <div class="education-content">
            <div class="content">
              <div class="year"><i class="bx bxs-calendar"></i>2006-2012</div>
              <h3>My primary studies</h3>
              <p>I attended the Alnahada and Spoir schools in Abéché.</p> 
            </div>
          </div>

          <div class="education-content">
            <div class="content">
              <div class="year"><i class="bx bxs-calendar"></i>2012-2019</div>
              <h3>My secondary studies</h3>
              <p>I attended Cheik Hamdan ben-rachid high school and hissein Mahamat itno bilingual high school in Abéché.</p> 
            </div>
          </div>

          <div class="education-content">
            <div class="content">
              <div class="year"><i class="bx bxs-calendar"></i>2012-202..</div>
              <h3>My university studies</h3>
              <p>Currently studying at namik kemal university in tekirdağ in turkey, in engineering-computer science.</p> 
            </div>
          </div>

        </div>
      </div>

      <div class="education-column">
        <h3 class="title">Language and hobbies</h3>

        <div class="education-box">

          <div class="education-content">
            <div class="content">
              <div class="year"><i class="bi bxs-shield-plus"></i>Language </div>
              <h3>French and arabic </h3>
              <p><b>French :</b> speak and write very well. <br><b>Arabic : </b>speak and write very well.</p> 
            </div>
          </div>

          <div class="education-content">
            <div class="content">
              <div class="year"><i class="bi bxs-shield-plus"></i>Language</div>
              <h3>Turkish and english </h3>
              <p><b>Turkish :</b> speak and write well. <br><b>English : </b>speak and write moderately.</p> 
            </div>
          </div>

          <div class="education-content">
            <div class="content">
              <div class="year"><i class="bi bxs-shield-plus"></i>hobbies</div>
              <h3>Reading, coding, sports...</h3>
              <p>There are several other hobbies that I can't finish all the lists and long.</p> 
            </div>
          </div>

        </div>
      </div>
    </div>
  </section>

  <!--skills section design-->

  <section class="skills" id="skills">
    <h2 class="heading">My <span>Skills</span></h2>

    <div class="skills-row">

      <div class="skills-column">
        <h3 class="title">Coding skills</h3>

        <div class="skills-box">
          <div class="skills-content">

            <div class="progress">
              <h3>HTML & CSS & JS <span>84%</span></h3>
              <div class="bar"><span></span></div>
            </div>

            <div class="progress">
              <h3> AI <span>57%</span></h3>
              <div class="bar"><span></span></div>
            </div>

            <div class="progress">
              <h3>Python<span>30%</span></h3>
              <div class="bar"><span></span></div>
            </div>

            <div class="progress">
              <h3>SwifUI<span>50%</span></h3>
              <div class="bar"><span></span></div>
            </div>

          </div>
        </div>
      </div>

      <div class="skills-column">
        <h3 class="title">Personal skills</h3>

        <div class="skills-box">
          <div class="skills-content">

            <div class="progress">
              <h3>Web design <span>45%</span></h3>
              <div class="bar"><span></span></div>
            </div>

            <div class="progress">
              <h3>Mobile App.dev<span>50%</span></h3>
              <div class="bar"><span></span></div>
            </div>

            <div class="progress">
              <h3>Graphic Design<span>65%</span></h3>
              <div class="bar"><span></span></div>
            </div>

            <div class="progress">
              <h3>MYSQL<span>70%</span></h3>
              <div class="bar"><span></span></div>
            </div>

          </div>
        </div>
      </div>
    </div>
    
  </section>
  
  <!--contact section design-->
  <section class="contact" id="contact">
    <h2 class="heading">Contactez <span>moi! </span></h2>

    <form action="amirhisseinabakar@gmail.com">
      <div class="input-box">
        <div class="input-field">
          <input type="text" placeholder="votre Nom complet..." required>
          <span class="focus"></span>
        </div>

        <div class="input-field">
          <input type="text" placeholder="Email Adress" required>
          <span class="focus"></span>
        </div>
      </div>

      <div class="input-box">
        <div class="input-field">
          <input type="number" placeholder="numero de tele..." required>
          <span class="focus"></span>
        </div>

        <div class="input-field">
          <input type="text" placeholder="votre e-mail" required>
          <span class="focus"></span>
        </div>
       
      </div>
      
      <div class="textarea-field">
        <textarea name="" id="" cols="30" rows="10" placeholder="votre Message"></textarea>
        <span class="focus"></span>
      </div>

      <div class="btn-box btns">
        <button type="submit" class="btn">Submit</button>
      </div>
      
    </form>
  </section>
  <!--footer design-->
  <footer class="footer">
    <div class="footer-text">
      <p>copyright &copy; 2024 | All right reserved.</p>
    </div>
    <div class="footer-iconTop">
      <a href="#"><i class="bx bx-up-arrow-alt"></i></a>
    </div>
  </footer>
  <!-- src="./script.js"> --> 
  <script>
    let menuIcon = document.querySelector('#menu-icon');

let navbar = document.querySelector('.navbar');

menuIcon.onclick = ()=> {

    menuIcon.classList.toggle('bx-x');
    navbar.classList.toggle('active');
}


//scroll section
let section = document.querySelector('section');

let navLinks = document.querySelector('header nav a');

window.onscroll = ()=>{

    section.foreach(sec => {

        let top = window.scrollY;
        let offset = sec.offsetTop - 100;
        let height = sec.offsetHeight;
        let id = sec.getAttribute('id');

        if(top >= offset && top < offset + height) {
            navLinks.forEach(links => {
                links.classList.remove('active');
                document.querySelector('header nav a[href*=' + id +']').classList.add('active');
            });
            // active sections for animation on scrolL
            sec.classList.add('show-animate');
        }
        // if want to use animation that repeats on scroll use this
        else {
            sec.classList.remove('show-animate');
        }

        
    });
    
    
    let header = document.querySelector('header');
    header.classList.toggle('sticky', window.scrollY > 100);

    // remove toggle icon and navbar when click navbar Links (scroll)

    menuIcon.classList.remove('bx-x');
    navbar.classList.remove('active');

   

}
  </script>
 
</body>
</html>