# Lectura 5-1: “Combining Predictions for Accurate RecommenderSystems”

En este artículo, se proporciona un análisis de diferentes métodos de combinación en el conjunto de datos de Netflix. Se discuten y prueban varios algoritmos prometedores para la combinación, que incluyen combinaciones de redes neuronales, árboles de decisión impulsados ​​por gradientes entre otros. En la Sección 2 los autores dan una descripción general de los algoritmos de filtrado colaborativo que se utilizarán como predictores base para los experimentos de combinación. La Sección 3 presenta los algoritmos utilizados para la combinación para finalizar mostrando los resultados obtenidos.

Fue interesante la separación del "*probe set*" que se realizó en los experimentos, donde fue dividido en dos subsets pTrain y pTest. Sin embargo, esta separación fue aleatoria y en partes iguales. ¿Por qué no se probó con otras divisiones? Quizás para alguna separación se hubiesen obtenido mejores resultados.

La cantidad de algortimos de filtrado colaborativo utilizados me parece apropiado, en este paper se utilizan 18 preditores diferentes, lo que da a lugar, a mi parecer, a un buen número de pruebas realizadas.

Se usa como métrica de evaluación RMSE, lo que me parece pertinente, pero creo que se pudo haber agregado otra métrica, por ejemplo MAE. Lo que hace preguntarme ¿Se hubiesen obtenido las mismas conclusiones al utilizar MAE?.

El algoritmo "*Binned Linear Regression*" el conjunto de entrenamiento se puede dividir mediante el uso de un histograma. Lo que me pareció interesante de esto, fue alguno de los criterios que posee este algoritmo. Por ejemplo, el criterio "*time*", al utilizar este criterio de agrupamiento, se puede modelar fácilmente una mezcla dependiente del tiempo. Por otro lado, esta "*frecuency*", con este criterio se tiene la capacidad de dar predicciones con otros pesos cuando un usuario vota muchas veces en un día en particular. No obstante, en la evaluación, se probaron las redes neuronales como algoritmo de combinación por *bin*, pero esto no tuvo tanto éxito en sus resultados como tomar el conjunto de datos completo.

El algoritmo "*Kernel Ridge Regression Blending*" me pareció prometedor, si bien en los resultados se muestra que funciona peor que una red neuronal, el autor menciona que un aumento del tamaño del conjunto de entrenamiento conduciría a un modelo más preciso. A pesar de esto, una de las barreras que presenta *KRR* son los enormes requisitos computacionales que exige, lo que limita a usar un cierto porcentaje de datos.

Este artículo demuestra la ventaja del aprendizaje conjunto aplicado a la combinación de diferentes  algoritmos de filtrado colaborativo. Se obtuvieron resultados muy prometedores y en algunos casos con tiempos de entrenamiento muy cortos, como es el caso de una red neuronal combinada con *bagging* que con una gran cantidad de datos puede predecir en unos pocos segundos.

