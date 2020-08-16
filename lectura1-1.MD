## Item-Based Collaborative Filtering Recommendation Algorithms

En este paper los autores proponen algoritmos de recomendación basados en ítems (Item KNN), y los comparan con los algoritmos de recomendación basados en usuarios (User KNN) que a la fecha eran ampliamnete usados en la web. Se plantea un análisis desde el punto de vista de la calidad y el desempeño de los algoritmos. 

Creo que el paper realiza un excelente trabajo explicando cada uno de los pasos requeridos para su algoritmo de recomendación, y cómo fueron definiendo cada uno de los parámetros base para la comparación.

Me surge la duda sobre la forma en que se realiza la separación de los sets de entrenamiento y prueba. Considerando que el algoritmo depende de la información de los vecinos cercanos, podría generarse un sesgo asociado a la construccion del modelo si este fue separado de una forma en que se cuenta con información nula sobre algunas películas / usuarios.

Me parece extraño que se incorpore en la comparación de resultados una referencia sobre la cual no se entrega mayor explicación: un algoritmo no personalizado. Supongo que puede entregar un *threshold* como punto de comparación, pero me parece poco relevante en el contexto que se planteó a través de todo el paper.

Si bien se considera viable precomputar muchos de los valores de similitudes entre items que se plantean en el paper, me parece prudente preguntarse si esto sigue siendo válido hoy en día, considerando que el paper es de 2001. Especialmente para plataformas como Amazon que cuentan com más de 10 millones de productos.