# Lectura 9-2: “Carousel Personalization in Music Streaming Apps with Contextual Bandits”

En este artículo, los autores modelan la personalización del carrusel como un problema contextual de "multi-armed bandit" con múltiples jugadas, visualización de brazos estocásticos y retroalimentación de lotes retardada. Buscan demostrar de forma empírica la efectividad de este marco para capturar características de carruseles del mundo real al abordar una tarea de recomendación de listas de reproducción a gran escala en la aplicación móvil de transmisión de música global. 

Me parecen interesantes los métodos "Semi-Personalization via User Clustering" y "Contextual Multi-Armed Bandits" ya que con esto evitan tener que utilizar un método costoso como ejecutar simultáneamente N algoritmos bandit estándar, para identificar identificar individualmente las L primeras cartas con mayores probabilidades de pui para cada usuario u. 

En el entorno propuesto en el paper, el usuario puede que no vea todas las cartas seleccionadas. El usuario debe deslizar el dedo hacia la derecha para ver tarjetas adicionales. Mientras que los algoritmos estándar de bandit generalmente consideran que el pronosticador recibe recompensas (0 o 1) de cada uno de los L brazos. Este aspecto es importante, ya que le da mayor realismo al sistema.

La app utilizada Deezer me parece pertinente, ya que le da un mayor realismo a sus resultados.

Se utilizan valores de L=12 y Linit=3, pero no se menciona la razón de esto. ¿Fueron valores elegidos al azar? ¿Se hubiesen obtenido resultados diferentes con otros valores?

Se realizó un "k-means clustering" con Q = 100 grupos para asignar a cada usuario a un solo grupo. Sin embargo, no se menciona porque  se selcciona el valor 100. ¿Se intento con otros valores?.

Se utilizan una gran variedad de métodos como "random", "etc-seg","ts-seg" entre otros. Esto le da mayor validez a sus estudios, ya que se nota que hubo un trabajo exhaustivo, además permite hacer una mejor comparación y análisis de resultados.

En los experimentos realizado, las recompensas no se procesan sobre la marcha, sino por lotes, al final de cada ronda, esto me parece interesante, ya que les permite ser coherentes con las limitaciones que existen en la realidad.

El paper presenta buenos resultados. No obstante, tiene alguno problemas: Se asume que la cantidad de usuarios y tarjetas se fijaba a lo largo de las rondas, esto podría ser una limitante que da pie a nuevos estudios sobre la integración de usuarios nuevos. Otro supuesto importante, es que se asume que la distribución de tarjetas son fijas e independientes, lo que en mi opinión, es poco realista, ya que el interes de la lista también puede depender de sus vecinos en el carrusel, y al solo considerar la selección individual de lista de reproducción, puede no siempre conducir al mejor conjunto de listas, por ejemplo en términos de diversidad.
