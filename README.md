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

![image](https://github.com/natalymogollon/Capstone---G11/assets/50871642/9b2a49a4-b3c6-4e1a-a322-b2c9d452a35e)

Y se procede a utilizar un código para importar el dataset en formato CSV y cargarlo a la carpeta de Google Colab. Se debe comprobar que el archivo se cargó correctamente.

![image](https://github.com/natalymogollon/Capstone---G11/assets/50871642/449641c4-4ddd-4a49-ae95-fef6c2505887)
![image](https://github.com/natalymogollon/Capstone---G11/assets/50871642/7d26594e-7b84-4b16-90de-ebd369f04553)

Se debe asignar el dataset a una variable para poder efectuar el análisis en el código posteriormente

![image](https://github.com/natalymogollon/Capstone---G11/assets/50871642/ad055a4b-485c-42b3-8bdc-be98cec26b5f)


