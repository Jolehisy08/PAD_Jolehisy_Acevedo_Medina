# Análisis de Calidad de Vinos con PCA y Clasificadores Probabilísticos

Este proyecto analiza la calidad del vino portugués "Vinho Verde" usando características fisicoquímicas. El objetivo es comparar el rendimiento de clasificadores probabilísticos con y sin reducción de dimensionalidad mediante PCA, enfrentando desafíos como desbalanceo de clases y colinealidad entre variables.

## 🚀 Características Principales
- Análisis exploratorio de datos (EDA) con distribuciones, estadísticas descriptivas y conteo de clases.
- Unión y etiquetado de datasets de vino tinto y blanco en un solo DataFrame.
- Escalado de características con `StandardScaler` para preparar datos para PCA y clasificación.
- Reducción de dimensionalidad con `PCA` para mejorar la eficiencia del modelo.
- Comparativa de modelos probabilísticos: **Linear Discriminant Analysis (LDA)** y **Gaussian Naive Bayes**.
- Manejo de desbalanceo con **SMOTE** y evaluación mediante validación cruzada, matriz de confusión y accuracy.

## 🧠 Stack Tecnológico
- Python 3.x
- Jupyter Notebook
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- imbalanced-learn (`imblearn`)

## 📂 Estructura del Proyecto
```text
PAD_Jolehisy_Acevedo_Medina/
├── PAD_Script_Jolehisy_Acevedo_Medina.ipynb  # Notebook principal con el análisis completo
├── winequality-red.csv                      # Dataset de vino tinto
├── winequality-white.csv                    # Dataset de vino blanco
├── winequality.names                        # Descripción de las variables del dataset
├── Acceso repositorio GitHub.txt            # Información de acceso al repositorio
├── PDA_JOLEHISY_ACEVEDO_MEDINA_INFORME.pdf  # Informe en PDF
└── README.md                                # Documentación del proyecto
```

## ⚙️ Instalación y Configuración
1. Clona el repositorio:
   ```bash
   git clone <URL-del-repositorio>
   cd PAD_Jolehisy_Acevedo_Medina
   ```
2. Instala Python 3.x si no está instalado.
3. Crea un entorno virtual (recomendado):
   ```bash
   python -m venv venv
   venv\Scripts\activate
   ```
4. Instala las dependencias:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn imblearn jupyter
   ```

## ▶️ Uso / Ejecución
1. Abre Jupyter Notebook desde la carpeta del proyecto:
   ```bash
   jupyter notebook
   ```
2. Abre `PAD_Script_Jolehisy_Acevedo_Medina.ipynb`.
3. Ejecuta las celdas en orden para revisar:
   - carga y unión de datos
   - análisis exploratorio y distribución de variables
   - preprocesamiento y escalado
   - aplicación de PCA
   - entrenamiento y evaluación de LDA y Naive Bayes

## 📈 Resultados Clave
- El dataset combina vino tinto y blanco con una etiqueta `type` que diferencia ambos.
- La variable objetivo es `quality` (puntuación de 3 a 9) y muestra un desbalance fuerte hacia las calidades medias.
- El escalado es crítico debido a la disparidad de magnitudes entre variables como `density` y `total sulfur dioxide`.
- PCA se usa para reducir dimensionalidad y limitar el efecto de la colinealidad.
- El proyecto compara el desempeño de modelos probabilísticos con y sin PCA, comprobando cómo la transformación afecta la capacidad predictiva.

## 💡 Observaciones
- El dataset presenta clases muy desbalanceadas, lo que dificulta la predicción de calidades extremas.
- Para mejorar resultados, se recomienda explorar ensembles, ajuste de umbrales o modelos no lineales con regularización.
