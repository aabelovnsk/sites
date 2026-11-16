# Cover sites

Статические витрины (HTML/CSS) для выкладки в `root` nginx. Без VPN/proxy-лексики.

## Новые сайты (не NPVX-архив)

| DOMAIN | Бренд | Ниша | Город | Палитра |
|--------|-------|------|-------|---------|
| `bilety-kat-b.ru` | Билеты кат. B | билеты ПДД категория B | Новосибирск | `#2d6a3e` / `#f3f5f2` |
| `sonnik-noch.ru` | Сонник Ночь | толкование снов | Казань | `#5c4a7a` / `#f4f0f7` |
| `taro-azbuka.ru` | Азбука Таро | справочник карт таро | Санкт-Петербург | `#6b2f3a` / `#f7f3ea` |

## Ранее (нишевые архивы)

| DOMAIN | Бренд | Ниша | Референс жанра |
|--------|-------|------|----------------|
| `rechnoy-stvor.ru` | Речной створ | речные знаки | bakeny.ru |
| `orbita-kadry.ru` | Орбита-кадры | атлас с орбиты | nadir-atlas.ru |
| `padun-sever.ru` | Падун | северные пороги | porogi-sever.ru |
| `malaya-koleya.ru` | Малая колея | УЖД / дрезины | dreziny.ru |
| `skaly-zapisi.ru` | Скалы-записи | каньоны / парки | kanyon-video.ru |
| `rechnoy-lyod.ru` | Речной лёд | ледоход | ledohod-zapis.ru |
| `bereg-chas.ru` | Берег-час | отлив–прилив | otliv-priliv.ru |
| `medunitsa-klub.ru` | Медуница | клуб пчеловодов | roevoy.online |

## Деплой

```bash
scp -r DOMAIN user@host:/var/www/
```

```nginx
server {
    listen 443 ssl http2;
    server_name DOMAIN;
    root /var/www/DOMAIN;
    index index.html;
    location / { try_files $uri $uri/ $uri/index.html =404; }
    location = /health {
        default_type application/json;
        alias /var/www/DOMAIN/health/index.json;
    }
    location = /status {
        default_type application/json;
        alias /var/www/DOMAIN/status/index.json;
    }
}
```

Перед продом замените ООО, город и email.
