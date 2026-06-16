# analysis_everpeak

##### Exploración y calidad de los datos

Como primer paso del análisis exploratorio, se evaluó la cardinalidad de las variables mediante nunique().sort_values(). Esto permitió identificar la cantidad de valores únicos en cada columna, encontrando 4 métodos de pago distintos, 10 ciudades y 1,829 clientes únicos.

Posteriormente, se analizó la presencia de valores faltantes utilizando df.isna().mean().sort_values(ascending=False), lo que permitió cuantificar el porcentaje de datos ausentes por variable y priorizar las acciones de limpieza.

Para evaluar la calidad y consistencia de los datos registrados, se realizaron diversas validaciones. Se revisó la distribución de las categorías de productos mediante df["product_category"].value_counts(), se identificaron cantidades inválidas o no positivas con df['quantity'].le(0).sum(), y se analizaron estadísticas descriptivas de variables numéricas como edad del cliente y cantidad de productos utilizando df[['customer_age', 'quantity']].describe(). Estas verificaciones permitieron detectar posibles anomalías, valores atípicos y registros inconsistentes antes de continuar con el análisis.
