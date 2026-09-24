# zanity-landing

Лендинг Zanity VPN — https://zanityvpn.com

Статическая страница на Cloudflare Workers (static assets). Все файлы сайта лежат в `public/`,
конфиг деплоя — `wrangler.jsonc` (custom domains `zanityvpn.com` и `www.zanityvpn.com`).

## Деплой

```bash
npx wrangler deploy
```

Нужна авторизация в Cloudflare: `npx wrangler login`.

## Настройки вне репозитория (Cloudflare, зона zanityvpn.com)

- Redirect Rule: `https://www.*` → `https://${1}`, 301.
- SSL/TLS → Edge Certificates → Always Use HTTPS: включено.
- DNS: MX и SPF пересылки почты Namecheap.
