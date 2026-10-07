version: alpha
name: "For Magos"
description: "Design system para tienda online de camisetas y accesorios de fútbol, con estética urbana, premium y deportiva."

colors:
primary: "#C6A15B"
primary-hover: "#D4B56F"
on-primary: "#0B0B0B"

secondary: "#171717"
on-secondary: "#FFFFFF"

tertiary: "#8E7445"
on-tertiary: "#FFFFFF"

neutral: "#0B0B0B"
surface: "#141414"
on-surface: "#F5F5F5"
on-surface-variant: "#A6A6A6"

disabled: "#343434"
on-disabled: "#777777"

error: "#D9534F"

typography:
headline-display:
fontFamily: "Montserrat"
fontSize: 48px
fontWeight: 700
lineHeight: 1.1

headline-lg:
fontFamily: "Montserrat"
fontSize: 32px
fontWeight: 700
lineHeight: 1.2

headline-md:
fontFamily: "Montserrat"
fontSize: 24px
fontWeight: 600
lineHeight: 1.25

body-md:
fontFamily: "Inter"
fontSize: 16px
fontWeight: 400
lineHeight: 1.6

label-md:
fontFamily: "Inter"
fontSize: 16px
fontWeight: 600
lineHeight: 1

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

button-primary:
backgroundColor: "{colors.primary}"
textColor: "{colors.on-primary}"
typography: "{typography.label-md}"
rounded: "{rounded.full}"
padding: 12px 24px

button-primary-hover:
backgroundColor: "{colors.primary-hover}"
textColor: "{colors.on-primary}"

button-primary-disabled:
backgroundColor: "{colors.disabled}"
textColor: "{colors.on-disabled}"

button-secondary:
backgroundColor: "{colors.surface}"
textColor: "{colors.primary}"
typography: "{typography.label-md}"
rounded: "{rounded.full}"
padding: 12px 24px
border: "1px solid #C6A15B"

card-product:
backgroundColor: "{colors.secondary}"
textColor: "{colors.on-secondary}"
rounded: "{rounded.md}"
padding: "{spacing.md}"
border: "1px solid #292929"

tag-offer:
backgroundColor: "{colors.primary}"
textColor: "{colors.on-primary}"
rounded: "{rounded.full}"
padding: "6px 12px"

tag-new:
backgroundColor: "#F5F5F5"
textColor: "#0B0B0B"
rounded: "{rounded.full}"
padding: "6px 12px"

input-field:
backgroundColor: "{colors.surface}"
textColor: "{colors.on-surface}"
typography: "{typography.body-md}"
rounded: "{rounded.md}"
padding: "12px 14px"
border: "1px solid #343434"

message-error:
backgroundColor: "{colors.surface}"
textColor: "{colors.error}"

page:
backgroundColor: "{colors.neutral}"
textColor: "{colors.on-surface}"

text-secondary:
backgroundColor: "{colors.neutral}"
textColor: "{colors.on-surface-variant}"

---

# For Magos – Design System

## Overview

For Magos es una tienda online especializada en camisetas de fútbol,
camisetas históricas, selecciones, clubes y accesorios relacionados
con la cultura futbolera.

La marca debe sentirse moderna, urbana, deportiva y premium.

La página debe transmitir la sensación de entrar a una tienda creada
por fanáticos del fútbol para fanáticos del fútbol.

La estética general debe ser oscura y elegante, utilizando negro carbón
como color dominante, blanco para mantener una lectura clara y dorado
suave como color de acento.

El dorado NO debe dominar la interfaz. Debe utilizarse estratégicamente
para destacar botones, precios, promociones, categorías y pequeños
detalles visuales.

El protagonista siempre debe ser el producto.

Palabras clave de la identidad visual:

- Fútbol
- Magia
- Pasión
- Historia
- Exclusividad
- Estilo urbano
- Premium
- Coleccionismo


## Colors

### Primary – Dorado suave (#C6A15B)

Se utiliza para:

- Botones principales.
- Precios destacados.
- Promociones.
- Links importantes.
- Indicadores activos.
- Pequeños detalles gráficos.
- Elementos relacionados con la identidad de For Magos.

NO utilizar grandes superficies completamente doradas.

El dorado debe funcionar como acento premium.


### Primary Hover – Dorado claro (#D4B56F)

Se utiliza exclusivamente para estados hover o interacción
sobre botones y enlaces dorados.


