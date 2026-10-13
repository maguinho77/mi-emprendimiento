# Color y tipografía — For Magos

> Guía: [Color y tipografía](../evaluacion/guias/fase-2-specs/05-color-y-tipografia.md)

## Paleta

| Rol | Color | HEX | Uso |
|---|---|---|---|
| Principal | Dorado suave | `#C6A15B` | Botón principal (`button-primary`), precios, chip activo, etiqueta de oferta y detalles de marca. Máximo 10 % de la pantalla. |
| Principal hover / active | Dorado claro / dorado profundo | `#D4B56F` / `#A8864A` | Solo estados hover y presionado de los elementos dorados. |
| Secundario | Gris negro | `#171717` | Fondo de las cards de producto, de categoría y del resumen del carrito. |
| Acento | Dorado oscuro | `#9C7F4C` | Íconos decorativos y enlace de WhatsApp. |
| Fondo | Negro carbón | `#0B0B0B` | Fondo de todas las páginas. |
| Superficie | Negro suave / negro elevado | `#141414` / `#1F1F1F` | Inputs, buscador, menús, cards de artículo; el elevado marca hover. |
| Texto | Blanco hueso | `#F5F5F5` | Títulos, nombres de producto, navegación y párrafos. |
| Texto secundario | Gris | `#A6A6A6` | Descripciones, categorías, fechas, footer. |
| Borde | Gris oscuro | `#343434` | Separadores y bordes de 1px. |
| Éxito | Verde | `#5FBF85` | "En stock", "Agregado al carrito", correo registrado. |
| Error | Rojo coral | `#E5645F` | Errores de formulario y "Agotado". |
| Deshabilitado | Gris carbón / gris | `#2A2A2A` / `#9A9A9A` | Botones y tallas no disponibles. |

## Contraste

Calculado con la fórmula de WCAG 2.1 y comprobado además con el validador oficial (`npx @google/design.md lint DESIGN.md`: 0 errores, 0 advertencias).

| Combinación | Ratio | Resultado |
|---|---|---|
| Texto `#F5F5F5` sobre fondo `#0B0B0B` | 18.05:1 | ✅ AAA |
| Texto secundario `#A6A6A6` sobre fondo `#0B0B0B` | 8.09:1 | ✅ AAA |
| Precio dorado `#C6A15B` sobre fondo `#0B0B0B` | 8.11:1 | ✅ AAA |
| Texto `#0B0B0B` sobre botón dorado `#C6A15B` | 8.11:1 | ✅ AAA |
| Nombre de producto `#F5F5F5` sobre card `#171717` | 16.44:1 | ✅ AAA |
| Precio `#C6A15B` sobre card `#171717` | 7.38:1 | ✅ AAA |
| "En stock" `#5FBF85` sobre card `#171717` | 7.92:1 | ✅ AAA |
| Error `#E5645F` sobre input `#141414` | 5.54:1 | ✅ AA |
| Botón deshabilitado `#9A9A9A` sobre `#2A2A2A` | 5.10:1 | ✅ AA |
| Footer `#A6A6A6` sobre `#080808` | 8.23:1 | ✅ AAA |

Ajustes hechos al validar: el gris de los botones deshabilitados pasó de `#8A8A8A` a `#9A9A9A` (tenía 4.16:1) y el acento de `#8E7445` a `#9C7F4C` (tenía 4.44:1).

## Tipografía

- **Títulos:** [Montserrat](https://fonts.google.com/specimen/Montserrat) (Bold 700 y SemiBold 600).
- **Textos:** [Inter](https://fonts.google.com/specimen/Inter) (Regular 400 y SemiBold 600 para botones y etiquetas).

| Elemento | Desktop | Mobile | Peso |
|---|---|---|---|
| h1 (hero) | 48px | 32px | Montserrat 700 |
| h1 de página / h2 | 32px | 26px | Montserrat 700 |
| h3 | 24px | 20px | Montserrat 600 |
| Nombre de producto | 18px | 16px | Montserrat 600 |
| Párrafo | 16px (interlineado 1.6) | 16px | Inter 400 |
| Botón | 16px, mayúsculas | 16px | Inter 600 |
| Etiqueta / chip | 12px, mayúsculas | 12px | Inter 600 |

## Justificación

El [moodboard](06-moodboard.md) define la sensación de **vitrina de colección en plena calle**. Por eso el fondo es negro carbón: hace que las camisetas (que traen sus propios colores de club) sean lo único que resalta, igual que en una vitrina iluminada. El dorado suave viene de los detalles del moodboard (escudos bordados, parches de campeón, trofeos) y se reserva para lo que Matías tiene que encontrar rápido: el precio y el botón para comprar. Así responde a dos de sus frustraciones: páginas desordenadas y no ver la información importante.

Montserrat se eligió para los títulos porque sus mayúsculas anchas y geométricas recuerdan los números y nombres estampados en las camisetas, y da el tono deportivo y urbano del moodboard. Inter acompaña porque es neutra y muy legible en celular, que es donde Matías compra. El verde y el rojo de estado se usan solo para stock y errores, para que nunca compitan con el dorado de la marca.
