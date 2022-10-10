# ModelosDiagnosticoCancerMama
Proyecto Final de modelos de aprendizaje. 

Problema

Los médicos han extraído características y las han anotado, su trabajo es crear un modelo capaz de identificar si un paciente tiene o no cáncer. 
Recordemos que un falso positivo no es tan preocupante como un falso negarivo, ya que en el futuro se le hacen 


Conclusiones
Codificamos el diagnóstico donde 1 es Maligno 0 es Benigno

Se han probado 4 tipos de modelos:

- Gradiente descendente estocástica

- Árbol de decisión

- Vecinos cercanos

- Random Forest

Dada la primicia que un falso negativo es mucho más preocupante y de acuerdo a los resultados de la matriz de confusión tanto en training como en test, concluyo que el mejor modelo para este caso es el de Vecínos cercanos ya que en ambos resultados presenta un porcentaje de precisión alto 97% y 95% respectivamente, y lo mejor es que prediciendo resultados benignos (0) tiene un 100% tanto en training como en test.
