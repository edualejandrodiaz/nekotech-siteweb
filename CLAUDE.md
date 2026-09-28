# Nekotech · sitio web

Sitio de marketing de Nekotech hecho con Astro (HTML estático).

## Identidad visual

La fuente oficial es el Design System "Nekotech" (artifact de claude.ai). Reglas que este código ya aplica y que todo cambio debe respetar:

- Colores solo desde `src/styles/tokens.css`; nunca hex sueltos en componentes. Mismos nombres que en el Design System (`--surface`, `--ink`, `--ambar`, …).
- `--ambar` es el único acento: botón primario una vez por vista y una palabra destacada (`<em>`) por titular. Texto sobre ámbar en `--on-ambar`.
- `--senal` significa solo "agente activo / en línea".
- Tipografías: Chakra Petch (titulares), Hanken Grotesk (texto), JetBrains Mono (etiquetas, datos, wordmark), servidas con @fontsource.
- Esquinas casi rectas: `--radius-sm` en controles, `--radius-md` en tarjetas. Bordes antes que sombras. Sin degradados.
- Voz: español de Chile, tuteo, resultados antes que tecnología, máximo un guiño felino por página (hoy está en la sección Soporte). Sin emojis.

## Estructura

- `src/pages/index.astro` arma la página con los componentes de `src/components/`.
- `src/site.json` guarda los datos de contacto y redes (WhatsApp, correo, LinkedIn, Instagram) y el número de WhatsApp de la demo pública (`demoWhatsapp`), distinto del WhatsApp real de contacto.
- `src/components/CatMark.astro` es el isotipo inline; toma el color del texto.
- `public/llms.txt` describe la empresa para asistentes de IA; actualízalo cuando cambien productos o servicios.

## Comandos

- `npm install`
- `npm run dev` (http://localhost:4321)
- `npm run build` (genera `dist/`)

## Logo

`public/logos/nekotech-logo-horizontal.svg` tiene el texto "nekotech" convertido a trazos vectoriales (a partir de JetBrains Mono Bold), no depende de ninguna fuente instalada. Existe también `nekotech-logo-horizontal-invertido.svg` para fondos oscuros. Si se regenera el logo, mantener el texto como paths, no como `<text>`.

## Deploy

- `.github/workflows/deploy.yml` construye el sitio y lo publica en GitHub Pages en cada push a `main` (o manualmente vía `workflow_dispatch`).
- En GitHub, Settings → Pages → Source debe estar en "GitHub Actions" (no "Deploy from a branch").
- El dominio propio vive en `public/CNAME` (no en la raíz del repo) para que Astro lo copie a `dist/` en cada build.
