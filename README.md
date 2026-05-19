# avto-car-motors.ru

Статическая копия сайта `avto-car-motors.ru` (Next.js prerender), скачанная через `wget --mirror`.

## Что в репозитории

- `index.html`, `about.html`, `contacts.html`, `contract.html`, `guarantees.html`, `jurisdiction.html`, `reviews.html` — страницы сайта.
- `_next/static/...` — JS/CSS/шрифты от Next.js.
- `avto.jpg`, `logo.jpg`, `icon.ico`, `manifest.json` — статические ресурсы.
- `avto1.MP4`..`avto5.MP4` — видео на главной/о компании.
- `otzivi/otziv1.mp4`..`otziv9.mp4` — видео-отзывы.
- `dogovor.pdf` — PDF договора.

## Запуск локально

```bash
python3 -m http.server 8000
# открыть http://127.0.0.1:8000
```

## Исправления навигации

В JS-бандлах Next.js (`_next/static/chunks/app/.../page-*.js` и `layout-*.js`) пути роутинга `/about`, `/contacts`, `/contract`, `/guarantees`, `/jurisdiction`, `/reviews` заменены на `/about.html`, `/contacts.html` и т.д., чтобы клик по кнопкам в шапке работал на любом обычном статическом HTTP-сервере без переписывания URL.
