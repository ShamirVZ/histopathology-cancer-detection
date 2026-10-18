# Histopathologic Cancer Detection — Deep Learning

Proyecto **académico grupal** de clasificación binaria de imágenes histopatológicas (presencia o ausencia de tejido tumoral) basado en el conjunto de datos [Histopathologic Cancer Detection de Kaggle](https://www.kaggle.com/competitions/histopathologic-cancer-detection).

> **Aviso:** Proyecto exclusivamente educativo. No es un dispositivo médico, no está validado clínicamente y no debe utilizarse para diagnóstico ni decisiones sobre pacientes.

## Objetivo y metodología

El notebook compara tres arquitecturas:
- **CNN Base**, como modelo convolucional de referencia.
- **EfficientNetB0**, utilizando transferencia de aprendizaje.
- **MLP-Mixer**, basada en parches de imagen y redes densas.

El flujo incluye exploración de datos, preparación de imágenes, partición estratificada de entrenamiento/validación/test interno, conversión a tensores, entrenamiento, curvas de aprendizaje y evaluación mediante accuracy, precision, recall, F1 y AUC-ROC. El umbral de clasificación se selecciona con validación y después se evalúa en test interno.

## Tecnologías

Python · TensorFlow / Keras · NumPy · Pandas · Pillow · scikit-learn · Matplotlib · Google Colab.

## Ejecución

1. Obtén el dataset desde Kaggle y respeta sus condiciones de uso.
2. Abre el notebook en **Google Colab** e instala las dependencias indicadas en `requirements.txt`.
3. Coloca el archivo ZIP de datos en Google Drive y **adapta las variables `zip_drive` y `BASE_DIR`** a tus carpetas (celda *PASO 2*). La ruta de salida `output_dir` también debe configurarse antes de guardar resultados.
4. Ejecuta las celdas en orden. El entrenamiento puede requerir GPU y bastante tiempo. Los resultados dependen del entorno y de los datos utilizados.

**Nota de reproducibilidad:** este repositorio documenta el trabajo académico original; no garantiza ejecución automática ni resultados idénticos en cualquier entorno.

## Resultados y limitaciones

El notebook contiene comparación de modelos, curvas de entrenamiento y evaluación interna. Las métricas obtenidas en una muestra interna **no representan precisión clínica**, no equivalen a validación externa y no deben extrapolarse a hospitales o pacientes.

## Autoría

**Trabajo académico realizado en equipo.** Los modelos, experimentos y resultados describen el alcance del trabajo grupal; no son una atribución individual de toda la implementación. Shamir Vargas participó en la preparación de datos.

## Contenido

- `notebooks/`: notebook del proyecto (por añadir).
- `requirements.txt`: bibliotecas principales.
- `.gitignore`: exclusiones de datasets, modelos y archivos locales.

Los datos de Kaggle y los pesos entrenados no se incluyen en el repositorio.
