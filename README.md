<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>For Teena Ji — With All My Heart ❤️</title>
  
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,500;0,700;1,400;1,600&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&family=Caveat:wght@600;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg-dark: #0f1118;
      --card-bg: rgba(26, 30, 43, 0.85);
      --card-border: rgba(243, 198, 119, 0.25);
      --gold: #f3c677;
      --gold-hover: #e5b35c;
      --rose: #f28b9f;
      --rose-soft: rgba(242, 139, 159, 0.15);
      --text: #f5f5f7;
      --text-muted: #abb1c0;
      --font-serif: 'Cormorant Garamond', Georgia, serif;
      --font-hand: 'Caveat', cursive;
      --font-sans: 'Plus Jakarta Sans', sans-serif;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      background: radial-gradient(circle at 50% 20%, #1f2538 0%, var(--bg-dark) 75%);
      color: var(--text);
      font-family: var(--font-sans);
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 2rem 1.2rem;
      position: relative;
      overflow-x: hidden;
    }

    .sparkle-canvas {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 0;
    }

    .main-wrapper {
      max-width: 660px;
      width: 100%;
      background: var(--card-bg);
      border: 1px solid var(--card-border);
      border-radius: 28px;
      backdrop-filter: blur(20px);
      -webkit-backdrop-filter: blur(20px);
      padding: 3rem 2rem;
      box-shadow: 0 30px 80px rgba(0, 0, 0, 0.6);
      position: relative;
      z-index: 2;
      text-align: center;
    }

    .audio-pill {
      position: absolute;
      top: 1.2rem;
      right: 1.5rem;
      background: rgba(255, 255, 255, 0.08);
      border: 1px solid rgba(255, 255, 255, 0.15);
      padding: 0.35rem 0.85rem;
      border-radius: 20px;
      font-size: 0.8rem;
      color: var(--gold);
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 6px;
      user-select: none;
      z-index: 10;
    }

    .gift-stage {
      display: block;
      transition: opacity 0.4s ease;
    }

    .subtitle {
      font-size: 0.85rem;
      letter-spacing: 3px;
      text-transform: uppercase;
      color: var(--gold);
      font-weight: 600;
      margin-bottom: 0.4rem;
    }

    .title {
      font-family: var(--font-serif);
      font-size: 2.3rem;
      font-weight: 700;
      margin-bottom: 0.6rem;
      color: #ffffff;
      line-height: 1.2;
    }

    .desc {
      color: var(--text-muted);
      font-size: 0.95rem;
      margin-bottom: 2rem;
      line-height: 1.6;
    }

    /* Interactive Box */
    .box-container {
      width: 140px;
      height: 140px;
      margin: 1.5rem auto 2.5rem;
      position: relative;
      cursor: pointer;
      user-select: none;
      animation: float 3s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-8px); }
    }

    .gift-box-base {
      width: 130px;
      height: 95px;
      background: linear-gradient(135deg, #e56586, #b83d5e);
      border-radius: 0 0 14px 14px;
      position: absolute;
      bottom: 0;
      left: 5px;
      box-shadow: 0 15px 30px rgba(0,0,0,0.4);
    }

    .gift-ribbon-v {
      position: absolute;
      width: 24px;
      height: 100%;
      background: var(--gold);
      left: 53px;
    }

    .gift-ribbon-h {
      position: absolute;
      width: 100%;
      height: 20px;
      background: var(--gold);
      top: 38px;
    }

    .gift-lid {
      width: 144px;
      height: 32px;
      background: linear-gradient(135deg, #f27999, #cc496c);
      border-radius: 8px;
      position: absolute;
      top: 18px;
      left: -2px;
      box-shadow: 0 6px 15px rgba(0,0,0,0.25);
      transition: transform 0.5s ease;
      z-index: 5;
    }

    .gift-bow {
      position: absolute;
      top: -14px;
      left: 52px;
      width: 40px;
      height: 24px;
    }

    .gift-bow::before, .gift-bow::after {
      content: "";
      position: absolute;
      width: 20px;
      height: 18px;
      border: 3px solid var(--gold);
      border-radius: 50% 50% 10% 50%;
      top: 0;
    }
    .gift-bow::before { left: 0; transform: rotate(-30deg); }
    .gift-bow::after { right: 0; transform: rotate(30deg) scaleX(-1); }

    .open-btn {
      background: linear-gradient(135deg, var(--gold), var(--gold-hover));
      color: #14161f;
      border: none;
      padding: 0.95rem 2.5rem;
      border-radius: 50px;
      font-size: 1rem;
      font-weight: 700;
      letter-spacing: 1px;
      cursor: pointer;
      box-shadow: 0 10px 25px rgba(243, 198, 119, 0.35);
      transition: transform 0.2s, box-shadow 0.2s;
    }

    .open-btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 14px 30px rgba(243, 198, 119, 0.5);
    }

    /* Unboxed Stage */
    .unboxed-stage {
      display: none;
      opacity: 0;
      transition: opacity 0.6s ease;
      text-align: left;
    }

    .greet-badge {
      display: inline-block;
      background: var(--rose-soft);
      border: 1px solid rgba(242, 139, 159, 0.3);
      color: var(--rose);
      padding: 0.3rem 0.9rem;
      border-radius: 20px;
      font-size: 0.82rem;
      font-weight: 600;
      margin-bottom: 0.8rem;
    }

    .unboxed-stage h2 {
      font-family: var(--font-serif);
      font-size: 2.1rem;
      color: #fff;
      line-height: 1.2;
      margin-bottom: 0.4rem;
    }

    .unboxed-sub {
      color: var(--text-muted);
      font-size: 0.95rem;
      margin-bottom: 2rem;
    }

    .gifts-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 1rem;
      margin-bottom: 2.5rem;
    }

    .gift-card {
      background: rgba(255, 255, 255, 0.04);
      border: 1px solid rgba(255, 255, 255, 0.08);
      border-radius: 16px;
      padding: 1.2rem 1rem;
      text-align: center;
      cursor: pointer;
      transition: all 0.3s;
    }

    .gift-card:hover {
      background: rgba(243, 198, 119, 0.1);
      border-color: rgba(243, 198, 119, 0.4);
      transform: translateY(-3px);
    }

    .gift-card .icon {
      font-size: 2.1rem;
      margin-bottom: 0.5rem;
      display: block;
    }

    .gift-card h4 {
      font-size: 1rem;
      color: #fff;
      margin-bottom: 0.25rem;
    }

    .gift-card p {
      font-size: 0.8rem;
      color: var(--text-muted);
    }

    /* Gussa Meter */
    .anger-slider-box {
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid var(--card-border);
      border-radius: 18px;
      padding: 1.5rem;
      margin-bottom: 1.5rem;
    }

    .slider-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 1rem;
    }

    .slider-header span {
      font-size: 0.95rem;
      font-weight: 600;
    }

    .slider-level {
      color: var(--gold);
      font-weight: 700;
      font-size: 1.1rem;
    }

    input[type=range] {
      width: 100%;
      height: 6px;
      background: rgba(255, 255, 255, 0.2);
      border-radius: 10px;
      outline: none;
      -webkit-appearance: none;
    }

    input[type=range]::-webkit-slider-thumb {
      -webkit-appearance: none;
      width: 22px;
      height: 22px;
      border-radius: 50%;
      background: var(--gold);
      cursor: pointer;
      box-shadow: 0 0 10px rgba(243, 198, 119, 0.7);
    }

    .reaction-text {
      margin-top: 1rem;
      font-family: var(--font-hand);
      font-size: 1.35rem;
      color: var(--rose);
      min-height: 42px;
    }

    /* Modals */
    .modal-backdrop {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(8, 10, 15, 0.88);
      backdrop-filter: blur(8px);
      z-index: 100;
      display: none;
      justify-content: center;
      align-items: center;
      padding: 1.5rem;
    }

    .modal-content {
      max-width: 520px;
      width: 100%;
      background: #171b26;
      border: 1px solid var(--gold);
      border-radius: 22px;
      padding: 2.2rem;
      position: relative;
      max-height: 85vh;
      overflow-y: auto;
      text-align: left;
    }

    .modal-close {
      position: absolute;
      top: 1rem;
      right: 1.2rem;
      background: none;
      border: none;
      color: var(--text-muted);
      font-size: 1.6rem;
      cursor: pointer;
    }

    .modal-content h3 {
      font-family: var(--font-serif);
      font-size: 1.8rem;
      color: var(--gold);
      margin-bottom: 1rem;
    }

    .letter-body {
      font-size: 0.95rem;
      color: #d1d5db;
      line-height: 1.7;
    }

    .letter-body p {
      margin-bottom: 1rem;
    }

    .coupon-card {
      border: 2px dashed var(--gold);
      border-radius: 14px;
      padding: 1.5rem;
      text-align: center;
      background: rgba(243, 198, 119, 0.06);
      margin-top: 1rem;
    }

    .coupon-card h4 {
      font-size: 1.25rem;
      color: #fff;
      margin-bottom: 0.3rem;
    }

    @media (max-width: 580px) {
      .main-wrapper { padding: 2rem 1.2rem; }
      .gifts-grid { grid-template-columns: 1fr; }
      .title { font-size: 1.9rem; }
    }
  </style>
