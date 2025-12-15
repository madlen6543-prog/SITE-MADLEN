<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BEST OF YOU 2026 - סדנת עומק רגשית</title>
    <!-- פונטים -->
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Rubik:wght@300;400;500;700;900&family=Oswald:wght@400;500;700&display=swap" rel="stylesheet">
    <!-- אייקונים -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

    <style>
        :root {
            --neon-glow: #ff00ff;
            --text-color: #ffffff;
            --paybox-color: #00b9ff;
            --bit-color: #0070f3;
            --whatsapp-color: #25D366;
            --instagram-gradient: linear-gradient(45deg, #f09433 0%,#e6683c 25%,#dc2743 50%,#cc2366 75%,#bc1888 100%);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
            /* מרווח עליון כדי שהתפריט לא יסתיר את הכותרת בגלילה */
            scroll-padding-top: 20px; 
        }

        /* --- רקע קבוע --- */
        #fixed-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100vh;
            z-index: -1;
            background-color: #0f0c29;
            background-image: 
                radial-gradient(circle at 20% 30%, rgba(245, 0, 212, 0.25) 0%, transparent 50%),
                radial-gradient(circle at 80% 70%, rgba(74, 0, 224, 0.3) 0%, transparent 50%),
                radial-gradient(circle at 50% 50%, #1a0b2e 0%, #000000 100%);
            background-size: cover;
        }

        body {
            font-family: 'Rubik', sans-serif;
            color: var(--text-color);
            overflow-x: hidden;
            min-height: 100vh;
            font-weight: 300;
            margin: 0;
        }

        /* --- עיצוב טקסט --- */
        .ombre-text {
            background: linear-gradient(90deg, #ff00cc, #9d4edd);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 900;
            display: inline-block;
            font-size: 1.5em;
            text-shadow: 0 0 20px rgba(255, 0, 204, 0.3);
            border-bottom: 2px solid rgba(255, 0, 204, 0.3);
            padding-bottom: 2px;
        }
        
        .pain-highlight {
            color: #ff4081;
            font-weight: 700;
            text-shadow: 0 0 15px rgba(255, 64, 129, 0.6);
        }

        /* --- אנימציות --- */
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            animation: fadeInUp 0.8s ease-out forwards;
        }
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease-out;
        }
        .reveal.active { opacity: 1; transform: translateY(0); }
        .fade-in-load { opacity: 0; transform: translateY(20px); animation: fadeInUp 0.8s ease-out forwards; }
        
        .delay-1 { animation-delay: 0.2s; }
        .delay-2 { animation-delay: 0.4s; }
        .delay-3 { animation-delay: 0.6s; }
        .delay-4 { animation-delay: 0.8s; }

        @keyframes fadeInUp { to { opacity: 1; transform: translateY(0); } }

        /* --- כפתורים --- */
        .cta-btn {
            background: linear-gradient(90deg, #d500f9, #651fff);
            color: white;
            padding: 16px 40px;
            font-size: 1.2rem;
            font-weight: 500;
            border: 2px solid rgba(255,255,255,0.3);
            border-radius: 50px;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            box-shadow: 0 0 30px rgba(213, 0, 249, 0.4);
            transition: all 0.3s ease;
            text-shadow: 0 1px 2px rgba(0,0,0,0.3);
            margin: 10px;
        }
        .cta-btn:hover { transform: scale(1.05); box-shadow: 0 0 50px rgba(213, 0, 249, 0.7); border-color: white; }

        .secondary-btn {
            background: rgba(255, 255, 255, 0.1);
            color: white;
            padding: 16px 40px;
            font-size: 1.2rem;
            font-weight: 500;
            border: 2px solid rgba(255,255,255,0.5);
            border-radius: 50px;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            transition: all 0.3s ease;
            margin: 10px;
        }
        .secondary-btn:hover { background: rgba(255, 255, 255, 0.2); border-color: white; }

        .hero-buttons { margin-top: 30px; display: flex; justify-content: center; flex-wrap: wrap; position: relative; z-index: 10; }

        /* --- HERO --- */
        .hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
            position: relative;
            overflow: hidden;
            padding-top: 80px;
        }

        .brand-signature {
            position: absolute; top: 30px; left: 30px;
            font-family: 'Dancing Script', cursive; font-size: 1.8rem;
            color: rgba(255, 255, 255, 0.9); z-index: 20;
            text-shadow: 0 0 10px rgba(255, 0, 255, 0.5);
        }

        .neon-ring {
            position: absolute; top: 50%; left: 50%;
            width: 120vw; max-width: 800px; height: 500px;
            border: 1px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            box-shadow: 0 0 25px var(--neon-glow), inset 0 0 25px var(--neon-glow);
            pointer-events: none; z-index: 0; opacity: 0.5;
            animation: slowRotate 60s linear infinite;
        }
        .neon-ring::before {
            content: ''; position: absolute;
            top: 20px; left: 20px; right: 20px; bottom: 20px;
            border: 1px solid rgba(255, 255, 255, 0.15); border-radius: 50%;
            transform: rotate(45deg);
        }
        @keyframes slowRotate {
            from { transform: translate(-50%, -50%) rotate(0deg); }
            to { transform: translate(-50%, -50%) rotate(360deg); }
        }

        .logo-container { position: relative; z-index: 2; margin-bottom: 15px; }
        
        h1.main-title { 
            font-family: 'Oswald', sans-serif; 
            text-transform: uppercase; 
            line-height: 0.9; 
            margin: 0; 
        }
        
        .title-text, .year-text { 
            display: block; 
            font-weight: 500; 
            color: transparent; 
            -webkit-text-stroke: 2px #ffffff; 
            text-shadow: 
                0 0 15px rgba(255, 0, 255, 0.8), 
                0 0 30px rgba(255, 0, 255, 0.5); 
            letter-spacing: 2px;
        }
        
        .title-text { font-size: 5rem; }
        .year-text { font-size: 4rem; margin-top: 5px; }
        
        .hero-kicker {
            font-size: 1.5rem; font-weight: 700; color: #ffffff;
            text-transform: uppercase; letter-spacing: 1px;
            margin-top: 20px; margin-bottom: 10px; z-index: 2;
            text-shadow: 0 0 10px rgba(255, 255, 255, 0.5);
        }

        .hero h2 { 
            font-size: 1.25rem; max-width: 800px; font-weight: 300; 
            margin-top: 20px; margin-bottom: 20px; line-height: 1.6; 
            color: #fff; text-shadow: 0 2px 4px rgba(0,0,0,0.5); 
            z-index: 1; background: rgba(0,0,0,0.3); 
            padding: 25px; border-radius: 15px; 
            backdrop-filter: blur(5px); border: 1px solid rgba(255,255,255,0.1); 
        }

        /* כוכבים */
        .sparkle { position: absolute; background: white; border-radius: 50%; box-shadow: 0 0 10px white, 0 0 20px white, 0 0 40px #ff00ff; animation: twinkle 4s infinite ease-in-out; z-index: 0; }
        .big-star { position: absolute; color: white; font-size: 3.5rem; text-shadow: 0 0 25px white; animation: float 5s infinite ease-in-out; z-index: 1; }
        .small-star { position: absolute; color: white; font-size: 1.5rem; text-shadow: 0 0 15px white; animation: float 4s infinite ease-in-out reverse; }
        @keyframes twinkle { 0%, 100% { opacity: 0.2; transform: scale(1); } 50% { opacity: 1; transform: scale(1.5); } }
        @keyframes float { 0%, 100% { transform: scale(1) rotate(0deg); } 50% { transform: scale(1.2) rotate(15deg); } }

        /* --- קונטיינרים --- */
        .container { max-width: 900px; margin: 0 auto; padding: 60px 20px; }
        
        .section-box { 
            background: rgba(60, 20, 80, 0.6); border: 1px solid rgba(255, 255, 255, 0.1); 
            padding: 40px; border-radius: 20px; backdrop-filter: blur(10px); 
            margin-bottom: 40px; box-shadow: 0 10px 40px rgba(0,0,0,0.3); 
        }
        
        .qual-list { list-style: none; padding: 0; }
        .qual-list li { margin-bottom: 25px; font-size: 1.15rem; padding-right: 35px; position: relative; line-height: 1.6; }
        .qual-list li:before { content: '✦'; position: absolute; right: 0; top: 2px; font-size: 1.2rem; background: linear-gradient(90deg, #ff00cc, #9d4edd); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        
        .qual-highlight { 
            font-weight: 700; 
            color: #330066; 
            background-color: rgba(255, 255, 255, 0.95); 
            padding: 2px 8px; 
            border-radius: 4px; 
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }

        /* --- JOURNEY --- */
        .journey-section { display: flex; align-items: stretch; justify-content: center; gap: 30px; margin-bottom: 50px; flex-wrap: wrap; }
        .year-card { flex: 1; min-width: 300px; padding: 35px; border-radius: 20px; position: relative; background: rgba(15, 12, 41, 0.7); border: 2px solid transparent; transition: transform 0.3s; }
        .year-card::before { content: ''; position: absolute; top: -2px; left: -2px; right: -2px; bottom: -2px; border-radius: 22px; background: linear-gradient(45deg, #ff00cc, #333399, #00d4ff); z-index: -1; opacity: 0.6; }
        .year-2026 { box-shadow: 0 0 30px rgba(255, 0, 204, 0.2); }
        .year-2026::before { opacity: 1; background: linear-gradient(45deg, #d500f9, #ff00cc); }
        .year-title { font-family: 'Oswald', sans-serif; font-size: 3rem; margin-bottom: 15px; text-shadow: 0 0 10px rgba(255,255,255,0.3); }
        
        .journey-arrow { display: flex; align-items: center; justify-content: center; font-size: 3rem; color: var(--neon-glow); text-shadow: 0 0 20px var(--neon-glow); animation: pulse 2s infinite; transform: rotate(180deg); }

        .state-list { list-style: none; padding: 0; text-align: right; }
        .state-list li { margin-bottom: 15px; font-size: 1.1rem; padding-right: 30px; position: relative; white-space: normal; line-height: 1.4; }
        .year-2025 .state-list li:before { content: '❌'; position: absolute; right: 0; font-size: 0.9em; opacity: 0.8; }
        .year-2026 .state-list li:before { content: '✅'; position: absolute; right: 0; font-size: 1em; }

        /* --- PROCESS --- */
        .process-steps { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; margin-top: 40px; }
        .step-card { background: rgba(255, 255, 255, 0.05); padding: 30px 25px; border-radius: 15px; border: 1px solid rgba(255, 255, 255, 0.1); text-align: center; position: relative; transition: transform 0.3s; }
        .step-card:hover { background: rgba(255, 255, 255, 0.1); transform: translateY(-5px); border-color: var(--neon-glow); }
        .step-card h3 { 
            font-family: 'Oswald', sans-serif; font-size: 1.8rem; color: transparent;
            -webkit-text-stroke: 1px #ffffff; text-shadow: 0 0 5px rgba(255, 0, 255, 0.6), 0 0 10px rgba(255, 0, 255, 0.4);
            margin: 15px 0; letter-spacing: 1px;
        }
        .step-num { display: block; font-family: 'Oswald', sans-serif; font-size: 2.5rem; color: rgba(255,255,255,0.1); position: absolute; top: 5px; right: 15px; font-weight: 700; }
        .step-card p { font-size: 1.05rem; line-height: 1.6; color: #ddd; font-weight: 300; padding: 0 5px; }
        .step-arrow { display: none; color: var(--neon-glow); font-size: 2rem; align-self: center; opacity: 0.7; }

        /* --- BIO --- */
        .bio-box { display: flex; align-items: flex-start; gap: 30px; background: rgba(255, 255, 255, 0.05); padding: 40px; border-radius: 20px; margin-bottom: 50px; border: 1px solid rgba(255,255,255,0.1); }
        .bio-img { width: 150px; height: 150px; border-radius: 50%; object-fit: cover; border: 3px solid #d500f9; box-shadow: 0 0 30px rgba(213, 0, 249, 0.3); flex-shrink: 0; }
        .bio-content { flex: 1; }
        .bio-content h3 { margin: 0 0 15px 0; font-family: 'Oswald', sans-serif; font-size: 2.2rem; color: #fff; text-transform: uppercase; letter-spacing: 1px; }
        
        /* חזרנו לעיצוב ה"נקי" והפשוט שהיה קודם לטקסט */
        .bio-content p { font-size: 1.1rem; color: #eee; margin-bottom: 15px; line-height: 1.8; font-weight: 300; text-align: right; }
        
        .bio-highlight { color: #ffd700; font-weight: bold; }

        /* --- COUNTDOWN --- */
        #countdown { display: flex; justify-content: center; gap: 20px; margin: 20px 0; color: #fff; }
        .timer-item { background: rgba(255,255,255,0.1); padding: 10px; border-radius: 10px; min-width: 70px; text-align: center; border: 1px solid rgba(255,255,255,0.2); }
        .timer-val { font-size: 1.5rem; font-weight: bold; display: block; color: #d500f9; }
        .timer-label { font-size: 0.8rem; opacity: 0.8; }

        /* --- FAQ --- */
        .faq-item { margin-bottom: 15px; border-bottom: 1px solid rgba(255,255,255,0.1); }
        .faq-question { cursor: pointer; padding: 15px; background: rgba(0,0,0,0.2); border-radius: 10px; font-weight: bold; position: relative; transition: background 0.3s; }
        .faq-question:hover { background: rgba(255,255,255,0.1); }
        .faq-answer { max-height: 0; overflow: hidden; transition: max-height 0.3s ease; color: #ddd; padding: 0 15px; }
        .faq-item.active .faq-answer { max-height: 200px; padding: 15px; }
        .faq-icon { float: left; transition: transform 0.3s; }
        .faq-item.active .faq-icon { transform: rotate(180deg); }

        /* --- CHECKOUT --- */
        .checkout-section { background: rgba(20, 20, 40, 0.7); color: #ffffff; border: 1px solid rgba(255, 255, 255, 0.2); border-radius: 20px; padding: 50px 30px; text-align: center; max-width: 650px; margin: 0 auto; box-shadow: 0 0 80px rgba(100, 0, 200, 0.3); position: relative; backdrop-filter: blur(10px); }
        .scarcity-badge { background: #ff4081; color: white; padding: 5px 15px; border-radius: 20px; font-size: 0.9rem; font-weight: bold; display: inline-block; margin-bottom: 15px; animation: pulse 2s infinite; }
        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.05); } 100% { transform: scale(1); } }
        .price-wrapper { margin: 20px 0; }
        .old-price { text-decoration: line-through; color: #bbb; font-size: 1.5rem; display: block; }
        .price-tag { font-size: 3.5rem; color: #d500f9; font-weight: 700; line-height: 1; text-shadow: 0 0 20px rgba(213, 0, 249, 0.5); }
        .bonuses-list { text-align: right; background: rgba(255, 255, 255, 0.1); padding: 20px; border-radius: 10px; margin: 20px auto; max-width: 400px; display: inline-block; width: 100%; border: 1px solid rgba(255,255,255,0.2); }
        .bonuses-list h4 { margin-top: 0; color: #d500f9; margin-bottom: 10px; font-weight: 700; }
        .bonuses-list li { list-style: none; margin-bottom: 8px; font-size: 1rem; color: #fff; }
        .payment-options { display: flex; flex-direction: column; gap: 15px; margin-top: 30px; }
        .pay-btn { display: flex; align-items: center; justify-content: center; gap: 10px; padding: 15px; border-radius: 12px; text-decoration: none; font-weight: bold; font-size: 1.1rem; transition: transform 0.2s; color: white; border: none; cursor: pointer; }
        .pay-btn:hover { transform: translateY(-3px); }
        .btn-bit { background-color: var(--bit-color); box-shadow: 0 4px 15px rgba(0, 112, 243, 0.3); }
        .btn-paybox { background-color: var(--paybox-color); box-shadow: 0 4px 15px rgba(0, 185, 255, 0.3); }
        .btn-whatsapp { background-color: var(--whatsapp-color); box-shadow: 0 4px 15px rgba(37, 211, 102, 0.3); }
        .pay-btn i { font-size: 1.4rem; }
        .final-note { margin-top: 25px; font-size: 1.1rem; font-weight: 500; color: #fff; text-shadow: 0 0 10px rgba(255,0,255,0.5); line-height: 1.5; }

        /* INSTAGRAM */
        .footer-social { margin-top: 20px; font-size: 1.5rem; }
        .footer-social a { color: #fff; text-decoration: none; display: flex; align-items: center; justify-content: center; gap: 10px; }
        .footer-social i {
            background: var(--instagram-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-size: 2rem;
        }

        @media (max-width: 768px) {
            .title-text { font-size: 3.5rem; -webkit-text-stroke: 1px #ffffff; }
            .year-text { font-size: 3rem; -webkit-text-stroke: 1px #ffffff; }
            .neon-ring { width: 90vw; height: 90vw; max-width: 400px; max-height: 400px; top: 40%; }
            .checkout-section { padding-bottom: 40px; }
            .process-steps { grid-template-columns: 1fr; }
            .big-star { font-size: 3rem; top: 10%; right: 5%; }
            .journey-section { flex-direction: column; }
            .journey-arrow { transform: rotate(90deg); margin: 10px 0; }
            .bio-box { flex-direction: column; text-align: center; }
            .bio-img { margin: 0 auto; }
            .brand-signature { top: 15px; font-size: 1.5rem; }
            .hero { padding-top: 60px; }
            .price-wrapper { flex-direction: row; align-items: center; gap: 15px; }
        }
        
        /* Grid with arrows fix */
        .process-steps {
            display: grid;
            grid-template-columns: 1fr auto 1fr auto 1fr auto 1fr;
            align-items: center;
            gap: 10px;
        }
        
        @media (max-width: 900px) {
            .process-steps {
                grid-template-columns: 1fr;
                gap: 20px;
            }
            .step-arrow {
                display: none;
            }
        }
    </style>
</head>
<body>

    <!-- רקע קבוע -->
    <div id="fixed-background"></div>

    <!-- חתימת מותג -->
    <div class="brand-signature">Madlen Frid</div>

    <!-- HERO -->
    <section class="hero fade-in-load">
        <div class="neon-ring"></div>
        <div class="big-star" style="top: 15%; right: 15%;">✦</div>
        <div class="small-star" style="top: 60%; left: 10%;">✦</div>
        <div class="sparkle" style="top: 20%; left: 20%;"></div>
        
        <div class="logo-container">
            <h1 class="main-title">
                <span class="title-text">BEST OF YOU</span>
                <span class="year-text">2026</span>
            </h1>
        </div>

        <div class="hero-kicker fade-in-load">סיכום 2025 ותכנון 2026 ✨</div>

        <h2 class="fade-in-load delay-1">
            <strong>מחכה לכם סדנת זום אינטימית,<br>ממלאת, מעצימה וחוויתית</strong><br><br>
            נשב יחד על השנה שהייתה, נבין את השיעורים שלמדנו, ונבנה <span class="ombre-text" style="font-size: 1.4rem;">תוכנית עבודה מדויקת ל-2026</span>.
        </h2>

        <div class="hero-buttons fade-in-load delay-2">
            <!-- קישור ישיר לצ'קאוט -->
            <a href="#checkout" class="cta-btn">אני רוצה להצטרף לזום ✨</a>
            <!-- קישור ישיר לביו -->
            <a href="#bio" class="secondary-btn">לקרוא עוד</a>
        </div>
    </section>

    <!-- Qualification -->
    <section id="about" class="container reveal">
        <div class="section-box">
            <h3 style="text-align: center; font-size: 1.8rem; margin-bottom: 30px; text-shadow: 0 0 10px white;">למי הסדנה מתאימה?</h3>
            <ul class="qual-list">
                <li>
                    מרגישים שלא מתקדמים בגלל <span class="pain-highlight">בלבול ובלאגן בראש</span>
                </li>
                <li>
                    יש יותר מידי דברים ולא יודעים במה להתמקד.<br>נבין יחד את <span class="pain-highlight">הרצונות העמוקים</span>
                </li>
                <li>
                    רוצים לעבוד על המיינדסט ולפתח <span class="pain-highlight">הסתכלות חיובית ומחזקת</span> על עצמכם.
                </li>
                <li>
                    מחפשים <span class="pain-highlight">תוכנית עבודה מדויקת</span> לשנה החדשה שתסדר לכם את כל החלקים בפאזל.
                </li>
            </ul>
        </div>
    </section>

    <!-- JOURNEY (Moved before Bio) -->
    <section class="container reveal">
        <h2 style="text-align: center; margin-bottom: 40px; font-weight: 300;">איפה אתם היום ולאן אתם רוצים להגיע?</h2>
        <div class="journey-section">
            <!-- Point A -->
            <div class="year-card year-2025">
                <div class="year-title">כרגע</div>
                <p style="font-weight: bold; margin-bottom: 15px;">התחושה הנוכחית:</p>
                <ul class="state-list">
                    <li>גוללים באינסטגרם ומרגישים שכולם מתקדמים ורק אנחנו תקועים מאחור.</li>
                    <li>החיים מרגישים על "אוטומט".</li>
                    <li>מפחדים להציב מטרות כי בינינו? לא מאמינים שנעמוד בהן.</li>
                    <li>הראש מלא ברעש ומחשבות, ואפס בהירות.</li>
                </ul>
            </div>
            
            <!-- Arrow -->
            <div class="journey-arrow">⬅</div>
            
            <!-- Point B -->
            <div class="year-card year-2026">
                <div class="year-title">2026</div>
                <p style="font-weight: bold; margin-bottom: 15px;">אחרי הסדנה:</p>
                <ul class="state-list">
                    <li>קמים בבוקר עם תוכנית פעולה ברורה – יודעים בדיוק מה הצעד הבא.</li>
                    <li>שקט וביטחון פנימי שמגיע מסדר אמיתי.</li>
                    <li>מטרות שמרגשות אתכם ולא מלחיצות.</li>
                    <li>אמונה בעצמכם שאתם מסוגלים להתמיד.</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- BIO (Restored to Full Authentic Version) -->
    <section id="bio" class="container reveal">
        <div class="bio-box">
            <img src="https://raw.githubusercontent.com/madlen6543-prog/IMAGES-/3837de9053438dc5551eeb803893dcf45ffb0d42/%D7%AA%D7%9E%D7%95%D7%A0%D7%94%20%D7%A9%D7%9C%D7%99%20-%20%D7%A7%D7%A6%D7%AA%20%D7%A2%D7%9C%D7%99%D7%99.png" alt="מדלן פריד" class="bio-img">
            <div class="bio-content">
                <h3>היי! אני <strong>מדלן פריד</strong>, בת 22.</h3>
                <p>בשנים האחרונות עברתי מסע של צמיחה משמעותית – הייתי הילדה הביישנית והסגורה בצד, והיום? אני הולכת עם הלב והאינטואיציה שלי עד הסוף.</p>
                <p>הדרך לא הייתה קלה. היו לא מעט נפילות בדרך, אבל בדיוק משם למדתי מה תוקע אותנו ואיך יוצאים מזה כדי להיות הגרסה הכי טובה של עצמנו.</p>
                <p>יצרתי את התוכנית הזו כדי לתת לכם את הקיצור דרך שאני הייתי צריכה. הכלים, הידע והניסיון שצברתי - הכל מוגש לכם, כדי שתוכלו לחסוך לעצמכם את הכאב ראש ולהתחיל את השנה בצורה הכי מדויקת שיש.</p>
                <p>זו קפיצת המדרגה הראשונה שלי, ואני מזמינה אתכם לקפוץ למים יחד איתי. <strong>עכשיו תורכם.</strong></p>
            </div>
        </div>
    </section>

    <!-- PROCESS -->
    <section id="process" class="container reveal">
        <h2 style="text-align: center; font-size: 2.2rem; margin-bottom: 20px; text-shadow: 0 0 10px #ff00ff;">מה מחכה לכם? <span style="font-size: 0.8em;">📝✍️</span></h2>
        <p style="text-align: center; opacity: 0.9; max-width: 600px; margin: 0 auto 40px auto;">
            ריפלקציה עמוקה על השנה שהייתה ותכנון שנה קדימה
        </p>
        
        <div class="process-steps">
            <!-- Step 1 -->
            <div class="step-card">
                <span class="step-num">01.</span>
                <h3>סיכום מלא של שנת 2025</h3>
                <p>לשחרר את הכובד. להבין מה עבר עלינו, לסלוח לעצמנו על מה שלא הספקנו, ולפנות מקום נקי בלב לשנה החדשה.</p>
            </div>
            
            <div class="step-arrow"><i class="fa-solid fa-chevron-left"></i></div>

            <!-- Step 2 -->
            <div class="step-card">
                <span class="step-num">02.</span>
                <h3>חיבור לרצונות הלב</h3>
                <p>להקשיב לקול הפנימי. מה <strong>באמת</strong> מרגש אותנו? לא מה שכולם עושים, אלא מה שיגרום לנו לקום בבוקר עם ניצוץ.</p>
            </div>

            <div class="step-arrow"><i class="fa-solid fa-chevron-left"></i></div>

            <!-- Step 3 -->
            <div class="step-card">
                <span class="step-num">03.</span>
                <h3>הגרסה הבאה שלך</h3>
                <p>לפגוש את הגרסה שאנחנו רוצים להיות ב-2026. איך היא מדברת? איך היא מרגישה? נתחבר לתדר שלה כבר עכשיו.</p>
            </div>

            <div class="step-arrow"><i class="fa-solid fa-chevron-left"></i></div>

            <!-- Step 4 -->
            <div class="step-card">
                <span class="step-num">04.</span>
                <h3>תוכנית עבודה<br>צעד אחר צעד</h3>
                <p>צעדים קטנים של אומץ. נפרק את החלום לפעולות פשוטות ונעימות, בלי לחץ, רק עשייה מדויקת מתוך ביטחון.</p>
            </div>
        </div>
    </section>

    <!-- DETAILS (MOVED UP) -->
    <div class="container reveal" style="text-align: center;">
        <h2 style="margin-bottom: 30px; text-shadow: 0 0 10px #ff00ff;">איפה ומתי?</h2>
        <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 15px;">
            <div style="background: rgba(255,255,255,0.2); padding: 10px 20px; border-radius: 30px;">📍 29/12 יום שני</div>
            <div style="background: rgba(255,255,255,0.2); padding: 10px 20px; border-radius: 30px;">⏰ 18:30 (כשעתיים וחצי)</div>
            <div style="background: rgba(255,255,255,0.2); padding: 10px 20px; border-radius: 30px;">👥 מספר מקומות מוגבל - אווירה אינטימית</div>
        </div>
        <!-- טיימר ספירה לאחור -->
        <div id="countdown"></div>
    </div>

    <!-- FAQ -->
    <div class="container reveal">
        <h3 style="text-align: center; margin-bottom: 20px;">שאלות נפוצות</h3>
        
        <div class="faq-item">
            <div class="faq-question" onclick="this.parentElement.classList.toggle('active')">
                <span class="faq-icon">▼</span> &nbsp; איך אדע שזה בשבילי?
            </div>
            <div class="faq-answer">אם אתם מרגישים שהשנה הזו עברה לידכם, אם אתם רוצים יותר בהירות ופחות רעש, ואם אתם מוכנים לעצור רגע כדי להתכוונן מחדש – זה בול בשבילכם. זה לא דורש ניסיון קודם, רק לב פתוח.</div>
        </div>

        <div class="faq-item">
            <div class="faq-question" onclick="this.parentElement.classList.toggle('active')">
                <span class="faq-icon">▼</span> &nbsp; מה אם לא נצליח ליישם?
            </div>
            <div class="faq-answer">בדיוק בגלל זה הסדנה בנויה בצעדים קטנים ופרקטיים. אנחנו לא מחפשים "מהפכות" ענקיות ומפחידות, אלא דיוקים קטנים שעושים שינוי גדול. וגם, תהיה לכם את החוברת והקבוצה לתמיכה.</div>
        </div>

        <div class="faq-item">
            <div class="faq-question" onclick="this.parentElement.classList.toggle('active')">
                <span class="faq-icon">▼</span> &nbsp; למי זה מתאים?
            </div>
            <div class="faq-answer">לכל מי שמרגיש/ה צורך לעצור רגע ולתכנן, גם אם מעולם לא עשיתם סדנת התפתחות אישית.</div>
        </div>
        <div class="faq-item">
            <div class="faq-question" onclick="this.parentElement.classList.toggle('active')">
                <span class="faq-icon">▼</span> &nbsp; מה צריך להכין?
            </div>
            <div class="faq-answer">מחברת יפה לכתיבה, עט שכיף לכתוב איתו, מים/תה ומקום שקט שבו תוכלו להתרכז בעצמכם.</div>
        </div>
    </div>

    <!-- CHECKOUT -->
    <div id="checkout" class="container reveal">
        <div class="checkout-section">
            <div class="scarcity-badge">🔥 מחיר השקה לימים הקרובים</div>
            <h2 style="color: #ffffff; font-weight: bold; margin-bottom: 5px;">לתפוס מקום עכשיו</h2>
            
            <div class="price-wrapper">
                <span class="old-price">97 ₪</span>
                <span class="price-tag">65 ₪</span>
            </div>

            <div class="bonuses-list">
                <h4 style="color: #d500f9;">🎁 בונוסים מתנה:</h4>
                <ul>
                    <li>✅ חוברת עבודה דיגיטלית לעבודת עומק</li>
                    <li>✅ קבוצת וואטסאפ אינטימית לשיתופים ותמיכה</li>
                </ul>
            </div>
            
            <p style="font-size: 1rem; color: #ddd; margin-bottom: 20px; margin-top: 30px; font-weight: 500;">
                בחרו איך נוח לכם לשלם:
            </p>

            <div class="payment-options">
                <!-- כפתור ביט -->
                <a href="https://www.bitpay.co.il/app/share-info?i=202438353617_19lBeNTa" class="pay-btn btn-bit" target="_blank">
                    <i class="fa-solid fa-mobile-screen-button"></i> תשלום מהיר ב-Bit
                </a>
                
                <!-- כפתור פייבוקס -->
                <a href="https://links.payboxapp.com/30vp7Oqh7Yb" class="pay-btn btn-paybox" target="_blank">
                    <i class="fa-solid fa-box-open"></i> תשלום מהיר ב-PayBox
                </a>

                <!-- כפתור וואטסאפ -->
                <a href="https://wa.me/972524073915?text=היי%20מדלן,%20אשמח%20להעביר%20ביט/העברה%20ולשריין%20מקום%20💖" class="pay-btn btn-whatsapp" target="_blank">
                    <i class="fa-brands fa-whatsapp"></i> תשלום בהעברה / עזרה
                </a>
            </div>
            <p class="final-note">מתרגשת לראות אתכם! הולך להיות ממלא, מרפא ופותח את הלב.</p>
        </div>
    </div>

    <footer style="text-align: center; padding: 40px 20px; font-size: 0.9rem; opacity: 0.6; margin-top: 50px;">
        <div class="footer-social">
            <a href="https://instagram.com/madlen.frid" target="_blank">
                <i class="fa-brands fa-instagram"></i> madlen.frid
            </a>
        </div>
        <p style="margin-top: 15px;">© כל הזכויות שמורות למדלן 2026</p>
    </footer>

    <script>
        // Scroll Reveal Animation
        const revealElements = document.querySelectorAll('.reveal');
        const revealOnScroll = () => {
            const windowHeight = window.innerHeight;
            const elementVisible = 150;
            revealElements.forEach((element) => {
                const elementTop = element.getBoundingClientRect().top;
                if (elementTop < windowHeight - elementVisible) {
                    element.classList.add('active');
                }
            });
        };
        window.addEventListener('scroll', revealOnScroll);
        revealOnScroll();

        // Countdown Timer
        const targetDate = new Date("Dec 29, 2025 18:30:00").getTime();
        const countdownInterval = setInterval(function() {
            const now = new Date().getTime();
            const distance = targetDate - now;
            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);
            document.getElementById("countdown").innerHTML = `
                <div class="timer-item"><span class="timer-val">${days}</span><span class="timer-label">ימים</span></div>
                <div class="timer-item"><span class="timer-val">${hours}</span><span class="timer-label">שעות</span></div>
                <div class="timer-item"><span class="timer-val">${minutes}</span><span class="timer-label">דקות</span></div>
                <div class="timer-item"><span class="timer-val">${seconds}</span><span class="timer-label">שניות</span></div>
            `;
            if (distance < 0) {
                clearInterval(countdownInterval);
                document.getElementById("countdown").innerHTML = "הסדנה התחילה!";
            }
        }, 1000);
    </script>

</body>
</html>
