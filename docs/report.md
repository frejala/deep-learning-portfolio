# Deep Learning

**Autor:** Fabrizio Rejala

**Fecha:** 2025-09-05

A continuación se enumeran las técnicas y modelos de entrenamiento disponibles en el repositorio.

## 01 DNN Classification

**Caso de uso**: Clasificación entre perros y gatos a partir de imágenes.

**Objetivo**: En este proyecto se utilizó una _DNN_, con el objetivo de clasificar imágenes entre perros y gatos. El modelo aprende características relevantes delimitadas por los pixeles para distinguir entre perros y gatos.

**Dataset**: [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html).

## 02 SAE Autoencoder

**Caso de uso**: Compresión y reconstrucción de dígitos manuscritos.

**Objetivo**: En este proyecto se utilizó un _SAE_, con el objetivo de comprimir y reconstruir imágenes de dígitos manuscritos.

**Dataset**: [MNIST](https://www.tensorflow.org/datasets/catalog/mnist).

## 03 Simple RNN

**Caso de uso**: Predicción de temperaturas.

**Objetivo**: En este proyecto se utilizó una _Simple RNN_ para modelar series temporales de temperaturas. El objetivo fue predecir valores futuros a partir de datos históricos, aprovechando la capacidad de las RNN para capturar dependencias secuenciales en el tiempo.

**Dataset:** Temperaturas de [Historical Hourly Weather Data](https://www.kaggle.com/datasets/selfishgene/historical-hourly-weather-data).

## 04 Bidirectional RNN

**Caso de uso**: Analisis de sentimientos de las reseñas hechas en IMDB.

**Objetivo**: Es este proyecto se utilizó una _Bidirectional RNN_ para el análisis de sentimientos en reseñas de películas de IMDB. El objetivo fue procesar las reseñas hechas en IMDB para construir un modelo que pueda tener un entendimiento más completo del contexto para clasificar las reseñas como positivas o negativas.

**Dataset:** [IMDB movie review](https://keras.io/api/datasets/imdb/) de Keras.

## 05 Seq2Seq

**Caso de uso**: Traducciónes de textos en ingles al español.

**Objetivo**: En este proyecto se utilizó un _Seq2Seq_, con el objetivo de traducir oraciones del inglés al español. El modelo aplica una arquitectura encoder y decoder, donde el encoder comprime la oración original en un vector de contexto y el decoder genera la traducción.

**Dataset**: [English-to-Spanish translation dataset provided by Anki](https://www.manythings.org/anki/spa-eng.zip).

## 06 Generative AI

**Caso de uso**: Análisis de sentimientos de imágenes obtenidas usando la webcam.

**Objetivo**: En este proyecto se utilizó _Generative AI_, con el objetivo de analizar sentimientos en imágenes capturadas con la webcam.

**Dataset:** Modelos preentrenados de HuggingFace (dima806/facial_emotions_image_detection, Robys01/facial_age_estimator)

## 07 RAG Transcription

**Caso de uso**: Realizar preguntas y respuestas utilizando la transcripción de un video de Youtube.

**Objetivo**: En este proyecto se utilizó un _RAG_, con el objetivo de responder preguntas a partir de la transcripción de un video de YouTube, combinando técnicas de recuperación de información con generación de texto, lo que permite buscar fragmentos relevantes en la transcripción y generar respuestas.

## 08 RAG SQL

**Caso de uso**: Generación automática de consultas SQL basadas en preguntas en lenguaje natural .

**Objetivo**: En este proyecto se utilizó un modelo de _RAG_, con el objetivo de transformar preguntas en lenguaje natural en consultas SQL automáticas.

## 09 VAEs y GANs

**Caso de uso**: Generación de estructuras de edificios usando como estructuras existentes como entrenamiento.

**Objetivo**: En este proyecto se utilizaron _VAEs_ y _GANs_, con el objetivo de generar nuevas estructuras de edificios a partir de ejemplos de entrenamiento. El modelo aprendió patrones de diseño y fue capaz de producir esbozos de estructuras.

**Dataset:** [Facades dataset](https://efrosgans.eecs.berkeley.edu/pix2pix/datasets/facades.tar.gz)

## Trabajos Futuros

1. Extender las GANs y VAEs para generación en entornos 3D.
1. Optimización y Despliegue en Producción
   Implementación de pipelines CI/CD para el despliegue en producción.
1. Estudio de sesgos en datasets y modelos, proponiendo técnicas de mitigación y buenas prácticas en el desarrollo
