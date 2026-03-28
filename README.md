# Solemne 1
# Análisis de Datos Financieros: S&P 500 vs. Oro (2019-2026)

### 1. Introducción y Contexto
Este pequeño proyecto presenta un análisis comparativo entre el índice bursátil S&P 500 y el oro, un activo considerado tradicionalmente como refugio de valor. El objetivo principal es evaluar la relación de riesgo (volatilidad), correlación y rendimiento acumulado de ambos activos durante un período que abarca desde inicios de 2019 hasta principios de 2026.

### 2. Obtención y Limpieza de Datos
Los datos fueron obtenidos directamente de la API de Yahoo Finance para los tickers SPY (S&P 500 ETF Trust) y GLD (SPDR Gold Shares).
El flujo de trabajo incluyó:
1. Descarga de los precios de cierre diarios.
2. Manejo de valores nulos.
3. Transformación de variables (normalización y cálculo de retornos diarios).

## 3. EDA y Visualización
### Rendimiento Acumulado: ¿Qué pasó con el precio del oro cuando las acciones cayeron por la pandemia en marzo de 2020?
Este gráfico muestra la evolución de $100 invertidos en cada activo a principios de 2019. Ambos activos están normalizados a base 100.

**Análisis:** A principios de 2020, se observa una caída brusca y profunda en el S&P 500. Simultáneamente, el oro muestra un comportamiento estable, ampliando significativamente la brecha. Este es un comportamiento clásico de flight-to-safety, posiblemente coincidiendo con el inicio de la pandemia de COVID-19. Tras el shock inicial, el S&P experimenta una recuperación sostenida, superando el rendimiento del oro del oro hacia principios de 2021 y manteniendo una ventaja considerable durante el período intermedio. Hacia el final del período (2025-26) el oro experimenta un aumento himperbólico, superando por un margen muy amplio el rendimiento acumulado del S&P 500 . Mientras las acciones siguen creciendo, el oro se convierte en el activo mde mejor rendimiento del período con diferencia.

### Volatilidad Anual del S&P 500: ¿Cuál fue el año de mayor riesgo e incertidumbre para el mercado accionario y cómo se evidencia estadísticamente?
Este diagrama de caja permite analizar cómo varió la volatilidad del mercado bursátil año tras año, utilizando retornos diarios.

**Análisis:** El año 2020 destaca visualmente como una anomalía. La caja (IQR) es notablemente más alta y los "bigotes" son mucho más largos que en cualquier otro año, indicando una dispersión de retornos diarios (volatilidad) mucho mayor. Años como 2019, 2023, 2024 y 2026 muestran cajas mucho más "aplastadas" y rangos más cortos, sugiriendo un crecimiento de mercado más estable y predecible.

### Distribución de Probabilidad de Retornos Diarios: ¿Cuál de los dos activos presenta una mayor desviación estándar?
Este gráfico superpone los histogramas y curvas de densidad de probabilidad (KDE) para el oro y las acciones, permitiendo evaluar el riesgo relativo.

**Análisis:** Ambas distribuciones tienen una forma aproximadamente normal, indicando una mayor probabilidad de eventos extremos de lo que predeciría una distribución normal pura. La distribución del S&P 500 (azul) presenta un "ancho" visualmente mayor y un pico ligeramente más bajo en comparación con la del oro (amarillo). Esto significa que los retornos diarios de las acciones varían más y tienen "colas" que se extienden más.

### Análisis de Correlación: ¿Si las acciones suben un día, el oro también tiende a subir, o se mueven de forma independiente?
Este gráfico de dispersión examina el grado de acoplamiento diario entre los dos activos.

**Análisis:** Se mueven de forma independiente. Como los puntos en el gráfico están muy dispersos y la línea roja es casi plana (correlación de solo $0.10$), podemos decir que lo que le pase a la bolsa no afecta mayormente al precio del oro. 

## 4. Conclusiones Finales
Basado en el análisis de los 4 gráficos generados, se pueden extraer las siguientes conclusiones:

1. El análisis detallado del shock de 2020 en el gráfico de rendimiento acumulado y la volatilidad extrema identificada en el boxplot confirman que, durante el período de pánico inicial, el oro cumplió eficazmente su función de activo refugio, permaneciendo estable o subiendo mientras las acciones se hundían.
2. El histograma y el boxplot confirman que el S&P 500 es el activo intrínsecamente más volátil y arriesgado día a día.
3. El hallazgo más impactante es que, a pesar de la fuerte recuperación de las acciones post-2020, el oro terminó el período (2019-2026) con un rendimiento superior, impulsado por una subida hiperbólica final.
4. La correlación cercana a cero (0.10) ratifica que el oro es un diversificador de portafolio efectivo.