### Neutral – Negro carbón (#0B0B0B)

Color principal del fondo de la página.

Debe dominar visualmente el sitio y generar contraste
con las fotografías de las camisetas.


### Surface – Negro suave (#141414)

Utilizar para:

- Cards.
- Menús.
- Secciones secundarias.
- Buscador.
- Inputs.
- Contenedores.


### Secondary – Gris negro (#171717)

Utilizar principalmente en tarjetas de productos
y bloques que necesiten separarse del fondo.


### White – Blanco (#F5F5F5)

Utilizar para:

- Títulos.
- Nombre de productos.
- Navegación.
- Información importante.


### Text Secondary – Gris (#A6A6A6)

Utilizar para:

- Descripciones.
- Información secundaria.
- Categorías.
- Textos complementarios.


## Typography

La tipografía debe sentirse deportiva, limpia y moderna.

### Titles

Font family: Montserrat.

Usar Montserrat Bold o SemiBold.

Los títulos deben tener presencia y utilizar poco texto.

Headline Display:
48px / 700

Headline Large:
32px / 700

Headline Medium:
24px / 600


### Body

Font family: Inter.

Body:
16px / 400

Line height:
1.6


### Labels and Buttons

Inter SemiBold.

16px / 600.

Los botones pueden utilizar texto en mayúsculas cuando
se quiera generar mayor impacto visual.

Ejemplo:

VER CAMISETAS

COMPRAR AHORA

VER COLECCIÓN


## Layout

El sitio debe utilizar bastante espacio visual.

No saturar la pantalla con demasiados elementos.

Desktop:

- Máximo de contenido: 1440px.
- Márgenes laterales amplios.
- Grid de productos de 4 columnas.
- Hero horizontal.
- Navegación completa.

Tablet:

768px – 1023px.

- Grid de productos de 2 o 3 columnas.
- Reducir tamaño de títulos.
- Navegación simplificada.

Mobile:

Hasta 767px.

- Grid de productos de 2 columnas.
- Menú hamburguesa.
- Hero vertical o adaptado.
- Botones grandes y fáciles de presionar.
- Fotografías como elemento dominante.


## Homepage Structure

La página principal debe seguir aproximadamente este orden:

1. Announcement bar.
2. Header / navegación.
3. Hero principal.
4. Categorías destacadas.
5. Productos destacados.
6. Camisetas históricas.
7. Nuevos ingresos.
8. Banner promocional.
9. Beneficios de comprar en For Magos.
10. Instagram / comunidad.
11. Newsletter.
12. Footer.


## Announcement Bar

Barra fina ubicada en la parte superior.

Fondo:
#C6A15B

Texto:
#0B0B0B

Ejemplos de mensajes:

"ENVÍOS A TODO CHILE"

"VISTE TU PASIÓN ⚽"

"NUEVOS INGRESOS DISPONIBLES"


## Header

Fondo negro carbón.

Debe contener:

- Logo FOR MAGOS.
- Inicio.
- Camisetas.
- Selecciones.
- Clubes.
- Retro.
- Accesorios.
- Ofertas.
- Buscador.
- Cuenta.
- Carrito.

El header debe ser limpio y minimalista.

Cuando el usuario hace scroll puede permanecer fijo.


## Hero

El hero debe ser uno de los elementos visuales más importantes.

Utilizar una fotografía potente relacionada con camisetas
o cultura futbolera.

Debe existir un degradado negro sobre la fotografía para
mantener legibilidad.

Ejemplo de contenido:

FOR MAGOS

LA MAGIA SE LLEVA PUESTA.

Camisetas que representan historia, pasión y fútbol.

[VER CAMISETAS]

[EXPLORAR COLECCIÓN]

El CTA principal debe utilizar dorado suave.


## Categories

Crear categorías visuales grandes:

CLUBES

SELECCIONES

RETRO

ACCESORIOS

OFERTAS

Cada categoría debe utilizar fotografía y un overlay oscuro.

Al hacer hover la fotografía puede aumentar ligeramente
de escala.


## Product Cards

Las tarjetas deben ser minimalistas.

Cada tarjeta contiene:

- Fotografía del producto.
- Etiqueta opcional.
- Nombre.
- Equipo o selección.
- Precio.
- Precio anterior si existe oferta.
- Botón o acceso rápido al producto.

Ejemplo:

NUEVO

Camiseta Brasil 2026

Selección de Brasil

$39.990

VER PRODUCTO


