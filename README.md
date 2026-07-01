# APX Bootstrap Theme

Ein individuelles Bootstrap-5-Theme im APX-Look: dark-first mit warmem
Gold-Akzent `#bea05d` und Helvetica-Neue-Typografie. Farben und Design-Tokens
stammen aus dem ApxWebsite Design-System.

🔗 **[Live Demo](https://apx-group.github.io/ApxBootstrap/)**

## Features

- ✅ **APX-Farben**: Primary/Gold `#bea05d`, near-black Surfaces `#0e0d0a` / `#15130e`
- ✅ **Helvetica Neue** Typografie mit versalen, eng getrackten Display-Headlines
- ✅ **Dark-first** mit vollständigem Light-Mode (`data-bs-theme`)
- ✅ **Content-Hashing** für Cache-Busting
- ✅ **Auto-Deploy** via GitHub Actions auf GitHub Pages

## Quick Start

```html
<link href="dist/bootstrap-apx.min.css" rel="stylesheet" />
```

### Theme-Toggle

```html
<button onclick="toggleTheme()">Theme wechseln</button>

<script>
  function toggleTheme() {
    const html = document.documentElement;
    const current = html.getAttribute("data-bs-theme") || "dark";
    html.setAttribute("data-bs-theme", current === "dark" ? "light" : "dark");
  }
</script>
```

## Entwicklung

```bash
# Abhängigkeiten installieren
npm install

# Theme bauen (dist/)
npm run build

# Demo-Server starten
npm run dev

# Watch-Modus (Live Reload)
npm run dev:watch
```

## Projektstruktur

```
├── scss/              # SCSS-Quelle (apx_theme.scss)
├── assets/            # Logo / Favicon
├── demo/              # Demo-Seite
├── dist/              # Gebautes CSS (+ gehashte Dateien)
└── .github/workflows/ # GitHub Pages Deployment
```

## Built With

- **Bootstrap 5.3** — Basis-Framework
- **Sass** — CSS-Präprozessor
- **PostCSS** (autoprefixer + cssnano) — Optimierung
- **GitHub Actions** — CI/CD → GitHub Pages

## Lizenz

MIT
