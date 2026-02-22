<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>CENTEC – Centre de Formation & Géomatique</title>
  <meta name="description" content="CENTEC – Centre National d'Etude en Territoire et Cartographie" />

  <!-- Icônes Font Awesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" />

  <style>
    :root {
      --primary: #0b5ed7;
      --secondary: #198754;
      --dark: #111;
      --light: #f5f7fa;
      --text: #222;
    }

    * { box-sizing: border-box; }

    body {
      font-family: 'Segoe UI', Tahoma, sans-serif;
      margin: 0;
      line-height: 1.7;
      color: var(--text);
      background: #fff;
    }

    header {
      background: linear-gradient(135deg, #7ec8ff 0%, #2ea3ff 100%);
      color: #fff;
      padding: 1.5rem 2rem;
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 6px 18px rgba(46,163,255,0.12);
    }

    header h1 { margin: 0; font-size: 1.8rem; }

    .header-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      max-width: 1200px;
      margin: 0 auto;
      gap: 1rem;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 0.9rem;
    }

    .logo {
      height: 56px;
      width: auto;
      border-radius: 8px;
      object-fit: contain;
      background: #fff;
      padding: 6px;
    }

    .tagline { margin: 0; font-size: 0.95rem; opacity: 0.95; }

    .header-photo {
      height: 56px;
      width: 56px;
      border-radius: 50%;
      object-fit: cover;
      border: 2px solid rgba(255,255,255,0.15);
    }

    .header-decor {
      display: flex;
      gap: 0.6rem;
      align-items: center;
    }

    .decor-item {
      background: rgba(255,255,255,0.12);
      color: #fff;
      padding: 0.45rem 0.7rem;
      border-radius: 10px;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      font-weight: 600;
      font-size: 0.95rem;
    }

    .decor-item .fa {
      color: #fff;
      opacity: 0.95;
    }

    .hamburger {
      display: none;
      background: none;
      border: none;
      cursor: pointer;
      color: #fff;
      font-size: 1.5rem;
      padding: 0.5rem;
    }

    nav {
      margin-top: 0.5rem;
      display: flex;
      flex-wrap: wrap;
    }

    nav.mobile-menu {
      display: none;
      position: absolute;
      top: 100px;
      left: 0;
      right: 0;
      background: linear-gradient(135deg, #7ec8ff 0%, #2ea3ff 100%);
      flex-direction: column;
      padding: 1rem;
      gap: 0.5rem;
      box-shadow: 0 4px 12px rgba(0,0,0,0.15);
      z-index: 999;
    }

    nav.mobile-menu.active {
      display: flex;
    }

    nav a {
      color: #fff;
      margin-right: 1rem;
      text-decoration: none;
      font-weight: 600;
      opacity: 0.9;
    }

    nav a:hover { opacity: 1; text-decoration: underline; }

    section {
      padding: 4rem 2rem;
      max-width: 1200px;
      margin: auto;
    }

    .hero {
      background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1504384308090-c894fdcc538d');
      background-size: cover;
      background-position: center;
      color: #fff;
      text-align: center;
      padding: 6rem 2rem;
    }

    .hero h2 { font-size: 2.6rem; margin-bottom: 1rem; }
    .hero p { max-width: 700px; margin: auto; font-size: 1.1rem; }

    h2 { font-size: 2.2rem; margin-bottom: 1.5rem; color: var(--primary); }

    .btn {
      display: inline-block;
      background: var(--secondary);
      color: #fff;
      padding: 0.8rem 1.8rem;
      border-radius: 30px;
      text-decoration: none;
      font-weight: bold;
      margin-top: 1.5rem;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }

    .btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 8px 20px rgba(0,0,0,0.2);
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 2rem;
    }

    .icon {
      color: var(--primary);
      margin-right: 0.5rem;
    }

    .apropos-card {
      text-align: center;
    }

    .apropos-img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 10px;
      margin-bottom: 1rem;
    }

    .card {
  background: #fff;
      border-radius: 12px;
      padding: 2rem;
      box-shadow: 0 10px 25px rgba(0,0,0,0.08);
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }

    .card:hover {
      transform: translateY(-5px);
      box-shadow: 0 15px 35px rgba(0,0,0,0.15);
    }

    form input, form textarea {
      width: 100%;
      padding: 0.8rem;
      border-radius: 6px;
      border: 1px solid #ddd;
      font-size: 1rem;
      transition: border-color 0.3s ease, box-shadow 0.3s ease;
    }

    form input:focus, form textarea:focus {
      outline: none;
      border-color: var(--primary);
      box-shadow: 0 0 8px rgba(11, 94, 215, 0.2);
    }

    form textarea { resize: vertical; }

    .form-group { margin-bottom: 1.2rem; }

    .form-group label {
      display: block;
      margin-bottom: 0.4rem;
      font-weight: 600;
      color: var(--text);
    }

    footer {
      background: var(--dark);
      color: #fff;
      padding: 2.5rem 1rem;
    }

    footer a { color: #fff; opacity: 0.8; text-decoration: none; }
    footer a:hover { opacity: 1; text-decoration: underline; }

    .footer-content {
      max-width: 1200px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
      text-align: left;
      margin-bottom: 2rem;
    }

    .footer-section h4 {
      margin-top: 0;
      margin-bottom: 1rem;
      font-size: 1.1rem;
      border-bottom: 2px solid var(--primary);
      padding-bottom: 0.5rem;
    }

    .footer-section p {
      margin: 0.5rem 0;
      font-size: 0.95rem;
      line-height: 1.6;
    }

    .footer-links {
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
    }

    .footer-links a {
      display: inline-block;
      width: fit-content;
    }

    .social-links {
      display: flex;
      gap: 1rem;
      margin-top: 1rem;
    }

    .social-links a {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 40px;
      height: 40px;
      background: rgba(255,255,255,0.1);
      border-radius: 50%;
      color: #fff;
      transition: all 0.3s ease;
    }

    .social-links a:hover {
      background: var(--primary);
      transform: translateY(-3px);
    }

    .footer-bottom {
      border-top: 1px solid rgba(255,255,255,0.2);
      padding-top: 1.5rem;
      text-align: center;
      font-size: 0.9rem;
    }

    .testimonial {
      border-left: 4px solid var(--primary);
      padding-left: 1.5rem;
      font-style: italic;
      color: #666;
    }

    .stats {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 2rem;
      text-align: center;
      margin: 2rem 0;
    }

    .stat-item h3 {
      font-size: 2.5rem;
      color: var(--primary);
      margin: 0.5rem 0;
    }

    .stat-item p {
      color: #666;
      margin: 0;
    }

    .formation-card {
      border: none;
      position: relative;
      overflow: hidden;
    }

    .formation-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 4px;
      background: linear-gradient(90deg, var(--primary), var(--secondary));
    }

    .formation-header {
      display: flex;
      align-items: center;
      gap: 0.6rem;
      margin-bottom: 0.8rem;
    }

    .formation-header h3 {
      margin: 0;
      color: var(--primary);
      font-size: 1.3rem;
    }

    .badge {
      display: inline-block;
      background: var(--primary);
      color: #fff;
      padding: 0.3rem 0.8rem;
      border-radius: 20px;
      font-size: 0.8rem;
      font-weight: bold;
      margin-bottom: 0.8rem;
    }

    .badge.intermediate {
      background: #ffc107;
    }

    .badge.advanced {
      background: #dc3545;
    }

    .formation-meta {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 0.8rem;
      margin: 1rem 0;
      padding: 0.8rem 0;
      border-top: 1px solid #eee;
      border-bottom: 1px solid #eee;
      font-size: 0.9rem;
    }

    .meta-item {
      display: flex;
      align-items: center;
      gap: 0.4rem;
      color: #666;
    }

    .meta-item .fa {
      color: var(--primary);
      width: 16px;
    }

    .formation-price {
      font-size: 1.5rem;
      color: var(--secondary);
      font-weight: bold;
      margin: 0.8rem 0;
    }

    .inscription-btn {
      display: inline-block;
      background: var(--primary);
      color: #fff;
      padding: 0.6rem 1.2rem;
      border-radius: 6px;
      text-decoration: none;
      font-weight: bold;
      margin-top: 0.5rem;
      transition: all 0.3s ease;
    }

    .inscription-btn:hover {
      background: #0a4cc4;
      transform: translateY(-2px);
      box-shadow: 0 6px 15px rgba(11, 94, 215, 0.2);
    }

    .service-card {
      border: none;
      position: relative;
      background: linear-gradient(135deg, #fff 0%, #f9fbff 100%);
    }

    .service-icon {
      font-size: 2.5rem;
      margin-bottom: 0.8rem;
      display: block;
    }

    .service-icon.icon-blue { color: var(--primary); }
    .service-icon.icon-green { color: var(--secondary); }
    .service-icon.icon-orange { color: #fd7e14; }

    .service-card h3 {
      color: var(--text);
      font-size: 1.3rem;
      margin-bottom: 0.8rem;
    }

    .service-list {
      list-style: none;
      padding: 0;
      margin: 1rem 0;
    }

    .service-list li {
      padding: 0.5rem 0;
      color: #666;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .service-list li:before {
      content: '✓';
      color: var(--secondary);
      font-weight: bold;
      margin-right: 0.3rem;
    }

    .contact-service-btn {
      display: inline-block;
      background: var(--secondary);
      color: #fff;
      padding: 0.6rem 1.2rem;
      border-radius: 6px;
      text-decoration: none;
      font-weight: bold;
      margin-top: 1rem;
      transition: all 0.3s ease;
    }

    .contact-service-btn:hover {
      background: #157347;
      transform: translateY(-2px);
      box-shadow: 0 6px 15px rgba(25, 135, 84, 0.2);
    }

    .facebook-wrapper {
      display: flex;
      justify-content: center;
      align-items: flex-start;
      padding: 1rem !important;
      background: #fff !important;
    }

    .facebook-wrapper iframe {
      max-width: 100%;
      width: 100% !important;
      height: auto !important;
      min-height: 400px;
    }

    @supports (aspect-ratio: 500/729) {
      .facebook-wrapper iframe {
        aspect-ratio: 500 / 729;
        height: auto;
      }
    }

    @media (max-width: 768px) {
      .hamburger {
        display: block;
      }

      header {
        position: relative;
      }

      nav:not(.mobile-menu) {
        display: none !important;
      }

      .hero h2 { font-size: 2rem; }
      .stats { grid-template-columns: repeat(2, 1fr); }

      .footer-content {
        grid-template-columns: 1fr;
        text-align: center;
      }

      .footer-section h4 {
        text-align: center;
      }

      .footer-links {
        align-items: center;
      }

      .social-links {
        justify-content: center;
      }
    }
  </style>
</head>
<body>

<header>
  <div class="header-inner">
    <div class="brand">
      
      <img src="assets/logo.jpg" alt="Logo CENTEC" class="logo" onerror="this.style.display='none'">
      <div>
        <h1>CENTEC</h1>
        <p class="tagline">Centre National d'Etude en Territoire et Cartographie</p>
      </div>
    </div>

    <div style="display:flex; align-items:center; gap:1rem;">
      <!-- Remplacez assets/header-photo.jpg par votre photo (bâtiment, équipe...) -->
      <img src="assets/header-photo.jpg" alt="Photo CENTEC" class="header-photo" onerror="this.style.display='none'">
      <div class="header-decor" aria-hidden="true">
        <span class="decor-item"><i class="fa-solid fa-map-location-dot"></i> SIG</span>
        <span class="decor-item">📡 Drones</span>
        <span class="decor-item"><i class="fa-solid fa-globe"></i> Web</span>
        <span class="decor-item">🌤️</span>
      </div>
    </div>
  </div>

  <nav>
    <a href="#accueil">Accueil</a>
    <a href="#apropos">À propos</a>
    <a href="#formations">Formations</a>
    <a href="#services">Services</a>
    <a href="#projets">Projets</a>
    <a href="#actualites">Actualités</a>
    <a href="#contact">Contact</a>
  </nav>

  <nav class="mobile-menu" id="mobileMenu">
    <a href="#accueil">Accueil</a>
    <a href="#apropos">À propos</a>
    <a href="#formations">Formations</a>
    <a href="#services">Services</a>
    <a href="#projets">Projets</a>
    <a href="#actualites">Actualités</a>
    <a href="#contact">Contact</a>
  </nav>

  <button class="hamburger" id="hamburger" aria-label="Menu">☰</button>
</header>

<section id="accueil" class="hero">
  <h2>Former, analyser et cartographier pour un meilleur territoire</h2>
  <p>CENTEC est un centre spécialisé en SIG, cartographie, télédétection, drones et collecte de données en Afrique francophone.</p>
  <a href="#formations" class="btn">Découvrir nos formations</a>
</section>

<section id="apropos">
  <h2>Qui sommes-nous ?</h2>
  <p><strong>CENTEC (Centre National d'Etude en Territoire et Cartographie)</strong> est une structure spécialisée dans la formation, la recherche appliquée et les prestations de services en géomatique. Né du constat d’un besoin croissant en compétences locales dans les domaines des SIG, de la cartographie, de la télédétection et de l’analyse spatiale, CENTEC œuvre pour le renforcement des capacités techniques et professionnelles des étudiants, des institutions, des collectivités et des entreprises en Afrique francophone.</p>
  <p>Notre approche repose sur une combinaison équilibrée entre la théorie, la pratique terrain et l’utilisation d’outils professionnels reconnus (SIG, drones, images satellites, collecte mobile de données). CENTEC se positionne ainsi comme un acteur clé du développement territorial et de la prise de décision basée sur les données spatiales.</p>

  <div class="grid">
    <div class="card apropos-card">
      <img src="https://images.unsplash.com/photo-1526378722484-bd91ca387e72" alt="Mission CENTEC" class="apropos-img">
      <h3>Notre mission</h3>
      <p>Former, accompagner et outiller des professionnels capables de collecter, analyser, interpréter et valoriser les données géospatiales afin de répondre efficacement aux enjeux de développement, d’aménagement du territoire et de gouvernance.</p>
    </div>

    <div class="card apropos-card">
      <img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee" alt="Vision CENTEC" class="apropos-img">
      <h3>Notre vision</h3>
      <p>Devenir une référence régionale et africaine en matière de formation et d’expertise en géomatique, en mettant l’innovation, la qualité pédagogique et l’excellence technique au service du développement durable.</p>
    </div>

    <div class="card apropos-card">
      <img src="https://images.unsplash.com/photo-1581092580497-e0d23cbdf1dc" alt="Pédagogie CENTEC" class="apropos-img">
      <h3>Notre pédagogie</h3>
      <p>Une pédagogie orientée vers la pratique, basée sur des études de cas réels, des travaux pratiques, des projets terrain et l’usage d’outils professionnels, afin de garantir des compétences directement opérationnelles.</p>
    </div>
  </div>
</section>

<section id="formations" style="background:#f5f7fa;">
  <h2>Nos formations</h2>
  <p style="text-align: center; color: #666; margin-bottom: 2rem;">Formations pratiques et reconnues pour devenir expert en géomatique</p>
  <div class="grid">
    <div class="card formation-card">
      <div class="formation-header">
        <i class="fa-solid fa-map-location-dot icon" style="font-size: 1.8rem; color: var(--primary);"></i>
        <h3>Initiation aux SIG</h3>
      </div>
      <span class="badge">Débutant</span>
      <p>Découvrez les fondamentaux des Systèmes d'Information Géographique (SIG) avec QGIS. Apprenez à manipuler les données spatiales, créer des cartes professionnelles et explorer les bases de la cartographie numérique.</p>
      <div class="formation-meta">
        <div class="meta-item">
          <i class="fa-solid fa-clock"></i>
          <span>3 jours (21h)</span>
        </div>
        <div class="meta-item">
          <i class="fa-solid fa-users"></i>
          <span>5-12 pers.</span>
        </div>
        <div class="meta-item">
          <i class="fa-solid fa-calendar"></i>
          <span>Mensuel</span>
        </div>
        <div class="meta-item">
          <i class="fa-solid fa-location-dot"></i>
          <span>En présentiel</span>
        </div>
      </div>
      <div class="formation-price">650 000 FCFA</div>
      <a href="formation-debutant.html" class="inscription-btn">S'inscrire</a>
    </div>

    <div class="card formation-card">
      <div class="formation-header">
        <i class="fa-solid fa-chart-area icon" style="font-size: 1.8rem; color: #ffc107;"></i>
        <h3>Cartographie statistique</h3>
      </div>
      <span class="badge intermediate">Intermédiaire</span>
      <p>Maîtrisez l'analyse spatiale et la représentation des données statistiques. Transformez les données socio-économiques en cartes thématiques impactantes pour une prise de décision éclairée.</p>
      <div class="formation-meta">
        <div class="meta-item">
          <i class="fa-solid fa-clock"></i>
          <span>4 jours (28h)</span>
        </div>
        <div class="meta-item">
          <i class="fa-solid fa-users"></i>
          <span>5-10 pers.</span>
        </div>
        <div class="meta-item">
          <i class="fa-solid fa-calendar"></i>
          <span>Trimestriel</span>
        </div>
        <div class="meta-item">
          <i class="fa-solid fa-location-dot"></i>
          <span>En présentiel</span>
        </div>
      </div>
      <div class="formation-price">850 000 FCFA</div>
      <a href="#contact" class="inscription-btn">S'inscrire</a>
    </div>

    <div class="card formation-card">
      <div class="formation-header">
        <i class="fa-solid fa-drone icon" style="font-size: 1.8rem; color: #dc3545;"></i>
        <h3>Télédétection & Drones</h3>
      </div>
      <span class="badge advanced">Avancé</span>
      <p>Explorez les technologies de télédétection par satellite et drone. Traitez les images aériennes et satellites pour l'analyse territoriale, la surveillance environnementale et les projets d'aménagement.</p>
      <div class="formation-meta">
        <div class="meta-item">
          <i class="fa-solid fa-clock"></i>
          <span>5 jours (35h)</span>
        </div>
        <div class="meta-item">
          <i class="fa-solid fa-users"></i>
          <span>4-8 pers.</span>
        </div>
        <div class="meta-item">
          <i class="fa-solid fa-calendar"></i>
          <span>Semestriel</span>
        </div>
        <div class="meta-item">
          <i class="fa-solid fa-location-dot"></i>
          <span>Terrain + labo</span>
        </div>
      </div>
      <div class="formation-price">1 200 000 FCFA</div>
      <a href="#contact" class="inscription-btn">S'inscrire</a>
    </div>
  </div>
</section>

<section id="services">
  <h2>Services & Prestations</h2>
  <p style="text-align: center; color: #666; margin-bottom: 2rem;">Solutions géomatiques complètes pour vos enjeux territoriaux</p>
  <div class="grid">
    <div class="card service-card">
      <i class="fa-solid fa-city service-icon icon-blue"></i>
      <h3>Bureau d'études</h3>
      <p>Nos experts réalisent des études territoriales approfondies et des analyses spatiales pour soutenir vos projets d'aménagement, de développement et de gouvernance.</p>
      <ul class="service-list">
        <li>Études de faisabilité spatiales</li>
        <li>Analyses d'aménagement du territoire</li>
        <li>Modélisation spatiale</li>
        <li>Rapports cartographiques</li>
        <li>Diagnostic territorial</li>
      </ul>
      <a href="#contact" class="contact-service-btn">Demander un devis</a>
    </div>

    <div class="card service-card">
      <i class="fa-solid fa-database service-icon icon-green"></i>
      <h3>Collecte de données</h3>
      <p>Collectez et gérez vos données géospatiales via des enquêtes terrain structurées, des applications mobiles et des outils professionnels éprouvés.</p>
      <ul class="service-list">
        <li>Enquêtes terrain (GPS, GNSS)</li>
        <li>Collecte mobile avec KoboToolbox</li>
        <li>Traitement et nettoyage de données</li>
        <li>Validation et analyse spatiale</li>
        <li>Reporting et visualisation</li>
      </ul>
      <a href="#contact" class="contact-service-btn">Demander un devis</a>
    </div>

    <div class="card service-card">
      <i class="fa-solid fa-globe service-icon icon-orange"></i>
      <h3>Webmapping</h3>
      <p>Créez des portails cartographiques interactifs pour visualiser, explorer et partager vos données géospatiales avec des outils web modernes et conviviaux.</p>
      <ul class="service-list">
        <li>Cartes interactives personnalisées</li>
        <li>Tableaux de bord géospatiales</li>
        <li>Portails de données ouvertes</li>
        <li>Intégrations API et WMS</li>
        <li>Formation aux outils</li>
      </ul>
      <a href="#contact" class="contact-service-btn">Demander un devis</a>
    </div>
  </div>
</section>

<section id="projets" style="background:#f5f7fa;">
  <h2>Réalisations</h2>
  <p>Cartes thématiques, projets SIG, études territoriales et analyses spatiales réalisées par CENTEC.</p>
  <div class="stats">
    <div class="stat-item">
      <h3>150+</h3>
      <p>Professionnels formés</p>
    </div>
    <div class="stat-item">
      <h3>25+</h3>
      <p>Projets réalisés</p>
    </div>
    <div class="stat-item">
      <h3>12</h3>
      <p>Pays couverts</p>
    </div>
    <div class="stat-item">
      <h3>8+</h3>
      <p>Années d'expérience</p>
    </div>
  </div>
</section>

<section id="actualites">
  <h2>Actualités & Événements</h2>
  <p style="text-align: center; color: #666; margin-bottom: 2rem;">Restez informé de nos dernières nouvelles, formations et appels à projets</p>
  <div class="grid">
    <div class="card">
      <span class="badge" style="background: #dc3545;">🔔 Événement</span>
      <h3>Atelier SIG & Drones – Mars 2026</h3>
      <p>Rejoignez nos experts pour un atelier intensif de 2 jours sur les applications pratiques des drones en cartographie et surveillance territoriale.</p>
      <p><small>📅 15-16 mars 2026 | 📍 Abidjan</small></p>
      <a href="#contact" class="btn" style="background: var(--primary); font-size: 0.9rem; padding: 0.5rem 1rem; margin-top: 0.5rem;">S'inscrire</a>
    </div>
    <div class="card">
      <span class="badge" style="background: #198754;">✓ Nouveau</span>
      <h3>Formation en ligne : Webmapping avancé</h3>
      <p>Découvrez la création de portails cartographiques interactifs avec Leaflet et Mapbox. Formation 100% en ligne, flexible, adaptée aux professionnels.</p>
      <p><small>📅 Démarrage : 15 février 2026</small></p>
      <a href="#formations" class="btn" style="background: var(--primary); font-size: 0.9rem; padding: 0.5rem 1rem; margin-top: 0.5rem;">Détails</a>
    </div>
    <div class="card">
      <span class="badge" style="background: #ffc107;">🎯 Appel</span>
      <h3>Appel à projets : Cartographie participative</h3>
      <p>CENTEC cherche des partenaires pour des projets de cartographie participative en Afrique de l'Ouest. Financements disponibles jusqu'au 28 février.</p>
      <p><small>📅 Deadline : 28 février 2026</small></p>
      <a href="#contact" class="btn" style="background: var(--primary); font-size: 0.9rem; padding: 0.5rem 1rem; margin-top: 0.5rem;">Candidater</a>
    </div>
    <div class="card facebook-wrapper">
      <div style="width: 100%; text-align: center;">
        <span class="badge" style="background: #1877f2; margin-bottom: 1rem;">📱 Nos actualités Facebook</span>
        <h3 style="margin-top: 0; color: var(--primary);">Suivez-nous sur Facebook</h3>
        <p style="color: #666; margin-bottom: 1.5rem;">Découvrez nos dernières actualités, événements et success stories directement depuis notre page Facebook officielle. Rejoignez notre communauté!</p>
        <iframe src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fweb.facebook.com%2Fpermalink.php%3Fstory_fbid%3Dpfbid02CQyeRdE9wbuEPWX8L9bPtDC5rNXjGcdH1GnZmUgfPpeS6RTkUq77nE4EbRmS17yql%26id%3D61566026256570&show_text=true&width=500" width="500" height="729" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowfullscreen="true" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"></iframe>
        <a href="https://www.facebook.com/share/1AFMBL3wkV/" target="_blank" rel="noopener" class="btn" style="background: #1877f2; font-size: 0.9rem; padding: 0.6rem 1.5rem; margin-top: 1.5rem; display: inline-block;">Consulter la page</a>
      </div>
    </div>
  </div>
</section>

<section id="contact" style="background:#f5f7fa;">
  <h2>Contact & Inscription</h2>
  <div style="max-width: 600px; margin: 0 auto;">
    <form onsubmit="return handleFormSubmit(event)">
      <div class="form-group">
        <label for="nom">Nom complet</label>
        <input type="text" id="nom" name="nom" placeholder="Entrez votre nom" required>
      </div>
      <div class="form-group">
        <label for="email">Email</label>
        <input type="email" id="email" name="email" placeholder="votre.email@exemple.com" required>
      </div>
      <div class="form-group">
        <label for="sujet">Sujet</label>
        <input type="text" id="sujet" name="sujet" placeholder="Ex: Formation en SIG" required>
      </div>
      <div class="form-group">
        <label for="message">Votre message</label>
        <textarea id="message" name="message" placeholder="Décrivez votre demande..." rows="5" required></textarea>
      </div>
      <button class="btn" type="submit" style="width: 100%; text-align: center;">Envoyer ma demande</button>
    </form>
    <p style="text-align: center; margin-top: 1.5rem; color: #666;">✉️ Ou envoyez-nous un email directement à <strong>centrecartographie@gmail.com</strong></p>
  </div>
</section>

<footer>
  <div class="footer-content">
    <div class="footer-section">
      <h4>📍 Contact</h4>
      <p><strong>Adresse :</strong><br>Abidjan, Côte d'Ivoire</p>
      <p><strong>Email :</strong><br><a href="mailto:centrecartographie@gmail.com">centrecartographie@gmail.com</a></p>
      <p><strong>Téléphone :</strong><br><a href="tel:+22512345678">+225 12 34 56 78</a></p>
    </div>
    <div class="footer-section">
      <h4>🔗 Liens rapides</h4>
      <div class="footer-links">
        <a href="#formations">Nos formations</a>
        <a href="#services">Nos services</a>
        <a href="#actualites">Actualités</a>
        <a href="#contact">Nous contacter</a>
      </div>
    </div>
    <div class="footer-section">
      <h4>🌐 Suivez-nous</h4>
      <div class="social-links">
        <a href="https://www.facebook.com/share/1AFMBL3wkV/" target="_blank" rel="noopener" aria-label="Facebook">
          <i class="fab fa-facebook-f"></i>
        </a>
        <a href="https://www.twitter.com/centec" target="_blank" rel="noopener" aria-label="Twitter">
          <i class="fab fa-twitter"></i>
        </a>
        <a href="https://www.linkedin.com/company/centec" target="_blank" rel="noopener" aria-label="LinkedIn">
          <i class="fab fa-linkedin-in"></i>
        </a>
        <a href="https://www.youtube.com/centec" target="_blank" rel="noopener" aria-label="YouTube">
          <i class="fab fa-youtube"></i>
        </a>
      </div>
    </div>
  </div>
  <div class="footer-bottom">
    <p>© 2026 CENTEC – Tous droits réservés</p>
    <p><a href="#">Mentions légales</a> | <a href="#">Politique de confidentialité</a></p>
  </div>
</footer>

</body>
  <script>
    // Menu hamburger
    const hamburger = document.getElementById('hamburger');
    const mobileMenu = document.getElementById('mobileMenu');
    
    hamburger.addEventListener('click', () => {
      mobileMenu.classList.toggle('active');
    });

    // Fermer le menu au clic sur un lien
    const menuLinks = mobileMenu.querySelectorAll('a');
    menuLinks.forEach(link => {
      link.addEventListener('click', () => {
        mobileMenu.classList.remove('active');
      });
    });

    // Formulaire avec FormSubmit.co
    const form = document.querySelector('form');
    form.action = 'https://formsubmit.co/centrecartographie@gmail.com';
    form.method = 'POST';

    function handleFormSubmit(event) {
      event.preventDefault();
      const nom = document.getElementById('nom').value;
      alert(`Merci ${nom}! Votre demande est en cours d'envoi.`);
      // FormSubmit gérera l'envoi automatiquement
      setTimeout(() => form.submit(), 1000);
    }
  </script>
</html>
