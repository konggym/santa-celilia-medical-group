# Dr. David Collazo Medical Group

App web (PWA) para los consultorios: agenda, historial clínico, recetas/certificados imprimibles y punto de venta de farmacia.

- `index.html` — toda la app (HTML/CSS/JS en un solo archivo, sin build). Estado en `localStorage` del dispositivo.
- `logo-mark.png` / `logo-full.png` — logotipo de la marca, usados en la app y en recetas/certificados impresos.
- `manifest.webmanifest`, `sw.js`, `icons/` — hacen la app instalable (PWA) y funcional sin internet.
- `wrangler.jsonc`, `_headers`, `.assetsignore` — configuración de publicación en Cloudflare Workers.

Publicada con Cloudflare Workers: cada cambio que se sube a la rama `main` se publica solo.

Si se actualiza `index.html` (o los logos), sube el número de versión en `sw.js` (`VERSION`) para que los celulares con la app ya instalada reciban el cambio.
