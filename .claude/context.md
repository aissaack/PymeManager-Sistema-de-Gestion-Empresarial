# Contexto general — PymeManager

## De qué trata

PymeManager es una aplicación web Full Stack de **gestión empresarial para pequeñas y medianas empresas (pymes)**, inspirada en las funcionalidades típicas de un ERP. Centraliza en un solo lugar la operación diaria del negocio:

- Usuarios y roles (Administrador, roles por modulo).
- Clientes y proveedores.
- Productos e inventario (con stock mínimo y movimientos).
- Ventas y compras, que actualizan el stock automáticamente.
- Dashboard con métricas del negocio (ventas del período, productos más vendidos, stock bajo, evolución de ventas).

## Qué problema resuelve

Una pyme suele manejar clientes, proveedores, stock, ventas y compras de forma dispersa (planillas, papel, memoria), lo que genera:

- Stock desactualizado y quiebres o sobrestock sin detectar.
- Falta de historial de operaciones por cliente o proveedor.
- Nula trazabilidad de quién hizo cada operación.
- Poca visibilidad del estado general del negocio.

PymeManager unifica esa información, registra cada movimiento con su usuario y fecha, y limita qué puede hacer cada persona según su rol.

## Propósito

Es un **proyecto de portfolio** desarrollado en equipo (dos personas), no un producto comercial. Los objetivos son:

- Construir una app Full Stack funcional y realista, bien terminada, documentada y técnicamente sólida.
- Practicar API REST, base de datos, autenticación/autorización, roles, validaciones y modelado de procesos empresariales.
- Trabajar colaborativamente con Git/GitHub (issues, branches por funcionalidad, pull requests, code reviews).
- Poder mostrarlo en GitHub y explicarlo técnicamente en entrevistas laborales.

No busca competir con sistemas como Tango.

## Stack propuesto

- **Frontend:** React (JavaScript/TypeScript), HTML, CSS.
- **Backend:** Node.js + Express, API REST.
- **Base de datos:** MongoDB.
- **Herramientas:** Git, GitHub, Postman/Insomnia, Docker (opcional).

Arquitectura en tres capas: React → (HTTP/REST) → NestJS → PrismaORM → PostgreSQL. El stack puede cambiar durante el desarrollo si hay una alternativa mejor para alguna funcionalidad.

## Seguridad

Autenticación, contraseñas almacenadas de forma segura, autorización por roles, protección de rutas, validación de datos, manejo adecuado de errores y variables de entorno para datos sensibles.

## Plazo y fases

Versión funcional y presentable para **noviembre de 2026**. Prioridad: un MVP sólido y luego mejoras.

1. **Base:** arquitectura, base de datos, backend, frontend, autenticación.
2. **Gestión:** usuarios, clientes, proveedores, productos, inventario.
3. **Procesos:** compras, ventas, actualización de stock.
4. **Presentación:** dashboard, validaciones, corrección de errores, responsive, documentación, deploy/demo.

## Fuera de alcance (inicialmente)

Facturación electrónica real, integración con AFIP, contabilidad completa, medios de pago reales, microservicios y funcionalidades empresariales avanzadas.
