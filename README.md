# geo

Statisk nettsted med ukentlig innhold. Strukturen er enkel: én `index.html` per mappe. Rotmappen inneholder en meny som lenker til alle ukemappene.

## Struktur

```
geo/
├── index.html          # Meny – oversikt over alle uker
├── uke17/
│   └── index.html      # Innhold for uke 17
├── uke18/
│   └── index.html      # Innhold for uke 18
└── README.md
```

## Prinsipp

- Én `index.html` per undermappe
- Mappenavnet er innholdets navn (f.eks. `uke17`)
- Rot-`index.html` fungerer som meny og følger samme visuell stil som de øvrige sidene
- Ny uke = ny mappe med en `index.html`

## Publisering

Siden publiseres via GitHub Pages. Workflow-konfigurasjon ligger i `.github/workflows/`.

Live: [https://ghveem.github.io/geo/](https://ghveem.github.io/geo/)

## Lenker

| Uke | URL |
|-----|-----|
| 17 | https://ghveem.github.io/geo/uke17/ |
| 18 | https://ghveem.github.io/geo/uke18/ |

## Legge til en ny uke

1. Opprett mappe, f.eks. `uke19/`
2. Legg til `uke19/index.html`
3. Legg til en ny kortlenke i rot-`index.html` under `.cards`

```html
<a class="card" href="uke19/">
  <span class="card-label">Uke</span>
  <span class="card-title">19</span>
  <span class="card-desc">Innhold for uke 19</span>
</a>
```
