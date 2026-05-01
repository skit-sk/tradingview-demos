# Changelog — TradingView Demos

## v3.0.0 (2026-05-01 16:45 MSK) — Breaking changes

### Breaking: изменены embed-widget типы TradingView

Ряд виджетов использовали устаревшие/несуществующие типы `embed-widget`, что приводило к HTTP 404 от `tradingview-widget.com`. Исправлено на актуальные:

| Файл | Старый тип (404) | Новый тип (200) |
|------|-----------------|-----------------|
| `crypto-heatmap` | `crypto-heatmap` | `crypto-coins-heatmap` |
| `crypto-market` | `crypto-screener` | `screener` |
| `economic-calendar`, `calendars` | `economic-calendar` | `events` |
| `forex-heatmap` | `forex-heatmap` | `forex-heat-map` |
| `single-ticker` | `single-ticker` | `single-quote` |
| `stock-market` | `stock-market` | `hotlists` |

### Breaking: конвертация 3 виджетов в web components

TradingView убрал iframe-версии для `mini-chart`, `economic-map`. Переведены на `<tv-*>` web components:

| Файл | Web component script |
|------|----------------------|
| `mini-chart` | `tv-mini-chart.js` |
| `economic-map` | `tv-economic-map.js` |
| `economics` | `tv-economic-map.js` |

### Прочее

- URL-кодировка: `%22` вместо `\"` во всех 31 widgets-full и 24 preview файлах
- 24 SVG-заглушки в preview заменены на реальные TradingView iframes
- Все 32 виджета загружаются корректно (подтверждено скриншотами)

---

## v2.5.7 (2026-05-01 15:30 MSK)

- 3 недостающих widgets-full добавлены: `company-profile`, `fundamental-data`, `symbol-info`
- 9 сломанных виджетов заменены на прямые iframe (без JS-обёртки)
- 14 новых preview-страниц
- Исправлены ссылки «Open Full» во всех виджетов
- Добавлен MSK timestamp в футер

---

## v2.5.6 (2026-05-01 05:24 MSK)

- Все виджеты переведены на прямые iframe (без JS-обёртки widget-loader)

---

## v2.5.5 (2026-05-01 05:02 MSK)

- Ticker / Ticker Tag исправлены
- Виджеты работают

---

## v2.5.4 (2026-05-01 04:46 MSK)

- Очищен widget loader

---

## v2.5.3 (2026-05-01 04:44 MSK)

- Обновлена версия виджетов

---

## v2.5.2 и ранее

- Начальная структура: gallery + widgets-full + widgets превью
- Динамическая загрузка iframes через JS