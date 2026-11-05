# Pruebas (v1.1) SIVI Oscar Montano

| ID | Requisito | Qué se prueba | Resultado esperado |
|---|---|---|---|
| PRU-001 | REQ-001 | Iniciar sesión con credenciales válidas y con 3 intentos fallidos | Redirección según el rol; al tercer intento fallido se bloquea el acceso |
| PRU-002 | REQ-002 | Registrar producto con datos válidos, con código repetido y con valores negativos | Producto registrado; en los otros dos casos se rechaza |
| PRU-003 | REQ-003 | Registrar cliente con datos válidos, con DNI repetido y con DNI de formato inválido | Cliente guardado; en los otros dos casos se rechaza |
| PRU-004 | REQ-004 | Buscar prenda por nombre, código o categoría | Muestra precio y stock por talla y color; sin coincidencias, mensaje de sin resultados |
| PRU-005 | REQ-005 | Registrar venta de varias prendas con cliente | Venta registrada con su pago; no permite cantidad mayor al stock ni venta sin cliente |
| PRU-006 | REQ-006 | Vender varias prendas con precios y cantidades distintos | Total igual a la suma de cantidad × precio unitario |
| PRU-007 | REQ-007 | Confirmar una venta | Stock de la talla y color vendidos disminuye; si el registro falla, no se descuenta |
| PRU-008 | REQ-008 | Confirmar una venta | Comprobante con número, fecha, detalle y total |
| PRU-009 | REQ-009 | Generar reporte de ventas por rango de fechas | Ventas del periodo con totales; con fechas inválidas o sin ventas, mensaje |
| PRU-010 | REQ-010 | Generar reporte de inventario con y sin filtros | Stock actual por prenda, talla y color |
| PRU-011 | REQ-011 | Consultar el historial por fecha y abrir una venta | Lista de ventas y su detalle; con fechas inválidas o sin ventas, mensaje |
| PRU-012 | REQ-012 | Vender hasta dejar una talla y color en 9 y en 10 unidades | Alerta con 9 unidades; sin alerta con 10 |
| PRU-013 | REQ-013 | Registrar el pago de una venta con cada método (Efectivo, Yape, Plin y Tarjeta) y con un monto distinto al total | Pago registrado con su método y monto, asociado a la venta; con un monto distinto al total o sin método, el sistema solicita corregirlo |
| PRU-014 | REQ-008, REQ-015 | Confirmar una venta con boleta a un cliente con DNI | Comprobante electrónico con serie, número correlativo, fecha, datos del cliente, detalle y total; estado Aceptado |
| PRU-015 | REQ-008, REQ-003 | Confirmar una venta con factura a un cliente con RUC válido | Factura emitida con RUC y razón social del cliente; estado Aceptado |
| PRU-016 | REQ-003 | Registrar cliente con RUC de 11 dígitos válido, con RUC repetido y con RUC de formato inválido | Cliente guardado; en los otros dos casos se rechaza antes de enviar nada al proveedor |
| PRU-017 | REQ-015 | Confirmar una venta con el servicio de facturación caído o sin respuesta | La venta se completa y el stock se descuenta; el comprobante queda Pendiente y se avisa al cajero |
| PRU-018 | REQ-015 | Restablecer el servicio con comprobantes Pendientes en cola | El sistema los reenvía automáticamente y su estado pasa a Aceptado; no se duplica ninguno |
| PRU-019 | REQ-015 | Enviar un comprobante que SUNAT rechaza | Estado Rechazado con el motivo visible; la venta se conserva |
| PRU-020 | REQ-015 | Anular un comprobante Aceptado y probar anular uno Pendiente o Rechazado | El Aceptado pasa a Anulado; en los otros dos casos el sistema no permite la anulación |
| PRU-021 | REQ-008 | Elegir factura para un cliente sin RUC | El sistema no permite emitirla y solicita registrar el RUC |
| PRU-022 | REQ-006, REQ-008 | Confirmar ventas de varias prendas con precios y cantidades distintos y comparar con el comprobante | El total del comprobante es igual al total de la venta |
| PRU-023 | REQ-012 | Consultar el historial por fecha con comprobantes en cada estado y reenviar uno Pendiente | Cada venta muestra el estado de su comprobante; el reenvío actualiza el estado; con fechas inválidas o sin ventas, mensaje |
| PRU-024 | RNF-DIS-001, RNF-REN-002 | Registrar 10 ventas consecutivas con el servicio operativo | Todas se completan y el resultado de la emisión se muestra en ≤ 5 s en el 95 % de los casos |
| PRU-025 | RNF-DIS-001, RNF-REN-002 | Registrar 50 ventas consecutivas con el servicio operativo | Mismo resultado que PRU-024, sin ventas perdidas ni comprobantes duplicados |
| PRU-026 | RNF-DIS-001, RNF-REN-002 | Registrar 100 ventas consecutivas, con el servicio caído en una parte de ellas | El 100 % de las ventas se completa; los comprobantes sin respuesta quedan Pendientes y se reenvían al restablecerse |






