# CLAUDE.md for geo

Geografigåteri: korte kartspel der spelaren les ei gåte og klikkar på rett stad i eit Leaflet-kart. Statisk nettstad på GitHub Pages med éi mappe per veke. Sjå README.md for struktur og korleis ein legg til ei ny veke.

## Køyring
- Ingen byggjesteg og ingen avhengigheiter å installere. Opne `index.html` direkte eller via ein lokal webtenar, t.d. `python3 -m http.server`.
- Push til `main` publiserer heile repoet (`path: '.'`) til GitHub Pages via `.github/workflows/static.yml`. Live: https://ghveem.github.io/geo/

## Struktur
- `index.html`: meny med eitt `<a class="card">` per veke inne i `.cards`.
- `ukeNN/index.html`: eitt sjølvstendig spel med inline CSS og JS. Gåtene ligg i `const gater = [...]` med `riddle`, `lat`, `lng`, `navn` og (frå `uke18`) `radius` i meter.
- Leaflet 1.9.4 frå unpkg og kartfliser frå CARTO (`basemaps.cartocdn.com`).
- Fargar i `:root` på kvar side: `--primary: #2A1C5E` og `--accent: #63F293`.

## Fallgruver
- Ny veke krev både ny mappe og nytt kort i rot-`index.html`. Kopier eit eksisterande kort med `card-arrow` (kortet for veke 19 manglar det).
- Kvar side har sin eigen kopi av CSS og JS. Endringar i felles stil eller logikk må gjerast i alle filene.
- `uke17` lastar `leaflet-control-geocoder` frå unpkg utan låst versjon, og gåtene der har ikkje `radius`.
- Speltekstane er på bokmål. Ikkje omset dei utan at det er bede om.
- Alt i repoet blir publisert offentleg. Ikkje legg inn filer eller persondata som ikkje skal vere ope tilgjengelege.

## Reglar
- Bruk git med små, tydelege commits, og aldri push direkte til `main`. Bruk eiga grein og PR.
- Trygg .gitignore, ingen hemmelegheiter eller tokens i repoet.
- Oppdater README.md når noko endrar seg.
- Bruk /ndla-brand for UI.
- Skriv nynorsk, utan tankestrek, bruk «me» og «K.I.».
- Gjer berre det som er bede om, kvar endra linje skal følgje av oppgåva.
