  `<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Network Way | AI-Powered Solutions</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@600;700&family=Open+Sans&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary: #0A2647;
      --secondary-accent: #15B06E;
      --white: #FFFFFF;
      --light-greay-bg: #F7F9FC;
      --text-dark: #3C3C3C;
      --font-heading: 'Poppins', sans-serif;
      --font-body: 'Open Sans', sans-serif;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: var(--font-body);
      background-color: var(--light-greay-bg);
      color: var(--text-dark);
      direction: ltr;
    }
    .container { max-width: 1200px; margin: 0 auto; padding: 0 20px; }
    header, footer {
      background-color: var(--white);
      border-bottom: 1px solid #E8ECF3;
    }
    .navbar { display: flex; justify-content: space-between; align-items: center; padding: 20px 0; }
    .logo-placeholder { font-family: var(--font-heading); color: var(--primary); font-size: 24px; }
    nav a { margin-left: 20px; text-decoration: none; color: var(--text-dark); font-weight: bold; }
    .lang-buttons button {
      margin-left: 10px; padding: 8px 16px; border: none; border-radius: 20px; cursor: pointer;
      background-color: var(--secondary-accent); color: #fff; font-size: 14px;
    }
    .hero {
      text-align: center; height: 80vh; display: flex; flex-direction: column; justify-content: center; align-items: center;
      background: url("https://images.pexels.com/photos/4968391/pexels-photo-4968391.jpeg") center/cover no-repeat;
      color: #fff;
    }
    .hero-overlay {
      background: rgba(0,0,0,0.6); width: 100%; height: 100%; display: flex; flex-direction: column;
      justify-content: center; align-items: center; padding: 20px;
    }
    h1, h2 { font-family: var(--font-heading); font-weight: bold; }
    .tagline { font-size: 18px; opacity: 0.9; margin-top: 10px; }
    .cta-button {
      background-color: var(--secondary-accent); color: #fff; border: none;
      padding: 15px 30px; border-radius: 30px; cursor: pointer; font-size: 16px; margin-top: 20px;
    }
    .services-listing {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 20px; margin-top: 40px;
    }
    .service-card {
      background: #fff; border-radius: 8px; padding: 20px; text-align: center;
      box-shadow: 0 5px 10px rgba(0,0,0,0.1);
    }
    .service-card img { width: 80px; margin-bottom: 15px; }
    footer { text-align: center; padding: 20px 0; margin-top: 50px; }
    .footer-link { margin: 0 10px; text-decoration: none; color: var(--text-dark); font-size: 14px; }
  </style>
</head>
<body>

  <!-- Navbar -->
  <header>
    <div class="container navbar">
      <div class="logo-placeholder">NW LOGO</div>
      <nav>
        <a href="#services" data-en="Services" data-ar="الخدمات">Services</a>
        <a href="#about" data-en="About Us" data-ar="من نحن">About Us</a>
        <a href="#contact" data-en="Contact" data-ar="اتصل بنا">Contact</a>
      </nav>
      <div class="lang-buttons">
        <button onclick="switchLang('en')">English</button>
        <button onclick="switchLang('ar')">العربية</button>
      </div>
    </div>
  </header>

  <!-- Hero -->
  <section class="hero">
    <div class="hero-overlay">
      <h1 id="hero-title" data-en="AI-Powered Payment Solutions" data-ar="حلول دفع مدعومة بالذكاء الاصطناعي">
        AI-Powered Payment Solutions
      </h1>
      <p class="tagline" id="hero-tagline" data-en="Smart POS and Payment Gateway services for your business"
         data-ar="أجهزة نقاط البيع وبوابات الدفع الذكية لعملك">
        Smart POS and Payment Gateway services for your business
      </p>
      <button class="cta-button" id="cta-btn" data-en="Get Started" data-ar="ابدأ الآن">Get Started</button>
    </div>
  </section>

  <!-- Services -->
  <section id="services" class="container">
    <h2 data-en="Our Services" data-ar="خدماتنا">Our Services</h2>
    <div class="services-listing">
      <div class="service-card">
        <img src="https://cdn-icons-png.flaticon.com/512/1040/1040230.png" alt="POS">
        <div data-en="POS Devices" data-ar="أجهزة نقاط البيع">POS Devices</div>
      </div>
      <div class="service-card">
        <img src="https://cdn-icons-png.flaticon.com/512/686/686308.png" alt="Gateway">
        <div data-en="Payment Gateway" data-ar="بوابات الدفع">Payment Gateway</div>
      </div>
      <div class="service-card">
        <img src="https://cdn-icons-png.flaticon.com/512/3208/3208730.png" alt="QR">
        <div data-en="QR Code Payment" data-ar="الدفع عبر QR">QR Code Payment</div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <a href="#" class="footer-link" data-en="Privacy Policy" data-ar="سياسة الخصوصية">Privacy Policy</a>
    <a href="#" class="footer-link" data-en="Terms of Service" data-ar="شروط الاستخدام">Terms of Service</a>
    <p style="margin-top:10px;">© 2025 Network Way</p>
  </footer>

  <!-- Language Switcher -->
  <script>
    function switchLang(lang) {
      document.querySelectorAll("[data-en]").forEach(el => {
        el.innerText = el.getAttribute("data-" + lang);
      });
      if(lang === "ar") {
        document.body.setAttribute("dir","rtl");
        document.body.style.fontFamily = "Tahoma, sans-serif";
      } else {
        document.body.setAttribute("dir","ltr");
        document.body.style.fontFamily = "Open Sans, sans-serif";
      }
    }
  </script>

</body>
</html>
