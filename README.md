# Análisis de Espectros de Absorbancia y Ajuste de Datos Experimentales

Este proyecto realiza el análisis de espectros de absorbancia de varios óxidos de manganeso utilizando Python. A través de este análisis, se comparan las intensidades medidas con las predicciones teóricas, ajustando los datos experimentales a un modelo lineal para obtener el número de oxidación de los compuestos.

## Contenido del Proyecto

1. **Lectura y preparación de datos experimentales**: Carga de archivos `.dat` con datos experimentales y preprocesamiento de los datos, incluida la normalización y ajuste de las intensidades.
2. **Ajuste de modelo**: Uso de un modelo lineal para ajustar los bordes de absorción y calcular el número de oxidación de los compuestos.
3. **Visualización de los datos**: Creación de gráficos que muestran las intensidades de absorbancia frente a la energía, y ajuste de curvas para los diferentes compuestos.
4. **Cálculo de incertidumbres**: Estimación de los errores en el ajuste del modelo utilizando las covarianzas calculadas por `curve_fit`.

## Requerimientos

Para ejecutar este proyecto, necesitas tener instaladas las siguientes bibliotecas de Python:

- `pandas`: Para la manipulación de datos.
- `numpy`: Para operaciones matemáticas.
- `matplotlib`: Para la visualización de datos.
- `scipy`: Para el ajuste de curvas y el cálculo de modelos.

Puedes instalar las dependencias con el siguiente comando:

```bash
pip install pandas numpy matplotlib scipy
```

## Descripción del Proceso

### Carga y Preprocesamiento de los Datos

El proyecto comienza con la carga de los archivos de datos `.dat`, los cuales contienen información sobre la energía y la intensidad de absorbancia para cada compuesto. Luego se realiza un preprocesamiento en el cual se normalizan las intensidades de absorbancia, y se calculan las relaciones entre las intensidades medidas y las intensidades iniciales.

### Ajuste de Curvas

Para cada conjunto de datos, se realiza un ajuste lineal de los bordes de absorción utilizando el método de mínimos cuadrados de `scipy.optimize.curve_fit`. Esto permite obtener el número de oxidación de cada compuesto, además de calcular los errores en el ajuste.

### Visualización

El análisis se presenta a través de gráficos que muestran las intensidades de absorbancia en función de la energía. Los gráficos se generan con `matplotlib` y se guardan como imágenes PNG.

## Contribuciones

Las contribuciones son bienvenidas. Si deseas mejorar este proyecto o agregar nuevas funcionalidades, siéntete libre de abrir un `issue` o enviar un `pull request`. Aquí hay algunas formas en las que puedes contribuir:

1. **Informar Bugs**: Si encuentras un error o algo que no funciona como se espera, abre un `issue` para que pueda investigarse.
2. **Mejoras**: Si tienes ideas para mejorar el rendimiento, la visualización o cualquier otra parte del proyecto, puedes hacer un `fork` del repositorio y enviar un `pull request` con los cambios propuestos.
3. **Documentación**: Si encuentras algo en la documentación que no está claro o que puede mejorarse, puedes hacer un `pull request` con tus sugerencias.
