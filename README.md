# astroesoteric.online — cover sites

Static cover websites for nginx root deploy under `*.astroesoteric.online`.

Example:

```nginx
server_name numbers.astroesoteric.online;
root /var/www/numbers.astroesoteric.online;
```

| Subdomain | Brand | Niche | City | Palette | Pages |
|-----------|-------|-------|------|---------|-------|
| numbers.astroesoteric.online | Число Смысла | нумерология | Казань | accent `#5b3d7a`, bg `#f5f1f8`, ink `#231a2b` | `/`, `/chisla/`, `/imya/`, `/data-rozhdeniya/`, `/sovmestimost/`, `/o-metode/`, `kontakty.html`, `politika.html` |
| tarot.astroesoteric.online | Колода Знаков | справочник таро | Санкт-Петербург | accent `#6b2f3a`, bg `#f7f3ea`, ink `#2a221c` | `/`, `/starshee/`, `/mladshee/`, `/rasklady/`, `/slovar/`, `/o-kolode/`, `kontakty.html`, `politika.html` |
| astrology.astroesoteric.online | Небо Дня | астрология / знаки зодиака | Москва | accent `#2f4f7a`, bg `#eef2f7`, ink `#1a2230` | `/`, `/znaki/`, `/planety/`, `/doma/`, `/tranzity/`, `/o-nebe/`, `kontakty.html`, `politika.html` |
| palm.astroesoteric.online | Линии Ладони | хиромантия | Краснодар | accent `#8a5a2b`, bg `#f6f0e6`, ink `#2b2218` | `/`, `/linii/`, `/bugry/`, `/forma-ruki/`, `/praktika/`, `/o-metode/`, `kontakty.html`, `politika.html` |
| natal.astroesoteric.online | Карта Рода | натальная карта (справочник) | Екатеринбург | accent `#3d5a4c`, bg `#eef4f0`, ink `#1c2620` | `/`, `/ascendent/`, `/aspekty/`, `/doma/`, `/kak-chitat/`, `/o-karte/`, `kontakty.html`, `politika.html` |
| matrix.astroesoteric.online | Матрица Пути | матрица судьбы | Новосибирск | accent `#7a3d5c`, bg `#f7f0f4`, ink `#271820` | `/`, `/energiya/`, `/arkan/`, `/sovmestimost/`, `/primer/`, `/o-matrix/`, `kontakty.html`, `politika.html` |
| runes.astroesoteric.online | Руны Севера | руны Elder Futhark | Петрозаводск | accent `#3a4d3f`, bg `#eef1ec`, ink `#1c241e` | `/`, `/futhark/`, `/znacheniya/`, `/rasklady/`, `/sovety/`, `/o-runah/`, `kontakty.html`, `politika.html` |
| moon.astroesoteric.online | Лунный Круг | лунный календарь / фазы | Мурманск | accent `#4a5f8a`, bg `#eef1f6`, ink `#1a2030` | `/`, `/fazy/`, `/kalendar/`, `/ritualy/`, `/znak-luny/`, `/o-kruge/`, `kontakty.html`, `politika.html` |

Each site also includes `static/site.css`, `favicon.svg`, `robots.txt`, `feed.xml`, `site.webmanifest`, `health/index.json`, and `status/index.json`.

Each homepage includes a **Смежные справочники** section with cross-links to the other seven `*.astroesoteric.online` cover sites.
