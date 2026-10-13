# Spec de desarrollo — For Magos

> Guía: [Spec de desarrollo](../evaluacion/guias/fase-2-specs/07-spec-de-desarrollo.md)

## Insumos y prompt para el asistente

```text
Lee DESIGN.md, docs/09-spec-diseno.md y docs/10-spec-desarrollo.md.
En la carpeta stitch/ está el código exportado de Stitch de cada pantalla.
Construye el sitio de For Magos siguiendo exactamente docs/10-spec-desarrollo.md:
solo HTML y CSS (sin frameworks, sin Tailwind y sin el CSS exportado de Stitch),
la estructura de archivos y la navegación definidas, las variables de :root
con los valores de DESIGN.md y la estructura semántica de cada página.
Usa los nombres de componentes de DESIGN.md como nombres de clase
(card-product → .card-product, button-primary → .button-primary).
Usa el código de Stitch solo como referencia visual. Diseña mobile first.
Al terminar, revisa cada criterio de aceptación de la sección 5 y dime
cuáles se cumplen y cuáles no.
```

## 1. Estructura de archivos

```text
for-magos/
├── index.html                  ← landing
├── tienda.html
├── producto.html               ← ficha de producto (Camiseta Chile 1998)
├── carrito.html
├── blog.html
├── articulo.html               ← "5 camisetas retro que todo coleccionista quiere"
├── contacto.html
├── preguntas-frecuentes.html   ← incluye guía de tallas, envíos y cambios
├── terminos.html
├── privacidad.html
├── 404.html
├── DESIGN.md
├── README.md
├── css/
│   ├── base.css                ← :root con tokens, reset, tipografía, layout
│   └── components.css          ← un bloque por componente de DESIGN.md
├── img/
│   ├── productos/              ← chile-1998-frente.webp, colo-colo-1991.webp…
│   ├── blog/
│   └── marca/                  ← logo-for-magos.svg, favicon.png
├── stitch/                     ← código exportado de Stitch (solo referencia)
└── docs/
```

Nombres de archivo en minúsculas, con guiones, sin espacios ni tildes. Las categorías de la tienda y del blog **no son páginas aparte**: son chips que filtran dentro de `tienda.html` y `blog.html` (en el prototipo, un chip activo distinto por pantalla).

## 2. Páginas y navegación

- **Navbar en todas las páginas:** logo (→ `index.html`), Tienda, Clubes, Selecciones, Retro (→ `tienda.html`), Blog (→ `blog.html`), buscador (→ `tienda.html`) y carrito (→ `carrito.html`).
- **Footer en todas las páginas:** Tienda (Clubes, Selecciones, Retro, Accesorios), Ayuda (Preguntas frecuentes, Envíos y cambios, Contacto), Legal (Términos y condiciones, Política de privacidad) e Instagram @for.magos.

| Desde | Elemento | Lleva a |
|---|---|---|
| index.html | `button-primary` "VER CAMISETAS" del hero | tienda.html |
| index.html | `button-secondary` "LEER EL BLOG" del hero | blog.html |
| index.html | `card-category` CLUBES / SELECCIONES / RETRO / ACCESORIOS | tienda.html |
| index.html | `card-product` de camisetas destacadas | producto.html |
| index.html | `newsletter-form` "QUIERO MI 10 % OFF" | misma página, muestra `message-success` |
| tienda.html | `card-product` (toda la card) | producto.html |
| producto.html | `button-primary` "AGREGAR AL CARRITO" | carrito.html |
| producto.html | Enlace "Guía de tallas" | preguntas-frecuentes.html#tallas |
| producto.html | `whatsapp-link` | https://wa.me/56900000000 (nueva pestaña) |
| producto.html | `card-product` de "También te puede gustar" | producto.html |
| carrito.html | `button-secondary` "SEGUIR COMPRANDO" | tienda.html |
| carrito.html | `button-primary` "FINALIZAR COMPRA" | carrito.html#pago (prototipo: mensaje "Pago no disponible en esta versión") |
| blog.html | `card-article` | articulo.html |
| articulo.html | `button-secondary` "VER PRODUCTO" de "Productos del artículo" | producto.html |
| articulo.html | `share-bar` | Enlaces para compartir en Instagram, WhatsApp (`https://wa.me/?text=`), X (`https://x.com/intent/post?url=`) y copiar enlace |
| Cualquier página | URL que no existe | 404.html (con botón "VOLVER A LA TIENDA" → tienda.html) |

