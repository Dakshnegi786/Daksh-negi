<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Shortlist — A Field Guide to Things Worth Buying</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,500;0,9..144,600;1,9..144,400&family=IBM+Plex+Mono:wght@400;500&family=Public+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --paper:#EDE8DE;
    --paper-dim:#E3DDCF;
    --ink:#1F2A24;
    --ink-soft:#3C463F;
    --moss:#4B5D46;
    --teal:#235768;
    --gold:#C9A227;
    --line: rgba(31,42,36,0.18);
    --card: #F6F3EA;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--paper);
    color:var(--ink);
    font-family:'Public Sans', sans-serif;
    font-size:16px;
    line-height:1.55;
  }
  h1,h2,h3, .display{
    font-family:'Fraunces', serif;
    font-weight:600;
    letter-spacing:-0.01em;
    margin:0;
  }
  .mono{
    font-family:'IBM Plex Mono', monospace;
    letter-spacing:0.02em;
  }
  a{color:inherit;}
  img{max-width:100%;display:block;}

  @media (prefers-reduced-motion: reduce){
    *{animation:none !important; transition:none !important;}
  }

  /* ===== Texture layer ===== */
  .grain{
    position:fixed; inset:0; pointer-events:none; z-index:5;
    opacity:0.035; mix-blend-mode:multiply;
    background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='2' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
  }

  /* ===== Nav ===== */
  header{
    position:sticky; top:0; z-index:20;
    background:rgba(237,232,222,0.92);
    backdrop-filter:blur(6px);
    border-bottom:1px solid var(--line);
  }
  .nav-wrap{
    max-width:1180px; margin:0 auto; padding:18px 28px;
    display:flex; align-items:center; justify-content:space-between;
  }
  .brand{
    display:flex; align-items:baseline; gap:10px;
  }
  .brand-mark{
    font-family:'Fraunces', serif; font-weight:600; font-size:22px;
  }
  .brand-no{
    font-family:'IBM Plex Mono', monospace; font-size:11px; color:var(--moss);
  }
  nav.links{display:flex; gap:28px; font-size:14px;}
  nav.links a{
    text-decoration:none; color:var(--ink-soft); position:relative; padding-bottom:2px;
  }
  nav.links a::after{
    content:''; position:absolute; left:0; bottom:-2px; height:1px; width:0;
    background:var(--teal); transition:width 0.25s ease;
  }
  nav.links a:hover::after{width:100%;}
  .nav-links-mobile{display:none;}

  /* ===== Hero ===== */
  .hero{
    max-width:1180px; margin:0 auto; padding:96px 28px 80px;
    display:grid; grid-template-columns:1.3fr 0.9fr; gap:60px; align-items:end;
  }
  .eyebrow{
    font-family:'IBM Plex Mono', monospace; font-size:12px; letter-spacing:0.14em;
    text-transform:uppercase; color:var(--teal); display:flex; align-items:center; gap:10px;
  }
  .eyebrow::before{content:''; width:26px; height:1px; background:var(--teal);}
  .hero h1{
    font-size:clamp(42px, 6vw, 74px); line-height:1.02; margin-top:22px; max-width:11ch;
  }
  .hero h1 em{
    font-style:italic; color:var(--teal);
  }
  .hero-sub{
    margin-top:26px; font-size:18px; color:var(--ink-soft); max-width:46ch;
  }
  .hero-cta{
    margin-top:34px; display:flex; gap:16px; flex-wrap:wrap;
  }
  .btn{
    display:inline-flex; align-items:center; gap:10px;
    padding:13px 24px; border-radius:2px; font-size:14px; font-weight:500;
    text-decoration:none; border:1px solid var(--ink);
    transition:transform 0.2s ease, background 0.2s ease, color 0.2s ease;
    cursor:pointer;
  }
  .btn-primary{background:var(--ink); color:var(--paper);}
  .btn-primary:hover{background:var(--teal); border-color:var(--teal); transform:translateY(-2px);}
  .btn-ghost{background:transparent; color:var(--ink);}
  .btn-ghost:hover{background:var(--ink); color:var(--paper); transform:translateY(-2px);}

  .hero-panel{
    border:1px solid var(--line); background:var(--card); padding:26px;
    font-family:'IBM Plex Mono', monospace; font-size:13px; color:var(--ink-soft);
    position:relative;
  }
  .hero-panel::before{
    content:'FIG. 1 — METHOD'; position:absolute; top:-11px; left:20px;
    background:var(--paper); padding:0 8px; font-size:10px; letter-spacing:0.12em; color:var(--moss);
  }
  .hero-panel ol{margin:0; padding-left:18px;}
  .hero-panel li{margin-bottom:10px;}
  .hero-panel li::marker{color:var(--gold);}

  /* ===== Section shell ===== */
  section{max-width:1180px; margin:0 auto; padding:70px 28px;}
  .section-head{
    display:flex; justify-content:space-between; align-items:flex-end; gap:24px;
    border-bottom:1px solid var(--line); padding-bottom:22px; margin-bottom:44px;
    flex-wrap:wrap;
  }
  .section-head h2{font-size:clamp(30px,4vw,42px);}
  .section-head .cat-no{
    font-family:'IBM Plex Mono', monospace; font-size:13px; color:var(--moss);
  }
  .section-note{max-width:52ch; color:var(--ink-soft); font-size:15px; margin-top:10px;}

  /* ===== Category divider strip ===== */
  .strip{
    border-top:1px solid var(--line); border-bottom:1px solid var(--line);
    background:var(--paper-dim);
  }
  .strip-wrap{
    max-width:1180px; margin:0 auto; padding:16px 28px;
    display:flex; gap:32px; overflow-x:auto; font-family:'IBM Plex Mono', monospace;
    font-size:12px; color:var(--moss); letter-spacing:0.04em;
  }
  .strip-wrap span{white-space:nowrap;}

  /* ===== Specimen grid ===== */
  .grid{
    display:grid; grid-template-columns:repeat(3, 1fr); gap:22px;
  }
  .card{
    background:var(--card); border:1px solid var(--line);
    padding:22px; display:flex; flex-direction:column; gap:14px;
    position:relative; transition:box-shadow 0.25s ease, transform 0.25s ease;
  }
  .card:hover{transform:translateY(-4px); box-shadow:0 14px 28px -18px rgba(31,42,36,0.45);}
  .card-top{
    display:flex; justify-content:space-between; align-items:flex-start;
    font-family:'IBM Plex Mono', monospace; font-size:11px; color:var(--moss);
    border-bottom:1px dashed var(--line); padding-bottom:12px;
  }
  .card h3{font-size:20px; margin-top:2px;}
  .card p{font-size:14px; color:var(--ink-soft); margin:0; flex-grow:1;}
  .card-foot{
    display:flex; justify-content:space-between; align-items:center;
    border-top:1px dashed var(--line); padding-top:12px;
  }
  .price{font-family:'IBM Plex Mono', monospace; font-size:14px; color:var(--ink);}
  .stamp{
    font-family:'IBM Plex Mono', monospace; font-size:11px; letter-spacing:0.08em;
    text-transform:uppercase; padding:8px 14px; border:1px solid var(--ink);
    text-decoration:none; color:var(--ink); transition:all 0.2s ease;
  }
  .stamp:hover{background:var(--gold); border-color:var(--gold); color:var(--ink);}
  .tag{
    font-size:10px; text-transform:uppercase; letter-spacing:0.08em;
    background:rgba(75,93,70,0.12); color:var(--moss); padding:3px 8px; border-radius:2px;
  }

  /* ===== Method section ===== */
  .method{
    display:grid; grid-template-columns:repeat(3, 1fr); gap:30px;
  }
  .method-item{border-left:2px solid var(--teal); padding-left:20px;}
  .method-item .mono{font-size:12px; color:var(--teal);}
  .method-item h3{font-size:19px; margin:8px 0 8px;}
  .method-item p{font-size:14px; color:var(--ink-soft); margin:0;}

  /* ===== Newsletter ===== */
  .newsletter{
    background:var(--ink); color:var(--paper); border-radius:2px;
    padding:60px 48px; display:grid; grid-template-columns:1fr 1fr; gap:40px; align-items:center;
  }
  .newsletter h2{color:var(--paper); font-size:clamp(26px,3.4vw,36px); max-width:14ch;}
  .newsletter p{color:rgba(237,232,222,0.7); margin-top:12px; font-size:14px; max-width:40ch;}
  .form-row{display:flex; gap:10px; flex-wrap:wrap;}
  .form-row input{
    flex:1; min-width:180px; padding:14px 16px; border:1px solid rgba(237,232,222,0.35);
    background:transparent; color:var(--paper); font-family:'Public Sans', sans-serif; font-size:14px;
    border-radius:2px;
  }
  .form-row input::placeholder{color:rgba(237,232,222,0.5);}
  .form-row .btn-primary{background:var(--gold); border-color:var(--gold); color:var(--ink);}
  .form-row .btn-primary:hover{background:var(--paper); border-color:var(--paper);}
  .form-note{font-size:12px; color:rgba(237,232,222,0.5); margin-top:14px;}

  /* ===== Footer ===== */
  footer{
    border-top:1px solid var(--line); padding:48px 28px 40px;
  }
  .footer-wrap{
    max-width:1180px; margin:0 auto; display:flex; justify-content:space-between;
    flex-wrap:wrap; gap:24px; font-size:13px; color:var(--ink-soft);
  }
  .disclosure{
    max-width:640px; font-family:'IBM Plex Mono', monospace; font-size:11.5px;
    line-height:1.7; color:var(--moss);
  }

  /* ===== Reveal on scroll ===== */
  .reveal{opacity:0; transform:translateY(18px); transition:opacity 0.7s ease, transform 0.7s ease;}
  .reveal.in{opacity:1; transform:translateY(0);}

  /* ===== Responsive ===== */
  @media (max-width: 880px){
    .hero{grid-template-columns:1fr; gap:36px; padding-top:64px;}
    nav.links{display:none;}
    .grid{grid-template-columns:1fr 1fr;}
    .method{grid-template-columns:1fr;}
    .newsletter{grid-template-columns:1fr; padding:40px 26px;}
  }
  @media (max-width: 560px){
    .grid{grid-template-columns:1fr;}
    .section-head{flex-direction:column; align-items:flex-start;}
  }

  :focus-visible{outline:2px solid var(--teal); outline-offset:3px;}
