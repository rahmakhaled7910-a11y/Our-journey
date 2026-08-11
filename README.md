[index.html](https://github.com/user-attachments/files/30926902/index.html)
# Our-journey

Index · HTML
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>EGY School | Student Activities</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;600;700;800;900&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --maroon-deep:#3a0e0f;
    --maroon:#5c1a1c;
    --maroon-line:#7a2a24;
    --cream:#f6efe4;
    --cream-2:#efe4d2;
    --ink:#22252f;
    --gold:#b5883a;
    --rose:#c94f4a;
  }
  *{margin:0;padding:0;box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    font-family:'Poppins',sans-serif;
    background:var(--cream);
    color:var(--ink);
    overflow-x:hidden;
  }
  h1,h2,h3,.serif{font-family:'Playfair Display',serif;}
  a{cursor:pointer;}
 
  ::selection{background:var(--gold);color:var(--cream);}
 
  .reveal{opacity:0;transform:translateY(28px);transition:opacity .8s ease, transform .8s ease;}
  .reveal.in{opacity:1;transform:translateY(0);}
 
  header{
    position:fixed;top:0;left:0;right:0;z-index:50;
    display:flex;align-items:center;justify-content:space-between;
    padding:20px 6%;
    background:rgba(58,14,15,0.88);
    backdrop-filter:blur(8px);
    border-bottom:1px solid rgba(181,136,58,0.18);
    transition:padding .3s ease, background .3s ease;
  }
  header.scrolled{padding:12px 6%;background:rgba(30,7,8,0.96);}
  .logo{
    color:var(--cream);
    font-family:'Playfair Display',serif;
    font-weight:700;
    font-size:1.35rem;
    letter-spacing:1px;
    cursor:pointer;
  }
  .logo span{color:var(--gold);}
  nav ul{list-style:none;display:flex;gap:38px;align-items:center;}
  nav a{
    color:var(--cream-2);text-decoration:none;
    font-size:.85rem;letter-spacing:.8px;font-weight:400;
    position:relative;padding-bottom:4px;
    transition:color .25s;
  }
  nav a:hover{color:var(--gold);}
  nav a::after{
    content:"";position:absolute;left:0;bottom:0;width:0;height:1px;
    background:var(--gold);transition:width .3s;
  }
  nav a:hover::after{width:100%;}
  nav .nav-cta{
    border:1px solid var(--gold);color:var(--gold);
    padding:9px 20px;border-radius:2px;letter-spacing:1px;font-size:.78rem;
    text-transform:uppercase;
  }
  nav .nav-cta::after{display:none;}
  nav .nav-cta:hover{background:var(--gold);color:var(--maroon-deep);}
 
  .hero{
    position:relative;
    min-height:100vh;
    display:flex;align-items:center;justify-content:center;
    background:var(--maroon-deep);
    overflow:hidden;
  }
  .hero::before{
    content:"";position:absolute;inset:0;
    background:radial-gradient(circle at 50% 0%, rgba(181,136,58,0.14), transparent 55%);
  }
  .hero-pattern{position:absolute;inset:0;opacity:.45;}
  .hero-pattern .arch{animation:float 8s ease-in-out infinite;}
  .hero-pattern .arch2{animation:float 10s ease-in-out infinite reverse;}
  @keyframes float{0%,100%{transform:translateY(0);}50%{transform:translateY(-14px);}}
 
  .hero-content{
    position:relative;z-index:2;text-align:center;color:var(--cream);
    padding:0 20px;max-width:920px;
  }
  .eyebrow{
    letter-spacing:5px;font-size:.78rem;color:var(--gold);
    margin-bottom:26px;text-transform:uppercase;display:inline-block;
    border-top:1px solid var(--maroon-line);border-bottom:1px solid var(--maroon-line);
    padding:9px 22px;
    opacity:0;animation:fadeUp .9s ease forwards .1s;
  }
  .hero h1{
    font-size:clamp(2.6rem,6.4vw,5.2rem);line-height:1.06;font-weight:700;
    margin-bottom:22px;opacity:0;animation:fadeUp .9s ease forwards .3s;
  }
  .hero h1 em{font-style:italic;color:var(--gold);font-weight:600;}
  .hero p.tag{
    font-size:1.08rem;color:var(--cream-2);font-weight:300;max-width:580px;
    margin:0 auto 44px;line-height:1.75;
    opacity:0;animation:fadeUp .9s ease forwards .5s;
  }
  .hero .btn-row{opacity:0;animation:fadeUp .9s ease forwards .7s;display:flex;gap:18px;justify-content:center;flex-wrap:wrap;}
  @keyframes fadeUp{from{opacity:0;transform:translateY(18px);}to{opacity:1;transform:translateY(0);}}
 
  .btn{
    display:inline-block;background:transparent;border:1px solid var(--gold);color:var(--gold);
    padding:14px 36px;font-size:.82rem;letter-spacing:2px;text-transform:uppercase;
    text-decoration:none;transition:.3s;border-radius:2px;
  }
  .btn:hover{background:var(--gold);color:var(--maroon-deep);}
  .btn.solid{background:var(--gold);color:var(--maroon-deep);border-color:var(--gold);}
  .btn.solid:hover{background:transparent;color:var(--gold);}
  .btn.ghost{border-color:var(--cream-2);color:var(--cream-2);}
  .btn.ghost:hover{border-color:var(--gold);color:var(--gold);background:transparent;}
 
  .scroll-cue{
    position:absolute;bottom:34px;left:50%;transform:translateX(-50%);
    color:var(--cream-2);font-size:.68rem;letter-spacing:3px;
    display:flex;flex-direction:column;align-items:center;gap:8px;opacity:.65;
  }
  .scroll-cue div{width:1px;height:40px;background:var(--gold);animation:pulse 1.8s ease-in-out infinite;}
  @keyframes pulse{0%,100%{opacity:.2;}50%{opacity:1;}}
 
  .strip{
    background:var(--gold);color:var(--maroon-deep);
    padding:12px 0;overflow:hidden;white-space:nowrap;
    font-size:.8rem;letter-spacing:2px;text-transform:uppercase;font-weight:600;
  }
  .strip .track{display:inline-block;animation:marquee 22s linear infinite;}
  .strip span{margin:0 26px;}
  @keyframes marquee{from{transform:translateX(0);}to{transform:translateX(-50%);}}
 
  section{padding:120px 6%;}
  .section-head{text-align:center;max-width:700px;margin:0 auto 64px;}
  .eyebrow-line{
    color:var(--maroon);letter-spacing:4px;font-size:.76rem;
    text-transform:uppercase;margin-bottom:16px;font-weight:600;
  }
  .section-head h2{font-size:clamp(2rem,4vw,2.8rem);color:var(--maroon-deep);font-weight:700;}
  .section-head p{color:#6b5f57;margin-top:16px;font-weight:300;line-height:1.75;}
 
  .about{background:var(--cream);position:relative;}
  .about-grid{
    display:grid;grid-template-columns:0.85fr 1.15fr;gap:80px;
    max-width:1180px;margin:0 auto;align-items:center;
  }
  .about-visual{position:relative;aspect-ratio:4/5;}
  .about-visual .frame-bg{
    position:absolute;inset:0;background:var(--maroon-deep);
    display:flex;align-items:center;justify-content:center;overflow:hidden;
  }
  .about-visual .frame-bg svg{width:74%;height:74%;}
  .about-visual .offset-line{
    position:absolute;top:22px;left:22px;right:-22px;bottom:-22px;
    border:1px solid var(--gold);z-index:-1;
  }
  .about-text .eyebrow-line{margin-bottom:16px;}
  .about-text h2{font-size:clamp(1.9rem,3.2vw,2.5rem);color:var(--maroon-deep);margin-bottom:22px;line-height:1.2;}
  .about-text p{color:#5a4f48;line-height:1.9;font-weight:300;margin-bottom:18px;}
  .pillars{display:grid;grid-template-columns:repeat(3,1fr);gap:28px;margin-top:36px;}
  .pillar{border-left:2px solid var(--gold);padding-left:16px;}
  .pillar .num{font-family:'Playfair Display',serif;color:var(--gold);font-size:1.7rem;font-weight:700;display:block;margin-bottom:6px;}
  .pillar .lbl{font-size:.85rem;color:var(--maroon-deep);letter-spacing:.4px;line-height:1.5;}
 
  .event{background:var(--maroon-deep);color:var(--cream);position:relative;overflow:hidden;}
  .event::before{
    content:"";position:absolute;inset:0;
    background:radial-gradient(circle at 85% 15%, rgba(181,136,58,0.12), transparent 50%);
  }
  .event-tag{text-align:center;position:relative;z-index:2;margin-bottom:60px;}
  .event-tag .eyebrow-line{color:var(--gold);}
  .event-tag h2{font-size:clamp(2.2rem,4.4vw,3.4rem);color:var(--cream);}
  .event-inner{
    max-width:1180px;margin:0 auto;position:relative;z-index:2;
    display:grid;grid-template-columns:0.85fr 1.15fr;gap:0;
    background:var(--cream);box-shadow:0 40px 90px rgba(0,0,0,.45);
  }
  .event-poster{
    background:var(--maroon-deep);border-right:1px solid var(--maroon-line);
    display:flex;flex-direction:column;align-items:center;justify-content:center;
    padding:64px 42px;position:relative;
  }
  .event-poster .corner{position:absolute;width:26px;height:26px;border:1px solid var(--gold);}
  .event-poster .c1{top:20px;left:20px;border-right:none;border-bottom:none;}
  .event-poster .c2{top:20px;right:20px;border-left:none;border-bottom:none;}
  .event-poster .c3{bottom:20px;left:20px;border-right:none;border-top:none;}
  .event-poster .c4{bottom:20px;right:20px;border-left:none;border-top:none;}
  .event-poster .frame{padding:26px 10px;text-align:center;width:100%;}
  .event-poster .kicker{letter-spacing:4px;font-size:.72rem;color:var(--gold);text-transform:uppercase;margin-bottom:22px;}
  .event-poster h3{font-size:clamp(2.2rem,3.6vw,3rem);line-height:1.15;color:var(--cream);margin-bottom:20px;}
  .event-poster .sub{font-size:.92rem;color:var(--cream-2);font-weight:300;line-height:1.75;margin-bottom:36px;padding:0 6px;}
  .date-row{display:flex;align-items:center;justify-content:center;gap:20px;margin-bottom:10px;}
  .date-block{text-align:center;}
  .date-block .small{
    font-size:.76rem;letter-spacing:2px;color:var(--gold);text-transform:uppercase;
    border-top:1px solid var(--maroon-line);border-bottom:1px solid var(--maroon-line);padding:7px 14px;
  }
  .date-block .big{font-family:'Playfair Display',serif;font-size:3.4rem;color:var(--rose);font-weight:800;line-height:1;}
  .month-year{margin-top:16px;font-size:.85rem;letter-spacing:2px;color:var(--cream-2);}
 
  .event-details{padding:70px 60px;display:flex;flex-direction:column;justify-content:center;}
  .event-details h2{font-size:clamp(1.8rem,3vw,2.4rem);color:var(--maroon-deep);margin-bottom:20px;line-height:1.25;}
  .event-details p{color:#5a4f48;line-height:1.9;font-weight:300;margin-bottom:26px;}
  .value-list{list-style:none;margin-bottom:34px;}
  .value-list li{
    display:flex;align-items:flex-start;gap:16px;padding:14px 0;border-bottom:1px solid #e2d5c4;
    font-size:.95rem;color:var(--ink);
  }
  .value-list li .mark{
    font-family:'Playfair Display',serif;color:var(--gold);font-weight:700;font-size:1.05rem;
    min-width:20px;
  }
  .value-list li b{color:var(--maroon-deep);font-weight:600;}
  .value-list li .desc{color:#6b5f57;display:block;font-size:.88rem;margin-top:2px;font-weight:300;}
  .meta-row{display:flex;gap:34px;margin-bottom:36px;flex-wrap:wrap;}
  .meta-item{font-size:.88rem;color:#5a4f48;}
  .meta-item b{display:block;color:var(--maroon-deep);font-size:.76rem;letter-spacing:1.5px;text-transform:uppercase;margin-bottom:5px;}
 
  .schedule{background:var(--cream);}
  .timeline{max-width:820px;margin:0 auto;}
  .t-item{
    display:grid;grid-template-columns:110px 1fr;gap:30px;padding:28px 0;
    border-bottom:1px solid #e2d5c4;align-items:start;
  }
  .t-item:last-child{border-bottom:none;}
  .t-time{font-family:'Playfair Display',serif;color:var(--maroon);font-weight:700;font-size:1.05rem;}
  .t-content h4{color:var(--maroon-deep);font-size:1.1rem;margin-bottom:6px;font-weight:600;}
  .t-content p{color:#6b5f57;font-size:.9rem;font-weight:300;line-height:1.7;}
 
  .activities{background:var(--cream-2);}
  .cards{display:grid;grid-template-columns:repeat(3,1fr);gap:30px;max-width:1180px;margin:0 auto;}
  .card{
    background:var(--cream);border:1px solid #e2d5c4;padding:42px 32px;text-align:left;
    position:relative;transition:transform .35s ease, box-shadow .35s ease, border-color .35s ease;
  }
  .card:hover{transform:translateY(-8px);box-shadow:0 24px 50px rgba(58,14,15,.14);border-color:var(--gold);}
  .card .icon{
    width:50px;height:50px;margin-bottom:24px;border:1px solid var(--maroon);border-radius:50%;
    display:flex;align-items:center;justify-content:center;color:var(--maroon);transition:.35s;
  }
  .card:hover .icon{background:var(--maroon);color:var(--cream);}
  .card h3{font-size:1.28rem;color:var(--maroon-deep);margin-bottom:14px;}
  .card p{font-size:.9rem;color:#6b5f57;line-height:1.75;font-weight:300;}
  .status{
    display:inline-block;margin-top:20px;font-size:.72rem;letter-spacing:1.5px;
    text-transform:uppercase;color:var(--gold);font-weight:600;
  }
 
  .quote{background:var(--maroon-deep);color:var(--cream);text-align:center;padding:100px 6%;}
  .quote blockquote{
    font-family:'Playfair Display',serif;font-size:clamp(1.5rem,3vw,2.2rem);font-style:italic;
    max-width:820px;margin:0 auto 24px;line-height:1.5;color:var(--cream);
  }
  .quote cite{color:var(--gold);font-size:.85rem;letter-spacing:2px;text-transform:uppercase;font-style:normal;}
 
  .cta{background:var(--cream);text-align:center;padding-bottom:140px;}
  .cta-box{
    max-width:820px;margin:0 auto;background:var(--maroon-deep);color:var(--cream);
    padding:70px 50px;position:relative;border:1px solid var(--maroon-line);
  }
  .cta-box::before,.cta-box::after{
    content:"";position:absolute;width:32px;height:32px;border:1px solid var(--gold);
  }
  .cta-box::before{top:-1px;left:-1px;border-right:none;border-bottom:none;}
  .cta-box::after{bottom:-1px;right:-1px;border-left:none;border-top:none;}
  .cta-box h2{font-size:clamp(1.8rem,3.6vw,2.5rem);margin-bottom:18px;}
  .cta-box p{color:var(--cream-2);font-weight:300;max-width:520px;margin:0 auto 36px;line-height:1.75;}
 
  footer{
    background:var(--maroon-deep);border-top:1px solid var(--maroon-line);padding:44px 6%;
    display:flex;align-items:center;justify-content:space-between;color:var(--cream-2);
    font-size:.8rem;flex-wrap:wrap;gap:16px;
  }
  footer .logo{font-size:1.1rem;}
  footer .foot-links{display:flex;gap:26px;list-style:none;}
  footer .foot-links a{color:var(--cream-2);text-decoration:none;font-size:.8rem;transition:.25s;}
  footer .foot-links a:hover{color:var(--gold);}
 
  @media(max-width:900px){
    nav ul{display:none;}
    .about-grid{grid-template-columns:1fr;gap:50px;}
    .about-visual{max-width:340px;margin:0 auto;}
    .event-inner{grid-template-columns:1fr;}
    .event-poster{border-right:none;border-bottom:1px solid var(--maroon-line);}
    .cards{grid-template-columns:1fr;}
    .pillars{grid-template-columns:1fr;}
    .t-item{grid-template-columns:80px 1fr;gap:18px;}
    section{padding:80px 6%;}
  }
</style>
</head>
<body>
 
<header id="siteHeader">
  <div class="logo" data-target="top">EGY <span>School</span></div>
  <nav>
    <ul>
      <li><a data-target="about">About</a></li>
      <li><a data-target="event">Ethics Journey</a></li>
      <li><a data-target="schedule">Schedule</a></li>
      <li><a data-target="activities">Activities</a></li>
      <li><a class="nav-cta" data-target="contact">Join Us</a></li>
    </ul>
  </nav>
</header>
 
<section class="hero" id="top">
  <svg class="hero-pattern" viewBox="0 0 1200 800" xmlns="http://www.w3.org/2000/svg">
    <g stroke="#f6efe4" stroke-width="1" fill="none" opacity="0.35">
      <path class="arch" d="M0 0 L200 200"/><path class="arch" d="M200 0 L0 200"/>
      <path class="arch2" d="M1000 0 Q1100 100 1200 0"/><path d="M0 800 Q100 700 200 800"/>
      <circle class="arch2" cx="1050" cy="650" r="90"/><circle cx="1050" cy="650" r="60"/><circle cx="1050" cy="650" r="30"/>
      <path d="M150 750 Q150 600 300 600 Q450 600 450 750"/>
      <path class="arch" d="M600 780 Q600 630 750 630 Q900 630 900 780"/>
      <path d="M50 50 L150 150 M150 50 L50 150"/>
    </g>
  </svg>
  <div class="hero-content">
    <span class="eyebrow">Student Activities</span>
    <h1>Where Character<br>Meets <em>Community</em></h1>
    <p class="tag">EGY School's Student Activities program builds skills, friendships, and values beyond the classroom &mdash; starting with our very first event.</p>
    <div class="btn-row">
      <a class="btn solid" data-target="event">Discover The Ethics Journey</a>
      <a class="btn ghost" data-target="about">Learn About Us</a>
    </div>
  </div>
  <div class="scroll-cue"><div></div>SCROLL</div>
</section>
 
<div class="strip"><div class="track">
  <span>RESPECT</span><span>&bull;</span><span>RESPONSIBILITY</span><span>&bull;</span><span>HONESTY</span><span>&bull;</span><span>KINDNESS</span><span>&bull;</span>
  <span>RESPECT</span><span>&bull;</span><span>RESPONSIBILITY</span><span>&bull;</span><span>HONESTY</span><span>&bull;</span><span>KINDNESS</span><span>&bull;</span>
</div></div>
 
<section class="about" id="about">
  <div class="about-grid">
    <div class="about-visual reveal">
      <div class="offset-line"></div>
      <div class="frame-bg">
        <svg viewBox="0 0 300 300" xmlns="http://www.w3.org/2000/svg">
          <g stroke="#f6efe4" stroke-width="1.2" fill="none">
            <path d="M150 20 A130 130 0 0 1 280 150"/>
            <path d="M150 20 A130 130 0 0 0 20 150"/>
            <circle cx="150" cy="150" r="60"/>
            <circle cx="150" cy="150" r="30"/>
            <path d="M20 150 Q150 300 280 150"/>
          </g>
        </svg>
      </div>
    </div>
    <div class="about-text reveal">
      <div class="eyebrow-line">Who We Are</div>
      <h2>Student Activities at EGY School</h2>
      <p>Our Student Activities program is dedicated to shaping well-rounded students &mdash; young people who lead with character as much as with knowledge. Through workshops, events, and hands-on experiences, we help students grow in mind, values, and community spirit.</p>
      <p>Every activity we host is built around a simple idea: school is where habits for life are formed.</p>
      <div class="pillars">
        <div class="pillar"><span class="num">01</span><span class="lbl">Character<br>Building</span></div>
        <div class="pillar"><span class="num">02</span><span class="lbl">Community<br>Engagement</span></div>
        <div class="pillar"><span class="num">03</span><span class="lbl">Real-World<br>Skills</span></div>
      </div>
    </div>
  </div>
</section>
 
<section class="event" id="event">
  <div class="event-tag reveal">
    <div class="eyebrow-line">First Student Activity Event</div>
    <h2>The Ethics Journey</h2>
  </div>
  <div class="event-inner reveal">
    <div class="event-poster">
      <div class="corner c1"></div><div class="corner c2"></div><div class="corner c3"></div><div class="corner c4"></div>
      <div class="frame">
        <div class="kicker">You're Invited To</div>
        <h3>The Ethics<br>Journey</h3>
        <div class="sub">A journey toward respect, responsibility, and better choices.</div>
        <div class="date-row">
          <div class="date-block"><div class="small">Tuesday</div></div>
          <div class="date-block"><div class="big">11</div></div>
          <div class="date-block"><div class="small">12:00 PM</div></div>
        </div>
        <div class="month-year">AUGUST &nbsp;&bull;&nbsp; 2026</div>
      </div>
    </div>
    <div class="event-details">
      <div class="eyebrow-line">What To Expect</div>
      <h2>A Conversation Worth Having</h2>
      <p>Our very first Student Activities event invites the EGY School community into an honest, engaging conversation about the values that shape who we are. Through interactive sessions and real discussions, students will explore what it truly means to live with integrity.</p>
      <ul class="value-list">
        <li><span class="mark">&mdash;</span><span><b>Respect</b><span class="desc">For ourselves, our peers, and our community</span></span></li>
        <li><span class="mark">&mdash;</span><span><b>Responsibility</b><span class="desc">Owning our actions and the choices we make</span></span></li>
        <li><span class="mark">&mdash;</span><span><b>Honesty</b><span class="desc">The foundation every trusted relationship is built on</span></span></li>
        <li><span class="mark">&mdash;</span><span><b>Kindness</b><span class="desc">Small, everyday acts that shape a stronger community</span></span></li>
      </ul>
      <div class="meta-row">
        <div class="meta-item"><b>Date</b>Tuesday, August 11, 2026</div>
        <div class="meta-item"><b>Time</b>12:00 PM</div>
        <div class="meta-item"><b>Venue</b>EGY School Campus</div>
      </div>
      <a class="btn solid" data-target="contact" style="align-self:flex-start;">Reserve Your Spot</a>
    </div>
  </div>
</section>
 
<section class="schedule" id="schedule">
  <div class="section-head reveal">
    <div class="eyebrow-line">Event Flow</div>
    <h2>How The Day Unfolds</h2>
    <p>A short, focused gathering designed to spark real reflection &mdash; not just another assembly.</p>
  </div>
  <div class="timeline reveal">
    <div class="t-item">
      <div class="t-time">12:00 PM</div>
      <div class="t-content"><h4>Welcome &amp; Opening</h4><p>Students gather on campus as the Student Activities team opens the very first event of the program.</p></div>
    </div>
    <div class="t-item">
      <div class="t-time">12:15 PM</div>
      <div class="t-content"><h4>The Ethics Journey Talk</h4><p>An honest conversation about respect, responsibility, honesty, and kindness &mdash; and why they matter every single day.</p></div>
    </div>
    <div class="t-item">
      <div class="t-time">12:45 PM</div>
      <div class="t-content"><h4>Group Reflection</h4><p>Students break into small groups to discuss real scenarios and practice making better choices together.</p></div>
    </div>
    <div class="t-item">
      <div class="t-time">1:15 PM</div>
      <div class="t-content"><h4>Closing &amp; Takeaways</h4><p>A closing moment to share commitments and carry the values of the day back into everyday school life.</p></div>
    </div>
  </div>
</section>
 
<section class="activities" id="activities">
  <div class="section-head reveal">
    <div class="eyebrow-line">What's Coming</div>
    <h2>More Activities on the Way</h2>
    <p>The Ethics Journey is only the beginning. Here's a look at the kind of experiences our program will keep bringing to campus.</p>
  </div>
  <div class="cards reveal">
    <div class="card">
      <div class="icon"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M12 2 L2 8 L12 14 L22 8 Z"/><path d="M6 11 V17 C6 19 9 20 12 20 C15 20 18 19 18 17 V11"/></svg></div>
      <h3>Leadership Workshops</h3>
      <p>Interactive sessions helping students build confidence, communication, and decision-making skills.</p>
      <div class="status">Coming Soon</div>
    </div>
    <div class="card">
      <div class="icon"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M4 21 V10 L12 4 L20 10 V21"/><path d="M9 21 V14 H15 V21"/></svg></div>
      <h3>Community Service Day</h3>
      <p>A campus-wide initiative connecting students with local causes and giving back to Egypt's communities.</p>
      <div class="status">Coming Soon</div>
    </div>
    <div class="card">
      <div class="icon"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><circle cx="12" cy="8" r="4"/><path d="M4 21 C4 16 8 14 12 14 C16 14 20 16 20 21"/></svg></div>
      <h3>Peer Mentorship Program</h3>
      <p>Pairing younger and older students to build friendship, guidance, and a stronger school community.</p>
      <div class="status">Coming Soon</div>
    </div>
  </div>
</section>
 
<section class="quote reveal">
  <blockquote>&ldquo;Character isn't taught in a single lesson &mdash; it's built one honest choice at a time.&rdquo;</blockquote>
  <cite>EGY School &bull; Student Activities</cite>
</section>
 
<section class="cta" id="contact">
  <div class="cta-box reveal">
    <h2>Join Us on The Ethics Journey</h2>
    <p>Tuesday, August 11, 2026 &middot; 12:00 PM &middot; EGY School Campus. Every student is welcome.</p>
    <a class="btn" data-target="top">Back to Top</a>
  </div>
</section>
 
<footer>
  <div class="logo" data-target="top">EGY <span>School</span></div>
  <ul class="foot-links">
    <li><a data-target="about">About</a></li>
    <li><a data-target="event">Ethics Journey</a></li>
    <li><a data-target="activities">Activities</a></li>
  </ul>
  <div>Student Activities Program &middot; EGY School Campus &middot; 2026</div>
</footer>
 
<script>
  document.querySelectorAll('[data-target]').forEach(function(el){
    el.addEventListener('click', function(e){
      e.preventDefault();
      var target = document.getElementById(el.getAttribute('data-target'));
      if(target){ target.scrollIntoView({behavior:'smooth', block:'start'}); }
    });
  });
 
  var header = document.getElementById('siteHeader');
  window.addEventListener('scroll', function(){
    if(window.scrollY > 40){ header.classList.add('scrolled'); }
    else{ header.classList.remove('scrolled'); }
  });
 
  var revealEls = document.querySelectorAll('.reveal');
  var observer = new IntersectionObserver(function(entries){
    entries.forEach(function(entry){
      if(entry.isIntersecting){ entry.target.classList.add('in'); observer.unobserve(entry.target); }
    });
  }, {threshold:0.15});
  revealEls.forEach(function(el){ observer.observe(el); });
</script>
 
</body>
</html>
 
