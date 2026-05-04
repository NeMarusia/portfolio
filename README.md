# Портфолио Марси

Статический сайт-портфолио на [Astro](https://astro.build/). Первая версия — русская, с карточками проектов, навыками и контактами.

## Как запустить локально

```bash
cd /home/sunrise/portfolio
npm install
npm run dev
```

После запуска Astro покажет адрес, обычно:

```text
http://localhost:4321
```

## Как собрать для сервера

```bash
cd /home/sunrise/portfolio
npm run build
```

Готовые статические файлы появятся в:

```text
/home/sunrise/portfolio/dist
```

Их можно отдавать через Caddy/nginx как обычный статический сайт.

## Минимальный Caddyfile

```caddy
example.com {
    root * /var/www/portfolio
    file_server
}
```

Затем скопировать сборку:

```bash
sudo mkdir -p /var/www/portfolio
sudo rsync -a --delete /home/sunrise/portfolio/dist/ /var/www/portfolio/
```

## Что доделать

- добавить скриншоты/гифки проектов;
- уточнить текст «Обо мне»;
- добавить PDF-резюме;
- добавить английскую версию;
- подключить домен и HTTPS.
