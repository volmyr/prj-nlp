## Генерація відповідей на фактологічні запитання українською мовою

Нині Siri та Google Assistant англійською та іншими мовами можуть дати пряму відповідь на фактологічні питання. Пошук у Google видає відповідь у формі "картки" над знайденими лінками, на які таким чином не треба клікати. Тим не менш, українською мовою ці функції недоступні. 

Основне завдання проекту - реалізувати питально-відповідальну систему для фактологічних питань на основі (підмножини) української вікіпедії. Наприклад, на питання "Коли помер Шевченко" система відповідатиме "Тарас Шевченко помер 10 березня 1861 року". Це буде knowledge-based або гібридна система (на відміну від Information Retrieval-based систем). Виконання завдання потребуватиме визначення зв'язків між сутностями у вікіпедії (для побудови бази знань) та тренування моделі для обробки питань (які можуть бути задані в різних формах) і пошуку найбільш імовірної відповіді на питання у базі знань.

Додаткове завдання (якщо буде час - так, я знаю що його не буде, але раптом) - створити бота, який зможе грати нескладні питання "Своєї гри" (пострадянського аналога гри Jeopardy, в яку у 2011 році перемогла програма IBM Watson).

Джерела даних:

- Wikipedia та DBPedia, українська версія. DBPedia вже містить RDF-трійки (суб'єкт-предикат-об'єкт) з інфобоксів української вікіпедії.
- Дані з Google Trends для пошуку форм, у яких користувачі формулюють питання.
- Набори питань "Своєї гри" українською мовою.

Етапи роботи:

1. Збір даних для бази знань, насамперед обробка інформації з DBPedia.
2. Побудова тестового набору пар "питання-відповідь" для оцінки моделі через Mean Reciprocal Rank.
3. Побудова заснованої на правилах системи обробки запитання та пошуку відповіді в базі. Ця система слугуватиме за бейзлайнову модель.
4. Застосування сучасних моделей машинного навчання до даних з метою вдосконалення системи. Використання досвіду системи "DeepQA", застосованої в IBM Watson.
5. (можливо) Адаптація готової системи до складнішого завдання - генерації відповідей для "Своєї гри". Тренування моделі на існуючих питаннях.
6. Створення інтерфейсу для системи генерації відповідей (веб і/або Телеграм-бот).

Обмеження проекту:

IBM Watson навіть у 2011 році мав доступ до більших ресурсів для обчислення та для зберігання даних, ніж я маю зараз, тому базу знань для проекту, можливо, буде обмежено тематично.
