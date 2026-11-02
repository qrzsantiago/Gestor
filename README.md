# Gestor · Finanzas e Inventario

Web App de una sola página (`index.html`) para iPhone (Safari → **Compartir → Agregar a pantalla de inicio**), ejecutada a pantalla completa.

- **Stack:** HTML + JavaScript puro, Tailwind CSS (CDN) y Lucide Icons (CDN).
- **Persistencia:** LocalStorage. Respaldo/restauración en JSON desde *Respaldo y Ajustes*.
- **Moneda:** Pesos Mexicanos (MXN), formato `$10,000.00`.
- **Sin datos precargados:** la app inicia vacía; todos los formularios inician en blanco.

## Secciones
- **Dashboard:** tarjetas de crédito y cuentas hasta arriba; luego balance, por cobrar, por pagar, stock, alertas, ventas del período e inventario activo.
- **Tarjetas y Cuentas:** el *pago del período* se muestra separado de MSI, otros saldos diferidos y compras posteriores al corte (que pasan solas al pago del período en el siguiente corte).
- **Inventario:** solo nombre/modelo libre y unidades disponibles.
- **Ventas:** historial completo; cada venta descuenta unidades del inventario.
- **Clientes** y **Créditos y Préstamos** (secciones independientes): sin plazos fijos; interés sobre saldo insoluto en cada fecha de corte, con % y día de corte modificables; abonos de cualquier monto.
- **Gastos:** categorías creadas por el usuario (libres, semanales, quincenales o mensuales).
- **Mis Deudas**, **Movimientos** (todo editable) y **Respaldo y Ajustes**.

Cualquier registro puede editarse o eliminarse; todo se recalcula al momento. Los datos de la versión anterior se migran automáticamente.
