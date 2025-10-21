import React, { useState } from "react";

// Single-file React component (Tailwind CSS required in the project) // Replace /logo.png by your real logo path or import it.

export default function MenuApp() { const WA_NUMBER = "22372910000"; // format pour wa.me (code pays + numéro)

const data = { "Plat du jour": { days: { Lundi: [ { name: "Yassa poulet", price: "3000f" }, { name: "Fakoye", price: "3000f" }, ], Mardi: [ { name: "Maffé", price: "3000f" }, { name: "Thiep poisson ou poulet", price: "3000f" }, ], Mercredi: [ { name: "Saga saga", price: "3000f" }, { name: "Sauce tomate", price: "3000f" }, ], Jeudi: [ { name: "Woudjila", price: "3000f" }, { name: "Atieké", price: "3000f" }, ], Vendredi: [ { name: "Tôt", price: "3000f" }, { name: "Tiep poisson ou poulet", price: "3000f" }, ], }, }, "Nos Sandwichs": [ { name: "Sandwich viande haché", price: "1000f" }, { name: "Sandwich poulet", price: "2000f" }, { name: "Sandwich Thon", price: "2000f" }, { name: "Sandwich foie", price: "2000f" }, { name: "Sandwich rognon", price: "2000f" }, { name: "Sandwich Steak", price: "1500f" }, ], "Nos Shawarmas": [ { name: "Shawarma poulet", price: "2500f" }, { name: "Shawarma BŒUF", price: "2000f" }, ], "Nos Tacos": [ { name: "Tacos viande", price: "2500f" }, { name: "Le régal", price: "3500f" }, { name: "Tacos yummies", price: "4500f" }, ], "Nos Burgers": [ { name: "Burger smile", price: "3000f" }, { name: "Burger chicken Masala", price: "3000f" }, { name: "Burger yummies", price: "4000f" }, ], };

const families = Object.keys(data); const [activeFamily, setActiveFamily] = useState(families[0]); const [activeDay, setActiveDay] = useState(null); const [selectedDish, setSelectedDish] = useState(null); const [orderMode, setOrderMode] = useState(null); // 'livraison' | 'surplace'

function openWhatsAppMessage(text) { const encoded = encodeURIComponent(text); const url = https://wa.me/${WA_NUMBER}?text=${encoded}; window.open(url, "_blank"); }

function handleOrder(dishName, familyName) { setSelectedDish({ name: dishName, family: familyName }); setOrderMode(null); }

function confirmOrder(mode) { // Construire message pré-rempli selon le mode const dish = selectedDish?.name ?? ""; const family = selectedDish?.family ?? ""; if (mode === "livraison") { const message = Bonjour 😊, je souhaite commander ${dish} (${family}). Je choisis la livraison. Je vais envoyer ma localisation via WhatsApp.; openWhatsAppMessage(message); } else { const message = Bonjour 😊, je souhaite commander ${dish} (${family}). Je vais manger sur place.; openWhatsAppMessage(message); } // reset setSelectedDish(null); setOrderMode(null); }

return ( <div className="min-h-screen bg-white text-gray-800 p-4 sm:p-8"> <header className="max-w-4xl mx-auto flex items-center gap-4"> <img src="/logo.png" alt="Logo" className="w-24 h-24 object-contain" /> <div> <h1 className="text-2xl font-bold text-violet-600">Menu - CJDC</h1> <p className="text-sm text-gray-500">Commande directe par WhatsApp: +223 72 91 0000</p> </div> </header>

<main className="max-w-4xl mx-auto mt-6 grid grid-cols-1 md:grid-cols-3 gap-6">
    {/* Left: Families list */}
    <aside className="md:col-span-1">
      <div className="bg-violet-50 border border-violet-100 rounded-xl p-4">
        <h2 className="font-semibold mb-3 text-violet-700">Catégories</h2>
        <ul className="space-y-2">
          {families.map((f) => (
            <li key={f}>
              <button
                className={`w-full text-left px-3 py-2 rounded-lg transition-shadow ${
                  activeFamily === f ? "bg-violet-600 text-white" : "bg-white shadow-sm"
                }`}
                onClick={() => {
                  setActiveFamily(f);
                  setActiveDay(null);
                }}
              >
                {f}
              </button>
            </li>
          ))}
        </ul>
      </div>

      <div className="mt-4 text-sm text-gray-600">
        <p>Cliquer sur un plat pour passer la commande via WhatsApp.</p>
      </div>
    </aside>

    {/* Right: Content */}
    <section className="md:col-span-2">
      <div className="bg-white rounded-xl p-4 shadow-sm">
        <h3 className="text-xl font-semibold mb-3 text-violet-700">{activeFamily}</h3>

        {/* If Plat du jour -> show days */}
        {activeFamily === "Plat du jour" ? (
          <div>
            <div className="flex flex-wrap gap-2 mb-4">
              {Object.keys(data[activeFamily].days).map((day) => (
                <button
                  key={day}
                  onClick={() => setActiveDay(day)}
                  className={`px-3 py-2 rounded-full border ${
                    activeDay === day ? "bg-violet-600 text-white" : "bg-white"
                  }`}
                >
                  {day}
                </button>
              ))}
            </div>

            {activeDay ? (
              <div className="grid grid-cols-1 sm:grid-cols-2 gap-3">
                {data[activeFamily].days[activeDay].map((dish) => (
                  <div key={dish.name} className="border rounded-lg p-3 flex justify-between items-center">
                    <div>
                      <div className="font-medium">{dish.name}</div>
                      <div className="text-sm text-gray-500">{dish.price}</div>
                    </div>
                    <div className="flex gap-2">
                      <button
                        onClick={() => handleOrder(dish.name, activeFamily)}
                        className="px-3 py-1 rounded-lg bg-violet-600 text-white"
                      >
                        Passer la commande
                      </button>
                    </div>
                  </div>
                ))}
              </div>
            ) : (
              <p className="text-sm text-gray-500">Sélectionnez un jour pour voir les plats.</p>
            )}
          </div>
        ) : (
          // Other families (array of dishes)
          <div className="grid grid-cols-1 sm:grid-cols-2 gap-3">
            {data[activeFamily].map((dish) => (
              <div key={dish.name} className="border rounded-lg p-3 flex justify-between items-center">
                <div>
                  <div className="font-medium">{dish.name}</div>
                  <div className="text-sm text-gray-500">{dish.price}</div>
                </div>
                <div className="flex gap-2">
                  <button
                    onClick={() => handleOrder(dish.name, activeFamily)}
                    className="px-3 py-1 rounded-lg bg-violet-600 text-white"
                  >
                    Passer la commande
                  </button>
                </div>
              </div>
            ))}
          </div>
        )}
      </div>

      {/* Illustrative images block (replace with your images) */}
      <div className="mt-4 grid grid-cols-2 sm:grid-cols-4 gap-3">
        <img src="https://source.unsplash.com/400x300/?sandwich" alt="sandwich" className="rounded-lg object-cover h-28 w-full" />
        <img src="https://source.unsplash.com/400x300/?burger" alt="burger" className="rounded-lg object-cover h-28 w-full" />
        <img src="https://source.unsplash.com/400x300?s=food" alt="food" className="rounded-lg object-cover h-28 w-full" />
        <img src="https://source.unsplash.com/400x300/?shawarma" alt="shawarma" className="rounded-lg object-cover h-28 w-full" />
      </div>
    </section>
  </main>

  {/* Modal: Order */}
  {selectedDish && (
    <div className="fixed inset-0 bg-black/40 flex items-center justify-center p-4">
      <div className="bg-white rounded-xl max-w-md w-full p-4">
        <h4 className="font-semibold text-lg">Commander: {selectedDish.name}</h4>
        <p className="text-sm text-gray-600 mt-2">Choisissez si vous souhaitez être livré ou manger sur place.</p>

        <div className="flex gap-2 mt-4">
          <button
            onClick={() => confirmOrder("livraison")}
            className="flex-1 px-3 py-2 rounded-lg bg-violet-600 text-white"
          >
            Livraison
          </button>
          <button
            onClick={() => confirmOrder("surplace")}
            className="flex-1 px-3 py-2 rounded-lg border"
          >
            Sur place
          </button>
        </div>

        <div className="mt-3 text-xs text-gray-500">
          Si vous choisissez livraison, après l'ouverture de WhatsApp envoyez votre position (bouton pièce jointe &gt; Localisation) au numéro +223 72 91 0000.
        </div>

        <button
          onClick={() => setSelectedDish(null)}
          className="mt-4 text-sm text-gray-600 underline"
        >
          Annuler
        </button>
      </div>
    </div>
  )}

  <footer className="max-w-4xl mx-auto mt-8 text-center text-gray-500 text-sm">
    <p>© CJDC - Menu interactif. Remplacez /logo.png par votre logo réel dans le dossier public.</p>
  </footer>
</div>

); }