La fotografía debe ocupar la mayor parte de la tarjeta.

No utilizar bordes dorados gruesos.

En hover:

- La imagen aumenta aproximadamente 3%.
- Aparece un pequeño brillo o borde dorado suave.
- Se puede mostrar "Ver producto".


## Product Page

La página de producto debe priorizar las fotografías.

Desktop:

Galería a la izquierda.

Información a la derecha.

Mostrar:

- Nombre del producto.
- Categoría.
- Precio.
- Precio anterior cuando corresponda.
- Selector de talla.
- Selector de cantidad.
- Botón "AGREGAR AL CARRITO".
- Descripción.
- Información de envío.
- Productos relacionados.

El botón principal debe ocupar todo el ancho disponible.


## Tags

Oferta:

Fondo dorado.
Texto negro.

NUEVO:

Fondo blanco.
Texto negro.

ÚLTIMAS UNIDADES:

Fondo oscuro.
Borde dorado.
Texto dorado.


## Football Visual Language

La temática de fútbol debe estar presente de manera sutil.

Se pueden utilizar:

- Líneas inspiradas en una cancha.
- Texturas muy suaves.
- Números grandes en fondos.
- Pequeños íconos de fútbol.
- Referencias visuales a estadios.
- Luces inspiradas en focos de estadio.
- Elementos gráficos relacionados con camisetas.

NO llenar la página de balones de fútbol.

La temática debe sentirse moderna, no infantil.


## Elevation & Depth

La jerarquía se genera principalmente mediante:

- Diferencias entre tonos negros.
- Bordes grises muy sutiles.
- Sombras suaves.
- Brillos dorados muy discretos.

Cards:

box-shadow:
0 8px 24px rgba(0,0,0,0.30)

Hover:

box-shadow:
0 10px 30px rgba(198,161,91,0.10)

No utilizar sombras excesivamente fuertes.


## Shapes

Botones:

Border radius completo:
9999px.

Cards:

8px.

Inputs:

8px.

Banners:

8px – 16px.

Las formas deben sentirse modernas y limpias.


## Components

### button-primary

Botón principal dorado.

Utilizar en:

- Comprar.
- Agregar al carrito.
- Ver colección.
- CTA principal.

No utilizar más de uno o dos botones primarios
en la misma sección.


### button-secondary

Fondo oscuro.

Borde dorado fino.

Texto dorado.

Utilizar para acciones secundarias.


### card-product

Debe destacar principalmente la fotografía.

Mantener suficiente espacio entre producto,
nombre y precio.


### tag-offer

Pequeño.

Dorado.

Ubicado sobre la fotografía del producto.


### Navbar

Debe ser simple y rápida de entender.

El logo debe tener espacio visual suficiente.

El carrito siempre debe ser fácilmente accesible.


### Footer

Fondo:
#080808

Debe contener:

FOR MAGOS

"Donde el fútbol se convierte en magia."

Links:

- Inicio
- Camisetas
- Retro
- Accesorios
- Contacto
- Preguntas frecuentes
- Cambios y devoluciones

Agregar redes sociales.

Agregar Instagram de For Magos.

Mostrar métodos de pago de forma discreta.


## Microinteractions

Los movimientos deben ser suaves.

Duración recomendada:

200ms – 300ms.

Ejemplos:

- Hover de botones.
- Zoom ligero de fotografías.
- Cambio de color en links.
- Aparición suave de cards.

No utilizar animaciones exageradas.


## Do's and Don'ts

### DO

- Mantener fondo predominantemente negro.
- Utilizar fotografías grandes.
- Mantener productos como protagonistas.
- Utilizar dorado de manera estratégica.
- Mantener mucho espacio entre elementos.
- Priorizar legibilidad.
- Mantener una estética premium y futbolera.
- Utilizar imágenes de camisetas de alta calidad.
- Mantener coherencia visual en todas las fotografías.
- Diseñar primero pensando en mobile.


### DON'T

- No utilizar dorado excesivamente.
- No llenar el fondo con elementos de fútbol.
- No utilizar demasiadas tipografías.
- No utilizar colores saturados que rompan la identidad.
- No agregar sombras exageradas.
- No saturar las tarjetas con información.
- No utilizar fondos diferentes para cada producto.
- No utilizar diseños infantiles.
- No deformar las fotografías de las camisetas.
- No modificar logos, escudos o detalles originales de los productos.


## Final Design Direction

