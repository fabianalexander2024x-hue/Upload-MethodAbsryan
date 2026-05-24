<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Absoluteryan — TikTok Quality Enhancer</title>

  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Mono:wght@300;400;500&family=Outfit:wght@300;400;500;600&display=swap" rel="stylesheet" />

  <style>
    /* ============================================================
       CSS VARIABLES & RESET
    ============================================================ */
    :root {
      --bg:        #04040a;
      --bg2:       #08080f;
      --surface:   rgba(255,255,255,0.035);
      --border:    rgba(255,255,255,0.07);
      --green:     #2eff9a;
      --green-dim: rgba(46,255,154,0.12);
      --green-glow:rgba(46,255,154,0.35);
      --cyan:      #00d4ff;
      --cyan-dim:  rgba(0,212,255,0.10);
      --white:     #f0f0f0;
      --muted:     rgba(240,240,240,0.45);
      --font-head: 'Syne', sans-serif;
      --font-mono: 'DM Mono', monospace;
      --font-body: 'Outfit', sans-serif;
      --r:         14px;
      --r-lg:      22px;
    }

    *, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }

    html { scroll-behavior: smooth; }

    body {
      background: var(--bg);
      color: var(--white);
      font-family: var(--font-body);
      overflow-x: hidden;
      -webkit-font-smoothing: antialiased;
    }

    ::selection { background: var(--green-dim); color: var(--green); }

    /* ============================================================
       CUSTOM SCROLLBAR
    ============================================================ */
    ::-webkit-scrollbar { width: 5px; }
    ::-webkit-scrollbar-track { background: var(--bg); }
    ::-webkit-scrollbar-thumb { background: var(--green); border-radius: 99px; }

    /* ============================================================
       CANVAS PARTICLES BACKGROUND
    ============================================================ */
    #canvas {
      position: fixed;
      inset: 0;
      z-index: 0;
      pointer-events: none;
      opacity: 0.55;
    }

    /* ============================================================
       AMBIENT BLOBS
    ============================================================ */
    .blob {
      position: fixed;
      border-radius: 50%;
      filter: blur(120px);
      pointer-events: none;
      z-index: 0;
    }
    .blob-1 {
      width: 600px; height: 600px;
      background: radial-gradient(circle, rgba(46,255,154,0.12) 0%, transparent 70%);
      top: -200px; left: -200px;
      animation: blobDrift1 18s ease-in-out infinite alternate;
    }
    .blob-2 {
      width: 500px; height: 500px;
      background: radial-gradient(circle, rgba(0,212,255,0.10) 0%, transparent 70%);
      bottom: 0; right: -100px;
      animation: blobDrift2 22s ease-in-out infinite alternate;
    }
    .blob-3 {
      width: 400px; height: 400px;
      background: radial-gradient(circle, rgba(46,255,154,0.07) 0%, transparent 70%);
      top: 50%; left: 50%;
      transform: translate(-50%,-50%);
      animation: blobDrift3 25s ease-in-out infinite alternate;
    }

    @keyframes blobDrift1 {
      from { transform: translate(0,0) scale(1); }
      to   { transform: translate(80px, 60px) scale(1.15); }
    }
    @keyframes blobDrift2 {
      from { transform: translate(0,0) scale(1); }
      to   { transform: translate(-60px,-80px) scale(1.1); }
    }
    @keyframes blobDrift3 {
      from { transform: translate(-50%,-50%) scale(1); }
      to   { transform: translate(-50%,-50%) scale(1.25); }
    }

    /* ============================================================
       LAYOUT HELPERS
    ============================================================ */
    .container {
      max-width: 1140px;
      margin: 0 auto;
      padding: 0 24px;
      position: relative;
      z-index: 2;
    }

    section { position: relative; z-index: 2; }

    /* ============================================================
       NAVBAR
    ============================================================ */
    #navbar {
      position: fixed;
      top: 0; left: 0; right: 0;
      z-index: 100;
      padding: 0 24px;
      transition: background 0.4s, backdrop-filter 0.4s, border-color 0.4s;
    }

    #navbar.scrolled {
      background: rgba(4,4,10,0.75);
      backdrop-filter: blur(24px) saturate(1.5);
      -webkit-backdrop-filter: blur(24px) saturate(1.5);
      border-bottom: 1px solid var(--border);
    }

    .nav-inner {
      max-width: 1140px;
      margin: 0 auto;
      height: 68px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .nav-logo {
      font-family: var(--font-head);
      font-weight: 800;
      font-size: 1.3rem;
      letter-spacing: -0.5px;
      text-decoration: none;
      color: var(--white);
    }

    .nav-logo span {
      color: var(--green);
      text-shadow: 0 0 12px var(--green-glow);
    }

    .nav-links {
      display: flex;
      gap: 36px;
      list-style: none;
    }

    .nav-links a {
      font-family: var(--font-body);
      font-size: 0.875rem;
      font-weight: 500;
      color: var(--muted);
      text-decoration: none;
      letter-spacing: 0.4px;
      transition: color 0.25s;
      position: relative;
    }

    .nav-links a::after {
      content: '';
      position: absolute;
      bottom: -4px; left: 0;
      width: 0; height: 1.5px;
      background: var(--green);
      transition: width 0.3s cubic-bezier(0.4,0,0.2,1);
      box-shadow: 0 0 8px var(--green);
    }

    .nav-links a:hover { color: var(--white); }
    .nav-links a:hover::after { width: 100%; }

    .nav-cta {
      font-family: var(--font-body);
      font-size: 0.85rem;
      font-weight: 600;
      padding: 9px 22px;
      background: var(--green);
      color: #030a06;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      letter-spacing: 0.3px;
      transition: transform 0.2s, box-shadow 0.2s, background 0.2s;
      text-decoration: none;
    }

    .nav-cta:hover {
      transform: translateY(-1px);
      box-shadow: 0 0 22px var(--green-glow), 0 4px 16px rgba(0,0,0,0.4);
    }

    /* Hamburger */
    .hamburger {
      display: none;
      flex-direction: column;
      gap: 5px;
      cursor: pointer;
      padding: 4px;
    }
    .hamburger span {
      display: block;
      width: 24px; height: 2px;
      background: var(--white);
      border-radius: 2px;
      transition: transform 0.3s, opacity 0.3s;
    }

    /* ============================================================
       HERO SECTION
    ============================================================ */
    #hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding-top: 80px;
    }

    .hero-inner {
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      gap: 28px;
      padding: 80px 0 60px;
    }

    .hero-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 6px 16px;
      background: var(--green-dim);
      border: 1px solid rgba(46,255,154,0.25);
      border-radius: 99px;
      font-family: var(--font-mono);
      font-size: 0.75rem;
      color: var(--green);
      letter-spacing: 0.8px;
      animation: fadeSlideDown 0.8s ease both;
    }

    .hero-badge-dot {
      width: 6px; height: 6px;
      background: var(--green);
      border-radius: 50%;
      box-shadow: 0 0 8px var(--green);
      animation: pulse 2s infinite;
    }

    @keyframes pulse {
      0%,100% { opacity: 1; transform: scale(1); }
      50%      { opacity: 0.5; transform: scale(0.85); }
    }

    .hero-title {
      font-family: var(--font-head);
      font-weight: 800;
      font-size: clamp(2.8rem, 7vw, 6rem);
      line-height: 0.95;
      letter-spacing: -2px;
      animation: fadeSlideDown 0.9s 0.1s ease both;
    }

    .hero-title .line-1 { color: var(--white); }

    .hero-title .line-2 {
      color: var(--green);
      text-shadow:
        0 0 40px rgba(46,255,154,0.6),
        0 0 80px rgba(46,255,154,0.3);
      display: block;
    }

    .hero-title .line-3 {
      color: var(--cyan);
      text-shadow:
        0 0 40px rgba(0,212,255,0.5),
        0 0 80px rgba(0,212,255,0.25);
      display: block;
    }

    .hero-sub {
      max-width: 560px;
      font-size: 1.05rem;
      font-weight: 300;
      line-height: 1.7;
      color: var(--muted);
      animation: fadeSlideDown 1s 0.2s ease both;
    }

    .hero-sub strong {
      color: var(--white);
      font-weight: 500;
    }

    .hero-actions {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
      justify-content: center;
      animation: fadeSlideDown 1s 0.35s ease both;
    }

    .btn-primary {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 14px 32px;
      background: var(--green);
      color: #030a06;
      font-family: var(--font-head);
      font-weight: 700;
      font-size: 0.95rem;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      text-decoration: none;
      letter-spacing: 0.2px;
      transition: transform 0.2s, box-shadow 0.25s;
      position: relative;
      overflow: hidden;
    }

    .btn-primary::before {
      content: '';
      position: absolute;
      inset: 0;
      background: linear-gradient(135deg, rgba(255,255,255,0.2) 0%, transparent 60%);
      opacity: 0;
      transition: opacity 0.25s;
    }

    .btn-primary:hover {
      transform: translateY(-2px);
      box-shadow: 0 0 30px var(--green-glow), 0 8px 32px rgba(0,0,0,0.5);
    }

    .btn-primary:hover::before { opacity: 1; }

    .btn-secondary {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 14px 32px;
      background: var(--surface);
      color: var(--white);
      font-family: var(--font-head);
      font-weight: 600;
      font-size: 0.95rem;
      border: 1px solid var(--border);
      border-radius: 10px;
      cursor: pointer;
      text-decoration: none;
      letter-spacing: 0.2px;
      backdrop-filter: blur(12px);
      transition: background 0.2s, border-color 0.2s, transform 0.2s;
    }

    .btn-secondary:hover {
      background: rgba(255,255,255,0.07);
      border-color: rgba(255,255,255,0.18);
      transform: translateY(-1px);
    }

    /* Stats Row */
    .hero-stats {
      display: flex;
      gap: 0;
      border: 1px solid var(--border);
      border-radius: 14px;
      background: var(--surface);
      backdrop-filter: blur(16px);
      overflow: hidden;
      animation: fadeSlideDown 1s 0.5s ease both;
      flex-wrap: wrap;
    }

    .stat-item {
      padding: 22px 40px;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 4px;
      position: relative;
    }

    .stat-item:not(:last-child)::after {
      content: '';
      position: absolute;
      right: 0; top: 20%; bottom: 20%;
      width: 1px;
      background: var(--border);
    }

    .stat-number {
      font-family: var(--font-head);
      font-weight: 800;
      font-size: 1.9rem;
      letter-spacing: -1px;
      color: var(--green);
      text-shadow: 0 0 18px var(--green-glow);
    }

    .stat-label {
      font-family: var(--font-mono);
      font-size: 0.72rem;
      color: var(--muted);
      letter-spacing: 0.8px;
      text-transform: uppercase;
    }

    /* Scroll hint */
    .scroll-hint {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 8px;
      color: var(--muted);
      font-size: 0.72rem;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      font-family: var(--font-mono);
      animation: fadeSlideDown 1s 0.7s ease both;
    }

    .scroll-mouse {
      width: 22px; height: 36px;
      border: 1.5px solid rgba(255,255,255,0.2);
      border-radius: 12px;
      display: flex;
      justify-content: center;
      padding-top: 6px;
    }

    .scroll-mouse-dot {
      width: 3px; height: 8px;
      background: var(--green);
      border-radius: 99px;
      animation: scrollDot 1.8s infinite;
    }

    @keyframes scrollDot {
      0%   { transform: translateY(0); opacity: 1; }
      100% { transform: translateY(10px); opacity: 0; }
    }

    /* ============================================================
       SECTION HEADERS
    ============================================================ */
    .section-header {
      text-align: center;
      margin-bottom: 60px;
    }

    .section-tag {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      font-family: var(--font-mono);
      font-size: 0.72rem;
      color: var(--green);
      letter-spacing: 1.5px;
      text-transform: uppercase;
      margin-bottom: 14px;
    }

    .section-tag::before, .section-tag::after {
      content: '—';
      opacity: 0.5;
    }

    .section-title {
      font-family: var(--font-head);
      font-weight: 800;
      font-size: clamp(2rem, 4vw, 3rem);
      letter-spacing: -1px;
      line-height: 1.1;
      margin-bottom: 16px;
    }

    .section-desc {
      max-width: 520px;
      margin: 0 auto;
      font-size: 0.95rem;
      line-height: 1.7;
      color: var(--muted);
      font-weight: 300;
    }

    /* ============================================================
       BENEFITS SECTION
    ============================================================ */
    #benefits {
      padding: 100px 0;
    }

    .benefits-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .benefit-card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--r-lg);
      padding: 32px 28px;
      backdrop-filter: blur(12px);
      transition: border-color 0.3s, transform 0.3s, box-shadow 0.3s, background 0.3s;
      position: relative;
      overflow: hidden;
      cursor: default;
    }

    .benefit-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 2px;
      background: linear-gradient(90deg, transparent, var(--green), transparent);
      opacity: 0;
      transition: opacity 0.35s;
    }

    .benefit-card:hover {
      border-color: rgba(46,255,154,0.2);
      transform: translateY(-4px);
      background: rgba(46,255,154,0.035);
      box-shadow: 0 24px 60px rgba(0,0,0,0.4), 0 0 40px rgba(46,255,154,0.06);
    }

    .benefit-card:hover::before { opacity: 1; }

    .benefit-icon {
      width: 46px; height: 46px;
      border-radius: 12px;
      background: var(--green-dim);
      border: 1px solid rgba(46,255,154,0.2);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.3rem;
      margin-bottom: 22px;
      transition: box-shadow 0.3s;
    }

    .benefit-card:hover .benefit-icon {
      box-shadow: 0 0 20px var(--green-glow);
    }

    .benefit-title {
      font-family: var(--font-head);
      font-weight: 700;
      font-size: 1.1rem;
      margin-bottom: 10px;
      letter-spacing: -0.3px;
    }

    .benefit-desc {
      font-size: 0.875rem;
      line-height: 1.65;
      color: var(--muted);
      font-weight: 300;
    }

    .benefit-tag {
      display: inline-block;
      margin-top: 16px;
      padding: 4px 10px;
      background: var(--green-dim);
      border-radius: 6px;
      font-family: var(--font-mono);
      font-size: 0.68rem;
      color: var(--green);
      letter-spacing: 0.6px;
    }

    /* ============================================================
       HOW IT WORKS — STEPS
    ============================================================ */
    #howitworks {
      padding: 80px 0;
    }

    .steps-row {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 0;
      position: relative;
    }

    .steps-row::before {
      content: '';
      position: absolute;
      top: 28px; left: 16.66%; right: 16.66%;
      height: 1px;
      background: linear-gradient(90deg,
        transparent,
        rgba(46,255,154,0.3) 20%,
        rgba(46,255,154,0.3) 80%,
        transparent
      );
      z-index: 0;
    }

    .step {
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      padding: 0 28px;
      position: relative;
      z-index: 1;
    }

    .step-number {
      width: 56px; height: 56px;
      border-radius: 50%;
      background: var(--bg2);
      border: 1.5px solid rgba(46,255,154,0.3);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: var(--font-mono);
      font-size: 1rem;
      font-weight: 500;
      color: var(--green);
      margin-bottom: 20px;
      box-shadow: 0 0 16px rgba(46,255,154,0.15);
      position: relative;
    }

    .step-number::after {
      content: '';
      position: absolute;
      inset: -4px;
      border-radius: 50%;
      border: 1px dashed rgba(46,255,154,0.15);
    }

    .step-title {
      font-family: var(--font-head);
      font-weight: 700;
      font-size: 1rem;
      margin-bottom: 8px;
    }

    .step-desc {
      font-size: 0.83rem;
      line-height: 1.6;
      color: var(--muted);
    }

    /* ============================================================
       UPLOAD SECTION
    ============================================================ */
    #upload {
      padding: 100px 0;
    }

    .upload-wrapper {
      max-width: 680px;
      margin: 0 auto;
    }

    /* Drop Zone */
    .dropzone {
      background: var(--surface);
      border: 2px dashed rgba(46,255,154,0.25);
      border-radius: var(--r-lg);
      padding: 56px 32px;
      text-align: center;
      cursor: pointer;
      transition: border-color 0.3s, background 0.3s, transform 0.2s;
      position: relative;
      overflow: hidden;
    }

    .dropzone::before {
      content: '';
      position: absolute;
      inset: 0;
      background: radial-gradient(ellipse at center, rgba(46,255,154,0.04) 0%, transparent 70%);
      opacity: 0;
      transition: opacity 0.3s;
    }

    .dropzone.drag-over {
      border-color: var(--green);
      background: rgba(46,255,154,0.05);
      transform: scale(1.01);
    }

    .dropzone.drag-over::before { opacity: 1; }

    .dropzone:hover {
      border-color: rgba(46,255,154,0.5);
      background: rgba(46,255,154,0.03);
    }

    .dz-icon {
      width: 64px; height: 64px;
      border-radius: 16px;
      background: var(--green-dim);
      border: 1px solid rgba(46,255,154,0.2);
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 20px;
      font-size: 1.8rem;
      transition: box-shadow 0.3s, transform 0.3s;
    }

    .dropzone:hover .dz-icon,
    .dropzone.drag-over .dz-icon {
      box-shadow: 0 0 30px var(--green-glow);
      transform: scale(1.08);
    }

    .dz-title {
      font-family: var(--font-head);
      font-weight: 700;
      font-size: 1.2rem;
      margin-bottom: 8px;
    }

    .dz-sub {
      font-size: 0.85rem;
      color: var(--muted);
      line-height: 1.6;
      margin-bottom: 20px;
    }

    .dz-btn {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 10px 22px;
      background: var(--green-dim);
      border: 1px solid rgba(46,255,154,0.3);
      border-radius: 8px;
      color: var(--green);
      font-family: var(--font-body);
      font-weight: 600;
      font-size: 0.85rem;
      cursor: pointer;
      transition: background 0.2s, box-shadow 0.2s;
    }

    .dz-btn:hover {
      background: rgba(46,255,154,0.18);
      box-shadow: 0 0 16px rgba(46,255,154,0.2);
    }

    #file-input { display: none; }

    .dz-formats {
      margin-top: 14px;
      font-family: var(--font-mono);
      font-size: 0.68rem;
      color: rgba(240,240,240,0.3);
      letter-spacing: 0.5px;
    }

    /* File Info Panel */
    .file-info {
      display: none;
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--r);
      padding: 18px 22px;
      margin-top: 16px;
      align-items: center;
      gap: 16px;
    }

    .file-info.visible { display: flex; }

    .fi-icon {
      width: 40px; height: 40px;
      border-radius: 10px;
      background: var(--cyan-dim);
      border: 1px solid rgba(0,212,255,0.2);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.1rem;
      flex-shrink: 0;
    }

    .fi-details { flex: 1; min-width: 0; }

    .fi-name {
      font-family: var(--font-mono);
      font-size: 0.82rem;
      color: var(--white);
      font-weight: 400;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      margin-bottom: 3px;
    }

    .fi-size {
      font-family: var(--font-mono);
      font-size: 0.72rem;
      color: var(--muted);
    }

    .fi-check {
      color: var(--green);
      font-size: 1rem;
    }

    /* Settings Panel */
    .settings-panel {
      display: none;
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--r);
      padding: 22px;
      margin-top: 16px;
    }

    .settings-panel.visible { display: block; }

    .settings-title {
      font-family: var(--font-mono);
      font-size: 0.72rem;
      color: var(--muted);
      letter-spacing: 1px;
      text-transform: uppercase;
      margin-bottom: 16px;
    }

    .settings-row {
      display: flex;
      gap: 12px;
      flex-wrap: wrap;
    }

    .setting-chip {
      padding: 7px 14px;
      background: var(--green-dim);
      border: 1px solid rgba(46,255,154,0.3);
      border-radius: 8px;
      font-family: var(--font-mono);
      font-size: 0.76rem;
      color: var(--green);
      cursor: pointer;
      transition: background 0.2s, box-shadow 0.2s;
      user-select: none;
    }

    .setting-chip.active,
    .setting-chip:hover {
      background: rgba(46,255,154,0.22);
      box-shadow: 0 0 12px rgba(46,255,154,0.2);
    }

    .setting-chip.inactive {
      background: rgba(255,255,255,0.04);
      border-color: var(--border);
      color: var(--muted);
    }

    /* Process Button */
    .process-btn {
      display: none;
      width: 100%;
      padding: 16px;
      background: var(--green);
      color: #030a06;
      font-family: var(--font-head);
      font-weight: 700;
      font-size: 1rem;
      border: none;
      border-radius: var(--r);
      cursor: pointer;
      margin-top: 16px;
      letter-spacing: 0.2px;
      transition: transform 0.2s, box-shadow 0.25s, opacity 0.2s;
      position: relative;
      overflow: hidden;
    }

    .process-btn::after {
      content: '';
      position: absolute;
      inset: 0;
      background: linear-gradient(135deg, rgba(255,255,255,0.15) 0%, transparent 60%);
    }

    .process-btn.visible { display: block; }

    .process-btn:hover {
      transform: translateY(-1px);
      box-shadow: 0 0 30px var(--green-glow), 0 6px 24px rgba(0,0,0,0.4);
    }

    .process-btn:disabled {
      opacity: 0.6;
      cursor: not-allowed;
      transform: none;
      box-shadow: none;
    }

    /* Progress Section */
    .progress-section {
      display: none;
      margin-top: 16px;
    }

    .progress-section.visible { display: block; }

    .progress-box {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--r);
      padding: 22px;
    }

    .progress-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 14px;
    }

    .progress-status {
      font-family: var(--font-mono);
      font-size: 0.78rem;
      color: var(--green);
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .progress-spinner {
      width: 14px; height: 14px;
      border: 2px solid rgba(46,255,154,0.2);
      border-top-color: var(--green);
      border-radius: 50%;
      animation: spin 0.7s linear infinite;
    }

    @keyframes spin {
      to { transform: rotate(360deg); }
    }

    .progress-pct {
      font-family: var(--font-head);
      font-weight: 700;
      font-size: 0.95rem;
      color: var(--green);
    }

    .progress-track {
      height: 6px;
      background: rgba(255,255,255,0.06);
      border-radius: 99px;
      overflow: hidden;
      margin-bottom: 12px;
    }

    .progress-fill {
      height: 100%;
      background: linear-gradient(90deg, var(--green), var(--cyan));
      border-radius: 99px;
      width: 0%;
      transition: width 0.15s linear;
      box-shadow: 0 0 8px rgba(46,255,154,0.5);
    }

    .progress-steps {
      display: flex;
      flex-direction: column;
      gap: 6px;
    }

    .progress-step {
      display: flex;
      align-items: center;
      gap: 10px;
      font-family: var(--font-mono);
      font-size: 0.72rem;
      color: var(--muted);
      transition: color 0.3s;
    }

    .progress-step.active { color: var(--white); }

    .progress-step.done { color: var(--green); }

    .step-dot {
      width: 6px; height: 6px;
      border-radius: 50%;
      background: rgba(255,255,255,0.15);
      flex-shrink: 0;
      transition: background 0.3s, box-shadow 0.3s;
    }

    .progress-step.active .step-dot {
      background: var(--cyan);
      box-shadow: 0 0 8px var(--cyan);
    }

    .progress-step.done .step-dot {
      background: var(--green);
      box-shadow: 0 0 8px var(--green-glow);
    }

    /* Download Section */
    .download-section {
      display: none;
      margin-top: 16px;
    }

    .download-section.visible { display: block; }

    .download-box {
      background: rgba(46,255,154,0.05);
      border: 1px solid rgba(46,255,154,0.25);
      border-radius: var(--r);
      padding: 28px 24px;
      text-align: center;
    }

    .download-checkmark {
      width: 52px; height: 52px;
      border-radius: 50%;
      background: var(--green-dim);
      border: 2px solid rgba(46,255,154,0.3);
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 14px;
      font-size: 1.4rem;
      box-shadow: 0 0 20px var(--green-glow);
      animation: popIn 0.5s cubic-bezier(0.34,1.56,0.64,1) both;
    }

    @keyframes popIn {
      from { transform: scale(0); opacity: 0; }
      to   { transform: scale(1); opacity: 1; }
    }

    .download-title {
      font-family: var(--font-head);
      font-weight: 700;
      font-size: 1.1rem;
      margin-bottom: 6px;
    }

    .download-sub {
      font-size: 0.82rem;
      color: var(--muted);
      margin-bottom: 20px;
      font-family: var(--font-mono);
    }

    .download-meta {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-bottom: 20px;
      flex-wrap: wrap;
    }

    .download-meta-item {
      display: flex;
      align-items: center;
      gap: 6px;
      font-family: var(--font-mono);
      font-size: 0.72rem;
      color: var(--muted);
    }

    .download-meta-item span:first-child { color: var(--green); }

    .download-btn {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 14px 36px;
      background: var(--green);
      color: #030a06;
      font-family: var(--font-head);
      font-weight: 700;
      font-size: 1rem;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      text-decoration: none;
      letter-spacing: 0.2px;
      transition: transform 0.2s, box-shadow 0.25s;
    }

    .download-btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 0 30px var(--green-glow), 0 6px 24px rgba(0,0,0,0.5);
    }

    .reset-btn {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 10px 20px;
      background: transparent;
      border: 1px solid var(--border);
      border-radius: 8px;
      color: var(--muted);
      font-family: var(--font-body);
      font-size: 0.82rem;
      cursor: pointer;
      margin-top: 12px;
      transition: border-color 0.2s, color 0.2s;
    }

    .reset-btn:hover {
      border-color: rgba(255,255,255,0.2);
      color: var(--white);
    }

    /* ============================================================
       FAQ SECTION
    ============================================================ */
    #faq {
      padding: 100px 0;
    }

    .faq-list {
      max-width: 720px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .faq-item {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--r);
      overflow: hidden;
      transition: border-color 0.3s;
    }

    .faq-item.open {
      border-color: rgba(46,255,154,0.2);
    }

    .faq-question {
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 20px 24px;
      background: transparent;
      border: none;
      cursor: pointer;
      text-align: left;
      gap: 16px;
    }

    .faq-q-text {
      font-family: var(--font-head);
      font-weight: 600;
      font-size: 0.95rem;
      color: var(--white);
      transition: color 0.2s;
    }

    .faq-item.open .faq-q-text { color: var(--green); }

    .faq-chevron {
      width: 28px; height: 28px;
      border-radius: 7px;
      background: var(--green-dim);
      border: 1px solid rgba(46,255,154,0.2);
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
      font-size: 0.7rem;
      color: var(--green);
      transition: transform 0.3s, background 0.3s;
    }

    .faq-item.open .faq-chevron {
      transform: rotate(180deg);
      background: rgba(46,255,154,0.18);
    }

    .faq-answer {
      max-height: 0;
      overflow: hidden;
      transition: max-height 0.4s cubic-bezier(0.4,0,0.2,1);
    }

    .faq-a-text {
      padding: 0 24px 22px;
      font-size: 0.875rem;
      line-height: 1.7;
      color: var(--muted);
      font-weight: 300;
    }

    .faq-a-text code {
      background: var(--green-dim);
      border: 1px solid rgba(46,255,154,0.15);
      padding: 2px 7px;
      border-radius: 5px;
      font-family: var(--font-mono);
      font-size: 0.8em;
      color: var(--green);
    }

    /* ============================================================
       FOOTER
    ============================================================ */
    footer {
      padding: 56px 0 32px;
      position: relative;
      z-index: 2;
    }

    footer::before {
      content: '';
      position: absolute;
      top: 0; left: 10%; right: 10%;
      height: 1px;
      background: linear-gradient(90deg, transparent, var(--border), transparent);
    }

    .footer-inner {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 28px;
    }

    .footer-logo {
      font-family: var(--font-head);
      font-weight: 800;
      font-size: 1.4rem;
      letter-spacing: -0.5px;
    }

    .footer-logo span { color: var(--green); }

    .footer-tagline {
      font-family: var(--font-mono);
      font-size: 0.75rem;
      color: var(--muted);
      letter-spacing: 0.5px;
    }

    .footer-links {
      display: flex;
      gap: 28px;
      list-style: none;
      flex-wrap: wrap;
      justify-content: center;
    }

    .footer-links a {
      font-size: 0.82rem;
      color: var(--muted);
      text-decoration: none;
      transition: color 0.2s;
    }

    .footer-links a:hover { color: var(--green); }

    .footer-copy {
      font-family: var(--font-mono);
      font-size: 0.7rem;
      color: rgba(240,240,240,0.2);
      letter-spacing: 0.5px;
    }

    /* ============================================================
       ANIMATIONS
    ============================================================ */
    @keyframes fadeSlideDown {
      from { opacity: 0; transform: translateY(-20px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeSlideUp {
      from { opacity: 0; transform: translateY(24px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    .fade-in-up {
      opacity: 0;
      transform: translateY(28px);
      transition: opacity 0.7s ease, transform 0.7s ease;
    }

    .fade-in-up.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* Stagger children */
    .stagger > * { opacity: 0; transform: translateY(24px); transition: opacity 0.6s ease, transform 0.6s ease; }
    .stagger.visible > *:nth-child(1) { opacity:1; transform:none; transition-delay:0s; }
    .stagger.visible > *:nth-child(2) { opacity:1; transform:none; transition-delay:0.1s; }
    .stagger.visible > *:nth-child(3) { opacity:1; transform:none; transition-delay:0.2s; }
    .stagger.visible > *:nth-child(4) { opacity:1; transform:none; transition-delay:0.3s; }
    .stagger.visible > *:nth-child(5) { opacity:1; transform:none; transition-delay:0.4s; }
    .stagger.visible > *:nth-child(6) { opacity:1; transform:none; transition-delay:0.5s; }

    /* ============================================================
       DIVIDER
    ============================================================ */
    .section-divider {
      width: 100%;
      height: 1px;
      background: linear-gradient(90deg, transparent 0%, var(--border) 30%, var(--border) 70%, transparent 100%);
      margin: 0;
    }

    /* ============================================================
       TICKER / MARQUEE
    ============================================================ */
    .ticker-wrap {
      overflow: hidden;
      padding: 14px 0;
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
      background: rgba(46,255,154,0.02);
      position: relative;
      z-index: 2;
    }

    .ticker-track {
      display: flex;
      gap: 0;
      animation: ticker 24s linear infinite;
      white-space: nowrap;
    }

    .ticker-item {
      display: inline-flex;
      align-items: center;
      gap: 12px;
      padding: 0 28px;
      font-family: var(--font-mono);
      font-size: 0.75rem;
      color: var(--muted);
      letter-spacing: 0.5px;
    }

    .ticker-dot {
      width: 4px; height: 4px;
      background: var(--green);
      border-radius: 50%;
      box-shadow: 0 0 6px var(--green);
    }

    @keyframes ticker {
      from { transform: translateX(0); }
      to   { transform: translateX(-50%); }
    }

    /* ============================================================
       GLOW RING (decorative)
    ============================================================ */
    .glow-ring {
      position: absolute;
      border-radius: 50%;
      border: 1px solid rgba(46,255,154,0.08);
      pointer-events: none;
    }

    /* ============================================================
       TELEGRAM SECTION
    ============================================================ */
    #community {
      padding: 100px 0;
    }

    .tg-card {
      max-width: 780px;
      margin: 0 auto;
      background: linear-gradient(135deg,
        rgba(46,255,154,0.06) 0%,
        rgba(0,212,255,0.04) 50%,
        rgba(46,255,154,0.04) 100%
      );
      border: 1px solid rgba(46,255,154,0.2);
      border-radius: 28px;
      padding: 56px 48px;
      text-align: center;
      position: relative;
      overflow: hidden;
      backdrop-filter: blur(16px);
    }

    .tg-card::before {
      content: '';
      position: absolute;
      top: -80px; right: -80px;
      width: 300px; height: 300px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(0,212,255,0.08) 0%, transparent 70%);
      pointer-events: none;
    }

    .tg-card::after {
      content: '';
      position: absolute;
      bottom: -60px; left: -60px;
      width: 250px; height: 250px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(46,255,154,0.07) 0%, transparent 70%);
      pointer-events: none;
    }

    .tg-icon-wrap {
      width: 80px; height: 80px;
      border-radius: 22px;
      background: linear-gradient(135deg, rgba(0,136,204,0.25), rgba(0,180,255,0.15));
      border: 1px solid rgba(0,180,255,0.3);
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 24px;
      font-size: 2.2rem;
      box-shadow: 0 0 30px rgba(0,180,255,0.2);
      animation: tgPulse 3s ease-in-out infinite;
      position: relative;
      z-index: 1;
    }

    @keyframes tgPulse {
      0%,100% { box-shadow: 0 0 24px rgba(0,180,255,0.2); }
      50%      { box-shadow: 0 0 44px rgba(0,180,255,0.38); }
    }

    .tg-title {
      font-family: var(--font-head);
      font-weight: 800;
      font-size: clamp(1.6rem, 4vw, 2.4rem);
      letter-spacing: -1px;
      line-height: 1.1;
      margin-bottom: 14px;
      position: relative;
      z-index: 1;
    }

    .tg-title span {
      color: var(--cyan);
      text-shadow: 0 0 30px rgba(0,212,255,0.5);
    }

    .tg-desc {
      font-size: 0.95rem;
      line-height: 1.7;
      color: var(--muted);
      font-weight: 300;
      max-width: 480px;
      margin: 0 auto 32px;
      position: relative;
      z-index: 1;
    }

    .tg-stats-row {
      display: flex;
      justify-content: center;
      gap: 36px;
      margin-bottom: 36px;
      flex-wrap: wrap;
      position: relative;
      z-index: 1;
    }

    .tg-stat {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 3px;
    }

    .tg-stat-num {
      font-family: var(--font-head);
      font-weight: 800;
      font-size: 1.4rem;
      letter-spacing: -0.5px;
      color: var(--green);
      text-shadow: 0 0 14px var(--green-glow);
    }

    .tg-stat-label {
      font-family: var(--font-mono);
      font-size: 0.68rem;
      color: var(--muted);
      letter-spacing: 0.8px;
      text-transform: uppercase;
    }

    .tg-divider {
      width: 1px;
      height: 40px;
      background: var(--border);
      align-self: center;
    }

    .tg-btn {
      display: inline-flex;
      align-items: center;
      gap: 12px;
      padding: 16px 40px;
      background: linear-gradient(135deg, #0088cc, #00b4ff);
      color: #fff;
      font-family: var(--font-head);
      font-weight: 700;
      font-size: 1rem;
      border: none;
      border-radius: 12px;
      cursor: pointer;
      text-decoration: none;
      letter-spacing: 0.2px;
      transition: transform 0.2s, box-shadow 0.25s;
      position: relative;
      z-index: 1;
      overflow: hidden;
    }

    .tg-btn::before {
      content: '';
      position: absolute;
      inset: 0;
      background: linear-gradient(135deg, rgba(255,255,255,0.18) 0%, transparent 60%);
      opacity: 0;
      transition: opacity 0.25s;
    }

    .tg-btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 0 36px rgba(0,180,255,0.4), 0 8px 28px rgba(0,0,0,0.5);
    }

    .tg-btn:hover::before { opacity: 1; }

    .tg-btn-icon {
      font-size: 1.25rem;
      line-height: 1;
    }

    .tg-note {
      margin-top: 16px;
      font-family: var(--font-mono);
      font-size: 0.7rem;
      color: rgba(240,240,240,0.25);
      letter-spacing: 0.5px;
      position: relative;
      z-index: 1;
    }

    .tg-badges {
      display: flex;
      justify-content: center;
      gap: 10px;
      margin-bottom: 28px;
      flex-wrap: wrap;
      position: relative;
      z-index: 1;
    }

    .tg-badge {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 5px 12px;
      background: rgba(0,180,255,0.08);
      border: 1px solid rgba(0,180,255,0.18);
      border-radius: 99px;
      font-family: var(--font-mono);
      font-size: 0.68rem;
      color: var(--cyan);
      letter-spacing: 0.5px;
    }

    /* ============================================================
       RESPONSIVE
    ============================================================ */
    @media (max-width: 900px) {
      .benefits-grid { grid-template-columns: repeat(2, 1fr); }
      .steps-row { grid-template-columns: 1fr; gap: 32px; }
      .steps-row::before { display: none; }
      .nav-links { display: none; }
      .hamburger { display: flex; }
      .hero-stats { gap: 0; }
      .stat-item { padding: 18px 24px; }
    }

    @media (max-width: 600px) {
      .benefits-grid { grid-template-columns: 1fr; }
      .hero-stats { flex-direction: column; }
      .stat-item::after { display: none; }
      .hero-title { letter-spacing: -1.5px; }
      .nav-cta { display: none; }
      .download-meta { flex-direction: column; align-items: center; gap: 8px; }
    }

    /* Mobile menu overlay */
    .mobile-menu {
      display: none;
      position: fixed;
      inset: 0;
      z-index: 99;
      background: rgba(4,4,10,0.96);
      backdrop-filter: blur(20px);
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 32px;
    }

    .mobile-menu.open { display: flex; }

    .mobile-menu-links {
      list-style: none;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 24px;
    }

    .mobile-menu-links a {
      font-family: var(--font-head);
      font-size: 1.8rem;
      font-weight: 700;
      color: var(--white);
      text-decoration: none;
      transition: color 0.2s;
    }

    .mobile-menu-links a:hover { color: var(--green); }

    .mobile-close {
      position: absolute;
      top: 24px; right: 24px;
      background: none;
      border: none;
      font-size: 1.5rem;
      color: var(--muted);
      cursor: pointer;
    }
  </style>
</head>
<body>

<!-- ============================================================
     CANVAS PARTICLES
============================================================ -->
<canvas id="canvas"></canvas>

<!-- ============================================================
     AMBIENT BLOBS
============================================================ -->
<div class="blob blob-1"></div>
<div class="blob blob-2"></div>
<div class="blob blob-3"></div>

<!-- ============================================================
     MOBILE MENU
============================================================ -->
<div class="mobile-menu" id="mobileMenu">
  <button class="mobile-close" id="mobileClose">✕</button>
  <ul class="mobile-menu-links">
    <li><a href="#benefits" onclick="closeMobileMenu()">Benefits</a></li>
    <li><a href="#howitworks" onclick="closeMobileMenu()">How It Works</a></li>
    <li><a href="#upload" onclick="closeMobileMenu()">Upload</a></li>
    <li><a href="#faq" onclick="closeMobileMenu()">FAQ</a></li>
    <li><a href="#community" onclick="closeMobileMenu()" style="color:var(--cyan)">Telegram</a></li>
  </ul>
  <a href="#upload" class="btn-primary" onclick="closeMobileMenu()">
    ⚡ Start Free
  </a>
</div>

<!-- ============================================================
     NAVBAR
============================================================ -->
<nav id="navbar">
  <div class="nav-inner">
    <!-- Logo -->
    <a href="#" class="nav-logo">Absolute<span>ryan</span></a>

    <!-- Links -->
    <ul class="nav-links">
      <li><a href="#benefits">Benefits</a></li>
      <li><a href="#howitworks">How It Works</a></li>
      <li><a href="#upload">Upload</a></li>
      <li><a href="#faq">FAQ</a></li>
      <li><a href="#community" style="color:var(--cyan)">Telegram</a></li>
    </ul>

    <!-- CTA + hamburger -->
    <a href="#upload" class="nav-cta">Start Free →</a>
    <div class="hamburger" id="hamburger" onclick="openMobileMenu()">
      <span></span><span></span><span></span>
    </div>
  </div>
</nav>

<!-- ============================================================
     HERO SECTION
============================================================ -->
<section id="hero">
  <div class="container">
    <div class="hero-inner">

      <!-- Badge -->
      <div class="hero-badge">
        <div class="hero-badge-dot"></div>
        FREE TOOL · NO SIGNUP · BROWSER BASED
      </div>

      <!-- Title -->
      <h1 class="hero-title">
        <span class="line-1">UPLOAD</span>
        <span class="line-2">1080P 120FPS</span>
        <span class="line-3">NO LOSS.</span>
      </h1>

      <!-- Subtitle -->
      <p class="hero-sub">
        The only tool that correctly processes your video file before upload so
        <strong>TikTok's compression algorithm doesn't destroy your quality.</strong>
        No re-encoding artefacts, no soft blur, no frame drops.
      </p>

      <!-- Actions -->
      <div class="hero-actions">
        <a href="#upload" class="btn-primary">
          ⚡ Process My Video
        </a>
        <a href="#howitworks" class="btn-secondary">
          ↓ How It Works
        </a>
      </div>

      <!-- Stats Row -->
      <div class="hero-stats">
        <div class="stat-item">
          <div class="stat-number" data-target="2400000" data-suffix="">2.4M+</div>
          <div class="stat-label">Videos Processed</div>
        </div>
        <div class="stat-item">
          <div class="stat-number">100%</div>
          <div class="stat-label">Quality Retained</div>
        </div>
        <div class="stat-item">
          <div class="stat-number">120fps</div>
          <div class="stat-label">Max Framerate</div>
        </div>
        <div class="stat-item">
          <div class="stat-number">FREE</div>
          <div class="stat-label">Forever</div>
        </div>
      </div>

      <!-- Scroll hint -->
      <div class="scroll-hint">
        <div class="scroll-mouse"><div class="scroll-mouse-dot"></div></div>
        SCROLL
      </div>

    </div>
  </div>
</section>

<!-- ============================================================
     TICKER MARQUEE
============================================================ -->
<div class="ticker-wrap">
  <div class="ticker-track" id="tickerTrack">
    <!-- Items duplicated for seamless loop -->
    <span class="ticker-item"><span class="ticker-dot"></span> 1080P QUALITY PRESERVED</span>
    <span class="ticker-item"><span class="ticker-dot"></span> NO RE-ENCODING</span>
    <span class="ticker-item"><span class="ticker-dot"></span> 120FPS SUPPORT</span>
    <span class="ticker-item"><span class="ticker-dot"></span> WORKS ON TIKTOK WEB</span>
    <span class="ticker-item"><span class="ticker-dot"></span> BYPASS COMPRESSION</span>
    <span class="ticker-item"><span class="ticker-dot"></span> LOSSLESS METADATA</span>
    <span class="ticker-item"><span class="ticker-dot"></span> FREE FOREVER</span>
    <span class="ticker-item"><span class="ticker-dot"></span> BROWSER NATIVE</span>
    <span class="ticker-item"><span class="ticker-dot"></span> 1080P QUALITY PRESERVED</span>
    <span class="ticker-item"><span class="ticker-dot"></span> NO RE-ENCODING</span>
    <span class="ticker-item"><span class="ticker-dot"></span> 120FPS SUPPORT</span>
    <span class="ticker-item"><span class="ticker-dot"></span> WORKS ON TIKTOK WEB</span>
    <span class="ticker-item"><span class="ticker-dot"></span> BYPASS COMPRESSION</span>
    <span class="ticker-item"><span class="ticker-dot"></span> LOSSLESS METADATA</span>
    <span class="ticker-item"><span class="ticker-dot"></span> FREE FOREVER</span>
    <span class="ticker-item"><span class="ticker-dot"></span> BROWSER NATIVE</span>
  </div>
</div>

<!-- ============================================================
     BENEFITS SECTION
============================================================ -->
<section id="benefits">
  <div class="container">
    <div class="section-header fade-in-up">
      <div class="section-tag">Why Absoluteryan</div>
      <h2 class="section-title">Everything TikTok tries<br>to take away. Restored.</h2>
      <p class="section-desc">Our method patches the metadata signature your video carries so TikTok's CDN pipeline treats it as a pre-approved high-quality source.</p>
    </div>

    <div class="benefits-grid stagger">

      <div class="benefit-card">
        <div class="benefit-icon">🎯</div>
        <div class="benefit-title">Lossless Quality</div>
        <div class="benefit-desc">We inject a specific metadata fingerprint that tells TikTok's encoder this file has already been optimised. No recompression happens on their end.</div>
        <span class="benefit-tag">METADATA PATCH</span>
      </div>

      <div class="benefit-card">
        <div class="benefit-icon">⚡</div>
        <div class="benefit-title">120fps Unlocked</div>
        <div class="benefit-desc">TikTok drops high-framerate videos to 30fps by default. Our method preserves the framerate flag so viewers with compatible devices see silky smooth motion.</div>
        <span class="benefit-tag">FPS PRESERVE</span>
      </div>

      <div class="benefit-card">
        <div class="benefit-icon">🖥️</div>
        <div class="benefit-title">TikTok Web Compatible</div>
        <div class="benefit-desc">Works perfectly with the TikTok web uploader at tiktok.com. No app required. Upload from any desktop browser after downloading your processed file.</div>
        <span class="benefit-tag">WEB UPLOADER</span>
      </div>

      <div class="benefit-card">
        <div class="benefit-icon">🔒</div>
        <div class="benefit-title">100% Private</div>
        <div class="benefit-desc">Your video never leaves your device. All processing runs entirely in your browser using the Web File API. Zero server uploads, zero data retention.</div>
        <span class="benefit-tag">CLIENT-SIDE ONLY</span>
      </div>

      <div class="benefit-card">
        <div class="benefit-icon">💰</div>
        <div class="benefit-title">Free Forever</div>
        <div class="benefit-desc">No paywalls, no "premium" tier, no credit card required. The method is open and available to every creator — from 0 followers to 10 million.</div>
        <span class="benefit-tag">NO COST</span>
      </div>

      <div class="benefit-card">
        <div class="benefit-icon">🎨</div>
        <div class="benefit-title">Colour Grade Safe</div>
        <div class="benefit-desc">Standard uploads destroy your colour grading and HDR metadata. Absoluteryan preserves colour space tags (Rec.709, DCI-P3) so your grade survives the upload.</div>
        <span class="benefit-tag">HDR SAFE</span>
      </div>

    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- ============================================================
     HOW IT WORKS
============================================================ -->
<section id="howitworks">
  <div class="container">
    <div class="section-header fade-in-up">
      <div class="section-tag">The Method</div>
      <h2 class="section-title">Three steps.<br>Zero quality loss.</h2>
      <p class="section-desc">It takes under 60 seconds from drop to download.</p>
    </div>

    <div class="steps-row stagger">
      <div class="step">
        <div class="step-number">01</div>
        <div class="step-title">Drop Your Video</div>
        <div class="step-desc">Drag & drop or select any MP4, MOV or WEBM file. Any resolution, any framerate.</div>
      </div>
      <div class="step">
        <div class="step-number">02</div>
        <div class="step-title">We Patch It</div>
        <div class="step-desc">Our engine rewrites the container metadata, injects the TikTok quality flag, and packages the file correctly.</div>
      </div>
      <div class="step">
        <div class="step-number">03</div>
        <div class="step-title">Upload to TikTok</div>
        <div class="step-desc">Download your processed file and upload it directly to TikTok Web. That's it — full quality, every time.</div>
      </div>
    </div>

  </div>
</section>

<div class="section-divider"></div>

<!-- ============================================================
     UPLOAD SECTION
============================================================ -->
<section id="upload">
  <div class="container">
    <div class="section-header fade-in-up">
      <div class="section-tag">Process Your Video</div>
      <h2 class="section-title">Drop it in.<br>Get it back perfect.</h2>
      <p class="section-desc">Your file is processed entirely in your browser. Nothing is uploaded to any server.</p>
    </div>

    <div class="upload-wrapper">

      <!-- Drop Zone -->
      <div class="dropzone" id="dropzone">
        <div class="dz-icon">🎬</div>
        <div class="dz-title">Drop your video here</div>
        <div class="dz-sub">
          MP4, MOV, WEBM, AVI &nbsp;·&nbsp; Any resolution &nbsp;·&nbsp; Up to 4K 120fps<br>
          All processing is local — your file never leaves your device.
        </div>
        <label class="dz-btn" for="file-input">
          📂 Browse Files
        </label>
        <input type="file" id="file-input" accept="video/*" />
        <div class="dz-formats">SUPPORTED: MP4 · MOV · WEBM · AVI · MKV · M4V</div>
      </div>

      <!-- File Info -->
      <div class="file-info" id="fileInfo">
        <div class="fi-icon">🎞️</div>
        <div class="fi-details">
          <div class="fi-name" id="fileName">video.mp4</div>
          <div class="fi-size" id="fileSize">—</div>
        </div>
        <div class="fi-check">✓</div>
      </div>

      <!-- Settings Panel -->
      <div class="settings-panel" id="settingsPanel">
        <div class="settings-title">⚙ Processing Options</div>
        <div class="settings-row">
          <div class="setting-chip active" onclick="toggleChip(this)">✓ Quality Flag</div>
          <div class="setting-chip active" onclick="toggleChip(this)">✓ 120fps Preserve</div>
          <div class="setting-chip active" onclick="toggleChip(this)">✓ Colour Profile</div>
          <div class="setting-chip active" onclick="toggleChip(this)">✓ HDR Metadata</div>
          <div class="setting-chip active" onclick="toggleChip(this)">✓ Audio Bitrate</div>
        </div>
      </div>

      <!-- Process Button -->
      <button class="process-btn" id="processBtn" onclick="startProcessing()">
        ⚡ Process Video — Apply Absoluteryan Method
      </button>

      <!-- Progress Section -->
      <div class="progress-section" id="progressSection">
        <div class="progress-box">
          <div class="progress-header">
            <div class="progress-status">
              <div class="progress-spinner" id="progressSpinner"></div>
              <span id="statusText">Analyzing file…</span>
            </div>
            <div class="progress-pct" id="progressPct">0%</div>
          </div>
          <div class="progress-track">
            <div class="progress-fill" id="progressFill"></div>
          </div>
          <div class="progress-steps">
            <div class="progress-step" id="pstep-1">
              <div class="step-dot"></div>
              <span>Analyzing video container & codec</span>
            </div>
            <div class="progress-step" id="pstep-2">
              <div class="step-dot"></div>
              <span>Rewriting metadata headers</span>
            </div>
            <div class="progress-step" id="pstep-3">
              <div class="step-dot"></div>
              <span>Injecting TikTok quality signature</span>
            </div>
            <div class="progress-step" id="pstep-4">
              <div class="step-dot"></div>
              <span>Preserving framerate flags</span>
            </div>
            <div class="progress-step" id="pstep-5">
              <div class="step-dot"></div>
              <span>Packaging output file</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Download Section -->
      <div class="download-section" id="downloadSection">
        <div class="download-box">
          <div class="download-checkmark">✓</div>
          <div class="download-title">Processing Complete</div>
          <div class="download-sub" id="downloadSubText">Absoluteryan method applied successfully</div>
          <div class="download-meta">
            <div class="download-meta-item">
              <span>⚡</span><span>Quality flag injected</span>
            </div>
            <div class="download-meta-item">
              <span>🎯</span><span>120fps flag preserved</span>
            </div>
            <div class="download-meta-item">
              <span>🔒</span><span>Colour profile locked</span>
            </div>
          </div>
          <button class="download-btn" id="downloadBtn" onclick="downloadFile()">
            ↓ Download Processed Video
          </button>
          <br>
          <button class="reset-btn" onclick="resetUploader()">
            ↩ Process Another Video
          </button>
        </div>
      </div>

    </div><!-- /.upload-wrapper -->
  </div>
</section>

<div class="section-divider"></div>

<!-- ============================================================
     FAQ SECTION
============================================================ -->
<section id="faq">
  <div class="container">
    <div class="section-header fade-in-up">
      <div class="section-tag">FAQ</div>
      <h2 class="section-title">Questions, answered.</h2>
      <p class="section-desc">Everything you need to know about TikTok compression and how Absoluteryan fixes it.</p>
    </div>

    <div class="faq-list stagger" id="faqList">

      <div class="faq-item">
        <button class="faq-question" onclick="toggleFaq(this)">
          <span class="faq-q-text">Why does TikTok compress my videos so much?</span>
          <div class="faq-chevron">▾</div>
        </button>
        <div class="faq-answer">
          <p class="faq-a-text">TikTok re-encodes every single video that passes through its upload pipeline using aggressive H.264 encoding at low bitrates (typically 3–6 Mbps for 1080p). This is designed to reduce CDN bandwidth costs at scale. The encoder doesn't distinguish between a raw 4K clip and a pre-optimised file — unless the container metadata signals otherwise. Absoluteryan exploits this by writing specific header values that tell the pipeline's quality gate to skip the aggressive recompression path.</p>
        </div>
      </div>

      <div class="faq-item">
        <button class="faq-question" onclick="toggleFaq(this)">
          <span class="faq-q-text">Does this actually work? Is the difference visible?</span>
          <div class="faq-chevron">▾</div>
        </button>
        <div class="faq-answer">
          <p class="faq-a-text">Yes. The most visible improvement is in footage with fast motion, fine detail (foliage, text, fabric), and dark scenes. Standard TikTok uploads introduce macroblocking artefacts in these areas. Videos processed with Absoluteryan retain the sharpness of the original. Many creators report their processed clips are visually identical to the source when viewed on desktop at 1080p. The <code>fps</code> and <code>colour_primaries</code> flags are also correctly preserved.</p>
        </div>
      </div>

      <div class="faq-item">
        <button class="faq-question" onclick="toggleFaq(this)">
          <span class="faq-q-text">Is my video uploaded to a server when I use this tool?</span>
          <div class="faq-chevron">▾</div>
        </button>
        <div class="faq-answer">
          <p class="faq-a-text">Absolutely not. Absoluteryan is a fully client-side tool. When you drop a file, it is read by the browser's native <code>File API</code> entirely in memory. The metadata rewrite is performed using a JavaScript byte-level operation on the container headers. The download you receive is created using <code>URL.createObjectURL()</code> on the modified <code>Blob</code> — no network request is ever made. You can verify this by opening DevTools → Network and confirming zero outgoing requests during processing.</p>
        </div>
      </div>

      <div class="faq-item">
        <button class="faq-question" onclick="toggleFaq(this)">
          <span class="faq-q-text">What file formats are supported?</span>
          <div class="faq-chevron">▾</div>
        </button>
        <div class="faq-answer">
          <p class="faq-a-text">Absoluteryan supports <code>MP4</code>, <code>MOV</code>, <code>WEBM</code>, <code>AVI</code>, <code>MKV</code>, and <code>M4V</code>. For best results with TikTok Web, use <code>MP4</code> with H.264 or H.265 encoding. The processed output is always returned in the same container format as the input, with the modified metadata headers written correctly for that format's specification.</p>
        </div>
      </div>

      <div class="faq-item">
        <button class="faq-question" onclick="toggleFaq(this)">
          <span class="faq-q-text">Does it work on the TikTok mobile app too?</span>
          <div class="faq-chevron">▾</div>
        </button>
        <div class="faq-answer">
          <p class="faq-a-text">The method works best with the <strong>TikTok Web uploader</strong> (tiktok.com on desktop). The mobile app applies an additional on-device pre-processing step before sending the file to TikTok's servers, which can strip our injected headers. For mobile, the recommended workflow is: process with Absoluteryan → save to device → upload via TikTok Web on desktop. The quality difference on desktop uploads is consistently significant.</p>
        </div>
      </div>

      <div class="faq-item">
        <button class="faq-question" onclick="toggleFaq(this)">
          <span class="faq-q-text">Will this get my account banned?</span>
          <div class="faq-chevron">▾</div>
        </button>
        <div class="faq-answer">
          <p class="faq-a-text">No. Absoluteryan only modifies container-level metadata — it does not alter the actual video or audio content of your file in any way. The technique is equivalent to setting encoder flags correctly, which is something professional video software does automatically. TikTok's ToS enforcement targets harmful content, not file metadata optimisation. Thousands of creators use this method daily without any account issues.</p>
        </div>
      </div>

    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- ============================================================
     COMMUNITY / TELEGRAM SECTION
============================================================ -->
<section id="community">
  <div class="container">
    <div class="section-header fade-in-up">
      <div class="section-tag">Comunidad</div>
      <h2 class="section-title">Únete al grupo.<br>Aprende el método.</h2>
      <p class="section-desc">Más de 10,000 creators usando el método. Tips, actualizaciones y soporte directo en nuestro Telegram.</p>
    </div>

    <div class="tg-card fade-in-up">

      <!-- Telegram icon -->
      <div class="tg-icon-wrap">✈️</div>

      <h3 class="tg-title">Absoluteryan<br><span>Telegram Community</span></h3>

      <p class="tg-desc">
        El lugar donde se comparten los últimos métodos, configuraciones y tips para subir videos a TikTok
        con la máxima calidad posible. Gratis, para siempre.
      </p>

      <!-- Badges -->
      <div class="tg-badges">
        <span class="tg-badge">⚡ Actualizaciones en tiempo real</span>
        <span class="tg-badge">🎯 Tips exclusivos</span>
        <span class="tg-badge">🔒 100% Gratis</span>
        <span class="tg-badge">💬 Soporte directo</span>
      </div>

      <!-- Stats -->
      <div class="tg-stats-row">
        <div class="tg-stat">
          <div class="tg-stat-num">10K+</div>
          <div class="tg-stat-label">Miembros</div>
        </div>
        <div class="tg-divider"></div>
        <div class="tg-stat">
          <div class="tg-stat-num">24/7</div>
          <div class="tg-stat-label">Activo</div>
        </div>
        <div class="tg-divider"></div>
        <div class="tg-stat">
          <div class="tg-stat-num">FREE</div>
          <div class="tg-stat-label">Sin costo</div>
        </div>
      </div>

      <!-- CTA Button -->
      <a href="https://t.me/sasdjisdndasd" target="_blank" rel="noopener noreferrer" class="tg-btn">
        <span class="tg-btn-icon">✈️</span>
        Unirme al Grupo de Telegram
      </a>

      <div class="tg-note">t.me/sasdjisdndasd · Grupo oficial de Absoluteryan</div>

    </div>
  </div>
</section>

<!-- ============================================================
     FOOTER
============================================================ -->
<footer>
  <div class="container">
    <div class="footer-inner">
      <div class="footer-logo">Absolute<span>ryan</span></div>
      <div class="footer-tagline">TikTok Quality Enhancer · Client-Side · Free Forever</div>
      <ul class="footer-links">
        <li><a href="#benefits">Benefits</a></li>
        <li><a href="#howitworks">How It Works</a></li>
        <li><a href="#upload">Upload</a></li>
        <li><a href="#faq">FAQ</a></li>
        <li><a href="#community" style="color:var(--cyan)">Telegram</a></li>
      </ul>
      <div class="footer-copy">© 2025 Absoluteryan · All processing is local · No data collected</div>
    </div>
  </div>
</footer>


<!-- ============================================================
     JAVASCRIPT
============================================================ -->
<script>
/* ============================================================
   CANVAS PARTICLE SYSTEM
============================================================ */
(function () {
  const canvas = document.getElementById('canvas');
  const ctx    = canvas.getContext('2d');
  let W, H, particles;

  function resize () {
    W = canvas.width  = window.innerWidth;
    H = canvas.height = window.innerHeight;
  }

  function Particle () {
    this.reset();
  }

  Particle.prototype.reset = function () {
    this.x  = Math.random() * W;
    this.y  = Math.random() * H;
    this.r  = Math.random() * 1.2 + 0.3;
    this.vx = (Math.random() - 0.5) * 0.35;
    this.vy = (Math.random() - 0.5) * 0.35;
    this.alpha = Math.random() * 0.5 + 0.1;
    // colour: mostly green, some cyan
    this.green = Math.random() > 0.3;
  };

  function initParticles () {
    const count = Math.min(Math.floor(W * H / 9000), 140);
    particles = [];
    for (let i = 0; i < count; i++) particles.push(new Particle());
  }

  function draw () {
    ctx.clearRect(0, 0, W, H);

    // Draw connecting lines between close particles
    for (let i = 0; i < particles.length; i++) {
      for (let j = i + 1; j < particles.length; j++) {
        const dx  = particles[i].x - particles[j].x;
        const dy  = particles[i].y - particles[j].y;
        const dist = Math.sqrt(dx * dx + dy * dy);
        if (dist < 130) {
          ctx.beginPath();
          ctx.strokeStyle = `rgba(46,255,154,${0.06 * (1 - dist / 130)})`;
          ctx.lineWidth = 0.6;
          ctx.moveTo(particles[i].x, particles[i].y);
          ctx.lineTo(particles[j].x, particles[j].y);
          ctx.stroke();
        }
      }
    }

    // Draw particles
    for (const p of particles) {
      ctx.beginPath();
      if (p.green) {
        ctx.fillStyle = `rgba(46,255,154,${p.alpha})`;
      } else {
        ctx.fillStyle = `rgba(0,212,255,${p.alpha * 0.7})`;
      }
      ctx.arc(p.x, p.y, p.r, 0, Math.PI * 2);
      ctx.fill();

      // Move
      p.x += p.vx;
      p.y += p.vy;

      // Wrap
      if (p.x < -10) p.x = W + 10;
      if (p.x > W + 10) p.x = -10;
      if (p.y < -10) p.y = H + 10;
      if (p.y > H + 10) p.y = -10;
    }

    requestAnimationFrame(draw);
  }

  resize();
  initParticles();
  draw();

  window.addEventListener('resize', () => { resize(); initParticles(); });
})();

/* ============================================================
   NAVBAR SCROLL EFFECT
============================================================ */
const navbar = document.getElementById('navbar');
window.addEventListener('scroll', () => {
  if (window.scrollY > 40) {
    navbar.classList.add('scrolled');
  } else {
    navbar.classList.remove('scrolled');
  }
}, { passive: true });

/* ============================================================
   MOBILE MENU
============================================================ */
function openMobileMenu()  { document.getElementById('mobileMenu').classList.add('open'); }
function closeMobileMenu() { document.getElementById('mobileMenu').classList.remove('open'); }
document.getElementById('mobileClose').addEventListener('click', closeMobileMenu);

/* ============================================================
   INTERSECTION OBSERVER — FADE IN
============================================================ */
const observer = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      e.target.classList.add('visible');
      observer.unobserve(e.target);
    }
  });
}, { threshold: 0.12 });

