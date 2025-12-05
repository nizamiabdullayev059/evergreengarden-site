<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Evergreengarden Ltd | Landscape & Garden Design</title>

  <meta name="description" content="Evergreengarden Ltd – premium landscape design, garden construction, and plant supply. Creating evergreen gardens for homes, villas, and public spaces." />

  <style>
    /* --------- RESET --------- */
    *, *::before, *::after {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      line-height: 1.5;
      color: #163020; /* deep green */
      background-color: #f5f7f4;
      scroll-behavior: smooth;
    }
    img {
      max-width: 100%;
      display: block;
    }
    a {
      text-decoration: none;
      color: inherit;
    }

    /* --------- LAYOUT HELPERS --------- */
    .container {
      width: min(1100px, 100% - 2rem);
      margin: 0 auto;
    }
    .section {
      padding: 4rem 0;
    }
    .section-header {
      text-align: center;
      margin-bottom: 2.5rem;
    }
    .section-title {
      font-size: clamp(1.8rem, 2.5vw, 2.2rem);
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: #163020;
    }
    .section-subtitle {
      margin-top: 0.6rem;
      color: #4f6f52;
      font-size: 0.95rem;
    }

    /* --------- NAVBAR --------- */
    header {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: blur(10px);
      background: rgba(245, 247, 244, 0.92);
      border-bottom: 1px solid #dde3da;
    }
    .nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0.8rem 0;
      gap: 1rem;
    }
    .logo {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      font-weight: 700;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      font-size: 0.85rem;
      color: #163020;
    }
    .logo-mark {
      width: 34px;
      height: 34px;
      border-radius: 999px;
      border: 2px solid #163020;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.1rem;
      background: #e1f0dd;
    }
    nav {
      display: flex;
      align-items: center;
      gap: 1.5rem;
    }
    nav ul {
      list-style: none;
      display: flex;
      gap: 1.5rem;
      align-items: center;
    }
    nav a {
      font-size: 0.9rem;
      text-transform: uppercase;
      letter-spacing: 0.15em;
      color: #4f6f52;
      position: relative;
    }
    nav a::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: -0.35rem;
      width: 0;
      height: 1px;
      background: #163020;
      transition: width 0.2s ease-out;
    }
    nav a:hover::after {
      width: 100%;
    }
    .nav-cta {
      padding: 0.5rem 1rem;
      border-radius: 999px;
      border: 1px solid #163020;
      font-size: 0.8rem;
      text-transform: uppercase;
      letter-spacing: 0.14em;
      background: #163020;
      color: #f5f7f4;
    }
    .nav-cta:hover {
      background: #1f3b28;
    }

    /* Language switcher */
    .lang-switch {
      display: flex;
      gap: 0.35rem;
      align-items: center;
      font-size: 0.75rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
    }
    .lang-btn {
      border-radius: 999px;
      border: 1px solid transparent;
      padding: 0.25rem 0.6rem;
      cursor: pointer;
      background: transparent;
      color: #4f6f52;
    }
    .lang-btn.active-lang {
      border-color: #163020;
      color: #163020;
      background: #e1f0dd;
    }

    /* Mobile nav */
    .nav-toggle {
      display: none;
      flex-direction: column;
      gap: 4px;
      cursor: pointer;
    }
    .nav-toggle span {
      width: 20px;
      height: 2px;
      background: #163020;
    }
    @media (max-width: 768px) {
      nav ul {
        display: none;
        position: absolute;
        inset: 56px 1rem auto 1rem;
        padding: 1rem;
        background: #f5f7f4;
        border-radius: 1rem;
        border: 1px solid #dde3da;
        flex-direction: column;
        gap: 1rem;
      }
      nav ul.open {
        display: flex;
      }
      .nav-toggle {
        display: flex;
      }
      .lang-switch {
        margin-left: auto;
      }
    }

    .lang-hidden {
      display: none !important;
    }

    /* --------- HERO --------- */
    .hero {
      padding: 4rem 0 4.5rem;
    }
    .hero-grid {
      display: grid;
      gap: 3rem;
      align-items: center;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1fr);
    }
    .hero-eyebrow {
      text-transform: uppercase;
      letter-spacing: 0.22em;
      font-size: 0.75rem;
      color: #708a74;
      margin-bottom: 0.8rem;
    }
    .hero-title {
      font-size: clamp(2.2rem, 4vw, 3.1rem);
      line-height: 1.1;
      margin-bottom: 1rem;
      color: #163020;
    }
    .hero-title span.highlight {
      color: #4f6f52;
    }
    .hero-text {
      color: #4d5c4f;
      max-width: 32rem;
      font-size: 0.99rem;
      margin-bottom: 1.8rem;
    }
    .hero-badges {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      margin-bottom: 2rem;
    }
    .badge {
      font-size: 0.75rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      padding: 0.45rem 0.9rem;
      border-radius: 999px;
      border: 1px solid #dde3da;
      background: #ffffffb8;
      backdrop-filter: blur(3px);
    }
    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem;
      align-items: center;
    }
    .btn-primary {
      padding: 0.8rem 1.6rem;
      border-radius: 999px;
      border: none;
      background: #163020;
      color: #f5f7f4;
      font-size: 0.9rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      cursor: pointer;
    }
    .btn-primary:hover {
      background: #1f3b28;
    }
    .btn-outline {
      padding: 0.8rem 1.6rem;
      border-radius: 999px;
      border: 1px solid #163020;
      background: transparent;
      color: #163020;
      font-size: 0.9rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      cursor: pointer;
    }
    .btn-outline:hover {
      background: #e9f2e5;
    }
    .hero-secondary-text {
      font-size: 0.8rem;
      color: #708a74;
    }

    .hero-media {
      position: relative;
    }
    .hero-main-card {
      border-radius: 1.8rem;
      overflow: hidden;
      background: linear-gradient(145deg, #163020, #4f6f52);
      min-height: 260px;
      display: grid;
      place-items: center;
      padding: 1.5rem;
    }
    .hero-main-card::before {
      content: "";
      position: absolute;
      inset: 1.2rem;
      border-radius: 1.5rem;
      border: 1px solid rgba(255, 255, 255, 0.25);
      pointer-events: none;
    }
    .hero-main-card-inner {
      position: relative;
      z-index: 1;
      text-align: center;
      color: #f5f7f4;
    }
    .hero-main-card-inner h2 {
      font-size: 1.3rem;
      letter-spacing: 0.16em;
      text-transform: uppercase;
      margin-bottom: 0.7rem;
    }
    .hero-main-card-inner p {
      font-size: 0.9rem;
      max-width: 14rem;
      margin: 0 auto;
      opacity: 0.9;
    }
    .hero-tag {
      position: absolute;
      bottom: -0.8rem;
      right: 0.6rem;
      background: #f5f7f4;
      color: #163020;
      padding: 0.7rem 1.1rem;
      border-radius: 1rem;
      font-size: 0.75rem;
      box-shadow: 0 18px 35px rgba(0, 0, 0, 0.18);
      display: flex;
      flex-direction: column;
      gap: 0.15rem;
    }
    .hero-tag span:first-child {
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.18em;
    }
    .hero-tag span:last-child {
      font-size: 0.8rem;
      color: #4f6f52;
    }

    @media (max-width: 768px) {
      .hero-grid {
        grid-template-columns: 1fr;
      }
      .hero {
        padding-top: 2.5rem;
      }
    }

    /* --------- SERVICES --------- */
    .services-grid {
      display: grid;
      gap: 1.5rem;
      grid-template-columns: repeat(3, minmax(0, 1fr));
    }
    .service-card {
      background: #ffffff;
      padding: 1.6rem 1.5rem;
      border-radius: 1.4rem;
      border: 1px solid #dde3da;
      box-shadow: 0 12px 30px rgba(0, 0, 0, 0.03);
      display: flex;
      flex-direction: column;
      gap: 0.6rem;
    }
    .service-label {
      font-size: 0.75rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: #708a74;
    }
    .service-title {
      font-weight: 600;
      font-size: 1rem;
    }
    .service-text {
      font-size: 0.9rem;
      color: #4d5c4f;
      flex: 1;
    }
    .service-meta {
      font-size: 0.8rem;
      color: #708a74;
    }
    @media (max-width: 900px) {
      .services-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
    }
    @media (max-width: 640px) {
      .services-grid {
        grid-template-columns: 1fr;
      }
    }

    /* --------- PROJECTS --------- */
    .projects-grid {
      display: grid;
      gap: 1.5rem;
      grid-template-columns: repeat(3, minmax(0, 1fr));
    }
    .project-card {
      border-radius: 1.4rem;
      overflow: hidden;
      background: #ffffff;
      border: 1px solid #dde3da;
      display: flex;
      flex-direction: column;
    }
    .project-image {
      height: 170px;
      background-image: url("https://images.pexels.com/photos/450516/pexels-photo-450516.jpeg?auto=compress&cs=tinysrgb&w=1200");
      background-size: cover;
      background-position: center;
    }
    .project-body {
      padding: 1.1rem 1.3rem 1.3rem;
    }
    .project-name {
      font-weight: 600;
      font-size: 0.98rem;
      margin-bottom: 0.3rem;
    }
    .project-location {
      font-size: 0.8rem;
      color: #708a74;
      margin-bottom: 0.6rem;
    }
    .project-text {
      font-size: 0.88rem;
      color: #4d5c4f;
      margin-bottom: 0.6rem;
    }
    .project-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
      font-size: 0.75rem;
      color: #708a74;
    }
    .project-tags span {
      padding: 0.25rem 0.55rem;
      border-radius: 999px;
      background: #f2f6f0;
    }
    @media (max-width: 900px) {
      .projects-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
    }
    @media (max-width: 640px) {
      .projects-grid {
        grid-template-columns: 1fr;
      }
    }

    /* --------- ABOUT --------- */
    .about-grid {
      display: grid;
      gap: 2.5rem;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 0.9fr);
      align-items: center;
    }
    .about-text h3 {
      font-size: 1.2rem;
      margin-bottom: 0.7rem;
    }
    .about-text p {
      font-size: 0.95rem;
      color: #4d5c4f;
      margin-bottom: 0.7rem;
    }
    .about-stats {
      display: flex;
      flex-wrap: wrap;
      gap: 1.5rem;
      margin-top: 1rem;
    }
    .stat-item {
      min-width: 110px;
    }
    .stat-number {
      font-size: 1.6rem;
      font-weight: 700;
      color: #163020;
    }
    .stat-label {
      font-size: 0.8rem;
      color: #708a74;
      text-transform: uppercase;
      letter-spacing: 0.12em;
    }
    .about-panel {
      border-radius: 1.6rem;
      padding: 1.4rem 1.5rem;
      background: #ffffff;
      border: 1px solid #dde3da;
    }
    .about-panel h4 {
      font-size: 0.95rem;
      letter-spacing: 0.16em;
      text-transform: uppercase;
      margin-bottom: 0.8rem;
      color: #4f6f52;
    }
    .about-list {
      list-style: none;
      display: grid;
      gap: 0.65rem;
      font-size: 0.9rem;
      color: #4d5c4f;
    }
    .about-list li::before {
      content: "•";
      color: #4f6f52;
      margin-right: 0.4rem;
    }
    @media (max-width: 900px) {
      .about-grid {
        grid-template-columns: 1fr;
      }
    }

    /* --------- TESTIMONIALS --------- */
    .testimonials-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1.5rem;
    }
    .testimonial {
      background: #ffffff;
      padding: 1.3rem 1.4rem;
      border-radius: 1.4rem;
      border: 1px solid #dde3da;
      font-size: 0.9rem;
      color: #4d5c4f;
      display: flex;
      flex-direction: column;
      gap: 0.9rem;
    }
    .testimonial-quote {
      font-style: italic;
    }
    .testimonial-name {
      font-weight: 600;
      font-size: 0.9rem;
    }
    .testimonial-meta {
      font-size: 0.75rem;
      color: #708a74;
    }
    @media (max-width: 900px) {
      .testimonials-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
    }
    @media (max-width: 640px) {
      .testimonials-grid {
        grid-template-columns: 1fr;
      }
    }

    /* --------- CONTACT --------- */
    .contact-grid {
      display: grid;
      gap: 2rem;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 0.9fr);
      align-items: flex-start;
    }
    .contact-info-block {
      font-size: 0.95rem;
      color: #4d5c4f;
      display: grid;
      gap: 1rem;
    }
    .contact-info-block h3 {
      font-size: 1.2rem;
    }
    .contact-row {
      display: flex;
      flex-direction: column;
      gap: 0.15rem;
    }
    .contact-label {
      font-size: 0.75rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: #708a74;
    }
    .contact-value {
      font-size: 0.95rem;
    }
    .whatsapp-link {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      margin-top: 0.4rem;
      font-size: 0.85rem;
      text-transform: uppercase;
      letter-spacing: 0.14em;
      border-radius: 999px;
      padding: 0.6rem 1.1rem;
      border: 1px solid #163020;
    }

    .contact-form-card {
      background: #ffffff;
      padding: 1.6rem 1.5rem 1.8rem;
      border-radius: 1.6rem;
      border: 1px solid #dde3da;
      box-shadow: 0 16px 35px rgba(0, 0, 0, 0.04);
    }
    .contact-form-card h3 {
      font-size: 1rem;
      letter-spacing: 0.16em;
      text-transform: uppercase;
      margin-bottom: 1rem;
      color: #4f6f52;
    }
    .form-grid {
      display: grid;
      gap: 0.8rem;
    }
    .form-field {
      display: flex;
      flex-direction: column;
      gap: 0.35rem;
      font-size: 0.85rem;
    }
    .form-field label {
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: #708a74;
      font-size: 0.75rem;
    }
    .form-field input,
    .form-field textarea,
    .form-field select {
      border-radius: 0.9rem;
      border: 1px solid #dde3da;
      padding: 0.65rem 0.8rem;
      background: #f8faf7;
      font-size: 0.9rem;
      font-family: inherit;
      resize: vertical;
      min-height: 42px;
    }
    .form-field textarea {
      min-height: 90px;
    }
    .form-footer {
      margin-top: 1rem;
      display: flex;
      justify-content: flex-end;
    }
    @media (max-width: 900px) {
      .contact-grid {
        grid-template-columns: 1fr;
      }
    }

    /* --------- FOOTER --------- */
    footer {
      border-top: 1px solid #dde3da;
      padding: 1.5rem 0 2.2rem;
      font-size: 0.8rem;
      color: #708a74;
    }
    .footer-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      justify-content: space-between;
      align-items: center;
    }
    .footer-links {
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem;
    }
  </style>
