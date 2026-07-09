# Law-Firm-Website
<title> LawFirm Website | Aleitha Laws </title>
<style>
    :root {
      --font-sans: 'Inter', system-ui, -apple-system, sans-serif;
    }
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: var(--font-sans); background: #12131a; color: #eee; }
    .nav {
      display: flex; justify-content: space-between; align-items: center;
      padding: 16px 36px;
      background: #12131aee;
      border-bottom: 1px solid #c9a84c33;
      position: sticky; top: 0; z-index: 100;
    }
    .logo { display: flex; align-items: center; gap: 11px; }
    .logo-icon {
      width: 38px; height: 38px;
      background: linear-gradient(135deg, #c9a84c, #f0d878);
      border-radius: 6px; display: flex; align-items: center; justify-content: center;
      font-size: 18px; color: #12131a;
    }
    .logo-name { color: #fff; font-size: 17px; font-weight: 500; letter-spacing: 1px; }
    .logo-sub { color: #c9a84c; font-size: 9px; letter-spacing: 3px; text-transform: uppercase; }
    .nav-links { display: flex; gap: 24px; }
    .nav-links a { color: #aaa; font-size: 12px; text-decoration: none; cursor: pointer; transition: color 0.2s; }
    .nav-links a:hover { color: #c9a84c; }
    .nav-cta { background: transparent; border: 1px solid #c9a84c; color: #c9a84c; padding: 8px 18px; border-radius: 4px; font-size: 12px; cursor: pointer; transition: background 0.2s; }
    .nav-cta:hover { background: #c9a84c1a; }
    .hero {
      background: linear-gradient(135deg, #12131a 0%, #1a1b2e 40%, #0f1520 100%);
      padding: 70px 36px 60px; text-align: center;
      position: relative; overflow: hidden;
    }
    .hero::before {
      content: ''; position: absolute; top: -1px; left: 50%; transform: translateX(-50%);
      width: 500px; height: 1px; background: linear-gradient(90deg, transparent, #c9a84c88, transparent);
    }
    .hero::after {
      content: ''; position: absolute; top: 0; left: 0; right: 0; bottom: 0;
      background: radial-gradient(ellipse at 50% 0%, #c9a84c08 0%, transparent 65%);
      pointer-events: none;
    }
    .hero-badge {
      display: inline-block; border: 1px solid #c9a84c44; color: #c9a84c;
      font-size: 10px; letter-spacing: 3px; text-transform: uppercase;
      padding: 6px 16px; border-radius: 2px; margin-bottom: 26px;
    }
    .hero h1 { font-size: 46px; font-weight: 500; color: #fff; line-height: 1.1; margin-bottom: 16px; }
    .hero h1 .gold { color: #c9a84c; }
    .hero p { color: #7a7d9a; font-size: 15px; line-height: 1.7; max-width: 480px; margin: 0 auto 32px; }
    .hero-btns { display: flex; gap: 12px; justify-content: center; margin-bottom: 52px; }
    .btn-gold { background: #c9a84c; color: #12131a; border: none; padding: 12px 26px; border-radius: 4px; font-size: 13px; font-weight: 500; cursor: pointer; transition: opacity 0.2s; }
    .btn-gold:hover { opacity: 0.85; }
    .btn-outline { background: transparent; color: #eee; border: 1px solid #2a2d40; padding: 12px 26px; border-radius: 4px; font-size: 13px; cursor: pointer; transition: border-color 0.2s; }
    .btn-outline:hover { border-color: #c9a84c; }
    .stats { display: flex; justify-content: center; }
    .stat { padding: 18px 32px; text-align: center; border-right: 1px solid #2a2d40; background: #1a1b2e88; }
    .stat:last-child { border-right: none; }
    .stat:first-child { border-radius: 8px 0 0 8px; }
    .stat:last-child { border-radius: 0 8px 8px 0; }
    .stat-num { font-size: 26px; font-weight: 500; color: #c9a84c; }
    .stat-label { font-size: 10px; color: #555; letter-spacing: 1px; text-transform: uppercase; margin-top: 3px; }
    .section { padding: 64px 36px; }
    .sec-a { background: #0e0f18; }
    .sec-b { background: #12131a; }
    .sec-tag { font-size: 10px; letter-spacing: 3px; text-transform: uppercase; color: #c9a84c; margin-bottom: 10px; }
    .sec-title { font-size: 30px; font-weight: 500; color: #fff; margin-bottom: 10px; }
    .sec-sub { color: #555; font-size: 14px; line-height: 1.6; max-width: 440px; }
    .gold-line { width: 40px; height: 2px; background: #c9a84c; margin: 14px 0 36px; }
    /* LAYANAN */
    .svc-grid { display: grid; grid-template-columns: repeat(5, 1fr); gap: 1px; background: #1a1b2e; border: 1px solid #1a1b2e; border-radius: 8px; overflow: hidden; }
    .svc { background: #12131a; padding: 28px 20px; position: relative; }
    .svc::before { content:''; position:absolute; top:0; left:0; right:0; height:2px; background:#c9a84c; opacity:0; transition:opacity 0.2s; }
    .svc:hover { background: #16172a; }
    .svc:hover::before { opacity: 1; }
    .svc-icon { font-size: 26px; color: #c9a84c; margin-bottom: 14px; }
    .svc h3 { font-size: 13px; font-weight: 500; color: #fff; margin-bottom: 8px; }
    .svc p { font-size: 11px; color: #555; line-height: 1.6; }
    .team-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; }
    .tc {
      background: #12131a; border: 1px solid #1e2035; border-radius: 8px; overflow: hidden;
      transition: border-color 0.2s; cursor: pointer;
    }
    .tc:hover { border-color: #c9a84c44; }
    .tc-photo {
      height: 130px; position: relative; overflow: hidden;
      background: linear-gradient(135deg, #1a1b2e, #0e0f18);
      display: flex; align-items: center; justify-content: center;
    }
    .tc-photo img {
      width: 100%; height: 100%; object-fit: cover; object-position: center top;
      transition: transform 0.4s;
    }
    .tc:hover .tc-photo img { transform: scale(1.05); }
    .tc-photo .fallback {
      width: 64px; height: 64px; border-radius: 50%;
      background: linear-gradient(135deg, #c9a84c22, #c9a84c44);
      border: 1px solid #c9a84c44;
      display: flex; align-items: center; justify-content: center;
      font-size: 22px; font-weight: 500; color: #c9a84c;
    }
    .tc-overlay {
      position: absolute; bottom: 0; left: 0; right: 0; height: 40px;
      background: linear-gradient(transparent, #12131a);
    }
    .tc-body { padding: 14px 16px; }
    .tc-name { font-size: 13px; font-weight: 500; color: #fff; margin-bottom: 3px; }
    .tc-role { font-size: 9px; color: #c9a84c; letter-spacing: 2px; text-transform: uppercase; margin-bottom: 8px; }
    .tc-bio { font-size: 11px; color: #555; line-height: 1.5; }
    .contact-grid { display: grid; grid-template-columns: 1fr 1.3fr; gap: 48px; }
    .ci { display: flex; gap: 14px; margin-bottom: 22px; }
    .ci-icon { width: 38px; height: 38px; background: #c9a84c1a; border-radius: 6px; display: flex; align-items: center; justify-content: center; font-size: 17px; color: #c9a84c; flex-shrink: 0; }
    .ci-label { font-size: 10px; color: #555; letter-spacing: 2px; text-transform: uppercase; margin-bottom: 3px; }
    .ci-val { font-size: 13px; color: #bbb; }
    .form-box { background: #0e0f18; border: 1px solid #1e2035; border-radius: 10px; padding: 28px; }
    .form-row { margin-bottom: 14px; }
    .form-grid2 { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
    label { display: block; font-size: 10px; color: #666; letter-spacing: 1px; text-transform: uppercase; margin-bottom: 7px; }
    input, select, textarea {
      width: 100%; background: #12131a; border: 1px solid #1e2035; color: #eee;
      padding: 10px 12px; border-radius: 4px; font-size: 13px; font-family: var(--font-sans); outline: none;
      transition: border-color 0.2s;
    }
    input:focus, select:focus, textarea:focus { border-color: #c9a84c55; }
    textarea { min-height: 90px; resize: vertical; }
    .sub-btn {
      width: 100%; background: #c9a84c; color: #12131a; border: none; border-radius: 4px;
      padding: 13px; font-size: 13px; font-weight: 500; cursor: pointer; margin-top: 8px;
      transition: opacity 0.2s;
    }
    .sub-btn:hover { opacity: 0.85; }
    footer { background: #0a0b12; border-top: 1px solid #1e2035; padding: 24px 36px; display: flex; justify-content: space-between; align-items: center; }
    .fl { font-size: 15px; font-weight: 500; color: #fff; }
    .fl span { color: #c9a84c; }
    footer p { font-size: 11px; color: #333; }
    .sr-only {
      position: absolute; width: 1px; height: 1px;
      padding: 0; margin: -1px; overflow: hidden;
      clip: rect(0,0,0,0); white-space: nowrap; border: 0;
    }
    @media (max-width: 768px) {
      .svc-grid { grid-template-columns: repeat(2, 1fr); }
      .team-grid { grid-template-columns: repeat(2, 1fr); }
      .contact-grid { grid-template-columns: 1fr; }
      .stats { flex-wrap: wrap; }
      .stat { flex: 1 1 45%; }
      .hero h1 { font-size: 30px; }
    }
  </style>
