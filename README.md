Objetivo
El análisis exploratorio de datos (EDA) examina información sobre vinos españoles para identificar patrones relacionados con sus características y precios, con especial atención a las denominaciones de origen (D.O.) y regiones, buscando comprender cómo estos factores influyen en el mercado vinícola.

Hipótesis
Principal: La relación calidad-precio es el principal factor que influye en las calificaciones y reseñas positivas de los vinos en España.

Secundarias:

Los vinos de regiones específicas (La Rioja, Ribera del Duero) tienden a recibir mejores calificaciones.

Los vinos de regiones menos conocidas pueden destacar por su autenticidad y buena relación calidad-precio.

Los vinos de bodegas reconocidas obtienen mejores calificaciones, independientemente del precio.

El equilibrio entre acidez y cuerpo en un vino suele asociarse con mejores valoraciones y precios más altos.

Datos
vinos_espana.csv: Contiene información sobre vinos españoles (bodega, vino, año, calificación, número de reseñas, país, región, precio, tipo, cuerpo, acidez).

totales_vino_y_otros.csv: Datos sobre consumo de vino en España.

bebidas_c_semanal.csv: Datos sobre consumo semanal de bebidas alcohólicas.

Procesamiento de Datos
Limpieza:

Conversión de nombres de regiones a minúsculas.

Relleno de valores faltantes en la columna 'type' con los de 'region'.

Relleno de valores faltantes en 'body' y 'acidity' con la media de la misma región.

Eliminación de filas con valores nulos.

División:

Creación de dos DataFrames: vinos con precio hasta 100€ y vinos con precio desde 100€.

Análisis
Resumen Estadístico:

Vinos hasta 100€: Precio medio ≈34.64€, calificación media ≈4.23.

Vinos desde 100€: Precio medio ≈388.42€, calificación media ≈4.53.

Correlaciones:

Vinos hasta 100€: Correlación moderada (0.34) entre precio y calificación, baja entre acidez/cuerpo y calificación.

Vinos desde 100€: Correlación más fuerte entre precio y calificación.

Visualizaciones:

Mapa de calor de correlaciones.

Gráfico de barras para varianzas de precio y calificación.

Gráfico de dispersión para relación calidad-precio.

Conclusiones
Relación calidad-precio: Existe una correlación moderada, especialmente en vinos de mayor precio, lo que sugiere que los consumidores valoran mejor los vinos más caros.

Regiones: Los vinos de regiones reconocidas como La Rioja y Ribera del Duero tienen calificaciones más altas.

Acidez y cuerpo: No son factores determinantes en las valoraciones, especialmente en vinos de menor precio.

Bodegas reconocidas: Los vinos de bodegas conocidas tienden a tener mejores calificaciones, independientemente del precio.

Recomendaciones
Marketing: Destacar la relación calidad-precio, especialmente para vinos de gama media-alta.

Enfoque regional: Promover vinos de regiones menos conocidas que ofrecen buena relación calidad-precio.

Futuros análisis: Profundizar en el impacto de la reputación de las bodegas y explorar más variables como el año de cosecha y el tipo de uva.
