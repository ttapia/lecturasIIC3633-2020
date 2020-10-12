# Carousel Personalization in Music Streaming Apps with Contextual Bandits

## Resumen

Este trabajo de Bendada, W., Salha, G. y Bontempelli, T. fue publicado el 30 de Septiembre de 2020. En él, se presenta un estudio de sistemas recomendadores usando *multi-armed bandits*, en que cada brazo corresponde a un ítem. Además, se incorpora en este estudio el concepto de "carrusel", una manera de presentar la información que puede contener un cierto número de ítems, pero que depende de las acciones del usuario si estos son visualizados (inicialmente se ve una porción pequeña de estos). Se definen dos formas de incorporar la información del contexto en el problema, una mediante un clustering de los usuarios, y otra mediante el acceso al vector de factores latentes de cada usuario, y un aprendizaje de los pesos asociados a cada brazo. Se realiza un análisis con diferentes algoritmos de aprendizaje de *policies*, y se presentan los resultados de estos. Además, se presentan resultados generales sobre la aplicación de estos algoritmos en un entorno online.

## *Contextual Multi-Armed Bandit for Carousel Personalization*

El problema es planteado como la selección de L brazos de un total de K brazos disponibles. En este caso, cada brazo corresponde a un ítem (playlist), que es recomendado a un usuario. Me parece relevante la incorporación del concepto de carrusel, ya que genera un cambio poco obvio en el proceso de recomendación y en la forma de analizarlo y estudiarlo. Al recomendar un set de ítems, normalmente se asume que el usuario tiene acceso a todos estos, pero en este caso el carrusel no certifica esto.

Las ventajas del carrusel tienen que ver más con un tema de usabilidad y experiencia de usuario en el uso de un dispositivo móvil. Por esto, omitir su existencia sería inadecuado. Me parece correcta la forma en que se modela el problema, suponiendo que el usuario solo ve aquellos items anteriores a los que interactuó.

La manera en que se captura la información del contexto no queda tan clara. Si bien se plantean dos maneras de hacerlo: una mediante un clustering de los usuarios, y otra mediante el acceso a vector de factores latentes de cada usuario, pareciera que cada una de estas maneras captura información diferente, y no se explica de manera clara cómo esto beneficia el proceso de recomendación.

## Experimentos

La selección de algoritmos para el procedimiento experimental está claramente enfocado en la primera manera de capturar la información del contexto (clustering). En este caso, se realizan múltiples pruebas de diversos algoritmos usados ampliamente en el área de aprendizaje reforzado. Me parece bueno que se utilicen diferentes grupos de parámetros que busquen analizar los distintos enfoques (de exploración y de explotación) para buscar explicar el funcionamiento de estos. Sin embargo, me parece que también podría ser de utilidad buscar términos intermedios entre estos parámetros que puedan converger a una solución más equilibrada.

## Resultados

Los resultados apuntan a que una semi-personalización logra mejores resultados que un enfoque completamente personalizado. Estos resultados, sin embargo y como se menciona en el trabajo, asumen que existen clusters buenos y bien definidos. Esta suposición podría aplicarse de buena forma a este problema, pero no a otros en otras áreas, por lo que debe tomarse con precaución.

Considerando los resultados mostrados en el entorno online, se puede validar esta suposición, dado que se siguen patrones similares a los mostrados en los experimentos offline.

## Conclusiones

Este estudio logra ilustrar de manera correcta y completa un sistema recomendador y las variantes y consideraciones que se tomaron en cuenta para lograr un correcto funcionamiento de este. Me parece relevante la conclusión respecto a la semi-personalización, pues puede liberar bastante carga de un modelo completamente personalizado, en términos de su procesamiento.
