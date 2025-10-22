# 🛒 Catálogo de Productos - JSON Limpio y Clasificado

Este repositorio contiene un conjunto de archivos **JSON** con datos de productos clasificados por categorías.  
Los datos fueron extraídos, depurados y organizados para facilitar su uso en sistemas de inventario, catálogos web o integraciones con APIs.

---

## 📁 Estructura del Proyecto

Cada archivo JSON representa una categoría específica.  
Todos los productos contienen los siguientes campos:

| Campo | Descripción |
|-------|--------------|
| `id` | Identificador único del producto |
| `nombre` | Nombre descriptivo del producto |
| `sku` | Código de referencia del producto |
| `precio` | Precio unitario del producto |
| `inventario` | Cantidad disponible |
| `tipoproducto` | Tipo de producto (1 = unidad, 2 = peso) |
| `preciooferta` | Precio en oferta (si aplica) |
| `imgprincipal` | URL de la imagen principal |
| `categoria_id` | ID numérico de la categoría |
| `categoria_nombre` | Nombre de la categoría |
| `multiplo` | Múltiplo de venta (por ejemplo, 0.2 = venta por peso) |
| `ventalocal` | Indica si se vende solo localmente (0 = no, 1 = sí) |

---

## 🗂️ Categorías Disponibles

| ID | Categoría | Archivo JSON |
|----|------------|--------------|
| 1 | Pollo | [`productos_pollo.json`](./productos_pollo.json) |
| 2 | Bebidas | [`productos_bebidas.json`](./productos_bebidas.json) |
| 3 | Res | [`productos_res.json`](./productos_res.json) |
| 4 | Cerdo | [`productos_cerdo.json`](./productos_cerdo.json) |
| 5 | Congelados | [`productos_congelados.json`](./productos_congelados.json) |
| 6 | Charcutería | [`productos_charcutería.json`](./productos_charcutería.json) |
| 7 | Snack | [`productos_snack.json`](./productos_snack.json) |
| 8 | Especias | [`productos_especias.json`](./productos_especias.json) |
| 9 | Hortalizas, frutas y verduras | [`productos_hortalizas_frutas_y_verduras.json`](./productos_hortalizas_frutas_y_verduras.json) |
| 10 | Hogar y bazar | [`productos_hogar_y_bazar.json`](./productos_hogar_y_bazar.json) |
| 11 | Licores | [`productos_licores.json`](./productos_licores.json) |
| 12 | Mascotas | [`productos_mascotas.json`](./productos_mascotas.json) |
| 13 | Panadería | [`productos_panadería.json`](./productos_panadería.json) |
| 14 | Despensa | [`productos_despensa.json`](./productos_despensa.json) |
| 15 | Productos personales | [`productos_productos_personales.json`](./productos_productos_personales.json) |
| 17 | Abarrotes | [`productos_abarrotes.json`](./productos_abarrotes.json) |

---

## ⚙️ Limpieza y Estructuración

El dataset fue procesado con las siguientes reglas:
- Se eliminaron los productos con **campos vacíos o nulos**.
- Se excluyó la categoría **16**.
- Se añadieron nombres descriptivos para cada categoría.
- Se ordenaron los productos por `categoria_id` y luego por `nombre`.
- Se eliminaron duplicados basados en el campo `id`.

---

## 🧩 Uso

Puedes cargar los archivos JSON en cualquier aplicación o entorno que soporte datos estructurados:

### Ejemplo en JavaScript
```js
import productos from './productos_bebidas.json';

console.log(productos[0].nombre);
