# ModelosDiagnosticoCancerMama
Proyecto Final de modelos de aprendizaje. 

## Problema

Los médicos han extraído características y las han anotado, su trabajo es crear un modelo capaz de identificar si un paciente tiene o no cáncer. 
Recordemos que un falso positivo no es tan preocupante como un falso negativo, ya que en el futuro se le hacen más pruebas a las pacientes y hay oportunidades de descubrir que estábamos en un error. 
Sin embargo un falso negarivo puede llevar a que el cáncer se desarrolle sin supervisiòn durante más tiempo del necesario y podría llevar a daños más graves o incluso la muerte de la paciente. 

## Objetivos

  -Desarrollar un modelo que funcione lo mejor posible ante el problema planteado. 
  -Realizar al menos tres diferente modelos

## Desarrollo

Primero descargamos el dataset de la carpeta data, el archivo se llama "data.csv".
Importamos todas las librerias que vamos a utilizar

![image](https://user-images.githubusercontent.com/24902098/194795035-07f90c1d-7897-4c9b-a9d5-b2203e25f345.png)

Cargamos nuestro dataset en un dataframe con pandas.

![image](https://user-images.githubusercontent.com/24902098/194795085-a4ffbe15-915e-4461-8047-d721cbb0a7f2.png)

Con lo que observamos que contiene 569 filas y 32 columnas.
Luego de esto procedemos a realizar el tratamiento de datos por lo que verificamos si alguna columna tiene nulos.
![image](https://user-images.githubusercontent.com/24902098/194795190-8b874ce6-733f-4813-ad0d-f37111b28e1c.png)

Después verificamos si existen valores duplicados.

![image](https://user-images.githubusercontent.com/24902098/194795346-dbe37a7b-017d-42b3-8b76-b88e0f86e82f.png)

Como no existen, despues de eso vemos algunas gráficas para entender mejor los datos.
Y después de esto extraemos nuestros datos tanto de X como de Y, donde X son todas las columnas menos "id" y "diagnosis", mientras Y es solo la columna "diagnosis"

![image](https://user-images.githubusercontent.com/24902098/194795623-29a818b6-df92-4d55-b7a9-663a273770be.png)

Como Y tiene una respuesta de M para maligno y B para benigno, la codificamos de la siguiente forma para que quede en: 
  -1 Maligno 
  -0 Benigno
  
  ![image](https://user-images.githubusercontent.com/24902098/194795700-17346989-5e70-4483-b062-2978e97b7f13.png)

Acabado este proceso procedemos a obtener nuestros conjuntos de entrenamiento y de testing.

![image](https://user-images.githubusercontent.com/24902098/194795735-ef8cc20f-aab2-47d6-aa35-5a7a82a805a1.png)

Y por último antes de empezar a entrenar nuestros modelos, realizamos un escalamiento para estandarizar nuestras escalas en todas las columnas de los conjuntos de X.

![image](https://user-images.githubusercontent.com/24902098/194795819-f17d6019-6789-454b-af1e-20cef2d0e031.png)

Acabado el tratamiento de datos, ahora si procedemos a probar con 4 diferentes modelos. 

- Gradiente descendente estocástica
![image](https://user-images.githubusercontent.com/24902098/194795891-49430560-f23f-4eb6-8d5b-d4e85ccdca08.png)


- Árbol de decisión

![image](https://user-images.githubusercontent.com/24902098/194795918-56c37e21-10ac-4763-be81-aab202be2b40.png)

- Vecinos cercanos
![image](https://user-images.githubusercontent.com/24902098/194795933-0e4ecadc-7aa6-497c-831b-dea12c546346.png)


- Random Forest
![image](https://user-images.githubusercontent.com/24902098/194795951-6f2305fb-26c4-477d-8825-1550b194d5f8.png)


## Conclusiones

Codificamos el diagnóstico donde 
  -1 es Maligno 
  -0 es Benigno

Se han probado 4 tipos de modelos:

- Gradiente descendente estocástica

- Árbol de decisión

- Vecinos cercanos

- Random Forest

Dada la primicia que un falso negativo es mucho más preocupante y de acuerdo a los resultados de la matriz de confusión tanto en training como en test, concluyo que el mejor modelo para este caso es el de Random forest ya que en ambos resultados presenta un porcentaje de precisión alto 100% y 96% respectivamente, y lo mejor es que prediciendo falsos negativos es el que mejor se comporta, viendo la esquina inferior izquierda de las matrices de confusión.
