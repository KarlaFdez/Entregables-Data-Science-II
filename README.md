# Entregables-Data-Science-II
[README.md](https://github.com/user-attachments/files/22391995/README.md)
# Data Vehículos Eléctricos en USA

**creado por Karla Fernández – Data Science II (Entrega I)**

## Descripción
Análisis del dataset de vehículos eléctricos (EV) del estado de Washington (USA) usando la API pública `https://data.wa.gov/resource/f6w7-q2d2.csv` o un CSV local equivalente. El flujo es **robusto** a nulos y variaciones de columnas, e incluye **limpieza**, **feature engineering**, **EDA** (matplotlib), y **modelos base** (clasificación, regresión y clustering).

## Contenidos
- `data_vehiculos_electricos_usa_v8.ipynb`: Notebook principal con secciones explícitas de **Preguntas e hipótesis** y **Conclusiones (desarrolladas)**.  
- `data_vehiculos_electricos_usa_storytelling_COMBINED.pptx`: Presentación **combinada** con **KPIs + tabla** e **imágenes del EDA** embebidas.  
- `outputs/ev_clean.csv`: Datos limpios (se genera al ejecutar el notebook).  
- `outputs/figs/`: Figuras del EDA (se generan al ejecutar el notebook o ya están incluidas como PNG).

## Hipótesis
- **Correlación:** H1 `electric_range` ~ `model_year` (+); H2 `electric_range` ~ `base_msrp` (+)  
- **Clasificación:** H3 predecir BEV vs PHEV con rango, año y precio  
- **Regresión:** H4 explicar `electric_range` por año, marca y MSRP  
- **Clustering:** H5 ≥3 clústeres (entrada/medio/premium)

## Conclusiones clave
- El rango aumenta con el año-modelo; MSRP–rango muestra relación positiva no lineal.  
- BEV tienden a mayor rango y precio; el tipo se puede clasificar con buena precisión según columnas disponibles.  
- Segmentación en 3 clústeres es útil para infraestructura y estrategia de producto.

## Notas de robustez
- Conversión numérica con `errors="coerce"` ⇒ inválidos a **NaN**.  
- Imputaciones conservadoras, protecciones ante división por cero y outliers por IQR sin fallos.  
- Modelos se ejecutan sólo si hay suficientes datos y variación; si no, se omiten sin romper el flujo.


