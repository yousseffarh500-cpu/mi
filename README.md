<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>من يوسف إلى ميرا - رمضان كريم</title>
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

        /* Password Screen */
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
            border-radius: 40px;
            padding: 40px 30px;
            text-align: center;
            border: 2px solid #ffd966;
            width: 90%;
            max-width: 350px;
        }

        .password-card h2 {
            font-size: 2.2rem;
            color: #ffd966;
            margin-bottom: 15px;
        }

        .password-card .sub {
            font-size: 1.3rem;
            margin-bottom: 25px;
            color: #fff5d6;
        }

        .password-input {
            width: 100%;
            padding: 12px;
            font-size: 1.5rem;
            text-align: center;
            border: 3px solid #ffd966;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50px;
            color: white;
            margin-bottom: 15px;
            outline: none;
            letter-spacing: 3px;
        }

        .password-btn {
            background: #ffd966;
            border: none;
            color: #0b0f2a;
            font-size: 1.5rem;
            font-weight: bold;
            padding: 12px 30px;
            border-radius: 50px;
            cursor: pointer;
            width: 100%;
            transition: all 0.2s;
        }

        .password-btn:active {
            transform: scale(0.95);
            background: #ffb347;
        }

        .error-message {
            color: #ff6b6b;
            font-size: 1rem;
            margin-top: 10px;
            display: none;
        }

        .error-message.show {
            display: block;
        }

        /* Main Card */
        .card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 40px;
            padding: 40px 20px;
            max-width: 700px;
            width: 100%;
            text-align: center;
            border: 2px solid #ffd966;
            position: relative;
            z-index: 10;
        }

        h1 {
            font-size: 3.5rem;
            font-weight: bold;
            margin-bottom: 10px;
            color: #ffd966;
            text-shadow: 0 0 15px #ffb347;
        }

        .subtitle {
            font-size: 2rem;
            font-weight: bold;
            margin-bottom: 25px;
            color: #fff5d6;
            border-bottom: 2px dashed #ffd966;
            padding-bottom: 15px;
            display: inline-block;
        }

        /* Audio Player */
        .audio-player {
            margin: 20px auto;
            padding: 15px;
            background: rgba(255, 215, 0, 0.15);
            border-radius: 60px;
            border: 2px solid #ffd966;
            display: inline-block;
            width: auto;
        }
        
        .audio-player audio {
            height: 40px;
            width: 250px;
            border-radius: 20px;
        }
        
        @media (max-width: 500px) {
            .audio-player audio {
                width: 200px;
                height: 35px;
            }
        }

        /* فوانيس بسيطة */
        .lanterns {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
        }

        .fanoos {
            width: 80px;
            height: 100px;
            background: linear-gradient(145deg, #ffd966, #ffb347);
            border-radius: 50% 50% 30% 30%;
            position: relative;
            box-shadow: 0 5px 20px gold;
        }

        .fanoos::before {
            content: '';
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 30px;
            height: 15px;
            background: #ffd966;
            border-radius: 10px 10px 0 0;
        }

        .fanoos::after {
            content: '🕯️';
            position: absolute;
            bottom: -5px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 20px;
        }

        .fanoos:nth-child(2) { height: 110px; background: linear-gradient(145deg, #ffb347, #ff8c42); }
        .fanoos:nth-child(3) { height: 90px; background: linear-gradient(145deg, #f4d03f, #f39c12); }

        /* نجوم وهلال */
        .decor {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 25px 0;
            font-size: 2.5rem;
        }

        .greeting {
            font-size: 1.5rem;
            margin: 25px 0;
            background: rgba(255, 215, 0, 0.15);
            padding: 20px;
            border-radius: 50px;
            border: 2px solid #ffd966;
            line-height: 2;
        }

        .greeting p {
            margin: 8px 0;
        }

        .footer {
            margin-top: 30px;
            font-size: 1.2rem;
            color: #ffe79e;
            border-top: 2px dashed #ffd966;
            padding-top: 20px;
        }

        .signature {
            font-size: 1.8rem;
            font-weight: bold;
            color: #ffd966;
        }

        /* رسومات بسيطة */
        .moon-simple {
            position: absolute;
            top: 30px;
            left: 30px;
            width: 50px;
            height: 50px;
            background: #f7f0c3;
            border-radius: 50%;
            box-shadow: 0 0 30px gold;
            opacity: 0.5;
        }

        @media (max-width: 500px) {
            h1 { font-size: 2.5rem; }
            .subtitle { font-size: 1.5rem; }
            .greeting { font-size: 1.2rem; }
            .lanterns { gap: 10px; }
            .fanoos { width: 60px; height: 80px; }
        }
    </style>
</head>
<body>
    <!-- شاشة الرقم السري -->
    <div class="password-screen" id="passwordScreen">
        <div class="password-card">
            <h2>🔒</h2>
            <div class="sub">من يوسف إلى ميرا</div>
            <input type="password" class="password-input" id="passwordInput" placeholder="الرقم السري" maxlength="6" inputmode="numeric">
            <button class="password-btn" id="passwordBtn">دخول</button>
            <div class="error-message" id="errorMessage">❌ الرقم خطأ</div>
        </div>
    </div>

    <!-- خلفية بسيطة -->
    <div class="moon-simple"></div>
    
    <!-- المحتوى الرئيسي -->
    <div class="card" id="mainContent" style="display: none;">
        <h1>رمضان كريم</h1>
        <div class="subtitle">من يوسف إلى ميرا</div>

        <!-- مشغل الأغنية -->
        <div class="audio-player">
            <audio id="ramadanSong" controls loop>
                <source src="songr.mp3" type="audio/mpeg">
                متصفحك لا يدعم تشغيل الصوت
            </audio>
        </div>

        <!-- فوانيس بسيطة -->
        <div class="lanterns">
            <div class="fanoos"></div>
            <div class="fanoos"></div>
            <div class="fanoos"></div>
        </div>

        <!-- نجوم وهلال -->
        <div class="decor">
            <span>🌟</span>
            <span>⭐</span>
            <span>🌙</span>
            <span>⭐</span>
            <span>🌟</span>
        </div>

        <!-- رسالة التهنئة -->
        <div class="greeting">
            <p>❤️ إلى ميرا الحبيبة ❤️</p>
            <p>كل سنة وأنتِ طيبة</p>
            <p>رمضانكِ مبارك</p>
            <p>🌙 من يوسف 🌙</p>
        </div>

        <!-- زخرفة -->
        <div class="decor">
            <span>🌙</span>
            <span>✨</span>
            <span>🪔</span>
            <span>✨</span>
            <span>🌙</span>
        </div>

        <!-- تذييل -->
        <div class="footer">
            <span class="signature">رمضان 2025</span>
        </div>
    </div>

    <script>
        const passwordScreen = document.getElementById('passwordScreen');
        const mainContent = document.getElementById('mainContent');
        const passwordInput = document.getElementById('passwordInput');
        const passwordBtn = document.getElementById('passwordBtn');
        const errorMessage = document.getElementById('errorMessage');
        const ramadanSong = document.getElementById('ramadanSong');
        
        // متغير لمنع تشغيل الأغنية أكثر من مرة
        let songPlayed = false;
        
        function checkPassword() {
            if (passwordInput.value === '962025') {
                // إخفاء شاشة الرقم السري
                passwordScreen.classList.add('hidden');
                // إظهار المحتوى
                mainContent.style.display = 'block';
                
                // تشغيل الأغنية تلقائياً بعد نجاح الدخول
                if (ramadanSong && !songPlayed) {
                    // محاولة تشغيل الأغنية
                    let playPromise = ramadanSong.play();
                    
                    if (playPromise !== undefined) {
                        playPromise.then(() => {
                            // تم التشغيل بنجاح
                            console.log("الأغنية تعمل");
                            songPlayed = true;
                        }).catch(error => {
                            // فشل التشغيل التلقائي - المستخدم يحتاج للتفاعل مع الصفحة
                            console.log("فشل التشغيل التلقائي", error);
                            
                            // نعرض رسالة للمستخدم
                            alert("اضغط على زر التشغيل في مشغل الصوت لبدء الأغنية");
                        });
                    }
                }
            } else {
                errorMessage.classList.add('show');
                passwordInput.value = '';
                passwordInput.focus();
            }
        }

        // أحداث الأزرار
        passwordBtn.onclick = checkPassword;
        
        passwordInput.onkeypress = (e) => {
            if (e.key === 'Enter') checkPassword();
        };

        // مسح رسالة الخطأ عند الكتابة
        passwordInput.oninput = () => {
            errorMessage.classList.remove('show');
        };

        // منع إدخال حروف
        passwordInput.onkeydown = (e) => {
            if (isNaN(e.key) && e.key !== 'Backspace' && e.key !== 'Delete' && e.key !== 'ArrowLeft' && e.key !== 'ArrowRight' && e.key !== 'Tab') {
                e.preventDefault();
            }
        };
        
        // حل لمشكلة التشغيل التلقائي في بعض المتصفحات
        // بعض المتصفحات تمنع التشغيل التلقائي للصوت
        // نضيف خاصية التشغيل عند أي تفاعل مع الصفحة بعد الدخول
        
        // نراقب إذا المستخدم ضغط على الصفحة بعد الدخول
        document.addEventListener('click', function playOnClick() {
            if (mainContent.style.display === 'block' && ramadanSong && ramadanSong.paused && !songPlayed) {
                ramadanSong.play().then(() => {
                    songPlayed = true;
                }).catch(e => console.log("لا يمكن التشغيل"));
            }
        }, { once: true }); // تشغيل مرة واحدة فقط
    </script>
</body>
</html>
