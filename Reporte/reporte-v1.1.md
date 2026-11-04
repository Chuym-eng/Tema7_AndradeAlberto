# Reporte de trazabilidad v1.1

| Métrica | Valor |
|---|---|
| Requisitos totales | 13 |
| Requisitos con prueba | 13 |
| Cobertura | 100 % |
| Requisitos modificados por CR-001 | REQ-005, REQ-013 |
| Artefactos modificados | SRS, CU-004, CLS-008, PRU-005, PRU-013 |

## Cambios frente a v1.0

- Se agregó REQ-013: registrar el pago de la venta con su método (Efectivo, Yape, Plin o Tarjeta) y el monto.
- REQ-005 pasó de "registrar ventas indicando la cantidad de cada prenda y el cliente" a incluir también el pago correspondiente (REQ-013).
- CU-004 incorpora el registro y la validación del pago (pasos 7 a 9) y ajusta sus excepciones 4 y 5.
- Se agregó la clase Pago (CLS-008) con 2 métodos (registrarPago, validarMonto) y la relación Venta 1 — 1 Pago.
- Se agregó 1 prueba (PRU-013) y se ajustó otra (PRU-005).
- Se vuelven a ejecutar PRU-005 a PRU-008 por regresión del proceso de venta.
