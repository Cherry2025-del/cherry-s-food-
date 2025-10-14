# cherry-s-food-
Menu
<!doctype html>
<html lang="fr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Cherry's Bakery & Ice Cream</title>
  <meta name="description" content="Menu Cherry's — Fast-food, Pizzas, Grillades, Glaces, Boissons, Café & Thé. Commander via WhatsApp +22384124748" />
  <link rel="icon" href="assets/logo.png" />

  <style>
    /* -------------------------
       CONFIG COULEURS & TYPO
       ------------------------- */
    :root{
      --accent:#b71c1c;       /* rouge Cherry's */
      --blue:#0f66a8;         /* bleu d'accent */
      --bg:#fffaf6;
      --glass: rgba(255,255,255,0.78);
      --glass-dark: rgba(0,0,0,0.38);
      --maxw:1100px;
      --radius:14px;
      font-family: "Inter", "Helvetica Neue", Arial, sans-serif;
    }
    *{box-sizing:border-box}
    html,body{height:100%;margin:0;background:var(--bg);color:#222;-webkit-font-smoothing:antialiased}
    a{color:inherit}
    img{max-width:100%;display:block}

    /* -------------------------
       HEADER NAV FIXE
       ------------------------- */
    header.site-header{
      position:fixed;top:0;left:0;right:0;z-index:999;
      backdrop-filter: blur(6px);
      background: linear-gradient(180deg, rgba(255,255,255,0.95), rgba(255,255,255,0.85));
      border-bottom: 1px solid rgba(0,0,0,0.06);
      display:flex;align-items:center;justify-content:space-between;padding:10px 18px;
    }
    .brand{display:flex;align-items:center;gap:12px}
    .brand img{height:56px;width:56px;object-fit:contain;border-radius:10px}
    .brand h1{margin:0;font-size:18px;color:var(--accent);letter-spacing:0.6px}
    nav.topnav{display:flex;gap:8px;align-items:center}
    nav.topnav a{
      display:inline-block;padding:8px 12px;border-radius:10px;text-decoration:none;font-weight:600;
      color:var(--blue);
    }
    nav.topnav a.active{background:var(--blue);color:#fff;box-shadow:0 6px 18px rgba(15,102,168,0.14)}

    /* -------------------------
       SECTIONS (full screen visual)
       ------------------------- */
    main{margin-top:88px}
    section.panel{
      min-height:84vh;display:flex;align-items:center;padding:48px 18px;
      background-position:center;background-size:cover;background-repeat:no-repeat;position:relative;
    }
    section.panel::after{
      content:"";position:absolute;inset:0;
      background:linear-gradient(180deg, rgba(0,0,0,0.28), rgba(0,0,0,0.08));
      pointer-events:none;
    }
    .panel-inner{
      position:relative;z-index:2;max-width:var(--maxw);margin:0 auto;width:100%;
      display:grid;grid-template-columns:1fr 420px;gap:22px;align-items:start;
    }
    /* card contenant texte du menu (semi transparent) */
    .menu-card{
      background:var(--glass);padding:18px;border-radius:12px;box-shadow:0 10px 30px rgba(0,0,0,0.12);
      max-height:66vh;overflow:auto;
    }
    .menu-card h2{margin:0 0 8px 0;color:var(--accent);letter-spacing:0.6px}
    .menu-section{margin-top:10px}
    .item{display:flex;justify-content:space-between;padding:10px 6px;border-bottom:1px dashed rgba(0,0,0,0.06)}
    .price{font-weight:800;color:var(--blue)}
    .hero-panel{
      border-radius:var(--radius);overflow:hidden;box-shadow:0 10px 30px rgba(0,0,0,0.15);
      background-size:cover;background-position:center;min-height:420px;
      display:flex;align-items:flex-end;padding:18px;color:#fff;
    }
    .hero-title{background:linear-gradient(90deg, rgba(0,0,0,0.6), rgba(0,0,0,0.12));padding:10px;border-radius:10px}
    .hero-title h1{margin:0;font-size:28px}
    .hero-title p{margin:6px 0 0 0;opacity:0.95}

    /* -------------------------
       STYLES GLOBAUX & UTILITAIRES
       ------------------------- */
    .actions{display:flex;gap:8px;margin-top:12px}
    .btn{
      display:inline-block;padding:10px 14px;border-radius:10px;text-decoration:none;font-weight:700;
      background:var(--blue);color:#fff;
    }
    .btn.secondary{background:transparent;border:2px solid rgba(0,0,0,0.06);color:#222}

    /* WhatsApp floating */
    .whatsapp{
      position:fixed;right:18px;bottom:18px;padding:12px 14px;border-radius:999px;
      background:#25D366;color:#053d2e;font-weight:800;display:flex;align-items:center;gap:10px;
      box-shadow:0 12px 30px rgba(37,211,102,0.18);text-decoration:none;z-index:9999;
    }
    .whatsapp small{display:block;font-size:12px;color:rgba(5,61,46,0.9)}

    /* Footer small */
    footer.site-foot{padding:30px 18px;text-align:center;color:#666}

    /* Responsive */
    @media (max-width:980px){
      .panel-inner{grid-template-columns:1fr}
      .hero-panel{min-height:260px}
      .menu-card{max-height:42vh}
    }
    @media (max-width:560px){
      .brand h1{display:none}
      nav.topnav{display:none}
      .whatsapp{right:12px;bottom:12px;padding:10px 12px}
    }

    /* Smooth scroll behavior for instant feel */
    html{scroll-behavior:smooth}
  </style>
</head>
<body>

  <!-- ============================
       HEADER / NAV
       ============================ -->
  <header class="site-header" role="banner">
    <div class="brand" aria-hidden="false">
      <!-- Place ton logo: assets/logo.png -->
      <img src="assets/logo.png" alt="Logo Cherry's">
      <h1>Cherry's</h1>
    </div>

    <nav class="topnav" aria-label="Navigation principale">
      <a href="#fastfood" data-target="fastfood">Fast-food</a>
      <a href="#pizzas" data-target="pizzas">Pizzas</a>
      <a href="#grillades" data-target="grillades">Grillades</a>
      <a href="#glaces" data-target="glaces">Glaces</a>
      <a href="#boissons" data-target="boissons">Boissons</a>
      <a href="#cafe" data-target="cafe">Café & Thé</a>
      <a href="#merci" data-target="merci">Merci</a>
    </nav>
  </header>

  <main>

    <!-- ============================
         FAST-FOOD
         Background image: assets/fastfood.jpg
         (image générée / prévue)
         ============================ -->
    <section id="fastfood" class="panel" style="background-image: url('assets/fastfood.jpg');" aria-label="Fast-food">
      <div class="panel-inner">
        <div class="menu-card" aria-labelledby="fastfood-title">
          <h2 id="fastfood-title">Fast-food</h2>
          <p>Gyros, tacos, burgers — rapides et savoureux.</p>

          <div class="menu-section" aria-label="Plats fast-food">
            <div class="item"><div>Gyros au poulet</div><div class="price">3000f</div></div>
            <div class="item"><div>Gyros au bœuf</div><div class="price">2000f</div></div>
            <div class="item"><div>Gyros Cherry's</div><div class="price">4500f</div></div>
            <div class="item"><div>Sandwich viande</div><div class="price">1000f</div></div>
            <div class="item"><div>Sandwich poulet</div><div class="price">1500f</div></div>
            <div class="item"><div>Chawarma poulet</div><div class="price">2000f</div></div>
            <div class="item"><div>Chawarma viande</div><div class="price">1500f</div></div>
            <div class="item"><div>Hamburger</div><div class="price">2500f</div></div>
            <div class="item"><div>Chicken burgers</div><div class="price">3000f</div></div>
            <div class="item"><div>Cherry's burgers</div><div class="price">4000f</div></div>
            <div class="item"><div>KFC</div><div class="price">4000f</div></div>
            <div class="item"><div>Plat de Nems (4 pièces)</div><div class="price">2500f</div></div>
            <div class="item"><div>Tacos viande</div><div class="price">2500f</div></div>
            <div class="item"><div>Tacos poulet</div><div class="price">3500f</div></div>
            <div class="item"><div>Tacos Cherry's</div><div class="price">4500f</div></div>
          </div>

          <div class="menu-section" style="margin-top:14px">
            <h3 style="margin:0 0 8px 0;color:#333">Menus Big</h3>
            <div class="item"><div>Big Sandwich</div><div class="price">10000f</div></div>
            <div class="item"><div>Big Burgers</div><div class="price">12500f</div></div>
          </div>

          <div class="actions">
            <a class="btn" href="https://wa.me/22384124748" target="_blank" rel="noreferrer">Commander sur WhatsApp</a>
            <a class="btn secondary" href="#pizzas">Voir Pizzas</a>
          </div>
        </div>

        <aside class="hero-panel" style="background-image:url('assets/fastfood.jpg');" aria-hidden="true">
          <div class="hero-title">
            <h1>Fast-food</h1>
            <p>Gyros, Tacos, Burgers — préparés avec amour.</p>
          </div>
        </aside>
      </div>
    </section>

    <!-- ============================
         PIZZAS
         Background image: assets/pizza.jpg
         ============================ -->
    <section id="pizzas" class="panel" style="background-image: url('assets/pizza.jpg');" aria-label="Pizzas">
      <div class="panel-inner">
        <div class="menu-card" aria-labelledby="pizzas-title">
          <h2 id="pizzas-title">Pizzas</h2>
          <p>Pizzas artisanales, cuisson parfaite.</p>

          <div class="menu-section">
            <div class="item"><div>Pizza Cherry's</div><div class="price">7000f</div></div>
            <div class="item"><div>Pizza Margarita</div><div class="price">5000f</div></div>
            <div class="item"><div>Pizza Orientale</div><div class="price">6000f</div></div>
            <div class="item"><div>Pizza Végétarienne</div><div class="price">6000f</div></div>
            <div class="item"><div>Pizza Kiss</div><div class="price">6500f</div></div>
          </div>

          <div class="actions">
            <a class="btn" href="https://wa.me/22384124748" target="_blank" rel="noreferrer">Commander sur WhatsApp</a>
            <a class="btn secondary" href="#grillades">Voir Grillades</a>
          </div>
        </div>

        <aside class="hero-panel" style="background-image:url('assets/pizza.jpg');" aria-hidden="true">
          <div class="hero-title">
            <h1>Pizzas</h1>
            <p>Chaudes, généreuses, goût inoubliable.</p>
          </div>
        </aside>
      </div>
    </section>

    <!-- ============================
         GRILLADES & MIXTES
         Background image: assets/brochettes.jpg
         (utiliser les images que tu as fournies)
         ============================ -->
    <section id="grillades" class="panel" style="background-image: url('assets/brochettes.jpg');" aria-label="Grillades">
      <div class="panel-inner">
        <div class="menu-card" aria-labelledby="grillades-title">
          <h2 id="grillades-title">Grillades & Mixtes</h2>
          <p>Brochettes savoureuses et mixtes à partager.</p>

          <div class="menu-section">
            <div class="item"><div>Brochette de bœuf</div><div class="price">6000f</div></div>
            <div class="item"><div>Brochette de poulet</div><div class="price">6000f</div></div>
            <div class="item"><div>Brochette de capitaine</div><div class="price">7000f</div></div>
            <div class="item"><div>1/2 poulet</div><div class="price">6000f</div></div>
          </div>

          <h3 style="margin-top:12px;color:#333">Les mixtes à partager</h3>
          <div class="menu-section">
            <div class="item"><div>Mixte fast-food (tacos, chawarma, nems, kfc, gyros)</div><div class="price">15000f</div></div>
            <div class="item"><div>Mixte grillade (brochette bœuf, capitaine, poulet)</div><div class="price">15000f</div></div>
          </div>

          <div class="actions">
            <a class="btn" href="https://wa.me/22384124748" target="_blank" rel="noreferrer">Commander sur WhatsApp</a>
            <a class="btn secondary" href="#glaces">Voir Glaces</a>
          </div>
        </div>

        <aside class="hero-panel" style="background-image:url('assets/brochettes.jpg');" aria-hidden="true">
          <div class="hero-title">
            <h1>Grillades</h1>
            <p>Idéal pour partager entre amis.</p>
          </div>
        </aside>
      </div>
    </section>

    <!-- ============================
         GLACES
         Background image: assets/glace.jpg
         (à générer si besoin)
         ============================ -->
    <section id="glaces" class="panel" style="background-image: url('assets/glace.jpg');" aria-label="Glaces">
      <div class="panel-inner">
        <div class="menu-card" aria-labelledby="glaces-title">
          <h2 id="glaces-title">Glaces</h2>
          <p>Boules, cornets et wafles bowls — gourmandise assurée.</p>

          <div class="menu-section">
            <div class="item"><div>Une boule</div><div class="price">1000f</div></div>
            <div class="item"><div>Deux boules</div><div class="price">1500f</div></div>
            <div class="item"><div>Trois boules</div><div class="price">2000f</div></div>
            <div class="item"><div>Cornet 2 boules</div><div class="price">2000f</div></div>
            <div class="item"><div>Cornet 3 boules</div><div class="price">2500f</div></div>
            <div class="item"><div>Cornet Américain 1 boule</div><div class="price">1000f</div></div>
            <div class="item"><div>Cornet Américain 2 boules</div><div class="price">1500f</div></div>
            <div class="item"><div>Wafles bowls 1 boule</div><div class="price">2000f</div></div>
            <div class="item"><div>Wafles bowls 2 boules</div><div class="price">2500f</div></div>
          </div>

          <div class="actions">
            <a class="btn" href="https://wa.me/22384124748" target="_blank" rel="noreferrer">Commander sur WhatsApp</a>
            <a class="btn secondary" href="#boissons">Voir Boissons</a>
          </div>
        </div>

        <aside class="hero-panel" style="background-image:url('assets/glace.jpg');" aria-hidden="true">
          <div class="hero-title">
            <h1>Glaces</h1>
            <p>Frais et colorés — parfait pour se rafraîchir.</p>
          </div>
        </aside>
      </div>
    </section>

    <!-- ============================
         BOISSONS (Mocktails)
         Background image: assets/cocktails.jpg
         ============================ -->
    <section id="boissons" class="panel" style="background-image: url('assets/cocktails.jpg');" aria-label="Boissons">
      <div class="panel-inner">
        <div class="menu-card" aria-labelledby="boissons-title">
          <h2 id="boissons-title">Mocktails</h2>
          <p>Boissons sans alcool, fruitées et rafraîchissantes.</p>

          <div class="menu-section">
            <div class="item"><div>Ener Cherry's</div><div class="price">2000f</div></div>
            <div class="item"><div>Virginie Colada</div><div class="price">3000f</div></div>
            <div class="item"><div>Virginie Mojito</div><div class="price">3000f</div></div>
            <div class="item"><div>Bora Bora</div><div class="price">3000f</div></div>
            <div class="item"><div>San Francisco</div><div class="price">3000f</div></div>
          </div>

          <div class="actions">
            <a class="btn" href="https://wa.me/22384124748" target="_blank" rel="noreferrer">Commander sur WhatsApp</a>
            <a class="btn secondary" href="#cafe">Voir Café & Thé</a>
          </div>
        </div>

        <aside class="hero-panel" style="background-image:url('assets/cocktails.jpg');" aria-hidden="true">
          <div class="hero-title">
            <h1>Mocktails</h1>
            <p>Cocktails sans alcool, parfaits pour tous.</p>
          </div>
        </aside>
      </div>
    </section>

    <!-- ============================
         CAFE & THE (page séparée)
         Background image: assets/cafe.jpg (ou cocktails.jpg si tu préfères)
         ============================ -->
    <section id="cafe" class="panel" style="background-image: url('assets/cafe.jpg');" aria-label="Café et Thé">
      <div class="panel-inner">
        <div class="menu-card" aria-labelledby="cafe-title">
          <h2 id="cafe-title">Café & Thé</h2>
          <p>Un bon café et des thés soigneusement préparés.</p>

          <div class="menu-section">
            <div class="item"><div>Nespresso</div><div class="price">1500f</div></div>
            <div class="item"><div>Cappuccino</div><div class="price">2000f</div></div>
            <div class="item"><div>Frappuccino glacé</div><div class="price">2500f</div></div>
          </div>

          <h3 style="margin-top:12px;color:#333">Thés</h3>
          <div class="menu-section">
            <div class="item"><div>Thé mixte</div><div class="price">1500f</div></div>
            <div class="item"><div>Thé Cherry's</div><div class="price">1500f</div></div>
            <div class="item"><div>Thé malien</div><div class="price">1000f</div></div>
          </div>

          <div class="actions">
            <a class="btn" href="https://wa.me/22384124748" target="_blank" rel="noreferrer">Commander sur WhatsApp</a>
            <a class="btn secondary" href="#merci">Merci</a>
          </div>
        </div>

        <aside class="hero-panel" style="background-image:url('assets/cafe.jpg');" aria-hidden="true">
          <div class="hero-title">
            <h1>Café & Thé</h1>
            <p>Une pause chaude ou glacée selon ton envie.</p>
          </div>
        </aside>
      </div>
    </section>

    <!-- ============================
         REMERCIEMENTS
         Logo en fond : assets/logo.png
         ============================ -->
    <section id="merci" class="panel" style="background-color:#fffaf6;min-height:60vh;display:flex;align-items:center;justify-content:center;">
      <div style="position:relative;max-width:900px;margin:0 18px;border-radius:12px;padding:28px;background:rgba(255,255,255,0.95);box-shadow:0 10px 40px rgba(0,0,0,0.06);text-align:center">
        <div style="position:absolute;inset:0;opacity:0.06;background-image:url('assets/logo.png');background-position:center;background-repeat:no-repeat;background-size:40vmin;border-radius:12px;pointer-events:none"></div>
        <div style="position:relative;z-index:2">
          <h1 style="color:var(--accent);margin-top:0">Merci pour votre visite</h1>
          <p style="color:#333;font-size:18px">Merci pour votre visite et votre confiance. <strong>Cherry’s Bakery & Ice Cream — le goût du bonheur !</strong></p>
          <div style="margin-top:18px">
            <a class="btn" href="https://wa.me/22384124748" target="_blank" rel="noreferrer">Commander sur WhatsApp</a>
            <a class="btn secondary" href="#fastfood">Retour au menu</a>
          </div>
        </div>
      </div>
    </section>

  </main>

  <footer class="site-foot" role="contentinfo">
    © Cherry's Bakery & Ice Cream — Le goût du bonheur
  </footer>

  <!-- WhatsApp floating button -->
  <a class="whatsapp" href="https://wa.me/22384124748" target="_blank" rel="noreferrer" aria-label="Commander sur WhatsApp">
    📲 Commander sur WhatsApp
    <small>+223 84 12 47 48</small>
  </a>

  <!-- ============================
       SCRIPT: Active nav highlight + smooth offset for fixed header
       ============================ -->
  <script>
    (function(){
      const headerHeight = document.querySelector('.site-header').offsetHeight || 88;
      // Smooth anchor offset: when clicking nav links, scroll a little above target
      document.querySelectorAll('a[href^="#"]').forEach(a=>{
        a.addEventListener('click', e=>{
          const href = a.getAttribute('href');
          if(!href.startsWith('#') || href === '#') return;
          e.preventDefault();
          const target = document.querySelector(href);
          if(!target) return;
          const top = target.getBoundingClientRect().top + window.scrollY - headerHeight - 8;
          window.scrollTo({top, behavior:'smooth'});
        });
      });

      // Active link on scroll
      const sections = Array.from(document.querySelectorAll('section[id]'));
      const navLinks = Array.from(document.querySelectorAll('nav.topnav a'));

      function setActive(){
        const y = window.scrollY + headerHeight + 20;
        let current = sections[0];
        for(const s of sections){
          if(s.offsetTop <= y) current = s;
        }
        navLinks.forEach(a => a.classList.toggle('active', a.getAttribute('href') === '#' + current.id));
      }

      window.addEventListener('scroll', setActive, {passive:true});
      window.addEventListener('resize', setActive);
      setActive();
    })();
  </script>
</body>
</html>