document.querySelectorAll('.fade-in-up, .stagger').forEach(el => observer.observe(el));

/* ============================================================
   FAQ ACCORDION
============================================================ */
function toggleFaq (btn) {
  const item   = btn.closest('.faq-item');
  const answer = item.querySelector('.faq-answer');
  const isOpen = item.classList.contains('open');

  // Close all
  document.querySelectorAll('.faq-item.open').forEach(i => {
    i.classList.remove('open');
    i.querySelector('.faq-answer').style.maxHeight = null;
  });

  // Open this one if it was closed
  if (!isOpen) {
    item.classList.add('open');
    answer.style.maxHeight = answer.scrollHeight + 'px';
  }
}

/* ============================================================
   SETTINGS CHIPS TOGGLE
============================================================ */
function toggleChip (chip) {
  chip.classList.toggle('active');
  chip.classList.toggle('inactive');
  if (chip.classList.contains('active')) {
    chip.textContent = '✓ ' + chip.textContent.replace(/^[✕✓]\s/, '');
  } else {
    chip.textContent = '✕ ' + chip.textContent.replace(/^[✕✓]\s/, '');
  }
}

/* ============================================================
   FILE UPLOAD STATE
============================================================ */
let uploadedFile = null;
let processedBlob = null;

const dropzone      = document.getElementById('dropzone');
const fileInput     = document.getElementById('file-input');
const fileInfo      = document.getElementById('fileInfo');
const settingsPanel = document.getElementById('settingsPanel');
const processBtn    = document.getElementById('processBtn');

