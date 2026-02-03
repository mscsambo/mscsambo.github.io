<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Digital Learning - Offers</title>

  <style>
    :root{
      --bg:#f5f7fb;
      --card:#ffffff;
      --text:#111827;
      --muted:#6b7280;
      --border:#e5e7eb;
      --primary:#0b5ed7;
      --primary-2:#567ece;
      --radius:16px;
      --shadow: 0 10px 30px rgba(17,24,39,.08);
    }

    *{ box-sizing:border-box; }
    body{
      margin:0;
      font-family: system-ui, -apple-system, Segoe UI, Roboto, Arial, Helvetica, sans-serif;
      background:var(--bg);
      color:var(--text);
      line-height:1.5;
    }

    a{ color:inherit; text-decoration:none; }
    img{ max-width:100%; display:block; }

    /* Layout */
    .wrapper{
      max-width: 1100px;
      margin: 0 auto;
      padding: 24px 14px 60px;
    }

    /* Header */
    .topbar{
      background: linear-gradient(135deg, var(--primary), #0a4fb5);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding: 22px 22px;
      color: #fff;
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:16px;
      flex-wrap:wrap;
    }
    .brand{
      display:flex;
      flex-direction:column;
      gap:6px;
      min-width: 220px;
    }
    .brand h1{
      margin:0;
      font-size: 28px;
      line-height:1.1;
      letter-spacing:-.5px;
      font-weight: 900;
    }
    .brand p{
      margin:0;
      opacity:.92;
      font-size: 14px;
    }
    .contact{
      text-align:right;
      display:flex;
      flex-direction:column;
      gap:6px;
    }
    .contact small{
      opacity:.92;
      font-size:12px;
    }
    .contact strong{
      font-size: 14px;
      letter-spacing:.2px;
    }

    /* Hero */
    .hero{
      margin-top: 18px;
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding: 18px 18px;
      display:flex;
      justify-content:space-between;
      align-items:flex-start;
      gap:12px;
      flex-wrap:wrap;
    }
    .hero h2{
      margin:0;
      font-size: 18px;
      font-weight: 800;
    }
    .hero p{
      margin:8px 0 0;
      color: #374151;
      font-size: 14px;
      max-width: 720px;
    }

    /* Cards grid */
    .grid{
      margin-top: 16px;
      display:grid;
      grid-template-columns: repeat(12, 1fr);
      gap: 14px;
    }
    .card{
      grid-column: span 6;
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      overflow:hidden;
      display:flex;
      flex-direction:column;
    }
    .card-inner{
      padding: 16px 16px 14px;
      display:flex;
      gap: 14px;
      align-items:flex-start;
    }
    .logo{
      width: 52px;
      height: 52px;
      border-radius: 12px;
      overflow:hidden;
      border: 1px solid rgba(255,255,255,.2);
      flex: 0 0 52px;
      background:#fff;
      display:flex;
      align-items:center;
      justify-content:center;
    }
    .logo img{
      width: 100%;
      height: 100%;
      object-fit: contain;
      padding: 8px;
    }

    .info{
      flex: 1;
      min-width: 0;
    }
    .title{
      display:flex;
      justify-content:space-between;
      gap:10px;
      align-items:flex-start;
      flex-wrap:wrap;
    }
    .title h3{
      margin:0;
      font-size: 16px;
      font-weight: 800;
      line-height:1.25;
    }
    .desc{
      margin: 6px 0 0;
      color: #374151;
      font-size: 13px;
    }
    .bullets{
      margin: 10px 0 0;
      padding: 0;
      list-style:none;
      color: var(--muted);
      font-size: 12.5px;
    }
    .bullets li{
      margin: 4px 0;
      display:flex;
      gap:8px;
      align-items:flex-start;
    }
    .bullets li::before{
      content:"✓";
      color: var(--primary);
      font-weight:800;
      line-height:1.2;
      margin-top:1px;
    }

    .price{
      text-align:right;
      flex: 0 0 auto;
      min-width: 92px;
    }
    .price small{
      display:block;
      color: var(--muted);
      font-size: 12px;
    }
    .price .amount{
      margin-top: 6px;
      color: var(--primary);
      font-size: 20px;
      font-weight: 900;
      line-height: 1.1;
    }
    .price .per{
      margin-top: 6px;
      color: var(--muted);
      font-size: 12px;
    }

    .card-actions{
      margin-top:auto;
      padding: 0 16px 16px;
    }
    .btn{
      display:inline-flex;
      align-items:center;
      justify-content:center;
      gap:10px;
      padding: 10px 14px;
      border-radius: 12px;
      background: var(--primary);
      color:#fff;
      font-weight: 800;
      font-size: 13px;
      border: 1px solid rgba(255,255,255,.18);
      transition: transform .12s ease, box-shadow .12s ease, opacity .12s ease;
      width: 100%;
      text-align:center;
    }
    .btn:hover{
      transform: translateY(-1px);
      box-shadow: 0 12px 26px rgba(11,94,215,.22);
    }
    .btn:active{ transform: translateY(0px); opacity:.95; }

    /* Footer */
    footer{
      margin-top: 18px;
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding: 16px 16px;
    }
    .footer-topline{
      border-top: 3px solid var(--primary-2);
      padding-top: 12px;
      display:flex;
      justify-content:space-between;
      gap:12px;
      flex-wrap:wrap;
    }
    .footer-left{
      min-width: 240px;
    }
    .footer-left strong{
      display:block;
      font-size: 12px;
      margin-bottom: 6px;
    }
    .footer-left div{
      font-size: 12px;
      color: var(--muted);
      line-height: 1.7;
    }
    .footer-right a{
      display:inline-block;
      font-size: 12.5px;
      font-weight: 800;
      color: var(--primary);
      margin-left: 10px;
    }

    /* Responsive */
    @media (max-width: 900px){
      .card{ grid-column: span 12; }
      .price{ min-width: 86px; }
    }
    @media (max-width: 520px){
      .topbar{ padding: 18px 16px; }
      .brand h1{ font-size: 22px; }
      .contact{ text-align:left; }
      .card-inner{ padding: 14px 14px 12px; }
      .card-actions{ padding: 0 14px 14px; }
      .logo{ width: 48px; height: 48px; flex-basis:48px; }
    }
  </style>
</head>

<body>
  <div class="wrapper">

    <header class="topbar">
      <div class="brand">
        <h1>Digital Learning</h1>
        <p>Special offers available now</p>
      </div>

      <div class="contact">
        <small>Contact</small>
        <strong>+855 97 83 72 999</strong>
      </div>
    </header>

    <section class="hero">
      <div>
        <h2>Choose your plan</h2>
        <p>
          Below are the current premium offers from <strong>Digital Learning</strong>.
          Click an offer to order via Telegram.
        </p>
      </div>
    </section>

    <section class="grid">

      <!-- Offer 1: Coursera -->
      <article class="card">
        <div class="card-inner">
          <div class="logo">
            <img src="https://api.unified.to/docs/images/coursera.png" alt="Coursera">
          </div>

          <div class="info">
            <div class="title">
              <h3>Coursera Premium — 12 months</h3>
              <div class="price">
                <small>Offer</small>
                <div class="amount">$20</div>
                <div class="per">per year</div>
              </div>
            </div>

            <p class="desc">Build professional skills, certificates, and career insights.</p>

            <ul class="bullets">
              <li>Upgrade your own account (or ready-made for $12)</li>
              <li>Includes: Professional Certificates & Guided Projects</li>
              <li>Support: Full setup assistance</li>
            </ul>
          </div>
        </div>

        <div class="card-actions">
          <a class="btn" href="https://t.me/linktome1" target="_blank" rel="noopener">
            Get Coursera Premium
          </a>
        </div>
      </article>

      <!-- Offer 2: LinkedIn -->
      <article class="card">
        <div class="card-inner">
          <div class="logo">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/LinkedIn_logo_initials.png/120px-LinkedIn_logo_initials.png" alt="LinkedIn">
          </div>

          <div class="info">
            <div class="title">
              <h3>LinkedIn Career — 12 months</h3>
              <div class="price">
                <small>Offer</small>
                <div class="amount">$20</div>
                <div class="per">per year</div>
              </div>
            </div>

            <p class="desc">Stand out to recruiters and access 16,000+ LinkedIn Learning courses.</p>

            <ul class="bullets">
              <li>Upgrade your own personal account</li>
              <li>Includes: Who viewed your profile & InMail credits</li>
              <li>Support: Quick activation</li>
            </ul>
          </div>
        </div>

        <div class="card-actions">
          <a class="btn" href="https://t.me/linktome1" target="_blank" rel="noopener">
            Get LinkedIn Career
          </a>
        </div>
      </article>

      <!-- Offer 3: Office 365 -->
      <article class="card">
        <div class="card-inner">
          <div class="logo">
            <img src="https://static.vecteezy.com/system/resources/previews/014/018/579/large_2x/ms-365-logo-on-transparent-background-free-vector.jpg" alt="Microsoft 365">
          </div>

          <div class="info">
            <div class="title">
              <h3>Microsoft Office 365</h3>
              <div class="price">
                <small>Offer</small>
                <div class="amount">$5</div>
                <div class="per">per year</div>
              </div>
            </div>

            <p class="desc">Word, Excel, PowerPoint, and Outlook for productivity.</p>

            <ul class="bullets">
              <li>For: PC, Mac, and Mobile devices</li>
              <li>Includes: 1TB OneDrive cloud storage</li>
              <li>Support: Remote installation help</li>
            </ul>
          </div>
        </div>

        <div class="card-actions">
          <a class="btn" href="https://t.me/linktome1" target="_blank" rel="noopener">
            Get Office 365
          </a>
        </div>
      </article>

      <!-- Offer 4: Canva -->
      <article class="card">
        <div class="card-inner">
          <div class="logo">
            <img src="https://tse3.mm.bing.net/th/id/OIP.jutIWsGUNnw19ycDCx7MEgHaHa?w=1024&h=1024&rs=1&pid=ImgDetMain&o=7&rm=3" alt="Canva">
          </div>

          <div class="info">
            <div class="title">
              <h3>Canva Pro</h3>
              <div class="price">
                <small>Offer</small>
                <div class="amount">$3</div>
                <div class="per">per year</div>
              </div>
            </div>

            <p class="desc">Premium templates, Brand Kit, and AI Design tools.</p>

            <ul class="bullets">
              <li>Generate video and image by prompt (AI)</li>
              <li>Includes: Background remover & Premium assets</li>
              <li>Support: Instant account upgrade</li>
            </ul>
          </div>
        </div>

        <div class="card-actions">
          <a class="btn" href="https://t.me/linktome1" target="_blank" rel="noopener">
            Get Canva Pro
          </a>
        </div>
      </article>

    </section>

    <footer>
      <div class="footer-topline">
        <div class="footer-left">
          <strong>Digital Learning</strong>
          <div>
            Phnom Penh, Cambodia<br>
            Email: linkedinlearningservices@gmail.com<br>
            Phone: +855 97 83 72 999
          </div>
        </div>

        <div class="footer-right">
          <a href="https://t.me/learningadventure" target="_blank" rel="noopener">Telegram</a>
          <a href="https://web.facebook.com/sbtech01" target="_blank" rel="noopener">Facebook</a>
        </div>
      </div>
    </footer>

  </div>
</body>
</html>

