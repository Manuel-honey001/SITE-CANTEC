<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>CENTEC – Centre de Formation & Géomatique</title>

  <meta name="description" content="CENTEC - Formation en SIG, télédétection, drones et géomatique en Afrique francophone." />

  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" />

  <style>
    :root {
      --primary:#0b5ed7;
      --secondary:#198754;
      --dark:#111;
      --text:#222;
      --bg:#f5f7fa;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Segoe UI, sans-serif;
      color: var(--text);
      background: white;
      line-height: 1.6;
    }

    html {
      scroll-behavior: smooth;
    }

    /* ===== HEADER ===== */
    header {
      position: sticky;
      top: 0;
      z-index: 1000;
      background: linear-gradient(135deg,#7ec8ff,#2ea3ff);
      color: white;
      padding: 1rem;
    }

    .container {
      max-width: 1200px;
      margin: auto;
    }

    nav {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 10px;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-weight: 600;
      padding: 5px 8px;
    }

    /* ===== HERO ===== */
    .hero {
      background: linear-gradient(rgba(0,0,0,0.5),rgba(0,0,0,0.5)),
      url('https://images.unsplash.com/photo-1504384308090-c894fdcc538d');
      background-size: cover;
      background-position: center;
      color: white;
      text-align: center;
      padding: 5rem 1rem;
    }

    /* ===== SECTIONS ===== */
    section {
      padding: 3rem 1rem;
      max-width: 1200px;
      margin: auto;
    }

    h2 {
      font-size: 1.8rem;
      margin-bottom: 1rem;
    }

    h2::after {
      content: "";
      width: 60px;
      height: 4px;
      background: var(--primary);
      display: block;
      margin-top: 6px;
      border-radius: 10px;
    }

    /* ===== GRID ===== */
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(240px,1fr));
      gap: 1.2rem;
    }

    /* ===== CARDS ===== */
    .card {
      background: white;
      border-radius: 16px;
      padding: 1.2rem;
      box-shadow: 0 10px 25px rgba(0,0,0,0.08);
      transition: 0.3s;
    }

    .card:hover {
      transform: translateY(-6px);
    }

    .program-banner {
      height: 120px;
      background: #ddd;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 10px;
      margin-bottom: 10px;
      font-weight: bold;
    }

    .badge {
      background: var(--primary);
      color: white;
      padding: 4px 10px;
      border-radius: 20px;
      font-size: 12px;
    }

    /* ===== BUTTON ===== */
    .btn {
      display: inline-block;
      background: var(--secondary);
      color: white;
      padding: 10px 18px;
      border-radius: 30px;
      text-decoration: none;
      font-weight: bold;
      margin-top: 10px;
    }

    /* ===== WHATSAPP ===== */
    .cta-whatsapp {
      position: fixed;
      bottom: 15px;
      right: 15px;
      background: #25D366;
      color: white;
      padding: 12px 14px;
      border-radius: 50px;
      font-weight: bold;
      text-decoration: none;
      font-size: 14px;
    }

    /* ===== FOOTER ===== */
    footer {
      background: var(--dark);
      color: white;
      text-align: center;
      padding: 2rem 1rem;
    }

    footer a {
      color: white;
      margin: 0 10px;
      text-decoration: none;
    }

    /* ===== MOBILE FIX ===== */
    @media (max-width: 768px) {

      header {
        text-align: center;
      }

      nav {
        justify-content: center;
      }

      .hero {
        padding: 4rem 1rem;
      }

      h2 {
        font-size: 1.5rem;
      }

      .card {
        padding: 1rem;
      }

      .cta-whatsapp {
        font-size: 12px;
        padding: 10px 12px;
      }
    }

  </style>
</head>

<body>

<header>
  <div class="container">
    <h1>CENTEC</h1>
    <nav>
      <a href="#accueil">Accueil</a>
      <a href="#apropos">À propos</a>
      <a href="#equipe">Équipe</a>
      <a href="#programmes">Programmes</a>
      <a href="#seminaires">Séminaires</a>
      <a href="#contact">Contact</a>
    </nav>
  </div>
</header>

<section class="hero" id="accueil">
  <h2>Former les experts de la géomatique</h2>
  <p>SIG, drones, cartographie et analyse territoriale</p>
  <a class="btn" href="#programmes">Découvrir</a>
</section>

<section id="apropos">
  <h2>À propos</h2>
  <p>CENTEC forme des professionnels en géomatique appliquée avec une approche pratique et moderne.</p>
</section>

<!-- ÉQUIPE -->
<section id="equipe">
  <h2>Notre équipe</h2>

  <div class="grid">
    <div class="card"><h3>Expert SIG</h3><p>Analyse spatiale et systèmes d’information géographique.</p></div>
    <div class="card"><h3>Spécialiste Drones</h3><p>Acquisition et traitement de données aériennes.</p></div>
    <div class="card"><h3>Data Analyst</h3><p>Visualisation et interprétation des données.</p></div>
    <div class="card"><h3>Formateur</h3><p>Accompagnement pédagogique des étudiants.</p></div>
  </div>
</section>

<section id="programmes">
  <h2>Programmes</h2>

  <div class="grid">

    <div class="card">
      <div class="program-banner">DIGI MAP</div>
      <h3>DIGI MAP</h3>
      <span class="badge">SIG</span>
      <p>Cartographie numérique de débutant à expert</p>
    </div>

    <div class="card">
      <div class="program-banner">TeleSense</div>
      <h3>Télédétection</h3>
      <span class="badge">Drones</span>
      <p>Analyse d’images satellites et drones</p>
    </div>

  </div>
</section>

<section id="seminaires">
  <h2>Séminaires</h2>

  <div class="grid">
    <div class="card">
      <h3>Webmapping</h3>
      <p>Création de cartes interactives</p>
      <a class="btn" href="#contact">S'inscrire</a>
    </div>

    <div class="card">
      <h3>Drones</h3>
      <p>Pratique terrain</p>
      <a class="btn" href="#contact">Réserver</a>
    </div>
  </div>
</section>

<section id="contact">
  <h2>Contact</h2>

  <form action="https://formsubmit.co/centrecartographie@gmail.com" method="POST">
    <input type="text" name="nom" placeholder="Nom" required />
    <input type="email" name="email" placeholder="Email" required />
    <textarea name="message" placeholder="Message"></textarea>
    <button class="btn" type="submit">Envoyer</button>
  </form>
</section>

<a class="cta-whatsapp" href="https://wa.me/225000000000">WhatsApp</a>

<footer>
  <p>CENTEC © 2026</p>

  <div>
    <a href="#"><i class="fab fa-facebook"></i></a>
    <a href="#"><i class="fab fa-linkedin"></i></a>
    <a href="#"><i class="fab fa-tiktok"></i></a>
  </div>
</footer>

</body>
</html>
