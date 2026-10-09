# Atributos de Calidad

## Ejercicio 06: Identificar atributos de calidad

### Objetivo
Determinar **cómo debe comportarse el sistema**, además de qué debe hacer.

### Escenario analizado
Durante una **campaña comercial**, el marketplace podría recibir una gran cantidad de usuarios consultando productos y realizando compras **simultáneamente**. ¿Qué atributos de calidad resultan importantes?

---

## Atributos de calidad identificados

| ID | Atributo de calidad | Escenario de calidad |
|----|---------------------|----------------------|
| AC01 | Rendimiento | Las consultas de productos y operaciones del carrito deben responder rápidamente incluso cuando exista una alta cantidad de usuarios concurrentes. |
| AC02 | Disponibilidad | El sistema debe permanecer disponible durante la campaña comercial y permitir que los usuarios realicen sus operaciones. |
| AC03 | Escalabilidad | El sistema debe poder soportar un incremento de usuarios y solicitudes sin afectar significativamente su funcionamiento. |
| AC04 | Seguridad | Los datos de los usuarios, cuentas y operaciones de compra deben estar protegidos frente a accesos no autorizados. |
| AC05 | Mantenibilidad | El sistema debe estar organizado de manera que permita realizar cambios y correcciones sin afectar innecesariamente otras funcionalidades. |

---

## Atributos de calidad complementarios (propuestos)

| ID | Atributo de calidad | Escenario de calidad |
|----|---------------------|----------------------|
| AC06 | Usabilidad | El cliente debe poder buscar y comprar un producto en pocos pasos, con una interfaz clara e intuitiva. |
| AC07 | Confiabilidad | Las transacciones de pago y generación de pedidos deben completarse sin errores ni duplicaciones, incluso ante fallos temporales. |
| AC08 | Interoperabilidad | El sistema debe integrarse correctamente con la pasarela de pago, el servicio de envío, el servicio de facturación y el ERP. |
| AC09 | Tolerancia a fallos | Ante la caída de un servicio externo (pago, envío o ERP), el sistema debe degradarse de forma controlada sin perder información. |
| AC10 | Observabilidad | El sistema debe permitir monitorear métricas, logs y trazas para detectar y diagnosticar problemas en producción. |
| AC11 | Escalabilidad del catálogo | El sistema debe soportar el crecimiento del número de productos y sellers sin degradar las búsquedas. |
| AC12 | Consistencia de datos | La información de stock, pedidos y pagos debe mantenerse consistente entre los distintos módulos y sistemas externos. |

---

## Clasificación por categoría

| Categoría | Atributos |
|-----------|-----------|
| **Operacionales** | AC01 Rendimiento, AC02 Disponibilidad, AC03 Escalabilidad, AC07 Confiabilidad, AC09 Tolerancia a fallos |
| **De desarrollo** | AC05 Mantenibilidad, AC10 Observabilidad |
| **De negocio / usuario** | AC04 Seguridad, AC06 Usabilidad, AC08 Interoperabilidad, AC11 Escalabilidad del catálogo, AC12 Consistencia de datos |
