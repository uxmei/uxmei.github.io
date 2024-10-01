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
            background-color: #000;
            color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
            position: relative;
            text-align: center; /* Центрируем текст */
        }
        body::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('https://raw.githubusercontent.com/uxmei/uxmei.github.io/main/5IUl.gif');
            background-repeat: no-repeat;
            background-size: cover;
            filter: brightness(0.5);
            z-index: -2;
        }
        .nickname {
            font-size: 3em;
            letter-spacing: 5px;
            margin: 10px 0; /* Добавляем немного отступа */
            text-decoration: line-through;
            z-index: 1;
        }
        .real-name {
            font-size: 1.5em;
            margin: 10px 0; /* Убираем лишние отступы */
            font-family: 'Courier New', monospace;
            z-index: 1;
        }
        img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
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
            background: rgba(0, 0, 139, 0.4);
        }
        .social-links {
            display: flex;
            justify-content: center; /* Центрируем ссылки */
            gap: 20px;
            z-index: 1;
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
    <h1 class="nickname" id="nickname">U҉̮̫͌̇X҈̘͇͖͉̔̊̐M̶̝̬̲̦̔͂ͅE҈̭͕̦̤̪̔̑̍̐̌I̴̟̠͖̙̣̎̎̐</h1>
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
