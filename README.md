import React, { useState } from "react";

export default function MenuRestaurantCJDC() {
  const [selectedDish, setSelectedDish] = useState(null);
  const [deliveryOption, setDeliveryOption] = useState("");

  const phoneNumber = "22372910000"; // Mali

  const menu = {
    "Plat du jour": {
      Lundi: ["Yassa poulet : 3000f", "Fakoye : 3000f"],
      Mardi: ["Maffé : 3000f", "Thiep poisson ou poulet : 3000f"],
      Mercredi: ["Saga saga : 3000f", "Sauce tomate : 3000f"],
      Jeudi: ["Woudjila : 3000f", "Atieké : 3000f"],
      Vendredi: ["Tôt : 3000f", "Tiep poisson ou poulet : 3000f"],
    },
    Sandwichs: [
      "Sandwich viande haché : 1000f",
      "Sandwich poulet : 2000f",
      "Sandwich Thon : 2000f",
      "Sandwich foie : 2000f",
      "Sandwich rognon : 2000f",
      "Sandwich Steak : 1500f",
    ],
    Shawarmas: ["Shawarma poulet : 2500f", "Shawarma bœuf : 2000f"],
    Tacos: ["Tacos viande : 2500f", "Le régal : 3500f", "Tacos yummies : 4500f"],
    Burgers: [
      "Burger smile : 3000f",
      "Burger chicken Masala : 3000f",
      "Burger yummies : 4000f",
    ],
  };

  const handleDishClick = (dish) => {
    setSelectedDish(dish);
    setDeliveryOption("");
  };

  const sendToWhatsApp = (option) => {
    let message = `Bonjour, je souhaite commander : ${selectedDish}.`;
    if (option === "livraison") {
      message += " Merci de m’envoyer votre localisation pour la livraison.";
    } else {
      message += " Je viendrai manger sur place.";
    }
    const url = `https://api.whatsapp.com/send?phone=${phoneNumber}&text=${encodeURIComponent(
      message
    )}`;
    window.open(url, "_blank");
    setSelectedDish(null);
    setDeliveryOption("");
  };

  return (
    <div className="min-h-screen bg-white text-gray-800 p-4">
      {/* Logo */}
      <div className="flex justify-center mb-6">
        <img src="/logo.png" alt="Logo CJDC" className="w-24 h-24 rounded-full shadow-lg" />
      </div>

      <h1 className="text-3xl font-bold text-center text-purple-700 mb-6">
        🍽️ Menu CJDC
      </h1>

      {/* Parcourir les familles */}
      {Object.entries(menu).map(([family, content]) => (
        <div key={family} className="mb-8">
          <h2 className="text-2xl font-semibold text-purple-600 mb-3 border-b-2 border-purple-200 pb-1">
            {family}
          </h2>

          {family === "Plat du jour" ? (
            <div>
              {Object.entries(content).map(([day, dishes]) => (
                <div key={day} className="mb-4">
                  <h3 className="text-lg font-medium text-gray-700">{day}</h3>
                  <ul className="pl-4">
                    {dishes.map((dish) => (
                      <li
                        key={dish}
                        className="cursor-pointer hover:text-purple-600"
                        onClick={() => handleDishClick(dish)}
                      >
                        {dish}
                      </li>
                    ))}
                  </ul>
                </div>
              ))}
            </div>
          ) : (
            <ul className="pl-4">
              {content.map((dish) => (
                <li
                  key={dish}
                  className="cursor-pointer hover:text-purple-600"
                  onClick={() => handleDishClick(dish)}
                >
                  {dish}
                </li>
              ))}
            </ul>
          ))}
        </div>
      ))}

      {/* Boîte de dialogue commande */}
      {selectedDish && (
        <div className="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center">
          <div className="bg-white p-6 rounded-xl shadow-lg text-center w-80">
            <h3 className="text-lg font-semibold mb-4">
              Commander : {selectedDish}
            </h3>
            <p className="mb-4">Souhaitez-vous être livré ou manger sur place ?</p>
            <div className="flex justify-around">
              <button
                onClick={() => sendToWhatsApp("livraison")}
                className="bg-purple-600 text-white px-3 py-2 rounded-lg hover:bg-purple-700"
              >
                Livraison
              </button>
              <button
                onClick={() => sendToWhatsApp("surplace")}
                className="bg-gray-300 text-gray-800 px-3 py-2 rounded-lg hover:bg-gray-400"
              >
                Sur place
              </button>
            </div>
            <button
              onClick={() => setSelectedDish(null)}
              className="mt-4 text-sm text-red-500 underline"
            >
              Annuler
            </button>
          </div>
        </div>
      )}
    </div>
  );
}
