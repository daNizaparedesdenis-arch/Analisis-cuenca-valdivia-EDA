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

## 🔜 Próximos Pasos (En desarrollo)
* **Análisis Exploratorio de Datos (EDA):** Cálculo de la evolución anual base para las tres variables.
* **Análisis de Tendencias:** Aplicación de medias móviles para suavizar la estacionalidad e identificar la macro-tendencia de la década.
* **Visualización de Datos:** Creación de gráficos de series de tiempo interactivos o estáticos utilizando Matplotlib/Seaborn.

---
*Este proyecto está siendo desarrollado de forma iterativa y "en público". Las actualizaciones de código y visualizaciones se subirán periódicamente.*