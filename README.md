<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Trozzy</title>
  <script src="https://telegram.org/js/telegram-web-app.js"></script>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #1f1f1f;
      color: #fff;
      padding: 20px;
    }
    h2 {
      color: #00ffcc;
    }
    .section {
      margin-bottom: 25px;
    }
    textarea {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      resize: none;
    }
    button {
      padding: 10px 20px;
      margin-top: 10px;
      background-color: #00ffcc;
      border: none;
      color: #000;
      font-weight: bold;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>Trozzy</h1>

  <div class="section">
    <h2>Bio</h2>
    <p>Nickname: Trozzy<br>Country: 🇲🇩<br><br>Один из владельцев крупного скрытого проекта по софтам, а также по заработку денег.<br>Менеджер: <a href="https://t.me/bestcrimes" target="_blank">@bestcrimes</a></p>
  </div>

  <div class="section">
    <h2>Проекты</h2>
    <ul>
      <li>SVT</li>
      <li>Neffa Casino</li>
      <li>Neffa Sale</li>
      <li>Neffa Project</li>
      <li>И много софтов и ботов написанных мною</li>
    </ul>
  </div>

  <div class="section">
    <h2>Чем я занимаюсь</h2>
    <ol>
      <li>Создаю ботов</li>
      <li>Создаю читы, скрипты на мобильные и ПК игры</li>
      <li>Работаю менеджером в крупных командах</li>
      <li>Создаю дизайн интерьеров и веб-дизайн</li>
    </ol>
    <p>Сотрудничество: <a href="https://t.me/bestcrimes" target="_blank">@bestcrimes</a></p>
  </div>

  <div class="section">
    <h2>Задать вопрос</h2>
    <textarea id="question" rows="4" placeholder="Введите ваш вопрос..."></textarea>
    <button onclick="sendQuestion()">Отправить</button>
  </div>

  <script>
    function sendQuestion() {
      const question = document.getElementById("question").value;
      if (!question.trim()) {
        alert("Введите вопрос");
        return;
      }

      const tg = window.Telegram.WebApp;
      tg.sendData(JSON.stringify({ type: "ask", text: question }));
      tg.close();
    }
  </script>
</body>
</html>
