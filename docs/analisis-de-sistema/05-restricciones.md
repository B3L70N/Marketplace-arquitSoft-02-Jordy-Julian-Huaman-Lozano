# Restricciones

## Ejercicio 07: Identificar restricciones

### Objetivo
Identificar las **restricciones** que condicionan las decisiones de diseño y arquitectura del sistema.

---

## Restricciones identificadas

| ID | Restricción | Descripción |
|----|-------------|-------------|
| RC01 | Aplicación web | El sistema debe desarrollarse como una aplicación accesible mediante un navegador web. |
| RC02 | Control de versiones | El código fuente debe gestionarse utilizando Git y mantenerse en un repositorio compartido. |
| RC03 | API REST | La comunicación entre el frontend y los servicios del sistema debe realizarse mediante una API REST. |
| RC04 | Pasarela de pago | El sistema debe integrarse con una pasarela de pago externa para procesar las operaciones de pago. |
| RC05 | Servicio de envío | El sistema debe integrarse con un servicio externo de envío para gestionar la información relacionada con la entrega de pedidos. |

---

## Restricciones complementarias (propuestas)

| ID | Restricción | Descripción |
|----|-------------|-------------|
| RC06 | Servicio de facturación | El sistema debe integrarse con un servicio externo de facturación para generar comprobantes de pago (boletas/facturas). |
| RC07 | ERP corporativo | El sistema debe consumir información de productos y stock desde el ERP de la empresa. |
| RC08 | Presupuesto | El proyecto debe desarrollarse con un presupuesto limitado para infraestructura y servicios cloud. |
| RC09 | Plazo de entrega | El MVP del marketplace debe estar operativo en un plazo máximo definido por el curso (por ejemplo, 3 meses). |
| RC10 | Tecnologías permitidas | El desarrollo debe realizarse con tecnologías web estándar (HTML5, JavaScript, REST, base de datos relacional). |
| RC11 | Cumplimiento legal | El sistema debe cumplir con la normativa de protección de datos personales vigente. |
| RC12 | Seguridad en pagos | El sistema debe cumplir con estándares de seguridad aplicables a transacciones con tarjeta (por ejemplo, PCI-DSS). |
| RC13 | Idioma y moneda | La interfaz y los precios deben presentarse en español y en la moneda local (PEN). |
| RC14 | Compatibilidad | El sistema debe funcionar correctamente en los navegadores más usados (Chrome, Firefox, Edge). |
| RC15 | Escalabilidad en la nube | La solución debe poder desplegarse en un proveedor cloud que permita escalado horizontal. |

---

## Clasificación de restricciones

| Tipo | Restricciones |
|------|---------------|
| **Técnicas** | RC01, RC03, RC07, RC10, RC14, RC15 |
| **De integración** | RC04, RC05, RC06, RC07 |
| **De gestión del proyecto** | RC02, RC08, RC09 |
| **Legales / normativas** | RC11, RC12 |
| **De negocio / usuario** | RC13 |
