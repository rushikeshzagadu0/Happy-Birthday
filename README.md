<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Peacemaker 💖</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Caveat:wght@600;700&family=Playfair+Display:ital,wght@0,600;0,800;1,400&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --accent-pink: #ec4899;
            --accent-purple: #8b5cf6;
            --accent-gold: #f59e0b;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background: #0f172a;
            color: #f8fafc;
            min-height: 100vh;
            overflow-x: hidden;
            margin: 0;
            user-select: none;
        }

        .font-serif-title {
            font-family: 'Playfair Display', serif;
        }

        .font-handwriting {
            font-family: 'Caveat', cursive;
        }

        /* Glassmorphism utility */
        .glass-card {
            background: rgba(255, 255, 255, 0.07);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.12);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.3);
        }

        .glass-modal {
            background: rgba(15, 23, 42, 0.85);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(244, 114, 182, 0.2);
        }

        /* Ambient Glowing Background Orbs */
        .orb {
            position: absolute;
            border-radius: 50%;
            filter: blur(80px);
            opacity: 0.5;
            pointer-events: none;
            animation: floatOrb 12s ease-in-out infinite alternate;
        }

        @keyframes floatOrb {
            0% { transform: translate(0, 0) scale(1); }
            50% { transform: translate(60px, -40px) scale(1.15); }
            100% { transform: translate(-40px, 50px) scale(0.9); }
        }

        /* 3D Envelope Container & Folding Mechanics */
        .env-3d-wrapper {
            perspective: 1200px;
            cursor: pointer;
        }

        .envelope-body {
            position: relative;
            width: 320px;
            height: 220px;
            background: linear-gradient(135deg, #be185d, #9d174d);
            border-radius: 0 0 16px 16px;
            box-shadow: 0 25px 50px -12px rgba(225, 29, 72, 0.35);
            transition: transform 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        @media (min-width: 640px) {
            .envelope-body {
                width: 440px;
                height: 290px;
            }
        }

        .envelope-body:hover {
            transform: translateY(-8px) rotateX(4deg);
        }

        /* Envelope Flap 3D rotation */
        .envelope-flap {
            position: absolute;
            top: 0;
            left: 0;
            width: 0;
            height: 0;
            border-left: 160px solid transparent;
            border-right: 160px solid transparent;
            border-top: 135px solid #e11d48;
            transform-origin: top center;
            transition: transform 0.7s cubic-bezier(0.4, 0, 0.2, 1);
            z-index: 5;
            filter: drop-shadow(0 6px 8px rgba(0,0,0,0.2));
        }

        @media (min-width: 640px) {
            .envelope-flap {
                border-left-width: 220px;
                border-right-width: 220px;
                border-top-width: 175px;
            }
        }

        .envelope-body.open .envelope-flap {
            transform: rotateX(180deg);
            z-index: 1;
        }

        /* Envelope Inner Pocket Walls */
        .pocket-side-left {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 0;
            border-left: 160px solid #f43f5e;
            border-top: 110px solid transparent;
            border-bottom: 110px solid #f43f5e;
            border-bottom-left-radius: 16px;
            z-index: 4;
        }

        .pocket-side-right {
            position: absolute;
            bottom: 0;
            right: 0;
            width: 0;
            height: 0;
            border-right: 160px solid #f43f5e;
            border-top: 110px solid transparent;
            border-bottom: 110px solid #f43f5e;
            border-bottom-right-radius: 16px;
            z-index: 4;
        }

        .pocket-bottom-lip {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 0;
            border-left: 160px solid transparent;
            border-right: 160px solid transparent;
            border-bottom: 125px solid #e11d48;
            border-bottom-left-radius: 16px;
            border-bottom-right-radius: 16px;
            z-index: 4;
        }

        @media (min-width: 640px) {
            .pocket-side-left {
                border-left-width: 220px;
                border-top-width: 145px;
                border-bottom-width: 145px;
            }
            .pocket-side-right {
                border-right-width: 220px;
                border-top-width: 145px;
                border-bottom-width: 145px;
            }
            .pocket-bottom-lip {
                border-left-width: 220px;
                border-right-width: 220px;
                border-bottom-width: 165px;
            }
        }

        /* Golden Wax Stamp Seal */
        .wax-seal-badge {
            position: absolute;
            top: 120px;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 56px;
            height: 56px;
            background: radial-gradient(circle at 30% 30%, #fef08a, #d97706);
            border-radius: 50%;
            z-index: 6;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.4), inset 0 2px 4px rgba(255, 255, 255, 0.6);
            color: #78350f;
            font-size: 20px;
            transition: transform 0.5s ease, opacity 0.4s ease;
        }

        @media (min-width: 640px) {
            .wax-seal-badge {
                top: 155px;
                width: 64px;
                height: 64px;
                font-size: 24px;
            }
        }

        .envelope-body.open .wax-seal-badge {
            opacity: 0;
            transform: translate(-50%, -50%) scale(0.2);
            pointer-events: none;
        }

        /* Sliding Folded Letter inside Envelope */
        .nested-letter {
            position: absolute;
            bottom: 12px;
            left: 5%;
            width: 90%;
            height: 88%;
            background: #fffdfa;
            border-radius: 12px;
            z-index: 3;
            transition: transform 0.8s cubic-bezier(0.34, 1.4, 0.64, 1);
            box-shadow: 0 -4px 15px rgba(0,0,0,0.15);
            padding: 16px;
            color: #1e293b;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
        }

        .envelope-body.open .nested-letter {
            transform: translateY(-145px) scale(1.04);
            z-index: 5;
        }

        @media (min-width: 640px) {
            .envelope-body.open .nested-letter {
                transform: translateY(-180px) scale(1.04);
            }
        }

        /* Cake Candle Animations */
        @keyframes flameWiggle {
            0%, 100% { transform: rotate(-2deg) scale(1); }
            50% { transform: rotate(3deg) scale(1.1); }
        }
        .flame-active {
            animation: flameWiggle 0.15s infinite ease-in-out alternate;
        }
    </style>
</head>
<body class="flex flex-col min-h-screen justify-between items-center relative px-4 py-6 overflow-x-hidden">

    <div class="orb bg-pink-600/40 w-80 h-80 top-10 -left-20"></div>
    <div class="orb bg-purple-600/30 w-96 h-96 bottom-10 -right-20"></div>
    <div class="orb bg-amber-500/20 w-72 h-72 top-1/2 left-1/3"></div>

    <!-- Canvas for Floating Particle Effects & Confetti -->
    <canvas id="fxCanvas" class="fixed inset-0 pointer-events-none z-30"></canvas>

    <!-- Top Navigation Header -->
    <header class="w-full max-w-4xl flex justify-between items-center z-20 py-2">
        <div class="flex items-center gap-3 glass-card px-4 py-2 rounded-full">
            <span class="text-pink-400 text-lg"><i class="fa-solid fa-crown"></i></span>
            <span class="font-semibold text-xs sm:text-sm tracking-wider uppercase text-pink-200">Peacemaker's Birthday</span>
        </div>

        <div class="flex items-center gap-2">
            <!-- Music Synthesizer Toggle -->
            <button id="musicToggleBtn" class="glass-card hover:bg-white/10 text-white px-4 py-2 rounded-full transition flex items-center gap-2 text-xs sm:text-sm font-medium border border-pink-500/30">
                <i class="fa-solid fa-music text-pink-400" id="musicIcon"></i>
                <span id="musicText">Play Music</span>
            </button>

            <!-- Shower Celebratory FX Button -->
            <button id="burstFxBtn" class="bg-gradient-to-r from-pink-500 to-rose-500 hover:from-pink-600 hover:to-rose-600 text-white px-4 py-2 rounded-full shadow-lg transition flex items-center gap-2 text-xs sm:text-sm font-semibold hover:scale-105 active:scale-95">
                <i class="fa-solid fa-sparkles"></i>
                <span class="hidden sm:inline">Celebrate</span>
            </button>
        </div>
    </header>

    <main class="w-full max-w-2xl flex flex-col items-center justify-center my-auto z-20 text-center py-6">
        
        <div class="mb-8 space-y-2">
            <span class="inline-block px-3 py-1 rounded-full bg-rose-500/20 text-rose-300 font-semibold text-xs tracking-widest uppercase border border-rose-500/30">
                Exclusive Invitation
            </span>
            <h1 class="text-4xl sm:text-6xl font-bold font-serif-title bg-gradient-to-r from-pink-200 via-rose-300 to-amber-200 bg-clip-text text-transparent">
                A Message From The Heart
            </h1>
            <p class="text-slate-400 text-sm sm:text-base flex items-center justify-center gap-2">
                <span>Tap the envelope to unseal your birthday card</span>
                <i class="fa-solid fa-hand-pointer text-pink-400 animate-bounce"></i>
            </p>
        </div>

        <!-- 3D Envelope Wrapper -->
        <div class="env-3d-wrapper my-6" id="envWrapper">
            <div class="envelope-body" id="envelopeObj">
                <div class="envelope-flap"></div>
                <div class="pocket-side-left"></div>
                <div class="pocket-side-right"></div>
                <div class="pocket-bottom-lip"></div>

                <!-- Gold Wax Stamp Seal -->
                <div class="wax-seal-badge">
                    <i class="fa-solid fa-heart"></i>
                </div>

                <!-- Folded Letter Preview inside Envelope -->
                <div class="nested-letter">
                    <i class="fa-solid fa-gem text-rose-500 text-2xl mb-1"></i>
                    <h3 class="font-serif-title text-xl font-bold text-rose-600">Happy Birthday</h3>
                    <p class="text-xs text-slate-500 mt-1 italic">Click to read message</p>
                </div>
            </div>
        </div>

        <p class="text-xs text-slate-500 mt-8 tracking-widest uppercase flex items-center gap-2">
            <i class="fa-regular fa-envelope"></i> Interactive Touch Envelope
        </p>
    </main>

    <!-- Full Letter Glass Overlay Modal -->
    <div id="letterModal" class="fixed inset-0 bg-slate-950/80 backdrop-blur-xl flex items-center justify-center p-4 opacity-0 pointer-events-none transition-opacity duration-500 z-50">
        <div class="glass-modal w-full max-w-lg rounded-3xl p-6 sm:p-10 relative text-slate-100 flex flex-col items-center text-center shadow-2xl transform scale-90 transition-transform duration-500" id="modalCard">
            
            <!-- Close Modal Button -->
            <button id="closeModalBtn" class="absolute top-4 right-4 w-10 h-10 bg-white/10 hover:bg-white/20 rounded-full flex items-center justify-center transition text-slate-300">
                <i class="fa-solid fa-xmark text-lg"></i>
            </button>

            <!-- Decorative Floating Icon -->
            <div class="w-16 h-16 rounded-full bg-gradient-to-tr from-rose-500 to-amber-400 p-0.5 shadow-lg mb-4">
                <div class="w-full h-full bg-slate-900 rounded-full flex items-center justify-center">
                    <i class="fa-solid fa-sparkles text-2xl text-amber-300"></i>
                </div>
            </div>

            <!-- Card Heading -->
            <h2 class="font-serif-title text-3xl sm:text-4xl font-bold bg-gradient-to-r from-pink-300 via-rose-300 to-amber-200 bg-clip-text text-transparent">
                Happy Birthday!
            </h2>

            <div class="w-20 h-0.5 bg-gradient-to-r from-transparent via-rose-400 to-transparent my-4"></div>

            <!-- Exact Requested Sentences -->
            <div class="space-y-4 my-2">
                <p class="font-handwriting text-3xl sm:text-4xl text-pink-300 font-bold leading-relaxed tracking-wide">
                    "Happy Birthday to you my Peacemaker 💖"
                </p>
                <p class="font-handwriting text-2xl sm:text-3xl text-slate-200 leading-relaxed px-2">
                    "Lots of Love to you Stay Happy, Stay Blessed. I'm so grateful to have you in my life"
                </p>
            </div>

            <!-- Interactive Cake & Flame Section -->
            <div class="my-6 p-4 rounded-2xl bg-white/5 border border-white/10 w-full flex flex-col items-center relative overflow-hidden">
                <div class="relative flex flex-col items-center">
                    <!-- Candle Flame -->
                    <div id="candleFlame" class="w-4 h-6 bg-gradient-to-t from-amber-500 via-yellow-300 to-amber-100 rounded-full flame-active shadow-[0_0_15px_#f59e0b] mb-1"></div>
                    <!-- Cake SVG / Emoji -->
                    <div class="text-4xl">🎂</div>
                </div>
                <p id="wishMsg" class="text-xs text-rose-300 mt-2 font-medium">Make a wish and blow out the candle!</p>
            </div>

            <!-- Interactive Action Controls inside Card -->
            <div class="flex gap-3 w-full mt-2">
                <button id="blowCandleBtn" class="flex-1 bg-gradient-to-r from-amber-500 to-amber-600 hover:from-amber-600 hover:to-amber-700 text-white font-semibold py-3 px-4 rounded-2xl shadow-lg transition text-xs sm:text-sm flex items-center justify-center gap-2">
                    <i class="fa-solid fa-wind"></i>
                    <span>Blow Candle</span>
                </button>

                <button id="giftShowerBtn" class="flex-1 bg-gradient-to-r from-rose-500 to-pink-600 hover:from-rose-600 hover:to-pink-700 text-white font-semibold py-3 px-4 rounded-2xl shadow-lg transition text-xs sm:text-sm flex items-center justify-center gap-2">
                    <i class="fa-solid fa-gift"></i>
                    <span>Shower Gifts</span>
                </button>
            </div>

        </div>
    </div>

    <!-- Footer -->
    <footer class="w-full text-center text-xs text-slate-500 z-20 py-2">
        <p>Crafted with ❤️ for a truly special birthday celebration</p>
    </footer>

    <script>
        /* Web Audio API Music & Sound Synthesizer */
        class BirthdayAudioEngine {
            constructor() {
                this.ctx = null;
                this.isPlaying = false;
                this.timers = [];
            }

            initCtx() {
                if (!this.ctx) {
                    const AudioCtx = window.AudioContext || window.webkitAudioContext;
                    this.ctx = new AudioCtx();
                }
            }

            playFreq(freq, type = 'sine', duration = 0.3, delay = 0) {
                if (!this.ctx) return;
                const t = setTimeout(() => {
                    try {
                        const osc = this.ctx.createOscillator();
                        const gain = this.ctx.createGain();
                        osc.type = type;
                        osc.frequency.setValueAtTime(freq, this.ctx.currentTime);

                        gain.gain.setValueAtTime(0.12, this.ctx.currentTime);
                        gain.gain.exponentialRampToValueAtTime(0.0001, this.ctx.currentTime + duration);

                        osc.connect(gain);
                        gain.connect(this.ctx.destination);

                        osc.start();
                        osc.stop(this.ctx.currentTime + duration);
                    } catch(e) {}
                }, delay * 1000);
                this.timers.push(t);
            }

            playPop() {
                this.initCtx();
                this.playFreq(350, 'sine', 0.08);
                this.playFreq(700, 'triangle', 0.12, 0.04);
            }

            playSparkle() {
                this.initCtx();
                const freqs = [523.25, 659.25, 783.99, 1046.50, 1318.51];
                freqs.forEach((f, i) => this.playFreq(f, 'sine', 0.25, i * 0.05));
            }

            playBirthdayMelody() {
                this.initCtx();
                if (this.isPlaying) return;
                this.isPlaying = true;

                // Happy Birthday Song Sheet (Note Frequencies & Durations)
                const melody = [
                    {f: 264, d: 0.3}, {f: 264, d: 0.3}, {f: 297, d: 0.6}, {f: 264, d: 0.6}, {f: 352, d: 0.6}, {f: 330, d: 1.0},
                    {f: 264, d: 0.3}, {f: 264, d: 0.3}, {f: 297, d: 0.6}, {f: 264, d: 0.6}, {f: 396, d: 0.6}, {f: 352, d: 1.0},
                    {f: 264, d: 0.3}, {f: 264, d: 0.3}, {f: 528, d: 0.6}, {f: 440, d: 0.6}, {f: 352, d: 0.6}, {f: 330, d: 0.6}, {f: 297, d: 0.8},
                    {f: 466, d: 0.3}, {f: 466, d: 0.3}, {f: 440, d: 0.6}, {f: 352, d: 0.6}, {f: 396, d: 0.6}, {f: 352, d: 1.2}
                ];

                const loopMelody = () => {
                    if (!this.isPlaying) return;
                    let offset = 0;
                    melody.forEach(note => {
                        this.playFreq(note.f, 'triangle', note.d, offset);
                        offset += note.d + 0.08;
                    });
                    this.loopTimer = setTimeout(() => {
                        if (this.isPlaying) loopMelody();
                    }, offset * 1000 + 800);
                };

                loopMelody();
            }

            stopMelody() {
                this.isPlaying = false;
                if (this.loopTimer) clearTimeout(this.loopTimer);
                this.timers.forEach(t => clearTimeout(t));
                this.timers = [];
            }
        }

        const audioEngine = new BirthdayAudioEngine();

        /* Particle Canvas System (Confetti & Floating Balloons) */
        const fxCanvas = document.getElementById('fxCanvas');
        const fxCtx = fxCanvas.getContext('2d');
        let particles = [];
        let balloons = [];

        function resizeFxCanvas() {
            fxCanvas.width = window.innerWidth;
            fxCanvas.height = window.innerHeight;
        }
        window.addEventListener('resize', resizeFxCanvas);
        resizeFxCanvas();

        class ConfettiPiece {
            constructor(x, y) {
                this.x = x;
                this.y = y;
                this.size = Math.random() * 8 + 4;
                this.vx = (Math.random() - 0.5) * 14;
                this.vy = (Math.random() - 1) * 14 - 4;
                this.gravity = 0.22;
                this.friction = 0.98;
                this.rotation = Math.random() * 360;
                this.rotSpeed = (Math.random() - 0.5) * 12;
                this.colors = ['#ec4899', '#f59e0b', '#38bdf8', '#a855f7', '#10b981', '#f43f5e'];
                this.color = this.colors[Math.floor(Math.random() * this.colors.length)];
                this.opacity = 1;
            }

            update() {
                this.vx *= this.friction;
                this.vy += this.gravity;
                this.x += this.vx;
                this.y += this.vy;
                this.rotation += this.rotSpeed;
                this.opacity -= 0.007;
            }

            draw(ctx) {
                ctx.save();
                ctx.translate(this.x, this.y);
                ctx.rotate((this.rotation * Math.PI) / 180);
                ctx.globalAlpha = Math.max(0, this.opacity);
                ctx.fillStyle = this.color;
                ctx.fillRect(-this.size / 2, -this.size / 2, this.size, this.size);
                ctx.restore();
            }
        }

        class FloatingBalloon {
            constructor() {
                this.x = Math.random() * fxCanvas.width;
                this.y = fxCanvas.height + 70;
                this.radius = Math.random() * 16 + 22;
                this.speed = Math.random() * 2 + 1.2;
                this.swing = Math.random() * 0.04;
                this.swingAngle = Math.random() * Math.PI * 2;
                this.colors = ['#f43f5e', '#ec4899', '#8b5cf6', '#3b82f6', '#10b981', '#f59e0b'];
                this.color = this.colors[Math.floor(Math.random() * this.colors.length)];
            }

            update() {
                this.y -= this.speed;
                this.swingAngle += this.swing;
                this.x += Math.sin(this.swingAngle) * 0.9;
            }

            draw(ctx) {
                ctx.save();
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                ctx.fillStyle = this.color;
                ctx.fill();

                // Knot & String
                ctx.beginPath();
                ctx.moveTo(this.x - 3, this.y + this.radius);
                ctx.lineTo(this.x + 3, this.y + this.radius);
                ctx.lineTo(this.x, this.y + this.radius + 6);
                ctx.fillStyle = this.color;
                ctx.fill();

                ctx.beginPath();
                ctx.moveTo(this.x, this.y + this.radius + 6);
                ctx.quadraticCurveTo(this.x + 6, this.y + this.radius + 20, this.x - 3, this.y + this.radius + 40);
                ctx.strokeStyle = 'rgba(255,255,255,0.4)';
                ctx.lineWidth = 1.5;
                ctx.stroke();

                // Highlight
                ctx.beginPath();
                ctx.arc(this.x - this.radius * 0.3, this.y - this.radius * 0.3, this.radius * 0.25, 0, Math.PI * 2);
                ctx.fillStyle = 'rgba(255,255,255,0.45)';
                ctx.fill();

                ctx.restore();
            }
        }

        function triggerBurst(x, y) {
            audioEngine.playPop();
            for (let i = 0; i < 70; i++) {
                particles.push(new ConfettiPiece(x, y));
            }
            for (let i = 0; i < 7; i++) {
                balloons.push(new FloatingBalloon());
            }
        }

        function renderFxLoop() {
            fxCtx.clearRect(0, 0, fxCanvas.width, fxCanvas.height);

            for (let i = particles.length - 1; i >= 0; i--) {
                particles[i].update();
                particles[i].draw(fxCtx);
                if (particles[i].opacity <= 0) particles.splice(i, 1);
            }

            for (let i = balloons.length - 1; i >= 0; i--) {
                balloons[i].update();
                balloons[i].draw(fxCtx);
                if (balloons[i].y < -80) balloons.splice(i, 1);
            }

            requestAnimationFrame(renderFxLoop);
        }
        renderFxLoop();

        /* DOM Event Handlers & Envelope Logic */
        const envWrapper = document.getElementById('envWrapper');
        const envelopeObj = document.getElementById('envelopeObj');
        const letterModal = document.getElementById('letterModal');
        const modalCard = document.getElementById('modalCard');
        const closeModalBtn = document.getElementById('closeModalBtn');
        const musicToggleBtn = document.getElementById('musicToggleBtn');
        const musicIcon = document.getElementById('musicIcon');
        const musicText = document.getElementById('musicText');
        const burstFxBtn = document.getElementById('burstFxBtn');
        const blowCandleBtn = document.getElementById('blowCandleBtn');
        const giftShowerBtn = document.getElementById('giftShowerBtn');
        const candleFlame = document.getElementById('candleFlame');
        const wishMsg = document.getElementById('wishMsg');

        let isEnvelopeOpen = false;

        function openEnvelope() {
            if (isEnvelopeOpen) {
                showModal();
                return;
            }

            isEnvelopeOpen = true;
            envelopeObj.classList.add('open');
            audioEngine.playSparkle();

            const rect = envelopeObj.getBoundingClientRect();
            triggerBurst(rect.left + rect.width / 2, rect.top + rect.height / 2);

            setTimeout(() => {
                showModal();
            }, 850);
        }

        function showModal() {
            letterModal.classList.remove('opacity-0', 'pointer-events-none');
            modalCard.classList.remove('scale-90');
            modalCard.classList.add('scale-100');
            audioEngine.playSparkle();
        }

        function closeModal() {
            letterModal.classList.add('opacity-0', 'pointer-events-none');
            modalCard.classList.remove('scale-100');
            modalCard.classList.add('scale-90');
        }

        // Toggle Audio Synthesizer
        musicToggleBtn.addEventListener('click', () => {
            if (audioEngine.isPlaying) {
                audioEngine.stopMelody();
                musicIcon.className = 'fa-solid fa-music text-pink-400';
                musicText.innerText = 'Play Music';
            } else {
                audioEngine.playBirthdayMelody();
                musicIcon.className = 'fa-solid fa-pause text-pink-400';
                musicText.innerText = 'Pause Music';
            }
        });

        // Event Listeners
        envWrapper.addEventListener('click', openEnvelope);
        closeModalBtn.addEventListener('click', closeModal);

        burstFxBtn.addEventListener('click', () => {
            triggerBurst(window.innerWidth / 2, window.innerHeight / 2);
        });

        giftShowerBtn.addEventListener('click', () => {
            triggerBurst(window.innerWidth / 2, window.innerHeight / 3);
        });

        blowCandleBtn.addEventListener('click', () => {
            candleFlame.style.opacity = '0';
            candleFlame.style.transform = 'scale(0)';
            candleFlame.style.transition = 'all 0.6s ease';
            audioEngine.playPop();

            wishMsg.innerText = "✨ Wish granted! May all your dreams come true ✨";
            wishMsg.className = "text-xs text-amber-300 font-semibold mt-2";

            blowCandleBtn.innerHTML = `<i class="fa-solid fa-check"></i> <span>Wish Made!</span>`;
            blowCandleBtn.className = blowCandleBtn.className.replace('from-amber-500 to-amber-600', 'from-emerald-500 to-emerald-600');

            triggerBurst(window.innerWidth / 2, window.innerHeight / 2);
        });

        letterModal.addEventListener('click', (e) => {
            if (e.target === letterModal) closeModal();
        });
    </script>
</body>
</html>
