# SEO LOG — giuseppebonellitattoo.art
Registro delle migliorie SEO. Una riga per giorno: data — categoria — cosa — pagine — esito IndexNow.
REGOLA: leggere tutto il log prima di scegliere la miglioria del giorno; mai ripetere una voce già fatta.

## Già fatto in fase di build (2026-06-25 → 2026-07-07) — NON rifare:
- 2026-07-07 — struttura — 40 pagine live: home + 4 stili + 6 tour (Event schema) + 28 città circuito Villain Arts (funnel "join the list", NO Event) + hub /us-tattoo-convention-circuit/ — tutte — IndexNow 202 (40 URL)
- 2026-07-07 — tecnica — sitemap con lastmod + urls.txt + chiave IndexNow attivata ({KEY}.txt sul sito)
- 2026-07-07 — foto — tigre brutta rimossa, manica-statua in 3 viste, minion raddrizzato, p09 aggiunta a Color
- 2026-06-25 — schema — @graph: TattooParlor + Person (alternateName, sameAs: IG @giuseppe_gibi_bonelli, studio, FB, TikTok, Tattoodo) + 4 Service + FAQPage (13 Q&A home) + WebSite + ImageObject (champ01)
- 2026-06-25 — contenuti — FAQ (13), Aftercare, How it works + policy, bio-entità (16 anni, Lautaro/Donnarumma/Romagnoli, NO studio Milano nel copy), sezione Champions/VIP con roster calciatori
- 2026-06-25 — AEO — llms.txt con fatti verificati + URL reali; robots.txt permissivo (GPTBot/ClaudeBot/PerplexityBot/Google-Extended/Bingbot); capsule-entità citabile in About; direct-answer block su ogni pagina città; 3 FAQ buyer-query
- 2026-06-25 — meta — en-US, geo.region US, canonical, keywords, OG; titles unici per pagina
- 2026-06-25 — internal linking — footer home → hub + 4 pagine stile

## Log giornaliero:
- 2026-07-12 — contenuti — copy locale unico (venue+quartiere, verificato via ricerca web) su 2 pagine città circuito: Wildwood NJ (Wildwoods Convention Center, boardwalk/Doo Wop motels, Love Rock Tattoo) e Colorado Springs CO (Norris Penrose Event Center, Cheyenne Mountain/Broadmoor) — sostituito il blocco generico "Worn by champions" con "The venue & ..." SOLO su queste 2, invariato sulle altre 26 — IndexNow 200 (2 URL)
- [NON loggato a suo tempo] 2026-07-15 — tecnica — commit "SEO: shorter meta, absolute og:image, og:url, H1 keyword" solo su homepage (meta description più corta, og:image/og:url assoluti, H1 con keyword) — retro-registrato oggi trovandolo in git log
- 2026-07-18 — contenuti — copy locale unico (venue+quartiere, verificato via ricerca web) su altre 2 pagine città circuito: Savannah GA (Savannah Convention Center su Hutchinson Island, scena tattoo historic district: Anonymous/Alien Arts su Bay St, Riverside Tattoo Starland District) e Asheville NC (Harrah's Cherokee Center su Haywood St, stessa via di Traveler Tattoo/Girl and Goblin/Heron Mark, vicino River Arts District e West Asheville) — blocco "The venue & scene" SOLO su queste 2, invariato sulle altre 24 — validazioni JSON-LD/immagini/node --check OK — deploy OK — IndexNow 200 (2 URL) — ⚠️ vedi nota cache sotto

## ⚠️ PROBLEMA APERTO (dal 2026-07-18): cache Cloudflare stale su tutte le pagine città circuito
Verificato oggi: tutte le pagine `/realism-tattoo-artist-*/` + l'hub `/us-tattoo-convention-circuit/` rispondono `Last-Modified: Mon, 13 Jul 2026` quando richieste dal dominio pubblico (via Cloudflare), NONOSTANTE il file sull'origin (droplet, verificato via IP diretto+Host header) sia corretto e aggiornato (Last-Modified oggi). Cloudflare mostra `cf-cache-status: DYNAMIC` (= non dovrebbe cachare) eppure serve contenuto vecchio in modo persistente anche con query cache-busting. La homepage invece risulta aggiornata. Sospetto: Page Rule/Cache Rule "Cache Everything" o tiered cache su Cloudflare con TTL lungo sulle pagine città, mai purgata dal deploy del 13/7. Serve: Marco controlla dashboard Cloudflare (zone giuseppebonellitattoo.art) e fa un purge cache mirato o globale — non ho credenziali/API token Cloudflare in questa sessione per farlo. Finché non risolto, le migliorie SEO sulle pagine città (incluse quelle di oggi) potrebbero non essere visibili a visitatori/crawler reali.

## Vietato sempre: eventi/date inventate, recensioni finte, claim "best" auto-proclamati, riferimenti a Penny/MCL.
## Idee in coda (da fare nei prossimi giorni, una al giorno):
- Copy locale unico per le altre 24 pagine città circuito (batch da 2-3 città/giorno, con dettagli veri da ricerca web: venue, quartieri, scena tattoo) — fatte finora: Wildwood, Colorado Springs, Savannah, Asheville
- Pulizia: rimuovere i file .bak lasciati nel commit del 15/7 (dist/index.html.bak, site/index.html.bak, gen_landing.py.bak) — dist/index.html.bak è pubblicamente accessibile sul sito, da valutare
- FAQ specifiche per pagina stile (1/giorno)
- Blocco "Convention day: how it works" su pagine tour
- Blocco "Fresh vs healed realism" (quando Beppe manda foto healed)
- Meta description più cliccabili (CTR) su pagine stile
- Breadcrumb visibili sulle landing
- Alt-text pass completo con pattern stile+soggetto+artista
---
