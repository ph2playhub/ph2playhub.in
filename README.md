<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>PH² PLAY HUB | Gaming Store</title>
  <meta name="description" content="PH² PLAY HUB - PlayStation, Xbox, PSP games, consoles, accessories and gaming services.">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: #08080d;
      color: #fff;
      line-height: 1.6;
    }

    /* NAVBAR */
    nav {
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 1000;
      background: rgba(5, 5, 10, 0.95);
      border-bottom: 1px solid #272733;
      backdrop-filter: blur(10px);
    }

    .nav-container {
      max-width: 1200px;
      margin: auto;
      padding: 16px 25px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 25px;
      font-weight: 900;
      color: #fff;
      text-decoration: none;
      letter-spacing: 1px;
    }

    .logo span {
      color: #9b4dff;
    }

    .nav-links {
      display: flex;
      gap: 25px;
      list-style: none;
    }

    .nav-links a {
      color: white;
      text-decoration: none;
      font-weight: bold;
      transition: 0.3s;
    }

    .nav-links a:hover {
      color: #b65cff;
    }

    /* HERO */
    .hero {
      min-height: 100vh;
      padding: 150px 25px 80px;
      display: flex;
      align-items: center;
      text-align: center;
      justify-content: center;
      background:
        radial-gradient(circle at 50% 40%, rgba(133, 42, 255, 0.28), transparent 35%),
        linear-gradient(135deg, #08080d, #14091e, #08080d);
      position: relative;
      overflow: hidden;
    }

    .hero-content {
      max-width: 900px;
    }

    .hero h1 {
      font-size: clamp(48px, 8vw, 95px);
      font-weight: 1000;
      line-height: 1;
      text-transform: uppercase;
      text-shadow: 0 0 30px rgba(166, 77, 255, 0.5);
    }

    .hero h1 span {
      color: #a855f7;
    }

    .hero h2 {
      margin-top: 20px;
      font-size: clamp(20px, 3vw, 32px);
      color: #ddd;
    }

    .hero p {
      margin: 20px auto;
      max-width: 700px;
      color: #aaa;
      font-size: 18px;
    }

    .buttons {
      margin-top: 35px;
      display: flex;
      justify-content: center;
      gap: 15px;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-block;
      padding: 14px 28px;
      border-radius: 30px;
      text-decoration: none;
      font-weight: bold;
      transition: 0.3s;
    }

    .btn-primary {
      background: #9b4dff;
      color: white;
      box-shadow: 0 0 25px rgba(155, 77, 255, 0.4);
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      background: #b56cff;
    }

    .btn-secondary {
      border: 1px solid #9b4dff;
      color: white;
    }

    .btn-secondary:hover {
      background: #9b4dff;
    }

    /* GENERAL */
    section {
      padding: 90px 25px;
    }

    .container {
      max-width: 1150px;
      margin: auto;
    }

    .section-title {
      text-align: center;
      margin-bottom: 50px;
    }

    .section-title h2 {
      font-size: 42px;
      text-transform: uppercase;
    }

    .section-title span {
      color: #a855f7;
    }

    .section-title p {
      color: #999;
      margin-top: 10px;
    }

    /* PLATFORMS */
    .platforms {
      background: #0c0c12;
    }

    .platform-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
      gap: 18px;
    }

    .platform {
      padding: 30px 15px;
      text-align: center;
      border: 1px solid #282832;
      border-radius: 15px;
      background: #111119;
      transition: 0.3s;
    }

    .platform:hover {
      transform: translateY(-6px);
      border-color: #a855f7;
      box-shadow: 0 0 25px rgba(168, 85, 247, 0.15);
    }

    .platform .icon {
      font-size: 42px;
      margin-bottom: 10px;
    }

    .platform h3 {
      font-size: 22px;
    }

    /* PRODUCTS */
    .products {
      background: #08080d;
    }

    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
    }

    .product-card {
      background: #111119;
      border: 1px solid #292934;
      border-radius: 18px;
      padding: 28px;
      text-align: center;
      transition: 0.3s;
    }

    .product-card:hover {
      transform: translateY(-8px);
      border-color: #a855f7;
    }

    .product-image {
      height: 160px;
      border-radius: 12px;
      margin-bottom: 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: linear-gradient(135deg, #20102e, #0e0e15);
      font-size: 65px;
    }

    .product-card h3 {
      font-size: 24px;
      margin-bottom: 8px;
    }

    .product-card p {
      color: #999;
      margin-bottom: 20px;
    }

    /* SERVICES */
    .services {
      background: #0c0c12;
    }

    .service-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
    }

    .service {
      padding: 30px;
      background: #111119;
      border-radius: 18px;
      border: 1px solid #292934;
    }

    .service-icon {
      font-size: 45px;
      margin-bottom: 15px;
    }

    .service h3 {
      margin-bottom: 10px;
      font-size: 23px;
    }

    .service p {
      color: #999;
    }

    /* OFFER */
    .offer {
      text-align: center;
      background:
        radial-gradient(circle, rgba(168, 85, 247, 0.25), transparent 55%),
        #110817;
    }

    .offer-box {
      max-width: 800px;
      margin: auto;
      padding: 55px 25px;
      border: 1px solid #9b4dff;
      border-radius: 25px;
      box-shadow: 0 0 40px rgba(155, 77, 255, 0.12);
    }

    .offer h2 {
      font-size: clamp(35px, 6vw, 60px);
    }

    .offer h2 span {
      color: #b866ff;
    }

    .offer p {
      color: #bbb;
      margin: 15px 0 25px;
    }

    /* CONTACT */
    .contact {
      background: #08080d;
    }

    .contact-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 25px;
    }

    .contact-card {
      background: #111119;
      border: 1px solid #292934;
      padding: 30px;
      border-radius: 18px;
      text-align: center;
    }

    .contact-card h3 {
      color: #a855f7;
      margin-bottom: 10px;
    }

    .contact-card p {
      color: #ccc;
    }

    .contact-card a {
      color: white;
      text-decoration: none;
    }

    .contact-card a:hover {
      color: #a855f7;
    }

    /* FOOTER */
    footer {
      text-align: center;
      padding: 35px 20px;
      background: #050509;
      border-top: 1px solid #22222c;
    }

    footer h3 {
      font-size: 25px;
      margin-bottom: 8px;
    }

    footer h3 span {
      color: #a855f7;
    }

    footer p {
      color: #777;
      font-size: 14px;
    }

    /* WHATSAPP */
    .whatsapp {
      position: fixed;
      right: 22px;
      bottom: 22px;
      width: 60px;
      height: 60px;
      border-radius: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #25D366;
      color: white;
      font-size: 29px;
      text-decoration: none;
      z-index: 999;
      box-shadow: 0 5px 25px rgba(0,0,0,0.4);
      transition: 0.3s;
    }

    .whatsapp:hover {
      transform: scale(1.1);
    }

    /* MOBILE */
    @media (max-width: 700px) {
      .nav-links {
        display: none;
      }

      .hero {
        padding-top: 130px;
      }

      section {
        padding: 65px 18px;
      }

      .section-title h2 {
        font-size: 32px;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->
  <nav>
    <div class="nav-container">
      <a href="#home" class="logo">PH<span>²</span> PLAY HUB</a>

      <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#platforms">Platforms</a></li>
        <li><a href="#products">Games</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </div>
  </nav>

  <!-- HERO -->
  <section class="hero" id="home">
    <div class="hero-content">

      <h1>PH<span>²</span> PLAY HUB</h1>

      <h2>Your Gaming Destination</h2>

      <p>
        PlayStation games, consoles, accessories, Xbox, PSP and
        professional gaming services — all in one place.
      </p>

      <div class="buttons">
        <a
          class="btn btn-primary"
          href="https://wa.me/919363735190?text=Hello%20PH2%20PLAY%20HUB%2C%20I%20want%20to%20know%20about%20your%20gaming%20products."
          target="_blank">
          💬 WhatsApp Us
        </a>

        <a class="btn btn-secondary" href="#products">
          🎮 Explore Games
        </a>
      </div>

    </div>
  </section>

  <!-- PLATFORMS -->
  <section class="platforms" id="platforms">

    <div class="container">

      <div class="section-title">
        <h2>Gaming <span>Platforms</span></h2>
        <p>Choose your gaming platform</p>
      </div>

      <div class="platform-grid">

        <div class="platform">
          <div class="icon">🎮</div>
          <h3>PS2</h3>
          <p>PlayStation 2</p>
        </div>

        <div class="platform">
          <div class="icon">🎮</div>
          <h3>PS3</h3>
          <p>PlayStation 3</p>
        </div>

        <div class="platform">
          <div class="icon">🎮</div>
          <h3>PS4</h3>
          <p>PlayStation 4</p>
        </div>

        <div class="platform">
          <div class="icon">🎮</div>
          <h3>PS5</h3>
          <p>PlayStation 5</p>
        </div>

        <div class="platform">
          <div class="icon">🕹️</div>
          <h3>XBOX</h3>
          <p>Xbox Gaming</p>
        </div>

        <div class="platform">
          <div class="icon">🎮</div>
          <h3>PSP</h3>
          <p>Portable Gaming</p>
        </div>

      </div>
    </div>
  </section>

  <!-- PRODUCTS -->
  <section class="products" id="products">

    <div class="container">

      <div class="section-title">
        <h2>Featured <span>Games</span></h2>
        <p>Level up your gaming collection</p>
      </div>

      <div class="product-grid">

        <div class="product-card">
          <div class="product-image">⚔️</div>
          <h3>God of War</h3>
          <p>Epic action and adventure gaming.</p>
          <a
            class="btn btn-primary"
            href="https://wa.me/919363735190?text=Hello%20PH2%20PLAY%20HUB%2C%20I%20am%20interested%20in%20God%20of%20War."
            target="_blank">
            Enquire
          </a>
        </div>

        <div class="product-card">
          <div class="product-image">🕷️</div>
          <h3>Spider-Man</h3>
          <p>Experience the Spider-Man universe.</p>
          <a
            class="btn btn-primary"
            href="https://wa.me/919363735190?text=Hello%20PH2%20PLAY%20HUB%2C%20I%20am%20interested%20in%20Spider-Man%20games."
            target="_blank">
            Enquire
          </a>
        </div>

        <div class="product-card">
          <div class="product-image">🔥</div>
          <h3>GTA</h3>
          <p>Open-world gaming action.</p>
          <a
            class="btn btn-primary"
            href="https://wa.me/919363735190?text=Hello%20PH2%20PLAY%20HUB%2C%20I%20am%20interested%20in%20GTA%20games."
            target="_blank">
            Enquire
          </a>
        </div>

        <div class="product-card">
          <div class="product-image">🧟</div>
          <h3>The Last of Us</h3>
          <p>Story-driven survival adventure.</p>
          <a
            class="btn btn-primary"
            href="https://wa.me/919363735190?text=Hello%20PH2%20PLAY%20HUB%2C%20I%20am%20interested%20in%20The%20Last%20of%20Us."
            target="_blank">
            Enquire
          </a>
        </div>

      </div>
    </div>
  </section>

  <!-- SERVICES -->
  <section class="services" id="services">

    <div class="container">

      <div class="section-title">
        <h2>Our <span>Services</span></h2>
        <p>Gaming support from PH² PLAY HUB</p>
      </div>

      <div class="service-grid">

        <div class="service">
          <div class="service-icon">🛠️</div>
          <h3>PS3 Service</h3>
          <p>
            Professional PlayStation 3 service and troubleshooting.
            Contact us for service details.
          </p>
        </div>

        <div class="service">
          <div class="service-icon">🎮</div>
          <h3>Console Sales</h3>
          <p>
            Gaming consoles and accessories for your gaming setup.
          </p>
        </div>

        <div class="service">
          <div class="service-icon">💿</div>
          <h3>Games</h3>
          <p>
            Explore games for PlayStation and other supported gaming platforms.
          </p>
        </div>

        <div class="service">
          <div class="service-icon">🕹️</div>
          <h3>Accessories</h3>
          <p>
            Controllers and gaming accessories to improve your setup.
          </p>
        </div>

      </div>
    </div>
  </section>

  <!-- OFFER -->
  <section class="offer">

    <div class="offer-box">

      <h2>READY TO <span>PLAY?</span></h2>

      <p>
        Contact PH² PLAY HUB today for products, games,
        consoles and gaming services.
      </p>

      <a
        class="btn btn-primary"
        href="https://wa.me/919363735190?text=Hello%20PH2%20PLAY%20HUB%2C%20I%20want%20to%20place%20an%20order."
        target="_blank">
        🚀 Order on WhatsApp
      </a>

    </div>

  </section>

  <!-- CONTACT -->
  <section class="contact" id="contact">

    <div class="container">

      <div class="section-title">
        <h2>Contact <span>Us</span></h2>
        <p>Let's talk gaming</p>
      </div>

      <div class="contact-grid">

        <div class="contact-card">
          <h3>📱 WhatsApp</h3>
          <p>
            <a href="https://wa.me/919363735190" target="_blank">
              +91 93637 35190
            </a>
          </p>
        </div>

        <div class="contact-card">
          <h3>📧 Email</h3>
          <p>
            <a href="mailto:ph2playhub@gmail.com">
              ph2playhub@gmail.com
            </a>
          </p>
        </div>

        <div class="contact-card">
          <h3>📍 Location</h3>
          <p>
            Ullur Chettaimadapam<br>
            Kumbakonam 612001
          </p>
        </div>

      </div>

    </div>

  </section>

  <!-- FOOTER -->
  <footer>

    <h3>PH<span>²</span> PLAY HUB</h3>

    <p>
      © 2026 PH² PLAY HUB. All Rights Reserved.
    </p>

    <p>
      Gaming • Consoles • Games • Accessories • Services
    </p>

  </footer>

  <!-- FLOATING WHATSAPP -->
  <a
    class="whatsapp"
    href="https://wa.me/919363735190?text=Hello%20PH2%20PLAY%20HUB"
    target="_blank"
    aria-label="Chat on WhatsApp">
    💬
  </a>

</body>
</html>
