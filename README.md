# sr500maps

Publiseringsrepo for interaktive HTML-kart fra SR500 motorsykkel/GPS-prosjektet.

## Formål
Dette repoet er presentasjonslaget for turkart.
Det inneholder ferdigrendrede HTML-filer som kan publiseres via Cloudflare Pages.

Dataene kommer fra `sr500exports`, men dette repoet skal bare inneholde publiserbare kartfiler og enkel statisk struktur.

## Forventet innhold
```text
.
├── index.html
├── latest.html
└── trips/
    └── trip-<trip_id>.html
```

## Flyt
1. GPS-data logges på Pi-en
2. turer eksporteres til `sr500exports`
3. kart rendres fra eksporterte trip-filer
4. publiserbare HTML-filer legges i dette repoet
5. Cloudflare Pages serverer repoet som statisk nettsted

## Målbilde
På sikt skal agenten kunne sende:
- bilde av tur
- lenke til publisert interaktivt kart
- eventuelt GPX som separat eksportformat

## Nåværende status
- repo opprettet
- planlagt brukt som Cloudflare Pages-kilde
- første struktur og publiseringsflyt gjenstår
