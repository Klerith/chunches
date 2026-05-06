# Chunches Web — Style Guide

Esta es la guía de estilos visual que comparten `index.html` y `policy.html`. Sirve como referencia para mantener consistencia entre páginas y para construir nuevas vistas o contenidos relacionados.

> Filosofía: una estética **dark editorial**, elegante y silenciosa, con acentos cálidos y un toque humano (la curva tipo squiggle bajo palabras clave, el botón coral, la firma "made with ♥ for families").

---

## 1. Paleta de colores

Todos los colores se exponen como variables CSS bajo `:root`.

### 1.1 Marca / acentos

| Token              | Valor                       | Uso                                                           |
| ------------------ | --------------------------- | ------------------------------------------------------------- |
| `--primary`        | `#10b981` (Emerald 500)     | CTA principal, badges activos, links, highlights              |
| `--primary-soft`   | `#34d399` (Emerald 400)     | Hover/links, texto sobre fondos verdes translúcidos           |
| `--primary-glow`   | `rgba(16, 185, 129, 0.32)`  | Halos / box-shadow alrededor del primario                     |
| `--secondary`      | `#06b6d4` (Cyan 500)        | Squiggle del hero, dots `<h3>`, indicadores de estado, notas  |
| `--secondary-soft` | `#22d3ee` (Cyan 400)        | Texto sobre fondos cyan translúcidos                          |
| `--tertiary`       | `#fc7c78` (coral)           | Tarjeta de cierre / contacto, palabra acentuada en el hero    |
| `--tertiary-soft`  | `#fda4a0`                   | Chips y badges suaves del coral                               |
| `--tertiary-deep`  | `#d8514c`                   | Glow radial dentro de la tarjeta coral                        |
| `--neutral`        | `#080808`                   | Negro de marca (igual que `--bg`)                             |

### 1.2 Fondos y superficies

| Token             | Valor      | Uso                                              |
| ----------------- | ---------- | ------------------------------------------------ |
| `--bg`            | `#080808`  | Fondo de la página                               |
| `--bg-2`          | `#0e0e10`  | Fondo de listas, tablas y placeholders de fotos  |
| `--surface`       | `#131318`  | Tarjetas principales (`.section`, chips, tags)   |
| `--surface-2`     | `#1a1a20`  | Cabecera de tablas                               |
| `--surface-hover` | `#22222a`  | Hover de TOC y botones fantasma                  |
| `--line`          | `#25252c`  | Borde estándar                                   |
| `--line-soft`     | `#1a1a20`  | Borde sutil (listas, tablas, footer)             |

### 1.3 Texto

| Token        | Valor      | Uso                                                  |
| ------------ | ---------- | ---------------------------------------------------- |
| `--ink`      | `#f0efea`  | Texto principal sobre fondo oscuro                   |
| `--ink-2`    | `#cfcec9`  | Texto secundario, párrafos largos                    |
| `--muted`    | `#8a8a92`  | Texto auxiliar (subtítulo del hero, captions, meta)  |
| `--muted-2`  | `#5e5e66`  | Texto muy tenue (footer, numeración inactiva del TOC)|

### 1.4 Fondo global

`body` lleva tres `radial-gradient` superpuestos que tiñen la página:

- Verde primario (16% de opacidad) en la esquina superior izquierda.
- Cyan secundario (12%) en la superior derecha.
- Coral terciario (8%) anclado en la parte inferior central.

`background-attachment: fixed` mantiene los halos al hacer scroll.

### 1.5 Selección de texto

`::selection` usa `--primary` como fondo y `--bg` como tinta — un guiño consistente con la identidad.

---

## 2. Tipografía

Tres familias importadas desde Google Fonts:

```html
<link
  href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500;600&display=swap"
  rel="stylesheet"
/>
```

### 2.1 Roles tipográficos

| Token       | Familia                                                  | Rol                                                                                |
| ----------- | -------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `--display` | **Space Grotesk** (`'Helvetica Neue', Arial`)            | Títulos (`.hero-title`, `<h2>`, `<h3>`), botones, brand, chips, TOC, closing card  |
| `--body`    | **Inter** (system fallbacks: Apple, Segoe UI, Roboto…)   | Cuerpo del texto, párrafos largos                                                  |
| `--label`   | **JetBrains Mono** (`ui-monospace`, `SFMono-Regular`…)   | Etiquetas micro (chips, captions, "Last updated", numeritos del TOC, footer)       |

