# Evaluating Recommender Systems

Gunawardana A. y Shani G. son los autores de este capítulo del libro Recommender Systems Handbook, publicado el año 2015. En este capítulo, buscan hacer un resumen de los procesos de evaluación de un sistema de recomendación, discutiendo sus diversas propiedades. Para cada propiedad se discuten sus implicaciones en tres tipos de experimentos: *offline*, con estudios de usuarios, y *online*. 

## Sobre los *guidelines*

Antes de comenzar con el análisis, los autores plantean *guidelines* que todo estudio de investigación experimental en el área debería seguir. Este punto me parece muy interesante ya que, si bien puede ser algo que apunte a un entendimiento básico del proceso investigativo, es importante tenerlo claro desde un principio.

## Sobre los tipos de experimentos

Posteriormente, durante la explicación del set de datos para experimentos *offline* se toca un punto que siempre me pareció extraño de los primeros papers. Esto es, que la recolección de estos datos puede generar un sesgo relevante (dado que son datos estáticos) en la forma en que se distribuyen. Me llamaba la atención que no había un mayor análisis del set de datos en los trabajos anteriores, sino que el foco estaba en los resultados solamente. Por esto mismo, me parece muy relevante la inclusión de los otros dos tipos de experimientos en que existe una interacción real con los usuarios. Entiendo que esto pueda tener muchas limitaciones para los investigadores, pero me parece que son metodologías mucho mas cercanas para representar la realidad (eliminando algunos sesgos y supuestos que se tomaban en el tipo *offline*).

## Sobre las propiedades

Considerando los tópicos discutidos en los papers anteriores, voy a omitir comentarios respecto a la precisión (tratada en casi todos los papers), a la cobertura (tratada en parte en el paper de *Top-N Recommendations*) y a la escalabilidad. Respecto a la confianza, me parece que es un tema interesante por tratar. Comúnmente en estos sistemas se busca evaluar la precisión tomando como un valor fijo únicamente el resultado que se obtiene al tomar el valor con mayor probabilidad. Esto podría hacer que un sistema que esté "tambaleando" (que tenga probabilidades muy parecidas para todas sus opciones, pero inclinadas hacia el lado correcto) tenga un buen desempeño en términos de su precisión y un nivel de confianza muy bajo.

Por otra parte, me parece muy interesante que se mencionen propiedades que tienen un impacto más notorio en el uso de los sistemas de recomendación en su implementación. Cosas como robustez o privacidad, son tal vez puntos que no serían discutidos en un paper de investigación de nuevos algoritmos de recomendación. No obstante, me parece relevante que sean puntos de discusión, pues cada uno revela distintas aristas que pueden verse ocultas normalmente.

## Conclusión

Creo que la lectura genera un aporte relevante agrupando y resumiendo los principales aspectos que se debe tener en cuenta para evaluar un sistema recomendador. La estructura del texto permite contextualizar de buena manera las propiedades discutidas y creo que se puede establecer como un marco teórico sólido para tomar en cuenta en investigaciones futuras.
