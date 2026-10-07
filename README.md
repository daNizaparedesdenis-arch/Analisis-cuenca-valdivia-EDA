# Análisis Ambiental y Económico de la Cuenca de Valdivia (2008-2020)

Descripción del Proyecto
Este proyecto busca analizar la tendencia histórica a largo plazo para comprender cómo interactúa la disponibilidad hídrica natural con el impacto económico. Específicamente, analiza la relación entre las precipitaciones, los caudales de la cuenca y la tarifa de agua potable fijada por la empresa Aguas Décima durante un periodo de 12 años.

Stack Tecnológico

Python

Pandas

Fase 1 completada: Preparación de Datos (Data Prep)
El mayor desafío de esta fase inicial fue estructurar bases de datos públicas complejas para poder unificarlas. Los hitos técnicos incluyen:

Limpieza de Fechas: Transformación y unificación de columnas separadas (año, mes, día) a un formato de serie de tiempo (datetime) estándar.

Transformación de Estructuras (Melt): Uso avanzado de pd.melt() para transformar bases de datos gubernamentales de tarifas desde un formato "ancho" (años distribuidos en múltiples columnas) a un formato "largo" analizable.

Limpieza de Celdas Combinadas: Resolución de problemas de lectura en archivos Excel con encabezados múltiples y años atrapados en las primeras filas de datos.

Consolidación Relacional: Integración de tres bases de datos de distinta naturaleza (clima, hidrología y economía) mediante pd.merge() (Inner Join) en un único DataFrame (df_final_valdivia) listo para la visualización.
