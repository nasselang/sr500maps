# sr500maps

Publiseringsrepo for interaktive HTML-kart fra SR500 motorsykkel/GPS-prosjektet.

## Formål
Dette repoet er presentasjonslaget for turkart.
Det inneholder ferdigrendrede HTML-filer som publiseres via GitHub Pages.

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
2. turer rebuildes og støy-turer filtreres bort
3. gyldige turer eksporteres til `sr500exports`
4. stale eksport- og kartfiler ryddes bort
5. kart rendres fra gyldige eksporterte trip-filer på Pi-en
6. publiserbare HTML-filer legges i dette repoet
7. GitHub Pages serverer repoet som statisk nettsted

## Målbilde
På sikt skal agenten kunne sende:
- bilde av tur
- lenke til publisert interaktivt kart
- eventuelt GPX som separat eksportformat

## Nåværende status
- repoet fylles automatisk fra Pi-en
- GitHub Pages er aktivert
- publisert base URL: `https://nasselang.github.io/sr500maps/`
- `index.html` viser bare turer som fortsatt finnes som gyldige eksporterte turer
- `latest.html` peker til siste publiserte turkart
- gamle HTML-sider fjernes når tilhørende tur ikke lenger finnes i eksportgrunnlaget
