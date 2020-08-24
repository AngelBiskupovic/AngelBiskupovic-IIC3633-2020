# Lectura 2-2: "*BPR: Bayesian Personalized Ranking from Implicit Feedback*"

En este artículo, los autores se basan en *feedback* implícitos, mostrando los diferentes modelos existentes hoy en día, y proponen un criterio de optimización generíco para estos modelos, llamado BPR-Opt para ranking personalizado. A su vez, proporcionan un algoritmo de aprendizaje para optimizar modelos con respecto a BPR-Opt. Explican como aplicar este método a los modelos basadosen factorización matricial y Knn adaptativo. Finalmente comparanlos resultados obtenidos con otros métodos.

El uso de la función sigmoide me pareció apropiada, ya que esta se puede ver como una aproximación de la función Heaviside.

El algoritmo de aprendizaje LearnBPR me pareció interesante, ya que soluciona algunos problemas de optimización que presentaban algunos algoritmos anteriores, como en algunos casos su lenta convergencia, además encontré pertinente que se basara en se basa en el descenso de gradiente estocástico con muestreo bootstrap.

La forma es que descompuso la matriz (el estimador) me pareció eficiente.

Una de las ventajas que presenta este enfoque, que me parece oportuno mencionar, es que, los valores perdidos entre dos elementos no observados son exactamente los pares de elementos que deben clasificarse en el futuro. Lo que a mi parecer, es una gran ventaja.

Me quedan algunas dudas sobre las presunciones que se hacen, como que todos los usuarios actúan independientemente unos de otros, ¿Qué sucede si esto no es así? ¿Se verán afectados los resultados finales?.

Me pareció interesante el resultado que se muestra en la figura 5 del paper, que compara la convergenia del método LearnBPR con el "user-wise stochastic gradient descent", ya que su método converge mucho más rápido que el mencionado.

Creo que los resultados obtenidos son muy buenos, pero se deberían haber hecho mayor cantidad de pruebas, variando el dataset de training, de testing, más que nada para comprobar que el modelo implementado es robusto antes cambios de parámetros.

Lo que más rescato de este artículo, es que demostró que el criterio de optimización utilizado es muy importante para obtener buena calidad en las predicciones, ya que compararon mismos modelos pero con diferente criterio de optimización y se demostró una mejora con el algoritmo propuesto por los autores.