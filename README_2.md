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
Se inicia el procedimiento colocando las librerías necesarias para la ejecución 

![image](https://github.com/natalymogollon/Capstone---G11/assets/50871642/cb76f15e-2ad0-4096-91db-2c00ff5943a3)

Y se procede a utilizar un código para importar el dataset en formato CSV y cargarlo a la carpeta de Google Colab. Se debe comprobar que el archivo se cargó correctamente.

![image](https://github.com/natalymogollon/Capstone---G11/assets/50871642/09731c3a-c8f0-4e0a-bbf3-a799c1e0c335)

![image](https://github.com/natalymogollon/Capstone---G11/assets/50871642/504d2dcb-2634-4df8-b5dd-74df24816d97)

Se debe asignar el dataset a una variable para poder efectuar el análisis en el código posteriormente, y para corrobar la carga correcta, hacemos un print a la cantidad de reviews consideradas.

![image](https://github.com/natalymogollon/Capstone---G11/assets/50871642/44eac72b-9853-43a5-9ce2-7e97a1f68954)

Se inicia la sección con el código para el método NBSVM.
La idea de selección de NBSVM es utilizar el clasificador Naive Bayes para obtener las probabilidades de pertenencia a cada clase y luego utilizar esas probabilidades como características de entrada para el clasificador SVM. Esto permite que el clasificador SVM capture relaciones más complejas utilizando las probabilidades del clasificador Naive Bayes como características.

![image](https://github.com/natalymogollon/Capstone---G11/assets/50871642/bae1aa76-91d1-4632-9482-df4875cb88ad)

