# Proyecto de Algoritmos Genéticos y Redes Neuronales  

Este repositorio contiene tres ejercicios principales donde se aplican *algoritmos genéticos* y técnicas de optimización en Machine Learning usando el dataset breast_cancer.csv. Cada ejercicio aborda un enfoque distinto:  

1. *Selección de características (Feature Selection)*  
2. *Optimización de hiperparámetros (Hyperparameter Optimization)*  
3. *Neuroevolution (Evolución de arquitecturas de redes neuronales)*  

---

## Ejercicio 1: Selección de Características (Feature Selection)  

### Descripción  
Se utilizó un *algoritmo genético* para seleccionar automáticamente las mejores características (variables) que optimizan el rendimiento de un modelo de clasificación basado en *Random Forest*.  

### Proceso  
- Se representó cada subconjunto de variables como un individuo (vector binario de 0 y 1).  
- El algoritmo genético evaluó la *precisión* de cada subconjunto entrenando el modelo.  
- Se aplicaron operadores evolutivos:  
  - *Selección* de los mejores individuos.  
  - *Cruzamiento* entre subconjuntos.  
  - *Mutación* de características.  
- Iteración durante varias generaciones para mejorar la calidad de las soluciones.  

### Resultados  
- El algoritmo se ejecutó durante *8 generaciones*.  
- Mejor precisión encontrada: *98.31% (generación 6)*.  
- Subconjunto óptimo de características seleccionadas:  
  - radius_mean  
  - concave points_se  
  - perimeter_worst  
  - smoothness_worst  

Se redujeron las variables de *30 a 4* manteniendo una precisión muy alta en la detección de cáncer de mama.  

---

## Ejercicio 2: Optimización de Hiperparámetros (Hyperparameter Optimization)  

### Descripción  
Se aplicó un *algoritmo genético* para optimizar los hiperparámetros *C* y *gamma* de un modelo *SVM (Support Vector Machine)*.  

### Proceso  
- Cada individuo representó una combinación de valores de *C* y *gamma*.  
- La aptitud de cada individuo fue medida con *validación cruzada*.  
- Se aplicaron operadores de selección, cruzamiento y mutación.  
- Se ejecutó el proceso durante varias generaciones para encontrar la mejor configuración.  

### Resultados  
- El algoritmo se ejecutó durante *20 generaciones*.  
- Mejor configuración encontrada:  
  - *C = 8.9973*  
  - *gamma = 0.0129*  
- Precisión en validación cruzada: *0.9807*  
- Precisión en conjunto de prueba: *0.9825*  

El algoritmo genético logró optimizar los hiperparámetros sin necesidad de *GridSearch*, mejorando la eficiencia del proceso.  

---

## Ejercicio 3: Neuroevolution (Evolución de Redes Neuronales)  

### Descripción  
Se utilizó el enfoque de *Neuroevolution, aplicando un algoritmo genético para encontrar automáticamente la mejor arquitectura de una **red neuronal* para clasificar cáncer de mama.  

### Proceso  
- Cada individuo representó una arquitectura de red:  
  - Número de capas ocultas.  
  - Neuronas por capa.  
  - Función de activación.  
  - Tasa de aprendizaje.  
  - Dropout.  
  - Batch size y épocas.  
- Evaluación mediante precisión en validación.  
- Aplicación de selección, cruzamiento y mutación en cada generación.  
- Reentrenamiento final con los mejores hiperparámetros.  

### Resultados  
- El algoritmo se ejecutó durante *12 generaciones*.  
- Mejor arquitectura encontrada:  
  - 2 capas ocultas con *256 y 32 neuronas*.  
  - Función de activación: *tanh*.  
  - Dropout = 0.2.  
  - Learning rate = 0.001.  
  - Batch size = 64.  
- Precisión en conjunto de prueba: *94.18%*.  
- F1-score = *0.94* (alto equilibrio entre sensibilidad y especificidad).  

El uso de algoritmos genéticos permitió optimizar automáticamente la arquitectura, evitando la prueba y error manual.  

---

## Conclusión General  

Los tres ejercicios muestran cómo los *algoritmos genéticos* son herramientas poderosas en el aprendizaje automático:  

- Permiten *reducir la complejidad* de los modelos (selección de características).  
- Encuentran *configuraciones óptimas* de hiperparámetros.  
- Optimizan automáticamente *arquitecturas de redes neuronales*.  

Estos enfoques combinan técnicas evolutivas con modelos de Machine Learning, logrando soluciones más eficientes y de alto rendimiento en la clasificación de cáncer de mama.  

---