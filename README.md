# PymeManager-Sistema-de-Gesti-n-Empresarial

# 🏢 PymeManager — Sistema de Gestión Empresarial

## 📌 Propuesta de proyecto

La idea es desarrollar en equipo una aplicación web de **gestión empresarial para una pequeña o mediana empresa**, tomando como referencia las funcionalidades y problemáticas que suelen resolver los sistemas ERP.

El proyecto busca ser una aplicación **Full Stack funcional y realista**, que nos permita poner en práctica conocimientos de desarrollo web, bases de datos, APIs, autenticación, control de usuarios y procesos empresariales.

No buscamos desarrollar un ERP completo ni competir con sistemas como Tango. El objetivo es construir un proyecto de portfolio **bien terminado, documentado y técnicamente sólido**, que podamos mostrar en GitHub y utilizar como experiencia práctica en futuras entrevistas laborales.

---

## 🎯 Objetivos

* Desarrollar una aplicación Full Stack trabajando en equipo.
* Aplicar buenas prácticas de desarrollo.
* Diseñar y consumir una API REST.
* Trabajar con una base de datos.
* Implementar autenticación y autorización.
* Manejar distintos roles de usuario.
* Modelar procesos empresariales reales.
* Utilizar Git y GitHub para trabajar colaborativamente.
* Finalizar el proyecto con una documentación y presentación profesional.

---

## 🧩 Funcionalidades principales

### 👥 Usuarios y roles

El sistema contará con diferentes tipos de usuario, por ejemplo:

* Administrador
* Vendedor
* Encargado de stock

Cada rol tendrá distintos permisos dentro del sistema.

### 👤 Clientes

* Registrar clientes.
* Modificar y eliminar clientes.
* Consultar información.
* Ver historial de operaciones.

### 🏭 Proveedores

* Alta, baja y modificación.
* Información de contacto.
* Historial de compras.

### 📦 Productos

* Nombre y descripción.
* Categoría.
* Precio de venta.
* Costo.
* Stock disponible.
* Stock mínimo.
* Estado del producto.

### 📊 Inventario

El sistema deberá registrar los movimientos de stock producidos por:

* Compras.
* Ventas.
* Ajustes manuales.

Se podrá consultar el historial de movimientos y detectar productos con stock bajo.

### 🛒 Ventas

Permitir crear ventas asociadas a clientes, incluyendo:

* Productos.
* Cantidades.
* Precio.
* Total.
* Usuario que realizó la operación.
* Fecha.

La venta deberá actualizar automáticamente el stock.

### 🛍️ Compras

Permitir registrar compras a proveedores.

La recepción de una compra deberá actualizar el stock correspondiente.

### 📈 Dashboard

Un panel principal permitirá visualizar información general del negocio, por ejemplo:

* Ventas del período.
* Cantidad de ventas.
* Productos más vendidos.
* Productos con stock bajo.
* Compras realizadas.
* Evolución de ventas.

---

## 🔐 Seguridad

Se buscará implementar:

* Autenticación de usuarios.
* Contraseñas almacenadas de forma segura.
* Autorización mediante roles.
* Protección de rutas.
* Validación de datos.
* Manejo adecuado de errores.
* Variables de entorno para información sensible.

---

## 🛠️ Tecnologías propuestas

### Frontend

* React
* JavaScript / TypeScript
* HTML
* CSS

### Backend

* Node.js
* Express
* API REST

### Base de datos

* MongoDB

### Herramientas

* Git
* GitHub
* Postman / Insomnia
* Docker *(si el tiempo y los conocimientos lo permiten)*

La elección definitiva de tecnologías puede modificarse durante el desarrollo si encontramos una alternativa que tenga más sentido para alguna funcionalidad.

---

## 🏗️ Arquitectura general

La idea inicial es trabajar con una arquitectura separando frontend, backend y base de datos:

```text
┌─────────────────────┐
│      React          │
│      Frontend       │
└──────────┬──────────┘
           │
        HTTP/REST
           │
           ▼
┌─────────────────────┐
│   Node + Express    │
│       Backend       │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│      MongoDB        │
│      Database       │
└─────────────────────┘
```

---

## 📅 Plazo

El objetivo es tener una **versión funcional y presentable para noviembre de 2026**.

No buscamos implementar absolutamente todas las funcionalidades desde el primer momento. La prioridad será construir un **MVP sólido** y posteriormente agregar mejoras si el tiempo disponible lo permite.

### Prioridad

**Fase 1 — Base**

* Arquitectura.
* Base de datos.
* Backend.
* Frontend.
* Autenticación.

**Fase 2 — Gestión**

* Usuarios.
* Clientes.
* Proveedores.
* Productos.
* Inventario.

**Fase 3 — Procesos**

* Compras.
* Ventas.
* Actualización de stock.

**Fase 4 — Presentación**

* Dashboard.
* Validaciones.
* Corrección de errores.
* Diseño responsive.
* Documentación.
* Deploy/demo.

---

## 🤝 Propuesta de trabajo

La idea es hacerlo **entre los dos**, aprovechando que tenemos distintos niveles de experiencia.

No espero que una sola persona se encargue de todo ni que el proyecto interfiera con nuestras obligaciones de estudio o trabajo.

Podemos dividir las tareas según nuestras fortalezas y disponibilidad, revisar el código del otro y ayudarnos cuando aparezcan problemas.

También podemos utilizar el proyecto como una oportunidad para aprender cosas que todavía no dominamos.

La organización podría hacerse mediante:

* GitHub Issues.
* Branches por funcionalidad.
* Pull Requests.
* Code reviews.
* Reuniones breves cuando sea necesario.

La cantidad de trabajo y la distribución de tareas se definirían entre los dos antes de comenzar.

---

## 🚫 Alcance inicial

Para mantener el proyecto realizable dentro del plazo, inicialmente quedarían fuera:

* Facturación electrónica real.
* Integración con AFIP.
* Contabilidad completa.
* Integración con medios de pago reales.
* Microservicios.
* Funcionalidades de nivel empresarial avanzado.

Estas funcionalidades podrían considerarse en una futura versión si el proyecto llega a un estado estable antes de noviembre.

---

## 💡 ¿Por qué hacer este proyecto?

La intención es que no sea simplemente otro proyecto de práctica de React/Node.

Queremos construir algo que nos permita demostrar que podemos:

> **Analizar un problema → diseñar una solución → modelar los datos → desarrollar el backend → desarrollar el frontend → integrar todo → probarlo → documentarlo y ponerlo en funcionamiento.**

El resultado final debería ser un proyecto que podamos incluir en nuestro **portfolio y GitHub**, y que podamos explicar técnicamente durante una entrevista laboral.

---

## 🙋 Propuesta para trabajar juntos

Esta es una propuesta abierta. Sé que ambos tenemos estudio, trabajo y otras responsabilidades, por lo que entiendo perfectamente si no tenés disponibilidad para participar.

Si te interesa, podemos revisar juntos el alcance, modificar funcionalidades, dividir las tareas y ver si el proyecto es viable para los dos antes de empezar.

**La idea es que sea un proyecto compartido, no que uno termine cargando con todo el trabajo del otro.**
