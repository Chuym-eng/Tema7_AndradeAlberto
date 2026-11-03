# Matriz de trazabilidad SIVI Oscar Montano (V1.0)
| Req | Descripción | CU | Clase | Prueba | ¿Cubierto? |
|---|---|---|---|---|---|
| REQ-001 | Inicio de sesión con bloqueo tras 3 intentos fallidos y control de acceso por rol | CU-001 | CLS-Administrador, CLS-Cajero, CLS-Encargado del almacen| PRU-001 | Si |
| REQ-002 | Registrar productos | CU-002 | CLS-Productos | PRU-002 | Si |
| REQ-003 | Registrar clientes con nombres, apellidos, DNI (formato fijo) y teléfono | CU-006 | CLS-Cliente | PRU-003 | Si |
| REQ-004 | Consultar prendas | CU-003 | CLS-Producto | PRU-004 | Pendiente |
| REQ-005 | Registrar ventas | CU-004 | CLS-Venta, CLS-DetalleVenta, CLS-Cliente, CLS-Cajero | PRU-005 | Si |
| REQ-006 | Calcular el total | CU-004 | CLS-Venta, CLS-DetalleVenta | PRU-006 | Si |
| REQ-007 | Descontar stock | CU-004 | CLS-Producto, CLS-DetalleVenta | PRU-007 | Si |
| REQ-008 | Generar comprobante interno de venta | CU-004 | CLS-Comprobante, CLS-Venta | PRU-008 | Si |
| REQ-009 | Generar reportes de ventas por rango de fechas | CU-005 | CLS-Reporte, CLS-Venta, CLS-Administrador | PRU-009 | Si |
| REQ-010 | Generar reportes de inventario por prenda, talla y color | CU-007 | CLS-Reporte, CLS-Producto | PRU-010 | Si |
| REQ-011 | Consultar historial de ventas por fecha | CU-008 | CLS-Venta, CLS-DetalleVenta, CLS-Comprobante, CLS-Cliente | PRU-011 | Si |
| REQ-012 | Alerta cuando el stock de un producto, por talla y color, sea menor a 10 unidades | CU-004, CU-003, CU-009 | CLS-Producto | PRU-012 | Si |


**Cobertura**

- Trazabilidad requisito → caso de uso → clase: 13 de 13(100 %)
