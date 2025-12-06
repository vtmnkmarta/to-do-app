# To-do App (React + TypeScript)

Цей репозиторій — простий додаток "To-do" побудований на React + TypeScript.

Коротко:
- Стартовий скрипт: `npm start` (викликає `mate-scripts start -l`)
- Білд: `npm run build`
- Деплой: `npm run deploy`

**Швидкий старт**

1. Встановіть залежності:

```powershell
npm install
```

2. Запустіть дев-сервер (Windows PowerShell):

```powershell
npm start
```

Після запуску серверу відкрийте в браузері `http://localhost:5175/` (порт може змінюватися, якщо стандартні порти зайняті).

Якщо ви хочете використовувати `npm run dev`, додайте у `package.json` скрипт `dev` (наприклад: `"dev": "vite"` або `"dev": "mate-scripts start -l"`).

**Доступні скрипти (в `package.json`)**

- `start` — запускає дев-сервер (`mate-scripts start -l`).
- `build` — збирає проєкт (`mate-scripts build`).
- `style-format` — форматування SCSS через `stylelint`.
- `lint-js` / `lint-css` / `lint` — перевірки та форматування коду.
- `format` — запускає `prettier` для файлів `src/**/*.{ts,tsx}`.
- `postinstall` — оновлює скрипти та перевіряє `cypress`.
- `deploy` — деплой через `mate-scripts deploy` (перед цим виконується `predeploy`, який запускає `build`).

**Рекомендації та примітки**

- Якщо побачите повідомлення `Missing script: "dev"` — використайте `npm start` або додайте `dev` у `scripts`.
- Якщо у терміналі була опечатка `сnpm` — це кириличний символ `с`; використовуйте `npm` латиницею.
- При старті можуть з'являтися інформаційні попередження:
  - `The CJS build of Vite's Node API is deprecated` — інформація про API Vite.
  - `Browserslist: browsers data (caniuse-lite) is X months old` — оновіть базу командою:

```powershell
npx update-browserslist-db@latest
```

  - Sass deprecation: `@import` та legacy JS API. Рекомендується мігрувати SCSS до `@use`/`@forward` у майбутньому, але це не блокує роботу зараз.

**Тестування**

- У проєкті налаштований `cypress` (e2e). Після встановлення залежностей `postinstall` запускає `cypress verify`.

**Розгортання на GitHub Pages**

- Перед деплоєм змініть поле `homepage` у `package.json` на шлях вашого репозиторію (наприклад `/your-repo-name`) якщо хочете публікувати на `gh-pages`.
- Деплой:

```powershell
npm run deploy
```

**Вирішення поширених проблем**

- "Port 5173 is in use, trying another one..." — Vite автоматично підбере інший порт; просто відкрийте Local URL, який виведе сервер.
- "Missing script: \"dev\"" — використайте `npm start` або додайте `dev` у `package.json`.
- Якщо з'являються помилки під час `npm install`, вставте в чат повний вивід терміналу — допоможу розібратися.

**Контрибуція**

Якщо хочете доповнити або змінити проєкт — створіть fork та зробіть pull request. Для локальної розробки дотримуйтеся стилю коду (ESLint / Prettier / Stylelint налаштовані).

**Ліцензія**

Перевірте файл `LICENSE` в корені репозиторію для деталей ліцензування.

---

Якщо хочете, можу:
- Додати скрипт `dev` до `package.json` зараз.
- Запустити `npx update-browserslist-db@latest` у вашому середовищі.
- Мігрувати `@import` → `@use` у SCSS (повністю або по файлах).

Скажіть, яку дію виконати далі.
