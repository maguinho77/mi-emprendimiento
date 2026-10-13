---
version: alpha
name: For Magos
description: "Design system de For Magos, tienda online de camisetas de fútbol actuales y retro, con estética urbana, premium y deportiva en negro carbón y dorado."
colors:
  primary: "#C6A15B"
  primary-hover: "#D4B56F"
  primary-active: "#A8864A"
  on-primary: "#0B0B0B"
  secondary: "#171717"
  on-secondary: "#F5F5F5"
  tertiary: "#9C7F4C"
  on-tertiary: "#FFFFFF"
  neutral: "#0B0B0B"
  surface: "#141414"
  surface-raised: "#1F1F1F"
  footer: "#080808"
  on-surface: "#F5F5F5"
  on-surface-variant: "#A6A6A6"
  outline: "#343434"
  disabled: "#2A2A2A"
  on-disabled: "#9A9A9A"
  success: "#5FBF85"
  error: "#E5645F"
  white: "#F5F5F5"
typography:
  headline-display:
    fontFamily: Montserrat
    fontSize: 48px
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: -0.01em
  headline-lg:
    fontFamily: Montserrat
    fontSize: 32px
    fontWeight: 700
    lineHeight: 1.2
  headline-md:
    fontFamily: Montserrat
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.25
  title-md:
    fontFamily: Montserrat
    fontSize: 18px
    fontWeight: 600
    lineHeight: 1.3
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
  label-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.04em
  label-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.08em
rounded:
  sm: 4px
  md: 8px
  lg: 16px
  full: 9999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  2xl: 48px
  3xl: 64px
components:
  announcement-bar:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-sm}"
    padding: 8px 16px
  navbar:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
    typography: "{typography.label-md}"
    height: 72px
    padding: 0 32px
  nav-link:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
    typography: "{typography.label-md}"
  nav-link-hover:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.primary-hover}"
  nav-link-active:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.primary}"
  hero:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
    typography: "{typography.headline-display}"
    padding: 64px 32px
    height: 560px
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 14px 28px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
  button-primary-active:
    backgroundColor: "{colors.primary-active}"
    textColor: "{colors.on-primary}"
  button-primary-disabled:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
  button-secondary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 14px 28px
  button-secondary-hover:
    backgroundColor: "{colors.surface-raised}"
    textColor: "{colors.primary-hover}"
  button-secondary-active:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.primary}"
  button-secondary-disabled:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-disabled}"
  search-bar:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.full}"
    padding: 12px 20px
    height: 48px
  input-field:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: 12px 14px
    height: 48px
  input-field-active:
    backgroundColor: "{colors.surface-raised}"
    textColor: "{colors.on-surface}"
  input-field-error:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.error}"
  input-field-disabled:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
  chip-filter:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: 10px 18px
  chip-filter-hover:
    backgroundColor: "{colors.surface-raised}"
    textColor: "{colors.primary-hover}"
  chip-filter-active:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
  card-category:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.white}"
    typography: "{typography.headline-md}"
    rounded: "{rounded.lg}"
    height: 320px
  card-product:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-secondary}"
    typography: "{typography.title-md}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  card-product-hover:
    backgroundColor: "{colors.surface-raised}"
    textColor: "{colors.on-secondary}"
  price:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.primary}"
    typography: "{typography.title-md}"
  size-selector:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    size: 48px
  size-selector-hover:
    backgroundColor: "{colors.surface-raised}"
    textColor: "{colors.primary-hover}"
  size-selector-active:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
  size-selector-disabled:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
  tag-offer:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: 6px 12px
  tag-new:
    backgroundColor: "{colors.white}"
    textColor: "{colors.neutral}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: 6px 12px
  tag-last-units:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.primary}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: 6px 12px
  tag-stock:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.success}"
    typography: "{typography.label-sm}"
  card-article:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.title-md}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  card-article-hover:
    backgroundColor: "{colors.surface-raised}"
    textColor: "{colors.on-surface}"
  share-bar:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface-variant}"
    typography: "{typography.label-sm}"
  comment-box:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: "{spacing.lg}"
  cart-item:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  order-summary:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-secondary}"
    typography: "{typography.body-md}"
    rounded: "{rounded.lg}"
    padding: "{spacing.lg}"
  newsletter-form:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.headline-md}"
    rounded: "{rounded.lg}"
    padding: "{spacing.2xl}"
  message-success:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.success}"
    typography: "{typography.body-sm}"
  message-error:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.error}"
    typography: "{typography.body-sm}"
  whatsapp-link:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.tertiary}"
    typography: "{typography.label-md}"
  footer:
    backgroundColor: "{colors.footer}"
    textColor: "{colors.on-surface-variant}"
    typography: "{typography.body-sm}"
    padding: 64px 32px
  page:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
  text-secondary:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface-variant}"
