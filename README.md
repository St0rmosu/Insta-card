# Insta-card: profilo personale e biglietto da visita digitale

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![FontAwesome](https://img.shields.io/badge/FontAwesome-528DD7?style=for-the-badge&logo=fontawesome&logoColor=white)](https://fontawesome.com/)

Un biglietto da visita digitale in una singola pagina: foto, nome, descrizione, link social (GitHub, LinkedIn, Instagram) e curriculum in PDF (IT/EN), ottimizzato per smartphone e desktop.

## Caratteristiche

- **Design moderno**: gradiente, icone social FontAwesome e layout card.
- **Download CV bilingue**: link diretti ai curriculum in PDF (italiano e inglese) con download immediato.
- **Link social**: accesso rapido a GitHub, LinkedIn e Instagram.
- **Fully responsive**: layout adattato a viewport mobile e desktop.
- **Zero dipendenze di build**: unico file HTML, pronto all'uso.

## Tech stack

- **HTML5** — struttura semantica della card digitale
- **CSS3** — layout Flexbox, gradienti personalizzati e responsive design
- **JavaScript** — logica interattiva e rotazione dinamica dei ruoli
- **FontAwesome** — iconografia vettoriale per social e documenti
- **PDF (IT / EN)** — curriculum scaricabili integrati

## Architettura

Pagina statica single-file: la card è composta da foto, testo (nome + descrizione animata via JS), menu dei social e un menu a tendina per i curriculum:

```
                    ┌──────────────────────────────────┐
                    │            index.html            │
                    ├──────────────────────────────────┤
                    │   Immagine profilo (IMG_*.jpg)   │
                    │   Nome · Descrizione (JS rotator)│
                    │   ┌────────────────────────────┐ │
                    │   │  Social: GitHub · LinkedIn │ │
                    │   │          · Instagram       │ │
                    │   │  CV:    IT ▾ · EN ▾        │ │
                    │   └────────────────────────────┘ │
                    └──────────────────────────────────┘
```

## Struttura del progetto

```
Insta-card/
├── index.html             # Unica pagina (markup, stile e JS inline)
├── IMG_20250725_214730.jpg # Immagine del profilo
├── Curriculum_Ita.pdf     # Curriculum in italiano (download)
├── Curriculum_Eng.pdf     # Curriculum in inglese (download)
├── .vscode/               # Configurazione editor
└── README.md
```

*Creato da Lorenzo Recchia.*
