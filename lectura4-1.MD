# Content-Based Recommendation Systems

## Resumen

En este capítulo del libro "The Adaptive Web" (2007), los autores (Pazzani M. y Bilsus D.) discuten sistemas de recomendación basados en el contenido de los ítems a recomendar. Para esto, se plantean tres principales puntos de discusión: la representación de los ítems, la creación del perfil del usuario que describe los ítems que le gustan y la manera de comparar ítems con perfiles de usuario para generar una recomendación.

## Representación de la información

Me parece relevante que se recalque la diferencia entre obtener la información de manera estructurada versus no estructurada. Creo que los autores son claros al explicar por qué es necesario trabajar con información estructurada, pero no tanto en cómo es posible transformar la información no estructurada. La principal crítica que tengo sobre este punto es que se habla sobre el *tf\*idf weight* pero no se explica lo que es el *tf\*idf*. Para comprender esto de mejor forma tuve que recurrir a otros recursos como [este](https://towardsdatascience.com/introduction-to-two-approaches-of-content-based-recommendation-system-fc797460c18c).

## Creación del perfil de usuario

Estas secciones (2 y 3) se enfocan en explicar qué es un perfil de usuario y cómo se construye. Al definir los  elementos que pueden componer el perfil me genera un poco de confusión pues el texto dice:

> El perfil de los intereses del usuario es usado por la mayoría de los sistemas recomendadores. Este perfil puede consistir en **un número de diferentes tipos de información**. Aquí, nos concentramos en dos tipos de información: ...

No queda claro qué otros tipos de información podrían conformar este perfil.

No obstante, el resto de las secciones son explicadas de manera correcta. Lo más positivo es el uso de ejemplos para mostrar casos de retroalimentación implícita o explícita que puede entregar el usuario. 

## Comparación de ítems

Diría que este punto es el principal foco del capítulo, pues se profundiza más cada tipo de comparación. Los autores estructuran su explicación planteando: en qué consiste cada método, qué variantes tiene, cuándo es útil (o qué estructura deben tener los datos para que lo sea) y qué resultados se han obtenido utilizándolos.

Personalmente, no me gusta esta forma de estructurar la información debido a que se pierde un poco el foco del capítulo. Creo que esto se debe a que los autores buscan entregar un detalle más fino en aquellas técnicas que son más complejas de comprender (como los métodos probabilísticos o el algoritmo de Rocchio) y no queda muy claro qué diferencias hay en las variantes de los algoritmos más "sencillos". Para ejemplificar esto, podemos ver que en los casos de las técnicas mencionadas, se busca explicar el método incorporando fórmulas, explicando cada variable. Por el contrario, al explicar árboles de decisión, no se incorpora ningúna figura explicativa que guíe el entendimiento del texto.

## Conclusiones

El principal aporte del texto es recopilar información sobre técnicas utilizadas en sistemas de recomendación basados en contenido. Me parece que actualmente existen otras técnicas más sofisticadas para extraer información de campos de texto "libre" que no son mencionadas. Esto puede deberse a la antiguedad del libro (2007), por lo que es comprensible que no sean mencionadas técnicas de procesamiento de lenguaje natural basadas en redes neuronales recursivas.