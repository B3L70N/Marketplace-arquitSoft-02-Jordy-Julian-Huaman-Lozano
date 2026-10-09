# Decisiones Arquitectónicas (ADR)

## Objetivo

Documentar las decisiones arquitectónicas importantes tomadas durante el diseño de la arquitectura del software, junto con su justificación y los drivers que las motivan.

ADR significa Architecture Decision Record (Registro de Decisión Arquitectónica).

---

## Listado de decisiones arquitectónicas

| ID | Decisión arquitectónica | Driver relacionado | Justificación | Resultado |
|----|-------------------------|--------------------|---------------|-----------|
| ADR001 | Monolito modular | DA01 Escalabilidad, DA06 Mantenibilidad | Organizar las funcionalidades en módulos independientes dentro de una misma aplicación desplegable. | Módulos de Catálogo, Carrito, Pedidos, Pagos y Usuarios. |
| ADR002 | Clean Architecture | DA06 Mantenibilidad | Separar las reglas del negocio de los detalles tecnológicos. | Dominio, Aplicación, Infraestructura y Presentación. |
| ADR003 | Estrategia de caché | DA02 Rendimiento | Reducir consultas repetitivas a la fuente de datos. | Caché para información de consulta frecuente. |
| ADR004 | Integración de pagos mediante interfaces y adaptadores | DA04 Integración con pagos | Desacoplar los casos de uso del proveedor de pagos. | Contrato de pagos y adaptador para la pasarela externa. |

---

## Relación con los drivers arquitectónicos

| ADR | Driver | Tipo de driver |
|-----|--------|----------------|
| ADR001 | DA01, DA06 | Escalabilidad, Mantenibilidad |
| ADR002 | DA06 | Mantenibilidad |
| ADR003 | DA02 | Rendimiento |
| ADR004 | DA04 | Integración con pagos |

---

## Descripción de cada decisión

### ADR001 - Monolito modular

**Decisión.** Organizar el sistema como un monolito modular, donde cada funcionalidad principal vive en su propio módulo dentro de una misma aplicación desplegable.

**Justificación.** Se elige esta opción en lugar de microservicios porque el proyecto tiene alcance académico y no requiere la complejidad operativa de un sistema distribuido. Al mismo tiempo, la separación en módulos permite mantener la mantenibilidad (DA06) y facilita una futura escalabilidad horizontal (DA01).

**Resultado.** Módulos de Catálogo, Carrito, Pedidos, Pagos y Usuarios.

---

### ADR002 - Clean Architecture

**Decisión.** Aplicar los principios de Clean Architecture, separando las reglas del negocio de los detalles tecnológicos.

**Justificación.** La mantenibilidad (DA06) exige que los cambios en la infraestructura (base de datos, servicios externos, frameworks) no obliguen a modificar las reglas del negocio. Separar las capas permite sustituir detalles técnicos sin afectar el dominio.

**Resultado.** Capas de Dominio, Aplicación, Infraestructura y Presentación.

---

### ADR003 - Estrategia de caché

**Decisión.** Incorporar una estrategia de caché para la información de consulta frecuente.

**Justificación.** El rendimiento (DA02) se ve afectado cuando hay alta concurrencia. Las consultas repetitivas a la base de datos se pueden resolver desde caché, reduciendo la carga y mejorando los tiempos de respuesta.

**Resultado.** Caché para información de consulta frecuente (catálogo de productos, categorías, datos de sesión).

---

### ADR004 - Integración de pagos mediante interfaces y adaptadores

**Decisión.** Integrar la pasarela de pagos mediante un contrato de interfaz y un adaptador específico para cada proveedor.

**Justificación.** El driver DA04 obliga a comunicarse con una pasarela externa. Acoplar directamente los casos de uso al SDK del proveedor dificultaría cambiar de pasarela o simularla en pruebas. Un contrato bien definido permite sustituir el adaptador sin afectar la lógica de negocio.

**Resultado.** Contrato de pagos y adaptador para la pasarela externa.