# Cover sites

Static cover websites for nginx root deploy.

## unqspace.tech — anime set (24)

Поддомены `*.unqspace.tech`. На каждом сайте раздел `/set/` со ссылками на все 24.

Обновлённый фан-портал: постеры с CDN Кинопоиска/Яндекса (`st.kp.yandex.net`), трейлеры VK Video / Кинопоиск (доступны в РФ), официальные сайты, манга, ru.Wikipedia.  
Визуал hero — hotlink официальных промо-постеров Kinopoisk/Yandex CDN + оригинальный CSS/SVG. Локальные кадры аниме в репозиторий не кладём; YouTube не используется.  
Каталог данных: `_data/anime-catalog.json`, медиа РФ: `_data/rf-media.json`.

| Subdomain | Аниме |
|-----------|-------|
| ghost.unqspace.tech | Призрак в доспехах |
| demon.unqspace.tech | Истребитель демонов |
| piece.unqspace.tech | One Piece |
| punch.unqspace.tech | One Punch Man |
| titan.unqspace.tech | Атака титанов |
| bleach.unqspace.tech | Блич |
| atelier.unqspace.tech | Ателье колдовских колпаков |
| naruto.unqspace.tech | Наруто |
| note.unqspace.tech | Тетрадь смерти |
| alchemist.unqspace.tech | Стальной алхимик |
| eva.unqspace.tech | Евангелион |
| bebop.unqspace.tech | Ковбой Бибоп |
| spirited.unqspace.tech | Унесённые призраками |
| jujutsu.unqspace.tech | Магическая битва |
| hero.unqspace.tech | Моя геройская академия |
| ghoul.unqspace.tech | Токийский гуль |
| mob.unqspace.tech | Моб Психо 100 |
| hunter.unqspace.tech | Hunter × Hunter |
| dragon.unqspace.tech | Драконий жемчуг |
| chainsaw.unqspace.tech | Человек-бензопила |
| spy.unqspace.tech | Семья шпиона |
| steins.unqspace.tech | Врата Штейна |
| geass.unqspace.tech | Код Гиас |
| frieren.unqspace.tech | Фрирен |

Пример nginx:

```nginx
server_name titan.unqspace.tech;
root /var/www/titan.unqspace.tech;
```

## astroesoteric.online — esoteric set (8)

| Subdomain | Brand | Niche |
|-----------|-------|-------|
| numbers.astroesoteric.online | Число Смысла | нумерология |
| tarot.astroesoteric.online | Колода Знаков | таро |
| astrology.astroesoteric.online | Небо Дня | астрология |
| palm.astroesoteric.online | Линии Ладони | хиромантия |
| natal.astroesoteric.online | Карта Рода | натальная карта |
| matrix.astroesoteric.online | Матрица Пути | матрица судьбы |
| runes.astroesoteric.online | Руны Севера | руны |
| moon.astroesoteric.online | Лунный Круг | лунный календарь |

Каждый сайт также содержит `static/site.css`, `favicon.svg`, `robots.txt`, `feed.xml`, `site.webmanifest`, `health/index.json`, `status/index.json`.

На главной esoteric-сайтов есть блок **Смежные справочники** со ссылками на остальные семь `*.astroesoteric.online`.
