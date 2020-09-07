# Lectura 4-1: “Content-Based Recommendation Systems”

Los autores de este capítulo analizan los sistemas de recomendación basados ​​en contenido, es decir, los sistemas que recomiendan un artículo a un usuario en función de una descripción del artículo y un perfil de los intereses del usuario. Primero analizan las representaciones alternativas de los elementos. A continuación, se discuten los algoritmos de recomendación adecuados para cada representación. El capítulo concluye con una discusión de las variantes de los enfoques, las fortalezas y debilidades de los sistemas de recomendación basados ​​en contenido y las direcciones para la investigación y el desarrollo futuros.

En cuanto a la representación de items, me parece interesante la idea de usar datos semiestructurados, y convertir un texto libre en una representación estructurada. Sin embargo, una de la mayores dificultades que presenta el lenguaje, es que se basa en un contexto, y la representación propuesta no es capaz de capturarlo.
Las técnicas para crear perfiles de usuario que tratan con datos estructurados deben diferir algo de aquellas técnicas que tratan con datos no estructurados o datos no estructurados que se convierten de forma automática e imprecisa en datos estructurados.

Los sistemas de personalización de usuario presentan algunas limitaciones. La primera, requiere que el usuario haga un esfuerzo, y creo que es complicado lograr que los usuarios realicen este esfuerzo. Segundo, los sistemas de personalización no proporcionan una forma de determinar el orden en el que presentar los elementos y pueden encontrar muy pocos o demasiados elementos coincidentes para mostrar.

Los árboles de decisión, a mi parecer, no es el mejor método de aprendizaje, ya que presenta sesgos inductivos para árboles de decisión con pocas pruebas. Además, este método de aprendizaje ha sido extesamente estudiado en su uso con datos estructurados, que no es el caso de los textos.

Cuando hablan sobre el algoritmo de *Rocchio* no menciona nada sobre los valores de *alpha*, *beta* y *gamma*, es importante saber, si estos valores poseen algún rango de operación recomendado.

Los clasificadores lineales me parecen un excelente método de clasificación, muy utilizado y estudiado. Sin embargo, para la clasificación de texto puede presentar algunos problemas de sobreajuste, esto debido a que en este dominio, se deben aprenden conceptos de alta dimensión a partir de datos de entrenamiento limitados.

En el texto no se hace mención al efecto "novedad". Por ejemplo, un usuario pudo haber interactuado con item por el simple hecho de que en ese momento el item era "novedoso". Tampoco se considera el caso en que un usuario interactua con un item, pero ese item no es para el, por ejemplo, un usuario que compra un regalo para otra persona. Tampoco se considera el efecto "serendipia", es decir, que pasa si el usuario encuentra "por casualidad" un item.






