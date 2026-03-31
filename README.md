# duranivan.com

Personal website built with [Astro](https://astro.build), deployed to GitHub Pages.

## Stack

- Astro 6
- IBM Plex Mono (self-hosted via @fontsource)
- Dark / light / system theme toggle
- Static site, no frameworks or runtime JS beyond the theme script

## Development

```sh
npm install
npm run dev
```

## Build & Deploy

Pushes to `main` trigger automatic deployment via GitHub Actions.

```sh
npm run build    # outputs to ./dist/
npm run preview  # preview build locally
```

## License

MIT
