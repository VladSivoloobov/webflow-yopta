# Webflow Utility

Утилита для автоматизации работы с эмбедами Webflow. Она позволяет:

- Вытягивать эмбеды из дизайнера Webflow в ваш редактор кода.
- Отправлять обратно модифицированные эмбеды в Webflow.

## Основные команды

- `npm run pull` — вытягивает эмбеды из Webflow и сохраняет их локально.
- `npm run push` — отправляет модифицированные эмбеды обратно в Webflow.

⚠️ **Важно:**

1. **Синхронизация изменений.** При каждом изменении сайта необходимо запускать `npm run pull`, чтобы синхронизировать локальную копию сайта Webflow с актуальной удаленной версией. Пропустите этот шаг — и готовьтесь к драмам, когда случайно перезатрете свои правки.
2. **Риск перезаписи.** Если пропустить синхронизацию из прошлого пункта, при запуске `npm run push` вы можете перезаписать изменения, внесенные через Webflow.
3. **Эмбеды в компонентах** пока не поддерживаются. Они как родственники на праздниках: находятся где-то отдельно и требуют отдельного подхода. Но не переживайте — в будущих версиях это исправим.

---

## Установка

1. Установите [Node.js](https://nodejs.org) последней версии.
2. Выполните установку зависимостей:
   ```bash
   npm i
   ```
3. Настройте конфигурационный файл в папке `config/default.json`:

   ```json
   {
     "cookies": "здесь нужны ваши куки авторизации вебфлоу",
     "projectName": "здесь нужно имя проекта вебфлоу",
     "homepageId": "здесь надо добавить айди домашней страницы",
     "xsrf-token": "добавьте xsrf-token"
   }
   ```

---

Теперь вы готовы использовать утилиту для упрощения работы с эмбедами Webflow! Помните: эта утилита — ваш верный помощник в борьбе с хаосом. Пусть она работает, пока вы пьете кофе или просто наслаждаетесь жизнью.

---

**Анекдот напоследок:**

Разработчик Webflow, уставший после очередного правки кастомного кода, говорит коллеге:
— Знаешь, в Webflow всё возможно!
Коллега удивляется:
— Даже идеально настроить адаптивность?
Разработчик вздыхает:
— Ну, всё, кроме этого...
