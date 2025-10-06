<!DOCTYPE html><html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Menu Cherry’s</title>
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #fff;
      color: #222;
    }
    header {
      text-align: center;
      padding: 20px;
      background-color: #fff;
      border-bottom: 3px solid #e60012;
    }
    header h1 {
      font-size: 2em;
      color: #e60012;
      margin: 0;
    }
    .menu-section {
      padding: 20px;
      max-width: 900px;
      margin: auto;
    }
    .menu-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }
    .menu-item {
      border-radius: 15px;
      overflow: hidden;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      transition: transform 0.3s ease;
      background-color: #fafafa;
    }
    .menu-item:hover {
      transform: translateY(-5px);
    }
    .menu-item img {
      width: 100%;
      height: 180px;
      object-fit: cover;
    }
    .menu-info {
      padding: 15px;
      text-align: center;
    }
    .menu-info h3 {
      margin: 5px 0;
      color: #333;
    }
    .menu-info p {
      color: #e60012;
      font-weight: bold;
      font-size: 1.1em;
    }
    footer {
      text-align: center;
      padding: 15px;
      background-color: #fff;
      font-size: 0.9em;
      color: #666;
      border-top: 2px solid #eee;
    }
  </style>
</head>
<body>
  <header>
    <h1>🍒 Menu Cherry’s</h1>
  </header>  <section class="menu-section">
    <div class="menu-grid">
      <div class="menu-item">
        <img src="https://images.unsplash.com/photo-1604908177225-5d1f9bce6c60" alt="Poulet braisé">
        <div class="menu-info">
          <h3>Poulet Braisé</h3>
          <p>12 000 F</p>
        </div>
      </div>
      <div class="menu-item">
        <img src="https://images.unsplash.com/photo-1617196037955-e98ceafc0400" alt="Poisson braisé">
        <div class="menu-info">
          <h3>Poisson Braisé</h3>
          <p>13 000 F</p>
        </div>
      </div>
      <div class="menu-item">
        <img src="https://images.unsplash.com/photo-1600891964599-f61ba0e24092" alt="Mixte grill">
        <div class="menu-info">
          <h3>Mixte Grill</h3>
          <p>15 000 F</p>
        </div>
      </div>
      <div class="menu-item">
        <img src="https://images.unsplash.com/photo-1586190848861-99aa4a171e90" alt="Burger spécial">
        <div class="menu-info">
          <h3>Burger Spécial</h3>
          <p>8 500 F</p>
        </div>
      </div>
      <div class="menu-item">
        <img src="https://images.unsplash.com/photo-1612874742278-6f8e79e21e3b" alt="Pizza Cherry’s">
        <div class="menu-info">
          <h3>Pizza Cherry’s</h3>
          <p>10 000 F</p>
        </div>
      </div>
      <div class="menu-item">
        <img src="https://images.unsplash.com/photo-1604152135912-04a2450c61e1" alt="Cocktail maison">
        <div class="menu-info">
          <h3>Cocktail Maison</h3>
          <p>4 500 F</p>
        </div>
      </div>
    </div>
  </section>  <footer>
    <p>© 2025 Cherry’s — Savourez le meilleur</p>
  </footer>
</body>
</html>
