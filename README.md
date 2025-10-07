<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cherry’s Fast-Food</title>
<style>
body {
  font-family: 'Poppins', sans-serif;
  background-color: #fffaf8;
  color: #333;
  margin: 0;
  padding: 0;
}
header {
  background: linear-gradient(90deg, #ff0055, #ff7b00);
  color: white;
  text-align: center;
  padding: 20px;
}
h1 {
  margin: 0;
  font-size: 2em;
}
section {
  max-width: 700px;
  margin: 20px auto;
  background: white;
  border-radius: 15px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
  overflow: hidden;
}
button {
  width: 100%;
  background: #ff0055;
  color: white;
  border: none;
  padding: 15px;
  font-size: 1.1em;
  cursor: pointer;
  transition: 0.3s;
}
button:hover {
  background: #ff3366;
}
.menu-items {
  display: none;
  padding: 15px;
}
.menu-items p {
  margin: 5px 0;
  display: flex;
  justify-content: space-between;
  border-bottom: 1px dashed #ddd;
}
footer {
  text-align: center;
  margin: 30px 0;
  font-size: 0.9em;
}
</style>
<script>
function toggleMenu(id) {
  const el = document.getElementById(id);
  el.style.display = el.style.display === "block" ? "none" : "block";
}
</script>
</head>
<body>

<header>
  <h1>🍒 Cherry’s Fast-Food 🍒</h1>
  <p>Découvrez nos délicieux menus !</p>
</header>

<section>
  <button onclick="toggleMenu('fastfood')">🍔 Fast-food</button>
  <div id="fastfood" class="menu-items">
    <p>Gyros au poulet <span>3000f</span></p>
    <p>Gyros au bœuf <span>2000f</span></p>
    <p>Gyros Cherry’s <span>4500f</span></p>
    <p>Sandwich viande <span>1000f</span></p>
    <p>Sandwich poulet <span>1500f</span></p>
    <p>Chawarma poulet <span>2000f</span></p>
    <p>Chawarma viande <span>1500f</span></p>
    <p>Hamburger <span>2500f</span></p>
    <p>Chicken burger <span>3000f</span></p>
    <p>Cherry’s burger <span>4000f</span></p>
    <p>KFC <span>4000f</span></p>
    <p>Plat de Nems (4 pièces) <span>2500f</span></p>
    <p>Tacos viande <span>2500f</span></p>
    <p>Tacos poulet <span>3500f</span></p>
    <p>Tacos Cherry’s <span>4500f</span></p>
    <p>Big Sandwich <span>10000f</span></p>
    <p>Big Burger <span>12500f</span></p>
  </div>
</section>

<section>
  <button onclick="toggleMenu('pizzas')">🍕 Les Pizzas</button>
  <div id="pizzas" class="menu-items">
    <p>Pizza Cherry’s <span>7000f</span></p>
    <p>Pizza Margharita <span>5000f</span></p>
    <p>Pizza Orientale <span>6000f</span></p>
    <p>Pizza Végétarienne <span>6000f</span></p>
    <p>Pizza Kiss <span>6500f</span></p>
  </div>
</section>

<section>
  <button onclick="toggleMenu('grillades')">🔥 Nos Grillades</button>
  <div id="grillades" class="menu-items">
    <p>Brochette de bœuf <span>6000f</span></p>
    <p>Brochette de poulet <span>6000f</span></p>
    <p>Brochette de capitaine <span>7000f</span></p>
    <p>1/2 poulet <span>6000f</span></p>
  </div>
</section>

<section>
  <button onclick="toggleMenu('mixte')">🍽️ Les mixtes à partager</button>
  <div id="mixte" class="menu-items">
    <p>Mixte fast-food <span>15000f</span></p>
    <p>Mixte grillade (bœuf, capitaine, 1/2 poulet)</p>
  </div>
</section>

<section>
  <button onclick="toggleMenu('cafe')">☕ Café</button>
  <div id="cafe" class="menu-items">
    <p>Nespresso <span>1500f</span></p>
    <p>Cappuccino <span>2000f</span></p>
    <p>Frappuccino glacé <span>2500f</span></p>
  </div>
</section>

<section>
  <button onclick="toggleMenu('the')">🍵 Thé</button>
  <div id="the" class="menu-items">
    <p>Thé mixte <span>1500f</span></p>
    <p>Thé Cherry’s <span>1500f</span></p>
    <p>Thé malien <span>1000f</span></p>
  </div>
</section>

<section>
  <button onclick="toggleMenu('mocktails')">🍹 Mocktails</button>
  <div id="mocktails" class="menu-items">
    <p>Ener Cherry’s <span>1500f</span></p>
    <p>Virgin Mojito <span>3000f</span></p>
    <p>Virgin Colada <span>3000f</span></p>
    <p>Bora Bora <span>3000f</span></p>
    <p>San Francisco <span>3000f</span></p>
    <p>Pina Colada <span>4000f</span></p>
  </div>
</section>

<footer>
  📞 Contact : Cherry’s Fast-Food | Bamako  
</footer>

</body>
</html>
