## Análisis Comercial – Online Retail II (2009–2011)
## Contexto
Proyecto de análisis comercial sobre el dataset Online Retail II (UCI / Kaggle), que contiene transacciones de e-commerce entre diciembre de 2009 y diciembre de 2011.
El objetivo fue construir un pipeline end-to-end que permitiera limpiar, estructurar y analizar los datos para extraer métricas clave de negocio por período, país, cliente y producto.

## Objetivo
Transformar datos transaccionales crudos en información accionable a través de:
Limpieza y validación del dataset original
Creación de métricas derivadas (Revenue)
Análisis multidimensional mediante SQL
Visualización de resultados en Power BI

-----------

## Herramientas Utilizadas
Excel (revisión inicial del CSV)
Python (pandas, sqlite3)
SQL (SQLite)
Power BI

-----------

## Estructura del Proyecto
Carpeta 0 — Documentación y datos limpios
Carpeta 1 — Revisión inicial del CSV en Excel
Carpeta 2 — Limpieza en Python y análisis en SQL
Carpeta 3 — Dashboard Power BI

-----------

## Metodología
Revisión visual del CSV en Excel para detectar errores estructurales.
Carga en Python y análisis de valores inválidos con pandas.
Filtrado de registros que no cumplían criterios de venta válida: Quantity > 0, Price > 0 y Customer ID presente.
Creación de columna Revenue = Quantity × Price.
Exportación del dataframe limpio a SQLite y construcción de consultas por período, país, cliente y producto.
Exportación de resultados SQL como CSV e importación a Power BI.
Construcción de dashboard de 3 páginas.

-----------

## Principales Hallazgos
El dataset original contaba con 1.067.371 filas. Tras la limpieza se retuvieron 805.549 registros válidos, eliminando un 24,5% del total por registros con Quantity negativa, Price igual a cero o sin Customer ID.
Los ingresos totales del período fueron $17,74 millones, con 5.878 clientes únicos y 36.969 órdenes.
United Kingdom concentra el 83% del revenue total ($14,7 mill.), evidenciando una alta dependencia geográfica. EIRE, Netherlands, Germany y France completan el top 5 con participaciones marginales.
El negocio muestra estacionalidad clara con picos en el último trimestre del año, especialmente en noviembre de 2010 (~$1,2 mill.) y noviembre de 2011 (~$1,15 mill.).
El cliente 18102 lidera el ranking con $608.821 en revenue total. Existe una brecha considerable entre los dos primeros clientes y el resto del top 10.
REGENCY CAKESTAND 3 TIER es el producto de mayor revenue ($286.486), pero WHITE HANGING HEART T-LIGHT HOLDER lidera en unidades vendidas (93.640), evidenciando una diferencia estructural entre productos de alto valor unitario y productos de alta rotación.

-----------

## Limitaciones
Los registros con Quantity < 0 (devoluciones y cancelaciones) fueron eliminados en la limpieza y no se analizaron por separado.
No se modeló la evolución del comportamiento individual de clientes a lo largo del tiempo.
La caída abrupta en diciembre de 2011 sugiere un corte de datos a mitad de mes, no una caída real del negocio.

-----------

## Competencias Demostradas
Pipeline end-to-end: Excel → Python → SQL → Power BI.
Limpieza y validación de datos con criterios de negocio explícitos.
Ingeniería de features (columna Revenue).
Consultas SQL para agregación multidimensional por tiempo, país, cliente y producto.
Construcción de dashboards en Power BI desde fuentes externas.
Comunicación estructurada de hallazgos con soporte en evidencia.