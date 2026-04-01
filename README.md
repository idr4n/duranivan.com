# duranivan.com

Personal website for Ivan Duran — assistant professor of economics, exploring ideas through data and code. Built with [Astro](https://astro.build) and deployed to GitHub Pages.

## Tech Stack

- **Astro 6** — static site generator (zero client-side framework JS)
- **IBM Plex Mono** — self-hosted via [@fontsource](https://fontsource.org/) (400, 500, 700 weights)
- **CSS custom properties** — theme tokens for dark and light modes
- **GitHub Pages** — static hosting with automatic deployment via GitHub Actions

## Project Structure

```
├── public/              # Static assets (favicon, robots.txt, CNAME)
├── src/
│   ├── layouts/
│   │   └── Layout.astro # HTML shell, meta tags, flash-prevention script
│   ├── pages/
│   │   └── index.astro  # Page content, theme toggle UI, scoped styles
│   └── styles/
│       └── global.css   # CSS reset, theme tokens, base styles
├── docs/
│   ├── ARCHITECTURE.md  # Technical architecture documentation
│   └── ROADMAP.md       # Planned features and enhancements
├── astro.config.mjs
├── package.json
└── tsconfig.json
```

## Theme System

The site ships with a three-way theme toggle: **light**, **dark**, and **system**.

- **System (default)** — follows the operating system preference on first visit and tracks changes in real time.
- **Light / Dark** — explicit override, persisted in `localStorage`.
- **Invalid or missing stored value** — treated as `system`, falling back to OS preference.

An inline `<script>` in the `<head>` reads the stored preference and sets the `data-theme` attribute before the first paint, preventing any flash of incorrect theme.

## Development

```sh
npm install
npm run dev
```

## Build & Deploy

```sh
npm run build     # outputs to ./dist/
npm run preview   # preview build locally
```

Pushes to `main` trigger automatic deployment via the GitHub Actions workflow (`.github/workflows/deploy.yml`).

## Requirements

- Node.js >= 22.12.0

## Documentation

- [Architecture](docs/ARCHITECTURE.md) — technical overview of the current codebase
- [Roadmap](docs/ROADMAP.md) — planned features and future enhancements

## License

MIT
