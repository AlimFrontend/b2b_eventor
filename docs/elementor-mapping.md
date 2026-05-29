# Карта переноса HTML → Elementor Pro (контейнеры)

Демо: **EventFlow** · WordPress + Elementor Pro · **Flexbox Containers only** (без Section/Column).

## Глобальные настройки Site Settings

| Токен CSS | Elementor Global | Значение |
|-----------|------------------|----------|
| `--color-accent` | Primary | `#3d7cff` |
| `--color-bg` | Background (body) | `#0c0f14` |
| `--font-sans` | Typography Body | DM Sans |
| Кнопки `.btn--primary` | Buttons | Padding 10/20, radius 8px |
| Container max | Layout Width | 1152px (72rem) |

**Global Widgets (создать один раз):**
1. `GW / Button Primary` — кнопка CTA
2. `GW / Button Outline` — вторичная
3. `GW / Card Surface` — контейнер с фоном `#1a2230`, border, radius 12px
4. `GW / Section Header` — eyebrow + H2 + lead
5. `GW / Logo Header` — логотип + текст EventFlow

---

## Структура страницы

```
Page: EventFlow Landing
├── Header (Theme Builder или верх страницы)
├── Main sections (8)
└── Footer (Theme Builder)
```

---

## Секция 1: Header `data-section="header"`

| HTML | Elementor |
|------|-----------|
| `.site-header` | Container (Full Width), direction row, sticky |
| `.site-header__inner` | Inner Container, justify: space-between, align: center |
| `.logo` | Container + Icon/Image + Heading (EventFlow) |
| `.site-nav` | Container (desktop: row) |
| `.site-nav__list` | — или Nav Menu widget |
| `.site-nav__cta` | Global Widget Button Primary |

**Mobile (< 768px):** Off-canvas или dropdown через Elementor Nav Menu + hamburger (без кастомного JS в Elementor — встроенное меню).

**Атрибут `data-editable="header"`** → вся шапка как Template Part.

---

## Секция 2: Hero `data-section="hero"`

| HTML | Elementor |
|------|-----------|
| `.hero` | Container, padding 48/64, background gradient (custom CSS ≤5 строк или Elementor BG) |
| `.hero__grid` | Container, 1 col mobile → 2 col desktop (50/50) |
| `.eyebrow` | Heading (span style) или Text Editor |
| `.hero__title` | Heading H1 |
| `.hero__lead` | Text Editor |
| `.hero__actions` | Container row, gap 16 |
| `.hero__stats` | Container grid 3 columns |
| `strong` + `span` | Inner Container × 3 |
| `.hero__visual` | Container column |
| `.hero-card` | Global Widget Card Surface × 2 |

**Редактируемость:** все `data-editable` на hero → Dynamic Tags OFF, plain text widgets.

---

## Секция 3: Benefits `data-section="benefits"`

| HTML | Elementor |
|------|-----------|
| `.section--alt` | Container BG `#12171f` |
| `.section-header` | Global Widget Section Header |
| `.card-grid` | Container Grid: 1 → 2 → 2 cols |
| `.feature-card` | Global Widget Card Surface |
| `.feature-card__icon` | Text "01" styled |
| `.feature-card__title` | Heading H3 |
| `.feature-card__text` | Text Editor |

**Поток 300 стр/мес:** сохранить секцию как **Template → Section "Benefits 4-col"** → Insert на новые страницы.

---

## Секция 4: How it works `data-section="how-it-works"`

| HTML | Elementor |
|------|-----------|
| `.steps` | Container Grid 3 columns (tablet+) |
| `.step` | Container, position relative |
| `.step__num` | Icon Box или Heading в circle |
| `.step__title` | H3 |
| `.step__text` | Text Editor |

---

## Секция 5: Pricing `data-section="pricing"`

| HTML | Elementor |
|------|-----------|
| `.pricing-grid` | Container Grid 3 equal columns |
| `.pricing-card` | Container column, border |
| `.pricing-card--featured` | Duplicate + border accent + badge |
| `.pricing-card__badge` | Text widget absolute |
| `.pricing-card__features` | Icon List widget |
| `.btn` | Global Widget buttons |

**Редактируемость:** цены и списки — отдельные виджеты (клиент меняет без ломки сетки).

---

## Секция 6: Cases `data-section="cases"`

| HTML | Elementor |
|------|-----------|
| `.case-grid` | Grid 1 → 2 → 3 |
| `.case-card` | Card Surface |
| `.case-card__metrics` | Inner Container 2 cols, counter/heading для цифр |

**Кейс Roadshow** — акцент на «35 мин/страница» для демонстрации потоковой модели работодателю.

---

## Секция 7: FAQ `data-section="faq"`

| HTML | Elementor |
|------|-----------|
| `.faq-item` | **Accordion widget** (Elementor Pro) — предпочтительно |
| Альтернатива | Toggle widget × 4 |

Не использовать тяжёлые FAQ-плагины. Native Accordion = 0 лишнего JS.

---

## Секция 8: CTA `data-section="cta"`

| HTML | Elementor |
|------|-----------|
| `.cta-box` | Container, centered text |
| `.cta-form` | Form widget (Name, Company, Email) + Button |
| Submit | Redirect or webhook (не demo alert) |

---

## Секция 9: Footer `data-section="footer"`

| HTML | Elementor |
|------|-----------|
| `.site-footer__grid` | Container 1 → 2 cols |
| `.site-footer__nav` | Grid 2 → 3 cols, Link lists |
| `.site-footer__bottom` | Text copyright |

**Theme Builder:** Footer template для всего сайта.

---

## Naming convention (поток)

| Тип | Имя |
|-----|-----|
| Page template | `TPL / Landing B2B Events` |
| Section | `SEC / Hero`, `SEC / Benefits`, … |
| Global widget | `GW / …` |
| Клон страницы | `LP / [Client] / [City]` |

**Клонирование под новый город (roadshow):** Duplicate page → заменить тексты в `data-editable` зонах → 30–40 мин при готовых GW.

---

## Минимальный custom CSS в Elementor

Разрешено только если нельзя иначе:

```css
/* Elementor > Custom CSS на контейнере Hero */
selector {
  background: radial-gradient(ellipse 80% 60% at 50% -20%, rgba(61,124,255,0.12), transparent);
}
```

Всё остальное — через контейнеры, фоны, типографику Global Styles.

---

## Чеклист переноса (1 страница)

- [ ] Site Settings + Global Colors/Typography
- [ ] 5 Global Widgets созданы
- [ ] Header/Footer в Theme Builder
- [ ] 8 секций собраны контейнерами (не Section legacy)
- [ ] Mobile 375 / Tablet 768 / Desktop 1200 проверены
- [ ] Accordion FAQ работает без сторонних плагинов
- [ ] Form отправляется
- [ ] Нет Slider Revolution / тяжёлых слайдеров
- [ ] Page saved as Template для потока
