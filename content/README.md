# Playground de Machine Learning

**Tópicos de Inteligencia de Negocios** · Análisis de Datos

Bienvenid@ al playground. Cada notebook es un laboratorio interactivo donde puedes experimentar con un modelo distinto.

## Modelos disponibles

| Notebook | Tipo | Qué practicas |
|----------|------|---------------|
| **regresion_lineal.ipynb** | Regresión | Ajuste polinomial, regularización Ridge/Lasso |
| **regresion_logistica.ipynb** | Clasificación binaria | Frontera lineal, umbral, curva ROC |
| **knn.ipynb** | Clasificación | Vecindad, K, distancias, pesos |
| **arboles_decision.ipynb** | Clasificación | Profundidad, criterio, poda, importancia |
| **kmeans.ipynb** | Clustering (no supervisado) | K, inicialización, codo y silueta |

## Cómo usar cada notebook

1. **Abre el notebook** desde el panel de la izquierda.
2. **Ejecuta la primera celda** (la de imports) con `Shift + Enter`. Espera unos segundos — la primera vez se descargan las librerías de Python.
3. **Ejecuta el resto de las celdas** en orden. Cuando llegues a un Playground, verás los controles interactivos.
4. **Mueve los sliders** y haz clic en el botón **🚀 Entrenar modelo** para aplicar los cambios.
5. **Botones `?`** junto a cada control: clic para ver la explicación.

## ¿No te aparecen los widgets?

Refresca la página (`F5`) y vuelve a ejecutar las celdas. La primera ejecución a veces toma 30-60 segundos porque descarga scikit-learn al navegador.

## Quiero subir un CSV propio

Cada notebook tiene un segundo Playground con la opción de subir tu CSV. Necesitas al menos 2 columnas numéricas (y una etiqueta para los modelos de clasificación).
