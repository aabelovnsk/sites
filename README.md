# Cover sites

Статические витрины (HTML/CSS) для выкладки в `root` nginx. Без VPN/proxy-лексики.

## Таблица

| DOMAIN | Бренд | Ниша | Референс NPVX | Тон | Город | Палитра |
|--------|-------|------|---------------|-----|-------|---------|
| `rechnoy-stvor.ru` | Речной створ | речные знаки | bakeny.ru | справочный | Нижний Новгород | `#2f6f8f` / `#e8eef2` |
| `orbita-kadry.ru` | Орбита-кадры | атлас с орбиты | nadir-atlas.ru | архив | Москва | `#e0a04a` / `#0f1419` |
| `padun-sever.ru` | Падун | северные пороги | porogi-sever.ru | архив | Петрозаводск | `#3d6b55` / `#eef2ec` |
| `malaya-koleya.ru` | Малая колея | УЖД / дрезины | dreziny.ru | справочный | Тула | `#9b4a2e` / `#f3ebe1` |
| `skaly-zapisi.ru` | Скалы-записи | каньоны / парки | kanyon-video.ru | архив | Екатеринбург | `#b45a32` / `#f7f1ea` |
| `rechnoy-lyod.ru` | Речной лёд | ледоход | ledohod-zapis.ru | архив | Архангельск | `#3a6d8f` / `#e9eef3` |
| `bereg-chas.ru` | Берег-час | отлив–прилив | otliv-priliv.ru | справочный | Мурманск | `#1f7a7a` / `#e7f0f0` |
| `medunitsa-klub.ru` | Медуница | клуб пчеловодов | roevoy.online | клубный | Подольск | `#b8860b` / `#f6f3e8` |

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

Перед продом замените ООО, город и email в подвале / контактах / политике.

## Запасные имена

`ogni-farvater.ru`, `zenit-lenta.ru`, `shum-poroga.ru`, `shpaly-uzkie.ru`, `krasnye-skaly.ru`, `shuga-dnevnik.ru`, `otmel-maya.ru`, `paseka-yug.ru`, `lom-kamnya.ru`, `tuman-ozera.ru`