</head>
<body>

  <canvas class="sparkle-canvas" id="canvas"></canvas>

  <div class="main-wrapper">
    <div class="audio-pill" id="audioBtn">
      <span id="audioIcon">🎵</span> <span id="audioLabel">Play Soft Tune</span>
    </div>

    <!-- STAGE 1: CLOSED BOX -->
    <div class="gift-stage" id="stage1">
      <div class="subtitle">For Teena Ji</div>
      <h1 class="title">I Am Truly Sorry, Meri Jaan</h1>
      <p class="desc">
        Maine aapse theek se baat nahi ki aur aapka dil dukhaya. Ye virtual gift meri sincere maafi aur aapko khush dekhne ki ek choti si koshish hai.
      </p>

      <div class="box-container" id="boxClickable">
        <div class="gift-box-base">
          <div class="gift-ribbon-v"></div>
          <div class="gift-ribbon-h"></div>
        </div>
        <div class="gift-lid" id="giftLid">
          <div class="gift-ribbon-v" style="left: 55px; height: 100%;"></div>
          <div class="gift-bow"></div>
        </div>
      </div>

      <button class="open-btn" id="openBtn">OPEN YOUR GIFT 🎁</button>
    </div>

    <!-- STAGE 2: UNBOXED DASHBOARD -->
    <div class="unboxed-stage" id="stage2">
      <div class="greet-badge">Apology & Comfort Pack</div>
      <h2>For Teena Ji — Meri Jaan</h2>
      <p class="unboxed-sub">Aapki narazgi 100% justified hai. Ye 4 chote gifts bas aapke chehre par wapas sukoon laane ke liye hain:</p>

      <div class="gifts-grid">
        <div class="gift-card" id="cardTeddy">
          <span class="icon">🧸</span>
          <h4>The Forgiveness Bear</h4>
          <p>Tap karein ek pyare virtual hug ke liye</p>
        </div>

        <div class="gift-card" id="cardLetter">
          <span class="icon">💌</span>
          <h4>Heartfelt Apology Letter</h4>
          <p>Bina kisi excuse ke meri sachai padhein</p>
        </div>

        <div class="gift-card" id="cardPriority">
          <span class="icon">🌸</span>
          <h4>Priority Cards</h4>
          <p>Kyun aap mere liye hamesha #1 hain</p>
        </div>

        <div class="gift-card" id="cardCoupon">
          <span class="icon">🎟️</span>
          <h4>Lifetime Peace Pass</h4>
          <p>Aapka unconditional pampering ticket</p>
        </div>
      </div>

      <!-- Gussa Meter -->
      <div class="anger-slider-box">
        <div class="slider-header">
          <span>Aapka Gussa Meter 💔</span>
          <span class="slider-level" id="sliderVal">100%</span>
        </div>
        <input type="range" id="angerRange" min="0" max="100" value="100">
        <div class="reaction-text" id="reactionMsg">
          "Aapka 100% naraz hona bilkul sahi hai... Main tab tak wait karunga jab tak aap normal feel na karein."
        </div>
      </div>

      <p style="text-align: center; font-size: 0.85rem; color: var(--text-muted);">
        Take all the time you need, Teena ji. Main yahin hoon, hamesha.
      </p>
    </div>
  </div>

  <!-- MODALS -->
  <div class="modal-backdrop" id="modalTeddy">
    <div class="modal-content" style="text-align:center;">
      <button class="modal-close" data-close="modalTeddy">&times;</button>
      <div style="font-size: 4.5rem; margin-bottom: 0.5rem;" id="bearEmoji">🧸</div>
      <h3>Warmest Hug For You</h3>
      <p style="color: #cbd5e1; font-size: 1rem; line-height: 1.6; margin-bottom: 1.5rem;">
        "I know meri laparwahi se aapke aansu aaye hain. Agar main wahan hota toh bas bina kuch bole aapko gale laga leta jab tak aapka mann shant na ho jata."
      </p>
      <button class="open-btn" style="padding: 0.7rem 1.8rem;" id="squeezeBearBtn">Squeeze Bear 🤗</button>
    </div>
  </div>

  <div class="modal-backdrop" id="modalLetter">
    <div class="modal-content">
      <button class="modal-close" data-close="modalLetter">&times;</button>
      <h3>Teena Ji, Meri Jaan...</h3>
      <div class="letter-body">
        <p>Main koi bahana nahi banaunga. Chaar baar aapko second choice feel karwana meri taraf se ek bahut badi na-samjhi aur laparwahi thi.</p>
        <p>Aap meri partner hain, aapko mujhse importance ya waqt maangne ki zarurat nahi honi chahiye. Wo aapka pehla haq tha jo maine cheena. Kisi aur rishte ya situation ke peeche main apni is galti ko nahi chhipaunga.</p>
        <p>Main aapse ye nahi keh raha ki turant sab bhool kar maaf kar dijiye. Main bas ye promise karta hoon ki aage se mere actions aapko batayenge ki aap mere liye sabse upar hain.</p>
      </div>
    </div>
  </div>

  <div class="modal-backdrop" id="modalPriority">
    <div class="modal-content" style="text-align: center;">
      <button class="modal-close" data-close="modalPriority">&times;</button>
      <h3>Why You Are Priority #1</h3>
      <div id="priorityCardContent" style="padding: 1.5rem; background: rgba(255,255,255,0.04); border-radius: 12px; margin: 1.2rem 0; font-size: 1.05rem; color: var(--gold);">
        "Aapki ek smile mere poore din ka sukoon hai, aur aapko rulaana meri sabse badi haar."
      </div>
      <button class="open-btn" style="padding: 0.6rem 1.4rem; font-size: 0.85rem;" id="nextPriorityBtn">Next Reason 💖</button>
    </div>
  </div>

  <div class="modal-backdrop" id="modalCoupon">
    <div class="modal-content" style="text-align: center;">
      <button class="modal-close" data-close="modalCoupon">&times;</button>
      <h3>A Special Peace Treaty</h3>
      <div class="coupon-card">
        <h4>ROYAL PAMPERING TICKET 🎟️</h4>
        <p style="font-size: 0.9rem; color: var(--gold); margin: 0.6rem 0;">Valid For: Teena Ji</p>
        <p style="font-size: 0.82rem; color: #cbd5e1; line-height: 1.6;">
          • Unlimited listening without any interruptions<br>
          • 100% priority in all phone calls & chats<br>
          • No expiry date — Redeemable whenever you're ready
        </p>
      </div>
      <p style="margin-top: 1.2rem; font-size: 0.85rem; color: var(--text-muted);">
        Signed from the bottom of my heart.
      </p>
    </div>
  </div>

  <script>
    // Pure Vanilla Confetti (Zero External CDN Dependency)
    function launchConfetti() {
      const colors = ['#f3c677', '#f28b9f', '#ffffff', '#e56586'];
      for (let i = 0; i < 60; i++) {
        const particle = document.createElement('div');
        particle.style.position = 'fixed';
        particle.style.left = Math.random() * window.innerWidth + 'px';
        particle.style.top = (window.innerHeight * 0.6) + 'px';
        particle.style.width = (Math.random() * 8 + 6) + 'px';
        particle.style.height = (Math.random() * 8 + 6) + 'px';
        particle.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
        particle.style.borderRadius = Math.random() > 0.5 ? '50%' : '2px';
        particle.style.zIndex = '999';
        particle.style.pointerEvents = 'none';
        particle.style.transition = 'all 1.4s cubic-bezier(0.25, 1, 0.5, 1)';
        document.body.appendChild(particle);

        const destX = (Math.random() - 0.5) * 400;
        const destY = -Math.random() * 350 - 50;

        requestAnimationFrame(() => {
          particle.style.transform = `translate(${destX}px, ${destY}px) rotate(${Math.random() * 720}deg)`;
          particle.style.opacity = '0';
        });

        setTimeout(() => particle.remove(), 1500);
      }
    }

    // Unboxing Action
    let opened = false;
    function openGift() {
      if (opened) return;
      opened = true;

      const lid = document.getElementById('giftLid');
      if (lid) lid.style.transform = "translateY(-50px) rotate(-20deg)";

      launchConfetti();

      // Safe Audio trigger
      try { playSoftTune(); } catch(e) {}

      setTimeout(() => {
        const s1 = document.getElementById('stage1');
        const s2 = document.getElementById('stage2');
        if (s1) s1.style.display = 'none';
        if (s2) {
          s2.style.display = 'block';
          setTimeout(() => { s2.style.opacity = '1'; }, 40);
        }
      }, 550);
    }

    // Attach Event Listeners Directly
    document.getElementById('openBtn').addEventListener('click', openGift);
    document.getElementById('boxClickable').addEventListener('click', openGift);

    // Modal Control
    function showModal(id) {
      const el = document.getElementById(id);
      if (el) el.style.display = 'flex';
    }
    function hideModal(id) {
      const el = document.getElementById(id);
      if (el) el.style.display = 'none';
    }

    document.getElementById('cardTeddy').addEventListener('click', () => showModal('modalTeddy'));
    document.getElementById('cardLetter').addEventListener('click', () => showModal('modalLetter'));
    document.getElementById('cardPriority').addEventListener('click', () => showModal('modalPriority'));
    document.getElementById('cardCoupon').addEventListener('click', () => showModal('modalCoupon'));

    document.querySelectorAll('.modal-close').forEach(btn => {
      btn.addEventListener('click', (e) => {
        hideModal(e.target.getAttribute('data-close'));
      });
    });

    document.querySelectorAll('.modal-backdrop').forEach(bg => {
      bg.addEventListener('click', (e) => {
        if (e.target === bg) bg.style.display = 'none';
      });
    });

    // Bear Squeeze
    document.getElementById('squeezeBearBtn').addEventListener('click', () => {
      const bear = document.getElementById('bearEmoji');
      bear.textContent = "🥰";
      launchConfetti();
      setTimeout(() => { bear.textContent = "🧸"; }, 1500);
    });

    // Priority Cards Cycling
    const reasons = [
      "Aapki ek smile mere poore din ka sukoon hai, aur aapko rulaana meri sabse badi haar.",
      "Aapne hamesha mera saath diya, jabki mujhe aapko protect aur support karna chahiye tha.",
      "Aap meri life ka wo hissa hain jise main kisi bhi keemat par khona nahi chahta.",
      "Aapki izzat aur aapka dhyan rakhna meri sabse pehli zimmedari hai."
    ];
    let rIdx = 0;
    document.getElementById('nextPriorityBtn').addEventListener('click', () => {
      rIdx = (rIdx + 1) % reasons.length;
      document.getElementById('priorityCardContent').textContent = `"${reasons[rIdx]}"`;
    });

    // Gussa Meter
    document.getElementById('angerRange').addEventListener('input', (e) => {
      const val = e.target.value;
      document.getElementById('sliderVal').textContent = val + "%";
      const msg = document.getElementById('reactionMsg');
      if (val > 80) {
        msg.textCon
