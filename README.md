# Gestor · Finanzas e Inventario

Web App de una sola página (`index.html`) para administrar ventas, inventario, clientes, créditos/préstamos, gastos, tarjetas de crédito y cuentas. Optimizada para iPhone (Safari → **Compartir → Agregar a pantalla de inicio**) y ejecución a pantalla completa.

- **Stack:** HTML + JavaScript puro, Tailwind CSS (CDN) y Lucide Icons (CDN).
- **Persistencia:** LocalStorage del navegador. Respaldo/restauración en JSON desde *Respaldo y Ajustes*.
- **Moneda:** Pesos Mexicanos (MXN), formato `$10,000.00`.

## Módulos
- **Dashboard:** Balance total, por cobrar, por pagar, stock total, alertas, tarjetas y cuentas, ventas del período e inventario activo.
- **Inventario y Ventas:** productos libres (nombre/modelo, unidades, costo, venta); las ventas descuentan stock al instante y pueden asignarse a un cliente, de contado o a crédito.
- **Clientes y Créditos:** préstamos y ventas a crédito en pago único, a plazos o MSI; intereses automáticos sobre saldo insoluto en cada fecha de corte; abonos con estado `Pendiente` / `Abonado` / `Pagado`.
- **Gastos:** filtros semanal, quincenal, mensual e histórico (sin reinicios).
- **Tarjetas y Cuentas:** varias tarjetas con límite, saldo utilizado, MSI, disponible, día de corte y de pago con alertas de color.
- **Mis Deudas** y **Movimientos** (historial completo, editable).

Cualquier registro puede editarse o eliminarse; todos los totales se recalculan al momento.

> Requiere conexión la primera vez para cargar Tailwind y Lucide desde CDN; Safari los conserva en caché.