Así se recorren los dos user flows de [`05-arquitectura.md`](05-arquitectura.md):

- **Compra:** index.html → tienda.html → producto.html → carrito.html.
- **Contenido:** index.html → blog.html → articulo.html → producto.html → carrito.html.

## 3. Estructura semántica

Todas las páginas comparten:

```html
<body>
  <a class="skip-link" href="#contenido">Saltar al contenido</a>
  <div class="announcement-bar">…</div>
  <header class="navbar"> <nav aria-label="Principal">…</nav> </header>
  <main id="contenido">…</main>
  <footer class="footer">…</footer>
</body>
```

### index.html

```html
<main>
  <section class="hero">           h1 + bajada + 2 botones + imagen
  <section class="categories">     h2 + 4 card-category (<a>)
  <section class="featured">       h2 + grilla de card-product (cada una <article>)
  <section class="benefits">       3 beneficios (<ul>)
  <section class="newsletter-form"> h2 + <form> con <label> e <input type="email">
</main>
```

### tienda.html

```html
<main>
  <section class="shop-header">  h1 "Tienda" + <form role="search"> + chips (<ul> de <a>)
  <aside class="filters">        <form> con <fieldset> Talla, Equipo, Precio
  <section class="product-grid"> resultado + card-product (<article>) + <nav aria-label="Paginación">
</main>
```

### producto.html

```html
<main>
  <nav aria-label="Migas de pan">
  <section class="product-detail">
    <div class="gallery">         <img> principal + miniaturas
    <div class="product-info">    h1, precio, tag-stock, <form> con <fieldset> de tallas
                                  (radio buttons), cantidad, button-primary, whatsapp-link, descripción
  </section>
  <section class="related">      h2 + card-product
</main>
```

### carrito.html

```html
<main>
  <h1>Tu carrito (2)</h1>
  <section class="cart-items">    <ul> de cart-item (<li>)
  <aside class="order-summary">   h2 + <form> comuna/código + <dl> subtotal, despacho, descuento, total + botones
</main>
```

### blog.html

```html
<main>
  <section class="blog-header"> h1 + bajada + chips de categoría
  <section class="article-grid"> card-article (<article>, con <time>)
  <section class="newsletter-form">
</main>
```

### articulo.html

```html
<main>
  <article class="post">
    <header> migas + h1 + <time> + share-bar </header>
    <figure> imagen + <figcaption>
    <section> cuerpo con h2 por camiseta
    <section class="post-products"> h2 + card-product
    <footer> share-bar
  </article>
  <section class="comment-box"> h2 + lista de comentarios + <form>
</main>
```

### Páginas obligatorias

`contacto.html` (h1 + formulario + WhatsApp + Instagram), `preguntas-frecuentes.html` (h1 + `<details>` por pregunta, con `id="tallas"` para la guía de tallas), `terminos.html` y `privacidad.html` (h1 + secciones h2), `404.html` (h1 "Esta camiseta no está en la vitrina" + botón a la tienda).

## 4. Organización del CSS

```css
:root {
  /* Colores (DESIGN.md → colors) */
  --color-primary: #C6A15B;
  --color-primary-hover: #D4B56F;
  --color-primary-active: #A8864A;
  --color-on-primary: #0B0B0B;
  --color-secondary: #171717;
  --color-tertiary: #9C7F4C;
  --color-bg: #0B0B0B;
  --color-surface: #141414;
  --color-surface-raised: #1F1F1F;
  --color-footer: #080808;
  --color-text: #F5F5F5;
  --color-text-soft: #A6A6A6;
  --color-outline: #343434;
  --color-disabled: #2A2A2A;
  --color-on-disabled: #9A9A9A;
  --color-success: #5FBF85;
  --color-error: #E5645F;

  /* Tipografía (DESIGN.md → typography) */
  --font-title: 'Montserrat', sans-serif;
  --font-body: 'Inter', sans-serif;
  --fs-display: 48px;
  --fs-lg: 32px;
  --fs-md: 24px;
  --fs-title: 18px;
  --fs-body: 16px;
  --fs-small: 14px;
  --fs-label: 12px;

  /* Espaciados (DESIGN.md → spacing) */
  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 32px;
  --space-2xl: 48px;
  --space-3xl: 64px;

  /* Radios (DESIGN.md → rounded) */
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 16px;
  --radius-full: 9999px;

  /* Sombras y movimiento (DESIGN.md → Elevation & Depth) */
  --shadow-card: 0 8px 24px rgba(0, 0, 0, 0.30);
  --shadow-card-hover: 0 10px 30px rgba(198, 161, 91, 0.10);
  --transition: 250ms ease;

  --max-width: 1280px;
}
```

