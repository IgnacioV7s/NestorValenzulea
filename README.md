# Néstor Valenzuela – sitio web

Sitio estático (HTML + CSS + JS, sin dependencias). Se despliega solo en GitHub Pages con `.github/workflows/static.yml` al hacer push a `main`.

```
index.html          Contenido y metadatos (SEO / vista previa al compartir)
css/style.css       Estilos (mobile-first; variables de color en :root)
js/main.js          Menú, enlace activo, reproductor, galería
assets/img/         Imágenes en WebP (og.jpg es la vista previa al compartir)
assets/audio/       Sencillos en MP3
assets/fonts/       Qualy Bold (WOFF)
```

## Cómo agregar cosas

- **Sencillo nuevo**: copia un bloque `<article class="track">` en `#singles`, cambia portada, título y `src` del `<audio>`. El JS lo detecta solo.
- **Foto nueva**: agrega un `<figure class="gallery__item">` en `#gallery` (con `width`, `height` y un `alt` que describa la foto). Exporta en WebP, ~1000 px de lado largo.
- **Álbum nuevo**: copia un `<article class="album">` en `#albums`.
- **Colores**: `--gold` y `--gold-bright` en `:root` de `css/style.css`.

## Pendiente recomendado

- Descargar las portadas de los álbumes (hoy se cargan desde `mzstatic.com` de Apple) a `assets/img/` y cambiar el `src`.
- Si se cambia el dominio, actualizar `og:url` y `og:image` en `index.html` (necesitan URL absoluta).
