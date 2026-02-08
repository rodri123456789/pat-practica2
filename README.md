# API REST - Gestión de Carrito de Compra

Este proyecto implementa una API REST para gestionar un recurso simplificado de "Carrito de la compra" utilizando **Spring Boot**. La aplicación permite realizar operaciones CRUD completas (Crear, Leer, Actualizar y Borrar).



A continuación se detallan los endpoints disponibles para interactuar con el recurso `Carrito`.

| Método | Ruta | Descripción | Cuerpo de la Petición (JSON) | Posibles Respuestas |
| :--- | :--- | :--- | :--- | :--- |
| **GET** | `/api/carrito` | Obtiene el listado de todos los carritos. | *N/A* | `200 OK` (Lista JSON) |
| **GET** | `/api/carrito/{idCarrito}` | Obtiene el detalle de un carrito específico por su ID. | *N/A* | `200 OK` (Objeto JSON)<br>`404 Not Found` |
| **POST** | `/api/carrito` | Crea un nuevo registro de carrito. | Ver *Ejemplo JSON* abajo | `201 Created` / `200 OK`<br>`400 Bad Request` (Validación fallida) |
| **PUT** | `/api/carrito/{idCarrito}` | Actualiza los datos de un carrito existente. | Ver *Ejemplo JSON* abajo | `200 OK` (Actualizado)<br>`404 Not Found`<br>`400 Bad Request` |
| **DELETE** | `/api/carrito/{idCarrito}` | Elimina un carrito por su ID. | *N/A* | `204 No Content`<br>`404 Not Found` |

###  Ejemplo de Cuerpo (JSON)

Cuerpo válido para las peticiones `POST` y `PUT`.

```json
{
  "idArticulo": 101,
  "descripcion": "Zapatillas deportivas",
  "unidades": 2,
  "precioFinal": 59.99
}
