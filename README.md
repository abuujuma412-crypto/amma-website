<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>

<title>AMMA | Africa Massive Movement Alliance</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
scroll-behavior:smooth;
}

body{
background:#050816;
color:white;
overflow-x:hidden;
}

/* NAVBAR */
nav{
width:100%;
padding:20px 8%;
display:flex;
justify-content:space-between;
align-items:center;
position:fixed;
top:0;
left:0;
z-index:1000;
background:rgba(0,0,0,0.4);
backdrop-filter:blur(10px);
}

.logo{
font-size:30px;
font-weight:800;
background:linear-gradient(90deg,#00e5ff,#00ff99);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
}

nav ul{
display:flex;
gap:25px;
list-style:none;
}

nav ul li a{
text-decoration:none;
color:white;
font-size:15px;
}

/* HERO */
.hero{
height:100vh;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
padding:20px;
background:
linear-gradient(rgba(0,0,0,0.7),rgba(0,0,0,0.8)),
url('https://i.postimg.cc/J42SXMkr/Whats-App-Image-2026-03-10-at-20-23-52-845x684.jpg');
background-size:cover;
background-position:center;
}

.hero h1{
font-size:60px;
font-weight:800;
line-height:1.2;
margin-bottom:20px;
}

.changing-text{
background:linear-gradient(90deg,#00e5ff,#00ff99,#ffcc00,#ff00cc);
background-size:300%;
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
animation:gradient 5s infinite;
}

@keyframes gradient{
0%{background-position:0%;}
50%{background-position:100%;}
100%{background-position:0%;}
}

.fade{
animation:fadeText 1s ease-in-out;
}

@keyframes fadeText{
0%{opacity:0;transform:translateY(20px);}
100%{opacity:1;transform:translateY(0);}
}

.hero p{
max-width:750px;
font-size:20px;
line-height:1.8;
color:#ddd;
margin-bottom:35px;
}

.learn-btn{
padding:18px 45px;
border:none;
border-radius:50px;
font-size:17px;
font-weight:600;
cursor:pointer;
background:linear-gradient(90deg,#00e5ff,#00ff99);
color:#000;
transition:0.3s;
}

.learn-btn:hover{
transform:scale(1.05);
}

/* POPUP */
.popup{
position:fixed;
top:50%;
left:50%;
transform:translate(-50%,-50%) scale(0);
width:90%;
max-width:650px;
background:#0f172a;
padding:40px;
border-radius:25px;
z-index:2000;
text-align:center;
transition:0.4s ease;
border:1px solid rgba(255,255,255,0.1);
box-shadow:0 0 40px rgba(0,0,0,0.6);
}

.popup.active{
transform:translate(-50%,-50%) scale(1);
}

.popup h2{
font-size:30px;
margin-bottom:20px;
background:linear-gradient(90deg,#00e5ff,#00ff99);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
}

.popup p{
font-size:17px;
line-height:2;
color:#ccc;
margin-bottom:30px;
}

.close-btn{
padding:14px 35px;
border:none;
border-radius:50px;
background:linear-gradient(90deg,#00e5ff,#00ff99);
color:#000;
font-weight:700;
cursor:pointer;
}

/* OVERLAY */
.overlay{
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:rgba(0,0,0,0.7);
backdrop-filter:blur(5px);
z-index:1500;
display:none;
}

.overlay.active{
display:block;
}

/* SECTIONS */
section{
padding:60px 10%;
}

.section-title{
font-size:46px;
margin-bottom:18px;
text-align:center;
background:linear-gradient(90deg,#00e5ff,#00ff99);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
}

.content{
max-width:1100px;
margin:auto;
text-align:center;
}

.content p{
font-size:18px;
line-height:2;
color:#ccc;
margin-bottom:15px;
}

.learn-more{
display:inline-block;
margin-top:20px;
padding:14px 35px;
border-radius:50px;
background:linear-gradient(90deg,#00e5ff,#00ff99);
color:#000;
font-weight:700;
cursor:pointer;
border:none;
}

/* CARDS */
.cards{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:20px;
margin-top:35px;
}

.card{
background:#111827;
padding:28px;
border-radius:20px;
border:1px solid rgba(255,255,255,0.08);
transition:0.3s;
}

.card:hover{
transform:translateY(-8px);
}

.card h3{
color:#00ff99;
margin-bottom:10px;
}

.card p{
font-size:14px;
color:#ccc;
line-height:1.8;
}

/* CTA */
.cta{
text-align:center;
background:linear-gradient(135deg,#00e5ff,#00ff99);
color:#000;
padding:80px 20px;
}

.cta h2{
font-size:45px;
margin-bottom:15px;
font-weight:800;
}

.cta p{
font-size:18px;
margin-bottom:25px;
}

.cta a{
display:inline-block;
padding:18px 45px;
border-radius:50px;
background:#000;
color:#fff;
text-decoration:none;
font-weight:600;
}

/* FOOTER */
footer{
padding:25px;
text-align:center;
background:#020617;
color:#888;
font-size:14px;
}

/* MOBILE */
@media(max-width:768px){

.hero h1{
font-size:38px;
}

.section-title{
font-size:30px;
}

nav ul{
display:none;
}

.popup{
padding:25px;
}

.popup h2{
font-size:24px;
}

}

</style>
</head>

<body>

<!-- OVERLAY -->
<div class="overlay" id="overlay"></div>

<!-- NAV -->
<nav>

<div class="logo">AMMA</div>

<ul>
<li><a href="#business">Business</a></li>
<li><a href="#problems">Problems</a></li>
<li><a href="#about">About</a></li>
<li><a href="#mission">Mission</a></li>
<li><a href="#vision">Vision</a></li>
</ul>

</nav>

<!-- HERO -->
<section class="hero">

<h1>
LIVE YOUR LIFE WITH <br>
<span id="changingWord" class="changing-text fade">PASSION</span>
</h1>

<p>
Learn how people are positioning themselves for growth, income, and a better future
</p>

<button class="learn-btn" onclick="openPopup('heroPopup')">
About AMMA
</button>

</section>

<!-- HERO POPUP -->
<div class="popup" id="heroPopup">

<h2>
A SYSTEM DESIGNED TO TURN YOUR VISION INTO REALITY
</h2>

<p>
AMMA exists to help people who want a better financial life but don’t know where to start. We provide guidance, support, and access to modern digital opportunities in a simple way anyone can understand.
</p>

<button class="close-btn" onclick="closePopup('heroPopup')">
CLOSE
</button>

</div>

<!-- BUSINESS -->
<section id="business">

<h2 class="section-title">
The Rise Of The Modern Digital Economy
</h2>

<!-- VIDEO SECTION -->
<div class="video-container">

<iframe
width="100%"
height="500"
src="https://www.youtube.com/embed/s5IctIYIMK0?autoplay=1&mute=1&loop=1&playlist=s5IctIYIMK0&controls=0&modestbranding=1&rel=0"
frameborder="0"
allow="autoplay; encrypted-media"
allowfullscreen>
</iframe>

</div>

<div class="content">

<p>
The rise of the modern digital economy is reshaping how people live, work, and create income. The world is gradually shifting from traditional systems to digital systems, where online platforms, technology, and social media are becoming powerful tools for opportunity and growth.
Many people in Africa are still struggling financially because they are relying only on old traditional ways of earning income, while the world is rapidly moving from analog to digital.
This shift has created a new path for those who are ready to adapt, learn, and take action.
And this is where the real opportunity begins.
</p>

</div>

</section>

<!-- PAIN POINTS -->
<section id="problems">

<h2 class="section-title">
Why Things Don't Change For Many People
</h2>

<div class="cards">

<div class="card">
<h3>Limited Opportunities</h3>
<p>
Many people struggle to access opportunities that can improve their financial future.
</p>
</div>

<div class="card">
<h3>The Cycle Never Breaks</h3>
<p>
Most people are stuck not because they are not trying, but because they are starting from zero every generation instead of building legacy
</p>
</div>

<div class="card">
<h3>Effort Without The Right Systems</h3>
<p>
Others leave home in search of opportunity, but face distance, pressure, and struggles along the way.
In both cases, effort is there but results often feel limited.
</p>
</div>

<div class="card">
<h3>One Source Of Income</h3>
<p>
Depending on one paycheck has become risky in today's economy.
</p>
</div>

<div class="card">
<h3>Lack Of Financial Education</h3>
<p>
Most people are never taught how modern income systems work.
</p>
</div>

<div class="card">
<h3>Survival Mindset</h3>
<p>
Many people are focused only on surviving instead of building long-term growth and freedom.
</p>
</div>

</div>

<div class="content">

<p>
All these challenges create a cycle that keeps many people in the same place, working hard but moving without direction and starting over again and again.
But change begins when awareness meets a different path.
This is where a new way forward begins a system designed to help people break the cycle and start building with direction, structure, and purpose.
</p>

</div>

</section>

<!-- ABOUT -->
<section id="about">

<h2 class="section-title">
What Is AMMA?
</h2>

<div class="content">

<p>
AMMA (Africa Massive Movement Alliance) is a digital empowerment movement helping people understand modern income opportunities in today’s connected world.
It is for anyone looking for a better financial direction or extra income.
Whether you are doing well, struggling, or just looking for a side hustle.
</p>

<button class="learn-more" onclick="openPopup('aboutPopup')">
The AMMA Movement
</button>

</div>

</section>

<!-- ABOUT POPUP -->
<div class="popup" id="aboutPopup">

<h2>
The AMMA Movement
</h2>

<p>
Focused on helping people grow through digital systems, mentorship, leadership, and modern opportunities.
AMMA gives you guidance, support, and a simple way to start without confusion or pressure. You don’t need special skills or experience, just the willingness to improve your financial life step by step.
</p>

<button class="close-btn" onclick="closePopup('aboutPopup')">
CLOSE
</button>
</div>

<!-- VIDEO SECTION -->
<div class="video-container">

<iframe
width="100%"
height="500"
src="https://www.youtube.com/embed/6DjBkcOhjVM?autoplay=1&mute=1&loop=1&playlist=6DjBkcOhjVM&controls=0&modestbranding=1&rel=0"
frameborder="0"
allow="autoplay; encrypted-media"
allowfullscreen>
</iframe>

</div>
</div
<section id="video">
<!-- WHO IS THIS FOR -->
<section id="who">

<h2 class="section-title">
Who Is This For?
</h2>

<div class="cards">

<div class="card">
<h3>Students</h3>
<p>
Young people looking for modern opportunities and financial direction.
</p>
</div>

<div class="card">
<h3>Employees</h3>
<p>
People searching for additional income and long-term financial growth.
</p>
</div>

<div class="card">
<h3>Entrepreneurs</h3>
<p>
Business-minded individuals ready to expand through digital systems.
</p>
</div>

<div class="card">
<h3>Job Seekers</h3>
<p>
Individuals looking for new ways to create opportunities in today’s economy.
</p>
</div>

<div class="card">
<h3>People In Gulf Countries</h3>
<p>
Kenyans and Africans abroad looking to build a better financial future back home.
</p>
</div>

<div class="card">
<h3>Dream Builders</h3>
<p>
Anyone ready to grow, learn, and create a better future through modern opportunities.
</p>
</div>

</div>

</section>

<!-- MISSION -->
<section id="mission">

<h2 class="section-title">
Our Mission
</h2>

<div class="content">

<p>
Our mission is to empower everyday people to break free from financial struggle by giving them access to simple digital systems, mentorship, and financial education. We exist to help people move from survival to stability, and from stability to real financial freedom no matter where they are starting from in life.
We believe that by using our business as force for good, we can positively impact 1,000,000 lives by 2030.
</p>

</div>
</section>
<!-- VISION -->
<section id="vision">

<h2 class="section-title">
Our Vision
</h2>

<div class="content">

<p>
To be a leader in our industry using our platform to raise awareness about important social and enviromental issues, make a positive impact in the world and empower individuals and communities through education and charitable initiatives.
</p>

<button class="learn-more" onclick="openPopup('visionPopup')">
OUR DREAM FOR NEW AFRICA
</button>

</div>

</section>

<!-- VISION POPUP -->
<div class="popup" id="visionPopup">

<h2>
OUR DREAM FOR NEW AFRICA
</h2>

<p>
We envision a generation of leaders, entrepreneurs, and dream builders rising from every corner of Africa, creating impact through modern digital opportunities.
</p>

<button class="close-btn" onclick="closePopup('visionPopup')">
CLOSE
</button>

</div>

<!-- WHY JOIN US -->
<div class="content">

<button class="learn-more" onclick="openPopup('solutionPopup')">
WHY JOIN US?
</button>

</div>

<!-- SOLUTION POPUP -->
<div class="popup" id="solutionPopup">

<h2>
WHY JOIN US?
</h2>

<p>
AMMA exists as a bridge into a new path of growth, clarity, and opportunity in the digital age, helping people move from confusion to direction, and from survival to purpose.
AMA is more than a system; it is a community and a family. You don’t walk alone. You are guided, supported, and mentored step by step. You learn what others are already doing.
</p>

<button class="close-btn" onclick="closePopup('solutionPopup')">
CLOSE
</button>

</div>

<!-- SOLUTION -->
<section id="community">

<h2 class="section-title">
What You Gain With AMMA
</h2>

<div class="cards">

<div class="card">
<h3>Modern Strategies</h3>
<p>
Embrace modern business strategies for growth and success.
</p>
</div>

<div class="card">
<h3>Digital Opportunities</h3>
<p>
Use online platforms to create income opportunities.
</p>
</div>

<div class="card">
<h3>Build Relationships</h3>
<p>
Develop strong networks locally and globally.
</p>
</div>

<div class="card">
<h3>Innovation</h3>
<p>
Leverage technology for expansion and growth.
</p>
</div>

<div class="card">
<h3>Free International Vacations</h3>
<p>
Top performers may qualify for international travel rewards based on performance.
</p>
</div>

<div class="card">
<h3>Daily Pay-Out System</h3>
<p>
A digital income system based on activity and engagement.
</p>
</div>

</div>

</section>
</div>
<!-- TESTIMONIALS -->
<section id="testimonials">

<h2 class="section-title">
Success Stories
</h2>

<div class="netflix-slider">

<div class="netflix-track">

<!-- CARD 1 -->
<div class="netflix-card">
<div class="image-slider">
    <img class="slide active"
src="https://i.postimg.cc/FzpSyX3d/Whats-App-Image-2026-03-16-at-09-38-11-495x400.jpg">
<img src="https://i.postimg.cc/SRd96bCs/Whats-App-Image-2026-03-16-at-09-38-12-1-845x684.jpg">
<img src="https://i.postimg.cc/3x5B3Y92/Whats-App-Image-2026-03-16-at-09-38-12-3-845x684.jpg">
<img src="https://i.postimg.cc/4ystHx7c/Whats-App-Image-2026-03-16-at-09-38-15-845x684.jpg">
<img src="https://i.postimg.cc/Z5s6CmxP/Whats-App-Image-2026-03-16-at-09-38-15-1-845x684.jpg">
<img src="https://i.postimg.cc/sxsSGgQ7/Whats-App-Image-2026-03-16-at-09-38-13-2-845x684.jpg">
</div>

<h3>ALLAN RUTO — Former Truck Turnboy</h3>
<p>“I used to be a long-distance truck turnboy—days and nights on the road, little sleep, little pay, and no real progress.

Life felt like a journey with no destination.

Then I found the Bonan Vivon Project.

I didn’t have connections. I didn’t have experience. But I was tired of the same cycle.

So I gave it a shot.

At first, it was slow—but I stayed consistent. I learned. I pushed through doubt.

And things began to change.

The small wins turned into real income. The struggle turned into growth. And for the first time, I wasn’t just moving—I was progressing.

Today, I’m no longer chasing miles just to survive.

I’m building a life with direction, freedom, and purpose.

Bonan Vivon didn’t just change my work.

It changed where my life is headed..”</p>

</div>

<!-- CARD 2 -->
<div class="netflix-card">
<div class="image-slider">
<img src="https://i.postimg.cc/SjbFqHJD/Whats-App-Image-2026-03-11-at-18-00-00-4-1-845x684.jpg">
<img src="https://i.postimg.cc/wjKL82F9/Whats-App-Image-2026-03-11-at-18-00-01-2-773x1030.jpg">
<img src="https://i.postimg.cc/ncVw9vDG/Whats-App-Image-2026-03-11-at-18-00-00-4-824x1030.jpg">
<img src="https://i.postimg.cc/qMH86066/Whats-App-Image-2026-03-11-at-17-59-58-845x684.jpg">
<img src="https://i.postimg.cc/qMr3MLW3/Whats-App-Image-2026-03-11-at-18-00-00-1-845x684.jpg">
<img src="https://i.postimg.cc/mkj2rQF5/Whats-App-Image-2026-03-11-at-17-59-59-1-845x684.jpg">
<img src="https://i.postimg.cc/nztHYd4R/Whats-App-Image-2026-03-11-at-17-59-59-845x684.jpg">
<img src="https://i.postimg.cc/Njq9PxkB/Whats-App-Image-2026-03-11-at-18-00-00-3-773x1030.jpg">
</div>

<h3>KEVIN NYAMAI — Graduate of Procurement</h3>
<p>“As a graduate of Procurement from Egerton University, I had high hopes after finishing my studies. But like many graduates, I soon realized that opportunities were limited and progress was slower than I had imagined. I wanted more for myself and for my family.

When I was introduced to Bonan Vivon, I was initially skeptical. Still, I chose to learn more instead of dismissing it.

That decision became a turning point. I began developing leadership skills, building a strong network, and creating an income stream beyond what I thought was possible at that stage of my life. Gradually, my lifestyle started to improve, and I was able to support my family better.

Bonan Vivon didn’t just change my finances — it changed my outlook on life and opened doors to a bigger future. I thank God I didn’t have to drop tonnes of CVs for just a paycheck..”</p>

</div>

<!-- CARD 3 -->
<div class="netflix-card">
<div class="image-slider">
<img src="https://i.postimg.cc/y8BtPwt8/Whats-App-Image-2026-03-10-at-23-45-32.jpg">
<img src="https://i.postimg.cc/ZqNN5MYx/Whats-App-Image-2026-03-10-at-23-44-09-845x684-(1).jpg">
<img src="https://i.postimg.cc/7PzqQrsn/Whats-App-Image-2026-03-10-at-23-44-13-686x1030.jpg">
<img src="https://i.postimg.cc/QxRxdxFq/Whats-App-Image-2026-03-10-at-23-44-10-2-845x684-(1).jpg">
<img src="https://i.postimg.cc/Y0vMtJMC/Whats-App-Image-2026-03-10-at-23-44-10-1-845x684-(1).jpg">
<img src="https://i.postimg.cc/L5gKcL3f/Whats-App-Image-2026-03-10-at-23-44-10-845x684-(1).jpg">
<img src="https://i.postimg.cc/15P1CnNQ/Whats-App-Image-2026-03-10-at-23-54-44-1-845x684-(1).jpg">
</div>

<h3>BEATRICE OWENGA— Former House Manager - Qatar</h3>
<p>“As a single mum from Kenya, I once worked as a househelp in Qatar just to provide for my family. The work was hard, the days were long, and being far from my children was one of the most painful sacrifices I had to make. I was doing my best to survive, but deep down I prayed for a better life for my family.

When I was introduced to Bonan Vivon, I was unsure at first. But I decided to stay open and give it a chance.

That decision changed my story. I began building something that gave me dignity, confidence, and a growing income. Slowly, my lifestyle began to change, and I could support my family in ways I never imagined before.

Bonan Vivon didn’t just change my life — it restored hope for me and created a brighter future for my children. This could not just be for you, but even the people around you..”</p>

</div>

<!-- CARD 4 -->
<div class="netflix-card">
<div class="image-slider">
<img src="https://i.postimg.cc/cHSGpr53/Whats-App-Image-2026-03-17-at-10-00-43-5-515x1030.jpg">
<img src="https://i.postimg.cc/25nP7C8L/Whats-App-Image-2026-03-17-at-09-28-25-2-1-845x684-(1).jpg">
<img src="https://i.postimg.cc/0NGBJZcn/Whats-App-Image-2026-03-17-at-10-01-16-3-845x684-(1).jpg">
<img src="https://i.postimg.cc/Y00nZ7kG/Whats-App-Image-2026-03-17-at-10-00-43-4-1-845x684-(1).jpg">
<img src="https://i.postimg.cc/j21gr1S2/Whats-App-Image-2026-03-17-at-10-08-47-2-1-845x684.jpg">
<img src="https://i.postimg.cc/7Z0Bpm88/Whats-App-Image-2026-03-18-at-17-19-00-2-845x684-(1).jpg">
</div>

<h3>MERCY GAKII— Former Teacher</h3>
<p>“I was a high school teacher—dedicated, consistent, but financially stuck. No matter how hard I worked, nothing really changed.

Then I came across the Bonan Vivon Project.

At first, I doubted it. It didn’t feel like “my world.” But I gave it a chance.

Slowly, things began to shift. I started earning extra income, meeting new people, and seeing possibilities I had never considered before.

For the first time, I felt in control of my future—not limited by my salary.

Bonan Vivon didn’t change who I was.”</p>

</div>

<!-- CARD 5 -->
<div class="netflix-card">
<div class="image-slider">
<img src="https://i.postimg.cc/R0QvV7ts/Whats-App-Image-2026-03-10-at-17-11-31-845x684.jpg">
<img src="https://i.postimg.cc/c4gZ8yYb/Whats-App-Image-2026-03-10-at-17-11-31-3-845x684.jpg">
<img src="https://i.postimg.cc/wjwSWwDn/Whats-App-Image-2026-03-10-at-17-11-31-6-773x1030.jpg">
<img src="https://i.postimg.cc/JnkvzmSy/Whats-App-Image-2026-03-10-at-18-23-59-773x1030.jpg">
<img src="https://i.postimg.cc/KctCXGnf/Whats-App-Image-2026-03-10-at-18-23-58-773x1030.jpg">
<img src="https://i.postimg.cc/BQsk4rpj/Whats-App-Image-2026-03-10-at-18-24-00-1-1030x579.jpg">
<img src="https://i.postimg.cc/Zq1sg20C/Whats-App-Image-2026-03-10-at-18-24-00-773x1030.jpg">
<img src="https://i.postimg.cc/6qhH8QcK/Whats-App-Image-2026-03-10-at-18-30-02-1-686x1030.jpg">
</div>
<h3>RONALD RATEMO— Former Construction Worker - QATAR</h3>
<p>“I spent years working in construction overseas in Doha, Qatar — long hours, tough conditions, and being far away from my family. The money helped, but the lifestyle was exhausting and lonely. Deep down, I knew I wanted a life where I could grow financially without sacrificing my time and relationships.

When I was introduced to Bonan Vivon, I was skeptical at first. But I decided to stay open and understand the opportunity.

That decision changed my direction. I started building something that gave me growth, flexibility, and a powerful network of like-minded people. Slowly, my lifestyle began to shift — from just working hard to building a future with purpose.

Bonan Vivon didn’t just improve my income — it gave me a new way to live and dream bigger. Coming Back home and getting back my freedom is more than what I could ask for.”</p>

</div>

<!-- CARD 6 -->
<div class="netflix-card">
<div class="image-slider">
<img src="https://i.postimg.cc/jSnFXRdN/Whats-App-Image-2026-03-11-at-01-22-13-894x1030.jpg">
<img src="https://i.postimg.cc/ydsps9hh/Whats-App-Image-2026-03-11-at-01-23-07-977x1030.jpg">
<img src="https://i.postimg.cc/sfnHCMMS/Whats-App-Image-2026-03-11-at-01-33-15.jpg">
<img src="https://i.postimg.cc/rpCgns6t/Whats-App-Image-2026-03-11-at-01-28-35.jpg">
<img src="https://i.postimg.cc/qR1wrFvB/Whats-App-Image-2026-03-11-at-01-29-53.jpg">
<img src="https://i.postimg.cc/7PQ9QjRB/Whats-App-Image-2026-03-11-at-01-25-24.jpg">
<img src="https://i.postimg.cc/TYz9TgfH/Whats-App-Image-2026-03-11-at-01-31-35.jpg">
<img src="https://i.postimg.cc/MGxmQwc7/Whats-App-Image-2026-03-11-at-14-24-33-675x1030.jpg">
</div>

<h3>MESHACK SAITABAU— Student @ MKU</h3>
<p>“As a student at Mount Kenya University, I was focused on my studies but constantly thinking about my future and finances. Like many students, I depended on limited support and wondered how life would look after graduation. When I was introduced to Bonan Vivon, I was curious but unsure. I decided to stay open and learn more instead of ignoring the opportunity. Getting involved changed my mindset. I started developing confidence, leadership skills, and an income stream while still in school. My lifestyle began to shift — from just surviving campus life to building a vision for my future. Bonan Vivon didn’t just support me financially; it helped me start designing the life I want much earlier. Now, I am one of the most celebrated young entrepreneurs in the country.””</p>
</div>
<!-- CARD 7 -->
<div class="netflix-card">
<div class="image-slider">
<img src="https://i.postimg.cc/k4Wc65sK/Whats-App-Image-2026-03-11-at-15-28-58-1-495x400-(1).jpg">
<img src="https://i.postimg.cc/J4rq0Mks/Whats-App-Image-2026-03-11-at-15-29-16-495x400-(1).jpg">
<img src="https://i.postimg.cc/4dRvggGn/Whats-App-Image-2026-03-11-at-15-29-18-1-579x1030.jpg">
<img src="https://i.postimg.cc/153GPBkt/Whats-App-Image-2026-03-11-at-15-28-56-773x1030.jpg">
<img src="https://i.postimg.cc/GmBvT2hm/Whats-App-Image-2026-03-11-at-15-29-10-773x1030.jpg">
<img src="https://i.postimg.cc/wBLJFGm0/Whats-App-Image-2026-03-11-at-15-29-14-849x1030.jpg">
<img src="https://i.postimg.cc/mD49ny3P/Whats-App-Image-2026-03-11-at-15-29-13-1-773x1030.jpg">
<img src="https://i.postimg.cc/MZdBsRn2/Whats-App-Image-2026-03-11-at-15-29-19-773x1030.jpg">
<img src="https://i.postimg.cc/K8ggvHJn/Whats-App-Image-2026-03-11-at-15-29-09-1-773x1030.jpg">
<img src="https://i.postimg.cc/3R9kc5xT/Whats-App-Image-2026-03-11-at-15-29-07-773x1030.jpg">
</div>

<h3>JOSEPHINE KINOTI</h3>
<p>“As a hotelier, I spent years in a fast-paced environment — long shifts, constant pressure, and little time to think about my own future. I loved serving people, but I often wondered if there was more I could build for myself beyond the hotel walls.

When I was introduced to Bonan Vivon, I was skeptical at first. But I chose to stay open and understand the opportunity.

That decision changed my path. I began building confidence, leadership, and an income stream that wasn’t tied to shifts or schedules. Slowly, my vision for the future became bigger and clearer.

Bonan Vivon didn’t just change my life — it gave me the belief and platform to design a better future. I have seen my dreams unfold before my eyes. Soon as I completed my mom’s house, I was able to buy a Voxswagen. And more is on the way.”</p>
</div>

</div>

<!-- VIDEO SECTION -->
<div class="video-container">

<iframe
width="100%"
height="500"
src="https://www.youtube.com/embed/b36PwyWyb68?autoplay=1&mute=1&loop=1&playlist=b36PwyWyb68&controls=0&modestbranding=1&rel=0"
frameborder="0"
allow="autoplay; encrypted-media"
allowfullscreen>
</iframe>

</div>
<section>

<!-- FAQ -->
<section id="faq">

<h2 class="section-title">
Frequently Asked Questions
</h2>

<div class="cards">

<div class="card">
<h3>Do I Need Experience?</h3>
<p>
No. You only need the willingness to learn and grow step by step.
</p>
</div>

<div class="card">
<h3>Can I Start Part Time?</h3>
<p>
Yes. Many people start while working or studying.
</p>
</div>

<div class="card">
<h3>Is This A Job?</h3>
<p>
No. It is a digital empowerment and business opportunity platform.
</p>
</div>

<div class="card">
<h3>How Do I Learn More?</h3>
<p>
Simply click the WhatsApp button below and speak with our team directly.
</p>
</div>
</section>

<!-- CTA -->
<section class="cta">

<h2>
START YOUR JOURNEY TODAY
</h2>

<p>
Click below to learn how AMMA works on WhatsApp.
</p>

<a href="https://wa.link/qh52o8" target="_blank">
JOIN VIA WHATSAPP
</a>

</section>

<!-- FOOTER -->
<footer>
© 2026 AMMA — Africa Massive Movement Alliance
</footer>

<script>

/* CHANGING WORDS */

const words=["PASSION","VISION","PURPOSE"];
let i=0;

setInterval(()=>{

const word=document.getElementById("changingWord");

word.classList.remove("fade");

setTimeout(()=>{

i=(i+1)%words.length;

word.innerHTML=words[i];

word.classList.add("fade");

},300);

},2500);

/* POPUPS */

function openPopup(id){

document.getElementById(id).classList.add("active");
document.getElementById("overlay").classList.add("active");

}

function closePopup(id){

document.getElementById(id).classList.remove("active");
document.getElementById("overlay").classList.remove("active");

}

</script>

</body>
</html>