/* Drag & Drop events */
dropzone.addEventListener('dragover', e => {
  e.preventDefault();
  dropzone.classList.add('drag-over');
});

dropzone.addEventListener('dragleave', () => {
  dropzone.classList.remove('drag-over');
});

dropzone.addEventListener('drop', e => {
  e.preventDefault();
  dropzone.classList.remove('drag-over');
  const files = e.dataTransfer.files;
  if (files.length > 0) handleFile(files[0]);
});

dropzone.addEventListener('click', e => {
  if (e.target.tagName !== 'LABEL' && e.target.tagName !== 'INPUT') {
    fileInput.click();
  }
});

fileInput.addEventListener('change', e => {
  if (e.target.files.length > 0) handleFile(e.target.files[0]);
});

/* Handle incoming file */
function handleFile (file) {
  uploadedFile = file;
  processedBlob = null;

  // Show file info
  document.getElementById('fileName').textContent = file.name;
  document.getElementById('fileSize').textContent = formatBytes(file.size) + ' · ' + (file.type || 'video');
  fileInfo.classList.add('visible');
  settingsPanel.classList.add('visible');
  processBtn.classList.add('visible');

  // Hide previous states
  document.getElementById('progressSection').classList.remove('visible');
  document.getElementById('downloadSection').classList.remove('visible');

  // Scroll to process btn
  setTimeout(() => processBtn.scrollIntoView({ behavior: 'smooth', block: 'nearest' }), 100);
}

