<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
<title>Happy Birthday Lulu 🎀</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700&family=Space+Mono&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
–bg: #0a0a0a;
–surface: #141414;
–surface2: #1c1c1c;
–border: rgba(255,255,255,0.07);
–text: #f0f0f0;
–muted: rgba(255,255,255,0.32);
–on-accent: #d4b896;
–asos-red: #e00028;
}

html { scroll-behavior: smooth; }

body {
font-family: ‘Syne’, sans-serif;
background: var(–bg);
color: var(–text);
min-height: 100vh;
overflow-x: hidden;
}

/* ── HERO ── */
.hero {
min-height: 100svh;
display: flex;
flex-direction: column;
align-items: center;
justify-content: center;
text-align: center;
padding: 60px 24px 40px;
position: relative;
}

.hero::before {
content: ‘’;
position: absolute;
inset: 0;
background: radial-gradient(ellipse 60% 40% at 50% 55%, rgba(212,184,150,0.07) 0%, transparent 70%);
pointer-events: none;
}

.ribbon {
font-size: 10px;
font-weight: 400;
letter-spacing: 0.45em;
text-transform: uppercase;
color: var(–muted);
margin-bottom: 32px;
animation: fadeUp 0.9s ease both;
}

.hero h1 {
font-size: clamp(58px, 16vw, 100px);
font-weight: 700;
line-height: 1.0;
letter-spacing: -0.03em;
color: var(–text);
animation: fadeUp 0.9s 0.12s ease both;
}

.hero h1 span { color: var(–on-accent); display: block; }

.scroll-hint {
position: absolute;
bottom: 30px;
left: 50%;
transform: translateX(-50%);
display: flex;
flex-direction: column;
align-items: center;
gap: 10px;
animation: fadeUp 0.9s 0.5s ease both;
}

.scroll-hint p { font-size: 9px; letter-spacing: 0.4em; text-transform: uppercase; color: var(–muted); }

.scroll-line {
width: 1px; height: 44px;
background: linear-gradient(to bottom, var(–on-accent), transparent);
animation: scrollPulse 2s ease-in-out infinite;
}

/* ── SECTIONS ── */
.gift-section { padding: 72px 0 80px; border-top: 1px solid var(–border); }

.section-inner { padding: 0 20px; max-width: 480px; margin: 0 auto; }

/* ── BRAND HEADER ── */
.brand-header { display: flex; align-items: center; gap: 18px; margin-bottom: 36px; }

.brand-logo-box {
width: 64px; height: 64px; border-radius: 16px;
display: flex; align-items: center; justify-content: center;
flex-shrink: 0; overflow: hidden; position: relative; cursor: pointer;
}

.brand-logo-box input[type=“file”] { position: absolute; inset: 0; opacity: 0; cursor: pointer; z-index: 5; }
.brand-logo-box .logo-img { width: 100%; height: 100%; object-fit: contain; display: none; }

