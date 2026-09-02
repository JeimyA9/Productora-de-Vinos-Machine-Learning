# Caso productora de vinos


## Objetivo

Una empresa productora de vinos desea automatizar la evaluación de calidad de sus productos utilizando técnicas de Machine Learning.
Para ello dispone de un conjunto de datos con propiedades físicoquímicas de distintas muestras de vino y una calificación de calidad 
otorgada por expertos. Antes de entrenar modelos predictivos es necesario analizar cómo 
afectan las transformaciones y escalados de datos al rendimiento de los algoritmos

## Enfoque Técnico

- **Exploración de datos:** verificación de cantidad de registros, minimos, maximos, media, desviación
- **Visualización:** visualización de los cambios despues de aplicar diferentes tipos de estandarización
- **Normalización y Estandarización:** MinMaxScaler() y StandardScaler().
- **Clasificación con KNN y SVM:** Entrenamiento

## Tecnologías

- Python
- sklearn.preprocessing
- pandas / numpy
- matplotlib 
- sklearn.metrics
- sklearn.neighbors / sklearn.svm

## Resultados

Tanto para KNN como para SVM el escalado es crucial y mejora significativamente el rendimiento del modelo en comparacion con otras tecnicas o datos originales. Pero el problema estructural persiste: ambos modelos son incapaces de detectar las clases 0, 1, 4 y 5 por el severo desbalance de clases — mejorar el accuracy general no resuelve ese problema de fondo, que necesitaría técnicas específicas de balanceo

## Estructura del Repositorio

```
├── data/                  # Dataset 
├── notebooks/             # Análisis exploratorio y modelado
└── README.md
```

## Cómo ejecutar

```bash
pip install -r requirements.txt
jupyter notebook notebooks/prodVinos.ipynb
```

##  Dataset

[Real Market Data for Association Rules](https://www.kaggle.com/datasets/rukenmissonnier/real-market-data)
