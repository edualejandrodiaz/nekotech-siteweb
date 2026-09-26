# nekotech-siteweb

Sitio web de [Nekotech](https://nekotech.cl): agentes de IA y software a medida para pymes.

Hecho con [Astro](https://astro.build) siguiendo el Design System de Nekotech (ver `CLAUDE.md`).

## Antes de publicar

Completa los datos reales en `src/site.json`:

- `whatsapp`: número en formato internacional sin `+` ni espacios (ej. `56912345678`). Hoy tiene un valor de relleno.
- `email`: correo de contacto real.
- `linkedin` e `instagram`: URLs de los perfiles cuando existan.

## Desarrollo

```bash
npm install
npm run dev      # http://localhost:4321
npm run build    # genera dist/
npm run preview  # sirve dist/ localmente
```

## Despliegue

`dist/` es HTML estático: sirve en Netlify, Vercel, Cloudflare Pages, GitHub Pages o S3 + CloudFront.
