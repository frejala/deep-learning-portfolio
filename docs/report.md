# Portfolio de Deep Learning

**Autor:** Fabrizio Rejala  
**Fecha:** 5 de octubre, 2025

---

## Resumen Ejecutivo

Durante este curso me metí de lleno en el mundo del deep learning y desarrollé 9 proyectos que cubren desde lo básico hasta temas más avanzados. Empecé con una red neuronal densa clásica para clasificar perros y gatos usando CIFAR-10, luego exploré autoencoders con MNIST para entender cómo comprimir y reconstruir datos. Me adentré en el procesamiento de secuencias con RNNs simples y bidireccionales, después implementé un traductor de frases inglés-español usando arquitecturas sequence-to-sequence. Para la parte más moderna, trabajé con modelos preentrenados de Transformers para detectar emociones y estimar edades, implementé sistemas RAG (Retrieval-Augmented Generation) para transcripciones de YouTube y generación de SQL, y finalmente exploré modelos generativos como VAEs y GANs para crear imágenes. Cada proyecto me permitió entender diferentes aspectos del deep learning, desde la clasificación básica hasta la generación de contenido y sistemas de recuperación de información.

---

## Problemas y Datasets

### 1. Clasificación DNN (Perros vs Gatos)

**Problema:** Clasificación binaria de imágenes para distinguir entre perros y gatos  
**Dataset:** CIFAR-10 (filtrado para clases 3 y 5), 32x32 píxeles RGB

### 2. Autoencoder SAE

**Problema:** Compresión y reconstrucción de dígitos manuscritos  
**Dataset:** MNIST, 28x28 píxeles en escala de grises

### 3. RNN Simple

**Problema:** Procesamiento de secuencias básico  
**Dataset:** Datos sintéticos para demostrar capacidades de memoria temporal

### 4. RNN Bidireccional

**Problema:** Análisis de secuencias con contexto pasado y futuro  
**Dataset:** Secuencias con patrones que requieren contexto bidireccional

### 5. Traducción Sequence-to-Sequence

**Problema:** Traducción de textos en inglés al español  
**Dataset:** Corpus de frases paralelas spa-eng.zip de TensorFlow

### 6. IA Generativa (Detección de Emociones/Edad)

**Problema:** Análisis de rostros para detectar emociones y estimar edad  
**Dataset:** Modelos preentrenados de HuggingFace (dima806/facial_emotions_image_detection, Robys01/facial_age_estimator)

### 7. RAG con Transcripciones de YouTube

**Problema:** Sistema de Q&A sobre contenido de videos de YouTube  
**Dataset:** Transcripciones automáticas de videos usando YouTube Transcript API

### 8. RAG para Generación de SQL

**Problema:** Generación automática de consultas SQL basadas en preguntas en lenguaje natural  
**Dataset:** Esquemas de bases de datos y consultas de ejemplo

### 9. VAE y GANs

**Problema:** Generación de imágenes sintéticas  
**Dataset:** Facades dataset (arquitectura) para transformación imagen-a-imagen

---

## Metodología por Módulo

### 1. DNN Clasificación

**Arquitectura:** Red neuronal densa multicapa con capas fully-connected  
**Hiperparámetros clave:** Learning rate adaptativo, dropout para regularización, early stopping  
**Recursos:** CPU/GPU básico, TensorFlow/Keras

### 2. Autoencoder SAE

**Arquitectura:** Encoder (784→512→256→128→64) + Decoder (64→128→256→512→784)  
**Hiperparámetros clave:** Dimensión del cuello de botella (64), función de pérdida MSE  
**Recursos:** Entrenamiento rápido en CPU, visualización de reconstrucciones

### 3. RNN Simple

**Arquitectura:** Capas LSTM/GRU básicas para procesamiento secuencial  
**Hiperparámetros clave:** Unidades ocultas, longitud de secuencia, dropout temporal  
**Recursos:** GPU recomendada para secuencias largas

### 4. RNN Bidireccional

**Arquitectura:** Bidirectional LSTM que procesa secuencias en ambas direcciones  
**Hiperparámetros clave:** Número de unidades LSTM, merge_mode para combinar direcciones  
**Recursos:** Mayor costo computacional que RNN unidireccional

### 5. Traducción Seq2Seq

**Arquitectura:** Encoder-Decoder con attention mechanism  
**Hiperparámetros clave:** Dimensiones de embedding, tamaño de vocabulario, beam search  
**Recursos:** GPU necesaria, dataset de ~100k pares de frases

### 6. IA Generativa

**Arquitectura:** Modelos Transformer preentrenados (fine-tuning)  
**Hiperparámetros clave:** Threshold de confianza, procesamiento de imágenes  
**Recursos:** Modelos HuggingFace, inferencia en tiempo real

### 7. RAG YouTube

**Arquitectura:** Embeddings (all-minilm) + ChromaDB + LLaMA3 local  
**Hiperparámetros clave:** Chunk size para splitting, top-k retrieval  
**Recursos:** Ollama local, vectorstore persistente

### 8. RAG SQL

**Arquitectura:** Similar a RAG YouTube pero especializado en esquemas SQL  
**Hiperparámetros clave:** Prompts específicos para SQL, validación de sintaxis  
**Recursos:** Base de conocimiento de esquemas SQL

### 9. VAE y GANs

**Arquitectura:** Variational Autoencoder + Generative Adversarial Networks  
**Hiperparámetros clave:** Learning rates diferenciados (G vs D), beta para VAE  
**Recursos:** GPU intensiva, dataset de imágenes de fachadas

---

## Lecciones Aprendidas y Trabajo Futuro

### Lo que aprendí

- **Progresión natural:** Empezar con modelos simples (DNN) me ayudó a entender los fundamentos antes de saltar a arquitecturas complejas
- **La importancia del preprocesamiento:** Normalización, tokenización y augmentación de datos marcan una diferencia huge en el rendimiento
- **Trade-offs everywhere:** Más complejidad no siempre significa mejores resultados; a veces un modelo simple y bien tunneado supera a uno complejo mal configurado
- **RAGs son el futuro:** Los sistemas de recuperación aumentada permiten crear aplicaciones súper útiles sin entrenar modelos desde cero
- **Transfer learning es oro:** Usar modelos preentrenados te ahorra tiempo y recursos

### Retos que enfrenté

- **Overfitting constante:** Aprendí a usar dropout, early stopping y data augmentation
- **Recursos computacionales:** GANs y VAEs requieren paciencia y una buena GPU
- **Debugging de modelos:** Cuando algo no funciona, hay mil cosas que pueden estar mal

### Trabajo futuro

- **Expandir RAGs:** Implementar sistemas multi-modal que trabajen con texto, imágenes y audio
- **Optimización:** Experimentar con pruning, quantization y destilación de modelos para deployment
- **MLOps:** Integrar pipelines de CI/CD para modelos en producción
- **Ethical AI:** Añadir métricas de fairness y bias detection a los modelos
- **Edge deployment:** Adaptar modelos para correr en dispositivos móviles y IoT
