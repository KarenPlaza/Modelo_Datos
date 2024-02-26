Descripción del dataset personalizado:
Se eliminaron los vacios, la columna Diagnosis se transforma el dato M(malo) y B(bueno) en 1 y 0.
1.Preparación deldataset:
La visión general inicial del dataset nos permite mostrando las primeras filas, información sobre los tipos de datos y características, estadísticas descriptivas y el conteo de muestras por etiqueta. Esto nos ayudará a entender mejor la estructura de los datos y comenzar a identificar posibles desafíos, como desbalance de clases o características faltantes.

Preprocesa el dataset para manejar valores nulos o inconsistentes:
Aplica técnicas de reducción de dimensionalidad:
Una de las aplicaciones de PCA es la reducción de dimensionalidad (variables), perdiendo la menor cantidad de información (varianza) posible: cuando contamos con un gran número de variables cuantitativas posiblemente correlacionadas (indicativo de existencia de información redundante), PCA permite reducirlas a un número menor de variables transformadas (componentes principales) que expliquen gran parte de la variabilidad en los datos. Este código aplica PCA para reducir la dimensionalidad de los datos a 100 componentes principales y devuelve el conjunto de datos transformado en función de estos componentes.

Selección de técnicas de aprendizaje automático
Random Forest : es un algoritmo de conjunto que combina múltiples árboles de decisión para realizar la clasificación. Es robusto, puede manejar grandes conjuntos de datos y es menos propenso al sobreajuste.
Gradient Boosting: es una técnica de aprendizaje automático que se utiliza para resolver problemas de regresión y clasificación, construye un modelo predictivo fuerte combinando múltiples modelos de aprendizaje débil, como árboles de decisión poco profundos, de manera secuencial.

Entrenamiento del modelo
Implementa las técnicas de aprendizaje automático elegidas:
Inicialización del modelo Random Forest, se define la cuadrícula de hiperparámetros a ajustar y se inicialización de GridSearchCV para búsqueda de hiperparámetros
Lo que hemos realizado es definir una cuadrícula de hiperparámetros que queremos ajustar utilizando GridSearchCV. Este método realiza una búsqueda exhaustiva sobre una cuadrícula de valores de hiperparámetros dados y evalúa el rendimiento del modelo utilizando la validación cruzada. Una vez que GridSearchCV ha encontrado los mejores hiperparámetros, los utilizamos para entrenar el modelo en todo el conjunto de entrenamiento.

Entrena el modelo utilizando el conjunto de entrenamiento:
Se corre el modelo, se pptimiza los hiperparámetros del modelo para obtener la mejor precisión posible, considerando el desbalance de clases y se mejora precisión obtenida durante la búsqueda de hiperparámetros dando como resultado durante la búsqueda de hiperparámetros un aproximadamente 0.996.

AUC-ROC (Random Forest): 0.9974358974358973
AUC-ROC (XGBoost): 1.0
