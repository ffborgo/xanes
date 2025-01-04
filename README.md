# Determinación del Estado de Oxidación de un Óxido Desconocido

Este proyecto utiliza un análisis de espectros de absorbancia K de óxidos de manganeso para determinar el estado de oxidación de un óxido desconocido. El proceso se basa en un ajuste lineal de los datos experimentales y su extrapolación para estimar el número de oxidación, implementado mediante Python.

## Contenido del Proyecto

1. **Lectura y Preprocesamiento de Datos**: Carga de archivos de datos experimentales y su preparación para el análisis (normalización y limpieza de datos).
2. **Ajuste Lineal**: Implementación de un modelo de regresión lineal para ajustar los bordes de absorción K y calcular los estados de oxidación.
3. **Extrapolación**: Uso de la recta ajustada para determinar el estado de oxidación del óxido desconocido.
4. **Visualización de Resultados**: Generación de gráficos de absorbancia frente a energía con las curvas ajustadas.
5. **Cálculo de Incertidumbres**: Estimación de errores en los ajustes utilizando las covarianzas obtenidas por `curve_fit`.

## Requerimientos

Para ejecutar este proyecto, necesitas tener instaladas las siguientes bibliotecas de Python:

- `pandas`: Para la manipulación de datos.
- `numpy`: Para operaciones matemáticas.
- `matplotlib`: Para la visualización de datos.
- `scipy`: Para el ajuste de curvas y cálculos relacionados.

Puedes instalar las dependencias con el siguiente comando:

```bash
pip install pandas numpy matplotlib scipy
```

## Descripción del Proceso

### Carga y Preprocesamiento de los Datos

El proyecto comienza con la carga de los archivos de datos `.dat` que contienen las intensidades de absorbancia K y las energías correspondientes para los óxidos de manganeso. Después, se realiza un preprocesamiento para normalizar las intensidades y preparar los datos para el ajuste.

### Ajuste Lineal y Extrapolación

Se aplica un modelo de regresión lineal utilizando `scipy.optimize.curve_fit` para ajustar los bordes de absorción K de los óxidos de manganeso. La recta ajustada se utiliza para extrapolar el estado de oxidación del óxido desconocido.

### Visualización

Los resultados se muestran mediante gráficos de absorbancia frente a energía, con las rectas ajustadas superpuestas. Los gráficos se generan utilizando `matplotlib` y se guardan como imágenes PNG. Un ejemplo es la siguiente:

<img src="https://github.com/ffborgo/xanes/blob/main/grafico.png" alt="Gráfico final" style="width: 60%; max-width: 500px;">

## Contribuciones y uso

Las contribuciones son bienvenidas. Si deseas mejorar este proyecto, por favor crea una nueva rama y sentite libre de modificarlo a tu gusto.

## Referencias

Los datos utilizados en este análisis fueron tomados del experimento realizado en el curso "Experimentos Cuanticos II" de la UNLP.
