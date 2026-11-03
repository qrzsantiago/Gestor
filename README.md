# Gestor · Finanzas e Inventario

Web App de una sola página (`index.html`) para iPhone (Safari → **Compartir → Agregar a pantalla de inicio**), ejecutada a pantalla completa.

- **Stack:** HTML + JavaScript puro, Tailwind CSS (CDN) y Lucide Icons (CDN).
- **Persistencia:** LocalStorage. Respaldo/restauración en JSON desde *Respaldo y Ajustes*.
- **Moneda:** Pesos Mexicanos (MXN), formato `$10,000.00`.
- **Sin datos precargados:** la app inicia vacía; todos los formularios inician en blanco.

## Secciones (menú ☰)
1. **Resumen:** tarjetas de crédito y cuentas hasta arriba; luego Balance total, Por cobrar (abre Clientes), **Por pagar volteable** (toca la tarjeta para alternar entre el *total acumulado* de deudas y tarjetas y lo que corresponde pagar *este mes*: pago del período de cada tarjeta más deudas vencidas o con fecha límite dentro del mes; la flecha abre Deudas) y Gastos del período; alertas, ventas del período e inventario activo.
2. **Gastos:** cada movimiento es **Ingreso** (verde, `+`) o **Gasto** (rojo, `−`); balance del período y **segmentos** de selección múltiple creados por el usuario.
3. **Tarjetas y Cuentas:** cada tarjeta se configura solo con límite, pago del período actual, día de corte y día límite de pago. Los gastos pagados con tarjeta se asignan solos: si su fecha es anterior o igual al corte del mes en curso se suman al pago del período actual; si es posterior, pasan al siguiente corte. Las **compras a meses** (p. ej. $6,000 a 6 meses) se dividen en mensualidades asignadas a cada corte, con calendario de pagos, saldo pendiente y avance por compra. Botones rápidos Pagar, Gasto y Compra a meses dentro de cada tarjeta. Historial de movimientos de cuentas y tarjetas.
4. **Ventas:** pestañas *Ventas* (historial), *Por cobrar* (ventas a cuotas y a crédito, con abonos) e *Inventario* (nombre/modelo y unidades). La cantidad de unidades solo aparece al vender un producto del inventario. Forma de pago: **Contado**, **Cuotas** (sin interés; plazo en **semanas o meses** y número de cuotas, con cálculo del monto por cuota, próxima cuota y aviso de atraso) o **Crédito** (con `%` de interés sobre saldo insoluto y día de corte).
5. **Clientes:** tres vistas — *Tarjetas* (saldo actual, deuda total e historial), *Mayor deuda* y *A – Z*.
6. **Deudas:** deudas propias + pago del período de tarjetas, con historial de pagos.

El botón ⚙ del encabezado abre **Respaldo y Ajustes** (exportar/importar JSON). Las semanas van de domingo a sábado. Si la fecha se deja vacía se usa la de hoy.

Cualquier registro puede editarse o eliminarse; todo se recalcula al momento. Los datos de versiones anteriores se migran automáticamente (las categorías pasan a ser segmentos). La versión instalada se ve en el menú ☰.
