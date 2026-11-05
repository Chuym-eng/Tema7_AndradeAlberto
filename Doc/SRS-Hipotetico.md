# SRS - Sistema Integrado de Ventas e Inventario para la tienda de ropa Oscar Montano (v1.1)
| ID | Requisito |
|---|---|
| REQ-001 | Inicio de sesión del usuario con bloqueo tras 3 intentos fallidos y control de acceso por rol. |
| REQ-002 | Registrar nuevos productos en el inventario |
| REQ-003 | Registrar clientes con nombres, apellidos, tipo de documento (DNI o RUC), número de documento y teléfono. Para clientes con RUC, registrar además la razón social | 
| REQ-004 | Permitir buscar prendas por nombre, código o categoría y mostrar su stock por talla y color, y su precio | 
| REQ-005 | Registrar ventas de una o más prendas, indicando la cantidad de cada una, el cliente, pago y fecha correspondiente |
| REQ-006 | Calcular automáticamente el total de la venta |
| REQ-007 | Descontar del stock, por talla y color, la cantidad vendida de cada prenda al confirmar la venta | 
| REQ-008 | Generar comprobante electrónico (boleta o factura) con serie, número correlativo, fecha, datos del cliente, detalle, monto y total, para ser validado por SUNAT mediante un OSE/PSE |
| REQ-009 | Generar reportes de ventas por rango de fechas |
| REQ-010 | Aplicar el 5% de descuento a clientes frecuentes |
| REQ-011 | Generar reportes de inventario con el stock actual por prenda, talla y color | 
| REQ-012 | Permitir consultar el historial de ventas por fecha, mostrar el estado de su comprobante electrónico por venta (Pendiente, Aceptado, Rechazado o Anulado) y permitir reenviar los comprobantes en estado Pendiente | 
| REQ-013 | Mostrar una alerta cuando el stock de un producto, por talla y color, sea menor a 10 unidades |
| REQ-014 | Registrar el pago de la venta indicando el método (Efectivo, Yape, Plin o tarjeta) y el monto|
| REQ-015 | El sistema debe enviar cada comprobante electrónico a SUNAT mediante un OSE/PSE y registrar su estado (Pendiente, Aceptado, Rechazado o Anulado), con el motivo cuando corresponda. | 
