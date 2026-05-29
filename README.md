# EventFlow — демо-портфолио B2B Events Landing

## Что внутри

| Файл                                                   | Назначение                           |
| ------------------------------------------------------ | ------------------------------------ |
| [index.html](index.html)                               | Готовый лендинг, 8 секций            |
| [assets/css/styles.css](assets/css/styles.css)         | Mobile-first стили, CSS-переменные   |
| [assets/js/main.js](assets/js/main.js)                 | Минимальный JS: меню, форма (демо)   |
| [content/landing-copy.md](content/landing-copy.md)     | Все тексты + AI-промпты              |
| [docs/elementor-mapping.md](docs/elementor-mapping.md) | Перенос в Elementor Pro (контейнеры) |
| [docs/qa-checklist.md](docs/qa-checklist.md)           | Чеклист перед сдачей                 |

## Секции (8)

1. Hero
2. Benefits (4 карточки)
3. How it works (3 шага)
4. Pricing (3 тарифа)
5. Cases (3 кейса, включая roadshow / поток)
6. FAQ (4 вопроса, native `<details>`)
7. Final CTA + форма
8. Footer

## Как открыть локально

1. Откройте `index.html` в браузере
2. Или: `npx serve .` в папке проекта → `http://localhost:3000`

## Соответствие требованиям вакансии

| Требование                    | Реализация                                           |
| ----------------------------- | ---------------------------------------------------- |
| Mobile first                  | CSS от 375px → 768px → 1200px                        |
| Адаптив без «плывущих» блоков | Grid/Flex, clamp(), без фикс. ширин контента         |
| Редактируемость               | `data-editable` на ключевых текстах                  |
| Минимум CSS/JS                | 1 CSS + ~70 строк JS                                 |
| Elementor контейнеры          | [elementor-mapping.md](docs/elementor-mapping.md)    |
| AI в работе                   | Промпты в [landing-copy.md](content/landing-copy.md) |
| Поток 300 стр/мес             | Кейс Roadshow + naming templates в mapping           |
| Без тяжёлых плагинов          | Нет слайдеров, jQuery                                |

## Git и публикация

Репозиторий готов к `git init` (см. `.gitignore`, workflow для GitHub Pages).

### Первый push на GitHub

```bash
cd portfolio-b2b-events
git init
git add .
git commit -m "Add EventFlow B2B landing demo portfolio"
git branch -M main
git remote add origin https://github.com/ВАШ_ЛОГИН/eventflow-demo.git
git push -u origin main
```

### GitHub Pages (бесплатный URL для HH)

1. Создайте репозиторий на GitHub (пустой, без README).  
2. Выполните команды выше.  
3. **Обязательно до первого деплоя:** откройте репозиторий → **Settings → Pages** → в блоке **Build and deployment** выберите **Source: GitHub Actions** (не «Deploy from branch»).  
4. **Actions** → workflow **Deploy to GitHub Pages** → **Re-run all jobs** (или сделайте новый `git push`).  
5. URL будет вида: `https://ВАШ_ЛОГИН.github.io/ИМЯ-РЕПО/`

#### Ошибка `Get Pages site failed` / `Not Found`

Это значит, что **Pages ещё не включены** или источник не **GitHub Actions**.

**Исправление (2 минуты):**
1. **Settings → Pages**  
2. **Build and deployment → Source:** **GitHub Actions**  
3. Если пункта нет — сначала сделайте репозиторий **Public** (для бесплатного Pages на личном аккаунте).  
4. **Actions** → упавший run → **Re-run all jobs**

### Альтернатива без Actions (проще)

**Settings → Pages → Deploy from branch → Branch `main` → Folder `/ (root)`** → Save.  
Workflow можно не использовать — достаточно `index.html` в корне. Сайт обновится через 1–2 минуты после push.

### Netlify / Vercel

Перетащите папку на [netlify.com/drop](https://app.netlify.com/drop) или импортируйте репозиторий — root directory: `/`.

## Сопроводительное (фрагмент)

> Демо под ваш стек: [URL]. Mobile first, 8 секций, минимум кастомного кода.  
> Готов перенести в Elementor Pro (контейнеры) — приложена карта переноса.  
> При 300 стр/мес — шаблоны + Global Widgets + ИИ; ориентир от 120 000 ₽ до вычета.

## Автор

Демо-проект портфолио · Алим · 2026
