# Insta-card — Profilo personale / biglietto da visita digitale

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![FontAwesome](https://img.shields.io/badge/FontAwesome-528DD7?style=for-the-badge&logo=fontawesome&logoColor=white)](https://fontawesome.com/)

Un biglietto da visita digitale, moderno e interattivo. Una singola pagina che raggruppa foto, nome, descrizione, link social (GitHub, LinkedIn, Instagram) e i curriculum in PDF (IT/EN) in un formato esteticamente curato, ottimizzato per smartphone e desktop.

## Caratteristiche

- **Design moderno**: gradiente elegante, icone social FontAwesome e layout card.
- **Download CV bilingue**: link diretti ai curriculum in PDF (italiano e inglese) con download immediato.
- **Link social**: accesso rapido a GitHub, LinkedIn e Instagram.
- **Fully responsive**: layout adattato a viewport mobile e desktop.
- **Zero dipendenze build**: unico file HTML, pronto all'uso.

## Tech Stack

- **HTML5** — Struttura semantica della card digitale
- **CSS3** — Layout Flexbox, gradienti personalizzati e responsive design
- **JavaScript** — Logica interattiva e rotazione dinamica dei ruoli
- **FontAwesome** — Iconografia vettoriale per social e documenti
- **PDF (IT / EN)** — Curriculum scaricabili integrati

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

## Project Structure

```
Insta-card/
├── index.html             # Unica pagina (markup, stile e JS inline)
├── IMG_20250725_214730.jpg # Immagine del profilo
├── Curriculum_Ita.pdf     # Curriculum in italiano (download)
├── Curriculum_Eng.pdf     # Curriculum in inglese (download)
├── .vscode/               # Configurazione editor
└── README.md
```

## Screenshots / Demo

Demo live disponibile su: [st0rmosu.github.io/Insta-card](https://st0rmosu.github.io/Insta-card/)

![Insta-card](IMG_20250725_214730.jpg)

---

*Creato da Lorenzo Recchia.*

