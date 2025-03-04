<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lotte Hotels Reviews | Отзывы</title>
    <style>
        body {
            background-color: #867669;
            color: white;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        .logo {
            text-align: center;
            margin-bottom: 40px;
        }
        .logo img {
            max-width: 200px;
        }
        .reviews-section {
            margin-bottom: 50px;
            display: none; 
        }
        .review-links {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        .review-link {
            background: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            transition: background 0.3s ease;
        }
        .review-link:hover {
            background: rgba(255, 255, 255, 0.2);
        }
        .review-link a {
            color: white;
            text-decoration: none;
            font-size: 18px;
            display: block;
            padding: 10px;
        }
        .language-switch {
            text-align: right;
            margin-bottom: 20px;
        }
        .language-button {
            background: none;
            border: 2px solid white;
            color: white;
            padding: 8px 16px;
            margin-left: 10px;
            cursor: pointer;
            border-radius: 5px;
            font-size: 16px;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        .language-button.active {
            background: white;
            color: #867669;
        }
        .language-button:hover {
            background: rgba(255, 255, 255, 0.1);
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="language-switch">
            <button onclick="switchLanguage('ru')" class="language-button active" id="ru-btn">RU</button>
            <button onclick="switchLanguage('en')" class="language-button" id="en-btn">EN</button>
        </div>
        <div class="logo">
            <img src="https://i.ibb.co/wNZTK2f0/gnb-logo-hotels.png" alt="Lotte Hotels Logo">
        </div>

        <!-- Russian Version -->
        <div class="reviews-section" lang="ru">
            <h1>Поделитесь своими впечатлениями</h1>
            <p>Мы ценим ваше мнение! Ознакомьтесь с отзывами наших гостей или оставьте свой отзыв на любой из этих платформ:</p>
            <div class="review-links">
                <div class="review-link">
                    <a href="https://www.tripadvisor.ru/UserReviewEdit-g298507-d12238367-Lotte_Hotel_St_Petersburg-St_Petersburg_Northwestern_District.html" target="_blank">Отзывы на TripAdvisor</a>
                </div>
                <div class="review-link">
                    <a href="https://www.google.com/search?hl=ru-RU&gl=ru&q=Lotte+Hotel+St.Petersburg,+Pereulok+Antonenko,+2,+St+Petersburg,+190000&ludocid=8205268314045433897&lsig=AB86z5Ucd1wkbEisI8_VKB-Hry_L#lrd=0x469631034b662bf1:0x71def80ee9724829,3" target="_blank">Отзывы на Google</a>
                </div>
                <div class="review-link">
                    <a href="https://2gis.ru/spb/firm/70000001027485962/tab/reviews?m=30.31061%2C59.931664%2F16&immersive=on" target="_blank">Отзывы на 2ГИС</a>
                </div>
                <div class="review-link">
                    <a href="https://yandex.ru/maps/org/lotte/69646388992/?ll=30.311168%2C59.931462&utm_source=share&z=17" target="_blank">Отзывы на Яндекc</a>
                </div>
            </div>
        </div>

        <!-- English Version -->
        <div class="reviews-section" lang="en">
            <h1>Share your experience</h1>
            <p>We value your feedback! Check out what our guests say about us or leave your own review on any of these platforms:</p>
            <div class="review-links">
                <div class="review-link">
                    <a href="https://www.tripadvisor.com/UserReviewEdit-g298507-d12238367-Lotte_Hotel_St_Petersburg-St_Petersburg_Northwestern_District.html" target="_blank">TripAdvisor Reviews</a>
                </div>
                <div class="review-link">
                    <a href="https://www.google.com/search?hl=en-RU&gl=ru&q=Lotte+Hotel+St.Petersburg,+Pereulok+Antonenko,+2,+St+Petersburg,+190000&ludocid=8205268314045433897&lsig=AB86z5Ucd1wkbEisI8_VKB-Hry_L#lrd=0x469631034b662bf1:0x71def80ee9724829,3" target="_blank">Google Reviews</a>
                </div>
                <div class="review-link">
                    <a href="https://2gis.ru/spb/firm/70000001027485962/tab/reviews?m=30.31061%2C59.931664%2F16&immersive=on" target="_blank">2GIS Reviews</a>
                </div>
                <div class="review-link">
                    <a href="https://yandex.com/maps/org/lotte/69646388992/?ll=30.311168%2C59.931462&utm_source=share&z=17" target="_blank">Yandex Reviews</a>
                </div>
            </div>
        </div>
    </div>

    <script>
        switchLanguage('ru');
		function switchLanguage(lang) {
            document.getElementById('ru-btn').classList.toggle('active', lang === 'ru');
            document.getElementById('en-btn').classList.toggle('active', lang === 'en');
            document.querySelectorAll('.reviews-section').forEach(section => {
                section.style.display = section.getAttribute('lang') === lang ? 'block' : 'none';
            });
        }
    </script>
</body>
</html>
