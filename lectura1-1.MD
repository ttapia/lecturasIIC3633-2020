## Item-Based Collaborative Filtering Recommendation Algorithms

En este paper los autores proponen algoritmos de recomendación basados en ítems (Item KNN), y los comparan con los algoritmos de recomendación basados en usuarios (User KNN) que a la fecha eran ampliamnete usados en la web. Se plantea un análisis desde el punto de vista de la calidad y el desempeño de los algoritmos. 

Me parece interesante el supuesto de que los items son más estáticos que los usuarios, pero creo que es razonable considerando que el paper es del 2001. ¿Será válido este supuesto hoy en día? Desde el punto de vista de la variabilidad en la similitud entre items puede ser, pero considerando la masividad en el uso de internet y la gran cantidad de productos nuevos que aparecen cada día, creo que la cantidad de vecinos nuevos podría variar más en los ítems que en los usuarios.

Creo que el paper realiza un excelente trabajo explicando cada uno de los pasos requeridos para su algoritmo de recomendación, y cómo fueron definiendo cada uno de los parámetros base para la comparación.

Me surge la duda sobre la forma en que se realiza la separación de los sets de entrenamiento y prueba. Considerando que el algoritmo depende de la información de los vecinos cercanos, podría generarse un sesgo asociado a la construccion del modelo si este fue separado de una forma en que se cuenta con información nula sobre algunas películas / usuarios.

Me parece extraño que se incorpore en la comparación de resultados una referencia sobre la cual no se entrega mayor explicación: un algoritmo no personalizado. Supongo que puede entregar un *threshold* como punto de comparación, pero me parece poco relevante en el contexto que se planteó a través de todo el paper.