.on-logo-box { background: #ffffff; }
.on-logo-text { font-weight: 700; font-size: 22px; color: #000; letter-spacing: 0.05em; }

.asos-logo-box { background: var(–asos-red); }
.asos-logo-text { font-weight: 700; font-size: 15px; color: #fff; letter-spacing: 0.14em; }

.brand-eyebrow { font-size: 10px; font-weight: 400; letter-spacing: 0.35em; text-transform: uppercase; color: var(–muted); margin-bottom: 6px; }

.brand-title { font-size: 26px; font-weight: 700; letter-spacing: -0.02em; line-height: 1.1; }

.on-accent { color: var(–on-accent); }
.asos-accent { color: var(–asos-red); }

/* ── CREDIT CARD ── */
.credit-card {
width: 100%;
aspect-ratio: 85.6 / 53.98;
border-radius: 22px;
padding: 20px 22px 18px;
position: relative;
overflow: hidden;
display: flex;
flex-direction: column;
justify-content: space-between;
margin-bottom: 14px;
box-shadow: 0 28px 64px rgba(0,0,0,0.7);
}

.on-cc {
background: linear-gradient(130deg, #1f1f1f 0%, #2c2c2c 60%, #1a1a1a 100%);
border: 1px solid rgba(255,255,255,0.09);
}

.asos-cc {
background: linear-gradient(130deg, #200008 0%, #400012 55%, #1a0006 100%);
border: 1px solid rgba(224,0,40,0.22);
}

.cc-glow {
position: absolute; top: -60px; right: -60px;
width: 180px; height: 180px; border-radius: 50%; pointer-events: none;
}

.on-cc .cc-glow { background: radial-gradient(circle, rgba(212,184,150,0.12) 0%, transparent 70%); }
.asos-cc .cc-glow { background: radial-gradient(circle, rgba(224,0,40,0.2) 0%, transparent 70%); }

.cc-top { display: flex; justify-content: space-between; align-items: flex-start; position: relative; }

.cc-brand-label { font-size: 10px; font-weight: 500; letter-spacing: 0.25em; text-transform: uppercase; color: rgba(255,255,255,0.4); }

.cc-chip {
width: 34px; height: 25px; border-radius: 5px;
background: linear-gradient(135deg, #c8942a, #f0d080, #b8821a);
opacity: 0.85;
}

.cc-number {
font-family: ‘Space Mono’, monospace;
font-size: clamp(14px, 4vw, 19px);
letter-spacing: 0.1em;
color: rgba(255,255,255,0.88);
text-align: center;
position: relative;
transition: filter 0.35s ease;
}

.cc-number.blurred { filter: blur(8px); user-select: none; }

.cc-bottom { display: flex; justify-content: space-between; align-items: flex-end; position: relative; }

.cc-meta { display: flex; flex-direction: column; gap: 3px; }
.cc-meta-label { font-size: 8px; letter-spacing: 0.22em; text-transform: uppercase; color: rgba(255,255,255,0.3); }

.cc-meta-value {
font-family: ‘Space Mono’, monospace;
font-size: 13px;
color: rgba(255,255,255,0.82);
transition: filter 0.35s ease;
}

.cc-meta-value.blurred { filter: blur(6px); user-select: none; }

/* CVV strip */
.cvv-strip {
display: flex; align-items: center; justify-content: space-between;
background: var(–surface); border: 1px solid var(–border);
border-radius: 14px; padding: 14px 20px; margin-bottom: 20px;
}

.cvv-inner { display: flex; flex-direction: column; gap: 3px; }
.cvv-label { font-size: 9px; letter-spacing: 0.3em; text-transform: uppercase; color: var(–muted); }

.cvv-val {
font-family: ‘Space Mono’, monospace;
font-size: 20px; color: var(–text);
transition: filter 0.35s ease;
}

.cvv-val.blurred { filter: blur(7px); user-select: none; }
.lock-icon { opacity: 0.2; }

/* ── UNLOCK PANEL ── */
.unlock-panel {
background: var(–surface);
border: 1px solid var(–border);
border-radius: 20px;
padding: 24px 20px;
margin-bottom: 20px;
display: flex;
flex-direction: column;
gap: 14px;
}

.unlock-title {
font-size: 11px;
font-weight: 500;
letter-spacing: 0.3em;
text-transform: uppercase;
color: var(–muted);
display: flex;
align-items: center;
gap: 8px;
}

.unlock-title svg { opacity: 0.5; }

.unlock-hint {
font-size: 13px;
font-weight: 400;
color: rgba(255,255,255,0.55);
line-height: 1.5;
}

/* Date pickers row */
.date-inputs {
display: grid;
grid-template-columns: 1fr 1fr 1fr;
gap: 8px;
}

.date-select {
background: var(–surface2);
border: 1px solid var(–border);
border-radius: 10px;
color: var(–text);
font-family: ‘Syne’, sans-serif;
font-size: 13px;
font-weight: 500;
padding: 12px 8px;
text-align: center;
appearance: none;
-webkit-appearance: none;
cursor: pointer;
outline: none;
transition: border-color 0.2s;
width: 100%;
}

.date-select:focus { border-color: rgba(255,255,255,0.25); }

.date-select option { background: #1c1c1c; }

.unlock-btn {
width: 100%;
padding: 14px;
border-radius: 12px;
font-family: ‘Syne’, sans-serif;
font-weight: 600;
font-size: 12px;
letter-spacing: 0.2em;
text-transform: uppercase;
border: none;
cursor: pointer;
transition: all 0.2s;
}

.on-unlock-btn { background: rgba(212,184,150,0.15); color: var(–on-accent); border: 1px solid rgba(212,184,150,0.25); }
.on-unlock-btn:active { background: rgba(212,184,150,0.25); transform: scale(0.98); }
.on-unlock-btn.unlocked { background: rgba(212,184,150,0.2); color: var(–on-accent); }

.asos-unlock-btn { background: rgba(224,0,40,0.12); color: var(–asos-red); border: 1px solid rgba(224,0,40,0.25); }
.asos-unlock-btn:active { background: rgba(224,0,40,0.22); transform: scale(0.98); }
.asos-unlock-btn.unlocked { background: rgba(224,0,40,0.18); color: var(–asos-red); }

/* Error shake */
.shake {
animation: shake 0.4s ease;
}

@keyframes shake {
0%,100% { transform: translateX(0); }
20% { transform: translateX(-8px); }
40% { transform: translateX(8px); }
60% { transform: translateX(-5px); }
80% { transform: translateX(5px); }
}

.error-msg {
font-size: 11px;
color: #ff4d6d;
text-align: center;
font-weight: 500;
letter-spacing: 0.05em;
min-height: 16px;
transition: opacity 0.3s;
}

.success-msg {
font-size: 11px;
color: #4caf87;
text-align: center;
font-weight: 500;
letter-spacing: 0.05em;
}

/* ── CTA ── */
.cta-btn {
display: block; width: 100%; padding: 17px; border-radius: 14px;
font-family: ‘Syne’, sans-serif; font-weight: 600; font-size: 13px;
letter-spacing: 0.18em; text-transform: uppercase;
text-align: center; text-decoration: none; border: none;
cursor: pointer; transition: all 0.2s ease;
}

.on-cta { background: #fff; color: #000; }
.on-cta:active { background: #e0e0e0; transform: scale(0.98); }

.asos-cta { background: var(–asos-red); color: #fff; }
.asos-cta:active { background: #b8001f; transform: scale(0.98); }

/* ── FOOTER ── */
.footer { padding: 56px 24px; text-align: center; border-top: 1px solid var(–border); }
.footer-love { font-size: 28px; font-weight: 700; letter-spacing: -0.02em; color: var(–on-accent); margin-bottom: 10px; }
.footer-sub { font-size: 10px; letter-spacing: 0.4em; text-transform: uppercase; color: var(–muted); }

/* ── ANIMATIONS ── */
@keyframes fadeUp {
from { opacity: 0; transform: translateY(22px); }
to   { opacity: 1; transform: translateY(0); }
}
@keyframes scrollPulse {
0%, 100% { opacity: 0.3; }
50% { opacity: 1; }
}

.fade-in { opacity: 0; transform: translateY(22px); transition: opacity 0.7s ease, transform 0.7s ease; }
.fade-in.visible { opacity: 1; transform: translateY(0); }
</style>

</head>
<body>

<!-- HERO -->

<section class="hero">
  <p class="ribbon">A little something for you 🎀</p>
  <h1>Happy Birthday<br><span>Lulu</span></h1>
  <div class="scroll-hint">
    <p>Your gifts</p>
    <div class="scroll-line"></div>
  </div>
</section>

<!-- ON CLOUD -->

<section class="gift-section">
  <div class="section-inner">

```
<div class="brand-header fade-in">
  <div class="brand-logo-box on-logo-box">
    <span class="on-logo-text" id="onLogoText">On</span>
    <img class="logo-img" id="onLogoImg" alt="On logo">
    <input type="file" accept="image/*" onchange="uploadLogo(event,'onLogoImg','onLogoText')">
  </div>
  <div>
    <p class="brand-eyebrow">Gift #1</p>
    <h2 class="brand-title">Your fav <span class="on-accent">On Cloud</span> shoes</h2>
  </div>
</div>

<!-- Credit Card -->
<div class="credit-card on-cc fade-in">
  <div class="cc-glow"></div>
  <div class="cc-top">
    <span class="cc-brand-label">Prepaid Card</span>
    <div class="cc-chip"></div>
  </div>
  <div class="cc-number blurred" id="onNum">5291 3582 2176 1272</div>
  <div class="cc-bottom">
    <div class="cc-meta">
      <span class="cc-meta-label">Card Holder</span>
      <span class="cc-meta-value">HBD LULU</span>
    </div>
    <div class="cc-meta">
      <span class="cc-meta-label">Expires</span>
      <span class="cc-meta-value blurred" id="onExp">06/30</span>
    </div>
    <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="rgba(255,255,255,0.25)" stroke-width="1.8" stroke-linecap="round"><rect x="3" y="11" width="18" height="11" rx="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>
  </div>
</div>

<div class="cvv-strip fade-in">
  <div class="cvv-inner">
    <span class="cvv-label">Security Code (CVV)</span>
    <span class="cvv-val blurred" id="onCvv">938</span>
  </div>
  <svg class="lock-icon" width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="1.8" stroke-linecap="round"><rect x="3" y="11" width="18" height="11" rx="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>
</div>

<!-- Unlock panel -->
<div class="unlock-panel fade-in" id="onUnlockPanel">
  <div class="unlock-title">
    <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><circle cx="12" cy="12" r="10"/><path d="M12 8v4M12 16h.01"/></svg>
    Unlock card details
  </div>
  <p class="unlock-hint">Enter your birthday to reveal the card info 🎂</p>
  <div class="date-inputs">
    <select class="date-select" id="onMonth">
      <option value="">Month</option>
      <option value="1">January</option><option value="2">February</option>
      <option value="3">March</option><option value="4">April</option>
      <option value="5">May</option><option value="6">June</option>
      <option value="7">July</option><option value="8">August</option>
      <option value="9">September</option><option value="10">October</option>
      <option value="11">November</option><option value="12">December</option>
    </select>
    <select class="date-select" id="onDay">
      <option value="">Day</option>
      <script>for(let i=1;i<=31;i++) document.write(`<option value="${i}">${i}</option>`);</script>
    </select>
    <select class="date-select" id="onYear">
      <option value="">Year</option>
      <script>for(let y=2010;y>=1990;y--) document.write(`<option value="${y}">${y}</option>`);</script>
    </select>
  </div>
  <div class="error-msg" id="onError"></div>
  <button class="unlock-btn on-unlock-btn" id="onUnlockBtn" onclick="tryUnlock('on')">
    🔒 Reveal My Gift
  </button>
</div>

<a class="cta-btn on-cta fade-in" href="https://www.on-running.com" target="_blank">Shop On Cloud →</a>
```

  </div>
</section>

<!-- ASOS -->

<section class="gift-section">
  <div class="section-inner">

```
<div class="brand-header fade-in">
  <div class="brand-logo-box asos-logo-box">
    <span class="asos-logo-text" id="asosLogoText">ASOS</span>
    <img class="logo-img" id="asosLogoImg" alt="ASOS logo">
    <input type="file" accept="image/*" onchange="uploadLogo(event,'asosLogoImg','asosLogoText')">
  </div>
  <div>
    <p class="brand-eyebrow">Gift #2 · $200</p>
    <h2 class="brand-title">Shop anything on <span class="asos-accent">ASOS</span></h2>
  </div>
</div>

<!-- Credit Card -->
<div class="credit-card asos-cc fade-in">
  <div class="cc-glow"></div>
  <div class="cc-top">
    <span class="cc-brand-label">Prepaid · $200</span>
    <div class="cc-chip"></div>
  </div>
  <div class="cc-number blurred" id="asosNum">5291 3582 2176 1272</div>
  <div class="cc-bottom">
    <div class="cc-meta">
      <span class="cc-meta-label">Card Holder</span>
      <span class="cc-meta-value">HBD LULU</span>
    </div>
    <div class="cc-meta">
      <span class="cc-meta-label">Expires</span>
      <span class="cc-meta-value blurred" id="asosExp">06/30</span>
    </div>
    <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="rgba(255,255,255,0.25)" stroke-width="1.8" stroke-linecap="round"><rect x="3" y="11" width="18" height="11" rx="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>
  </div>
</div>

<div class="cvv-strip fade-in">
  <div class="cvv-inner">
    <span class="cvv-label">Security Code (CVV)</span>
    <span class="cvv-val blurred" id="asosCvv">938</span>
  </div>
  <svg class="lock-icon" width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="1.8" stroke-linecap="round"><rect x="3" y="11" width="18" height="11" rx="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>
</div>

<!-- Unlock panel -->
<div class="unlock-panel fade-in" id="asosUnlockPanel">
  <div class="unlock-title">
    <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><circle cx="12" cy="12" r="10"/><path d="M12 8v4M12 16h.01"/></svg>
    Unlock card details
  </div>
  <p class="unlock-hint">Enter Saeed's birthday to reveal 🎂</p>
  <div class="date-inputs">
    <select class="date-select" id="asosMonth">
      <option value="">Month</option>
      <option value="1">January</option><option value="2">February</option>
      <option value="3">March</option><option value="4">April</option>
      <option value="5">May</option><option value="6">June</option>
      <option value="7">July</option><option value="8">August</option>
      <option value="9">September</option><option value="10">October</option>
      <option value="11">November</option><option value="12">December</option>
    </select>
    <select class="date-select" id="asosDay">
      <option value="">Day</option>
      <script>for(let i=1;i<=31;i++) document.write(`<option value="${i}">${i}</option>`);</script>
    </select>
    <select class="date-select" id="asosYear">
      <option value="">Year</option>
      <script>for(let y=2010;y>=1990;y--) document.write(`<option value="${y}">${y}</option>`);</script>
    </select>
  </div>
  <div class="error-msg" id="asosError"></div>
  <button class="unlock-btn asos-unlock-btn" id="asosUnlockBtn" onclick="tryUnlock('asos')">
    🔒 Reveal My Gift
  </button>
</div>

<a class="cta-btn asos-cta fade-in" href="https://www.asos.com" target="_blank">Shop ASOS →</a>
```

  </div>
</section>

<!-- FOOTER -->

<footer class="footer">
  <p class="footer-love">With all my love 🤍</p>
  <p class="footer-sub">Happy Birthday, Lulu</p>
</footer>

<script>
  // Scroll fade-in
  const obs = new IntersectionObserver(entries => {
    entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('visible'); obs.unobserve(e.target); } });
  }, { threshold: 0.08 });
  document.querySelectorAll('.fade-in').forEach(el => obs.observe(el));

  // Passwords: month, day, year
  const answers = {
    on:   { month: 4,  day: 25, year: 2004 },  // April 25, 2004 — Lulu's birthday
    asos: { month: 7,  day: 24, year: 2002 }   // July 24, 2002 — Saeed's birthday
  };

  function tryUnlock(brand) {
    const m = parseInt(document.getElementById(brand + 'Month').value);
    const d = parseInt(document.getElementById(brand + 'Day').value);
    const y = parseInt(document.getElementById(brand + 'Year').value);
    const err = document.getElementById(brand + 'Error');

    if (!m || !d || !y) {
      showError(brand, 'Please select month, day, and year ✦');
      return;
    }

    const a = answers[brand];
    if (m === a.month && d === a.day && y === a.year) {
      // Correct!
      revealCard(brand);
    } else {
      showError(brand, 'Wrong date — try again 🔒');
      const panel = document.getElementById(brand + 'UnlockPanel');
      panel.classList.remove('shake');
      void panel.offsetWidth;
      panel.classList.add('shake');
    }
  }

  function showError(brand, msg) {
    const el = document.getElementById(brand + 'Error');
    el.textContent = msg;
    setTimeout(() => { el.textContent = ''; }, 3000);
  }

  function revealCard(brand) {
    // Unblur
    document.getElementById(brand + 'Num').classList.remove('blurred');
    document.getElementById(brand + 'Exp').classList.remove('blurred');
    document.getElementById(brand + 'Cvv').classList.remove('blurred');

    // Replace unlock panel with success msg
    const panel = document.getElementById(brand + 'UnlockPanel');
    panel.innerHTML = `<div class="success-msg" style="padding:8px 0; font-size:14px;">🎉 Unlocked! Enjoy your gift, Lulu 💛</div>`;
  }

  // Logo upload
  function uploadLogo(e, imgId, txtId) {
    const file = e.target.files[0]; if (!file) return;
    const r = new FileReader();
    r.onload = ev => {
      const img = document.getElementById(imgId);
      const txt = document.getElementById(txtId);
      img.src = ev.target.result; img.style.display = 'block'; txt.style.display = 'none';
    };
    r.readAsDataURL(file);
  }
</script>

</body>
</html>
