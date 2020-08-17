# Lectura 1-2: "*Post original FunkSVD*"

El *post* trata sobre un problema planteado por Netflix, donde fueron proporcionados cierta cantidad de calificaciones a películas, una cantidad de usuarios y de películas, el objetivo es predecir como un usuario dado calificaría una película dada. El autor del *post* describe en detalle el problema planteado, luego explica el modelo utilizado, que se llama descomposición de valor singular (SVD), y describe los pasos seguidos, junto con los problemas que se le han presentado, para finalizar con sus resultados.

Me interesó la idea de descomponer una película en base a atributos básicos que esta tenga, creo que reducir a 40 parámetros una pelicula simplifica el problema. Sin embargo, veo un problema con algún usuario que tenga preferencia por diferentes estilos de peliculas, ¿El sistema que película le recomendaría? Si la persona tiene un gusto variado ¿Cuál de los géneros de películas tendría la prioridad? Son algunas dudas que tengo sobre esta descomposición.

No estoy de acuerdo con la tasa de aprendizaje utilizada, el *learning rate* fue de 0.001, y no se hizo ningún estudio de como podría variar los resultados variando este hyperparámetro, sólo se consideró este valor.

No me parece adecuado el método de recorte que se utiliza para la función G, ya que en el ejemplo que dan sugiere que si la primera característica tiene +10 y la segunda -1 , el resultado para la puntuación final es un 4, y no me parece justo, ya que son escalas diferentes, en mi opinión se podría utilizar algún método de normalización, para que todas las calificaciones se encuentren en una escala de evaluación adecuado. Además, comentar que el autor dice que le faltó "jugar" más para determinar si había una mejor estrategia.

La idea del uso de una función G (no lineal) me pareció pertinente. Sin embargo, creo que al agregar esta función, también se agregó un desafio mayor, si bien obtuvo resultados favorables, no fueron capacez de encontrar una función que fuese capaz de adaptarse a los datos. 

El principal problema que presenta el método propuesto, es el sobreajuste (*overfitting*), a mi parecer, creo que faltó una mayor busqueda de métodos de regularización.    

Por último, mencionar que sería interesante comparar resultados, con los métodos y lenguajes de programación que hoy existen, ya que este *post* fue realizado el 2006, y creo que varios de los problemas que se presentaron, hoy podrían ser resueltos.