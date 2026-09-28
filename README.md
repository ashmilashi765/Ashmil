# <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>VB Visuals — Videography & Editing</title>

  <meta name="description"
        content="VB Visuals — Videography, Photography and Video Editing Portfolio">

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
      font-family: Arial, Helvetica, sans-serif;
      background: #080808;
      color: #fff;
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    /* NAVBAR */

    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      padding: 20px 7%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      z-index: 1000;

      background: rgba(8, 8, 8, 0.75);
      backdrop-filter: blur(15px);
    }

    .logo {
      font-size: 24px;
      font-weight: 900;
      letter-spacing: 2px;
    }

    .logo span {
      color: #888;
    }

    nav ul {
      display: flex;
      gap: 25px;
      list-style: none;
    }

    nav a {
      font-size: 14px;
      color: #ccc;
      transition: 0.3s;
    }

    nav a:hover {
      color: #fff;
    }

    /* HERO */

    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: 120px 8% 80px;

      background:
        linear-gradient(
          rgba(0,0,0,.55),
          rgba(0,0,0,.85)
        ),
        url("https://images.unsplash.com/photo-1492691527719-9d1e07e534b4?auto=format&fit=crop&w=2000&q=90")
        center/cover;
    }

    .hero-content {
      max-width: 800px;
    }

    .tag {
      color: #aaa;
      text-transform: uppercase;
      letter-spacing: 4px;
      font-size: 12px;
      margin-bottom: 20px;
    }

    h1 {
      font-size: clamp(55px, 11vw, 120px);
      line-height: .9;
      letter-spacing: -5px;
      margin-bottom: 30px;
    }

    h1 span {
      color: #777;
    }

    .hero p {
      color: #ccc;
      max-width: 600px;
      font-size: 18px;
      margin-bottom: 35px;
    }

    .button {
      display: inline-block;
      padding: 14px 25px;
      border: 1px solid #fff;
      border-radius: 30px;
      transition: .3s;
      margin-right: 10px;
    }

    .button:hover {
      background: #fff;
      color: #000;
    }

    .button.secondary {
      border-color: #444;
      color: #aaa;
    }

    /* GENERAL */

    section {
      padding: 100px 8%;
    }

    .section-title {
      font-size: 45px;
      margin-bottom: 50px;
      letter-spacing: -2px;
    }

    .section-title span {
      color: #666;
    }

    /* ABOUT */

    .about {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 70px;
      align-items: center;
    }

    .about-text p {
      color: #aaa;
      font-size: 17px;
      margin-bottom: 20px;
    }

    .about-card {
      min-height: 350px;
      display: flex;
      align-items: center;
      justify-content: center;

      background:
        linear-gradient(135deg, #171717, #080808);

      border: 1px solid #222;
      border-radius: 20px;
    }

    .big-vb {
      font-size: 130px;
      font-weight: 900;
      letter-spacing: -10px;
    }

    .big-vb span {
      color: #555;
    }

    /* WORK */

    .work-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 20px;
    }

    .work {
      position: relative;
      height: 400px;
      overflow: hidden;
      border-radius: 15px;
      background: #151515;
    }

    .work img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: .6s;
    }

    .work:hover img {
      transform: scale(1.08);
    }

    .work-info {
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      padding: 30px;

      background:
        linear-gradient(transparent, rgba(0,0,0,.9));
    }

    .work-info h3 {
      font-size: 25px;
    }

    .work-info p {
      color: #aaa;
    }

    /* SERVICES */

    .services {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 15px;
    }

    .service {
      padding: 30px;
      min-height: 180px;

      border: 1px solid #222;
      border-radius: 15px;

      transition: .3s;
    }

    .service:hover {
      background: #151515;
      transform: translateY(-5px);
    }

    .service-number {
      color: #555;
      font-size: 13px;
    }

    .service h3 {
      margin-top: 35px;
      font-size: 20px;
    }

    .service p {
      color: #777;
      margin-top: 10px;
      font-size: 14px;
    }

    /* CONTACT */

    .contact {
      text-align: center;
      padding-bottom: 130px;
    }

    .contact h2 {
      font-size: clamp(45px, 8vw, 90px);
      line-height: 1;
      margin-bottom: 25px;
    }

    .contact p {
      color: #888;
      margin-bottom: 35px;
    }

    .socials {
      display: flex;
      justify-content: center;
      gap: 15px;
      flex-wrap: wrap;
    }

    .socials a {
      border: 1px solid #333;
      padding: 12px 22px;
      border-radius: 30px;
      color: #bbb;
      transition: .3s;
    }

    .socials a:hover {
      background: #fff;
      color: #000;
    }

    /* FOOTER */

    footer {
      border-top: 1px solid #1c1c1c;
      padding: 25px 8%;
      display: flex;
      justify-content: space-between;
      color: #555;
      font-size: 13px;
    }

    /* MOBILE */

    @media (max-width: 800px) {

      nav {
        padding: 18px 6%;
      }

      nav ul {
        display: none;
      }

      .hero {
        padding: 120px 7% 70px;
      }

      h1 {
        font-size: 65px;
        letter-spacing: -3px;
      }

      .hero p {
        font-size: 16px;
      }

      section {
        padding: 75px 7%;
      }

      .about {
        grid-template-columns: 1fr;
        gap: 40px;
      }

      .work-grid {
        grid-template-columns: 1fr;
      }

      .work {
        height: 350px;
      }

      .services {
        grid-template-columns: 1fr 1fr;
      }

      .section-title {
        font-size: 38px;
      }

      footer {
        flex-direction: column;
        gap: 10px;
      }
    }

    @media (max-width: 450px) {

      .services {
        grid-template-columns: 1fr;
      }

      .button {
        margin-bottom: 10px;
      }

      .big-vb {
        font-size: 90px;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->

  <nav>
    <div class="logo">VB<span>.</span></div>

    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#work">Work</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>


  <!-- HERO -->

  <section class="hero" id="home">

    <div class="hero-content">

      <div class="tag">
        Videography • Photography • Editing
      </div>

      <h1>
        Visual<br>
        <span>Stories.</span>
      </h1>

      <p>
        I create cinematic visuals, memorable photographs
        and engaging edits that turn ordinary moments into
        stories worth remembering.
      </p>

      <a href="#work" class="button">
        View My Work
      </a>

      <a href="#contact" class="button secondary">
        Contact Me
      </a>

    </div>

  </section>


  <!-- ABOUT -->

  <section id="about">

    <div class="about">

      <div class="about-text">

        <div class="section-title">
          About <span>Me</span>
        </div>

        <p>
          I'm a visual creator passionate about videography,
          photography and editing.
        </p>

        <p>
          My goal is simple — capture moments, build
          atmosphere and tell stories through visuals.
        </p>

        <p>
          Every frame should have a feeling behind it.
        </p>

      </div>

      <div class="about-card">
        <div class="big-vb">
          V<span>B</span>
        </div>
      </div>

    </div>

  </section>


  <!-- WORK -->

  <section id="work">

    <div class="section-title">
      Selected <span>Work</span>
    </div>

    <div class="work-grid">

      <div class="work">

        <img
          src="https://images.unsplash.com/photo-1485846234645-a62644f84728?auto=format&fit=crop&w=1200&q=90"
          alt="Cinematic filmmaking">

        <div class="work-info">
          <h3>Cinematic Films</h3>
          <p>Storytelling through motion</p>
        </div>

      </div>


      <div class="work">

        <img
          src="https://images.unsplash.com/photo-1516035069371-29a1b244cc32?auto=format&fit=crop&w=1200&q=90"
          alt="Photography">

        <div class="work-info">
          <h3>Photography</h3>
          <p>Moments frozen in time</p>
        </div>

      </div>


      <div class="work">

        <img
          src="https://images.unsplash.com/photo-1536240478700-b869070f9279?auto=format&fit=crop&w=1200&q=90"
          alt="Video editing">

        <div class="work-info">
          <h3>Video Editing</h3>
          <p>Turning footage into stories</p>
        </div>

      </div>


      <div class="work">

        <img
          src="https://images.unsplash.com/photo-1492619375914-88005aa9e8fb?auto=format&fit=crop&w=1200&q=90"
          alt="Creative production">

        <div class="work-info">
          <h3>Creative Projects</h3>
          <p>Ideas brought to life</p>
        </div>

      </div>

    </div>

  </section>


  <!-- SERVICES -->

  <section id="services">

    <div class="section-title">
      What I <span>Do</span>
    </div>

    <div class="services">

      <div class="service">
        <div class="service-number">01</div>
        <h3>Videography</h3>
        <p>Cinematic videos and visual storytelling.</p>
      </div>

      <div class="service">
        <div class="service-number">02</div>
        <h3>Photography</h3>
        <p>Creative photography for people and events.</p>
      </div>

      <div class="service">
        <div class="service-number">03</div>
        <h3>Reels</h3>
        <p>Short-form content designed for social media.</p>
      </div>

      <div class="service">
        <div class="service-number">04</div>
        <h3>Editing</h3>
        <p>Professional cuts, transitions and color grading.</p>
      </div>

    </div>

  </section>


  <!-- CONTACT -->

  <section class="contact" id="contact">

    <h2>
      Let's create<br>
      something.
    </h2>

    <p>
      Have a project or idea? Let's turn it into a visual story.
    </p>

    <div class="socials">

      <!-- CHANGE THESE LINKS -->

      <a href="https://instagram.com/YOUR_USERNAME"
         target="_blank">
        Instagram
      </a>

      <a href="https://wa.me/YOUR_NUMBER"
         target="_blank">
        WhatsApp
      </a>

      <a href="mailto:YOUR_EMAIL@gmail.com">
        Email
      </a>

    </div>

  </section>


  <!-- FOOTER -->

  <footer>

    <div>
      © 2026 VB Visuals
    </div>

    <div>
      Videography • Photography • Editing
    </div>

  </footer>

</body>
</html>