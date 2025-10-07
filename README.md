<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Menu Cherry's</title>
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
<style>
    body {
        font-family: 'Roboto', sans-serif;
        background-color: #fff5f7;
        margin: 0;
        padding: 0;
    }
    header {
        text-align: center;
        background-color: #ff4d4d;
        color: white;
        padding: 25px;
        font-size: 2em;
        font-weight: bold;
        box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
    .menu-category {
        background-color: #ff9999;
        margin: 10px;
        padding: 18px;
        border-radius: 12px;
        text-align: center;
        cursor: pointer;
        font-size: 1.3em;
        font-weight: bold;
        transition: background 0.3s;
    }
    .menu-category:hover {
        background-color: #ff6666;
    }
    .menu-items {
        display: none;
        margin: 10px;
        padding: 15px 20px;
        background-color: #ffe6e6;
        border-radius: 12px;
        box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    .menu-items ul {
        list-style: none;
        padding: 0;
        margin: 0;
    }
    .menu-items li {
        padding: 8px 0;
        font-size: 1em;
        display: flex;
        align-items: center;
        gap: 10px;
    }
    .menu-items img {
        width: 60px;
        height: 60px;
        object-fit: cover;
        border-radius: 8px;
    }
</style>
</head>
<body>

<header>🍔 Menu Cherry's 🍕</header>

<div class="menu-category" onclick="toggleMenu('fastfood')">● Fast-food</div>
<div class="menu-items" id="fastfood">
    <ul>
        <li><img src="https://via.placeholder.com/60" alt=""> Gyros au poulet : 3000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Gyros au bœuf : 2000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Gyros cherry's : 4500f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Sandwich viande : 1000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Sandwich poulet : 1500f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Chawarma poulet : 2000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Chawarma viande : 1500f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Hamburger : 2500f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Chicken burgers : 3000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Cherry's burgers : 4000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> KFC : 4000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Plat de Nems 4 pièces : 2500f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Tacos viande : 2500f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Tacos poulet : 3500f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Tacos cherry's : 4500f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Big Sandwich : 10000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Big burgers : 12500f</li>
    </ul>
</div>

<div class="menu-category" onclick="toggleMenu('pizzas')">● Pizzas</div>
<div class="menu-items" id="pizzas">
    <ul>
        <li><img src="https://via.placeholder.com/60" alt=""> Pizza cherry's : 7000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Pizza marguarita : 5000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Pizza orientale : 6000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Pizza végétarien : 6000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Pizza Kiss : 6500f</li>
    </ul>
</div>

<div class="menu-category" onclick="toggleMenu('grillades')">● Nos Grillade</div>
<div class="menu-items" id="grillades">
    <ul>
        <li><img src="https://via.placeholder.com/60" alt=""> Brochette de bœuf : 6000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Brochette de poulet : 6000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Brochette de capitaine : 7000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> 1/2 poulet : 6000f</li>
    </ul>
</div>

<div class="menu-category" onclick="toggleMenu('mixtes')">● Les mixtes à partager</div>
<div class="menu-items" id="mixtes">
    <ul>
        <li><img src="https://via.placeholder.com/60" alt=""> Mixte fast-food : 15000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Mixte grille : 15000f</li>
    </ul>
</div>

<div class="menu-category" onclick="toggleMenu('cafe')">● Café</div>
<div class="menu-items" id="cafe">
    <ul>
        <li><img src="https://via.placeholder.com/60" alt=""> Nespresso : 1500f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Cappuccino : 2000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Frappucino glacé : 2500f</li>
    </ul>
</div>

<div class="menu-category" onclick="toggleMenu('the')">● Thé</div>
<div class="menu-items" id="the">
    <ul>
        <li><img src="https://via.placeholder.com/60" alt=""> Thé mixte : 1500f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Thé Cherry's : 1500f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Thé malien : 1000f</li>
    </ul>
</div>

<div class="menu-category" onclick="toggleMenu('mocktail')">● Mocktail</div>
<div class="menu-items" id="mocktail">
    <ul>
        <li><img src="https://via.placeholder.com/60" alt=""> Ener cherry's : 1500f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Virginie colada : 4000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Virginie mojito : 4000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> Bora bora : 4000f</li>
        <li><img src="https://via.placeholder.com/60" alt=""> San francisco : 4000f</li>
    </ul>
</div>

<script>
function toggleMenu(id) {
    const el = document.getElementById(id);
    el.style.display = (el.style.display === 'block') ? 'none' : 'block';
}
</script>

</body>
</html>