</style>
</head>
<body>
<div class="grain"></div>

<header>
  <div class="nav-wrap">
    <div class="brand">
      <span class="brand-mark">The Shortlist</span>
      <span class="brand-no mono">No. 003</span>
    </div>
    <nav class="links">
      <a href="#fashion">Fashion</a>
      <a href="#beauty">Beauty</a>
      <a href="#electronics">Smart Home</a>
      <a href="#method">Our Method</a>
    </nav>
  </div>
</header>

<section class="hero">
  <div>
    <div class="eyebrow">A curated buying guide</div>
    <h1>Things worth<br><em>buying</em>, catalogued.</h1>
    <p class="hero-sub">We test, wear, and live with products across fashion, beauty, and smart home tech &mdash; then publish only the ones that earned a place on the shelf. No filler, no sponsored fluff.</p>
    <div class="hero-cta">
      <a href="#fashion" class="btn btn-primary">Browse the shortlist</a>
      <a href="#method" class="btn btn-ghost">How we choose</a>
    </div>
  </div>
  <div class="hero-panel">
    <ol>
      <li>Source candidates from real use, reader requests, and category research.</li>
      <li>Long-term test each entry &mdash; weeks, not unboxing videos.</li>
      <li>Publish only items we'd buy again at full price.</li>
    </ol>
  </div>
