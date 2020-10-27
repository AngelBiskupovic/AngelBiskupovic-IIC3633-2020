# Lectura 11-1: “Deep Learning based Recommender System: A Survey and New Perspectives” (Desde sección 3.5 en adelante).

El objetivo de esta estudio es revisar a fondo la literatura sobre los avances del sistema de recomendación basado en el aprendizaje profundo. Proporciona un panorama con el que los lectores pueden comprender rápidamente y entrar en el campo de la recomendación basada en el aprendizaje profundo. El resto de este artículo está organizado de la siguiente manera: La Sección 2 presenta los preliminares para los sistemas de recomendación y las redes neuronales profundas. La sección 3 presenta en primer lugar nuestro marco de clasificación y luego ofrece una introducción detallada al estado de la técnica. La sección 4 discute los desafíos y los temas de investigación abiertos prominentes, mientras que la sección 5 concluye el artículo. En esta semana, la letura se enfocará desde la sección 3.5 en adelante.

Me parece interesante la inclusión de las redes neuronales recurrentes (RNN) sin identificador de usuario, ya que se menciona en el paper que estás son muy efectivas para el procesamiento secuencial de datos, lo que lo hace una de las redes neuronales con mayor efectividad a la hora de detectar patrones. Sin embargo, a pesar del éxito de las RNN en la recomendación basada en sesiones, en [1] se indica que el enfoque de vecindario simple podría lograr los mismos resultados de precisión que GRU4Rec.

La integración del mecanismo de atención en las RNN me parece oportuno, ya que si bien el mecanismo de atención neural no es exactamente una técnica neural profunda independiente, al aplicar el mecanismo de atención al sistema de recomendación, se podría aprovechar el mecanismo de atención para filtrar el contenido no informativo y seleccionar los elementos más representativos al tiempo que se proporciona una buena interpretación.

Me parece escasa la información relativa al "Deep Reinforcement Learning", ya que en mi opinión es un punto relevante, debido a que la mayoria de los sistemas de recomendación consideran el proceso de recomendación como un proceso estático, lo que dificulta captar las intenciones temporales del usuario y responder de manera oportuna, con "reinforcement learning" esto se puede solucionar. Sin embargo, en el texto no se hace más que mencionar algunos trabajos relacionados, sin entrar en mayo detalle.

Es interesante el modelo propuesto en [2], donde se propuso un modelo híbrido basado en CNN y RNN para la recomendación de hashtags. Dado un tweet con las imágenes correspondientes, los autores utilizaron CNN para extraer características de imágenes y LSTM para aprender características de texto de tweets. Mientras tanto, los autores propusieron un mecanismo de co-atención para modelar las influencias de correlación y equilibrar la contribución de textos e imágenes. Esto muestra la potencialidad que tienen las redes neuronales, y la cantidad de combinaciones que se pueden hacer dadas diferentes situaciones y problemas.

En cuanto a los trabajos futuros y problemas abiertos, uno de los mas interesantes, es el problema de explicabilidad de la recomendación basada en deep learning, uno de las "desventajas" de las redes neuronales profundas, es la poca interpretabilidad que se puede tener, es decir, muchas veces el usuario no entiende el porque de la recomendación. Si bien con el mecanismo de atención ayuda mejorar este problema, es un punto relevante que se debe seguir mejorando.

REFERENCIAS

[1] Dietmar Jannach and Malte Ludewig. 2017. When Recurrent Neural Networks Meet the Neighborhood for Session-Based Recommenda-tion. InRecsys

[2] Qi Zhang, Jiawen Wang, Haoran Huang, Xuanjing Huang, and Yeyun Gong. Hashtag Recommendation for Multimodal MicroblogUsing Co-Aention Network. InIJCAI.