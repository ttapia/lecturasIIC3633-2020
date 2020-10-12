# Multi-Armed Recommender System Bandit Ensembles

## Resumen

Este trabajo publicado el año 2019 por Cañamares, R., Redondo, M. y Castells, P. plantea un sistema recomendador basado en *multi-armed bandits*. El problema de recomendación es planteado como uno dinámico, en el cual las recomendaciones son entregadas secuencialmente y las recomendaciones entregadas en un momento son información valiosa para la realización de recomendaciones posteriores. Así, se busca estudiar el rendimiento de un sistema de *multi-armed bandit*, el cual en cada iteración debe decidir qué algoritmo (brazo) usará para entregar la recomendación a un usuario determinado. Se prueba que este sistema tiene un mejor funcionamiento que un ensamble común que no considera la temporalidad en la toma de decisiones.

## *Bandit Ensembles*

La justificación de este método tiene su base principalmente en la importancia de analizar el problema como uno dinámico. Considerando esto, me parece que existe una gran flexibilidad en cuanto a los posibles experimentos que pueden ser realizados en este entorno, pero pareciera que los autores buscaron generar un contexto lo más sencillo posible para probar su método. 

En específico, me parece que se podría haber aprovechado que los datos existentes (de Movielens) tenían un rating asociado y haber seleccionado este rating como reward, en vez de haber binarizado los datos como se hizo.

## Experimentos

Los experimentos realizados son relativamente sencillos. Se parte con una porción (5%) de los datos como set de training y se comienza a iterar simulando interacciones de los usuarios con los items. En base a esto se calcula un recall acumulado y cada dato nuevo es añadido al set de training. Con esto, el set de training va aumentando a medida que pasan las iteraciones.

En el trabajo se menciona que se realizó solo 1 recomendación por época, pero no se justifica realmente. Sería más razonable que en cada época se realicen varias recomendaciones, para simular de manera más fidedigna el uso de un sistema así. No obstante, me parece que una razón para esto sería que hay datos limitados y la simulación solo puede durar hasta que se acaben los datos del set de test que van pasando al set de train.

Del mismo modo, me parece curioso que no se actualicen los datos de todos los *arms* cuando se ve una recomendación, y solamente se actualiza ese *arm*. No estoy seguro si será por un tema de rendimiento, pero sería útil para mejorar el ensamble completo que cada dato sirviera para todos los brazos (algoritmos) y no solo para aquellos que logran ver ese dato.

## Conclusiones

Me parece que el trabajo presenta un método novedoso para realizar recomendaciones considerando características importantes que no son analizadas consistentemente en la literatura, como lo es el dinamismo del problema. Creo que el trabajo es sencillo, pero ilustra de buena manera las potenciales mejoras que podrían lograrse en el área, y abre un espacio de investigación relevante.