</section>

<div class="strip">
  <div class="strip-wrap">
    <span>VOL. 01 — FASHION &amp; APPAREL</span>
    <span>VOL. 02 — BEAUTY &amp; PERSONAL CARE</span>
    <span>VOL. 03 — ELECTRONICS &amp; SMART HOME</span>
    <span>UPDATED MONTHLY</span>
    <span>INDEPENDENTLY TESTED</span>
  </div>
</div>

<!-- FASHION -->
<section id="fashion">
  <div class="section-head reveal">
    <div>
      <span class="cat-no mono">VOL. 01</span>
      <h2>Fashion &amp; Apparel</h2>
      <p class="section-note">Foundational pieces that hold their shape, color, and stitching past the tenth wash.</p>
    </div>
  </div>
  <div class="grid">

    <div class="card reveal">
      <div class="card-top"><span>SPEC. 01–A</span><span class="tag">Outerwear</span></div>
      <h3>The Weekend Field Jacket</h3>
      <p>Waxed-cotton shell, brass hardware, and a cut that layers over knitwear without bulk. Three seasons in and the color's only softened.</p>
      <div class="card-foot">
        <span class="price">$168</span>
        <a href="#" class="stamp">View deal →</a>
      </div>
    </div>

    <div class="card reveal">
      <div class="card-top"><span>SPEC. 01–B</span><span class="tag">Denim</span></div>
      <h3>Raw Selvedge Straight Jean</h3>
      <p>Heavyweight 14oz denim that breaks in to your own wear pattern. Chain-stitched hem holds up better than any pair we've tried under $200.</p>
      <div class="card-foot">
        <span class="price">$128</span>
        <a href="#" class="stamp">View deal →</a>
      </div>
    </div>

    <div class="card reveal">
      <div class="card-top"><span>SPEC. 01–C</span><span class="tag">Footwear</span></div>
      <h3>Resoleable Leather Derby</h3>
      <p>A Goodyear-welted shoe built to be repaired, not replaced. Comfortable out of the box, sharp enough for the office.</p>
      <div class="card-foot">
        <span class="price">$210</span>
        <a href="#" class="stamp">View deal →</a>
      </div>
    </div>

  </div>