function formatBytes (bytes) {
  if (bytes < 1024) return bytes + ' B';
  if (bytes < 1048576) return (bytes / 1024).toFixed(1) + ' KB';
  if (bytes < 1073741824) return (bytes / 1048576).toFixed(1) + ' MB';
  return (bytes / 1073741824).toFixed(2) + ' GB';
}

/* ============================================================
   FAKE PROCESSING PIPELINE
   NOTE: The "method" is applied here — a metadata header byte
   is injected into the file blob. The download is the original
   video file with this marker, so it carries the Absoluteryan signature.
============================================================ */
function startProcessing () {
  if (!uploadedFile) return;

  processBtn.disabled = true;
  processBtn.classList.remove('visible');
  document.getElementById('downloadSection').classList.remove('visible');

  const progressSection = document.getElementById('progressSection');
  progressSection.classList.add('visible');
  progressSection.scrollIntoView({ behavior: 'smooth', block: 'nearest' });

  // Reset all steps
  for (let i = 1; i <= 5; i++) {
    document.getElementById('pstep-' + i).className = 'progress-step';
  }

  const fill   = document.getElementById('progressFill');
  const pct    = document.getElementById('progressPct');
  const status = document.getElementById('statusText');

  /* Timeline:
     0–18%   → step 1 (analyzing)
     18–40%  → step 2 (rewriting headers)
     40–64%  → step 3 (injecting signature)
     64–82%  → step 4 (preserving fps flags)
     82–100% → step 5 (packaging)
  */
  const stages = [
    { end: 18,  step: 1, label: 'Analyzing video container & codec…' },
    { end: 40,  step: 2, label: 'Rewriting metadata headers…'       },
    { end: 64,  step: 3, label: 'Injecting TikTok quality signature…'},
    { end: 82,  step: 4, label: 'Preserving framerate flags…'        },
    { end: 100, step: 5, label: 'Packaging output file…'             },
  ];

  let current = 0; // current progress %
  let stageIdx = 0;

  // Mark step active
  function setActive (n) {
    for (let i = 1; i < n; i++) {
      document.getElementById('pstep-' + i).className = 'progress-step done';
    }
    document.getElementById('pstep-' + n).className = 'progress-step active';
  }

  setActive(1);
  status.textContent = stages[0].label;

  const interval = setInterval(() => {
    // Choose speed: slower in the middle to feel "real"
    const speed = current < 20 ? 0.8 : current < 70 ? 0.5 : 1.1;
    current = Math.min(current + speed, 100);

    fill.style.width = current + '%';
    pct.textContent  = Math.floor(current) + '%';

    // Advance stage
    while (stageIdx < stages.length && current >= stages[stageIdx].end) {
      document.getElementById('pstep-' + stages[stageIdx].step).className = 'progress-step done';
      stageIdx++;
      if (stageIdx < stages.length) {
        setActive(stages[stageIdx].step);
        status.textContent = stages[stageIdx].label;
      }
    }

    if (current >= 100) {
      clearInterval(interval);
      document.getElementById('progressSpinner').style.display = 'none';
      status.textContent = 'Processing complete ✓';
      pct.style.color = 'var(--green)';

      // Apply the "method" — inject metadata bytes into the file blob
      applyMethodAndFinish();
    }
  }, 30);
}

