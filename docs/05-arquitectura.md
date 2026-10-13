# Arquitectura de la información — For Magos

## Mapa de sitio

```text
Inicio (landing)
├── Tienda
│   ├── Clubes
│   ├── Selecciones
│   ├── Camisetas retro
│   ├── Accesorios
│   └── Ofertas
│       └── Ficha de producto
│           └── Carrito
├── Blog
│   ├── Camisetas icónicas
│   ├── Guía de compra
│   └── Novedades y lanzamientos
│       └── Artículo
├── Contacto
├── Preguntas frecuentes (incluye guía de tallas, envíos y cambios)
├── Términos y condiciones
├── Política de privacidad
└── Página 404
```

La tienda y el blog están en el primer nivel del menú porque son las dos puertas de entrada de Matías: llega desde Instagram buscando una camiseta concreta (tienda) o atraído por una historia de una camiseta (blog).

## User flows

### Flujo 1: compra

Matías vio en Instagram la camiseta retro de Chile 1998 y quiere comprarla.

```text
Instagram → Landing → [Ver camisetas] → Tienda
→ Elige la categoría "Camisetas retro" (o escribe "Chile" en el buscador)
→ Filtra por talla M
→ ¿El producto tiene stock en su talla?
    ├── Sí → Ficha de producto → Revisa fotos, precio y guía de tallas
    │        → Selecciona talla M → [Agregar al carrito] → Carrito
    │        → Revisa total y costo de despacho → [Finalizar compra]
    └── No → Ficha de producto con talla "Agotada" → [Consultar por WhatsApp]
```

### Flujo 2: contenido

Matías entra al blog porque le interesa la historia detrás de las camisetas.

```text
Landing → [Leer el blog] → Blog
→ Elige la categoría "Camisetas icónicas"
→ Artículo "5 camisetas retro que todo coleccionista quiere"
→ Lee el artículo → [Compartir en Instagram/WhatsApp] (opcional)
→ Bloque "Productos del artículo" → [Ver producto] → Ficha de producto
→ Selecciona talla → [Agregar al carrito] → Carrito
```

## Categorías

### Categorías de productos

Las categorías se nombran como Matías busca: por el equipo que sigue, no por la temporada o el proveedor.

| Categoría | Productos |
|---|---|
| Clubes | Camiseta Colo-Colo local 2026, Camiseta Universidad de Chile local 2026, Camiseta Real Madrid local 2025/26, Camiseta Barcelona local 2025/26, Camiseta Boca Juniors local 2026 |
| Selecciones | Camiseta Chile local 2026, Camiseta Argentina local 2026, Camiseta Brasil local 2026, Camiseta Francia visita 2026 |
| Camisetas retro | Camiseta Chile 1998, Camiseta Colo-Colo 1991, Camiseta Argentina 1986, Camiseta Holanda 1988, Camiseta Brasil 2002 |
| Accesorios | Bufandas de clubes, jockeys de selecciones, parches y estampados de dorsal, fundas protectoras para colección |
| Ofertas | Camisetas de temporadas anteriores y últimas unidades con descuento |

### Categorías del blog

| Categoría | Idea de artículo | Necesidad o motivación de la proto-persona | Producto relacionado |
|---|---|---|---|
| Camisetas icónicas | "5 camisetas retro que todo coleccionista quiere" | Motivación: coleccionar camisetas especiales o históricas. | Camiseta Chile 1998 |
| Guía de compra | "Cómo elegir tu talla: fan, jugador y retro calzan distinto" | Frustración: no encontrar información sobre tallas antes de comprar. | Camiseta Chile local 2026 |
| Novedades y lanzamientos | "Las camisetas del Mundial 2026 que ya llegaron a For Magos" | Necesidad: encontrar camisetas actuales de sus selecciones favoritas. | Camiseta Argentina local 2026 |
