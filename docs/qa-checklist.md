# QA-чеклист — EventFlow demo

Использовать перед показом работодателю и после переноса в Elementor.

## Адаптив (mobile first)

| Viewport | Ширина | Проверить |
|----------|--------|-----------|
| Mobile | 375px | Меню hamburger, колонки в 1 ряд, stats 3 col не ломаются |
| Mobile L | 414px | Текст hero не обрезается |
| Tablet | 768px | Pricing 3 col, steps 3 col |
| Desktop | 1200px+ | Horizontal nav, hero 2 col |

- [ ] Нет горизонтального скролла на всех брейкпоинтах
- [ ] Нет «плывущих» блоков (overflow, fixed widths в px на контенте)
- [ ] Кнопки min-height ≥ 44px (touch target)
- [ ] Шрифты читаемы (body ≥ 16px effective)

## Контент и редактируемость

- [ ] Все `data-editable` зоны имеют осмысленный текст
- [ ] Нет lorem ipsum
- [ ] CTA ведут к `#cta` / форме
- [ ] Год в footer актуален (JS)

## Интерактив

- [ ] Меню открывается/закрывается, Escape закрывает
- [ ] FAQ `<details>` раскрывается (или Accordion в Elementor)
- [ ] Форма: demo submit без реальной отправки (или настроен webhook)
- [ ] Focus visible на интерактивных элементах (Tab)

## Производительность

- [ ] Нет тяжёлых библиотек (jQuery, слайдеры)
- [ ] 1 файл CSS, 1 файл JS
- [ ] Шрифт Google Fonts с `display=swap` (или self-host для prod)
- [ ] Изображения: при добавлении — WebP, width ≤ 1920

## Доступность (базово)

- [ ] `lang="ru"` на `<html>`
- [ ] Skip link работает
- [ ] `aria-expanded` на menu toggle
- [ ] Form labels (sr-only или visible)
- [ ] Контраст текста на фоне (WCAG AA для body text)

## Соответствие вакансии

- [ ] Mobile first подход
- [ ] 8 секций по ТЗ
- [ ] Документ `elementor-mapping.md` приложен
- [ ] Кейс Roadshow упоминает поток (~35 мин/стр)
- [ ] Минимум custom JS (только nav + form stub)
- [ ] Готовность к Global Widgets / шаблонам описана в README

## Браузеры (выборочно)

- [ ] Chrome / Edge последний
- [ ] Firefox последний
- [ ] Safari iOS (если есть устройство) или DevTools emulation

## Перед отправкой работодателю

- [ ] `index.html` открывается локально (double-click или Live Server)
- [ ] Ссылка на хостинг (GitHub Pages / Netlify / Vercel) работает
- [ ] В отклике честно: «демо-проект под ваш стек Elementor»
