🛵 Food Delivery Logistics & Bottleneck Analysis (50,000 Records)

**Análisis de Eficiencia Operativa, Tasa de Cancelación y Desfase de ETA en Plataformas de Delivery**
Análisis de 50,000 pedidos de delivery para identificar la causa raíz del incremento en el tiempo estimado de llegada (ETA), retrasos y cancelaciones. El estudio reveló que el cuello de botella proviene de tiempos muertos en restaurantes, no de los repartidores, permitiendo diseñar un plan de eficiencia.

🎯 Problema de Negocio
Las plataformas de *Quick-Commerce* enfrentan pérdidas operativas debido a cancelaciones y cuellos de botella en horas pico. El objetivo del análisis fue:
1. Identificar la causa raíz de los retrasos en las entregas.
2. Medir el impacto monetario e imprecisión del $ETA$ (*Estimated Time of Arrival*).
3. Diseñar propuestas estratégicas (SLA y asignación dinámica) para optimizar el margen operativo por hora.

🛠️ Tech Stack Utilizado
* **Python (Pandas, NumPy):** Limpieza de datos, imputación de valores nulos, ingeniería de variables (cálculo de deltas de tiempo) y análisis exploratorio (EDA).
* **Power BI & DAX:** Modelado de datos, creación de medidas interactivas (Tasa de Retraso, Error de ETA %, Cancelaciones por causa raíz).
* **SQL:** Consultas analíticas y filtrado de segmentos por franja horaria y categoría.

📊 Principales Hallazgos (Insights)
1. **El Mito del Repartidor:** El 68% de las cancelaciones por demora estuvieron asociadas a tiempos de espera excesivos en la sucursal antes de que el repartidor iniciara el viaje.
2. **Brecha de ETA:** En horas pico (14:00 - 16:00 y 20:00 - 22:00), el $ETA$ prometido al cliente tuvo una desviación promedio de +14 minutos sobre el tiempo real de preparación.
3. **Impacto Financiero:** Un retraso acumulado superior a 20 minutos incrementa la probabilidad de cancelación del pedido en un 35%, generando pérdidas directas en comisiones no cobradas.

💡 Recomendaciones de Negocio & Solución Estratégica
* **Asignación Dinámica de Conductores:** Desfasar la notificación al repartidor según el tiempo histórico de preparación de cada restaurante (evita minutos muertos del chofer en la tienda).
* **Acuerdos de Nivel de Servicio (SLA) & Penalizaciones:** Implementar ajustes en el algoritmo de visibilidad o cargos por tiempo de espera a tiendas que superen recurrentemente el tiempo límite de cocina.
* **Incentivos a Aliados Eficientes:** Priorizar en el motor de búsqueda a los comercios con menor tiempo de preparación e imprecisión de $ETA$.

