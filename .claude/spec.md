# Especificaciones — PymeManager

## Stack técnico

| Capa | Tecnología |
|------|------------|
| Frontend | React + TypeScript + TailwindCSS |
| Backend | NestJS (API REST) |
| ORM | Prisma |
| Base de datos | PostgreSQL |
| Autenticación | JWT almacenado en cookies |

Arquitectura: React → (HTTP/REST) → NestJS → Prisma → PostgreSQL.

## Autenticación y autorización

- Login con credenciales; el backend emite un JWT y lo guarda en una cookie.
- Las rutas protegidas del backend validan el JWT de la cookie.
- Contraseñas almacenadas hasheadas, nunca en texto plano.
- Autorización por roles: Administrador, Vendedor, Encargado de stock.
- Rutas del frontend protegidas según sesión y rol.
- Datos sensibles (secretos JWT, credenciales de la DB) en variables de entorno.

## Requerimientos funcionales

### Usuarios y roles
- Cada usuario tiene un rol que define sus permisos.

### Clientes
- Alta, modificación y eliminación.
- Consulta de información e historial de operaciones.

### Proveedores
- Alta, baja y modificación.
- Información de contacto e historial de compras.

### Productos
- Campos: nombre, descripción, categoría, precio de venta, costo, stock disponible, stock mínimo, estado.

### Inventario
- Registro de movimientos de stock originados por compras, ventas y ajustes manuales.
- Consulta del historial de movimientos.
- Detección de productos con stock bajo (stock disponible por debajo del mínimo).

### Ventas
- Una venta se asocia a un cliente e incluye productos, cantidades, precio, total, usuario que la realizó y fecha.
- Al registrarse, descuenta el stock automáticamente.

### Compras
- Registro de compras a proveedores.
- La recepción de una compra aumenta el stock correspondiente.

### Dashboard
- Ventas del período y cantidad de ventas.
- Productos más vendidos.
- Productos con stock bajo.
- Compras realizadas.
- Evolución de ventas.

## Requerimientos no funcionales

- Validación de datos en el backend.
- Manejo adecuado de errores.
- Diseño responsive.
- Íconos con Bootstrap Icons (ver `rules.md`).

## Criterios de aceptación generales

- Cada operación de venta, compra o ajuste deja un movimiento de inventario registrado.
- Un usuario sin el rol adecuado no puede acceder a las rutas o acciones restringidas.
- Los endpoints protegidos rechazan peticiones sin JWT válido.

## Fuera de alcance

Facturación electrónica real, integración con AFIP, contabilidad completa, medios de pago reales, microservicios y funcionalidades empresariales avanzadas.

## Pendientes por definir

Estos puntos no están definidos todavía; hay que decidirlos antes de implementar:

- Matriz de permisos por rol (qué puede hacer cada uno).
- Modelo de datos (entidades y relaciones en Prisma).
- Estados de venta y de compra (por ejemplo pendiente, recibida, anulada).
- Estructura de carpetas de frontend y backend.
- Librerías de UI, estado y ruteo del frontend.
