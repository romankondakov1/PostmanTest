# API Course Homework

Цей репозиторій створений для домашнього завдання з курсу тестування API. Він містить:

- колекції Postman для прогону API-тестів,
- файли з прикладами JavaScript,
- результати запусків Newman.

## Де що знаходиться

- `HWPostmanTests/` — основна папка для запуску тестів Newman.
- `HWPostmanTests/package.json` — залежності для Newman та HTML-репортера.
- `Tests/Roma.postman_collection.json` — колекція Postman для запуску.
- `newman/` — папка для звітів, збережених після прогону.
- `HomeWork1/` — додаткові домашні завдання на JavaScript.

## Встановлення

З кореневої папки репозиторію виконайте:

```powershell
npm install
```

Якщо потрібно встановити лише залежності для тестів Postman, перейдіть у папку `HWPostmanTests`:

```powershell
cd HWPostmanTests
npm install
```

## Запуск тестів Newman

Запустити колекцію з кореня репозиторію:

```powershell
npx newman run HWPostmanTests\Roma.postman_collection.json -r html
```

Якщо ви вже у папці `HWPostmanTests`, виконайте:

```powershell
npx newman run Roma.postman_collection.json -r html
```

## Звіт

Прапорець `-r html` генерує HTML-звіт. Після запуску звіт з?явиться в поточній директорії. Щоб зберегти звіт у папці `newman`, можна вказати шлях:

```powershell
npx newman run HWPostmanTests\Roma.postman_collection.json -r html --reporter-html-export newman\report.html
```

## Корисні зауваження

- Переконайтеся, що Node.js та npm встановлені.
- `npx` використовує локально встановлений `newman`, якщо він є, або завантажує його тимчасово.
- Для додавання нових тестів можна покласти колекції в `Tests/` і запускати їх аналогічно.
