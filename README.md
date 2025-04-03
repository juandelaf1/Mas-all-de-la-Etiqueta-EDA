![cabecera-vinedos](https://github.com/user-attachments/assets/78828135-359f-415b-a8e0-894c8142f7ab)


# Análisis Exploratorio de Datos (EDA) sobre Vinos Españoles

## 📌 Objetivo
Realizar un análisis exploratorio de datos (EDA) para identificar patrones en vinos españoles, centrándose en:
- Relación entre características (precio, región, tipo) y calificaciones.
- Influencia de las denominaciones de origen (D.O.) y regiones en el mercado vinícola.

---

## 📋 Hipótesis
### 🔍 Principal
- **Relación calidad-precio**: Es el factor principal que influye en las calificaciones y reseñas positivas.

### 🔍 Secundarias
1. **Regiones reconocidas**: Vinos de La Rioja/Ribera del Duero tienen mejores calificaciones.
2. **Regiones menos conocidas**: Destacan por autenticidad y relación calidad-precio.
3. **Bodegas reconocidas**: Obtienen mejores calificaciones, independientemente del precio.
4. **Acidez y cuerpo**: Asociados a mejores valoraciones y precios altos.

---

## 📂 Datos
- `vinos_espana.csv`: Información de vinos (bodega, año, calificación, precio, región, tipo, etc.).
- `totales_vino_y_otros.csv`: Consumo de vino en España.
- `bebidas_c_semanal.csv`: Consumo semanal de bebidas alcohólicas.

---

## 🛠 Procesamiento
### 🔧 Limpieza
1. Normalización de nombres de regiones (minúsculas).
2. Relleno de valores faltantes:
   - `type`: Usando datos de `region`.
   - `body` y `acidity`: Con la media por región.
3. Eliminación de filas con valores nulos.

### ➗ División
- Dos DataFrames:
  - Vinos con precio ≤ 100€.
  - Vinos con precio > 100€.

---

## 📊 Análisis
### 📌 Estadísticas Clave
| **Variable**       | **Vinos ≤100€**       | **Vinos >100€**       |
|--------------------|-----------------------|-----------------------|
| Precio medio       | 34.64€               | 388.42€              |
| Calificación media | 4.23                 | 4.53                 |

### 🔗 Correlaciones
- **Vinos ≤100€**:
  - Precio-Calificación: Moderada (0.34).
  - Acidez/Cuerpo-Calificación: Baja.
- **Vinos >100€**: Correlación más fuerte entre precio y calificación.

### 📈 Visualizaciones
1. **Mapa de calor**: Correlaciones entre variables.
2. **Gráfico de barras**: Varianzas de precio y calificación.
3. **Gráfico de dispersión**: Relación calidad-precio.

---

## 🎯 Conclusiones
1. **Calidad-precio**: Correlación moderada (especialmente en vinos caros).
2. **Regiones**: La Rioja/Ribera del Duero tienen calificaciones más altas.
3. **Acidez/cuerpo**: No determinantes en valoraciones (para vinos económicos).
4. **Bodegas reconocidas**: Mejores calificaciones, sin depender del precio.

---

## 💡 Recomendaciones
1. **Marketing**: Enfatizar relación calidad-precio en gama media-alta.
2. **Enfoque regional**: Promover vinos de regiones menos conocidas con buena relación calidad-precio.
3. **Futuros análisis**:
   - Impacto de reputación de bodegas.
   - Influencia del año de cosecha y tipo de uva.

---

## 🚀 Próximos Pasos
- Analizar datos de consumo.
- Integrar variables adicionales (ej.: maridaje, envejecimiento).
- Modelar predicciones de calificación basadas en características clave.
