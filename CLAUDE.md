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
