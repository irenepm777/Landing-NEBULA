# Landing page de Nébula

Landing page de **Nébula**, una artista digital especializada en paisajes de ciencia ficción.
Práctica de Diseño de Interfaces Web · 2º DAW · iLERNA · Irene Pascual Moreno.

**Web online (GitHub Pages):** `https://irenepm777.github.io/Landing-NEBULA/`

---

## Idea y guía de estilo

Muchas de las landings que he visto para este ejercicio acaban siendo fotos coloridas de nebulosas. Yo quería que Nébula tuviera una identidad propia, así que fui a una estética **monocroma de semitono y grano**, como un grabado o una fotocopia, con un aire editorial.

| Elemento | Decisión |
|---|---|
| Fondo | `#141312` (carbón cálido, no negro puro, para que el grano respire) |
| Tinta | `#e9e4d8` (blanco hueso). Contraste sobre el fondo: **14,9:1 (AAA)** |
| Texto secundario | `#9c968a`. Contraste: **5,6:1 (AA)** |
| Títulos | *Instrument Serif* en cursiva y mayúsculas (lo "humano", lo poético) |
| Texto | *IBM Plex Mono* (lo técnico, el código del que salen las obras) |
| Textura | Imagen de fondo SVG con ruido muy sutil, a juego con el grano de las obras |
| Accesibilidad | `alt` descriptivos, estado `:focus` visible, jerarquía H1 → H2 → H3, contrastes AA/AAA |

## Estructura del proyecto

```
Landing-NEBULA/
├── .gitignore
├── index.html
├── README.md
└── assets/
    ├── audio/
    │   └── audio-nebula.mp3            (15 s)
    ├── img/
    │   ├── animacion/
    │   │   ├── animacion_01.webp       (fotograma 1)
    │   │   ├── animacion_02.webp       (fotograma 2)
    │   │   ├── animacion_03.webp       (fotograma 3)
    │   │   ├── animacion_04.webp       (fotograma 4)
    │   │   └── animacion.webp          (WebP animado en bucle)
    │   ├── galeria/                    (6 obras: 0N_nombre.webp a tamaño completo
    │   │                                + 0N_nombre_thumbnail.webp de 400×250)
    │   ├── hero-nebula.webp            (1920×667, 153 KB)
    │   ├── logo.webp
    │   ├── poster.webp
    │   └── retrato-nebula.webp         (750×1000) · sección "Sobre mí"
    └── video/
        └── video-nebula.mp4            (H.264, menos de 3 MB)
```

---

## 1. Tabla de recursos y licencias

En el HTML, el hero, el retrato, cada obra de la galería, el vídeo y el audio llevan su atribución en un
`<figure>` + `<figcaption>` con título, autoría, enlace a la obra original y enlace al texto de la licencia. El logotipo se atribuye en el `<footer>`.

**Sobre las licencias:** Pexels, Unsplash y Pixabay **no usan licencias Creative Commons**, sino licencias propias. Las tres permiten usar, modificar y publicar el contenido gratis, incluso con fines comerciales, y sin obligación de atribuir. Aun así, en la web y en esta tabla atribuyo cada recurso (título, autor con enlace a la obra, plataforma y licencia), que es lo que piden los apuntes y la rúbrica.

