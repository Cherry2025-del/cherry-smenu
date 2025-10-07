
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Menu Cherry’s</title>
  <style>
    body {
      font-family: 'Poppins', Arial, sans-serif;
      background: #fff;
      color: #333;
      margin: 0;
      padding: 0;
    }
    header {
      text-align: center;
      background: #d6004a;
      color: white;
      padding: 25px;
      font-size: 2em;
      letter-spacing: 1px;
      font-weight: bold;
      text-shadow: 1px 1px 2px #00000033;
    }
    .menu {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      padding: 20px;
    }
    .item {
      background: white;
      border-radius: 15px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      width: 300px;
      margin: 15px;
      text-align: center;
      overflow: hidden;
      transition: 0.3s;
    }
    .item:hover {
      transform: scale(1.03);
    }
    .item img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }
    .item h3 {
      color: #d6004a;
      margin: 10px 0 5px 0;
    }
    .item p {
      font-size: 1.2em;
      color: #444;
      margin-bottom: 15px;
    }
  </style>
</head>
<body>
  <header>🍒 Menu Cherry’s</header>
  <section class="menu">
    <div class="item">
      <img src="https://cdn.pixabay.com/photo/2017/12/09/08/18/roast-chicken-3007397_1280.jpg" alt="Poulet braisé">
      <h3>Poulet Braisé</h3>
      <p>12 000 F</p>
    </div>
    <div class="item">
      <img src="https://cdn.pixabay.com/photo/2016/03/05/22/34/fish-1239423_1280.jpg" alt="Poisson braisé">
      <h3>Poisson Braisé</h3>
      <p>13 000 F</p>
    </div>
    <div class="item">
      <img src="https://cdn.pixabay.com/photo/2015/04/08/13/13/food-712665_1280.jpg" alt="Mixte grill">
      <h3>Mixte Grill</h3>
      <p>15 000 F</p>
    </div>
  </section>
</body>
</html>
