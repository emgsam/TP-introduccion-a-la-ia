# ¿Qué artículos se venden juntos?

**Detección de ventas perdidas y armado de combos en un mayorista de construcción en seco**

Trabajo Final Integrador · Introducción a la Inteligencia Artificial
Diplomatura de Posgrado en IA Generativa (UNLu) · 2026

## Descripción

Se analizan facturas de venta reales (anonimizadas) de un mayorista de construcción en seco, de octubre de 2024 a septiembre de 2026, para descubrir qué artículos se compran juntos. El trabajo tiene cuatro objetivos:

1. **Predicción de accesorios acompañantes:** clasificación binaria (árbol de decisión, regresión logística, Random Forest, entre otros) para saber si una compra incluye cada accesorio.
2. **Detección de ventas perdidas:** se usa el modelo para marcar compras en las que el cliente probablemente necesitaba un accesorio y no lo llevó.
3. **Segmentación de clientes y combos:** aprendizaje no supervisado (k-means) para definir perfiles de compra y proponer combos.
4. **Estimación de cantidades (exploratorio):** regresión para estimar cuántos perfiles acompañan a una cantidad de placas.

El notebook también incluye el diseño de la puesta en producción, una reflexión crítica y el análisis ético.

## Estructura

```
.
├── TF_ventas_juntas.ipynb   # Notebook con todo el trabajo
└── datos/
    ├── Export_seco_anonimizado.xlsx   # Líneas de factura (anonimizadas)
    ├── familias.xlsx
    ├── productos.xlsx
    ├── rubros.xlsx
    └── unidades.xlsx
```

## Cómo ejecutarlo

1. Cloná el repositorio y abrí `TF_ventas_juntas.ipynb` en Jupyter o Google Colab.
2. Verificá que la carpeta `datos/` esté junto al notebook (en Colab, subí los archivos desde el panel lateral).
3. Ejecutá las celdas en orden. La primera instala `python-calamine`, el lector de Excel que usa el notebook.

Librerías principales: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`.