</head>
<body>
  <!-- NAVBAR -->
  <header>
    <div class="container nav">
      <div class="logo">
        <div class="logo-mark">EG</div>
        <span>Evergreengarden Ltd</span>
      </div>

      <nav>
        <div class="nav-toggle" id="navToggle">
          <span></span><span></span><span></span>
        </div>
        <ul id="navMenu">
          <li>
            <a href="#hero">
              <span data-lang="en">Home</span>
              <span data-lang="ru" class="lang-hidden">Главная</span>
              <span data-lang="az" class="lang-hidden">Ana səhifə</span>
            </a>
          </li>
          <li>
            <a href="#services">
              <span data-lang="en">Services</span>
              <span data-lang="ru" class="lang-hidden">Услуги</span>
              <span data-lang="az" class="lang-hidden">Xidmətlər</span>
            </a>
          </li>
          <li>
            <a href="#projects">
              <span data-lang="en">Projects</span>
              <span data-lang="ru" class="lang-hidden">Проекты</span>
              <span data-lang="az" class="lang-hidden">Layihələr</span>
            </a>
          </li>
          <li>
            <a href="#about">
              <span data-lang="en">About</span>
              <span data-lang="ru" class="lang-hidden">О компании</span>
              <span data-lang="az" class="lang-hidden">Haqqımızda</span>
            </a>
          </li>
          <li>
            <a href="#contact">
              <span data-lang="en">Contact</span>
              <span data-lang="ru" class="lang-hidden">Контакты</span>
              <span data-lang="az" class="lang-hidden">Əlaqə</span>
            </a>
          </li>
          <li>
            <a href="#contact" class="nav-cta">
              <span data-lang="en">Get a quote</span>
              <span data-lang="ru" class="lang-hidden">Заказать расчёт</span>
              <span data-lang="az" class="lang-hidden">Təklif istəyin</span>
            </a>
          </li>
        </ul>

        <div class="lang-switch">
          <button class="lang-btn active-lang" data-lang-btn="en">EN</button>
          <button class="lang-btn" data-lang-btn="ru">RU</button>
          <button class="lang-btn" data-lang-btn="az">AZ</button>
        </div>
      </nav>
    </div>
  </header>

  <!-- HERO -->
  <main>
    <section class="hero section" id="hero">
      <div class="container hero-grid">
        <div>
          <div class="hero-eyebrow">
            <span data-lang="en">Premium landscape studio</span>
            <span data-lang="ru" class="lang-hidden">Премиальная студия ландшафта</span>
            <span data-lang="az" class="lang-hidden">Premium landşaft studiyası</span>
          </div>

          <h1 class="hero-title">
            <span data-lang="en">
              Evergreen gardens<br />
              for homes that <span class="highlight">never feel empty.</span>
            </span>
            <span data-lang="ru" class="lang-hidden">
              Вечнозелёные сады<br />
              для домов, которые <span class="highlight">никогда не выглядят пустыми.</span>
            </span>
            <span data-lang="az" class="lang-hidden">
              Heç vaxt <span class="highlight">boş görünməyən</span> evlər üçün həmişəyaşıl bağlar.
            </span>
          </h1>

          <p class="hero-text">
            <span data-lang="en">
              Evergreengarden Ltd designs, builds and maintains high-end gardens and outdoor
              spaces. From the first sketch to the last plant, we create landscapes that stay
              beautiful in every season.
            </span>
            <span data-lang="ru" class="lang-hidden">
              Evergreengarden Ltd проектирует, строит и обслуживает премиальные сады и
              придомовые территории. От первого эскиза до последнего кустарника — мы создаём
              ландшафт, который остаётся красивым в любое время года.
            </span>
            <span data-lang="az" class="lang-hidden">
              Evergreengarden Ltd premium bağlar və həyət məkanları layihələndirir, qurur və
              qulluq edir. İlk eskizdən son bitkiyə qədər hər fəsildə gözəl qalan landşaftlar
              yaradırıq.
            </span>
          </p>

          <div class="hero-badges">
            <div class="badge" data-lang="en">Landscape Design</div>
            <div class="badge lang-hidden" data-lang="ru">Ландшафтный дизайн</div>
            <div class="badge lang-hidden" data-lang="az">Landşaft dizaynı</div>

            <div class="badge" data-lang="en">Garden Construction</div>
            <div class="badge lang-hidden" data-lang="ru">Строительство сада</div>
            <div class="badge lang-hidden" data-lang="az">Bağın qurulması</div>

            <div class="badge" data-lang="en">Plant Supply &amp; Care</div>
            <div class="badge lang-hidden" data-lang="ru">Поставка и уход за растениями</div>
            <div class="badge lang-hidden" data-lang="az">Bitkilərin təchizatı və qulluq</div>
          </div>

          <div class="hero-actions">
            <a href="#contact">
              <button class="btn-primary">
                <span data-lang="en">Request a site visit</span>
                <span data-lang="ru" class="lang-hidden">Заказать выезд на участок</span>
                <span data-lang="az" class="lang-hidden">Sahəyə baxış sifariş et</span>
              </button>
            </a>
            <a href="#projects">
              <button class="btn-outline">
                <span data-lang="en">View recent projects</span>
                <span data-lang="ru" class="lang-hidden">Посмотреть проекты</span>
                <span data-lang="az" class="lang-hidden">Layihələrə baxın</span>
              </button>
            </a>
            <span class="hero-secondary-text">
              <span data-lang="en">Average project: 3–8 weeks, turnkey.</span>
              <span data-lang="ru" class="lang-hidden">Средний срок проекта: 3–8 недель «под ключ».</span>
              <span data-lang="az" class="lang-hidden">Orta layihə müddəti: 3–8 həftə, açar təhvil.</span>
            </span>
          </div>
        </div>

        <div class="hero-media">
          <div class="hero-main-card">
            <div class="hero-main-card-inner">
              <h2>EVERGREENGARDEN</h2>
              <p>
                <span data-lang="en">
                  Structural evergreens, seasonal color, atmospheric lighting &amp; clean lines
                  tailored to your property.
                </span>
                <span data-lang="ru" class="lang-hidden">
                  Структурные вечнозелёные растения, сезонный колорит, атмосферная подсветка и
                  чистые линии, адаптированные под ваш участок.
                </span>
                <span data-lang="az" class="lang-hidden">
                  Struktur həmişəyaşıl bitkilər, mövsümi rəng, atmosfer işıqlandırma və
                  sahənizə uyğun təmiz xətlər.
                </span>
              </p>
            </div>
            <div class="hero-tag">
              <span>Since 2008</span>
              <span data-lang="en">Evergreengarden Ltd • Landscape &amp; Garden Design • Terter / Qarabağ</span>
              <span data-lang="ru" class="lang-hidden">Evergreengarden Ltd • Ландшафт и садовый дизайн • Тертер / Карабах</span>
              <span data-lang="az" class="lang-hidden">Evergreengarden Ltd • Landşaft və bağ dizaynı • Tərtər / Qarabağ</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- SERVICES -->
    <section class="section" id="services">
      <div class="container">
        <div class="section-header">
          <h2 class="section-title">
            <span data-lang="en">Services</span>
            <span data-lang="ru" class="lang-hidden">Услуги</span>
            <span data-lang="az" class="lang-hidden">Xidmətlər</span>
          </h2>
          <p class="section-subtitle">
            <span data-lang="en">
              A complete service &mdash; from concept to fully planted and maintained garden.
            </span>
            <span data-lang="ru" class="lang-hidden">
              Полный цикл работ &mdash; от концепции до полностью засаженного и ухоженного сада.
            </span>
            <span data-lang="az" class="lang-hidden">
              Konsepsiyadan tam əkilmiş və qulluq olunan bağa qədər tam xidmət paketi.
            </span>
          </p>
        </div>

        <div class="services-grid">
          <article class="service-card">
            <div class="service-label">
              <span>01</span>
              <span data-lang="en"> • Design</span>
              <span data-lang="ru" class="lang-hidden"> • Дизайн</span>
              <span data-lang="az" class="lang-hidden"> • Dizayn</span>
            </div>
            <h3 class="service-title">
              <span data-lang="en">Landscape &amp; garden design</span>
              <span data-lang="ru" class="lang-hidden">Ландшафтный и садовый дизайн</span>
              <span data-lang="az" class="lang-hidden">Landşaft və bağ dizaynı</span>
            </h3>
            <p class="service-text">
              <span data-lang="en">
                Site analysis, concept plans, 2D/3D visualizations and planting schemes
                tailored to climate, architecture and lifestyle.
              </span>
              <span data-lang="ru" class="lang-hidden">
                Анализ участка, концептуальные планы, 2D/3D-визуализации и посадочные схемы
                с учётом климата, архитектуры и образа жизни.
              </span>
              <span data-lang="az" class="lang-hidden">
                Sahənin analizi, konsept planlar, 2D/3D vizuallaşdırmalar və iqlimə,
                memarlığa və həyat tərzinə uyğun əkilmə sxemləri.
              </span>
            </p>
            <div class="service-meta">
              <span data-lang="en">Ideal for new homes, villas, public and commercial spaces.</span>
              <span data-lang="ru" class="lang-hidden">Идеально для новых домов, вилл, общественных и коммерческих территорий.</span>
              <span data-lang="az" class="lang-hidden">Yeni evlər, villalar, ictimai və kommersiya sahələri üçün idealdır.</span>
            </div>
          </article>

          <article class="service-card">
            <div class="service-label">
              <span>02</span>
              <span data-lang="en"> • Build</span>
              <span data-lang="ru" class="lang-hidden"> • Строительство</span>
              <span data-lang="az" class="lang-hidden"> • Tikinti</span>
            </div>
            <h3 class="service-title">
              <span data-lang="en">Turnkey garden construction</span>
              <span data-lang="ru" class="lang-hidden">Строительство сада «под ключ»</span>
              <span data-lang="az" class="lang-hidden">Bağın “açar təhvil” qurulması</span>
            </h3>
            <p class="service-text">
              <span data-lang="en">
                Hardscape, planting, irrigation, lighting and garden structures. We manage
                the entire build so you work with one team from start to finish.
              </span>
              <span data-lang="ru" class="lang-hidden">
                Дорожки и мощение, посадка, полив, освещение и садовые конструкции. Мы
                берём на себя весь процесс, и вы работаете с одной командой от начала до конца.
              </span>
              <span data-lang="az" class="lang-hidden">
                Sert örtük işləri, əkilmə, suvarma sistemi, işıqlandırma və bağ konstruksiyaları.
                Bütün prosesi bir komanda olaraq idarə edirik.
              </span>
            </p>
            <div class="service-meta">
              <span data-lang="en">Reliable timelines, clear budgets, professional crew.</span>
              <span data-lang="ru" class="lang-hidden">Чёткие сроки, прозрачный бюджет, профессиональная команда.</span>
              <span data-lang="az" class="lang-hidden">Dəqiq müddətlər, şəffaf büdcə, peşəkar komanda.</span>
            </div>
          </article>

          <article class="service-card">
            <div class="service-label">
              <span>03</span>
              <span data-lang="en"> • Care</span>
              <span data-lang="ru" class="lang-hidden"> • Уход</span>
              <span data-lang="az" class="lang-hidden"> • Qulluq</span>
            </div>
            <h3 class="service-title">
              <span data-lang="en">Maintenance &amp; plant care</span>
              <span data-lang="ru" class="lang-hidden">Обслуживание и уход за садом</span>
              <span data-lang="az" class="lang-hidden">Bağa servis və bitkilərə qulluq</span>
            </h3>
            <p class="service-text">
              <span data-lang="en">
                Seasonal pruning, fertilising, pest control and plant replacement to keep your
                garden looking as fresh as day one.
              </span>
              <span data-lang="ru" class="lang-hidden">
                Сезонная обрезка, удобрения, защита от вредителей и замена растений, чтобы
                сад выглядел свежим как в первый день.
              </span>
              <span data-lang="az" class="lang-hidden">
                Mövsümi budama, gübrələmə, zərərvericilərə qarşı mübarizə və bitki yenilənməsi
                sayəsində bağınız həmişə ilk günkü kimi qalır.
              </span>
            </p>
            <div class="service-meta">
              <span data-lang="en">Available as weekly, monthly or seasonal care plans.</span>
              <span data-lang="ru" class="lang-hidden">Доступны недельные, месячные и сезонные программы ухода.</span>
              <span data-lang="az" class="lang-hidden">Həftəlik, aylıq və mövsümi qulluq paketləri mövcuddur.</span>
            </div>
          </article>
        </div>
      </div>
    </section>

    <!-- PROJECTS -->
    <section class="section" id="projects">
      <div class="container">
        <div class="section-header">
          <h2 class="section-title">
            <span data-lang="en">Selected projects</span>
            <span data-lang="ru" class="lang-hidden">Примеры проектов</span>
            <span data-lang="az" class="lang-hidden">Seçilmiş layihələr</span>
          </h2>
          <p class="section-subtitle">
            <span data-lang="en">
              A glimpse into the type of outdoor spaces we create for our clients.
            </span>
            <span data-lang="ru" class="lang-hidden">
              Небольшой обзор тех уличных пространств, которые мы создаём для клиентов.
            </span>
            <span data-lang="az" class="lang-hidden">
              Müştərilərimiz üçün yaratdığımız açıq məkanlara qısa baxış.
            </span>
          </p>
        </div>

        <div class="projects-grid">
          <article class="project-card">
            <div class="project-image"></div>
            <div class="project-body">
              <div class="project-name">
                <span data-lang="en">Evergreen Courtyard</span>
                <span data-lang="ru" class="lang-hidden">Вечнозелёный дворик</span>
                <span data-lang="az" class="lang-hidden">Həmişəyaşıl həyət</span>
              </div>
              <div class="project-location">
                <span data-lang="en">Private villa &bullet; 300 m²</span>
                <span data-lang="ru" class="lang-hidden">Частная вилла &bullet; 300 m²</span>
                <span data-lang="az" class="lang-hidden">Fərdi villa &bullet; 300 m²</span>
              </div>
              <p class="project-text">
                <span data-lang="en">
                  Minimalist patio with evergreen structure, scented shrubs and discreet
                  lighting for late dinners outside.
                </span>
                <span data-lang="ru" class="lang-hidden">
                  Минималистичный внутренний двор с вечнозелёной структурой, ароматными
                  кустарниками и мягкой подсветкой для вечерних ужинов на улице.
                </span>
                <span data-lang="az" class="lang-hidden">
                  Həmişəyaşıl struktura, ətirli kollar və axşam yeməkləri üçün zərif işıqlandırma
                  ilə minimalist həyət.
                </span>
              </p>
              <div class="project-tags">
                <span data-lang="en">Courtyard</span>
                <span data-lang="ru" class="lang-hidden">Внутренний двор</span>
                <span data-lang="az" class="lang-hidden">Həyət</span>

                <span data-lang="en">Lighting</span>
                <span data-lang="ru" class="lang-hidden">Подсветка</span>
                <span data-lang="az" class="lang-hidden">İşıqlandırma</span>

                <span data-lang="en">Irrigation</span>
                <span data-lang="ru" class="lang-hidden">Полив</span>
                <span data-lang="az" class="lang-hidden">Suvarma</span>
              </div>
            </div>
          </article>

          <article class="project-card">
            <div class="project-image" style="background-image: url('https://images.pexels.com/photos/450516/pexels-photo-450516.jpeg?auto=compress&cs=tinysrgb&w=1200');"></div>
            <div class="project-body">
              <div class="project-name">
                <span data-lang="en">Family Garden with Play Zone</span>
                <span data-lang="ru" class="lang-hidden">Семейный сад с зоной для детей</span>
                <span data-lang="az" class="lang-hidden">Uşaq meydançası olan ailə bağı</span>
              </div>
              <div class="project-location">
                <span data-lang="en">Residential garden &bullet; 500 m²</span>
                <span data-lang="ru" class="lang-hidden">Частный сад &bullet; 500 m²</span>
                <span data-lang="az" class="lang-hidden">Fərdi bağ &bullet; 500 m²</span>
              </div>
              <p class="project-text">
                <span data-lang="en">
                  Functional garden combining a safe children's play area with lush green
                  borders, lawn and shade trees.
                </span>
                <span data-lang="ru" class="lang-hidden">
                  Функциональный сад, сочетающий безопасную детскую площадку с зелёными
                  бордюрами, газоном и теневыми деревьями.
                </span>
                <span data-lang="az" class="lang-hidden">
                  Təhlükəsiz uşaq zonasını sıx yaşıl haşiyələr, çəmənlik və kölgə ağacları ilə
                  birləşdirən funksional bağ.
                </span>
              </p>
              <div class="project-tags">
                <span data-lang="en">Family</span>
                <span data-lang="ru" class="lang-hidden">Семья</span>
                <span data-lang="az" class="lang-hidden">Ailə</span>

                <span data-lang="en">Playground</span>
                <span data-lang="ru" class="lang-hidden">Игровая зона</span>
                <span data-lang="az" class="lang-hidden">Uşaq meydançası</span>

                <span data-lang="en">Lawn</span>
                <span data-lang="ru" class="lang-hidden">Газон</span>
                <span data-lang="az" class="lang-hidden">Çəmənlik</span>
              </div>
            </div>
          </article>

          <article class="project-card">
            <div class="project-image" style="background-image: url('https://images.pexels.com/photos/1400375/pexels-photo-1400375.jpeg?auto=compress&cs=tinysrgb&w=1200');"></div>
            <div class="project-body">
              <div class="project-name">
                <span data-lang="en">Evergreen Entrance</span>
                <span data-lang="ru" class="lang-hidden">Зелёный вход</span>
                <span data-lang="az" class="lang-hidden">Həmişəyaşıl giriş</span>
              </div>
              <div class="project-location">
                <span data-lang="en">Commercial facade</span>
                <span data-lang="ru" class="lang-hidden">Коммерческий фасад</span>
                <span data-lang="az" class="lang-hidden">Kommersiya fasadı</span>
              </div>
              <p class="project-text">
                <span data-lang="en">
                  Strong first impression with containers, topiary and lighting guiding
                  visitors to the main entrance.
                </span>
                <span data-lang="ru" class="lang-hidden">
                  Сильное первое впечатление за счёт контейнерных посадок, топиара и подсветки,
                  направляющей гостей к главному входу.
                </span>
                <span data-lang="az" class="lang-hidden">
                  Ziyarətçiləri əsas girişə yönləndirən dekorativ qablar, topiarlar və
                  işıqlandırma ilə güclü ilk təəssürat.
                </span>
              </p>
              <div class="project-tags">
                <span data-lang="en">Commercial</span>
                <span data-lang="ru" class="lang-hidden">Коммерция</span>
                <span data-lang="az" class="lang-hidden">Kommersiya</span>

                <span data-lang="en">Containers</span>
                <span data-lang="ru" class="lang-hidden">Контейнеры</span>
                <span data-lang="az" class="lang-hidden">Qablarda əkilmə</span>

                <span data-lang="en">All-year interest</span>
                <span data-lang="ru" class="lang-hidden">Круглогодичный интерес</span>
                <span data-lang="az" class="lang-hidden">İlboyu dekorativlik</span>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section class="section" id="about">
      <div class="container">
        <div class="section-header">
          <h2 class="section-title">
            <span data-lang="en">About Evergreengarden Ltd</span>
            <span data-lang="ru" class="lang-hidden">О компании Evergreengarden Ltd</span>
            <span data-lang="az" class="lang-hidden">Evergreengarden Ltd haqqında</span>
          </h2>
          <p class="section-subtitle">
            <span data-lang="en">
              A boutique landscape company focused on long-lasting, evergreen beauty.
            </span>
            <span data-lang="ru" class="lang-hidden">
              Бутиковая ландшафтная компания, сфокусированная на долговечной, вечнозелёной красоте.
            </span>
            <span data-lang="az" class="lang-hidden">
              Uzunömürlü, həmişəyaşıl gözəlliyə fokuslanan butik landşaft şirkəti.
            </span>
          </p>
        </div>

        <div class="about-grid">
          <div class="about-text">
            <h3>
              <span data-lang="en">We create gardens that age beautifully.</span>
              <span data-lang="ru" class="lang-hidden">Мы создаём сады, которые красиво взрослеют.</span>
              <span data-lang="az" class="lang-hidden">Biz illərlə gözəlləşən bağlar yaradırıq.</span>
            </h3>
            <p>
              <span data-lang="en">
                Evergreengarden Ltd brings together designers, plant specialists and
                experienced construction teams. We fully coordinate each project &mdash; from
                the first meeting on site to the moment you walk into your finished garden.
              </span>
              <span data-lang="ru" class="lang-hidden">
                Evergreengarden Ltd объединяет дизайнеров, специалистов по растениям и опытные
                строительные бригады. Мы сопровождаем каждый проект от первой встречи на участке
                до момента, когда вы выходите в готовый сад.
              </span>
              <span data-lang="az" class="lang-hidden">
                Evergreengarden Ltd dizaynerləri, bitki mütəxəssislərini və təcrübəli tikinti
                komandalarını bir araya gətirir. Hər bir layihəni sahədə ilk görüşdən hazır
                bağa qədər tam şəkildə koordinasiya edirik.
              </span>
            </p>
            <p>
              <span data-lang="en">
                Our approach is simple: listen carefully, design with precision, build with
                respect for your property, and choose plants that will thrive in your local
                climate for many years.
              </span>
              <span data-lang="ru" class="lang-hidden">
                Наш подход прост: внимательно слушать, тщательно проектировать, аккуратно
                строить и подбирать растения, которые будут чувствовать себя комфортно в вашем
                климате долгие годы.
              </span>
              <span data-lang="az" class="lang-hidden">
                Yanaşmamız sadədir: diqqətlə dinləmək, dəqiq layihələndirmək, sahənizə hörmətlə
                tikinti aparmaq və yerli iqlimdə uzun illər inkişaf edəcək bitkilər seçmək.
              </span>
            </p>
            <div class="about-stats">
              <div class="stat-item">
                <div class="stat-number">17+</div>
                <div class="stat-label">
                  <span data-lang="en">Years of work</span>
                  <span data-lang="ru" class="lang-hidden">Лет работы</span>
                  <span data-lang="az" class="lang-hidden">İllik təcrübə</span>
                </div>
              </div>
              <div class="stat-item">
                <div class="stat-number">80+</div>
                <div class="stat-label">
                  <span data-lang="en">Completed gardens</span>
                  <span data-lang="ru" class="lang-hidden">Реализованных садов</span>
                  <span data-lang="az" class="lang-hidden">Tamamlanmış bağlar</span>
                </div>
              </div>
              <div class="stat-item">
                <div class="stat-number">90%</div>
                <div class="stat-label">
                  <span data-lang="en">Repeat clients</span>
                  <span data-lang="ru" class="lang-hidden">Повторные клиенты</span>
                  <span data-lang="az" class="lang-hidden">Təkrar müştərilər</span>
                </div>
              </div>
            </div>
          </div>

          <aside class="about-panel">
            <h4>
              <span data-lang="en">What you can expect</span>
              <span data-lang="ru" class="lang-hidden">Что вы получаете</span>
              <span data-lang="az" class="lang-hidden">Nələr əldə edirsiniz</span>
            </h4>
            <ul class="about-list">
              <li>
                <span data-lang="en">Clear, detailed proposals without hidden costs.</span>
                <span data-lang="ru" class="lang-hidden">Понятные и подробные сметы без скрытых расходов.</span>
                <span data-lang="az" class="lang-hidden">Gizli xərclərsiz, aydın və detallı təkliflər.</span>
              </li>
              <li>
                <span data-lang="en">Designs adapted to your architecture and lifestyle.</span>
                <span data-lang="ru" class="lang-hidden">Дизайн, адаптированный под вашу архитектуру и образ жизни.</span>
                <span data-lang="az" class="lang-hidden">Memarlığa və həyat tərzinizə uyğun dizayn.</span>
              </li>
              <li>
                <span data-lang="en">Planting schemes that stay green and structured all year.</span>
                <span data-lang="ru" class="lang-hidden">Посадочные схемы, которые выглядят структурно и зелено круглый год.</span>
                <span data-lang="az" class="lang-hidden">İlboyu struktur və həmişəyaşıl qalan əkilmə sxemləri.</span>
              </li>
              <li>
                <span data-lang="en">Professional communication and clean, respectful work on site.</span>
                <span data-lang="ru" class="lang-hidden">Профессиональное общение и аккуратная работа на объекте.</span>
                <span data-lang="az" class="lang-hidden">Peşəkar kommunikasiya və sahədə səliqəli, hörmətli iş.</span>
              </li>
              <li>
                <span data-lang="en">Optional long-term maintenance after completion.</span>
                <span data-lang="ru" class="lang-hidden">При желании — долгосрочное обслуживание после сдачи проекта.</span>
                <span data-lang="az" class="lang-hidden">Layihə bitdikdən sonra uzunmüddətli qulluq imkanı.</span>
              </li>
            </ul>
          </aside>
        </div>
      </div>
    </section>

    <!-- TESTIMONIALS -->
    <section class="section" id="testimonials">
      <div class="container">
        <div class="section-header">
          <h2 class="section-title">
            <span data-lang="en">What clients say</span>
            <span data-lang="ru" class="lang-hidden">Отзывы клиентов</span>
            <span data-lang="az" class="lang-hidden">Müştərilərin rəyləri</span>
          </h2>
          <p class="section-subtitle">
            <span data-lang="en">
              A few words from homeowners and businesses who trusted us with their outdoor spaces.
            </span>
            <span data-lang="ru" class="lang-hidden">
              Несколько слов от частных и корпоративных клиентов, доверивших нам свои территории.
            </span>
            <span data-lang="az" class="lang-hidden">
              Açıq məkanlarını bizə etibar edən fərdi və korporativ müştərilərimizin fikirləri.
            </span>
          </p>
        </div>

        <div class="testimonials-grid">
          <article class="testimonial">
            <p class="testimonial-quote">
              <span data-lang="en">
                “Evergreengarden transformed a plain yard into our favourite room of the house.
                The garden looks beautiful from every window.”
              </span>
              <span data-lang="ru" class="lang-hidden">
                «Evergreengarden превратили обычный двор в нашу любимую “комнату” дома.
                Сад красиво смотрится из каждого окна».
              </span>
              <span data-lang="az" class="lang-hidden">
                “Evergreengarden adi həyəti evimizin ən sevimli “otağına” çevirdi.
                Bağ hər pəncərədən möhtəşəm görünür.”
              </span>
            </p>
            <div>
              <div class="testimonial-name">
                <span data-lang="en">Private client</span>
                <span data-lang="ru" class="lang-hidden">Частный клиент</span>
                <span data-lang="az" class="lang-hidden">Fərdi müştəri</span>
              </div>
              <div class="testimonial-meta">
                <span data-lang="en">Residential garden</span>
                <span data-lang="ru" class="lang-hidden">Частный сад</span>
                <span data-lang="az" class="lang-hidden">Fərdi bağ</span>
              </div>
            </div>
          </article>

          <article class="testimonial">
            <p class="testimonial-quote">
              <span data-lang="en">
                “From design to final planting, everything was clear, on schedule and
                professionally managed. We continue working with them for maintenance.”
              </span>
              <span data-lang="ru" class="lang-hidden">
                «От проекта до финальной посадки всё было понятно, в срок и очень профессионально.
                Сейчас продолжаем работать по обслуживанию сада».
              </span>
              <span data-lang="az" class="lang-hidden">
                “Layihədən son əkilməyə qədər hər şey aydın, vaxtında və peşəkar şəkildə oldu.
                İndi də bağın servisi üçün onlarla işləməyə davam edirik.”
              </span>
            </p>
            <div>
              <div class="testimonial-name">
                <span data-lang="en">Villa owner</span>
                <span data-lang="ru" class="lang-hidden">Владелец виллы</span>
                <span data-lang="az" class="lang-hidden">Villa sahibi</span>
              </div>
              <div class="testimonial-meta">
                <span data-lang="en">Full garden renovation</span>
                <span data-lang="ru" class="lang-hidden">Полная реконструкция сада</span>
                <span data-lang="az" class="lang-hidden">Bağın tam yenilənməsi</span>
              </div>
            </div>
          </article>

          <article class="testimonial">
            <p class="testimonial-quote">
              <span data-lang="en">
                “Our entrance now reflects the quality of our brand. Clients notice the
                greenery immediately when they arrive.”
              </span>
              <span data-lang="ru" class="lang-hidden">
                «Теперь вход в наш офис отражает уровень бренда. Клиенты сразу обращают
                внимание на зелёное оформление».
              </span>
              <span data-lang="az" class="lang-hidden">
                “Artıq ofisimizin girişi brendimizin keyfiyyətini əks etdirir.
                Müştərilər gələn kimi yaşıllığı hiss edirlər.”
              </span>
            </p>
            <div>
              <div class="testimonial-name">
                <span data-lang="en">Business client</span>
                <span data-lang="ru" class="lang-hidden">Корпоративный клиент</span>
                <span data-lang="az" class="lang-hidden">Biznes müştərisi</span>
              </div>
              <div class="testimonial-meta">
                <span data-lang="en">Commercial landscape</span>
                <span data-lang="ru" class="lang-hidden">Коммерческий ландшафт</span>
                <span data-lang="az" class="lang-hidden">Kommersiya landşaftı</span>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section class="section" id="contact">
      <div class="container">
        <div class="section-header">
          <h2 class="section-title">
            <span data-lang="en">Contact &amp; site visit</span>
            <span data-lang="ru" class="lang-hidden">Контакты и выезд на участок</span>
            <span data-lang="az" class="lang-hidden">Əlaqə və sahəyə baxış</span>
          </h2>
          <p class="section-subtitle">
            <span data-lang="en">
              Tell us about your space, and we’ll get back with a short proposal and available dates.
            </span>
            <span data-lang="ru" class="lang-hidden">
              Расскажите немного об участке, и мы подготовим короткое предложение и варианты дат.
            </span>
            <span data-lang="az" class="lang-hidden">
              Sahəniz barədə qısa məlumat verin, biz isə sizə təklif və uyğun tarixlərlə geri dönək.
            </span>
          </p>
        </div>

        <div class="contact-grid">
          <div class="contact-info-block">
            <h3>
              <span data-lang="en">Let’s plan your evergreen garden</span>
              <span data-lang="ru" class="lang-hidden">Давайте спланируем ваш вечнозелёный сад</span>
              <span data-lang="az" class="lang-hidden">Gəlin həmişəyaşıl bağınızı planlayaq</span>
            </h3>
            <p>
              <span data-lang="en">
                Share a few details about your property and your ideas. We usually respond
                within one business day to arrange a call or a site visit.
              </span>
              <span data-lang="ru" class="lang-hidden">
                Напишите несколько деталей о вашем участке и ожиданиях. Обычно мы отвечаем
                в течение одного рабочего дня, чтобы согласовать звонок или выезд.
              </span>
              <span data-lang="az" class="lang-hidden">
                Sahəniz və istəkləriniz barədə qısa məlumat göndərin. Adətən bir iş günü ərzində
                zəng və ya sahəyə baxış üçün sizinlə əlaqə saxlayırıq.
              </span>
            </p>

            <div class="contact-row">
              <span class="contact-label">
                <span data-lang="en">Email</span>
                <span data-lang="ru" class="lang-hidden">E-mail</span>
                <span data-lang="az" class="lang-hidden">E-poçt</span>
              </span>
              <span class="contact-value">
                <a href="mailto:nizamiabdullayev@yahoo.com">nizamiabdullayev@yahoo.com</a>
              </span>
            </div>

            <div class="contact-row">
              <span class="contact-label">
                <span data-lang="en">Phone</span>
                <span data-lang="ru" class="lang-hidden">Телефон</span>
                <span data-lang="az" class="lang-hidden">Telefon</span>
              </span>
              <span class="contact-value">
                <a href="tel:+994502446600">+994 50 244 66 00</a>
              </span>
              <a class="whatsapp-link" href="https://wa.me/994502446600" target="_blank" rel="noopener">
                <span data-lang="en">WhatsApp • Send photos of your site</span>
                <span data-lang="ru" class="lang-hidden">WhatsApp • Отправить фото участка</span>
                <span data-lang="az" class="lang-hidden">WhatsApp • Sahənin fotolarını göndərin</span>
              </a>
            </div>

            <div class="contact-row">
              <span class="contact-label">
                <span data-lang="en">Company</span>
                <span data-lang="ru" class="lang-hidden">Компания</span>
                <span data-lang="az" class="lang-hidden">Şirkət</span>
              </span>
              <span class="contact-value">
                Evergreengarden Ltd<br />
                <span data-lang="en">Landscape &amp; Garden Design</span>
                <span data-lang="ru" class="lang-hidden">Ландшафт и садовый дизайн</span>
                <span data-lang="az" class="lang-hidden">Landşaft və bağ dizaynı</span>
              </span>
            </div>

            <div class="contact-row">
              <span class="contact-label">
                <span data-lang="en">Service area</span>
                <span data-lang="ru" class="lang-hidden">Регион работы</span>
                <span data-lang="az" class="lang-hidden">Xidmət göstərdiyimiz ərazi</span>
              </span>
              <span class="contact-value">
                <span data-lang="en">Terter / Qarabağ region and nearby territories.</span>
                <span data-lang="ru" class="lang-hidden">Регион Тертер / Карабах и ближайшие районы.</span>
                <span data-lang="az" class="lang-hidden">Tərtər / Qarabağ regionu və yaxın ərazilər.</span>
              </span>
            </div>
          </div>

          <div class="contact-form-card">
            <h3>
              <span data-lang="en">Send us a message</span>
              <span data-lang="ru" class="lang-hidden">Написать нам</span>
              <span data-lang="az" class="lang-hidden">Bizə yazın</span>
            </h3>
            <!-- NOTE: This form sends nowhere yet; needs backend or service like Formspree -->
            <form>
              <div class="form-grid">
                <div class="form-field">
                  <label for="name">
                    <span data-lang="en">Name</span>
                    <span data-lang="ru" class="lang-hidden">Имя</span>
                    <span data-lang="az" class="lang-hidden">Ad, soyad</span>
                  </label>
                  <input id="name" type="text"
                    placeholder="Your full name" />
                </div>
                <div class="form-field">
                  <label for="email">
                    <span data-lang="en">Email</span>
                    <span data-lang="ru" class="lang-hidden">E-mail</span>
                    <span data-lang="az" class="lang-hidden">E-poçt</span>
                  </label>
                  <input id="email" type="email"
                    placeholder="you@example.com" />
                </div>
                <div class="form-field">
                  <label for="phone">
                    <span data-lang="en">Phone / WhatsApp</span>
                    <span data-lang="ru" class="lang-hidden">Телефон / WhatsApp</span>
                    <span data-lang="az" class="lang-hidden">Telefon / WhatsApp</span>
                  </label>
                  <input id="phone" type="tel"
                    placeholder="+994 ..." />
                </div>
                <div class="form-field">
                  <label for="service">
                    <span data-lang="en">Service type</span>
                    <span data-lang="ru" class="lang-hidden">Тип услуги</span>
                    <span data-lang="az" class="lang-hidden">Xidmət növü</span>
                  </label>
                  <select id="service">
                    <option data-lang="en">Landscape design</option>
                    <option data-lang="ru" class="lang-hidden">Ландшафтный дизайн</option>
                    <option data-lang="az" class="lang-hidden">Landşaft dizaynı</option>

                    <option data-lang="en">Full design &amp; build</option>
                    <option data-lang="ru" class="lang-hidden">Проектирование и строительство</option>
                    <option data-lang="az" class="lang-hidden">Layihə + tikinti</option>

                    <option data-lang="en">Garden maintenance</option>
                    <option data-lang="ru" class="lang-hidden">Обслуживание сада</option>
                    <option data-lang="az" class="lang-hidden">Bağa qulluq</option>

                    <option data-lang="en">Plant selection / consulting</option>
                    <option data-lang="ru" class="lang-hidden">Подбор растений / консультация</option>
                    <option data-lang="az" class="lang-hidden">Bitki seçimi / konsultasiya</option>
                  </select>
                </div>
                <div class="form-field">
                  <label for="message">
                    <span data-lang="en">Project details</span>
                    <span data-lang="ru" class="lang-hidden">Кратко о проекте</span>
                    <span data-lang="az" class="lang-hidden">Layihə barədə məlumat</span>
                  </label>
                  <textarea id="message"
                    placeholder="Tell us about your garden, size, photos, deadlines..."></textarea>
                </div>
              </div>
              <div class="form-footer">
                <button type="submit" class="btn-primary">
                  <span data-lang="en">Send request</span>
                  <span data-lang="ru" class="lang-hidden">Отправить заявку</span>
                  <span data-lang="az" class="lang-hidden">Sorğunu göndər</span>
                </button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </section>
  </main>

  <!-- FOOTER -->
  <footer>
    <div class="container footer-grid">
      <div>
        © <span id="year"></span> Evergreengarden Ltd.
        <span data-lang="en">All rights reserved.</span>
        <span data-lang="ru" class="lang-hidden">Все права защищены.</span>
        <span data-lang="az" class="lang-hidden">Bütün hüquqlar qorunur.</span>
      </div>
      <div class="footer-links">
        <span data-lang="en">Landscape &amp; Garden Design Studio • Terter / Qarabağ</span>
        <span data-lang="ru" class="lang-hidden">Студия ландшафта и сада • Тертер / Карабах</span>
        <span data-lang="az" class="lang-hidden">Landşaft və bağ studiyası • Tərtər / Qarabağ</span>
      </div>
    </div>
  </footer>

  <script>
    // Mobile nav toggle
    const navToggle = document.getElementById("navToggle");
    const navMenu = document.getElementById("navMenu");
    if (navToggle) {
      navToggle.addEventListener("click", () => {
        navMenu.classList.toggle("open");
      });

      // Close mobile menu on link click
      document.querySelectorAll("#navMenu a").forEach(link => {
        link.addEventListener("click", () => navMenu.classList.remove("open"));
      });
    }

    // Language switching
    const langButtons = document.querySelectorAll("[data-lang-btn]");
    const langElements = document.querySelectorAll("[data-lang]");

    function setLanguage(lang) {
      document.documentElement.setAttribute("lang", lang);
      // Toggle text elements
      langElements.forEach(el => {
        if (el.dataset.lang === lang) {
          el.classList.remove("lang-hidden");
        } else {
          el.classList.add("lang-hidden");
        }
      });
      // Toggle buttons
      langButtons.forEach(btn => {
        btn.classList.toggle("active-lang", btn.dataset.langBtn === lang);
      });
      // Save preference
      try {
        localStorage.setItem("egLang", lang);
      } catch (e) {}
    }

    langButtons.forEach(btn => {
      btn.addEventListener("click", () => setLanguage(btn.dataset.langBtn));
    });

    // Load saved language or default EN
    (function initLanguage() {
      let saved = "en";
      try {
        saved = localStorage.getItem("egLang") || "en";
      } catch (e) {}
      setLanguage(saved);
    })();

    // Set current year
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