- **Clases:** mismos nombres que los componentes de `DESIGN.md` (`.navbar`, `.hero`, `.button-primary`, `.button-secondary`, `.chip-filter`, `.card-product`, `.card-article`, `.size-selector`, `.cart-item`, `.order-summary`, `.footer`). Estados con modificador `is-`: `.chip-filter.is-active`, `.size-selector.is-disabled`, `.nav-link.is-active`.
- **Breakpoints** (de `## Layout`), mobile first:
  - base: mobile (hasta 767px) → 2 columnas de productos, menú hamburguesa.
  - `@media (min-width: 768px)` tablet → 3 columnas.
  - `@media (min-width: 1024px)` desktop → 4 columnas, navbar completa, filtros en columna lateral.
- **Fuentes:** Montserrat 600/700 e Inter 400/600 desde Google Fonts con `display=swap`.
- **Archivos:** `base.css` (variables, reset, tipografía, contenedor, utilidades) y `components.css` (un bloque comentado por componente, en el mismo orden que `DESIGN.md`).
- Ningún color, tamaño de letra o radio se escribe a mano: todo sale de las variables.

## 5. Criterios de aceptación

**Navegación**
- [ ] La announcement-bar, la navbar y el footer son iguales en las 11 páginas.
- [ ] Se completa el flujo de compra: index → tienda → producto → carrito, solo con clics.
- [ ] Se completa el flujo de contenido: index → blog → artículo → producto → carrito.
- [ ] El ícono del carrito es visible en todas las páginas y en todos los anchos.
- [ ] No hay enlaces rotos (revisado con la extensión "Check My Links" o similar).
- [ ] La página 404 tiene un botón que lleva a la tienda.

**Funcionalidades**
- [ ] La landing tiene un formulario de correo con el texto "10 % OFF en tu primera compra" y un input `type="email"` con `required`.
- [ ] La tienda tiene buscador, 6 chips de categoría y filtros por talla, equipo y precio.
- [ ] Cada card-product muestra foto, nombre, equipo, precio y estado de stock.
- [ ] La ficha de producto muestra tallas (con las agotadas deshabilitadas), stock, guía de tallas, botón "Agregar al carrito" y enlace a WhatsApp.
- [ ] El carrito muestra comuna de despacho, subtotal, despacho, descuento y total.
- [ ] El blog tiene chips de categoría (Camisetas icónicas, Guía de compra, Novedades y lanzamientos).
- [ ] El artículo tiene botones para compartir en Instagram, WhatsApp y X, productos del artículo y una sección de comentarios con formulario.

**Diseño**
- [ ] Todos los colores, fuentes, espaciados y radios del CSS salen de las variables de `:root`, con los valores de `DESIGN.md`.
- [ ] El sitio usa solo HTML y CSS propios (sin Tailwind ni el CSS exportado de Stitch).
- [ ] El fondo de todas las páginas es `--color-bg` y el dorado solo aparece en botones principales, precios, chips activos y etiquetas.
- [ ] El nombre del producto ocupa máximo 2 líneas (`-webkit-line-clamp: 2`).
- [ ] Hay máximo un `button-primary` por sección.
- [ ] Botones, chips, cards y enlaces tienen estado hover con transición de 200–300ms.

**Responsive**
- [ ] En mobile (375px) la tienda muestra 2 productos por fila; en tablet, 3; en desktop, 4.
- [ ] En mobile la navbar usa menú hamburguesa y los filtros se abren con un botón "Filtrar".
- [ ] En mobile el botón "Agregar al carrito" de la ficha queda fijo al fondo de la pantalla.
- [ ] No hay scroll horizontal en 375px de ancho.
- [ ] Las áreas táctiles miden al menos 44 × 44px.

**Accesibilidad y publicación**
- [ ] Todas las imágenes tienen `alt` descriptivo (ej: "Camiseta retro de Chile 1998, vista frontal").
- [ ] Cada página tiene un solo `h1` y los títulos siguen el orden h1 → h2 → h3.
- [ ] Todos los inputs tienen un `<label>` asociado.
- [ ] El contraste de texto cumple AA (4.5:1), como se verificó en `08-color-tipografia.md`.
- [ ] Se puede recorrer el sitio con teclado y el foco es visible (contorno dorado).
- [ ] El sitio está publicado en GitHub Pages y el link está en el `README.md`.
