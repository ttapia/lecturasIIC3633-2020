# Context-Aware Recommender Systems

## Resumen 

Este artículo es del año 2011 y sus autores son Adomavicius G., Mobasher, B., Ricci, F, y Tuzhilin A. En él, se busca explorar las formas en que la información asociada al contexto en el que un usuario se encuentra al momento de elegir un determinado ítem puede ser introducida en un sistemas recomendador. Se comienza por definir el contexto desde una perspectiva general, para luego definirlo en el contexto (valga la redundancia) de los sistemas de recomendación. Posteriormente se definen los distintos casos segun el nivel de conocimiento del sistema recomendador sobre los factores contextuales (completo, parcial, nulo) y según cómo cambian estos factores (estáticos o dinámicos). Luego, enfocándose en el caso en que el conocimiento es completo y los factores son estáticos, se explican 3 formas en que el sistema recomendador puede introducir este contexto: *prefiltering*, *postfiltering* y *modeling*. Finalmente se muestran algunos ejemplos en que se aplican estas nociones de introducción de contexto en la recomendación.

## Contexto en Sistemas Recomendadores

Me parece que las definiciones planteadas en este punto son algo confusas, pues el resto del artículo se enfoca principalmente en el caso estático y con conocimiento completo del contexto. Si bien me parece razonable introducir los distintos casos que son planteados, creo que hacen falta ejemplos más concretos para comprender de mejor forma cada uno de las celdas de la matriz de 3x2 presentada en la figura 1. Asimismo, creo que esta figura no aporta mucho al artículo. Esto porque contiene celdas que simplemente conectan los nombres de las filas/columnas (como las de *Partially Observable*). Podría haberse planteado de otra forma el contenido de cada celda, quizás aprovechando de introducir ejemplos en esta misma tabla.

A continuación se presenta la figura en cuestión.

![](https://i.imgur.com/HOFkhOJ.png)

## Paradigmas en el uso de la información contextual

A partir de lo anterior, se comienza a definir las distintas formas en que podemos incorporar la información del contexto en la recomendación. Este punto me parece que está bien desarrollado y quedan claras las diferencias entre las 3 formas definidas. La principal duda que me queda y que parece no ser resuelta es: ¿Qué ocurre con las recomendaciones "eliminadas" en el caso de "postfiltering"? Esto último dado que se busca generar un listado de top-N recomendaciones. No sé si se busca nuevamente con ciertos filtros adicionales, o simplemente se acorta el listado de recomendaciones, o inicialmente se solicita un número mayor de recomendaciones... Me parece que puede ser resuelto de diversas formas, pero al no haber un ejemplo concreto de su uso queda abierto a algunas dudas.

## Aplicaciones

Un punto que es expuesto posteriormente es el de las aplicaciones de estos sistemas. De estos, los que más me llaman la atención son aquellos descritos en la subsección *Proactive and Distributed Approaches*. Me parece muy interesante cómo se describe la manera de capturar el contexto que tiene uno de estos sistemas, basado en la interacción que puede tener un usuario con un objeto de compras en un entorno de realidad aumentada. Asimismo, considero interesante las diversas características del contexto que son capturadas en cada uno de estas aplicaciones, y me parece destacable la importancia que se le debe dar a cada característica según la tarea que busca cumplir. Tal vez en este ejemplo de compras (de gafas por ejemplo), es importante conocer si un usuario simplemente vió un objeto, lo tomó o se lo probó. Por otra parte, puede ser útil en otro contexto conocer los usuarios que están en la misma red local, o el estado anímico del usuario, entre muchas otras características.

## Conclusiones y Comentarios

Me parece que el artículo como un todo logra presentar una especie de revisión bibliográfica respecto al tópico del contexto en sistemas de recomendación, y es un buen artículo en este sentido. Aborda aspectos relevantes para que un lector pueda comprender el alcance que tiene este tipo de sistemas de recomendación y presenta aplicaciones interesantes que sirven para ejemplificar la diversidad de características que puede contener una representación del contexto.