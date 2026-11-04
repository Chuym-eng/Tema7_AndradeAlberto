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







