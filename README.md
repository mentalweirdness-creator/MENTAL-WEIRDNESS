<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Mental Weirdness — Streetwear</title>
  <meta name="description" content="Mental Weirdness — streetwear for the strange, mysterious, and off-center. Limited drops. Tees, hoodies, hats." />

  <!-- Optional: social preview (works best once you have a real URL and an OG image) -->
  <meta property="og:title" content="Mental Weirdness — Streetwear" />
  <meta property="og:description" content="Streetwear for the strange, mysterious, and off-center. Limited drops." />

  <style>
    :root{
      --bg:#050507;
      --card:rgba(18,18,24,.78);
      --text:#f4f4f6;
      --muted:#b8b8c6;
      --line:#232330;
      --accent:#8b5cf6;   /* purple */
      --accent2:#39ff88;  /* eerie neon */
      --shadow: 0 10px 30px rgba(0,0,0,.55);
      --radius: 18px;
      --max: 1100px;
      --pad: 18px;
      text-rendering: geometricPrecision;
    }

    *{ box-sizing:border-box; }
    html,body{ height:100%; }
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial;
      background:
        radial-gradient(900px 500px at 15% -10%, rgba(139,92,246,.28), transparent 55%),
        radial-gradient(900px 600px at 85% 10%, rgba(57,255,136,.10), transparent 55%),
        var(--bg);
      color:var(--text);
      line-height:1.4;
    }

    a{ color:inherit; text-decoration:none; }
    button, input, textarea{ font: inherit; }
    .container{ max-width:var(--max); margin:0 auto; padding:0 var(--pad); }

    header{
      position: sticky; top:0; z-index:50;
      background: rgba(5,5,7,.70);
      border-bottom: 1px solid rgba(35,35,48,.55);
      backdrop-filter: blur(12px);
    }
    .nav{
      display:flex; align-items:center; justify-content:space-between;
      padding: 14px 0;
      gap: 14px;
    }
    .brand{
      display:flex; align-items:center; gap:10px;
      font-weight:900; letter-spacing:.6px;
      text-transform: uppercase;
    }

    /* LOGO */
    .brand-logo{
      width:36px; height:36px;
      border-radius: 12px;
      background: rgba(255,255,255,.04);
      border: 1px solid rgba(255,255,255,.08);
      box-shadow: 0 10px 20px rgba(139,92,246,.20);
      display:flex; align-items:center; justify-content:center;
      overflow:hidden;
    }
    .brand-logo img{
      width: 82%;
      height: 82%;
      object-fit: contain;
      display:block;
      filter: drop-shadow(0 6px 12px rgba(0,0,0,.35));
    }

    .navlinks{
      display:flex; gap: 16px; align-items:center;
      flex-wrap: wrap;
      justify-content: flex-end;
    }
    .navlinks a{
      color: var(--muted);
      padding: 10px 12px;
      border-radius: 999px;
      transition: .2s ease;
    }
    .navlinks a:hover{ color: var(--text); background: rgba(255,255,255,.05); }

    .cta{
      display:inline-flex; gap:10px; align-items:center; justify-content:center;
      padding: 10px 14px;
      border-radius: 999px;
      border:1px solid rgba(139,92,246,.45);
      background: rgba(139,92,246,.18);
      color: var(--text);
      transition: .2s ease;
      cursor:pointer;
      font-weight: 800;
    }
    .cta:hover{ transform: translateY(-1px); background: rgba(139,92,246,.26); }
    .icon{ width:18px; height:18px; display:inline-block; }

    .pill{
      display:inline-flex; gap:10px; align-items:center;
      border:1px solid var(--line);
      background: rgba(18,18,24,.70);
      padding:10px 14px; border-radius:999px;
      backdrop-filter: blur(10px);
      box-shadow: var(--shadow);
    }
    .dot{ width:10px; height:10px; border-radius:50%; background: var(--accent2); box-shadow: 0 0 0 4px rgba(57,255,136,.12); }

    /* Hero */
    .hero{ padding: 44px 0 22px; }
    .hero-grid{
      display:grid;
      grid-template-columns: 1.15fr .85fr;
      gap: 18px;
      align-items: stretch;
    }
    .hero-card{
      border:1px solid rgba(35,35,48,.8);
      background: var(--card);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding: 22px;
      overflow:hidden;
      position: relative;
    }
    .hero-card::before{
      content:"";
      position:absolute; inset:-2px;
      background:
        radial-gradient(520px 260px at 20% 10%, rgba(139,92,246,.22), transparent 60%),
        radial-gradient(420px 220px at 75% 40%, rgba(57,255,136,.12), transparent 60%);
      pointer-events:none;
      opacity:.95;
    }
    .hero-card > *{ position:relative; }

    h1{
      margin: 14px 0 10px;
      font-size: clamp(34px, 4.6vw, 58px);
      line-height: 1.02;
      letter-spacing: -1px;
      text-transform: uppercase;
    }
    .sub{
      color: var(--muted);
      font-size: 16px;
      max-width: 60ch;
      margin: 0 0 18px;
    }

    .hero-actions{ display:flex; gap: 12px; flex-wrap: wrap; margin-top: 8px; }
    .btn{
      border:1px solid rgba(255,255,255,.10);
      background: rgba(255,255,255,.06);
      color: var(--text);
      padding: 12px 16px;
      border-radius: 14px;
      cursor:pointer;
      transition: .2s ease;
      display:inline-flex; gap:10px; align-items:center;
      font-weight: 800;
    }
    .btn:hover{ transform: translateY(-1px); background: rgba(255,255,255,.09); }
    .btn.primary{
      border-color: rgba(139,92,246,.55);
      background: rgba(139,92,246,.22);
    }
    .btn.primary:hover{ background: rgba(139,92,246,.30); }
    .btn.green{
      border-color: rgba(57,255,136,.40);
      background: rgba(57,255,136,.10);
    }
    .btn.green:hover{ background: rgba(57,255,136,.14); }

    .kpis{
      display:grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 10px;
      margin-top: 18px;
    }
    .kpi{
      border:1px solid rgba(255,255,255,.08);
      background: rgba(5,5,7,.35);
      border-radius: 14px;
      padding: 12px;
    }
    .kpi .big{ font-weight:900; font-size:18px; text-transform: uppercase; }
    .kpi .small{ color: var(--muted); font-size:12px; margin-top:4px; }

    /* Drop card image */
    .drop-card{ display:flex; flex-direction:column; justify-content:space-between; }
    .drop-img{
      border-radius: 16px;
      border:1px solid rgba(255,255,255,.08);
      background:
        linear-gradient(135deg, rgba(139,92,246,.18), rgba(57,255,136,.10)),
        url("https://images.unsplash.com/photo-1520975916090-3105956dac38?auto=format&fit=crop&w=1200&q=80");
      background-size: cover;
      background-position: center;
      height: 220px;
      box-shadow: 0 16px 34px rgba(0,0,0,.35);
      position: relative;
      overflow:hidden;
    }
    .drop-img::after{
      content:"";
      position:absolute; inset:0;
      background: radial-gradient(400px 250px at 30% 10%, rgba(57,255,136,.08), transparent 60%);
      mix-blend-mode: screen;
      opacity:.9;
    }
    .tag{
      display:inline-flex;
      padding: 8px 10px;
      border-radius: 999px;
      border:1px solid rgba(255,255,255,.10);
      background: rgba(255,255,255,.05);
      color: var(--muted);
      font-size: 12px;
      gap: 8px;
      align-items:center;
    }

    section{ padding: 24px 0; }
    .section-head{
      display:flex; align-items:flex-end; justify-content:space-between;
      gap: 12px; margin-bottom: 12px;
    }
    h2{ margin:0; font-size: 22px; letter-spacing: -.2px; text-transform: uppercase; }
    .section-head p{ margin:0; color: var(--muted); font-size: 14px; }

    .grid{
      display:grid;
      grid-template-columns: repeat(12, 1fr);
      gap: 12px;
    }
    .card{
      border:1px solid rgba(35,35,48,.85);
      background: var(--card);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding: 16px;
    }

    /* Products */
    .product{ grid-column: span 4; display:flex; flex-direction:column; gap: 10px; }
    .pimg{
      height: 180px;
      border-radius: 16px;
      border:1px solid rgba(255,255,255,.08);
      background: linear-gradient(135deg, rgba(255,255,255,.08), rgba(255,255,255,.02));
      overflow:hidden;
      position: relative;
    }
    .pimg img{ width:100%; height:100%; object-fit: cover; display:block; transform: scale(1.02); }
    .prow{ display:flex; align-items:flex-start; justify-content:space-between; gap:10px; }
    .pname{ font-weight:900; text-transform: uppercase; }
    .pprice{ color: var(--muted); font-weight:800; }
    .pdesc{ color: var(--muted); font-size: 13px; margin-top:-4px; }
    .buyrow{ display:flex; gap:10px; margin-top: 6px; }
    .qty{
      width: 70px;
      border-radius: 14px;
      border:1px solid rgba(255,255,255,.10);
      background: rgba(5,5,7,.45);
      color: var(--text);
      padding: 10px 12px;
      outline:none;
    }
    .add{
      flex:1;
      border-radius: 14px;
      border:1px solid rgba(255,255,255,.10);
      background: rgba(255,255,255,.06);
      color: var(--text);
      padding: 10px 12px;
      cursor:pointer;
      transition: .2s ease;
      font-weight: 900;
      text-transform: uppercase;
      letter-spacing: .4px;
    }
    .add:hover{ transform: translateY(-1px); background: rgba(255,255,255,.09); }
    .add.primary{
      border-color: rgba(139,92,246,.55);
      background: rgba(139,92,246,.22);
    }
    .add.primary:hover{ background: rgba(139,92,246,.30); }

    /* Lookbook + About */
    .look{ grid-column: span 7; }
    .about{ grid-column: span 5; }
    .masonry{ display:grid; grid-template-columns: repeat(2,1fr); gap: 10px; }
    .shot{ border-radius: 16px; overflow:hidden; border:1px solid rgba(255,255,255,.08); height: 160px; }
    .shot.tall{ height: 240px; grid-row: span 2; }
    .shot img{ width:100%; height:100%; object-fit: cover; display:block; }

    /* Forms */
    .formrow{ display:flex; gap:10px; flex-wrap: wrap; }
    .field{
      flex:1; min-width: 220px;
      border-radius: 14px;
      border:1px solid rgba(255,255,255,.10);
      background: rgba(5,5,7,.45);
      color: var(--text);
      padding: 12px 12px;
      outline:none;
    }
    textarea.field{ min-height: 120px; resize: vertical; }

    /* Footer */
    footer{
      border-top: 1px solid rgba(35,35,48,.8);
      padding: 22px 0 34px;
      color: var(--muted);
    }
    .footgrid{ display:flex; justify-content:space-between; align-items:flex-start; gap: 18px; flex-wrap:wrap; }
    .smalllinks{ display:flex; gap: 12px; flex-wrap:wrap; }
    .smalllinks a{ color: var(--muted); padding: 6px 10px; border-radius: 999px; }
    .smalllinks a:hover{ color: var(--text); background: rgba(255,255,255,.05); }

    /* Cart drawer */
    .drawer{
      position: fixed; inset: 0;
      background: rgba(0,0,0,.55);
      display:none; align-items: flex-end; justify-content: flex-end;
      z-index: 100;
    }
    .drawer.open{ display:flex; }
    .panel{
      width: min(440px, 100%);
      height: 100%;
      background: rgba(18,18,24,.96);
      border-left:1px solid rgba(35,35,48,.9);
      padding: 16px;
      backdrop-filter: blur(10px);
      display:flex; flex-direction:column; gap: 12px;
    }
    .panelhead{ display:flex; align-items:center; justify-content:space-between; gap:10px; }
    .close{
      border:1px solid rgba(255,255,255,.10);
      background: rgba(255,255,255,.06);
      color: var(--text);
      padding: 10px 12px;
      border-radius: 14px;
      cursor:pointer;
      font-weight: 900;
      text-transform: uppercase;
    }
    .cartlist{ display:flex; flex-direction:column; gap: 10px; overflow:auto; padding-right: 6px; }
    .cartitem{
      border:1px solid rgba(255,255,255,.08);
      background: rgba(5,5,7,.35);
      border-radius: 16px;
      padding: 12px;
      display:flex; gap: 10px;
      align-items:flex-start;
    }
    .thumb{
      width:64px; height:64px;
      border-radius: 14px;
      border:1px solid rgba(255,255,255,.08);
      overflow:hidden;
      flex: 0 0 auto;
    }
    .thumb img{ width:100%; height:100%; object-fit:cover; display:block; }
    .ci-main{ flex:1; }
    .ci-top{ display:flex; justify-content:space-between; gap:10px; }
    .ci-name{ font-weight: 900; text-transform: uppercase; }
    .ci-meta{ color: var(--muted); font-size: 13px; margin-top: 4px; }
    .remove{
      border:1px solid rgba(239,68,68,.35);
      background: rgba(239,68,68,.10);
      color: var(--text);
      padding: 8px 10px;
      border-radius: 14px;
      cursor:pointer;
      font-weight: 900;
      text-transform: uppercase;
    }
    .total{
      margin-top:auto;
      border-top:1px solid rgba(35,35,48,.9);
      padding-top: 12px;
      display:flex; flex-direction:column; gap: 10px;
    }
    .row{ display:flex; justify-content:space-between; align-items:center; gap:10px; }
    .checkout{
      width:100%;
      border-radius: 14px;
      border:1px solid rgba(57,255,136,.40);
      background: rgba(57,255,136,.12);
      color: var(--text);
      padding: 12px 14px;
      font-weight: 900;
      cursor:pointer;
      transition: .2s ease;
      text-transform: uppercase;
      letter-spacing: .4px;
    }
    .checkout:hover{ transform: translateY(-1px); background: rgba(57,255,136,.16); }

    @media (max-width: 900px){
      .hero-grid{ grid-template-columns: 1fr; }
      .product{ grid-column: span 6; }
      .look{ grid-column: span 12; }
      .about{ grid-column: span 12; }
    }
    @media (max-width: 560px){
      .product{ grid-column: span 12; }
      .kpis{ grid-template-columns: 1fr; }
      .navlinks{ display:none; }
    }
  </style>
