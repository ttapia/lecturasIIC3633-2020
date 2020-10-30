# Deep learning based recommender system: A survey and new perspectives (desde 3.5)


## Resumen

Este trabajo, publicado el año 2019 por Zhang, S., Tao, L. & Tay, Y., busca resumir los diferentes enfoques que se le ha dado a los sistemas de recomendación basados en técnicas de aprendizaje profundo. Para esta semana, se revisó el material restante sobre el estado del arte en técnicas asociadas a RNN, RBM, atención, NADE, DRL, GANs y modelos híbridos. Además, se discute el trabajo futuro y oportunidades de investigación en esta área.

## Deep Learning + RecSys

Respecto a las redes recurrentes, encuentro destacable su capacidad de modelar elementos secuenciales. Como se explica en el trabajo, esto puede tener un efecto interesante en el uso de sesiones, y también en la recomendación asociada a los comportamientos cambiantes de los usuarios en el tiempo. Al tener acceso a modelos secuenciales, es posible recomendar basado en las decisiones pasadas teniendo en consideración la temporalidad.

Me parece interesante, respecto a los mecanismos de atención, que puedan ser usados para eliminar datos que son poco informativos. Llevándolo un poco al trabajo que he realizado para el proyecto, me parece que hay muchos datos que uno puede encontrar y no está seguro de su utilidad. Utilizar atención para reconocer qué datos son de mayor utilidad me parece una técnica razonable, pero me preocupa que introduzca una cantidad excesiva de parámetros en algunos modelos. Quizá se podrían inspeccionar algunos datos de manera manual, a menos que en realidad la cantidad de categorías sea inmanejable.

## Trabajo futuro

La posibilidad de generar representaciones conjuntas entre usuarios e items me parece muy interesante, y creo que se conecta también con el punto siguiente respecto a la explicabilidad de los sistemas. Si podemos generar una representación conjunta usuario-item, es posible entender qué pares de usuarios e ítems el sistema está considerando que son similares en ciertos sentidos, pudiendo realizar operaciones de distancia y comparaciones de sus dimensiones.
