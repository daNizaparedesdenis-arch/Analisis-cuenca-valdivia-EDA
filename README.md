# Análisis Ambiental y Económico de la Cuenca de Valdivia (2008-2020) 💧📉

## 📖 Descripción del Proyecto
Este proyecto de análisis de series de tiempo busca comprender la interacción histórica a largo plazo entre la disponibilidad hídrica natural y su impacto económico. Específicamente, explora la relación entre las precipitaciones, los caudales de la cuenca de Valdivia y la tarifa de agua potable fijada por la empresa Aguas Décima durante un periodo continuo de 12 años.

El objetivo principal es responder a la pregunta: **¿Cómo reacciona la tarifa económica del agua frente a las variaciones y tendencias a largo plazo en la disponibilidad hídrica de la cuenca?**

## 🛠️ Stack Tecnológico
* **Lenguaje:** Python
* **Librerías:** Pandas
* **Entorno:** Jupyter Notebook / Entorno de desarrollo interactivo

## 🚀 Fase 1 Completada: Data Preparation (Limpieza y Unificación)
El mayor desafío de esta fase inicial fue estructurar y limpiar bases de datos gubernamentales y públicas complejas para unificarlas en un único marco de análisis temporal. Los principales hitos técnicos incluyen:

* **Ingeniería de Fechas (Datetime):** Transformación y unificación de variables temporales separadas (año, mes, día) hacia un formato estándar de serie de tiempo (`datetime64`) en múltiples fuentes de datos.
* **Transformación de Estructuras (Reshaping):** Uso avanzado de `pd.melt()` para transformar bases de datos tarifarias desde un formato "ancho" (múltiples años distribuidos como columnas) a un formato "largo" analizable, aislando específicamente a la concesionaria de interés (Aguas Décima).
* **Limpieza de Formatos Complejos:** Resolución de problemas de lectura en archivos Excel con encabezados múltiples, extrayendo dinámicamente años atrapados en las primeras filas de datos y ajustando dinámicamente los nombres de las columnas.
* **Consolidación Relacional (Merge):** Integración exitosa de tres bases de datos de distinta naturaleza (clima, hidrología y economía) mediante `pd.merge()` (Inner Join) utilizando la fecha como llave principal, resultando en un único DataFrame (`df_final_valdivia`) estructurado y sin valores vacíos.

  ## 📊 Fase 2: Visualización y Análisis de Tendencias

El primer hito analítico del proyecto consiste en visualizar la tendencia histórica a largo plazo de la Cuenca de Valdivia (2008-2020). Específicamente, se explora la relación entre la disponibilidad hídrica natural y el impacto económico fijado por Aguas Décima utilizando Python y Pandas.

📈 Gráfico de doble eje Y: Integración de la disponibilidad hídrica (Caudal promedio en m³/s) en el eje principal y el impacto económico (Tarifa en $/m³) en el eje secundario utilizando la librería Matplotlib.

🧹 Limpieza en caliente: Estandarización final de encabezados de columnas y agrupación de series de tiempo por año calendario (.groupby) para aislar la macro-tendencia y mitigar el ruido estacional de los datos.

💡 Insights Iniciales: En el gráfico realizado no se puede ver una relación directa entre el caudal y la tarifa media anual, aunque si se puede ver una ligera variación en los mismos periodos de tiempo entre los caudales más grandes y los cobros un poco más bajo en el consumo de agua, aunque el periodo de tiempo es demasiado limitado como para asegurar que tengan que ver uno con el otro.

## 🔜 Próximos Pasos (En desarrollo)
* **Análisis Exploratorio de Datos (EDA):** Cálculo de la evolución anual base para las tres variables.
* **Análisis de Tendencias:** Aplicación de medias móviles para suavizar la estacionalidad e identificar la macro-tendencia de la década.
* **Visualización de Datos:** Creación de gráficos de series de tiempo interactivos o estáticos utilizando Matplotlib/Seaborn.

---
*Este proyecto está siendo desarrollado de forma iterativa y "en público". Las actualizaciones de código y visualizaciones se subirán periódicamente.*