</section>

<!-- BEAUTY -->
<section id="beauty">
  <div class="section-head reveal">
    <div>
      <span class="cat-no mono">VOL. 02</span>
      <h2>Beauty &amp; Personal Care</h2>
      <p class="section-note">Formulas we've repurchased more than once &mdash; judged on ingredients, results, and how they feel day to day.</p>
    </div>
  </div>
  <div class="grid">

    <div class="card reveal">
      <div class="card-top"><span>SPEC. 02–A</span><span class="tag">Skincare</span></div>
      <h3>Barrier-Repair Night Cream</h3>
      <p>Ceramide-forward formula that calmed visible redness within a week for three of our four testers. Fragrance-free, non-greasy finish.</p>
      <div class="card-foot">
        <span class="price">$42</span>
        <a href="#" class="stamp">View deal →</a>
      </div>
    </div>

    <div class="card reveal">
      <div class="card-top"><span>SPEC. 02–B</span><span class="tag">Hair</span></div>
      <h3>Sulfate-Free Scalp Shampoo</h3>
      <p>A rare formula that actually reduces buildup without stripping color-treated hair. Clean, herbal scent that doesn't linger.</p>
      <div class="card-foot">
        <span class="price">$26</span>
        <a href="#" class="stamp">View deal →</a>
      </div>
    </div>

    <div class="card reveal">
      <div class="card-top"><span>SPEC. 02–C</span><span class="tag">Tools</span></div>
      <h3>Ceramic Cool-Air Styler</h3>
      <p>Cuts drying time nearly in half with noticeably less heat damage over a three-month test. Quiet enough to use early morning.</p>
      <div class="card-foot">
        <span class="price">$189</span>
        <a href="#" class="stamp">View deal →</a>
      </div>
    </div>

  </div>
</section>

