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

| Tecnologia | Ruolo |
|---|---|
| HTML5 | Struttura semantica della card |
| CSS3 | Layout Flexbox, gradienti custom e responsive design |
| JavaScript | Effetti dinamici e rotazione testi (descrizione) |
| FontAwesome | Iconografia social e file |
| PDF (ITA/ENG) | Curriculum scaricabili |

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

## Installation & Setup

Nessuna dipendenza da installare. Basta servire la cartella:

```bash
git clone https://github.com/St0rmosu/Insta-card.git
cd Insta-card
# apri index.html direttamente, oppure avvia un server statico
python3 -m http.server 8080
```

## Usage

1. Apri `index.html` nel browser.
2. Leggi il profilo: foto, nome e descrizione ruotata automaticamente.
3. Clicca le icone social per aprire i relativi profili.
4. Usa il menu CV per scaricare il curriculum in italiano o in inglese (PDF).

## Screenshots / Demo

![Insta-card](IMG_20250725_214730.jpg)

> Inserire qui uno screenshot della card renderizzata (es. `screenshot.png`). La demo live è pubblicata su GitHub Pages.

## API Documentation

Nessuna API esterna: la pagina è completamente statica e non effettua richieste di rete. L'unico "endpoint" sono i download dei PDF locali (`Curriculum_Ita.pdf`, `Curriculum_Eng.pdf`).

## Engineering Decisions

- **Single-file static**: nessun framework, nessun build step, hosting ovunque (anche file://). Compromesso: personalizzazione solo modificando l'HTML.
- **FontAwesome via CDN**: icone professionali senza bundling; richiede connettività, con fallback testuale via `aria-label`.
- **Descrizione animata in JS puro**: effetto a rotazione dei ruoli senza librerie esterne.

## Testing

- Test manuale su browser (Chromium, Firefox) e su viewport mobile/desktop tramite DevTools.
- Verifica dei download dei PDF (IT/EN) e dei link social.
- Nessuna suite di test automatici (progetto statico).

## Limitations & Future Improvements

- Dipende dal CDN FontAwesome: offline mancano le icone.
- Contenuti (foto, CV, link) da aggiornare manualmente nel file.
- Non c'è sistema di analisi degli accessi.
- Prossimi passi: versione multi-lingua automatica, microinterazioni, tema scuro/chiaro e sostituzione delle icone CDN con SVG inline.

---

*Creato da Lorenzo Recchia.*
