# Gestor · Finanzas e Inventario

Web App de una sola página (`index.html`) para iPhone (Safari → **Compartir → Agregar a pantalla de inicio**), ejecutada a pantalla completa.

- **Stack:** HTML + JavaScript puro, Tailwind CSS (CDN) y Lucide Icons (CDN).
- **Persistencia:** LocalStorage. Respaldo/restauración en JSON desde *Respaldo y Ajustes*.
- **Moneda:** Pesos Mexicanos (MXN), formato `$10,000.00`.
- **Sin datos precargados:** la app inicia vacía; todos los formularios inician en blanco.

## Secciones (menú ☰)
1. **Resumen:** tarjetas de crédito y cuentas hasta arriba; luego Balance total, Por cobrar (abre Clientes), **Por pagar volteable** (toca la tarjeta para alternar entre el *total acumulado* de deudas y tarjetas y lo que corresponde pagar *este mes*: pago del período de cada tarjeta más deudas vencidas o con fecha límite dentro del mes; la flecha abre Deudas) y Gastos del período; alertas, ventas del período e inventario activo.
2. **Gastos:** cada movimiento es **Ingreso** (verde, `+`) o **Gasto** (rojo, `−`); balance del período y **segmentos** de selección múltiple creados por el usuario.
3. **Tarjetas y Cuentas:** el *pago del período* va separado de MSI, saldos diferidos y compras posteriores al corte; historial de movimientos de cuentas y tarjetas.
4. **Ventas:** pestañas *Ventas* (historial), *Por cobrar* (cuotas, créditos y préstamos, con abonos) e *Inventario* (nombre/modelo y unidades). Forma de pago: **Contado**, **Cuotas** (sin interés) o **Crédito / Préstamo** (con `%` de interés sobre saldo insoluto y día de corte). Los préstamos de dinero se registran aquí mismo.
5. **Clientes:** tres vistas — *Tarjetas* (saldo actual, deuda total e historial), *Mayor deuda* y *A – Z*.
6. **Deudas:** deudas propias + pago del período de tarjetas, con historial de pagos.

El botón ⚙ del encabezado abre **Respaldo y Ajustes** (exportar/importar JSON). Las semanas van de domingo a sábado. Si la fecha se deja vacía se usa la de hoy.

Cualquier registro puede editarse o eliminarse; todo se recalcula al momento. Los datos de versiones anteriores se migran automáticamente (las categorías pasan a ser segmentos). La versión instalada se ve en el menú ☰.