### 2.2 Pesos usados

- Space Grotesk: 400 / 500 / 600 / 700
- Inter: 400 / 500 / 600
- JetBrains Mono: 400 / 500 / 600

> Regla general: **600** para títulos y CTA, **500** para chips/badges/labels, **400** para cuerpo.

### 2.3 Escala de tamaños

| Elemento                   | Tamaño                            | Line-height | Tracking          |
| -------------------------- | --------------------------------- | ----------- | ----------------- |
| `body`                     | 16.5px (16px en mobile)           | 1.65        | normal            |
| `.hero-title` (`<h1>`)     | `clamp(48px, 8vw, 104px)`         | 0.98        | `-0.035em`        |
| `.section h2`              | `clamp(22px, 2.6vw, 28px)`        | 1.2         | `-0.02em`         |
| `.section h3`              | 15px                              | 1.4         | `-0.01em`         |
| `.lede` / `.hero-sub`      | 18px                              | 1.55        | normal            |
| Chips / TOC / botones      | 13–14px                           | 1.4         | `-0.005em`        |
| Labels mono (caps)         | 11–11.5px                         | 1.4         | `0.04em`–`0.06em` |

### 2.4 Detalle decorativo: el squiggle

El hero usa una palabra envuelta en `<span class="squiggle">` con un SVG inline como `background` del `::after`. El stroke del SVG está fijo en `#06B6D4` (cyan, mismo que `--secondary`).

Si se cambia el color secundario, **acordarse de sincronizar el color del SVG en el `data:` URL**.

---

## 3. Forma y elevación

### 3.1 Radios

| Token       | Valor    | Uso                                                |
| ----------- | -------- | -------------------------------------------------- |
| `--r-sm`    | 10px     | Pequeños badges internos                           |
| `--r-md`    | 16px     | Listas, tablas, notas, foto placeholders           |
| `--r-lg`    | 22px     | Tarjetas grandes (`.section`, `.contact`, `.closing`) |
| `--r-pill`  | 999px    | Chips, tags, TOC links, botones                    |

### 3.2 Bordes

- Borde estándar: `1px solid var(--line)`.
- Borde suave (interno): `1px solid var(--line-soft)`.
- Foto placeholders: `1px dashed var(--line)` para indicar contenido pendiente.

### 3.3 Sombras y glows

- CTA primaria: `0 12px 32px -10px var(--primary-glow)`.
- TOC activo: `0 10px 28px -10px var(--primary-glow)`.
- Tarjeta coral (`.contact`, `.closing`): `0 18px 48px -22px rgba(252, 124, 120, 0.55)`.
- Marca (`.brand-mark`): `0 6px 18px var(--primary-glow)`.

> Nunca usar sombras puras negras: siempre derivadas del color del componente, en versión "glow".

---

## 4. Componentes clave

### 4.1 Topbar

- `.brand` con `.brand-mark`: cuadrado 28×28, gradiente `135deg` de `--primary` a `--secondary`, letra C blanca-negruzca (`var(--bg)`).
- `.topbar-meta`: pill con borde `--line`, fondo translúcido, dot cyan a la izquierda con halo verde.

### 4.2 Hero

- `.tag`: pill micro (label mono) con dot `--primary`.
- `.hero-title`: tipografía display al máximo, con dos efectos:
  - `.squiggle`: subrayado ondulado cyan.
  - `.accent`: color `--tertiary` (coral) sobre la palabra final.
- `.hero-sub`: 18px, `--muted`, máx. 60ch.
- `.chip` y variantes (`chip-primary`, `chip-secondary`, `chip-tertiary`): pills tintadas al 14% con bordes al 40%.

### 4.3 Botones (`index.html`)

- `.btn-primary`: fondo `--primary`, texto `--bg`, glow primario, `translateY(-1px)` al hover.
- `.btn-ghost`: fondo `--surface`, borde `--line`, texto `--ink-2`, hover hacia `--surface-hover` y texto `--ink`.

