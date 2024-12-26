<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Обо мне</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            margin: 0;
            font-family: 'Roboto', sans-serif;
            background: #ff0000; /* Красный фон */
            color: #fff;
            overflow-x: hidden;
        }

        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(0, 0, 0, 0.7);
            padding: 10px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        nav img {
            height: 50px; /* Размер аватарки */
            border-radius: 50%;
        }

        nav ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
            gap: 20px;
        }

        nav ul li a {
            text-decoration: none;
            color: #fff;
            font-weight: bold;
            transition: color 0.3s ease;
        }

        nav ul li a:hover {
            color: #ffd700;
        }

        .main-section {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        .main-section h1 {
            font-size: 4rem;
            margin: 0;
            color: #007bff; /* Синий цвет для заголовка */
            animation: fadeIn 2s ease-in-out;
        }

        .main-section p {
            font-size: 1.5rem;
            margin-top: 10px;
            background: linear-gradient(45deg, #ff0000, #00ff00, #0000ff, #ffff00);
            -webkit-background-clip: text;
            color: transparent;
            animation: fadeIn 2s ease-in-out;
        }

        @keyframes arrow-bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0);
            }
            40% {
                transform: translateY(-10px);
            }
            60% {
                transform: translateY(-5px);
            }
        }

        .main-section .arrow {
            margin-top: 20px;
            font-size: 2rem;
            animation: arrow-bounce 2s infinite;
            color: #ffd700; /* Золотистый цвет стрелки */
        }

        .about {
            padding: 50px 20px;
            background: rgba(0, 0, 0, 0.8);
            text-align: center;
            opacity: 0; /* Для анимации появления */
            transform: translateY(50px);
            transition: opacity 1s ease, transform 1s ease;
        }

        .about.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .about h2 {
            margin-bottom: 20px;
            font-size: 2.5rem;
            background: linear-gradient(45deg, #ff0000, #00ff00, #0000ff, #ffff00);
            -webkit-background-clip: text;
            color: transparent;
        }

        .about p {
            line-height: 1.8;
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto;
            color: #fff;
        }

        #projects {
            padding: 50px 20px;
            background: rgba(0, 0, 0, 0.9);
            color: #fff;
            text-align: center;
        }

        #projects h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        #projects .project {
            margin-bottom: 20px;
        }

        #contact {
            padding: 50px 20px;
            text-align: center;
            background: rgba(0, 0, 0, 0.8);
        }

        #contact h2 {
            margin-bottom: 20px;
            font-size: 2.5rem;
        }

        #contact form {
            display: flex;
            flex-direction: column;
            gap: 10px;
            max-width: 500px;
            margin: 0 auto;
        }

        #contact input, #contact textarea, #contact button {
            padding: 10px;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
        }

        #contact button {
            background: #007bff;
            color: #fff;
            cursor: pointer;
        }

        footer {
            background: rgba(0, 0, 0, 0.9);
            color: #fff;
            padding: 20px;
            text-align: center;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 10px;
        }

        .social-links a {
            text-decoration: none;
            color: #ffd700;
            font-size: 1.2rem;
            font-weight: bold;
            border: 1px solid #ffd700;
            padding: 5px 10px;
            border-radius: 5px;
            transition: background 0.3s ease, color 0.3s ease;
        }

        .social-links a:hover {
            background: #ffd700;
            color: #000;
        }

        #back-to-top {
            display: none;
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: #007bff;
            color: #fff;
            border: none;
            padding: 10px 15px;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <nav>
        <img src="avatar.jpg" alt="Avatar"> <!-- Аватарка -->
        <ul>
            <li><a href="#about">Обо мне</a></li>
            <li><a href="#projects">Проекты</a></li>
            <li><a href="#contact">Контакты</a></li>
        </ul>
    </nav>
    
    <section class="main-section">
        <h1>Krypton</h1>
        <p>Анархист и разработчик</p>
        <div class="arrow">⬇️</div> <!-- Стрелка вниз -->
    </section>
    
    <section class="about" id="about">
        <h2>Обо мне</h2>
        <p>
            <span style="color: #00ffff;">Псевдоним:</span> Krypton <br>
            <span style="color: #ff00ff;">Что учу:</span> Пентестинг (ИБ) <br>
            <span style="color: #ffff00;">Хобби:</span> Играю в Rust с 10 до 23:00
        </p>
    </section>

    <section id="projects">
        <h2>Мои проекты</h2>
        <div class="project">
            <h3>Проект 1</h3>
            <p>Не сделан</p>
            <a href="https://project1-link.com" target="_blank">Посмотреть</a>
        </div>
        <div class="project">
            <h3>Проект 2</h3>
            <p>Не сделан</p>
            <a href="https://project2-link.com" target="_blank">заценить</a>
        </div>
    </section>

    <section id="contact">
        <h2>Связаться со мной</h2>
        <form action="https://formsubmit.co/YOUR_EMAIL" method="POST">
            <input type="text" name="name" placeholder="Ваше имя" required>
            <input type="email" name="email" placeholder="Ваш email" required>
            <textarea name="message" placeholder="Ваше сообщение" required></textarea>
            <button type="submit">Отправить</button>
        </form>
    </section>

    <footer>
        <p>Мои соцсети:</p>
        <div class="social-links">
            <a href="https://steamcommunity.com/profiles/76561199498224495/" target="_blank">Тык на мой стим</a>
            <a href="https://instagram.com" target="_blank">Тык на мой Instagram</a>
            <a href="t.me/Cheplburnet" target="_blank">Тык на мой Telegram</a>
        </div>
    </footer>

    <button id="back-to-top">⬆️</button>

    <script>
        const backToTopButton = document.getElementById('back-to-top');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 300) {
                backToTopButton.style.display = 'block';
            } else {
                backToTopButton.style.display = 'none';
            }
        });

        backToTopButton.addEventListener('click', () => {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });

        document.addEventListener('scroll', () => {
            const aboutSection = document.querySelector('.about');
            const rect = aboutSection.getBoundingClientRect();
            if (rect.top < window.innerHeight) {
                aboutSection.classList.add('visible');
            }
        });
    </script>
</body>
</html>
