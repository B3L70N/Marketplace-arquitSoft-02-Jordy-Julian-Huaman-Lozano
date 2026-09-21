# Drivers Arquitectónicos

## Ejercicio 08: Identificar drivers arquitectónicos

### Objetivo
Integrar los elementos identificados anteriormente y determinar cuáles tienen una **influencia significativa** en las decisiones de arquitectura.

---

## Drivers arquitectónicos identificados

| ID | Driver arquitectónico | Origen | ¿Por qué influye en la arquitectura? |
|----|-----------------------|--------|--------------------------------------|
| DA01 | El sistema debe soportar un incremento importante de usuarios durante campañas comerciales. | AC03 – Escalabilidad | Puede influir en la estrategia de escalamiento y despliegue. |
| DA02 | El sistema debe mantener tiempos de respuesta adecuados durante una alta concurrencia. | AC01 – Rendimiento | Puede influir en la comunicación entre componentes, procesamiento y almacenamiento. |
| DA03 | El sistema debe proteger los datos de usuarios y operaciones de compra. | AC04 – Seguridad | Puede influir en autenticación, autorización y protección de datos. |
| DA04 | El sistema debe integrarse con una pasarela de pago externa mediante una API. | RC04 – Pasarela de pago | Condiciona la forma de comunicación e integración con servicios externos. |
| DA05 | El sistema debe utilizar una API REST para la comunicación entre frontend y backend. | RC03 – API REST | Limita las alternativas de comunicación entre las partes del sistema. |

---

## Drivers arquitectónicos complementarios (propuestos)

| ID | Driver arquitectónico | Origen | ¿Por qué influye en la arquitectura? |
|----|-----------------------|--------|--------------------------------------|
| DA06 | El sistema debe permanecer disponible durante la campaña comercial. | AC02 – Disponibilidad | Impulsa el uso de redundancia, balanceo de carga y tolerancia a fallos. |
| DA07 | El sistema debe poder mantener y evolucionar sus funcionalidades sin afectar otras. | AC05 – Mantenibilidad | Favorece una arquitectura modular y por capas con bajo acoplamiento. |
| DA08 | El sistema debe integrarse con el servicio de envío, el servicio de facturación y el ERP. | RC05, RC06, RC07 | Obliga a diseñar adaptadores e interfaces para múltiples sistemas externos. |
| DA09 | El sistema debe mantener la consistencia de datos entre pedidos, stock y pagos. | AC12 – Consistencia de datos | Influye en la gestión transaccional y en la comunicación entre módulos. |
| DA10 | El sistema debe degradarse de forma controlada ante fallos de servicios externos. | AC09 – Tolerancia a fallos | Impulsa patrones como circuit breaker, retry y colas de mensajes. |
| DA11 | El sistema debe permitir monitorear su comportamiento en producción. | AC10 – Observabilidad | Requiere logging, métricas y trazas distribuidas desde el diseño. |

---

## Clasificación de drivers

| Categoría | Drivers |
|-----------|---------|
| **Atributos de calidad** | DA01, DA02, DA03, DA06, DA07, DA09, DA10, DA11 |
| **Restricciones** | DA04, DA05, DA08 |

---

## Influencia de los drivers en la arquitectura

- **Escalabilidad (DA01) y Rendimiento (DA02):** impulsan el uso de caché, balanceo de carga, componentes desacoplados y escalado horizontal.
- **Seguridad (DA03):** exige autenticación centralizada, autorización por roles y cifrado de datos sensibles.
- **Integración con sistemas externos (DA04, DA08):** obliga a diseñar adaptadores y contratos bien definidos con pasarela de pago, envío, facturación y ERP.
- **API REST (DA05):** define el estilo de comunicación principal y las interfaces entre frontend y backend.
- **Disponibilidad (DA06) y Tolerancia a fallos (DA10):** requieren redundancia, monitoreo y mecanismos de recuperación.
- **Mantenibilidad (DA07) y Observabilidad (DA11):** favorecen una arquitectura modular, con separación de responsabilidades y visibilidad operativa.
- **Consistencia de datos (DA09):** influye en el manejo de transacciones y la coordinación entre módulos.
