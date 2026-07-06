# lavida
<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>La Vida Events | מתחם אירועים יוקרתי בעומר</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #d4af37; /* זהב יוקרתי */
            --secondary: #f3e5ab; /* זהב בהיר / פנינה */
            --dark-bg: #0d0d11; /* שחור עמוק */
            --card-bg: #16161f; /* גרפיט כהה */
            --text-light: #e0e0e6;
        }

        body {
            background-color: var(--dark-bg);
            color: #ffffff;
            overflow-x: hidden;
            line-height: 1.6;
        }

        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(13, 13, 17, 0.95);
            backdrop-filter: blur(8px);
            z-index: 1000;
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 20px;
        }

        .logo {
            font-size: 26px;
            font-weight: 800;
            letter-spacing: 1px;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .nav-links a {
            color: #ffffff;
            text-decoration: none;
            margin-right: 25px;
            font-weight: 600;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        /* מסך הבית - משתמש בתמונת הבריכה המטורפת שלכם מהקישורים */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.5), var(--dark-bg)), 
                        url('https://i.ibb.co/wh9L82pw/Whats-App-Image-2026-07-06-at-22-53-08.jpg') center/cover no-repeat;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 20px;
        }

        .hero-content h1 {
            font-size: 4.5rem;
            margin-bottom: 10px;
            text-shadow: 0 4px 15px rgba(0,0,0,0.8);
            background: linear-gradient(45deg, #ffffff, var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-content .subtitle {
            font-size: 1.8rem;
            color: var(--primary);
            margin-bottom: 20px;
            text-shadow: 0 2px 10px rgba(0,0,0,0.5);
        }

        .hero-content .location {
            font-size: 1.2rem;
            color: var(--text-light);
            margin-bottom: 35px;
        }

        .btn {
            display: inline-block;
            padding: 14px 40px;
            background: linear-gradient(45deg, #bxaf37, var(--primary));
            background-color: var(--primary);
            color: #0d0d11;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.1rem;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 4px 20px rgba(212, 175, 55, 0.3);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 25px rgba(212, 175, 55, 0.6);
            color: #000;
        }

        .btn-whatsapp {
            background: linear-gradient(45deg, #25d366, #128c7e);
            color: white;
            box-shadow: 0 4px 20px rgba(37, 211, 102, 0.3);
            margin-top: 20px;
        }

        .btn-whatsapp:hover {
            box-shadow: 0 6px 25px rgba(37, 211, 102, 0.5);
            color: white;
        }

        section {
            padding: 90px 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.8rem;
            margin-bottom: 15px;
            background: linear-gradient(45deg, #ffffff, var(--primary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .section-subtitle {
            text-align: center;
            color: var(--text-light);
            margin-bottom: 50px;
            font-size: 1.2rem;
        }

        .about-box {
            background: var(--card-bg);
            padding: 40px;
            border-radius: 20px;
            border: 1px solid rgba(212, 175, 55, 0.1);
            margin-bottom: 40px;
            text-align: center;
        }

        .about-box p {
            font-size: 1.2rem;
            color: var(--text-light);
            max-width: 900px;
            margin: 0 auto 30px;
        }

        .tags-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
        }

        .tag {
            background: rgba(212, 175, 55, 0.08);
            border: 1px solid var(--primary);
            padding: 8px 20px;
            border-radius: 25px;
            font-size: 1rem;
            font-weight: 600;
            color: var(--secondary);
        }

        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .card {
            background: var(--card-bg);
            padding: 35px;
            border-radius: 15px;
            border: 1px solid rgba(255,255,255,0.03);
            transition: all 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: var(--primary);
        }

        .card h3 {
            color: var(--primary);
            font-size: 1.4rem;
            margin-bottom: 15px;
        }

        .card ul {
            list-style: none;
        }

        .card ul li {
            margin-bottom: 10px;
            position: relative;
            padding-right: 20px;
            color: var(--text-light);
        }

        .card ul li::before {
            content: "✓";
            position: absolute;
            right: 0;
            color: var(--primary);
            font-weight: bold;
        }

        .specs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .spec-item {
            background: rgba(255, 255, 255, 0.02);
            padding: 20px;
            border-radius: 12px;
            text-align: center;
            border: 1px solid rgba(212, 175, 55, 0.05);
        }

        .spec-item .icon {
            font-size: 2rem;
            margin-bottom: 10px;
            display: block;
        }

        /* גלריית תמונות חכמה ורספונסיבית */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .gallery-item {
            height: 280px;
            border-radius: 15px;
            overflow: hidden;
            position: relative;
            border: 1px solid rgba(212, 175, 55, 0.1);
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.08);
        }

        .gallery-item .overlay-text {
            position: absolute;
            bottom: 0;
            width: 100%;
            background: linear-gradient(transparent, rgba(13,13,17,0.95));
            padding: 15px;
            font-size: 1rem;
            font-weight: bold;
            text-align: center;
            color: var(--secondary);
        }

        .important-notice {
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 15px;
            margin-top: 40px;
        }

        .important-notice h3 {
            color: var(--primary);
            margin-bottom: 15px;
        }

        .important-notice ul {
            list-style-type: none;
        }

        .important-notice ul li {
            margin-bottom: 8px;
            color: var(--text-light);
        }

        .contact-section {
            text-align: center;
            background: linear-gradient(rgba(13, 13, 17, 1), rgba(212, 175, 55, 0.05));
            border-radius: 30px;
            padding: 60px 20px;
        }

        .phone-number {
            font-size: 3.5rem;
            color: #ffffff;
            text-decoration: none;
            display: block;
            margin: 25px 0;
            font-weight: bold;
            transition: color 0.3s;
            background: linear-gradient(45deg, #ffffff, var(--primary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .phone-number:hover {
            color: var(--primary);
        }

        .address-text {
            font-size: 1.3rem;
            color: var(--text-light);
            margin-bottom: 20px;
        }

        footer {
            text-align: center;
            padding: 40px 20px;
            border-top: 1px solid rgba(212, 175, 55, 0.1);
            color: #555;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .hero-content h1 { font-size: 2.8rem; }
            .nav-links { display: none; }
            .phone-number { font-size: 2.5rem; }
        }
    </style>
</head>
<body>

    <header>
        <div class="nav-container">
            <div class="logo">La Vida Events</div>
            <nav class="nav-links">
                <a href="#about">על המתחם</a>
                <a href="#specs">מה במתחם</a>
                <a href="#gallery">גלריה</a>
                <a href="#contact">להזמנות</a>
            </nav>
        </div>
    </header>

    <section class="hero">
        <div class="hero-content">
            <h1>La Vida Events</h1>
            <div class="subtitle">מתחם אירועים פרטיים יוקרתי וחדש</div>
            <div class="location">מושב עומר, רחוב נורית 2</div>
            <a href="#contact" class="btn">שריינו תאריך עכשיו</a>
        </div>
    </section>

    <section id="about">
        <div class="about-box">
            <h2 class="section-title">ברוכים הבאים ל-La Vida Events</h2>
            <p>
                מתחם אירועים פרטי וחדש בעומר, המשלב בריכה מרשימה, מתחם ישיבה מעוצב ואבזור מלא, 
                כדי שתוכלו ליהנות מאירוע באווירה מושלמת ובלי להתפשר על שום פרט. המתחם מיועד לעד 30 אורחים 
                ומעניק לכם פרטיות מלאה, כך שכל המקום עומד לרשותכם בלבד.
            </p>
            <div class="tags-container">
                <span class="tag">✓ מתחם חדש ומעוצב</span>
                <span class="tag">✓ עד 30 אורחים</span>
                <span class="tag">✓ ללא לינה</span>
                <span class="tag">✓ פרטיות מלאה לכל אירוע</span>
            </div>
        </div>

        <div class="grid-3">
            <div class="card">
                <h3>מתאים למגוון אירועים</h3>
                <ul>
                    <li>ימי הולדת</li>
                    <li>מסיבות רווקים ורווקות</li>
                    <li>אירועי חברה וגיבוש</li>
                    <li>אירועי חיילים וחיילות</li>
                    <li>מסיבות פרטיות ומשפחתיות</li>
                </ul>
            </div>

            <div class="card">
                <h3>מפרט המקום המושלם</h3>
                <ul>
                    <li>בריכת שחייה ענקית 11X5 מטר</li>
                    <li>מפלי מים וג'טים מפנקים</li>
                    <li>סאונה יבשה מקצועית</li>
                    <li>מיטות שיזוף, ערסל ופינות ישיבה</li>
                </ul>
            </div>

            <div class="card">
                <h3>כל מה שצריך לאירוע</h3>
                <ul>
                    <li>מערכת הגברה מקצועית ועמדת DJ</li>
                    <li>מקרן ענק ומסך להקרנות</li>
                    <li>פינת מנגל גחלים ופינת מנגל גז</li>
                    <li>רשת אינטרנט אלחוטית (WiFi)</li>
                </ul>
            </div>
        </div>
    </section>

    <section id="specs" style="background: rgba(255,255,255,0.01); border-radius: 20px;">
        <h2 class="section-title" style="font-size: 2.2rem;">אבזור ומפרט טכני</h2>
        <div class="specs-grid">
            <div class="spec-item"><span class="icon">♿</span>גישה לנכים</div>
            <div class="spec-item"><span class="icon">🔊</span>מערכת הגברה ועמדת DJ</div>
            <div class="spec-item"><span class="icon">📽️</span>מקרן ומסך ענק</div>
            <div class="spec-item"><span class="icon">🚿</span>חדר רחצה ושירותים</div>
            <div class="spec-item"><span class="icon">📶</span>Free WiFi</div>
            <div class="spec-item"><span class="icon">🏊</span>בריכה 11X5 עם מפלים</div>
            <div class="spec-item"><span class="icon">🔥</span>סאונה יבשה</div>
            <div class="spec-item"><span class="icon">🍖</span>מנגל גז וגחלים</div>
        </div>
    </section>

    <!-- גלריית התמונות המלאה של המתחם באמצעות הקישורים הישירים שלך -->
    <section id="gallery">
        <h2 class="section-title">גלריית תמונות מהמתחם</h2>
        <p class="section-subtitle">הצצה אמיתית מתוך La Vida Events</p>
        <div class="gallery-grid">
            <div class="gallery-item">
                <img src="https://i.ibb.co/mFFFQjzm/Whats-App-Image-2026-07-06-at-22-53-09-8.jpg" alt="בריכה רחבה בשעות היום">
                <div class="overlay-text">בריכת שחייה גדולה ומפלי מים זורמים</div>
            </div>
            <div class="gallery-item">
                <img src="https://i.ibb.co/wFJvkVqv/Whats-App-Image-2026-07-06-at-22-53-09-3.jpg" alt="מתחם ישיבה יוקרתי ומקרן">
                <div class="overlay-text">מתחם לאונג' מקורה עם מקרן ענק ומערכת שמע</div>
            </div>
            <div class="gallery-item">
                <img src="https://i.ibb.co/wh9L82pw/Whats-App-Image-2026-07-06-at-22-53-08.jpg" alt="בריכה מוארת בלילה">
                <div class="overlay-text">אווירת לילה קסומה ומוארת סביב הבריכה</div>
            </div>
            <div class="gallery-item">
                <img src="https://i.ibb.co/WW9C3jJ5/Whats-App-Image-2026-07-06-at-22-53-08-1.jpg" alt="סאונה יבשה">
                <div class="overlay-text">סאונה יבשה מעץ בחצר המתחם</div>
            </div>
            <div class="gallery-item">
                <img src="https://i.ibb.co/WvKYz2kH/Whats-App-Image-2026-07-06-at-22-53-09-5.jpg" alt="מיטת שיזוף מפנקת">
                <div class="overlay-text">מיטות שיזוף וריהוט גן יוקרתי על מדשאה ירוקה</div>
            </div>
            <div class="gallery-item">
                <img src="https://i.ibb.co/Df24jhmz/Whats-App-Image-2026-07-06-at-22-53-09-9.jpg" alt="מבט מלא על החצר והבריכה">
                <div class="overlay-text">פינות ישיבה ומרחב פתוח ומפנק</div>
            </div>
            <div class="gallery-item">
                <img src="https://i.ibb.co/SXNH276x/Whats-App-Image-2026-07-06-at-22-53-09-1.jpg" alt="חצר ומדשאה">
                <div class="overlay-text">מדשאות מטופחות ואזור משחקים רחב</div>
            </div>
            <div class="gallery-item">
                <img src="https://i.ibb.co/zTw6WRYs/Whats-App-Image-2026-07-06-at-22-53-09-2.jpg" alt="פינת מנגל ואזור בישול">
                <div class="overlay-text">מתחם מנגל גז וגחלים מאובזר</div>
            </div>
            <div class="gallery-item">
                <img src="https://i.ibb.co/gb0qqbt3/Whats-App-Image-2026-07-06-at-22-53-09-4.jpg" alt="מיטות שיזוף ליד הבריכה">
                <div class="overlay-text">עיצוב נקי ויוקרתי המשרה חופש מוחלט</div>
            </div>
            <div class="gallery-item">
                <img src="https://i.ibb.co/ymj7h9cJ/Whats-App-Image-2026-07-06-at-22-53-09-6.jpg" alt="בריכה וזילוני מים">
                <div class="overlay-text">מפלי מים וג'טים מעוצבים</div>
            </div>
            <div class="gallery-item">
                <img src="https://i.ibb.co/ymnQmSv3/Whats-App-Image-2026-07-06-at-22-53-09-7.jpg" alt="מבט נוסף לבריכה">
                <div class="overlay-text">חוויה מושלמת של מסיבות ופרטיות</div>
            </div>
            <div class="gallery-item">
                <img src="https://i.ibb.co/999FcQv9/Whats-App-Image-2026-07-06-at-22-53-09.jpg" alt="שער כדורגל ומדשאה">
                <div class="overlay-text">מדשאה סינתטית איכותית ומתקני פנאי</div>
            </div>
        </div>

        <div class="important-notice">
            <h3>⚠️ מידע נוסף:</h3>
            <ul>
                <li>• למקום קיימת נגישות חלקית, הכוללת מדרגה אחת בלבד בכניסה.</li>
                <li>• ניתן להוסיף בתאום מראש שמשיות למקום.</li>
            </ul>
        </div>
    </section>

    <section id="contact" class="contact-section">
        <h2 class="section-title">חייגו אלינו, שריינו תאריך, ובואו לחגוג!</h2>
        <p class="address-text">📍 מושב עומר, רחוב נורית 2</p>
        <a href="tel:0554307251" class="phone-number">055-4307251</a>
        <a href="https://wa.me/972554307251?text=היי,%20אשמח%20לקבל%20פרטים%20נוספים%20ולשריין%20תאריך%20ב-La%20Vida%20Events%20בעומר" class="btn btn-whatsapp" target="_blank">לחצו כאן להודעה בוואטסאפ</a>
    </section>

    <footer>
        <p>© 2026 La Vida Events. כל הזכויות שמורות.</p>
    </footer>

</body>
</html>
וילת מסיבות בדרום
