# Rebuild spec for *.unqspace.tech

## Broken — DELETE ALL uses of
- `st.kp.yandex.net/images/film_big/`
- `st.kp.yandex.net/images/film_iphone/`
- `kinopoisk.ru/images/sm_film/`
These returned wrong posters (Top Gear etc).

## Images (use these)
Primary posters from MAL CDN (verified). For each host use poster + 2–4 extras from the same host line in `mal-posters.tsv` BUT only URLs that share the same anime folder when possible; prefer the first (og) poster and add `l.jpg` variant if exists (`99889.jpg` → also try `99889l.jpg`).

Also pull character images from Fandom:
`https://{wiki}.fandom.com/api.php?action=query&titles=...&prop=pageimages|extracts&exintro=1&explaintext=1&pithumbsize=500&format=json`
RU demon wiki: kimetsu-no-yaiba.fandom.com/ru
EN fallbacks: attackontitan, jujutsu-kaisen, one-piece, naruto, bleach, etc.

Download key posters into each site `static/img/` (poster1.jpg, poster2.jpg, char-*.jpg) by fetching MAL/fandom URLs so pages are not empty if CDN blocks hotlink. Attribute sources in footer: MyAnimeList / Fandom wiki (CC-BY-SA text where used).

## Trailers — embed 2–3 players, no redirect
VK iframe:
`<iframe src="https://vk.com/video_ext.php?oid=-73629052&id=456249581" width="100%" height="360" allow="autoplay; encrypted-media; fullscreen; picture-in-picture; screen-wake-lock;" frameborder="0" allowfullscreen></iframe>`
Parse `vk.com/video-{group}_{id}` → oid=-{group}&id={id}.
Also show text links under each player to the VK page and Kinopoisk card.
Per site: 2–3 unique trailers (from rf-media.json + kinopoisk /video/ + second VK if available).

## Text volume
Each homepage: 400–800 words Russian total across sections.
Character pages: 120–250 words bio each, 3–5 characters.
Source mix: paraphrased + quoted short passages with links to Fandom, Kinopoisk, official site. Link the example style wiki pages.
Do NOT leave thin stub paragraphs.

## Required pages per site
- index.html — hero with poster collage (3+ images), long about, gallery strip, 2–3 embedded trailers, resource links, network grid
- personazhi/index.html — list of characters with photo + short bio
- personazhi/{slug}.html — full bio + image + wiki link (at least 3 chars)
- o-mire/, resursy/, set/, o-sayte/, kontakty.html, politika.html
- static/site.css overhaul: media-rich layout, gallery grid, trailer embeds responsive
- health/status, favicon, robots, feed, webmanifest

## Attribution footer
«Тексты и факты: открытые источники (Fandom wiki CC-BY-SA, Кинопоиск, официальные сайты). Постеры: промо MyAnimeList CDN. Трейлеры: VK Video / Кинопоиск.»
