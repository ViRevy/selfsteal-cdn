# Nexlify — selfsteal landing (CDN-style)

Статичный лендинг под маскировку origin/CDN-туннеля.

Выглядит как продуктовая страница edge-CDN: live-метрики, PoP, тарифы, статус.

**Repo:** https://github.com/ViRevy/selfsteal-cdn

## Установка на сервер

```bash
git clone --depth 1 https://github.com/ViRevy/selfsteal-cdn.git /tmp/selfsteal-cdn
mkdir -p /var/www/html
cp -r /tmp/selfsteal-cdn/index.html /var/www/html/
rm -rf /tmp/selfsteal-cdn
```

## Структура

- `index.html` — весь сайт (CSS + лёгкий JS внутри)
- Зависимость только Google Fonts (Inter)

## Назначение

Selfsteal для схемы **Yandex Cloud CDN + xHTTP / VLESS**: при заходе на домен без auth отдаётся нормальный «CDN-сервис», а не 404.
