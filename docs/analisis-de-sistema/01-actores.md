# Actores del Sistema

## Ejercicio 02: Comprender el caso de negocio

### Contexto
La empresa se dedica a la **venta y distribución de alimento y otros artículos para mascotas**. Desea contar con un **marketplace** donde diferentes **sellers** puedan ofrecer productos para mascotas.

### Problema a resolver
Actualmente no existe una plataforma centralizada que permita:
- A los **clientes** encontrar y comprar productos para mascotas de distintos vendedores.
- A los **sellers** publicar y gestionar su catálogo de productos.
- A la **empresa** administrar y monitorear toda la operación del marketplace.

El sistema debe resolver la **integración** entre clientes, sellers, procesos de pago, envío, facturación y sistemas internos (ERP), ofreciendo una experiencia unificada.

---

## Ejercicio 03: Identificar actores

### Objetivo
Determinar **quiénes interactúan con el sistema** y **qué necesitan realizar**.

### Tabla de actores

| Actor | ¿Qué necesita realizar? |
|-------|-------------------------|
| **Cliente** | Buscar productos, consultar información, agregar productos al carrito, realizar pedidos, efectuar el pago y consultar sus pedidos. |
| **Seller** | Ofrecer productos, registrar productos, actualizar productos, consultar sus productos y gestionar la información relacionada con sus ventas. |
| **Administrador** | Administrar la plataforma. |
| **Pasarela de pago** | Procesar pagos. |
| **Servicio de envío** | Gestionar información de entrega. |
| **Servicio de Facturación** | Generar comprobantes de pago. |
| **ERP** | Proporcionar información de productos y stock. |

### Clasificación de actores

| Tipo | Actores |
|------|---------|
| **Usuarios humanos** | Cliente, Seller, Administrador |
| **Sistemas externos** | Pasarela de pago, Servicio de envío, Servicio de Facturación, ERP |

### Descripción breve por actor

- **Cliente:** Usuario final que navega el marketplace, compra productos y da seguimiento a sus pedidos.
- **Seller:** Vendedor que publica y mantiene actualizada su oferta de productos dentro de la plataforma.
- **Administrador:** Responsable de la operación, moderación y configuración general del marketplace.
- **Pasarela de pago:** Servicio externo que autoriza y procesa las transacciones económicas.
- **Servicio de envío:** Servicio externo que gestiona la logística y entrega de los pedidos.
- **Servicio de Facturación:** Servicio externo que emite comprobantes de pago (boletas/facturas).
- **ERP:** Sistema interno de la empresa que provee información de productos y stock.
