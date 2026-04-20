<!doctype html>
<html lang="fr" class="h-full">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ESSAIYE VOYAGE</title>
  <script src="https://cdn.tailwindcss.com/3.4.17"></script>
  <script src="https://cdn.jsdelivr.net/npm/lucide@0.263.0/dist/umd/lucide.min.js"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700;800;900&amp;family=Space+Mono:wght@400;700&amp;display=swap" rel="stylesheet">
  <script>
tailwind.config = {
  theme: {
    extend: {
      fontFamily: {
        outfit: ['Outfit', 'sans-serif'],
        mono: ['Space Mono', 'monospace']
      }
    }
  }
}
</script>
  <style>
  @keyframes float { 0%,100%{transform:translateY(0)} 50%{transform:translateY(-12px)} }
  @keyframes slideUp { from{opacity:0;transform:translateY(40px)} to{opacity:1;transform:translateY(0)} }
  @keyframes fadeIn { from{opacity:0} to{opacity:1} }
  @keyframes pulse-glow { 0%,100%{box-shadow:0 0 20px rgba(234,179,8,0.3)} 50%{box-shadow:0 0 40px rgba(234,179,8,0.6)} }
  .float-anim { animation: float 4s ease-in-out infinite; }
  .slide-up { animation: slideUp 0.7s ease-out both; }
  .fade-in { animation: fadeIn 0.5s ease-out both; }
  .glow { animation: pulse-glow 2s ease-in-out infinite; }
  .card-hover { transition: all 0.4s cubic-bezier(0.175,0.885,0.32,1.275); }
  .card-hover:hover { transform: translateY(-8px) scale(1.02); }
  .gradient-text { background: linear-gradient(135deg, #eab308, #f59e0b, #fbbf24); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
  .nav-blur { backdrop-filter: blur(16px); -webkit-backdrop-filter: blur(16px); }
  .search-panel { background: linear-gradient(135deg, rgba(15,23,42,0.95), rgba(30,41,59,0.95)); backdrop-filter: blur(20px); }
  .price-tag { background: linear-gradient(135deg, #eab308, #d97706); }
  .site-badge { font-size: 0.65rem; padding: 2px 6px; border-radius: 4px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.5px; }
  html, body { height: 100%; margin: 0; }
  body { overflow-x: hidden; }
  .tab-active { border-bottom: 3px solid #eab308; color: #eab308; }
  .result-card { border-left: 4px solid transparent; transition: all 0.3s ease; }
  .result-card:hover { border-left-color: #eab308; }
  input[type="date"]::-webkit-calendar-picker-indicator { filter: invert(1); }
</style>
  <style>body { box-sizing: border-box; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
 </head>
 <body class="h-full bg-slate-950 font-outfit text-white overflow-auto">
  <div id="app-wrapper" class="w-full min-h-full" style="background: radial-gradient(ellipse at 20% 0%, rgba(234,179,8,0.08) 0%, transparent 50%), radial-gradient(ellipse at 80% 100%, rgba(59,130,246,0.06) 0%, transparent 50%), #0a0e1a;"><!-- NAV -->
   <nav class="fixed top-0 left-0 right-0 z-50 nav-blur bg-slate-950/70 border-b border-white/5">
    <div class="max-w-7xl mx-auto px-4 py-3 flex items-center justify-between">
     <div class="flex items-center gap-3">
      <div class="w-10 h-10 rounded-xl bg-gradient-to-br from-yellow-400 to-amber-600 flex items-center justify-center font-black text-slate-950 text-lg">
       E
      </div>
      <div>
       <div id="nav-title" class="font-extrabold text-sm tracking-wide">
        ESSAIYE VOYAGE
       </div>
       <div id="nav-slogan" class="text-[10px] text-yellow-400/70 font-light">
        Voyagez malin, payez moins
       </div>
      </div>
     </div>
     <div class="hidden md:flex items-center gap-6 text-sm text-slate-400"><a href="#search-section" class="hover:text-yellow-400 transition cursor-pointer">Rechercher</a> <a href="#destinations-section" class="hover:text-yellow-400 transition cursor-pointer">Destinations</a> <a href="#deals-section" class="hover:text-yellow-400 transition cursor-pointer">Offres</a> <a href="#contact-section" class="hover:text-yellow-400 transition cursor-pointer">Contact</a>
     </div><button onclick="document.getElementById('search-section').scrollIntoView({behavior:'smooth'})" class="px-4 py-2 rounded-lg bg-yellow-500 text-slate-950 font-bold text-xs hover:bg-yellow-400 transition">Réserver</button>
    </div>
   </nav><!-- HERO -->
   <header class="relative pt-28 pb-20 px-4 text-center overflow-hidden">
    <div class="absolute inset-0 opacity-10">
     <div class="absolute top-20 left-[10%] w-64 h-64 rounded-full bg-yellow-400 blur-[100px]"></div>
     <div class="absolute bottom-10 right-[15%] w-48 h-48 rounded-full bg-blue-500 blur-[80px]"></div>
    </div>
    <div class="relative z-10 max-w-4xl mx-auto">
     <div class="float-anim inline-block mb-6 text-6xl">
      ✈️
     </div>
     <h1 class="slide-up text-4xl md:text-6xl lg:text-7xl font-black mb-4 leading-tight"><span id="hero-title" class="gradient-text">ESSAIYE VOYAGE</span></h1>
     <p id="hero-slogan" class="slide-up text-lg md:text-xl text-slate-400 mb-8 font-light" style="animation-delay:0.15s">Voyagez malin, payez moins</p>
     <div class="slide-up flex flex-wrap justify-center gap-4 text-xs text-slate-500" style="animation-delay:0.3s"><span class="flex items-center gap-1 bg-white/5 px-3 py-1.5 rounded-full"><i data-lucide="shield-check" class="w-3 h-3 text-green-400"></i> Paiement sécurisé</span> <span class="flex items-center gap-1 bg-white/5 px-3 py-1.5 rounded-full"><i data-lucide="badge-euro" class="w-3 h-3 text-yellow-400"></i> EUR + DZD</span> <span class="flex items-center gap-1 bg-white/5 px-3 py-1.5 rounded-full"><i data-lucide="globe" class="w-3 h-3 text-blue-400"></i> Toutes les compagnies</span>
     </div>
    </div>
   </header><!-- SEARCH -->
   <section id="search-section" class="px-4 pb-16 -mt-4">
    <div class="max-w-5xl mx-auto search-panel rounded-2xl p-6 border border-white/10 shadow-2xl"><!-- Tabs -->
     <div class="flex gap-6 mb-6 border-b border-white/10 pb-3"><button onclick="switchTab('flights')" id="tab-flights" class="flex items-center gap-2 pb-1 text-sm font-semibold tab-active transition"> <i data-lucide="plane" class="w-4 h-4"></i> Vols </button> <button onclick="switchTab('hotels')" id="tab-hotels" class="flex items-center gap-2 pb-1 text-sm font-semibold text-slate-500 hover:text-slate-300 transition"> <i data-lucide="building-2" class="w-4 h-4"></i> Hôtels </button>
     </div><!-- Flight Search -->
     <div id="panel-flights">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4 mb-4">
       <div><label class="block text-xs text-slate-400 mb-1 font-medium">Départ</label>
        <div class="relative"><i data-lucide="map-pin" class="absolute left-3 top-1/2 -translate-y-1/2 w-4 h-4 text-yellow-400"></i> <select id="flight-from" class="w-full bg-white/5 border border-white/10 rounded-xl pl-10 pr-4 py-3 text-sm focus:border-yellow-400 focus:outline-none transition appearance-none text-white"> <option value="ALG">Alger (ALG)</option> <option value="ORN">Oran (ORN)</option> <option value="CZL">Constantine (CZL)</option> <option value="AAE">Annaba (AAE)</option> <option value="TLM">Tlemcen (TLM)</option> </select>
        </div>
       </div>
       <div><label class="block text-xs text-slate-400 mb-1 font-medium">Arrivée</label>
        <div class="relative"><i data-lucide="map-pin" class="absolute left-3 top-1/2 -translate-y-1/2 w-4 h-4 text-blue-400"></i> <select id="flight-to" class="w-full bg-white/5 border border-white/10 rounded-xl pl-10 pr-4 py-3 text-sm focus:border-yellow-400 focus:outline-none transition appearance-none text-white"> <option value="CDG">Paris CDG</option> <option value="IST">Istanbul (IST)</option> <option value="BCN">Barcelone (BCN)</option> <option value="FCO">Rome (FCO)</option> <option value="DXB">Dubaï (DXB)</option> <option value="TUN">Tunis (TUN)</option> <option value="CMN">Casablanca (CMN)</option> <option value="LHR">Londres (LHR)</option> </select>
        </div>
       </div>
       <div><label class="block text-xs text-slate-400 mb-1 font-medium">Date départ</label> <input type="date" id="flight-date" class="w-full bg-white/5 border border-white/10 rounded-xl px-4 py-3 text-sm focus:border-yellow-400 focus:outline-none transition text-white">
       </div>
       <div><label class="block text-xs text-slate-400 mb-1 font-medium">Passagers</label> <select id="flight-pax" class="w-full bg-white/5 border border-white/10 rounded-xl px-4 py-3 text-sm focus:border-yellow-400 focus:outline-none transition appearance-none text-white"> <option>1 passager</option> <option>2 passagers</option> <option>3 passagers</option> <option>4 passagers</option> </select>
       </div>
      </div><button onclick="searchFlights()" class="w-full glow bg-gradient-to-r from-yellow-500 to-amber-500 text-slate-950 font-bold py-3.5 rounded-xl hover:from-yellow-400 hover:to-amber-400 transition text-sm flex items-center justify-center gap-2"> <i data-lucide="search" class="w-4 h-4"></i> Comparer les prix des vols </button>
     </div><!-- Hotel Search -->
     <div id="panel-hotels" class="hidden">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4 mb-4">
       <div><label class="block text-xs text-slate-400 mb-1 font-medium">Destination</label>
        <div class="relative"><i data-lucide="building-2" class="absolute left-3 top-1/2 -translate-y-1/2 w-4 h-4 text-yellow-400"></i> <select id="hotel-city" class="w-full bg-white/5 border border-white/10 rounded-xl pl-10 pr-4 py-3 text-sm focus:border-yellow-400 focus:outline-none transition appearance-none text-white"> <option value="Paris">Paris</option> <option value="Istanbul">Istanbul</option> <option value="Barcelone">Barcelone</option> <option value="Rome">Rome</option> <option value="Dubaï">Dubaï</option> <option value="Tunis">Tunis</option> <option value="Marrakech">Marrakech</option> </select>
        </div>
       </div>
       <div><label class="block text-xs text-slate-400 mb-1 font-medium">Check-in</label> <input type="date" id="hotel-checkin" class="w-full bg-white/5 border border-white/10 rounded-xl px-4 py-3 text-sm focus:border-yellow-400 focus:outline-none transition text-white">
       </div>
       <div><label class="block text-xs text-slate-400 mb-1 font-medium">Check-out</label> <input type="date" id="hotel-checkout" class="w-full bg-white/5 border border-white/10 rounded-xl px-4 py-3 text-sm focus:border-yellow-400 focus:outline-none transition text-white">
       </div>
       <div><label class="block text-xs text-slate-400 mb-1 font-medium">Chambres</label> <select id="hotel-rooms" class="w-full bg-white/5 border border-white/10 rounded-xl px-4 py-3 text-sm focus:border-yellow-400 focus:outline-none transition appearance-none text-white"> <option>1 chambre</option> <option>2 chambres</option> <option>3 chambres</option> </select>
       </div>
      </div><button onclick="searchHotels()" class="w-full glow bg-gradient-to-r from-yellow-500 to-amber-500 text-slate-950 font-bold py-3.5 rounded-xl hover:from-yellow-400 hover:to-amber-400 transition text-sm flex items-center justify-center gap-2"> <i data-lucide="search" class="w-4 h-4"></i> Comparer les prix des hôtels </button>
     </div>
    </div><!-- RESULTS -->
    <div id="results-container" class="max-w-5xl mx-auto mt-8 hidden">
     <div class="flex items-center justify-between mb-4">
      <h2 id="results-title" class="text-lg font-bold text-white"></h2>
      <div class="flex gap-2"><button onclick="sortResults('price')" class="text-xs bg-white/5 border border-white/10 px-3 py-1.5 rounded-lg hover:border-yellow-400/50 transition">Prix ↑</button> <button onclick="sortResults('rating')" class="text-xs bg-white/5 border border-white/10 px-3 py-1.5 rounded-lg hover:border-yellow-400/50 transition">Note ↓</button>
      </div>
     </div>
     <div id="results-list" class="space-y-3"></div>
    </div>
   </section><!-- DEALS -->
   <section id="deals-section" class="px-4 pb-20">
    <div class="max-w-6xl mx-auto">
     <div class="text-center mb-10">
      <h2 class="text-2xl md:text-3xl font-black mb-2">🔥 <span class="gradient-text">Offres du moment</span></h2>
      <p class="text-slate-500 text-sm">Les meilleurs tarifs sélectionnés pour vous</p>
     </div>
     <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-5" id="deals-grid">
     </div>
    </div>
   </section><!-- DESTINATIONS -->
   <section id="destinations-section" class="px-4 pb-20">
    <div class="max-w-6xl mx-auto">
     <div class="text-center mb-10">
      <h2 class="text-2xl md:text-3xl font-black mb-2">🌍 <span class="gradient-text">Destinations du Monde</span></h2>
      <p class="text-slate-500 text-sm">Découvrez nos destinations les plus populaires pour vos prochains voyages.</p>
     </div>
     <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-5">
      <div class="bg-slate-900/70 p-6 rounded-3xl border border-white/10 card-hover">
       <h3 class="text-lg font-bold mb-2">Paris, France</h3>
       <p class="text-slate-400 text-sm">Culture, gastronomie et romance au cœur de l'Europe.</p>
      </div>
      <div class="bg-slate-900/70 p-6 rounded-3xl border border-white/10 card-hover">
       <h3 class="text-lg font-bold mb-2">Dubaï, Émirats</h3>
       <p class="text-slate-400 text-sm">Luxe futuriste, shopping et plages ensoleillées.</p>
      </div>
      <div class="bg-slate-900/70 p-6 rounded-3xl border border-white/10 card-hover">
       <h3 class="text-lg font-bold mb-2">Bali, Indonésie</h3>
       <p class="text-slate-400 text-sm">Plages, temples et nature tropicale pour se ressourcer.</p>
      </div>
      <div class="bg-slate-900/70 p-6 rounded-3xl border border-white/10 card-hover">
       <h3 class="text-lg font-bold mb-2">New York, USA</h3>
       <p class="text-slate-400 text-sm">Vivez l'effervescence de la ville qui ne dort jamais.</p>
      </div>
     </div>
    </div>
   </section><!-- CONTACT -->
   <section id="contact-section" class="px-4 pb-20">
    <div class="max-w-2xl mx-auto search-panel rounded-2xl p-8 border border-white/10">
     <h2 class="text-xl font-bold mb-6 text-center gradient-text">Contactez-nous</h2>
     <form onsubmit="submitContact(event)" class="space-y-4">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
       <div><label class="block text-xs text-slate-400 mb-1">Nom complet</label> <input type="text" required class="w-full bg-white/5 border border-white/10 rounded-xl px-4 py-3 text-sm focus:border-yellow-400 focus:outline-none transition text-white" placeholder="Votre nom">
       </div>
       <div><label class="block text-xs text-slate-400 mb-1">Téléphone</label> <input type="tel" class="w-full bg-white/5 border border-white/10 rounded-xl px-4 py-3 text-sm focus:border-yellow-400 focus:outline-none transition text-white" placeholder="+213...">
       </div>
      </div>
      <div><label class="block text-xs text-slate-400 mb-1">Email</label> <input type="email" required class="w-full bg-white/5 border border-white/10 rounded-xl px-4 py-3 text-sm focus:border-yellow-400 focus:outline-none transition text-white" placeholder="votre@email.com">
      </div>
      <div><label class="block text-xs text-slate-400 mb-1">Message</label> <textarea rows="3" required class="w-full bg-white/5 border border-white/10 rounded-xl px-4 py-3 text-sm focus:border-yellow-400 focus:outline-none transition text-white resize-none" placeholder="Décrivez votre voyage idéal..."></textarea>
      </div><button type="submit" class="w-full bg-gradient-to-r from-yellow-500 to-amber-500 text-slate-950 font-bold py-3 rounded-xl hover:from-yellow-400 hover:to-amber-400 transition text-sm">Envoyer</button>
      <div id="contact-success" class="hidden text-center text-green-400 text-sm py-2 bg-green-400/10 rounded-lg">
       ✅ Message envoyé ! Nous vous répondrons rapidement.
      </div>
     </form>
    </div>
   </section><!-- FOOTER -->
   <footer class="border-t border-white/5 px-4 py-8">
    <div class="max-w-6xl mx-auto flex flex-col md:flex-row items-center justify-between gap-4 text-xs text-slate-600">
     <div class="flex items-center gap-2">
      <div class="w-6 h-6 rounded-md bg-gradient-to-br from-yellow-400 to-amber-600 flex items-center justify-center font-black text-slate-950 text-[10px]">
       E
      </div><span id="footer-title" class="font-semibold text-slate-500">ESSAIYE VOYAGE</span>
     </div>
     <div class="flex items-center gap-4"><span id="footer-phone" class="flex items-center gap-1"><i data-lucide="phone" class="w-3 h-3"></i> +213 XX XX XX XX</span> <span id="footer-email" class="flex items-center gap-1"><i data-lucide="mail" class="w-3 h-3"></i> contact@essaiyevoyage.com</span>
     </div><span>© 2025 Tous droits réservés</span>
    </div>
   </footer>
  </div>
  <script>
// Exchange rate
const DZD_RATE = 147.5;
const formatEUR = (n) => n.toFixed(0) + ' €';
const formatDZD = (n) => Math.round(n * DZD_RATE).toLocaleString('fr') + ' DZD';

// Site colors for comparison badges
const SITES = {
  flights: [
    { name: 'Skyscanner', color: '#0770e3', text: '#fff' },
    { name: 'Kayak', color: '#ff690f', text: '#fff' },
    { name: 'Google Flights', color: '#34a853', text: '#fff' },
    { name: 'Kiwi', color: '#00a991', text: '#fff' },
    { name: 'Air Algérie', color: '#d42e12', text: '#fff' },
    { name: 'Transavia', color: '#00b2a9', text: '#fff' },
  ],
  hotels: [
    { name: 'Booking.com', color: '#003580', text: '#fff' },
    { name: 'Hotels.com', color: '#d32f2f', text: '#fff' },
    { name: 'Trivago', color: '#007faf', text: '#fff' },
    { name: 'Agoda', color: '#5c2d91', text: '#fff' },
    { name: 'Expedia', color: '#00355f', text: '#fff' },
  ]
};

// Flight data generator
const FLIGHT_ROUTES = {
  'CDG': { base: 120, airlines: ['Air Algérie', 'Air France', 'Transavia', 'ASL Airlines'] },
  'IST': { base: 140, airlines: ['Turkish Airlines', 'Air Algérie', 'Pegasus'] },
  'BCN': { base: 90, airlines: ['Vueling', 'Air Algérie', 'Transavia'] },
  'FCO': { base: 100, airlines: ['Air Algérie', 'ITA Airways', 'Ryanair'] },
  'DXB': { base: 280, airlines: ['Emirates', 'Air Algérie', 'Turkish Airlines'] },
  'TUN': { base: 70, airlines: ['Tunisair', 'Air Algérie', 'Nouvelair'] },
  'CMN': { base: 95, airlines: ['Royal Air Maroc', 'Air Algérie'] },
  'LHR': { base: 150, airlines: ['British Airways', 'Air Algérie', 'easyJet'] },
};

const HOTEL_DATA = {
  'Paris': [
    { name: 'Hôtel Le Marais Charme', stars: 4, base: 95 },
    { name: 'Ibis Gare du Nord', stars: 3, base: 62 },
    { name: 'Mercure Montmartre', stars: 4, base: 110 },
    { name: 'Novotel Tour Eiffel', stars: 4, base: 135 },
  ],
  'Istanbul': [
    { name: 'Sultan Ahmet Palace', stars: 4, base: 55 },
    { name: 'Galata Tower Hotel', stars: 3, base: 38 },
    { name: 'Bosphorus View Suites', stars: 5, base: 90 },
  ],
  'Barcelone': [
    { name: 'Hotel Ramblas Centro', stars: 3, base: 70 },
    { name: 'Casa Gràcia Barcelona', stars: 4, base: 95 },
    { name: 'W Barcelona', stars: 5, base: 180 },
  ],
  'Rome': [
    { name: 'Hotel Colosseo Roma', stars: 3, base: 65 },
    { name: 'Palazzo Navona', stars: 4, base: 105 },
  ],
  'Dubaï': [
    { name: 'Rove Downtown', stars: 3, base: 70 },
    { name: 'JW Marriott Marquis', stars: 5, base: 150 },
    { name: 'Atlantis The Palm', stars: 5, base: 220 },
  ],
  'Tunis': [
    { name: 'Hôtel Laico Tunis', stars: 5, base: 60 },
    { name: 'Golden Tulip El Mechtel', stars: 4, base: 42 },
  ],
  'Marrakech': [
    { name: 'Riad Jardin Secret', stars: 4, base: 50 },
    { name: 'La Mamounia', stars: 5, base: 200 },
    { name: 'Ibis Marrakech Palmeraie', stars: 3, base: 35 },
  ],
};

let currentResults = [];
let currentType = 'flights';

function switchTab(type) {
  currentType = type;
  document.getElementById('panel-flights').classList.toggle('hidden', type !== 'flights');
  document.getElementById('panel-hotels').classList.toggle('hidden', type !== 'hotels');
  document.getElementById('tab-flights').classList.toggle('tab-active', type === 'flights');
  document.getElementById('tab-hotels').classList.toggle('tab-active', type === 'hotels');
  if (type !== 'flights') document.getElementById('tab-flights').classList.add('text-slate-500');
  else document.getElementById('tab-flights').classList.remove('text-slate-500');
  if (type !== 'hotels') document.getElementById('tab-hotels').classList.add('text-slate-500');
  else document.getElementById('tab-hotels').classList.remove('text-slate-500');
  document.getElementById('results-container').classList.add('hidden');
}

function randomVariation(base, min, max) {
  return Math.round(base * (1 + (Math.random() * (max - min) + min)));
}

function searchFlights() {
  const from = document.getElementById('flight-from').value;
  const to = document.getElementById('flight-to').value;
  const route = FLIGHT_ROUTES[to];
  if (!route) return;

  currentResults = [];
  const sites = SITES.flights;
  route.airlines.forEach(airline => {
    const offers = [];
    const numSites = 2 + Math.floor(Math.random() * 3);
    const shuffled = [...sites].sort(() => Math.random() - 0.5).slice(0, numSites);
    shuffled.forEach(site => {
      offers.push({ site: site.name, color: site.color, textColor: site.text, price: randomVariation(route.base, -0.15, 0.35) });
    });
    offers.sort((a, b) => a.price - b.price);
    const rating = (3.5 + Math.random() * 1.5).toFixed(1);
    const duration = `${Math.floor(2 + Math.random() * 4)}h${Math.floor(Math.random() * 50).toString().padStart(2,'0')}`;
    const stops = Math.random() > 0.6 ? 'Direct' : '1 escale';
    currentResults.push({ type: 'flight', name: airline, offers, rating: parseFloat(rating), duration, stops, bestPrice: offers[0].price });
  });
  currentResults.sort((a, b) => a.bestPrice - b.bestPrice);
  renderResults(`Vols ${from} → ${to}`);
}

function searchHotels() {
  const city = document.getElementById('hotel-city').value;
  const hotels = HOTEL_DATA[city];
  if (!hotels) return;

  currentResults = [];
  const sites = SITES.hotels;
  hotels.forEach(h => {
    const offers = [];
    const numSites = 2 + Math.floor(Math.random() * 3);
    const shuffled = [...sites].sort(() => Math.random() - 0.5).slice(0, numSites);
    shuffled.forEach(site => {
      offers.push({ site: site.name, color: site.color, textColor: site.text, price: randomVariation(h.base, -0.1, 0.3) });
    });
    offers.sort((a, b) => a.price - b.price);
    const rating = (3.5 + Math.random() * 1.5).toFixed(1);
    currentResults.push({ type: 'hotel', name: h.name, stars: h.stars, offers, rating: parseFloat(rating), bestPrice: offers[0].price });
  });
  currentResults.sort((a, b) => a.bestPrice - b.bestPrice);
  renderResults(`Hôtels à ${city}`);
}

function sortResults(by) {
  if (by === 'price') currentResults.sort((a, b) => a.bestPrice - b.bestPrice);
  else currentResults.sort((a, b) => b.rating - a.rating);
  renderResults(document.getElementById('results-title').textContent);
}

function renderResults(title) {
  const container = document.getElementById('results-container');
  const list = document.getElementById('results-list');
  document.getElementById('results-title').textContent = title;
  container.classList.remove('hidden');
  list.innerHTML = '';

  currentResults.forEach((item, idx) => {
    const card = document.createElement('div');
    card.className = 'result-card bg-white/[0.03] border border-white/10 rounded-xl p-5 fade-in hover:bg-white/[0.06] transition';
    card.style.animationDelay = `${idx * 0.08}s`;

    const starsHTML = item.type === 'hotel' ? '⭐'.repeat(item.stars) : '';
    const metaHTML = item.type === 'flight'
      ? `<span class="text-xs text-slate-500 flex items-center gap-1"><i data-lucide="clock" class="w-3 h-3"></i>${item.duration}</span>
         <span class="text-xs px-2 py-0.5 rounded-full ${item.stops === 'Direct' ? 'bg-green-500/10 text-green-400' : 'bg-yellow-500/10 text-yellow-400'}">${item.stops}</span>`
      : `<span class="text-xs text-slate-500">${starsHTML}</span>`;

    const offersHTML = item.offers.map((o, i) => `
      <div class="flex items-center justify-between py-2 ${i > 0 ? 'border-t border-white/5' : ''}">
        <span class="site-badge" style="background:${o.color};color:${o.textColor}">${o.site}</span>
        <div class="text-right">
          <span class="font-bold text-sm ${i === 0 ? 'text-yellow-400' : 'text-white'}">${formatEUR(o.price)}</span>
          <span class="text-[10px] text-slate-500 ml-2">${formatDZD(o.price)}</span>
          ${i === 0 ? '<span class="ml-2 text-[9px] bg-yellow-400/20 text-yellow-300 px-1.5 py-0.5 rounded font-bold">MEILLEUR</span>' : ''}
        </div>
      </div>
    `).join('');

    card.innerHTML = `
      <div class="flex items-start justify-between mb-3">
        <div>
          <h3 class="font-bold text-white text-sm">${item.name}</h3>
          <div class="flex items-center gap-2 mt-1">${metaHTML}</div>
        </div>
        <div class="flex items-center gap-1 bg-yellow-400/10 px-2 py-1 rounded-lg">
          <i data-lucide="star" class="w-3 h-3 text-yellow-400"></i>
          <span class="text-xs font-bold text-yellow-400">${item.rating}</span>
        </div>
      </div>
      <div class="bg-white/[0.02] rounded-lg p-3">${offersHTML}</div>
      <div class="mt-3 text-center">
        <button onclick="bookNow('${item.name}', ${item.bestPrice})" class="text-xs bg-yellow-500/20 text-yellow-400 px-6 py-2 rounded-lg hover:bg-yellow-500/30 transition font-semibold">
          Réserver à partir de ${formatEUR(item.bestPrice)}
        </button>
      </div>
    `;
    list.appendChild(card);
  });
  lucide.createIcons();
  container.scrollIntoView({ behavior: 'smooth', block: 'start' });
}

// Booking inline confirmation
function bookNow(name, price) {
  const overlay = document.createElement('div');
  overlay.className = 'fixed inset-0 z-[100] flex items-center justify-center bg-black/60 fade-in';
  overlay.innerHTML = `
    <div class="bg-slate-900 border border-white/10 rounded-2xl p-8 max-w-md w-full mx-4 text-center slide-up">
      <div class="text-4xl mb-4">🎉</div>
      <h3 class="text-xl font-bold gradient-text mb-2">Demande de réservation</h3>
      <p class="text-slate-400 text-sm mb-1"><strong class="text-white">${name}</strong></p>
      <p class="text-yellow-400 font-bold text-lg mb-1">${formatEUR(price)}</p>
      <p class="text-slate-500 text-xs mb-6">${formatDZD(price)}</p>
      <p class="text-slate-500 text-xs mb-6">Un conseiller ESSAIYE VOYAGE vous contactera sous 24h pour finaliser votre réservation.</p>
      <button onclick="this.closest('.fixed').remove()" class="bg-yellow-500 text-slate-950 font-bold px-8 py-2.5 rounded-xl text-sm hover:bg-yellow-400 transition">Compris !</button>
    </div>
  `;
  document.body.appendChild(overlay);
  overlay.addEventListener('click', (e) => { if (e.target === overlay) overlay.remove(); });
}

// Contact form
function submitContact(e) {
  e.preventDefault();
  document.getElementById('contact-success').classList.remove('hidden');
  e.target.reset();
  setTimeout(() => document.getElementById('contact-success').classList.add('hidden'), 4000);
}

// Deals
function renderDeals() {
  const deals = [
    { emoji: '🇫🇷', route: 'Alger → Paris', type: 'Vol A/R', price: 119, tag: '-30%' },
    { emoji: '🇹🇷', route: 'Oran → Istanbul', type: 'Vol + Hôtel 5j', price: 349, tag: 'POPULAIRE' },
    { emoji: '🇪🇸', route: 'Alger → Barcelone', type: 'Vol A/R', price: 89, tag: 'FLASH' },
    { emoji: '🇦🇪', route: 'Constantine → Dubaï', type: 'Vol + Hôtel 7j', price: 599, tag: 'LUXE' },
    { emoji: '🇲🇦', route: 'Tlemcen → Marrakech', type: 'Vol A/R', price: 75, tag: '-25%' },
    { emoji: '🇮🇹', route: 'Annaba → Rome', type: 'Vol + Hôtel 4j', price: 279, tag: 'NOUVEAU' },
  ];
  const grid = document.getElementById('deals-grid');
  grid.innerHTML = deals.map((d, i) => `
    <div class="card-hover bg-white/[0.03] border border-white/10 rounded-xl p-5 cursor-pointer group" style="animation: slideUp 0.6s ease-out ${i * 0.1}s both">
      <div class="flex items-center justify-between mb-3">
        <span class="text-3xl">${d.emoji}</span>
        <span class="text-[10px] font-bold px-2 py-1 rounded-full bg-yellow-400/20 text-yellow-300">${d.tag}</span>
      </div>
      <h3 class="font-bold text-white text-sm mb-1">${d.route}</h3>
      <p class="text-xs text-slate-500 mb-4">${d.type}</p>
      <div class="flex items-end justify-between">
        <div>
          <span class="text-xl font-black text-yellow-400">${formatEUR(d.price)}</span>
          <span class="block text-[10px] text-slate-500">${formatDZD(d.price)}</span>
        </div>
        <span class="text-xs text-slate-600 group-hover:text-yellow-400 transition flex items-center gap-1">Voir <i data-lucide="arrow-right" class="w-3 h-3"></i></span>
      </div>
    </div>
  `).join('');
  lucide.createIcons();
}

// Set default dates
function setDefaultDates() {
  const today = new Date();
  const next = new Date(today); next.setDate(today.getDate() + 14);
  const fmt = d => d.toISOString().split('T')[0];
  document.getElementById('flight-date').value = fmt(next);
  document.getElementById('hotel-checkin').value = fmt(next);
  const co = new Date(next); co.setDate(co.getDate() + 5);
  document.getElementById('hotel-checkout').value = fmt(co);
}

// Element SDK
const defaultConfig = {
  site_title: 'ESSAIYE VOYAGE',
  slogan: 'Voyagez malin, payez moins',
  phone_number: '+213 XX XX XX XX',
  email_address: 'contact@essaiyevoyage.com',
  background_color: '#0a0e1a',
  surface_color: '#0f172a',
  text_color: '#f8fafc',
  primary_action_color: '#eab308',
  secondary_action_color: '#64748b',
  font_family: 'Outfit',
  font_size: 16
};

function applyConfig(config) {
  const c = { ...defaultConfig, ...config };
  const t = (id, val) => { const el = document.getElementById(id); if (el) el.textContent = val; };
  t('nav-title', c.site_title);
  t('nav-slogan', c.slogan);
  t('hero-title', c.site_title);
  t('hero-slogan', c.slogan);
  t('footer-title', c.site_title);
  t('footer-phone', c.phone_number);
  t('footer-email', c.email_address);

  const root = document.getElementById('app-wrapper');
  root.style.background = `radial-gradient(ellipse at 20% 0%, ${c.primary_action_color}14 0%, transparent 50%), radial-gradient(ellipse at 80% 100%, ${c.secondary_action_color}10 0%, transparent 50%), ${c.background_color}`;
  document.body.style.fontFamily = `${c.font_family}, Outfit, sans-serif`;
}

window.elementSdk.init({
  defaultConfig,
  onConfigChange: async (config) => applyConfig(config),
  mapToCapabilities: (config) => ({
    recolorables: [
      { get: () => config.background_color || defaultConfig.background_color, set: (v) => { config.background_color = v; window.elementSdk.setConfig({ background_color: v }); } },
      { get: () => config.surface_color || defaultConfig.surface_color, set: (v) => { config.surface_color = v; window.elementSdk.setConfig({ surface_color: v }); } },
      { get: () => config.text_color || defaultConfig.text_color, set: (v) => { config.text_color = v; window.elementSdk.setConfig({ text_color: v }); } },
      { get: () => config.primary_action_color || defaultConfig.primary_action_color, set: (v) => { config.primary_action_color = v; window.elementSdk.setConfig({ primary_action_color: v }); } },
      { get: () => config.secondary_action_color || defaultConfig.secondary_action_color, set: (v) => { config.secondary_action_color = v; window.elementSdk.setConfig({ secondary_action_color: v }); } },
    ],
    borderables: [],
    fontEditable: { get: () => config.font_family || defaultConfig.font_family, set: (v) => { config.font_family = v; window.elementSdk.setConfig({ font_family: v }); } },
    fontSizeable: { get: () => config.font_size || defaultConfig.font_size, set: (v) => { config.font_size = v; window.elementSdk.setConfig({ font_size: v }); } },
  }),
  mapToEditPanelValues: (config) => new Map([
    ['site_title', config.site_title || defaultConfig.site_title],
    ['slogan', config.slogan || defaultConfig.slogan],
    ['phone_number', config.phone_number || defaultConfig.phone_number],
    ['email_address', config.email_address || defaultConfig.email_address],
  ])
});

setDefaultDates();
renderDeals();
lucide.createIcons();
</script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9ecc7f47b2cc304e',t:'MTc3NjI3MjMyOS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