</head>

<body>
  <header>
    <div class="container nav">
      <a class="brand" href="#top" aria-label="Go to top">
        <span class="brand-logo" aria-hidden="true">
          <img src="mw-logo.png" alt="" />
        </span>
        <span>Mental Weirdness</span>
      </a>

      <nav class="navlinks" aria-label="Primary">
        <a href="#drop">Drop</a>
        <a href="#shop">Shop</a>
        <a href="#lookbook">Lookbook</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </nav>

      <button class="cta" id="openCart" type="button" aria-label="Open cart">
        <svg class="icon" viewBox="0 0 24 24" fill="none" aria-hidden="true">
          <path d="M7 7h14l-2 8H8L7 7Z" stroke="currentColor" stroke-width="2" stroke-linejoin="round"/>
          <path d="M7 7 6 3H3" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
          <path d="M9 21a1 1 0 1 0 0-2 1 1 0 0 0 0 2Z" fill="currentColor"/>
          <path d="M18 21a1 1 0 1 0 0-2 1 1 0 0 0 0 2Z" fill="currentColor"/>
        </svg>
        <span>Cart</span>
        <span id="cartCount" style="color:var(--muted); font-weight:900;">0</span>
      </button>
    </div>
  </header>

  <main id="top">
    <div class="container hero">
      <div class="hero-grid">
        <div class="hero-card">
          <div class="pill">
            <span class="dot" aria-hidden="true"></span>
            <span style="color:var(--muted); font-weight:800; font-size:13px;">
              Limited drops • Strange essentials • Stay unseen
            </span>
          </div>

          <h1>MENTAL WEIRDNESS<br/>wear what lurks inside.</h1>
          <p class="sub">
            Streetwear for the strange, the quiet, and the unapologetically off-center.
            Limited quantities. Shadowy details. Clean fits.
          </p>

          <div class="hero-actions">
            <a class="btn primary" href="#shop">Shop the Drop <span aria-hidden="true">→</span></a>
            <a class="btn" href="#lookbook">View Lookbook <span aria-hidden="true">↗</span></a>
            <button class="btn green" type="button" id="joinBtn">Join Early Access <span aria-hidden="true">★</span></button>
          </div>

          <div class="kpis" aria-label="Highlights">
            <div class="kpi"><div class="big">Drop #01</div><div class="small">First release</div></div>
            <div class="kpi"><div class="big">Weird clean</div><div class="small">Mystery, not messy</div></div>
            <div class="kpi"><div class="big">Limited</div><div class="small">When it’s gone, it’s gone</div></div>
          </div>
        </div>

        <div class="hero-card drop-card" id="drop">
          <div>
            <div class="drop-img" role="img" aria-label="Lifestyle photo"></div>
            <div style="margin-top:14px;">
              <span class="tag">🕯️ <b style="color:var(--text)">NEW</b> <span style="color:var(--muted)">Drop live</span></span>
              <h2 style="margin:12px 0 6px;">THE UNKNOWN CAPSULE</h2>
              <p style="margin:0; color:var(--muted); font-size:14px;">
                Quiet chaos. Minimal color. Strange energy.
              </p>
            </div>
          </div>
          <div style="display:flex; gap:10px; margin-top: 14px;">
            <a class="btn primary" href="#shop" style="flex:1; justify-content:center;">Shop now</a>
            <a class="btn" href="#contact" style="justify-content:center;">Collabs</a>
          </div>
        </div>
      </div>
    </div>

    <section id="shop">
      <div class="container">
        <div class="section-head">
          <div>
            <h2>Featured</h2>
            <p>Tees • Hoodies • Hats</p>
          </div>
          <div class="pill"><span style="font-weight:900;">Free ship</span><span style="color:var(--muted);">orders $75+</span></div>
        </div>

        <div class="grid">
          <!-- HOODIE -->
          <div class="card product" data-id="hoodie" data-name="Shadow Script Hoodie" data-price="68"
               data-img="https://images.unsplash.com/photo-1520975682031-a2efc40f6e98?auto=format&fit=crop&w=1200&q=80">
            <div class="pimg">
              <img alt="Shadow Script Hoodie" src="https://images.unsplash.com/photo-1520975682031-a2efc40f6e98?auto=format&fit=crop&w=1200&q=80" />
            </div>
            <div class="prow">
              <div>
                <div class="pname">Shadow Script Hoodie</div>
                <div class="pdesc">Heavyweight • soft inside • clean front</div>
              </div>
              <div class="pprice">$68</div>
            </div>
            <div class="buyrow">
              <input class="qty" type="number" min="1" value="1" aria-label="Quantity" />
              <button class="add primary" type="button">Add</button>
            </div>
          </div>

          <!-- TEE -->
          <div class="card product" data-id="tee" data-name="Mind Static Tee" data-price="34"
               data-img="https://images.unsplash.com/photo-1520975747935-52a6a5fca1cb?auto=format&fit=crop&w=1200&q=80">
            <div class="pimg">
              <img alt="Mind Static Tee" src="https://images.unsplash.com/photo-1520975747935-52a6a5fca1cb?auto=format&fit=crop&w=1200&q=80" />
            </div>
            <div class="prow">
              <div>
                <div class="pname">Mind Static Tee</div>
                <div class="pdesc">Relaxed fit • durable print</div>
              </div>
              <div class="pprice">$34</div>
            </div>
            <div class="buyrow">
              <input class="qty" type="number" min="1" value="1" aria-label="Quantity" />
              <button class="add" type="button">Add</button>
            </div>
          </div>

          <!-- HAT -->
          <div class="card product" data-id="hat" data-name="Odd Frequency Hat" data-price="28"
               data-img="https://images.unsplash.com/photo-1520975861904-cf1a9f3a6b44?auto=format&fit=crop&w=1200&q=80">
            <div class="pimg">
              <img alt="Odd Frequency Hat" src="https://images.unsplash.com/photo-1520975861904-cf1a9f3a6b44?auto=format&fit=crop&w=1200&q=80" />
            </div>
            <div class="prow">
              <div>
                <div class="pname">Odd Frequency Hat</div>
                <div class="pdesc">Adjustable • subtle embroidery</div>
              </div>
              <div class="pprice">$28</div>
            </div>
            <div class="buyrow">
              <input class="qty" type="number" min="1" value="1" aria-label="Quantity" />
              <button class="add" type="button">Add</button>
            </div>
          </div>
        </div>

        <div class="card" style="margin-top:12px;">
          <div class="section-head" style="margin-bottom:10px;">
            <div>
              <h2 style="font-size:18px;">Early Access</h2>
              <p>Drop alerts • restocks • secret links</p>
            </div>
          </div>
          <form class="formrow" id="newsletterForm">
            <input class="field" required type="email" name="email" placeholder="you@email.com" aria-label="Email address" />
            <button class="btn primary" type="submit">Join</button>
            <span id="newsletterMsg" style="color:var(--muted); font-size:13px; align-self:center;"></span>
          </form>
        </div>
      </div>
    </section>

    <section id="lookbook">
      <div class="container">
        <div class="section-head">
          <div>
            <h2>Lookbook</h2>
            <p>Swap these for your shoot photos.</p>
          </div>
        </div>

        <div class="grid">
          <div class="card look">
            <div class="masonry">
              <div class="shot tall">
                <img alt="Lookbook shot 1" src="https://images.unsplash.com/photo-1520975599306-1f2a1bc60d8a?auto=format&fit=crop&w=1200&q=80" />
              </div>
              <div class="shot">
                <img alt="Lookbook shot 2" src="https://images.unsplash.com/photo-1520975861904-cf1a9f3a6b44?auto=format&fit=crop&w=1200&q=80" />
              </div>
              <div class="shot">
                <img alt="Lookbook shot 3" src="https://images.unsplash.com/photo-1520975747935-52a6a5fca1cb?auto=format&fit=crop&w=1200&q=80" />
              </div>
            </div>
          </div>

          <div class="card about" id="about">
            <h2 style="margin-top:0;">About</h2>
            <p style="color:var(--muted); margin-top:8px;">
              Mental Weirdness is for people who don’t fit the template.
              Clean streetwear with a strange edge — quiet, eerie, and intentional.
            </p>

            <div style="margin-top:14px; display:flex; flex-direction:column; gap:10px;">
              <div class="pill"><span style="font-weight:900;">Code</span><span style="color:var(--muted);">weird • mysterious • clean</span></div>
              <div class="pill"><span style="font-weight:900;">Quality</span><span style="color:var(--muted);">premium blanks + durable prints</span></div>
              <div class="pill"><span style="font-weight:900;">Drops</span><span style="color:var(--muted);">limited by design</span></div>
            </div>

            <div style="margin-top:14px; display:flex; gap:10px; flex-wrap:wrap;">
              <a class="btn" href="#contact">Contact</a>
              <a class="btn primary" href="#shop">Shop</a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="contact">
      <div class="container">
        <div class="section-head">
          <div>
            <h2>Contact</h2>
            <p>Collabs • wholesale • support</p>
          </div>
        </div>

        <div class="grid">
          <div class="card" style="grid-column: span 7;">
            <form id="contactForm">
              <div class="formrow">
                <input class="field" required name="name" placeholder="Name" />
                <input class="field" required type="email" name="email" placeholder="Email" />
              </div>
              <div style="height:10px;"></div>
              <input class="field" name="subject" placeholder="Subject (optional)" />
              <div style="height:10px;"></div>
              <textarea class="field" required name="message" placeholder="Message"></textarea>
              <div style="height:10px;"></div>
              <button class="btn primary" type="submit">Send</button>
              <span id="contactMsg" style="color:var(--muted); font-size:13px; margin-left:10px;"></span>
            </form>
            <p style="color:var(--muted); font-size:12px; margin:12px 0 0;">
              Demo uses mailto. For a real inbox, connect Formspree / Netlify Forms / Shopify.
            </p>
          </div>

          <div class="card" style="grid-column: span 5;">
            <h2 style="margin-top:0;">Socials</h2>
            <p style="color:var(--muted); margin-top:8px;">
              Add your links:
            </p>
            <div class="smalllinks" style="margin-top:10px;">
              <a href="#" aria-label="Instagram link">Instagram</a>
              <a href="#" aria-label="TikTok link">TikTok</a>
              <a href="#" aria-label="X link">X</a>
            </div>

            <div class="card" style="margin-top:12px; background: rgba(5,5,7,.35); border-color: rgba(255,255,255,.08);">
              <div style="display:flex; justify-content:space-between; gap:10px; align-items:flex-start;">
                <div>
                  <div style="font-weight:900;">Support</div>
                  <div style="color:var(--muted); margin-top:4px; font-size:13px;">Reply within 24h</div>
                </div>
                <div class="tag">🕳️ <span style="color:var(--muted)">Stay weird</span></div>
              </div>
              <div style="margin-top:10px; color:var(--muted); font-size:13px;">
                Email: <a href="mailto:hello@mentalweirdness.com" style="color:var(--text); text-decoration:underline;">hello@mentalweirdness.com</a><br/>
                Location: Your City
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container footgrid">
      <div>
        <div style="display:flex; align-items:center; gap:10px;">
          <span class="brand-logo" aria-hidden="true" style="width:30px;height:30px;border-radius:10px;">
            <img src="mw-logo.png" alt="" />
          </span>
          <div style="font-weight:900; color:var(--text); text-transform:uppercase;">Mental Weirdness</div>
        </div>
        <div style="margin-top:10px; font-size:13px;">
          © <span id="year"></span> Mental Weirdness. All rights reserved.
        </div>
      </div>

      <div class="smalllinks" aria-label="Footer links">
        <a href="#shop">Shop</a>
        <a href="#lookbook">Lookbook</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </div>
    </div>
  </footer>

  <!-- Cart Drawer -->
  <div class="drawer" id="drawer" aria-hidden="true">
    <div class="panel" role="dialog" aria-modal="true" aria-label="Shopping cart">
      <div class="panelhead">
        <div style="display:flex; align-items:center; gap:10px;">
          <div style="font-weight:900; font-size:18px; text-transform:uppercase;">Cart</div>
          <span class="tag"><span style="color:var(--muted)">Demo cart</span></span>
        </div>
        <button class="close" id="closeCart" type="button">Close</button>
      </div>

      <div class="cartlist" id="cartList"></div>

      <div class="total">
        <div class="row">
          <div style="color:var(--muted); font-weight:800;">Subtotal</div>
          <div style="font-weight:900;" id="subtotal">$0.00</div>
        </div>
        <button class="checkout" type="button" id="checkoutBtn">Checkout (demo)</button>
        <div style="color:var(--muted); font-size:12px;">
          To take payments: Shopify / Stripe Checkout.
        </div>
      </div>
    </div>
  </div>

  <script>
    const $ = (sel, root=document) => root.querySelector(sel);
    const $$ = (sel, root=document) => Array.from(root.querySelectorAll(sel));
    const cart = new Map();

    function money(n){
      const v = Number(n || 0);
      return v.toLocaleString(undefined, { style: "currency", currency: "USD" });
    }
    function cartCount(){
      let c = 0;
      for (const item of cart.values()) c += item.qty;
      return c;
    }
    function cartSubtotal(){
      let t = 0;
      for (const item of cart.values()) t += item.price * item.qty;
      return t;
    }

    function renderCart(){
      const list = $("#cartList");
      list.innerHTML = "";

      if (cart.size === 0){
        list.innerHTML = `
          <div class="card" style="background: rgba(5,5,7,.35); border-color: rgba(255,255,255,.08);">
            <div style="font-weight:900; text-transform:uppercase;">Your cart is empty</div>
            <div style="color:var(--muted); margin-top:6px; font-size:13px;">Add an item to see it here.</div>
          </div>
        `;
      } else {
        for (const item of cart.values()){
          const el = document.createElement("div");
          el.className = "cartitem";
          el.innerHTML = `
            <div class="thumb"><img alt="${item.name}" src="${item.img}"></div>
            <div class="ci-main">
              <div class="ci-top">
                <div class="ci-name">${item.name}</div>
                <button class="remove" type="button" data-remove="${item.id}">Remove</button>
              </div>
              <div class="ci-meta">${money(item.price)} • Qty ${item.qty}</div>
            </div>
          `;
          list.appendChild(el);
        }
      }

      $("#cartCount").textContent = String(cartCount());
      $("#subtotal").textContent = money(cartSubtotal());

      $$("[data-remove]").forEach(btn => {
        btn.addEventListener("click", () => {
          const id = btn.getAttribute("data-remove");
          cart.delete(id);
          renderCart();
        });
      });
    }

    function openDrawer(){
      const d = $("#drawer");
      d.classList.add("open");
      d.setAttribute("aria-hidden", "false");
      renderCart();
    }
    function closeDrawer(){
      const d = $("#drawer");
      d.classList.remove("open");
      d.setAttribute("aria-hidden", "true");
    }

    $("#openCart").addEventListener("click", openDrawer);
    $("#closeCart").addEventListener("click", closeDrawer);
    $("#drawer").addEventListener("click", (e) => {
      if (e.target.id === "drawer") closeDrawer();
    });

    $$(".product").forEach(card => {
      const addBtn = $(".add", card);
      const qtyInput = $(".qty", card);

      addBtn.addEventListener("click", () => {
        const id = card.dataset.id;
        const name = card.dataset.name;
        const price = Number(card.dataset.price);
        const img = card.dataset.img;
        const qty = Math.max(1, Math.floor(Number(qtyInput.value || 1)));

        if (cart.has(id)) cart.get(id).qty += qty;
        else cart.set(id, { id, name, price, qty, img });

        qtyInput.value = 1;
        renderCart();
        openDrawer();
      });
    });

    $("#checkoutBtn").addEventListener("click", () => {
      alert("Demo checkout. Connect Shopify/Stripe to accept payments.");
    });

    $("#newsletterForm").addEventListener("submit", (e) => {
      e.preventDefault();
      $("#newsletterMsg").textContent = "You’re on the list (demo).";
      e.target.reset();
      setTimeout(()=> $("#newsletterMsg").textContent = "", 4000);
    });

    $("#contactForm").addEventListener("submit", (e) => {
      e.preventDefault();
      const fd = new FormData(e.target);
      const name = fd.get("name");
      const email = fd.get("email");
      const subject = fd.get("subject") || "Website inquiry";
      const message = fd.get("message");

      const body = encodeURIComponent(`Name: ${name}\nEmail: ${email}\n\n${message}`);
      const to = "hello@mentalweirdness.com"; // change to your real inbox
      window.location.href = `mailto:${to}?subject=${encodeURIComponent(subject)}&body=${body}`;

      $("#contactMsg").textContent = "Opening your email app…";
      setTimeout(()=> $("#contactMsg").textContent = "", 4000);
    });

    $("#joinBtn").addEventListener("click", () => {
      document.querySelector("#shop").scrollIntoView({ behavior: "smooth" });
      setTimeout(() => {
        const emailField = document.querySelector("#newsletterForm input[type=email]");
        if (emailField) emailField.focus();
      }, 350);
    });

    $("#year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
