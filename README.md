<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>2651</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif;
            background-color: #000; /* Фоновый цвет для поддержки */
            color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
            position: relative;
        }
        /* Псевдоэлемент для наложения цвета */
        body::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('https://raw.githubusercontent.com/uxmei/uxmei.github.io/main/5IUl.gif'); /* Путь к твоему GIF */
            background-repeat: no-repeat;
            background-size: cover;
            filter: brightness(0.5); /* Уменьшение яркости */
            z-index: -2; /* Убедимся, что это под другими элементами */
        }
        .nickname {
            font-size: 3em;
            letter-spacing: 5px;
            margin: 0;
            text-decoration: line-through; /* Зачеркивание текста */
            z-index: 1; /* Слой текста выше фона */
            font-family: 'Arial', sans-serif; /* Заменить на нужный шрифт, если есть */
            transition: color 0.3s;
        }
        .real-name {
            font-size: 1.5em;
            margin: 0;
            font-family: 'Courier New', monospace; /* Здесь можно заменить на другой шрифт */
            z-index: 1; /* Слой текста выше фона */
        }
        img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin-bottom: 20px;
            position: relative;
            z-index: 1; /* Слой фото выше фона */
        }
        img::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border-radius: 50%;
            border: 4px solid #ff0000;
            box-shadow: 0 0 10px 3px #ff0000;
            filter: blur(1px);
            z-index: -1;
            background: rgba(0, 0, 139, 0.4); /* Более темный синий оттенок */
            border-radius: 50%;
        }
        .social-links {
            display: flex;
            gap: 20px;
            z-index: 1; /* Слой ссылок выше фона */
        }
        .social-links a {
            color: #fff;
            text-decoration: none;
            font-size: 1.5em;
            transition: color 0.3s;
        }
        .social-links a:hover {
            color: #ff0000;
        }
    </style>
</head>
<body>

    <img src="https://raw.githubusercontent.com/uxmei/uxmei.github.io/main/2651.jpeg" alt="Твое фото">
    <h1 class="nickname" id="nickname">UXMEI</h1>
    <h2 class="real-name">Георгий</h2>
    <div class="social-links">
        <a href="https://steamcommunity.com/id/aziat_v_stonike" target="_blank">Steam</a>
        <a href="https://www.instagram.com/uxmei52/" target="_blank">Instagram</a>
        <a href="https://vk.com/uxmei" target="_blank">VK</a>
    </div>

    <script>
        const nicknameElement = document.getElementById('nickname');
        const nicknames = [
            "ɄӾ₥Ɇł",
            "𝖚𝖝𝖒𝖊𝖎",
            "?????",
            "𝓾𝔁𝓶𝓮𝓲",
            "𝓤𝓧𝓜𝓔𝓘",
            "𝖀𝖃𝕸𝕰𝕴",
            "UXMEI",
            "uxmei",
            "UxMeI",
            "uXmEi"
        ];
        const hoverNickname = "U҉̮̫͌̇X҈̘͇͖͉̔̊̐M̶̝̬̲̦̔͂ͅE҈̭͕̦̤̪̔̑̍̐̌I̴̟̠͖̙̣̎̎̐";

        function randomGlitch() {
            const randomIndex = Math.floor(Math.random() * nicknames.length);
            nicknameElement.textContent = nicknames[randomIndex];
            const randomInterval = Math.random() * 1000 + 500; // от 0.5 до 1.5 секунд
            setTimeout(randomGlitch, randomInterval);
        }

        nicknameElement.addEventListener('mouseenter', () => {
            const originalText = nicknameElement.textContent; // Сохраняем текущий текст
            let hoverDuration = 0; // Начинаем таймер для наведения
            const hoverInterval = setInterval(() => {
                nicknameElement.textContent = hoverNickname; // Меняем на эффект
                hoverDuration += 500; // Увеличиваем время
                if (hoverDuration >= 2000) {
                    nicknameElement.textContent = originalText; // Возвращаемся к оригинальному
                    clearInterval(hoverInterval); // Останавливаем интервал
                }
            }, 500); // Каждые 0.5 секунд
        });

        randomGlitch(); // Запускаем первый раз
    </script>
    
</body>
</html>