---

## Overview

For Magos es una tienda online de camisetas de fútbol: clubes, selecciones, camisetas retro de colección y accesorios. Su usuario principal es **Matías, 22 años**, estudiante e hincha que compra desde el celular, llega desde Instagram y usa la camiseta como prenda de moda y como símbolo de identidad. Busca camisetas actuales y retro, compara precios y tallas, y abandona si el sitio es desordenado, si no ve el stock o si la foto no muestra bien el producto.

La sensación que se busca (ver moodboard) es **abrir una vitrina de colección en plena calle**: exclusivo, premium y con historia, pero con actitud streetwear. El negro carbón domina y deja que la camiseta sea protagonista; el dorado es el detalle de trofeo y edición limitada.

Palabras clave: coleccionismo, retro, streetwear deportivo, premium, nostalgia, autenticidad, edición limitada.

## Colors

- **Primary – Dorado suave (#C6A15B):** botones principales, precios, chips activos, enlaces importantes, `tag-offer` e indicadores activos. Es un acento: nunca cubre más del 10 % de una pantalla.
- **Primary Hover (#D4B56F) / Primary Active (#A8864A):** solo para estados hover y presionado de elementos dorados.
- **Neutral – Negro carbón (#0B0B0B):** fondo de la página. Domina el sitio y genera contraste con las fotos de camisetas.
- **Surface (#141414) y Surface Raised (#1F1F1F):** cards, menús, buscador, inputs y contenedores. Surface Raised marca el hover.
- **Secondary – Gris negro (#171717):** fondo de `card-product`, `card-category` y `order-summary`, para separarlos del fondo.
- **Footer (#080808):** solo en el footer.
- **On Surface – Blanco (#F5F5F5):** títulos, nombres de producto, navegación e información importante.
- **On Surface Variant – Gris (#A6A6A6):** descripciones, categorías, fechas y textos complementarios.
- **Tertiary – Dorado oscuro (#9C7F4C):** íconos decorativos y el enlace de WhatsApp. No se usa para texto pequeño sobre fondos claros.
- **Success (#5FBF85):** "En stock" y confirmaciones (correo registrado, producto agregado).
- **Error (#E5645F):** errores de formulario y "Agotado".
- No se usan colores saturados fuera de esta paleta, ni fondos distintos por producto.

## Typography

- **Títulos: Montserrat** (Google Fonts), Bold 700 y SemiBold 600. Se siente deportiva y recuerda la tipografía de los dorsales.
- **Textos y botones: Inter** (Google Fonts), Regular 400 y SemiBold 600. Muy legible en pantallas pequeñas.

| Token | Uso | Desktop | Mobile |
|---|---|---|---|
| `headline-display` | h1 del hero | 48px / 700 | 32px |
| `headline-lg` | h1 de página, h2 de sección | 32px / 700 | 26px |
| `headline-md` | h2/h3 de bloque | 24px / 600 | 20px |
| `title-md` | Nombre de producto y de artículo | 18px / 600 | 16px |
| `body-md` | Párrafos | 16px / 400 | 16px |
| `body-sm` | Textos secundarios, footer | 14px / 400 | 14px |
| `label-md` | Botones y navegación (MAYÚSCULAS en CTA) | 16px / 600 | 16px |
| `label-sm` | Etiquetas y chips | 12px / 600 | 12px |

Los botones principales van en mayúsculas: "VER CAMISETAS", "AGREGAR AL CARRITO", "FINALIZAR COMPRA". Máximo dos familias tipográficas en todo el sitio.

## Layout

- Ancho máximo de contenido: **1280px**, centrado. Márgenes laterales de 32px en desktop, 24px en tablet y 16px en mobile.
- Espaciado en múltiplos de 4px usando los tokens `spacing` (xs 4 → 3xl 64). Entre secciones: `3xl` (64px) en desktop y `2xl` (48px) en mobile.

| Dispositivo | Ancho | Columnas de productos | Navegación | Filtros |
|---|---|---|---|---|
| Mobile | hasta 767px | 2 columnas (card de 160px aprox.) | Menú hamburguesa, carrito siempre visible | Botón "Filtrar" que abre un panel inferior |
| Tablet | 768px a 1023px | 3 columnas | Menú hamburguesa + buscador visible | Panel lateral desplegable |
| Desktop | desde 1024px | 4 columnas | Navbar completa | Columna lateral fija a la izquierda (240px) |

- **Hero:** en desktop texto a la izquierda y foto a la derecha (o foto de fondo con degradado negro); en mobile la foto va arriba y el texto debajo, alto máximo 480px.
- **Ficha de producto:** en desktop galería a la izquierda (60 %) e información a la derecha (40 %); en mobile galería arriba y el botón "AGREGAR AL CARRITO" fijo al fondo de la pantalla.
- **Carrito:** en desktop lista a la izquierda y `order-summary` a la derecha; en mobile el resumen va debajo de la lista.
- **Blog:** grilla de 3 `card-article` en desktop, 2 en tablet y 1 en mobile. El artículo usa una columna de lectura de máximo 720px.
- Áreas táctiles de mínimo 44 × 44px en mobile.

## Elevation & Depth

La jerarquía se marca con capas de negro, no con sombras fuertes:

1. `neutral` (#0B0B0B) → fondo.
2. `surface` / `secondary` (#141414 / #171717) → cards y contenedores.
3. `surface-raised` (#1F1F1F) → hover y elementos elevados (panel de filtros, menú abierto).

- Cards: sombra `0 8px 24px rgba(0,0,0,0.30)`.
- Hover de cards: sombra `0 10px 30px rgba(198,161,91,0.10)` y borde de 1px dorado al 40 %.
- Bordes de separación de 1px en `outline` (#343434).
- La navbar queda fija al hacer scroll, con fondo `neutral` al 95 % de opacidad.

## Shapes

- Botones, chips, buscador y etiquetas: `rounded.full` (9999px), forma de píldora.
- Cards de producto, de artículo, inputs, selector de talla e ítems del carrito: `rounded.md` (8px).
- Cards de categoría, `order-summary`, newsletter y banners: `rounded.lg` (16px).
- Fotos de producto: proporción 4:5 (vertical), como una camiseta colgada.
- Sin bordes dorados de más de 1px.

## Components

### Announcement bar (`announcement-bar`)
Barra fina sobre la navbar, fondo dorado y texto negro en `label-sm`. Un solo mensaje a la vez: "ENVÍOS A TODO CHILE · 10 % OFF EN TU PRIMERA COMPRA".

### Navbar (`navbar`, `nav-link`)
Logo "FOR MAGOS" a la izquierda; al centro los enlaces Tienda, Clubes, Selecciones, Retro, Blog; a la derecha buscador (ícono), favoritos y carrito con contador.
- El ícono del carrito siempre es visible, también en mobile, y muestra el número de productos.
- `nav-link-active` (dorado) marca la sección actual; `nav-link-hover` cambia a dorado claro en 200ms.
- En mobile los enlaces van en un menú hamburguesa.

### Hero (`hero`)
Foto potente de una camiseta o de un hincha con degradado negro (de 80 % a 0 %) para que el texto sea legible. Contiene h1 en `headline-display`, una bajada en `body-md` y dos botones: `button-primary` "VER CAMISETAS" y `button-secondary` "LEER EL BLOG".
- El h1 tiene máximo 6 palabras.
- Solo un `button-primary` en el hero.

### Botones (`button-primary`, `button-secondary`)
- `button-primary`: acción principal (Ver camisetas, Agregar al carrito, Finalizar compra). Máximo uno por sección.
- `button-secondary`: fondo oscuro, texto dorado y borde de 1px dorado. Acciones secundarias (Leer el blog, Seguir comprando).
- Estados: hover (más claro, 200ms), active (más oscuro), disabled (gris `disabled`, cursor no permitido, texto "Agotado" cuando aplica).

### Buscador (`search-bar`)
Píldora con ícono de lupa y placeholder "Busca tu equipo o selección…". En la tienda va arriba de la grilla, a todo el ancho del contenido.

### Chips de categoría (`chip-filter`)
Fila horizontal: Todo, Clubes, Selecciones, Retro, Accesorios, Ofertas. Solo un chip activo a la vez (dorado). En mobile la fila se desplaza horizontalmente.

### Card de categoría (`card-category`)
Foto con overlay negro al 50 % y el nombre en mayúsculas (CLUBES, SELECCIONES, RETRO, ACCESORIOS). Hover: la foto crece al 103 % en 300ms. Toda la card es un enlace a la tienda filtrada.

### Product card (`card-product`, `price`, tags)
Foto 4:5, etiqueta opcional, nombre en `title-md`, equipo en `text-secondary`, precio en `price` y precio anterior tachado si hay oferta.
- El precio siempre es visible.
- El nombre ocupa máximo 2 líneas; si es más largo termina en "…".
- Máximo una etiqueta por card, arriba a la izquierda de la foto: `tag-offer` ("-20%"), `tag-new` ("NUEVO") o `tag-last-units` ("ÚLTIMAS UNIDADES", borde dorado de 1px).
- Agotado: foto en escala de grises al 60 % y texto "Agotado" en `error`.
- Hover (`card-product-hover`): la foto crece al 103 %, aparece un borde dorado suave y el texto "VER PRODUCTO".

### Selector de talla (`size-selector`)
Cuadros de 48px con S, M, L, XL, XXL. Uno seleccionado a la vez (`size-selector-active`, dorado). Las tallas sin stock usan `size-selector-disabled` con la letra tachada. Debajo, enlace "Guía de tallas".

### Indicador de stock (`tag-stock`)
Texto junto al precio: "En stock" en `success`, "Quedan 2 unidades" en `primary` o "Agotado" en `error`. Siempre visible en la ficha de producto.

### Inputs y formularios (`input-field`, `newsletter-form`, mensajes)
Inputs de 48px de alto con label visible arriba (no solo placeholder).
- Active/foco: fondo `surface-raised` y borde dorado de 1px.
- Error: borde y mensaje en `error` debajo del campo ("Ingresa un correo válido").
- El `newsletter-form` tiene título "Entérate primero de los nuevos ingresos", input de correo y `button-primary` "QUIERO MI 10 % OFF". Al enviar muestra `message-success`.

### Card de artículo (`card-article`)
Foto 16:9, categoría en `label-sm` dorado, título en `title-md` (máximo 3 líneas), fecha y tiempo de lectura en `text-secondary`. Hover: fondo `surface-raised`.

### Barra para compartir (`share-bar`) y comentarios (`comment-box`)
- `share-bar`: íconos de Instagram, WhatsApp, X y "Copiar enlace", arriba y al final del artículo.
- `comment-box`: lista de comentarios (nombre, fecha, texto) y formulario con nombre y comentario, más `button-primary` "PUBLICAR COMENTARIO".

### Carrito (`cart-item`, `order-summary`)
- `cart-item`: miniatura, nombre, talla, selector de cantidad (− 1 +), precio y "Eliminar".
- `order-summary`: subtotal, despacho (calculado por comuna), descuento y total en `price`, más `button-primary` "FINALIZAR COMPRA" y `button-secondary` "SEGUIR COMPRANDO".
- El total siempre es visible; en mobile el resumen queda fijo al fondo.

### Enlace de WhatsApp (`whatsapp-link`)
Texto "¿Dudas con tu talla? Escríbenos por WhatsApp" con ícono, en la ficha de producto y en el carrito.

### Footer (`footer`)
Fondo #080808. Logo FOR MAGOS y la frase "Donde el fútbol se convierte en magia."; columnas Tienda (Clubes, Selecciones, Retro, Accesorios), Ayuda (Preguntas frecuentes, Envíos y cambios, Contacto), Legal (Términos y condiciones, Política de privacidad); redes sociales e Instagram @for.magos; métodos de pago en gris.

### Lenguaje visual de fútbol
Se usa de forma sutil: líneas de cancha muy tenues, números de dorsal grandes de fondo al 5 % de opacidad, luces de estadio. Nunca balones repetidos como patrón ni estética infantil.

### Microinteracciones
Transiciones de 200ms a 300ms (hover de botones, zoom de fotos, cambio de color de enlaces). Sin animaciones exageradas.

## Do's and Don'ts

### Do

- Mantener el fondo predominantemente negro y las fotos de camisetas como protagonistas.
- Usar el dorado como acento: precios, CTA principal y detalles.
- Mostrar siempre precio, tallas y stock sin que Matías tenga que hacer clic.
- Usar fotos reales con el mismo fondo y la misma luz en todos los productos.
- Dejar espacio entre elementos (mínimo `spacing.lg` dentro de cards).
- Diseñar primero para mobile.
- Mantener contraste AA (4.5:1) en todo texto.

### Don't

- No usar grandes superficies doradas ni bordes dorados gruesos.
- No llenar el fondo con balones u otros elementos de fútbol.
- No usar más de dos tipografías.
- No usar colores saturados fuera de la paleta.
- No saturar las cards con información (máximo: foto, etiqueta, nombre, equipo, precio).
- No esconder el carrito ni el precio.
- No deformar las fotos ni modificar escudos o logos de los productos.
