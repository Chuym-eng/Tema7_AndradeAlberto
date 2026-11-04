### Análisis de impacto

| Dimensión | Análisis | Mitigación |
|---|---|---|
| Alcance | Modificación de REQ-005 y creación de REQ-013, CLS-008 (Pago, con MetodoPago) y PRU-013. Impacta CU-004 (ingreso de datos de pago), el diagrama de clases (relación Venta 1 — 1 Pago) y la matriz de trazabilidad | Limitar el cambio al registro del método (Efectivo, Yape, Plin o Tarjeta) y del monto, sin integración con servicios externos de pago. Actualizar en el mismo cambio todos los artefactos afectados |
| Tiempo | Actualización de requisitos, incorporación y ajuste de clases, desarrollo de nuevas pruebas | Realizar los ajustes en orden: SRS, casos de uso, diagrama de clases, pruebas y matriz de trazabilidad, para evitar retrabajo |
| Calidad | Riesgo de inconsistencia entre artefactos y de regresión en el proceso de venta (total, stock y comprobante). Riesgo de pagos con monto incorrecto | Ejecutar nuevamente las pruebas de venta (PRU-005 a PRU-008) y la nueva PRU-013, validando que el monto coincida con el total y que cada método quede registrado |

**Decisión:** Aprobado

**Motivo de la decisión:** El cambio es de prioridad alta y completa el proceso de venta, que hoy no registra cómo se paga. Su alcance es acotado, porque solo agrega una clase, un requisito y una prueba, y modifica un caso de uso. No requiere integraciones externas, por lo que su riesgo para la línea base es bajo.