| Archivo | Tipo | URL original de descarga | Autor/a | Licencia |
|---|---|---|---|---|
| `assets/img/hero-nebula.webp` | Imagen (hero) | [Pexels](https://www.pexels.com/photo/light-painting-in-close-up-shot-14314635/) | Merlin Lightpainting | [Licencia de Pexels](https://www.pexels.com/license/) |
| `assets/img/retrato-nebula.webp` | Retrato "Sobre mí" | [Pexels](https://www.pexels.com/es-es/foto/ligero-mujer-creativo-pared-5785454/) | Diana | [Licencia de Pexels](https://www.pexels.com/license/) |
| `assets/img/logo.webp` | Logotipo | [Unsplash](http://unsplash.com/es/fotos/un-anillo-morado-con-fondo-negro-Zw2nRt2z5f0) | Maxim Landolfi | [Licencia de Unsplash](https://unsplash.com/es/licencia) |
| `assets/img/galeria/01_deriva_urbana.webp` + `_thumbnail` | Galería | [Pexels](https://www.pexels.com/photo/dynamic-abstract-digital-light-burst-30547579/) | Pachon In Motion | [Licencia de Pexels](https://www.pexels.com/license/) |
| `assets/img/galeria/02_reliquia.webp` + `_thumbnail` | Galería | [Pexels](https://www.pexels.com/photo/futuristic-spacecraft-hovering-above-clouds-32232401/) | Adis Resic | [Licencia de Pexels](https://www.pexels.com/license/) |
| `assets/img/galeria/03_corona.webp` + `_thumbnail` | Galería | [Pexels](https://www.pexels.com/photo/electric-light-streaks-14314637/) | Merlin Lightpainting | [Licencia de Pexels](https://www.pexels.com/license/) |
| `assets/img/galeria/04_interfaz.webp` + `_thumbnail` | Galería | [Pexels](https://www.pexels.com/photo/modern-illuminated-machine-in-black-and-white-21044343/) | Kylie Miller | [Licencia de Pexels](https://www.pexels.com/license/) |
| `assets/img/galeria/05_transito.webp` + `_thumbnail` | Galería | [Unsplash](https://unsplash.com/es/fotos/un-primer-plano-de-un-objeto-con-un-fondo-borroso-hJBexgY80cs) | Steve A Johnson | [Licencia de Unsplash](https://unsplash.com/es/licencia) |
| `assets/img/galeria/06_cupula.webp` + `_thumbnail` | Galería | [Pexels](https://www.pexels.com/photo/dome-in-black-and-white-18180323/) | Rishabh Mewada | [Licencia de Pexels](https://www.pexels.com/license/) |
| `assets/video/video-nebula.mp4` | Vídeo | [Pexels](https://www.pexels.com/video/mesmerizing-black-and-white-kaleidoscope-loop-33760678/) | Tunnel Motions | [Licencia de Pexels](https://www.pexels.com/license/) |
| `assets/img/poster.webp` | Póster del vídeo | Captura de un fotograma del vídeo anterior | Tunnel Motions | [Licencia de Pexels](https://www.pexels.com/license/) |
| `assets/audio/audio-nebula.mp3` | Audio | [Pixabay](https://pixabay.com/es/sound-effects/pel%C3%ADculas-y-efectos-especiales-sci-fi-survival-dreamscape-6319/) | freesound_community | [Licencia de contenido de Pixabay](https://pixabay.com/es/service/license-summary/) |
| `assets/img/animacion/animacion_01.webp` … `animacion_04.webp` y `animacion.webp` | Animación CTA | Creación propia: 4 fotogramas generados con Gemini y montados con Aspose | Irene Pascual Moreno | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.es) |
| Instrument Serif · IBM Plex Mono | Tipografías | [Google Fonts](https://fonts.google.com/) | Rodrigo Fuenzalida / IBM | [SIL Open Font License 1.1](https://openfontlicense.org/) |

---

## 2. Justificación técnica de formatos

| Recurso | Formato | Por qué |
|---|---|---|
| Hero | **WebP** | Imagen de trama compleja sin transparencia. Exactamente **1920 px** de ancho y **153 KB** (por debajo de 250 KB). WebP ahorra un 25-35 % frente a JPG con la misma calidad visual y es compatible con todos los navegadores modernos. |
| Retrato | **WebP con canal alfa** | La imagen tiene el fondo transparente. WebP conserva esa transparencia igual que un PNG, pero pesa mucho menos. La redimensioné a 750×1000 px, que se ve nítido en pantallas 2x sin cargar píxeles de más. |
| Galería | **WebP** | Miniaturas de **400×250 exactos** (`_thumbnail`) para la rejilla, que pesan muy poco. La versión grande solo se descarga si se pulsa la obra. |
| Logotipo | **WebP con canal alfa** | El logo es un anillo de semitono con puntos y degradados, así que no se puede convertir en formas vectoriales limpias. Por eso uso un formato de mapa de bits y no SVG. Elegí WebP en lugar de PNG porque también tiene canal alfa, así que el fondo es transparente y el anillo queda bien sobre el fondo oscuro de la web, pero pesa bastante menos que un PNG con la misma calidad. Se muestra a 32 px en la cabecera y también se usa como favicon. |
| Animación CTA | **WebP animado** | Monté los 4 fotogramas fijos en un WebP animado en bucle. Frente a un GIF, el WebP animado pesa menos, admite millones de colores (el GIF solo 256) y transparencia suave de 8 bits (el GIF solo binaria, lo que deja bordes dentados). Es la opción que recomienda el enunciado por rendimiento. |
| Vídeo | **MP4 (H.264)** | MP4 con el códec H.264 es la combinación con compatibilidad universal: funciona en todos los navegadores modernos, en iOS y en Android. El archivo pesa menos de 3 MB. Formatos como .avi o .mov no se reproducen de forma nativa en la web. |
| Póster | **WebP** | Es la miniatura de precarga del vídeo: se ve antes de que el usuario pulse play, así que tiene que pesar poco. WebP da la misma calidad que un JPG con menos peso. |
| Audio | **MP3** | Compatible con el 100 % de los navegadores. Es un ambiente musical, así que lo exporté con el bitrate recomendado para música (192 kbps, estéreo, 44,1 kHz) en vez del de voz (128 kbps). |

**Nota WPO:** el enunciado pide `loading="lazy"` en todas las imágenes estáticas, así que también lo lleva el hero.
En un proyecto real, el hero (el *Largest Contentful Paint*) iría con `loading="eager"` y `fetchpriority="high"`.

Todas las `<img>` llevan `alt` descriptivo, `width` y `height` (así se reserva el hueco y se evitan los saltos de
maquetación) y `loading="lazy"`. El vídeo usa `poster="assets/img/poster.webp"` y `preload="metadata"`.

---

## 3. Tratamiento y herramientas utilizadas

| Proceso | Herramienta | Qué hice |
|---|---|---|
| Descarga de recursos | **Pexels**, **Unsplash** y **Pixabay** | Descargué todas las fotos y el vídeo de Pexels y Unsplash, y el audio de Pixabay. Comprobé la licencia de cada recurso y apunté su autor y su enlace (ver tabla de recursos). |
| Hero | **GIMP** | Redimensioné la imagen a un ancho exacto de 1920 px, manteniendo el aspect ratio (1920×667), y la exporté a WebP para que pesara menos de 250 KB. |
| Galería | **GIMP** | Creé una miniatura de 400×250 px de cada obra (`_thumbnail`) y exporté tanto las miniaturas como las versiones grandes a WebP. |
| Retrato y logotipo | **GIMP** | Redimensioné las imágenes y las exporté a WebP conservando el canal alfa (fondo transparente). |
| Audio | **Audacity** | Recorté el clip para que durara exactamente 15 segundos, le apliqué un fade-in y un fade-out suaves y lo exporté a MP3 a 192 kbps. |
| Fotogramas de la animación | **Gemini** (IA generativa, permitida por el profesor) | Generé 4 imágenes fijas (`animacion_01.webp` a `animacion_04.webp`) que funcionan como fotogramas de la animación del botón de contacto. |
| Montaje de la animación | **Aspose** (conversor web) | Uní los 4 fotogramas en un WebP animado en bucle (`animacion.webp`). |
| Vídeo | **Pexels** | El vídeo descargado ya cumplía los requisitos (MP4 con H.264 y menos de 3 MB), así que no tuve que transcodificarlo. |
| Póster del vídeo | **GIMP** | Hice una captura de pantalla de un fotograma del vídeo, la redimensioné y la exporté como `poster.webp`. |
| Maquetación | **HTML5 + CSS** | Estructura semántica con `header`, `nav`, `main`, `section`, `figure` y `footer`, y diseño responsive con Flexbox, Grid y media queries. |

## Publicación en GitHub Pages
*Settings → Pages → Deploy from a branch → `main` / `(root)`*. Como el `index.html` está en la raíz, la web queda publicada directamente en la URL del repositorio.