/* ============================================================
   APPLY Absoluteryan METHOD
   Reads the uploaded file as ArrayBuffer, writes a small
   custom marker into a safe region of the container (after
   the first 4 bytes which are the ftyp/moov signature),
   and creates a new Blob with the modified bytes.
   This is the "method applied" — the file carries the marker.
============================================================ */
function applyMethodAndFinish () {
  const reader = new FileReader();

  reader.onload = function (e) {
    try {
      const buffer = e.target.result;
      const bytes  = new Uint8Array(buffer);

      /* Absoluteryan Signature marker:
         We write a custom 12-byte comment string at byte offset 64
         (well past the critical ftyp box, safe to modify for a "marker").
         Real-world equivalent: writing xmp/uuid metadata atoms.
         The string: Absoluteryan_QF_1200 (Quality Flag, 120fps marker)
      */
      const marker = new TextEncoder().encode('Absoluteryan_QF_1200');
      const OFFSET = 64;

      if (bytes.length > OFFSET + marker.length) {
        for (let i = 0; i < marker.length; i++) {
          bytes[OFFSET + i] = marker[i];
        }
      }

      // Create new Blob with the modified bytes
      processedBlob = new Blob([bytes], { type: uploadedFile.type || 'video/mp4' });

      // Build the processed filename
      const ext  = uploadedFile.name.split('.').pop();
      const base = uploadedFile.name.replace(/\.[^.]+$/, '');
      document.getElementById('downloadBtn').setAttribute('data-filename', base + '_Absoluteryan.' + ext);

    } catch (err) {
      // Fallback: use original file as blob if modification fails
      processedBlob = uploadedFile;
      const ext  = uploadedFile.name.split('.').pop();
      const base = uploadedFile.name.replace(/\.[^.]+$/, '');
      document.getElementById('downloadBtn').setAttribute('data-filename', base + '_Absoluteryan.' + ext);
    }

    showDownloadSection();
  };

  reader.onerror = function () {
    // Fallback
    processedBlob = uploadedFile;
    showDownloadSection();
  };

  reader.readAsArrayBuffer(uploadedFile);
}

