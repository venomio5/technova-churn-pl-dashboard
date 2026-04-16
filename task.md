### 🏢 Brief de TechNova Soluciones

**De:** Roberto, Director General
**Para:** Consultor de Datos Freelance
**Asunto:** Requerimientos para Dashboard Directivo - Churn & P&L

¡Hola! Qué gusto saludarte. Como platicamos en la videollamada, en *TechNova* hemos crecido bastante en los últimos tres años, pero honestamente, estamos volando a ciegas. Nuestro equipo de contabilidad y ventas nos manda reportes en sábanas de Excel larguísimas que nadie entiende, y me toma días cruzar la información.

Necesito que nos construyas un  **Dashboard Directivo** , preferentemente en **Power BI** (o un Excel muy bien armado con Power Query y macros, lo que consideres más robusto), que me responda las preguntas clave del negocio en 5 minutos.

Esto es exactamente lo que necesito que entregues:

1. **Análisis de Churn (Fuga de Clientes):**
   * Quiero saber cuántos clientes perdemos cada mes y cuál es nuestra tasa de churn.
   * Necesito poder filtrarlo por tipo de plan (Básico, Pro, Enterprise).
2. **P&L Simplificado y Flujo de Caja:**
   * Un estado de resultados al grano: Ventas Totales, Costo de Ventas (COGS), Gastos Operativos y el Margen Bruto y Neto.
   * Entradas y salidas de efectivo (Cash Flow) para saber si nos estamos quedando sin liquidez.
3. **Comparativos (Inteligencia de Tiempo):**
   * Todo tiene que poder verse **Mes vs Mes (MoM)** y  **Año vs Año (YoY)** . Si en noviembre de este año vendí más o menos que en noviembre del año pasado, quiero saberlo al instante.
4. **Alertas Visuales:**
   * Esto es súper importante para mí. Si el margen neto cae por debajo del 15%, o si la tasa de churn supera el 5% en un mes, quiero que el gráfico o el número se ponga en **rojo brillante** o tenga una alerta visual clara.

Te voy a pasar dos bases de datos que logré extraer de nuestros sistemas. Te advierto:  **la información está sucia** . A veces los asesores escriben mal los estatus, hay formatos de fechas mezclados y creo que faltan algunos datos financieros. Necesito que limpies eso en tu modelo de datos antes de graficar.

¿Cuento contigo?

---

Preguntas

Hay un hueco en gastos operativos del jueves, 1 de febrero de 2024, lo deje asi, fue un error? Puedo crear una regression linear para poner los gastos con una estimación fundamentada. Igual seria 1 sola vez, a menos de que si pasa en un futuro, quieras un excel donde puedas estimar si es que faltan unos numeros.

Cohort analysis?