### 4.4 Layout

Grid de dos columnas en ≥1024px: `240px` para el TOC sticky + `1fr` para el contenido. En mobile colapsa a una sola columna y el TOC se vuelve un carrusel horizontal con `scroll-snap-type: x mandatory`.

### 4.5 TOC

- Inactivo: pill `--surface` + número `--muted-2` sobre `--bg-2`.
- Activo: pill `--primary` con glow, número en negro semitransparente.
- Sincronizado con un `IntersectionObserver` que marca la sección visible y, en mobile, hace `scrollIntoView({ inline: 'center' })` sobre el TOC.

### 4.6 Section card

- Tarjeta `.section`: padding 40×36, fondo `--surface`, borde `--line`, radio `--r-lg`.
- `.section-head`: número en cuadrado verde tintado (40×40, label mono) + `<h2>`.
- `<h3>` con un cuadradito cyan delante (`::before`), separador visual sutil entre subsecciones.
- Listas estilizadas: cada `<li>` es una tarjeta `--bg-2` con dot verde con halo a la izquierda.

### 4.7 Tabla

- Wrapper redondeado (`--r-md`), `overflow: hidden` para clipping limpio.
- `thead th`: label mono, mayúsculas, `--muted` sobre `--surface-2`.
- Primer `<td>`: `--ink` y peso 500. Último `<td>`: `--muted`.

### 4.8 Note (banner informativo)

`.note` con gradiente cyan al 12→4%, borde cyan al 32%, ícono circular sólido cyan con signo "!" en display bold. Se usa para reforzar mensajes (ej. "We don't run ads on your data").

### 4.9 Foto placeholder (`index.html`)

`.photo`: aspect-ratio 16/9, gradiente diagonal verde-cyan-coral muy tenue sobre `--bg-2`, borde dashed, grilla de 32px superpuesta vía `::before`. La caption es una pill con blur, label mono y dot cyan.

> Sustituir el placeholder por una `<img>` real cuando estén las capturas. Mantener el `aspect-ratio` y el `border-radius`.

### 4.10 Tarjeta coral (`.contact` / `.closing`)

- Fondo `--tertiary`, texto `#1a0808`.
- Glow blanco superior (`::before`) y glow rojo profundo inferior derecho (`::after`).
- Label mono en versión semitransparente; título display 600.

### 4.11 Footer

- Borde superior `--line-soft`, label mono, color `--muted-2`.
- Corazón en `--tertiary` para sumar calidez.
- En `index.html` añade `.footer-links` con enlaces a privacidad y contacto.

---

## 5. Accesibilidad y motion

- `:focus-visible` global: outline de 2px en `--primary` + offset 4px.
- Botones, TOC y links tienen estados hover y focus diferenciados.
- `@media (prefers-reduced-motion: reduce)`: anula `scroll-behavior: smooth` y baja todas las transiciones/animaciones a `0.001ms`.
- `<meta name="theme-color" content="#080808" />` para que la barra del navegador móvil herede el negro.
- `aria-labelledby` en cada `<section>` apuntando al `id` de su `<h2>`.

---

## 6. Reglas para mantener consistencia

1. **No introducir colores nuevos** sin agregarlos como tokens en `:root`.
2. **Toda tipografía pasa por las tres familias** (`--display`, `--body`, `--label`). No usar fuentes ad-hoc.
3. Los radios siempre vienen de los tokens `--r-*`. Nada de `border-radius: 12px` mágicos (excepto `.section-num` que ya está definido como 12px puntual).
4. Las sombras son **glows** del color del propio componente — nunca negro puro.
5. Si se añade una nueva tarjeta tipo "section", reutilizar `.section` y `.section-head` con su numerito.
6. Los labels mono (`--label`) siempre van con `letter-spacing: 0.04em`–`0.06em` y `text-transform: uppercase` cuando son etiquetas.
7. Para enlaces dentro de párrafos: heredan el color `--primary-soft` y un borde inferior animado; no usar `text-decoration: underline` plano.
8. Mobile breakpoint principal: `720px`. Layout 2-col: `1024px`.

---

_Última actualización: mayo 2026._
