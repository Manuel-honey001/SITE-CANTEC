<!DOCTYPE html><html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>CENTEC – Centre de Formation & Géomatique</title>
  <meta name="description" content="CENTEC – Centre National d'Etude en Territoire et Cartographie" />  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" />  <style>
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
      background:#fff;
      padding:6px;
      border-radius:8px;
    }

    nav a {
      color:#fff;
      margin-right:1rem;
      text-decoration:none;
      font-weight:600;
    }

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

    .btn {
      display: inline-block;
      background: var(--secondary);
      color: #fff;
      padding: 0.8rem 1.8rem;
      border-radius: 30px;
      text-decoration: none;
      font-weight: bold;
      margin-top: 1.5rem;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 2rem;
    }

    .card {
      background:#fff;
      border-radius:12px;
      padding:2rem;
      box-shadow:0 10px 25px rgba(0,0,0,0.08);
      transition:0.3s;
    }

    .card:hover {
      transform: translateY(-5px);
    }

    .program-banner {
      height:160px;
      background:#ddd;
      display:flex;
      align-items:center;
      justify-content:center;
      font-weight:bold;
      color:#666;
      border-radius:10px;
      margin-bottom:1rem;
    }

    footer {
      background: var(--dark);
      color:#fff;
      padding:2rem;
      text-align:center;
    }
  </style></head>
<body><header>
  <div class="header-inner">
    <div class="brand">
      <img src="assets/logo.jpg" class="logo" alt="logo">
      <div>
        <h1>CENTEC</h1>
        <small>Géomatique & Formation</small>
      </div>
    </div>
    <nav>
      <a href="#accueil">Accueil</a>
      <a href="#apropos">À propos</a>
      <a href="#pourquoi">Pourquoi nous</a>
      <a href="#programmes">Programmes</a>
      <a href="#seminaires">Séminaires</a>
      <a href="#contact">Contact</a>
    </nav>
  </div>
</header><section class="hero" id="accueil">
  <h2>Former, analyser et cartographier</h2>
  <p>Devenez expert en géomatique avec nos programmes progressifs.</p>
  <a href="#programmes" class="btn">Découvrir les programmes</a>
</section><section id="apropos">
  <h2>À propos</h2>
  <p>CENTEC est un centre spécialisé en SIG, télédétection, drones et collecte de données en Afrique francophone.</p>
</section><!-- POURQUOI NOUS --><section id="pourquoi">
  <h2>💡 Pourquoi choisir CENTEC ?</h2>  <div class="grid"><div class="card">
  <h3>🎯 Formation 100% pratique</h3>
  <p>Nous privilégions la pratique sur des cas réels pour garantir des compétences directement utilisables sur le terrain.</p>
</div>

<div class="card">
  <h3>🌍 Expertise en géomatique</h3>
  <p>Nos formations couvrent SIG, télédétection, drones et analyse spatiale avec des outils professionnels.</p>
</div>

<div class="card">
  <h3>🚀 Parcours progressif</h3>
  <p>Du niveau débutant jusqu’à expert, chaque apprenant évolue étape par étape selon un programme structuré.</p>
</div>

<div class="card">
  <h3>🤝 Accompagnement personnalisé</h3>
  <p>Chaque participant bénéficie d’un suivi pour maximiser sa réussite et son insertion professionnelle.</p>
</div>

  </div>
</section><!-- PROGRAMMES --><section id="programmes">
  <h2>🎓 Nos Programmes de Formation</h2>  <div class="grid"><div class="card">
  <div class="program-banner">Bannière DIGI MAP</div>
  <h3>DIGI MAP</h3>
  <p>Cartographie numérique & SIG</p>
  <p>Niveaux : Débutant → Intermédiaire → Expert</p>
</div>

<div class="card">
  <div class="program-banner">Bannière TeleSense Pro</div>
  <h3>TeleSense Pro</h3>
  <p>Télédétection appliquée</p>
  <p>Niveaux : Débutant → Intermédiaire → Expert</p>
</div>

<div class="card">
  <div class="program-banner">Bannière GEOSKILL</div>
  <h3>GEOSKILL</h3>
  <p>Géomatique appliquée</p>
  <p>Niveaux : Débutant → Intermédiaire → Expert</p>
</div>

<div class="card">
  <div class="program-banner">Bannière E-Enquêteur</div>
  <h3>E-Enquêteur</h3>
  <p>Enquêtes terrain & données</p>
  <p>Niveaux : Débutant → Intermédiaire → Expert</p>
</div>

  </div>
</section><!-- SEMINAIRES --><section id="seminaires" style="background:#f5f7fa;">
  <h2>🎤 Séminaires & Ateliers</h2>  <div class="grid">
    <div class="card">
      <h3>Atelier SIG</h3>
      <p>Formation pratique intensive</p>
    </div><div class="card">
  <h3>Bootcamp Drones</h3>
  <p>Pratique terrain</p>
</div>

<div class="card">
  <h3>Masterclass Webmapping</h3>
  <p>Cartographie interactive</p>
</div>

  </div>
</section><section id="contact">
  <h2>Contact</h2>
  <form action="https://formsubmit.co/centrecartographie@gmail.com" method="POST">
    <input type="text" placeholder="Nom" required><br><br>
    <input type="email" placeholder="Email" required><br><br>
    <textarea placeholder="Message"></textarea><br><br>
    <button class="btn">Envoyer</button>
  </form>
</section><footer>
  © 2026 CENTEC - Tous droits réservés
</footer></body>
</html>