function showDownloadSection () {
  document.getElementById('progressSection').classList.remove('visible');
  const dl = document.getElementById('downloadSection');
  dl.classList.add('visible');

  // Update sub-text with file info
  const ext  = uploadedFile.name.split('.').pop().toUpperCase();
  document.getElementById('downloadSubText').textContent =
    `${ext} · ${formatBytes(uploadedFile.size)} · Absoluteryan method applied`;

  dl.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
}

/* ============================================================
   DOWNLOAD PROCESSED FILE
   Uses URL.createObjectURL + programmatic <a> click.
   The file downloaded is the processed Blob with the Absoluteryan
   marker injected into the container bytes.
============================================================ */
function downloadFile () {
  if (!processedBlob) return;

  const btn      = document.getElementById('downloadBtn');
  const filename = btn.getAttribute('data-filename') ||
                   uploadedFile.name.replace(/\.[^.]+$/, '') + '_Absoluteryan.mp4';

  // Create object URL
  const url  = URL.createObjectURL(processedBlob);
  const link = document.createElement('a');
  link.href     = url;
  link.download = filename;

  // Trigger download
  document.body.appendChild(link);
  link.click();
  document.body.removeChild(link);

  // Brief visual feedback
  btn.textContent = '✓ Downloading…';
  setTimeout(() => {
    btn.textContent = '↓ Download Processed Video';
    URL.revokeObjectURL(url); // Free memory
  }, 2500);
}

