# LexIT Executive Governance Website

Premium-Unternehmensberatung für IT-Compliance und IT-Governance.

## Tech Stack

- **Framework:** Astro (Static Site Generation)
- **Styling:** Tailwind CSS v4
- **Typography:** IBM Plex Sans (Google Fonts)
- **JavaScript:** Keines im Frontend (reine SSG)

## Setup

```bash
# Dependencies installieren
npm install

# Development Server starten
npm run dev

# Production Build erstellen
npm run build

# Production Build lokal testen
npm run preview
```

Der Development Server läuft auf `http://localhost:4321`.

## Projektstruktur

```
/
├── public/
│   ├── Lexit_Textlogo.png    # Vollständiges Text-Logo
│   └── Lexit_x.png           # X-Icon für Favicon & Intervention
├── src/
│   ├── components/
│   │   ├── Header.astro      # Navigation
│   │   └── Footer.astro      # Kontakt & Legal
│   ├── layouts/
│   │   └── BaseLayout.astro  # SEO Meta Tags, Font Loading
│   ├── pages/
│   │   └── index.astro       # Homepage
│   └── styles/
│       ├── global.css        # Design System (Tailwind Theme)
│       └── print.css         # Print Stylesheet
├── astro.config.mjs
└── package.json
```

## Design System

### Farben

| Name              | Hex       | Verwendung                    |
|-------------------|-----------|-------------------------------|
| Trust Blue        | `#1F3A5F` | Headlines, Links              |
| Ink               | `#111827` | Body Text                     |
| Slate             | `#4B5563` | Meta Text, Subtitles          |
| Line Grey         | `#E5E7EB` | Borders, Separators           |
| Controlled Amber  | `#E07A2F` | Hover States, Akzent          |
| Off-White         | `#F9FAFB` | Section Backgrounds           |

### Typography

- **H1:** 48px / 36px mobile, -0.02em tracking, weight 600
- **H2:** 32px / 28px mobile, -0.01em tracking, weight 600
- **H3:** 20px, weight 600
- **Body:** 18px / 16px mobile, line-height 1.6
- **Meta:** 14px, 0.01em tracking

### Spacing

- Section gaps: 120px / 80px mobile
- Large pause: 160px / 100px mobile
- Medium pause: 100px / 60px mobile
- Internal: 60px, 40px, 20px

## Deployment

Das Projekt generiert statische HTML-Dateien. Nach `npm run build` liegt das
fertige Projekt im `/dist` Verzeichnis und kann auf jeden Static Host deployed werden:

- Netlify
- Vercel
- Cloudflare Pages
- Traditionelles Webhosting

## Logo-Assets

Die Logos müssen manuell im `/public` Verzeichnis platziert werden:

1. `Lexit_Textlogo.png` - Vollständiges Logo mit Text
2. `Lexit_x.png` - X-Icon (140px Breite empfohlen)

## Drucken

Die Website ist für den Druck optimiert. Das Print Stylesheet:
- Entfernt das X-Intervention Element
- Konvertiert zu Schwarz/Weiß
- Zeigt Link-URLs inline
- Optimiert Seitenumbrüche

## Änderungen vornehmen

### Texte ändern
Alle Texte befinden sich direkt in `src/pages/index.astro`.

### Farben ändern
Design System Farben in `src/styles/global.css` unter `@theme`.

### Neue Seiten hinzufügen
Neue `.astro` Datei in `src/pages/` erstellen. Beispiel: `impressum.astro`.
