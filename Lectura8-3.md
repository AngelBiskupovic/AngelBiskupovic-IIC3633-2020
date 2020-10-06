# Lectura 8-3: “Inspectability and Control in Social Recommenders”

El paper se basa en el estudio de la inspeccionabilidad y control del usuario en los sistemas de recomendación. Se revisan las investigaciones realizadas sobre estos conceptos, se mencioná el término de sistema recomendador "social". Finalmente, realizan un experimento de usuario en línea con un sistema de recomendación de música de Facebook que le da a los usuarios control sobre las recomendaciones y explica cómo surgieron. Los resultados que obtuvieron muestran que la capacidad de inspección y el control de hecho aumentan la comprensión y el control percibidos por los usuarios sobre el sistema, su calificación de la calidad de la recomendación y su satisfacción con el sistema.

Me parece interesante un aspecto de los recomendadores sociales, y es que las recomendaciones se basan en la similitud de los usuarios con sus amigos en lugar de un conjunto de vecinos anónimos más cercanos. En mi opinión, esto hace que los recomendadores sociales puedan aprovechar el conocimiento de los usuarios con la fuente de la recomendación. Por otro lado, creo que se puede provocar un tipo de sesgo, si es que solo se considera la similitud de los usuarios con sus amigos, haciendo que al usuario no se le recomienden todos los items que le pudiesen gustar, por esto es que debería existir un equilibrio, es decir, algún tipo de ponderación entre la similitud del usuario y sus amigos, y la similitud entre el usuario y el resto de items.

En el algoritmo de recomendación se utiliza solo recomendación de Pearson, creo que hubiese sido bueno hacer pruebas con otros tipos de correlación.

Solo se permitió que los usuarios participaran si su gráfico de recomendación mostraba al menos 5 "Me gusta" de música, que se superponen con al menos 5 amigos y dan como resultado al menos 10 recomendaciones. Esto no me parece adecuado, si bien es claro que esto dará una experiencia más significativa al usuario, es importante considerar la posibilidad de usuarios con pocas interacciones o considerar usuarios nuevos.

Me parece interesante la idea de que el usuario sea capaz de controlar las recomendaciones. Sin embargo, el método utilizado en el paper, que consistía en que el usuario podía cambiar los "pesos" de sus amigos, no me parece óptima, ya que no todos los usuarios entienden el concepto de peso, y pueden asignar un valor de peso mayor (o menor) al esperado, haciendo que la recomendación no sea óptimo.

Los 7 factores estimados me parecen adecuados.

En cuanto a los métodos de control implementados en el artículo, creo que se deben mantener ambos, ya que dar a los usuarios control sobre los pesos de los amigos da como resultado recomendaciones de calidad ligeramente más altas. Por otro lado, controlar los pesos de los elementos puede aumentar la percepción de los usuarios de la novedad de la recomendación.

Uno de los aspectos que se podría agregar en este estudio, es permitir a los usuarios encontrar y corregir errores en el proceso de recomendación, esto podría ayudar a los usuarios a mejorar aún más su experiencia.

