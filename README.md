<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>For Teena Ji — With All My Heart ❤️</title>
  
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,500;0,700;1,400;1,600&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&family=Caveat:wght@600;700&display=swap" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

  <style>
    :root {
      --bg-dark: #0f1118;
      --card-bg: rgba(26, 30, 43, 0.75);
      --card-border: rgba(243, 198, 119, 0.2);
      --gold: #f3c677;
      --gold-hover: #e5b35c;
      --rose: #f28b9f;
      --rose-soft: rgba(242, 139, 159, 0.12);
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

    /* Ambient Floating Sparkles */
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
      backdrop-filter: blur(24px);
      -webkit-backdrop-filter: blur(24px);
      padding: 3rem 2rem;
      box-shadow: 0 30px 80px rgba(0, 0, 0, 0.6);
      position: relative;
      z-index: 1;
      text-align: center;
    }

    /* Top Audio Controller */
    .audio-pill {
      position: absolute;
      top: 1.2rem;
      right: 1.5rem;
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255, 255, 255, 0.1);
      padding: 0.35rem 0.85rem;
      border-radius: 20px;
      font-size: 0.78rem;
      color: var(--gold);
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 6px;
      transition: all 0.3s;
    }
    .audio-pill:hover {
      background: rgba(243, 198, 119, 0.15);
    }

    /* Stage 1: Gift Presentation */
    .gift-stage {
      display: block;
      animation: fadeIn 0.8s ease;
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
      font-size: 2.4rem;
      font-weight: 700;
      margin-bottom: 0.6rem;
      color: #ffffff;
    }

    .desc {
      color: var(--text-muted);
      font-size: 0.96rem;
      margin-bottom: 2.2rem;
      line-height: 1.6;
    }

    /* 3D Animated Gift Box */
    .box-container {
      width: 140px;
      height: 140px;
      margin: 1.5rem auto 2.5rem;
      position: relative;
      cursor: pointer;
      animation: float 3s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
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
      transition: transform 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
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
      padding: 0.9rem 2.4rem;
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
      box-shadow: 0 15px 30px rgba(243, 198, 119, 0.45);
    }

    /* Stage 2: Dashboard Content */
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
      font-size: 2.2rem;
      color: #fff;
      line-height: 1.2;
      margin-bottom: 0.4rem;
    }

    .unboxed-sub {
      color: var(--text-muted);
      font-size: 0.95rem;
      margin-bottom: 2rem;
    }

    /* 4 Interactive Gifts Grid */
    .gifts-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 1rem;
      margin-bottom: 2.5rem;
    }

    .gift-card {
      background: rgba(255, 255, 255, 0.04);
      border: 1px solid rgba(255, 255, 255, 0.07);
      border-radius: 16px;
      padding: 1.25rem 1rem;
      text-align: center;
      cursor: pointer;
      transition: all 0.3s;
    }

    .gift-card:hover {
      background: rgba(243, 198, 119, 0.08);
      border-color: rgba(243, 198, 119, 0.4);
      transform: translateY(-4px);
    }

    .gift-card .icon {
      font-size: 2rem;
      margin-bottom: 0.5rem;
      display: block;
    }

    .gift-card h4 {
      font-size: 1rem;
      color: #fff;
      margin-bottom: 0.25rem;
    }

    .gift-card p {
      font-size: 0.78rem;
      color: var(--text-muted);
    }

    /* Gussa Meter Section */
    .anger-slider-box {
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid var(--card-border);
      border-radius: 18px;
      padding: 1.5rem;
      margin-bottom: 2rem;
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
      background: rgba(255, 255, 255, 0.15);
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
      min-height: 40px;
    }

    /* Modals for Gifts */
    .modal-backdrop {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(8, 10, 15, 0.85);
      backdrop-filter: blur(8px);
      z-index: 99;
      display: none;
      justify-content: center;
      align-items: center;
      padding: 1.5rem;
    }

    .modal-content {
      max-width: 540px;
      width: 100%;
      background: #171b26;
      border: 1px solid var(--gold);
      border-radius: 22px;
      padding: 2.2rem;
      position: relative;
      animation: modalPop 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      max-height: 85vh;
      overflow-y: auto;
    }

    @keyframes modalPop {
      from { transform: scale(0.9); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }

    .modal-close {
      position: absolute;
      top: 1rem;
      right: 1.2rem;
      background: none;
      border: none;
      color: var(--text-muted);
      font-size: 1.5rem;
      cursor: pointer;
    }

    .modal-content h3 {
      font-family: var(--font-serif);
      font-size: 1.9rem;
      color: var(--gold);
      margin-bottom: 1rem;
    }

    .letter-body {
      font-size: 0.95rem;
      color: #d1d5db;
      line-height: 1.7;
      text-align: left;
    }

    .letter-body p {
      margin-bottom: 1rem;
    }

    .coupon-card {
      border: 2px dashed var(--gold);
      border-radius: 14px;
      padding: 1.5rem;
      text-align: center;
      background: rgba(243, 198, 119, 0.05);
      margin-top: 1rem;
    }

    .coupon-card h4 {
      font-size: 1.3rem;
      color: #fff;
      margin-bottom: 0.3rem;
    }

    @media (max-width: 580px) {
      .main-wrapper { padding: 2.2rem 1.4rem; }
      .gifts-grid { grid-template-columns: 1fr; }
      .title { font-size: 2rem; }
    }
  </style>
</head>
<body>

  <canvas class="sparkle-canvas" id="canvas"></canvas>

  <div class="main-wrapper">
    <!-- Ambient Melodic Audio Trigger -->
    <div class="audio-pill" onclick="toggleAudio()" id="audioBtn">
      <span id="audioIcon">🎵</span> <span id="audioLabel">Play Soft Tune</span>
    </div>

    <!-- STAGE 1: CLOSED GIFT -->
    <div class="gift-stage" id="stage1">
      <div class="subtitle">For Teena Ji</div>
      <h1 class="title">I Am Truly Sorry, Meri Jaan</h1>
      <p class="desc">
        Maine aapse theek se baat nahi ki aur aapka dil dukhaya. Ye virtual gift meri sincere maafi aur aapko khush dekhne ki ek choti si koshish hai.
      </p>

      <div class="box-container" onclick="openGift()">
        <div class="gift-box-base">
          <div class="gift-ribbon-v"></div>
          <div class="gift-ribbon-h"></div>
        </div>
        <div class="gift-lid" id="giftLid">
          <div class="gift-ribbon-v" style="left: 55px; height: 100%;"></div>
          <div class="gift-bow"></div>
        </div>
      </div>

      <button class="open-btn" onclick="openGift()">OPEN YOUR GIFT 🎁</button>
    </div>

    <!-- STAGE 2: UNBOXED DASHBOARD -->
    <div class="unboxed-stage" id="stage2">
      <div class="greet-badge">Apology & Comfort Pack</div>
      <h2>For Teena Ji — Meri Jaan</h2>
      <p class="unboxed-sub">Aapki narazgi 100% justified hai. Ye 4 chote gifts bas aapke honton par wapas muskan laane ke liye hain:</p>

      <!-- 4 Gifts Grid -->
      <div class="gifts-grid">
        <div class="gift-card" onclick="openModal('modalTeddy')">
          <span class="icon">🧸</span>
          <h4>The Forgiveness Bear</h4>
          <p>Tap karein ek pyare virtual hug ke liye</p>
        </div>

        <div class="gift-card" onclick="openModal('modalLetter')">
          <span class="icon">💌</span>
          <h4>Heartfelt Apology Letter</h4>
          <p>Bina kisi excuse ke meri sachai padhein</p>
        </div>

        <div class="gift-card" onclick="openModal('modalPriority')">
          <span class="icon">🌸</span>
          <h4>Priority Cards</h4>
          <p>Kyun aap mere liye hamesha #1 hain</p>
        </div>

        <div class="gift-card" onclick="openModal('modalCoupon')">
          <span class="icon">🎟️</span>
          <h4>Lifetime Peace Pass</h4>
          <p>Aapka unconditional pampering ticket</p>
        </div>
      </div>

      <!-- Interactive Gussa Meter -->
      <div class="anger-slider-box">
        <div class="slider-header">
          <span>Aapka Gussa Meter 💔</span>
          <span class="slider-level" id="sliderVal">100%</span>
        </div>
        <input type="range" id="angerRange" min="0" max="100" value="100" oninput="updateGussa(this.value)">
        <div class="reaction-text" id="reactionMsg">
          "Aapka 100% gussa hona bilkul sahi hai... Main tab tak wait karunga jab tak aap normal feel na karein."
        </div>
      </div>

      <p style="text-align: center; font-size: 0.85rem; color: var(--text-muted);">
        Take all the time you need, Teena ji. Main yahin hoon, hamesha.
      </p>
    </div>
  </div>

  <!-- MODAL: TEDDY HUG -->
  <div class="modal-backdrop" id="modalTeddy">
    <div class="modal-content" style="text-align:center;">
      <button class="modal-close" onclick="closeModal('modalTeddy')">&times;</button>
      <div style="font-size: 4.5rem; margin-bottom: 0.5rem;" id="bearEmoji">🧸</div>
      <h3>Warmest Hug For You</h3>
      <p style="color: #cbd5e1; font-size: 1rem; line-height: 1.6; margin-bottom: 1.5rem;">
        "I know mere galti se aapke aansu aaye hain. Agar main wahan hota toh bas bina bole aapko gale laga leta jab tak aap theek mehsoos na karti."
      </p>
      <button class="open-btn" style="padding: 0.7rem 1.8rem;" onclick="squeezeBear()">Squeeze Bear 🤗</button>
    </div>
  </div>

  <!-- MODAL: HEARTFELT LETTER -->
  <div class="modal-backdrop" id="modalLetter">
    <div class="modal-content">
      <button class="modal-close" onclick="closeModal('modalLetter')">&times;</button>
      <h3>Teena Ji, Meri Jaan...</h3>
      <div class="letter-body">
        <p>Main koi bahana nahi banaunga. Chaar baar aapko second choice feel karwana meri taraf se ek bahut badi na-samjhi aur laparwahi thi.</p>
        <p>Aap meri partner hain, aapko mujhse importance ya waqt maangne ki zarurat nahi honi chahiye. Wo aapka pehla haq tha jo maine cheena. Kisi aur rishte ya situation ke peeche main apni is galti ko nahi chhipaunga.</p>
        <p>Main aapse ye nahi keh raha ki turant sab bhool kar maaf kar dijiye. Main bas ye promise karta hoon ki aage se mere actions aapko batayenge ki aap mere liye sabse upar hain.</p>
      </div>
    </div>
  </div>

  <!-- MODAL: PRIORITY CARDS -->
  <div class="modal-backdrop" id="modalPriority">
    <div class="modal-content" style="text-align: center;">
      <button class="modal-close" onclick="closeModal('modalPriority')">&times;</button>
      <h3>Why You Are Priority #1</h3>
      <div id="priorityCardContent" style="padding: 1.5rem; background: rgba(255,255,255,0.03); border-radius: 12px; margin: 1.2rem 0; font-size: 1.05rem; color: var(--gold);">
        "Aapki ek smile mere poore din ka sukoon hai, aur aapko rulaana meri sabse badi haar."
      </div>
      <button class="open-btn" style="padding: 0.6rem 1.4rem; font-size: 0.85rem;" onclick="cyclePriority()">Next Reason 💖</button>
    </div>
  </div>

  <!-- MODAL: COUPON -->
  <div class="modal-backdrop" id="modalCoupon">
    <div class="modal-content" style="text-align: center;">
      <button class="modal-close" onclick="closeModal('modalCoupon')">&times;</button>
      <h3>A Special Peace Treaty</h3>
      <div class="coupon-card">
        <h4>ROYAL PAMPERING TICKET 🎟️</h4>
        <p style="font-size: 0.9rem; color: var(--gold); margin: 0.6rem 0;">Valid For: Teena Ji</p>
        <p style="font-size: 0.82rem; color: #cbd5e1; line-height: 1.5;">
          • Unlimited listening without interruptions<br>
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
    /* Unboxing Animation */
    function openGift() {
      const lid = document.getElementById('giftLid');
      lid.style.transform = "translateY(-45px) rotate(-18deg)";
      
      triggerConfetti();
      playSoftTune();

      setTimeout(() => {
        document.getElementById('stage1').style.display = 'none';
        const s2 = document.getElementById('stage2');
        s2.style.display = 'block';
        setTimeout(() => { s2.style.opacity = '1'; }, 50);
      }, 700);
    }

    /* Confetti Particle Burst */
    function triggerConfetti() {
      if (typeof confetti === 'function') {
        confetti({
          particleCount: 70,
          spread: 70,
          origin: { y: 0.6 },
          colors: ['#f3c677', '#f28b9f', '#ffffff']
        });
      }
    }

    /* Modal Navigation */
    function openModal(id) {
      document.getElementById(id).style.display = 'flex';
    }
    function closeModal(id) {
      document.getElementById(id).style.display = 'none';
    }

    /* Squeeze Bear Action */
    function squeezeBear() {
      const bear = document.getElementById('bearEmoji');
      bear.textContent = "🥰";
      triggerConfetti();
      setTimeout(() => { bear.textContent = "🧸"; }, 1500);
    }

    /* Interactive Reasons Cycling */
    const reasons = [
      "Aapki ek smile mere poore din ka sukoon hai, aur aapko rulaana meri sabse badi haar.",
      "Aapne hamesha mera saath diya, jabki mujhe aapko protect aur support karna chahiye tha.",
      "Aap meri life ka wo hissa hain jise main kisi bhi keemat par khona nahi chahta.",
      "Aapki izzat aur aapka dhyan rakhna meri sabse pehli zimmedari hai."
    ];
    let rIdx = 0;
    function cyclePriority() {
      rIdx = (rIdx + 1) % reasons.length;
      document.getElementById('priorityCardContent').textContent = `"${reasons[rIdx]}"`;
    }

    /* Gussa Meter Responses */
    function updateGussa(val) {
      document.getElementById('sliderVal').textContent = val + "%";
      const msg = document.getElementById('reactionMsg');
      if (val > 80) {
        msg.textContent = '"Aapka 100% naraz hona bilkul lazmi hai... Main tab tak intazar karunga jab tak aap theek na hon."';
      } else if (val > 40) {
        msg.textContent = '"Gussa thoda kam hua, lekin main jaanta hoon abhi bhi dil dukha hai. I am here for you."';
      } else if (val > 0) {
        msg.textContent = '"Ek choti si muskan bhi mere liye duniya barabar hai. Thank you for listening to me."';
      } else {
        msg.textContent = '"Agar 0% par aa gaye hain, toh please mujhe ek baar call karke meri awaaz sun lijiye ❤️"';
        triggerConfetti();
      }
    }

    /* Web Audio API Synthesizer (No external sound files required) */
    let audioCtx = null;
    let isPlaying = false;
    let timer = null;

    function playSoftTune() {
      if (isPlaying) return;
      try {
        const AudioContext = window.AudioContext || window.webkitAudioContext;
        audioCtx = new AudioContext();
        isPlaying = true;
        document.getElementById('audioLabel').textContent = "Melody Playing 🎶";

        const notes = [261.63, 329.63, 392.00, 440.00, 392.00, 329.63]; // C - E - G - A - G - E
        let i = 0;

        function playNote() {
          if (!isPlaying) return;
          const osc = audioCtx.createOscillator();
          const gain = audioCtx.createGain();
          osc.type = 'sine';
          osc.frequency.setValueAtTime(notes[i % notes.length], audioCtx.currentTime);

          gain.gain.setValueAtTime(0.001, audioCtx.currentTime);
          
