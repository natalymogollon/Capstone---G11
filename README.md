# USIL_Capstone_202301_G11
## Integrantes
- Canales Del Rio, Ana Belen
- Mogollon Bermudez, Nataly Karla

Titulo: Un estudio comparativo de las técnicas computacionales para la detección de fake reviews en los productos de Amazon

Descripción: Código en Python para la ejecución de dos métodos computacionales para la detección de fake reviews y su comparación para analizar, en el determinado número de datos, cuál tuvo un porcentaje más alto de precisión en la detección de las reseñas falsas.

El dataset seleccionado cuenta con aproximadamente más de 568 000 registros, por lo que seleccionamos una media de 25 000 reviews para entrenar en los modelos empleados y tener un resultado más rápido.

Dataset utilizado: https://drive.google.com/file/d/1kdZN5LVfOPiKUkka-iKzUJ2nEhcW_Fgz/view?usp=sharing

Fuente del dataset: https://www.kaggle.com/code/ak1982/amazon-review-sentiment-analysis-prediction/notebook

Fuentes de los métodos mencionados:
SF-BiLSTM: https://inass.org/wp-content/uploads/2022/06/2022103141-2.pdf
NBSVM: https://www.sciencedirect.com/science/article/pii/S0969698921003374

## Ejecución Modelo SF-BiLSTM
El modelo SF-BiLSTM es una arquitectura de red neuronal utilizada para tareas de procesamiento del lenguaje natural, como la clasificación de texto. SF significa "Sentiment-Focused" (centrado en el sentimiento) y BiLSTM se refiere a Memoria de Corto y Largo Plazo Bidireccional.

Este modelo es capaz de analizar el sentimiento o la emoción en un texto dado. Utiliza una estructura de red neuronal llamada LSTM, que es capaz de capturar información de contexto a largo plazo. La característica "bidireccional" significa que la red neuronal procesa la información tanto en el orden normal como en el orden inverso, lo que ayuda a capturar mejor las dependencias y relaciones entre las palabras en el texto.

El modelo SF-BiLSTM se entrena con un conjunto de datos previamente etiquetados, donde cada ejemplo de texto está asociado con una etiqueta de sentimiento específica, como positivo, negativo o neutral. Durante el entrenamiento, la red neuronal aprende a reconocer patrones y características en el texto que indican el sentimiento asociado.

### Se inicia el procedimiento colocando las librerías necesarias para la ejecución 

![image](https://github.com/natalymogollon/Capstone---G11/assets/50871642/9b2a49a4-b3c6-4e1a-a322-b2c9d452a35e)

Y se procede a utilizar un código para importar el dataset en formato CSV y cargarlo a la carpeta de Google Colab. Se debe comprobar que el archivo se cargó correctamente.

![image](https://github.com/natalymogollon/Capstone---G11/assets/50871642/449641c4-4ddd-4a49-ae95-fef6c2505887)
![image](https://github.com/natalymogollon/Capstone---G11/assets/50871642/7d26594e-7b84-4b16-90de-ebd369f04553)

Se debe asignar el dataset a una variable para poder efectuar el análisis en el código posteriormente, y para corrobar la carga correcta, hacemos un print a la cantidad de reviews consideradas.

![image](https://github.com/natalymogollon/Capstone---G11/assets/50871642/ad055a4b-485c-42b3-8bdc-be98cec26b5f)

Se inicia una nueva sección el código a implementar para realizar el método SF-BiLSTM 

![image](https://github.com/natalymogollon/Capstone---G11/assets/50871642/88f498e9-f19f-4651-970f-5ed30639dfa9)

Los componentes clave utilizados en esta parte fueron considerados por diferentes razones:

- Embedding layer: Esta capa se utiliza para representar palabras o tokens en forma de vectores densos. Aprende representaciones vectoriales de palabras en función de su contexto y proximidad semántica.
- Bidirectional LSTM layer: Esta capa utiliza la arquitectura LSTM, que es una variante de las redes neuronales recurrentes (RNN). Al ser bidireccional, la capa LSTM procesa la secuencia tanto en dirección directa como inversa, lo que permite capturar el contexto pasado y futuro de cada palabra.
- SpatialDropout1D layer: Esta capa de Dropout se aplica a las secuencias en lugar de a las neuronas individuales.
- Dense layer: Es una capa densamente conectada que toma las representaciones de secuencia generadas por la capa Bi-LSTM y las proyecta en una salida final. En este caso, se utiliza una función de activación softmax para clasificar las secuencias en diferentes categorías.

![image](https://github.com/natalymogollon/Capstone---G11/assets/50871642/cbafd3c9-a6ee-4190-b3b4-5aab711a436c)

Se procede con la compilación y evaluación de datos con lo ingresado previamente, para finalmente arrojar los siguientes resultados:

![image](https://github.com/natalymogollon/Capstone---G11/assets/50871642/d656106c-1bdb-41f0-bfa2-c9723b1a4a69)

Los resultados obtenidos en las métricas indican el desempeño del modelo de detección de reseñas falsas en base a los datos de prueba:

Accuracy (exactitud): El modelo tiene una exactitud de 0.6674, lo que significa que clasifica correctamente aproximadamente el 66.74% de las muestras.

Precision (precisión): El modelo tiene una precisión de 0.6621, lo que indica que aproximadamente el 66.21% de las predicciones positivas (detecciones de reseñas falsas) son correctas.

Recall (recuperación): En este caso, el modelo tiene un recall de 0.6674, lo que significa que logra encontrar y clasificar correctamente aproximadamente el 66.74% de las reseñas falsas en el conjunto de datos.

En conclusión, el modelo tiene un desempeño moderado en la detección de reseñas falsas, con una exactitud, precisión y recall alrededor del 66-67%. Esto implica que el modelo clasifica correctamente un porcentaje considerable de las muestras, pero también puede haber margen de mejora en la identificación de fake reviews.



Link al video de GitHub:

Link al video de Implementación:


