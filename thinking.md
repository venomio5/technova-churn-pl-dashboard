Entonces lo primero que voy a hacer es diseccionar exactamente qué es lo que quiere Roberto, el director general para este proyecto del dashboard directivo. Okay, entonces primero que nada es un dashboard directivo, es decir, voy a estar creando un Power BI en donde tenga información. Okay, vamos a ir poco a poco. ¿Cuál es el negocio que tienen ellos? Ellos tienen un negocio de ventas y es un B2B, business to business. Okay. Entonces, ¿qué es lo que quieren? Un análisis de churn, fuga de clientes. Con esto entendemos que tienen una suscripción y quieren saber su tasa de fuga. ¿Por qué? Porque eso te dice qué tanta retención tiene un cliente, básicamente, ¿no? Pues prácticamente esto está relacionado con ventas en un futuro, pero bueno, no voy a explicar exactamente lo que es la fuga de clientes, aunque igual sería muy importante tenerla en cuenta, porque normalmente también lo que piden aquí es un lifetime value por cliente, ¿no? Entonces, ¿por qué esa tasa de churn que es realmente lo que van a tener en cuenta, para qué la quieren? Es como una métrica de calidad de la suscripción de lo que se está vendiendo. Y lo va a filtrar por plan básico, pro y enterprise, dependiendo qué tan bueno es en ciertos tipos de planes, para saber qué plan necesita a lo mejor apoyo, un análisis más detallado. Luego después tenemos un profit and loss simplificado y flujo de caja, un estado de resultados al grano, ventas totales, cuánto vendimos. Yo creo que más que nada es en dinero, no en las suscripciones pero normalmente se trata de dinero. Costo de ventas, COGS, okay, sale prácticamente cuánto costó vender uno. Gastos operativos y el margen de producto neto. Prácticamente un profit and loss de finanzas, pero en el dashboard. Entradas y salidas de efectivo, cash flow para saber si nos estamos quedando sin liquidez, a lo mejor se va a necesitar tener dos páginas o tres páginas a lo mejor para que esté bien todo organizado y luego tenemos comparativos de inteligencia que es el year over year, month over month, muy bien, alertas visuales. Están bien. Okay, perfecto. Entonces el lobo me dice que los datos están mal. Alright.

Entonces, ¿cuál es el plan? Las estrategias y los planes siempre vienen desde el objetivo final, pero para saber el objetivo final necesito saber exactamente qué significa o exactamente cómo lo voy a estar viendo y qué significan ciertos datos. Y como este es mi primer proyecto en esto, voy a tener que primero entender muy bien lo que es la fuga de clientes y lo que son las ventas totales, los costos de ventas, costos operativos, margen bruto y neto, y también el cash flow. Tengo que saberlo todo. Ya, necesito primero aprender qué significa cada uno, qué es lo que realmente quiere ver el director, y para eso aprender exactamente qué significan esas cosas a mayor detalle. O sea, aprender eso de negocios. Normalmente esto no lo haría, pero como esto es de las primeras veces, nada más quiero reforzar exactamente estas definiciones.

### Guía del Diseño (Layout Ejecutivo)

Como puedes ver, logramos meter los tres pilares (Churn, P&L y Cash Flow) sin que se viera apretado. Aquí te explico la lógica de cada sección para cuando empieces a arrastrar datos en Power BI:

#### 1. Banner de Filtros (Top Row)

Ubicamos los segmentadores (Slicers) de forma horizontal para ahorrar espacio vertical.

* **Plan:** El selector con "Básico", "Pro" y "Enterprise".
* **Año/Mes:** Filtros estándar para la inteligencia de tiempo.
* **Switch MTD/YTD (Lo que platicamos):** Un botón selector para que Roberto elija si los números grandes son del mes actual o del acumulado del año.

#### 2. Las Tarjetas KPI (El "Resumen en 2 segundos")

Aquí es donde aplicamos el truco de los **Triángulos de Delta** que te gustó:

* **Métrica Principal:** El número grande (ej. Tasa de Churn Actual).
* **Contexto (Abajo del número):** Puse dos pequeños indicadores para MoM y YoY con flechas triangulares. (▲ Rojo = Malo en Churn, Verde = Bueno en Churn; ▲ Verde = Bueno en Margen/Caja).

#### 3. El Waterfall Magnífico (P&L)

Usamos el objeto visual **Waterfall Chart** para el Estado de Resultados:

* **Flujo:** Empieza en  **Ventas Totales** , bajan los **COGS** (en rojo), y aquí creamos el primer **Punto de Control/Subtotal** llamado **Margen Bruto** (barra verde).
* **Final:** Siguen bajando los **OpEx** (rojo) hasta llegar al subtotal final de  **Margen Neto** .

#### 4. Gráfico de Cash Flow y Churn por Plan (Bottom Row)

* **Cash Flow (Combo Chart):** Usamos barras para Entradas/Salidas mensuales y una **línea azul** para el  **Efectivo Acumulado** . Esta línea es la que Roberto debe vigilar: si baja mucho, no hay liquidez.
* **Churn por Plan (Barras):** Una vista rápida para complementar el KPI de arriba, permitiendo ver qué plan está fallando más.

Ok, entonces como ya tengo el diseño, ahora lo que voy a hacer es enviar los datos al Power BI, limpiarlo todo, después juntar todas las tablas, generar la tabla del calendario e ir armándolo poco a poco.
