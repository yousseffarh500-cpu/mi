<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>من يوسف إلى ميرا - رمضان 2026</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(145deg, #0b0f2a, #1a1f3a);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            color: white;
            padding: 15px;
        }

        /* Password Screen - مطورة */
        .password-screen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(145deg, #0b0f2a, #1a1f3a);
            z-index: 1000;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .password-screen.hidden {
            display: none;
        }

        .password-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(5px);
            border-radius: 50px;
            padding: 50px 30px;
            text-align: center;
            border: 3px solid #ffd966;
            width: 90%;
            max-width: 400px;
            box-shadow: 0 0 50px rgba(255, 215, 0, 0.3);
        }

        .password-card h2 {
            font-size: 3rem;
            color: #ffd966;
            margin-bottom: 10px;
            text-shadow: 0 0 20px gold;
        }

        .password-card .sub {
            font-size: 2rem;
            font-weight: bold;
            margin-bottom: 20px;
            color: #fff5d6;
        }

        .password-hint {
            background: rgba(255, 215, 0, 0.2);
            padding: 15px;
            border-radius: 60px;
            margin: 25px 0;
            font-size: 2rem;
            font-weight: bold;
            color: #ffd966;
            border: 2px dashed #ffd966;
            letter-spacing: 5px;
            direction: ltr;
        }

        .password-input {
            width: 100%;
            padding: 15px;
            font-size: 2rem;
            text-align: center;
            border: 4px solid #ffd966;
            background: rgba(255, 255, 255, 0.15);
            border-radius: 60px;
            color: white;
            margin-bottom: 20px;
            outline: none;
            letter-spacing: 8px;
            font-weight: bold;
        }

        .password-input:focus {
            box-shadow: 0 0 30px gold;
        }

        .password-btn {
            background: linear-gradient(145deg, #ffd966, #ffb347);
            border: none;
            color: #0b0f2a;
            font-size: 2rem;
            font-weight: bold;
            padding: 15px 30px;
            border-radius: 60px;
            cursor: pointer;
            width: 100%;
            transition: all 0.2s;
            border: 2px solid white;
        }

        .password-btn:hover {
            transform: scale(1.02);
            box-shadow: 0 0 30px gold;
        }

        .password-btn:active {
            transform: scale(0.98);
        }

        .error-message {
            color: #ff6b6b;
            font-size: 1.3rem;
            margin-top: 15px;
            display: none;
        }

        .error-message.show {
            display: block;
        }

        /* Main Card */
        .card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(5px);
            border-radius: 60px;
            padding: 50px 30px;
            max-width: 900px;
            width: 100%;
            text-align: center;
            border: 3px solid #ffd966;
            position: relative;
            z-index: 10;
            box-shadow: 0 0 50px rgba(0,0,0,0.5);
        }

        h1 {
            font-size: 5rem;
            font-weight: bold;
            margin-bottom: 10px;
            color: #ffd966;
            text-shadow: 0 0 30px #ffb347, 0 0 60px gold;
            animation: glow 2s infinite;
        }

        @keyframes glow {
            0% { text-shadow: 0 0 20px gold; }
            50% { text-shadow: 0 0 50px #ffb347, 0 0 30px gold; }
            100% { text-shadow: 0 0 20px gold; }
        }

        .subtitle {
            font-size: 2.5rem;
            font-weight: bold;
            margin-bottom: 30px;
            color: #fff5d6;
            border-bottom: 3px dashed #ffd966;
            padding-bottom: 15px;
            display: inline-block;
        }

        /* Audio Player */
        .audio-player {
            margin: 25px auto;
            padding: 15px 25px;
            background: rgba(255, 215, 0, 0.2);
            border-radius: 60px;
            border: 2px solid #ffd966;
            display: inline-block;
        }
        
        .audio-player audio {
            height: 45px;
            width: 280px;
            border-radius: 30px;
        }

        /* فوانيس متحركة */
        .lanterns {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin: 40px 0;
        }

        .fanoos {
            width: 100px;
            height: 130px;
            background: linear-gradient(145deg, #ffd966, #ffb347);
            border-radius: 50% 50% 30% 30%;
            position: relative;
            box-shadow: 0 10px 30px gold;
            animation: swing 2s infinite ease-in-out;
            transform-origin: top center;
        }

        .fanoos:nth-child(2) {
            animation-delay: 0.3s;
            height: 140px;
            background: linear-gradient(145deg, #ffb347, #ff8c42);
        }

        .fanoos:nth-child(3) {
            animation-delay: 0.6s;
            height: 120px;
            background: linear-gradient(145deg, #f4d03f, #f39c12);
        }

        @keyframes swing {
            0% { transform: rotate(0deg); }
            25% { transform: rotate(5deg); }
            75% { transform: rotate(-5deg); }
            100% { transform: rotate(0deg); }
        }

        .fanoos::before {
            content: '';
            position: absolute;
            top: -20px;
            left: 50%;
            transform: translateX(-50%);
            width: 35px;
            height: 20px;
            background: #ffd966;
            border-radius: 10px 10px 0 0;
            box-shadow: 0 -5px 10px rgba(255,215,0,0.5);
        }

        .fanoos::after {
            content: '🕯️';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 25px;
            animation: flame 1s infinite;
        }

        @keyframes flame {
            0% { opacity: 0.8; transform: translateX(-50%) scale(1); }
            50% { opacity: 1; transform: translateX(-50%) scale(1.2); }
            100% { opacity: 0.8; transform: translateX(-50%) scale(1); }
        }

        /* نجوم متحركة */
        .decor {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin: 30px 0;
            font-size: 3rem;
        }

        .decor span {
            animation: starTwinkle 1.5s infinite;
            display: inline-block;
        }

        .decor span:nth-child(2) { animation-delay: 0.2s; }
        .decor span:nth-child(3) { animation-delay: 0.4s; }
        .decor span:nth-child(4) { animation-delay: 0.6s; }
        .decor span:nth-child(5) { animation-delay: 0.8s; }

        @keyframes starTwinkle {
            0% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.3); opacity: 0.8; text-shadow: 0 0 30px gold; }
            100% { transform: scale(1); opacity: 1; }
        }

        /* كلام رمضاني */
        .greeting {
            font-size: 1.8rem;
            margin: 30px 0;
            background: rgba(255, 215, 0, 0.15);
            padding: 30px 20px;
            border-radius: 70px;
            border: 3px solid #ffd966;
            line-height: 2.2;
        }

        .greeting p {
            margin: 15px 0;
        }

        .ramadan-quote {
            font-size: 1.4rem;
            color: #ffe79e;
            font-style: italic;
            margin: 20px 0;
            padding: 15px;
            border-right: 5px solid #ffd966;
            border-left: 5px solid #ffd966;
        }

        .footer {
            margin-top: 40px;
            font-size: 1.4rem;
            color: #ffe79e;
            border-top: 3px dashed #ffd966;
            padding-top: 25px;
        }

        .signature {
            font-size: 2.2rem;
            font-weight: bold;
            color: #ffd966;
            text-shadow: 0 0 15px gold;
        }

        .moon-simple {
            position: absolute;
            top: 30px;
            left: 30px;
            width: 70px;
            height: 70px;
            background: #f7f0c3;
            border-radius: 50%;
            box-shadow: 0 0 50px gold;
            opacity: 0.4;
        }

        /* علامة 2026 مميزة */
        .year-badge {
            display: inline-block;
            background: #ffd966;
            color: #0b0f2a;
            padding: 8px 25px;
            border-radius: 60px;
            font-size: 2rem;
            font-weight: bold;
            margin: 15px 0;
            box-shadow: 0 0 30px gold;
            border: 2px solid white;
        }

        @media (max-width: 600px) {
            h1 { font-size: 3.5rem; }
            .subtitle { font-size: 2rem; }
            .greeting { font-size: 1.4rem; }
            .lanterns { gap: 15px; }
            .fanoos { width: 70px; height: 100px; }
            .fanoos:nth-child(2) { height: 110px; }
            .fanoos:nth-child(3) { height: 90px; }
            .password-card h2 { font-size: 2.5rem; }
            .password-card .sub { font-size: 1.5rem; }
            .password-hint { font-size: 1.5rem; }
            .year-badge { font-size: 1.5rem; }
        }
    </style>
</head>
<body>
    <!-- شاشة الرقم السري -->
    <div class="password-screen" id="passwordScreen">
        <div class="password-card">
            <h2>🔒 رمضان 2026 🔒</h2>
            <div class="sub">من يوسف → إلى ميرا</div>
            
            <!-- الرقم السري مكتوب -->
            <div class="password-hint">
                ✨ 962025 ✨
            </div>
            
            <input type="password" class="password-input" id="passwordInput" placeholder="أدخل الرقم السري" maxlength="6" inputmode="numeric">
            <button class="password-btn" id="passwordBtn">ادخل يا رمضان</button>
            <div class="error-message" id="errorMessage">❌ الرقم غلط! حاول تاني</div>
            <div style="margin-top: 20px; color: #ffd966; font-size: 1.2rem;">⬆️ الرقم السري مكتوب فوق ⬆️</div>
        </div>
    </div>

    <!-- خلفية -->
    <div class="moon-simple"></div>
    
    <!-- المحتوى الرئيسي -->
    <div class="card" id="mainContent" style="display: none;">
        <h1>🌙 رمضان كريم 🌙</h1>
        <div class="subtitle">من يوسف إلى ميرا</div>
        
        <!-- بطاقة 2026 -->
        <div class="year-badge">
            ✨ 2026 ✨
        </div>

        <!-- مشغل الأغنية -->
        <div class="audio-player">
            <audio id="ramadanSong" controls loop>
                <source src="songr.mp3" type="audio/mpeg">
                متصفحك لا يدعم الصوت
            </audio>
        </div>

        <!-- فوانيس متحركة -->
        <div class="lanterns">
            <div class="fanoos"></div>
            <div class="fanoos"></div>
            <div class="fanoos"></div>
        </div>

        <!-- نجوم وهلال متحركة -->
        <div class="decor">
            <span>🌟</span>
            <span>⭐</span>
            <span>🌙</span>
            <span>⭐</span>
            <span>🌟</span>
        </div>

        <!-- رسالة التهنئة - 2026 -->
        <div class="greeting">
            <p>❤️ إلى ميرا الحبيبة ❤️</p>
            <p>✨ كل سنة وأنتِ طيبة ✨</p>
            <p>🌙 رمضان 2026 مبارك عليكِ 🌙</p>
            <p>🕌 تقبل الله صيامك وقيامك 🕌</p>
            <p>💫 سنة جديدة مليئة بالبركات 💫</p>
            <p>⭐ من يوسف ⭐</p>
        </div>

        <!-- كلام رمضاني -->
        <div class="ramadan-quote">
            "شهر رمضان الذي أنزل فيه القرآن"<br>
            ✨ اللهم بارك لنا في رمضان 2026 ✨
        </div>

        <!-- زخرفة -->
        <div class="decor">
            <span>🌙</span>
            <span>✨</span>
            <span>🪔</span>
            <span>✨</span>
            <span>🌙</span>
        </div>

        <!-- تهنئة خاصة -->
        <div style="font-size: 1.4rem; margin: 25px 0; color: #fff5d6; background: rgba(255,215,0,0.1); padding: 15px; border-radius: 50px;">
            ♥️ كل رمضان وأنتِ أجمل ♥️<br>
            🗓️ 2026 - عام الخير والبركة 🗓️
        </div>

        <!-- تذييل -->
        <div class="footer">
            <span class="signature">رمضان 2026 - مبارك عليكم الشهر</span>
        </div>
    </div>

    <script>
        // كود التشغيل
        const passwordScreen = document.getElementById('passwordScreen');
        const mainContent = document.getElementById('mainContent');
        const passwordInput = document.getElementById('passwordInput');
        const passwordBtn = document.getElementById('passwordBtn');
        const errorMessage = document.getElementById('errorMessage');
        const ramadanSong = document.getElementById('ramadanSong');
        
        let songPlayed = false;
        
        function checkPassword() {
            if (passwordInput.value === '962025') {
                // إخفاء شاشة الرقم السري
                passwordScreen.classList.add('hidden');
                // إظهار المحتوى
                mainContent.style.display = 'block';
                
                // تشغيل الأغنية
                if (ramadanSong && !songPlayed) {
                    let playPromise = ramadanSong.play();
                    
                    if (playPromise !== undefined) {
                        playPromise.then(() => {
                            songPlayed = true;
                        }).catch(error => {
                            // المستخدم يحتاج للتفاعل
                            alert("اضغط على زر التشغيل لسماع الأغنية 🎵");
                        });
                    }
                }
            } else {
                errorMessage.classList.add('show');
                passwordInput.value = '';
                passwordInput.focus();
            }
        }

        // أحداث
        passwordBtn.onclick = checkPassword;
        
        passwordInput.onkeypress = (e) => {
            if (e.key === 'Enter') checkPassword();
        };

        passwordInput.oninput = () => {
            errorMessage.classList.remove('show');
        };

        // منع الحروف
        passwordInput.onkeydown = (e) => {
            if (isNaN(e.key) && e.key !== 'Backspace' && e.key !== 'Delete' && e.key !== 'ArrowLeft' && e.key !== 'ArrowRight' && e.key !== 'Tab') {
                e.preventDefault();
            }
        };
        
        // تشغيل الأغنية عند أي ضغطة بعد الدخول
        document.addEventListener('click', function playOnClick() {
            if (mainContent.style.display === 'block' && ramadanSong && ramadanSong.paused && !songPlayed) {
                ramadanSong.play().then(() => {
                    songPlayed = true;
                }).catch(e => {});
            }
        });
    </script>
</body>
</html>
