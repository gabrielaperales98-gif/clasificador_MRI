### clasificador_MRI


# Clasificación de imágenes de resonancia magnética con CNN–LSTM

Este proyecto académico explora cómo usar la visión artificial para distinguir entre imágenes de resonancia magnética que ya tienen una región delimitada y aquellas que están sin segmentar.

**[Ver el cuaderno del proyecto](./Clasificador_MRI_Colab.ipynb)**

## Cómo funciona

Las imágenes se convierten a escala de grises y se ajustan a un tamaño de 128 × 128 píxeles. La red convolucional (CNN) extrae características visuales y una LSTM bidireccional procesa esas características por filas. A partir de ellas, el modelo asigna la imagen a una de las dos clases.

El cuaderno separa los datos en conjuntos de entrenamiento, validación y prueba. La validación se usa para elegir el mejor modelo y la prueba se reserva para la evaluación final. El cuaderno genera un reporte de clasificación, una matriz de confusión y una curva ROC.

## Cómo probarlo en Google Colab

1. Descarga `Clasificador_MRI_Colab.ipynb` y ábrelo en Google Colab.
2. Sube tus imágenes a `/content/datos` o cambia la ruta `DATA_DIR` en el cuaderno.
3. Ajusta `FOLDERS` a los nombres de tus carpetas y verifica qué etiqueta corresponde a cada clase.
4. Ejecuta las celdas en orden. Para comprobar el flujo con una ejecución corta, cambia `EPOCHS` a `1`.

## Alcance del proyecto

El modelo clasifica las imágenes según su estado de segmentación. Una línea de trabajo que me interesa explorar es cómo la visión artificial podría ayudar a los especialistas a delimitar lesiones y comparar sus cambios entre estudios.

Queda pendiente verificar los resultados con el conjunto de datos original. Si varias imágenes provienen de un mismo paciente o estudio, deben quedar juntas en un solo conjunto para que la evaluación sea independiente.

## Herramientas

Python · OpenCV · NumPy · TensorFlow/Keras · scikit-learn · Matplotlib
```
