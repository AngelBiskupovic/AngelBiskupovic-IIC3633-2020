# Lectura 4-2: “Document Clustering Based On Non-negative Matrix Factorization”

En este artículo, se propone un método de agrupamiento de documentos basado en la factorización no negativa de la matriz de documentos de término del corpus de documentos dado. En el espacio semántico latente derivado de la factorización matricial no negativa (NMF), cada eje captura el tema base de un grupo de documentos en particular, y cada documento se representa como una combinación aditiva de los temas base. Comienza haciendo un resumen de los trabajos realizados en métodos de clustering. Luego realizan una descripción del método propuesto, comparandolo con el SVD. Finalmente hacen una evaluación del método, comparandolo con "*Average* *Association*" y "*Normalized* *Cut*".

-El método presenta una clara ventaja ante los métodos basados en LSI: NMF no requiere la semántica latente derivada el espacio sea ortogonal, y garantiza que cada documento tome solo valores no negativos en todas las direcciones semánticas latentes. Además, en el espacio NMF, cada eje corresponde a un grupo, y todos los puntos de datos que pertenecen al mismo grupo se distribuyen a lo largo del mismo eje. Determinar la etiqueta del grupo para cada punto de datos es tan simple como encontrar el eje con el cual el punto de datos tiene el valor de proyección más grande. Por otro lado, en el espacio SVD, aunque los tres ejes separan los puntos de datos que pertenecen a los diferentes grupos, no existe una relación directa entre los ejes (vectores propios) y los grupos. Los métodos tradicionales de agrupación de datos, como K-means, deben aplicarse en este espacio de vector propio para encontrar el conjunto final de agrupaciones de datos. 
Sin embargo, cuando se aplica NMF para la representación de datos, una gran desventaja es que no considera la estructura geométrica en los datos. En [1] se trata este punto, se desarrolla un enfoque basado en gráficos para la representación de datos basada en partes con el fin de superar esta limitación. Los autores en [1] construyen un gráfico de afinidad para codificar la información geométrica y buscamos una factorización matricial que respete la estructura del gráfico. Y demuestran de forma clara el éxito de este algoritmo aplicandolo a problemas de la vida real.

En cuanto a la evaluación, los autores se preocuparon de equilibrar el dataset excluyendo aquellos eventos con menos de 5 documentos, creo que fue un error, en mi opinión se debe considerar un dataset lo más cercano a la realidad.

Las métricas de evaluación utilizadas en los experimentos (AC y MI) me parecieron adecuadas.

Debido a que no se garantiza que el algoritmo NMF encuentre el óptimo global, es beneficioso realizar el algoritmo NMF unas cuantas veces con valores iniciales diferentes y elegir la prueba con un error cuadrado mínimo J. Esto puede presentar una desventaja, ya que si no se tiene un conjunto de datos con grupos razonables se podrían requerir muchos ensayos.







