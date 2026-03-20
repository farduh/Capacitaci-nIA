# Workshop: Inteligencia Artificial aplicada a Distribución de Energía

Workshop práctico y orientado al negocio para alinear conceptos de IA y aplicar ML, Deep Learning e IA Generativa a problemas reales de distribución eléctrica. Se prioriza un enfoque claro y accionable con ejemplos y mini-demos, evitando jerga innecesaria.

## Formato

- **Duración:** 4 módulos de ~2 horas cada uno
- **Modalidad:** Presencial o remota
- **Plataforma:** Google Colab (no requiere instalación local)
- **Audiencia:** Equipos de IT/sistemas sin experiencia previa en Python

Alternativas de agenda: 1 jornada intensiva (~8 h), 2 medias jornadas o 4 sesiones semanales.

## Notebooks

Los notebooks están en la carpeta `notebooks/` y están preparados para ejecutarse directamente en Google Colab. Todos usan la misma semilla (`np.random.seed(42)`) para generar datos sintéticos consistentes de demanda energética.

### Módulo 1 — Fundamentos de IA y Regresión

`notebooks/Modulo_1_Fundamentos_IA.ipynb`

Introduce Python de forma práctica para la audiencia. Presenta el panorama IA/ML/DL/GenAI de forma conceptual, explica la anatomía de un modelo (features, target, split) y desarrolla un caso completo de predicción de demanda energética: baseline ingenuo, regresión lineal (y por qué falla con datos en U), feature engineering (`temperatura^2`), y árbol de decisión. Cierra con un teaser de clasificación (detección de anomalías).

### Módulo 2 — Clasificación, Clustering y Ciclo de Vida

`notebooks/Modulo_2_Clasificacion_y_No_Supervisado.ipynb`

Clasificación completa con regresión logística y árbol de decisión, incluyendo métricas (matriz de confusión, precision, recall, F1, curva Precision-Recall) y manejo de datos desbalanceados con `class_weight`. Clustering con K-Means para segmentación de clientes, método del codo y PCA para reducción de dimensionalidad. Cierra con CRISP-DM, una demo de data drift y un checklist para iniciar pilotos.

### Módulo 3 — Modelos Avanzados

`notebooks/Modulo_3_Modelos_Avanzados.ipynb`

Ensembles (Random Forest, XGBoost) comparados contra los baselines del Módulo 1. Deep Learning para series temporales con enfoque de ventanas: red neuronal densa (MLP) y LSTM con Keras. Sección conceptual de Transformers. Aprendizaje por Refuerzo: formulación para energía y demo de Q-Learning para gestión de batería. Incluye guía de decisión "cuándo usar qué".

### Módulo 4 — IA Generativa aplicada a Operaciones

`notebooks/Modulo_4_IA_Generativa.ipynb`

LLMs (tokenización, temperatura, parámetros), embeddings con `sentence-transformers` (heatmap de similitud, búsqueda semántica vs SQL LIKE). RAG completo con ChromaDB usando 8 procedimientos operativos de una distribuidora como base de conocimiento. Copilotos: generador de SQL, generador de Python, extractor de datos de partes de incidentes y clasificador de reclamos por embeddings. Datos sintéticos para eventos raros. Riesgos de GenAI (alucinaciones, privacidad, sesgo, human-in-the-loop). Cierra con un template para diseñar pilotos de IA.

## Contenido por módulo

| Módulo | Temas | Duración |
|--------|-------|----------|
| 1 | Panorama IA/ML/DL/GenAI, conceptos base, regresión, teaser clasificación | ~2 h |
| 2 | Clasificación, métricas, K-Means, PCA, CRISP-DM, data drift | ~2 h |
| 3 | Random Forest, XGBoost, LSTM, Transformers (conceptual), Q-Learning | ~2 h |
| 4 | LLMs, embeddings, RAG, copilotos, datos sintéticos, riesgos GenAI | ~2 h |


## Requisitos previos

- Navegador web actualizado
- No se requiere instalación de software local
- Las dependencias adicionales (`xgboost`, `sentence-transformers`, `chromadb`, etc.) se instalan desde los propios notebooks

## Cómo ejecutar los notebooks

### Opción 1: Google Colab (recomendada)

La forma más simple. Solo necesitás una cuenta de Google.

1. Descargar el archivo `.ipynb` que quieras ejecutar (desde Teams o desde este repositorio).
2. Ir a [https://colab.research.google.com](https://colab.research.google.com).
3. Click en **Archivo > Subir notebook** (o en la pestaña **Subir** del diálogo inicial).
4. Seleccionar el archivo `.ipynb` descargado.
5. Ejecutar las celdas con **Shift + Enter**.

### Opción 2: Binder

Permite ejecutar los notebooks sin instalar nada, directamente desde un repositorio de GitHub público.

> **Nota:** Esta opción solo funciona si el repositorio es público en GitHub. Si no tenés acceso al repositorio público, usá la Opción 1.
