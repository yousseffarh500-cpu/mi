<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>من يوسف إلى ميرا - رمضان كريم</title>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Cairo', sans-serif;
            background: linear-gradient(145deg, #0b0f2a 0%, #1a1f3a 70%, #2b2f55 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow-x: hidden;
            color: white;
            padding: 20px;
        }

        /* Stars and Moon background */
        .stars, .twinkling, .clouds {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            width: 100%;
            height: 100%;
            display: block;
            pointer-events: none;
        }

        .stars {
            background: #000 url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIzMDAiIGhlaWdodD0iMzAwIj48Y2lyY2xlIGN4PSI2IiBjeT0iMTQiIHI9IjEiIGZpbGw9IndoaXRlIiAvPjxjaXJjbGUgY3g9IjE2MCIgY3k9IjYwIiByPSIxLjUiIGZpbGw9IndoaXRlIiAvPjxjaXJjbGUgY3g9IjQwIiBjeT0iMjAwIiByPSIxLjIiIGZpbGw9IndoaXRlIiAvPjxjaXJjbGUgY3g9IjI4MCIgY3k9IjE4MCIgcj0iMSIgZmlsbD0id2hpdGUiIC8+PGNpcmNsZSBjeD0iMjAwIiBjeT0iMjAiIHI9IjEuOCIgZmlsbD0id2hpdGUiIC8+PC9zdmc+');
            background-repeat: repeat;
            background-size: 300px 300px;
            animation: stars-move 200s linear infinite;
            opacity: 0.8;
        }

        @keyframes stars-move {
            0% { background-position: 0 0; }
            100% { background-position: 300px 300px; }
        }

        .moon {
            position: absolute;
            top: 50px;
            left: 50px;
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background: #f7f0c3;
            box-shadow: 0 0 50px 20px rgba(247, 240, 195, 0.3);
            z-index: 2;
        }

        .moon::before {
            content: "";
            position: absolute;
            top: -10px;
            left: 20px;
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background: linear-gradient(145deg, #0b0f2a 0%, #1a1f3a 70%);
            box-shadow: inset -5px -5px 15px rgba(0,0,0,0.5);
        }

        /* Container */
        .card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            border-radius: 50px;
            padding: 50px 30px;
            max-width: 800px;
            width: 100%;
            text-align: center;
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.5), 0 0 0 2px rgba(255, 215, 0, 0.3) inset;
            border: 1px solid rgba(255, 255, 255, 0.2);
            z-index: 10;
            position: relative;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }

        h1 {
            font-size: 4rem;
            font-weight: 900;
            margin-bottom: 10px;
            text-shadow: 0 0 20px gold, 0 0 40px orange;
            background: linear-gradient(45deg, #ffd700, #f5e56b, #ffb347);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .subtitle {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 30px;
            color: #fff5d6;
            border-bottom: 2px dashed #ffd966;
            padding-bottom: 20px;
            display: inline-block;
        }

        .greeting {
            font-size: 1.6rem;
            margin: 30px 0 20px;
            background: rgba(255, 215, 0, 0.2);
            padding: 20px;
            border-radius: 60px;
            border: 2px solid #ffd966;
            line-height: 1.8;
        }

        .greeting p {
            margin: 10px 0;
        }

        .greeting i {
            color: #ffd966;
            margin: 0 5px;
        }

        /* Fanoos (Lanterns) */
        .lanterns-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
            margin: 40px 0;
        }

        .fanoos {
            width: 120px;
            height: 150px;
            filter: drop-shadow(0 10px 15px rgba(255, 215, 0, 0.6));
            animation: swing 3s infinite alternate ease-in-out;
            transform-origin: top center;
        }

        .fanoos.top {
            animation-delay: 0.5s;
        }

        .fanoos.bottom {
            animation-delay: 1s;
        }

        @keyframes swing {
            0% { transform: rotate(3deg); }
            100% { transform: rotate(-3deg); }
        }

        .fanoos svg {
            width: 100%;
            height: 100%;
        }

        /* Stars and Moon icons decoration */
        .decor-stars {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
            font-size: 2.5rem;
            color: #ffd966;
            text-shadow: 0 0 15px gold;
        }

        .decor-stars span {
            animation: twinkle 2s infinite;
        }

        .decor-stars span:nth-child(2) {
            animation-delay: 0.4s;
        }
        .decor-stars span:nth-child(3) {
            animation-delay: 0.8s;
        }
        .decor-stars span:nth-child(4) {
            animation-delay: 1.2s;
        }
        .decor-stars span:nth-child(5) {
            animation-delay: 1.6s;
        }

        @keyframes twinkle {
            0% { opacity: 1; transform: scale(1); }
            50% { opacity: 0.5; transform: scale(1.2); text-shadow: 0 0 30px gold; }
            100% { opacity: 1; transform: scale(1); }
        }

        .footer-note {
            margin-top: 40px;
            font-size: 1.3rem;
            color: #ffe79e;
            border-top: 1px solid #ffd966;
            padding-top: 25px;
        }

        .footer-note i {
            font-size: 1.8rem;
            vertical-align: middle;
        }

        .signature {
            font-size: 2rem;
            font-weight: bold;
            background: linear-gradient(45deg, #ffb347, #ffd966);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Responsive */
        @media (max-width: 600px) {
            h1 { font-size: 2.8rem; }
            .subtitle { font-size: 1.5rem; }
            .greeting { font-size: 1.2rem; }
        }
    </style>
</head>
<body>
    <!-- Stars background -->
    <div class="stars"></div>
    
    <!-- Moon shape -->
    <div class="moon"></div>

    <!-- Main Card -->
    <div class="card">
        <h1>رمضان كريم</h1>
        <div class="subtitle">من يوسف إلى ميرا</div>

        <!-- Fanoos (Lanterns) SVG -->
        <div class="lanterns-container">
            <!-- فانوس 1 -->
            <div class="fanoos">
                <svg viewBox="0 0 100 150" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <rect x="35" y="20" width="30" height="10" rx="5" fill="#FFD966" />
                    <rect x="30" y="30" width="40" height="70" rx="10" fill="#FFB347" />
                    <rect x="40" y="100" width="20" height="25" rx="10" fill="#FFD966" />
                    <circle cx="50" cy="50" r="10" fill="#FFD700" />
                    <circle cx="50" cy="50" r="5" fill="#FFA500" />
                    <rect x="45" y="125" width="10" height="15" rx="5" fill="#FFB347" />
                    <circle cx="50" cy="70" r="5" fill="#FFD700" />
                </svg>
            </div>
            <!-- فانوس 2 -->
            <div class="fanoos top">
                <svg viewBox="0 0 100 150" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <rect x="35" y="20" width="30" height="10" rx="5" fill="#FFD966" />
                    <rect x="30" y="30" width="40" height="80" rx="15" fill="#FFB347" />
                    <rect x="40" y="110" width="20" height="20" rx="8" fill="#FFD966" />
                    <circle cx="50" cy="60" r="12" fill="#FFD700" />
                    <circle cx="50" cy="60" r="6" fill="#FFA500" />
                    <circle cx="50" cy="85" r="5" fill="#FFD700" />
                    <rect x="45" y="130" width="10" height="15" rx="5" fill="#FFB347" />
                </svg>
            </div>
            <!-- فانوس 3 -->
            <div class="fanoos bottom">
                <svg viewBox="0 0 100 150" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <rect x="35" y="20" width="30" height="10" rx="5" fill="#FFD966" />
                    <rect x="30" y="30" width="40" height="75" rx="12" fill="#FFB347" />
                    <rect x="40" y="105" width="20" height="22" rx="8" fill="#FFD966" />
                    <circle cx="50" cy="55" r="10" fill="#FFD700" />
                    <circle cx="50" cy="80" r="6" fill="#FFD700" />
                    <rect x="45" y="127" width="10" height="18" rx="5" fill="#FFB347" />
                </svg>
            </div>
        </div>

        <!-- Stars and Crescent decoration -->
        <div class="decor-stars">
            <span>🌟</span>
            <span>⭐</span>
            <span>🌙</span>
            <span>⭐</span>
            <span>🌟</span>
        </div>

        <!-- Main greeting message -->
        <div class="greeting">
            <p>❤️ إلى ميرا الحبيبة ❤️</p>
            <p>كل سنة وأنتِ طيبة</p>
            <p>رمضانكِ مبارك</p>
            <p>🌙✨ من يوسف ✨🌙</p>
        </div>

        <!-- Another decoration with moon and stars -->
        <div class="decor-stars">
            <span>🌙</span>
            <span>🪔</span>
            <span>✨</span>
            <span>🪔</span>
            <span>🌙</span>
        </div>

        <!-- Footer with extra love -->
        <div class="footer-note">
            <i>✨</i> تقبل الله صيامك وقيامك <i>✨</i><br>
            <span class="signature">رمضان 2025</span>
        </div>
    </div>

    <!-- Floating stars and lanterns effect (small js for extra spark) -->
    <script>
        (function() {
            // Add some floating elements dynamically for more fun
            const body = document.body;
            const symbols = ['🌙', '⭐', '🌟', '🪔', '✨'];
            for (let i = 0; i < 12; i++) {
                const span = document.createElement('span');
                span.innerHTML = symbols[Math.floor(Math.random() * symbols.length)];
                span.style.position = 'absolute';
                span.style.fontSize = (Math.random() * 30 + 15) + 'px';
                span.style.left = Math.random() * 100 + '%';
                span.style.top = Math.random() * 100 + '%';
                span.style.opacity = 0.2 + Math.random() * 0.3;
                span.style.pointerEvents = 'none';
                span.style.zIndex = 1;
                span.style.animation = `twinkle ${Math.random() * 4 + 3}s infinite`;
                span.style.transform = `rotate(${Math.random() * 360}deg)`;
                body.appendChild(span);
            }
        })();
    </script>
    <style>
        /* Ensure dynamic stars are behind content but visible */
        body > span {
            z-index: 5 !important;
            text-shadow: 0 0 20px gold;
            user-select: none;
        }
    </style>
</body>
</html>
