# PAGINA-WEB
Portfolio de Cristina Mora Pérez, montadora y coordinadora de postproducción.

La web es un único `index.html`, sin dependencias aparte de Google Fonts. Tiene tres secciones, Trabajos, Showreel y Sobre mí, que se muestran una a una desde el menú de arriba.

## Editar el contenido
Al principio del `<script>` de `index.html`:
- `SHOWREEL`: pega el enlace de Vimeo o YouTube. Si está vacío, se ve "Showreel próximamente".
- `TRABAJOS`: un objeto por trabajo, en el orden en que se muestran, con:
  - `titulo`, `categoria`, `rol` y `anio` (`anio` puede ir vacío).
  - `video`: enlace de Vimeo o YouTube.
  - `thumb`: imagen de la tarjeta.
  - Opcionales: `encaje: "contain"` y `fondo` para carteles verticales, `poster` (cartel) y `fotos` (lista de fotogramas).

  - `duracion`: duración del vídeo (`"HH:MM:SS:FF"`). Si solo hay fotos, la tarjeta muestra `00:00:00:00`.

  Las imágenes van en `assets/fotos/`.
- `IDIOMAS`: los idiomas que aparecen en Sobre mí.
- `TRADUCCIONES`: la versión en catalán (`ca`) e inglés (`en`) de cada categoría y rol escritos en castellano. Si falta una, se muestra en castellano. El resto de textos está en `TEXTOS`, en catalán, castellano e inglés.

La web se abre en el idioma del navegador (catalán, castellano o inglés; si no es ninguno de ellos, en castellano). El selector CA · ES · EN de arriba a la derecha lo cambia y la web lo recuerda.
- `EXPERIENCIA`: `desde` (año), `hasta` (año; `null` si sigue en curso; se puede quitar si es un solo año), `rol`, `proyecto` y `tipo`. La timeline se ordena y se reparte en pistas sola.

Los enlaces normales de Vimeo y YouTube (`https://vimeo.com/123456`, `https://youtu.be/abc`) se convierten solos al formato para insertarlos en la página.

## Ver la web en local
Abre `index.html` con el navegador. Desde `file://`, YouTube puede bloquear los vídeos; en GitHub Pages funcionan.

## Publicar (GitHub Pages)
Settings → Pages → "Deploy from branch" → `main` / `(root)`.
La web queda en `https://crismorape.github.io/PAGINA-WEB/`.