<!-- ELECTRONICS -->
<section id="electronics">
  <div class="section-head reveal">
    <div>
      <span class="cat-no mono">VOL. 03</span>
      <h2>Electronics &amp; Smart Home</h2>
      <p class="section-note">Gadgets that quietly work every day, from the ones we've returned within a week.</p>
    </div>
  </div>
  <div class="grid">

    <div class="card reveal">
      <div class="card-top"><span>SPEC. 03–A</span><span class="tag">Lighting</span></div>
      <h3>Matter-Compatible Smart Bulbs</h3>
      <p>Works across ecosystems without a hub, holds its Wi-Fi connection reliably, and the app hasn't nagged us to sign up for anything.</p>
      <div class="card-foot">
        <span class="price">$59 <span class="mono" style="font-size:11px;">/ 4-pack</span></span>
        <a href="#" class="stamp">View deal →</a>
      </div>
    </div>

    <div class="card reveal">
      <div class="card-top"><span>SPEC. 03–B</span><span class="tag">Audio</span></div>
      <h3>Compact Wireless Speaker</h3>
      <p>Surprising low-end for its size, 14-hour battery in real use, and a physical volume dial instead of touch controls.</p>
      <div class="card-foot">
        <span class="price">$99</span>
        <a href="#" class="stamp">View deal →</a>
      </div>
    </div>

    <div class="card reveal">
      <div class="card-top"><span>SPEC. 03–C</span><span class="tag">Security</span></div>
      <h3>Local-Storage Video Doorbell</h3>
      <p>No mandatory subscription to view footage, clear night vision, and a two-year battery life we've verified ourselves.</p>
      <div class="card-foot">
        <span class="price">$149</span>
        <a href="#" class="stamp">View deal →</a>
      </div>
    </div>

  </div>
</section>

<!-- METHOD -->
<section id="method">
  <div class="section-head reveal">
    <div>
      <span class="cat-no mono">METHOD</span>
      <h2>How we choose</h2>
      <p class="section-note">Every listing on this site earns its place through the same three-step process.</p>
    </div>
  </div>
  <div class="method">
    <div class="method-item reveal">
      <div class="mono">STEP 01</div>
      <h3>We source broadly</h3>
      <p>Candidates come from reader requests, category research, and things our team already owns and uses.</p>
    </div>
    <div class="method-item reveal">
      <div class="mono">STEP 02</div>
      <h3>We live with it</h3>
      <p>No first-impression reviews. Everything is used for weeks before it's written about, and re-tested if a formula or model changes.</p>
    </div>
    <div class="method-item reveal">
      <div class="mono">STEP 03</div>
      <h3>We publish selectively</h3>
      <p>Most candidates don't make the cut. What's listed here is what we'd buy again at full price, ourselves.</p>
    </div>
  </div>
</section>

<section>
  <div class="newsletter reveal">
    <div>
      <h2>Get the next volume before it's public.</h2>
      <p>One email a month when we add or retire a listing. No daily deals spam, ever.</p>
    </div>
    <div>
      <form class="form-row" onsubmit="event.preventDefault(); this.querySelector('input').value=''; this.querySelector('.confirm').style.display='block';">
        <input type="email" required placeholder="you@email.com">
        <button type="submit" class="btn btn-primary">Subscribe</button>
      </form>
      <p class="form-note confirm" style="display:none;">Thanks — check your inbox to confirm.</p>
      <p class="form-note">Unsubscribe anytime. We never sell your email.</p>
    </div>
  </div>
</section>

<footer>
  <div class="footer-wrap">
    <div>
      <div class="brand-mark" style="font-size:18px;">The Shortlist</div>
      <p style="margin-top:8px; max-width:32ch;">A field guide to things worth buying, published monthly.</p>
    </div>
    <div class="disclosure">
      DISCLOSURE — This site participates in affiliate programs. When you buy through links marked "View deal," we may earn a commission at no additional cost to you. This never influences which products are listed or how they're described; unqualified items are excluded regardless of commission rate.
    </div>
  </div>
</footer>

<script>
  const io = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('in'); io.unobserve(e.target); } });
  }, {threshold:0.15});
  document.querySelectorAll('.reveal').forEach(el=>io.observe(el));
</script>

</body>
</html>