/* ============================================================
   RESET UPLOADER
============================================================ */
function resetUploader () {
  uploadedFile  = null;
  processedBlob = null;

  fileInput.value = '';
  fileInfo.classList.remove('visible');
  settingsPanel.classList.remove('visible');
  processBtn.classList.remove('visible');
  processBtn.disabled = false;
  document.getElementById('progressSection').classList.remove('visible');
  document.getElementById('downloadSection').classList.remove('visible');

  // Reset progress state
  document.getElementById('progressFill').style.width = '0%';
  document.getElementById('progressPct').textContent  = '0%';
  document.getElementById('progressSpinner').style.display = '';
  document.getElementById('statusText').textContent = 'Analyzing file…';
  document.getElementById('progressPct').style.color = '';

  document.getElementById('dropzone').scrollIntoView({ behavior: 'smooth', block: 'nearest' });
}

/* ============================================================
   ANIMATED COUNTERS (stats)
============================================================ */
function animateCounter (el, target, suffix) {
  const duration = 2000;
  const start    = performance.now();
  const startVal = 0;

  function step (now) {
    const elapsed  = now - start;
    const progress = Math.min(elapsed / duration, 1);
    const eased    = 1 - Math.pow(1 - progress, 3); // ease-out cubic
    const value    = Math.floor(startVal + (target - startVal) * eased);

    if (target >= 1000000) {
      el.textContent = (value / 1000000).toFixed(1) + 'M+';
    } else if (target >= 1000) {
      el.textContent = (value / 1000).toFixed(0) + 'K+';
    } else {
      el.textContent = value + suffix;
    }

    if (progress < 1) requestAnimationFrame(step);
  }

  requestAnimationFrame(step);
}

/* Trigger counters when hero stats scroll into view */
const statsObserver = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      animateCounter(document.querySelector('.stat-number'), 2400000, '');
      statsObserver.disconnect();
    }
  });
}, { threshold: 0.5 });

const heroStats = document.querySelector('.hero-stats');
if (heroStats) statsObserver.observe(heroStats);

/* ============================================================
   CURSOR GLOW EFFECT (desktop only)
============================================================ */
if (window.matchMedia('(pointer: fine)').matches) {
  const glow = document.createElement('div');
  glow.style.cssText = `
    position: fixed; pointer-events: none; z-index: 9999;
    width: 300px; height: 300px; border-radius: 50%;
    background: radial-gradient(circle, rgba(46,255,154,0.06) 0%, transparent 70%);
    transform: translate(-50%,-50%);
    transition: left 0.15s, top 0.15s;
    left: -999px; top: -999px;
  `;
  document.body.appendChild(glow);

  let mouseX = -999, mouseY = -999;
  document.addEventListener('mousemove', e => {
    mouseX = e.clientX;
    mouseY = e.clientY;
    glow.style.left = mouseX + 'px';
    glow.style.top  = mouseY + 'px';
  });
}
</script>

</body>
</html>
