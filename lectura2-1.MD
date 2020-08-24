## Collaborative Filtering for Implicit Feedback Datasets

*Collaborative Filtering for Implicit Feedback Datasets* es un paper de Hu et. al. publicado el año 2008. Busca plantear la tarea de recomendación determinando los factores latentes de los usuarios e ítems (como en FunkSVD) pero con la salvedad de que, a diferencia de los papers anteriores, el feedback obtenido es implícito.

Desde un inicio se plantean las limitaciones que puede llegar a tener un modelo de feedback implícito. Se plantea, entre otras cosas, que el modelo no puede obtener feedback negativo analizando el comportamiento del usuario, sino solamente aproximar la preferencia que tiene un determinado usuario por un ítem basado en intervalos de confianza.

Asimismo, el paper plantea que la preferencia, dada por el valor numérico asociado a un feedback explícito como un rating, puede ser aproximada analizando estos comportamientos implícitos. Para esto, se plantean las siguientes fórmulas:

$$p_{u,i} = \left \{
    \begin{array}{ll}
        1 & r_{u,i}>0 \\
        0 & r_{u,i}=0 \\
    \end{array}
\right. 
$$

$$ c_{u,i} = 1 + \alpha r_{u,i} $$

Para luego formular el problema de optimización de la siguiente forma:

$$
    \displaystyle min_{x*,y*}\sum_{u,i} c_{u,i}(p_{u,i}-x_{u}^{T}y_{i})^2 + \lambda(\sum_u ||x_u||^2 + \sum_i ||y_i||^2)
$$

Con la formulación anterior, queda muy clara la noción que se plantea respecto a la confianza que se le da a los comportamientos implícitos. Esto es, que una repetición del contenido va a tener un impacto positivo sobre la preferencia de los ítems a analizar, mientras que una visualización parcial va a tener una menor confianza lo cual se va a ponderar usando el factor $c_{u,i}$.

Posteriormente, en la sección 5, se plantea una solución matemática para resolver el problema asociado a cómo explicar una recomendación. Se plantea que la determinación de los factores latentes impide obtener una relación directa entre un ítem y el historial de ítems con que se relaciona. Pero se plantea una solución utilizando un truco matemático muy simple que finalmente predice las preferencias en base a una función lineal basada en el historial. Esta parte del paper me parece que explica de manera muy buena todo el modelo, pues finalmente en su metodología se vuelve en cierta forma a lo planteado en un inicio, como aquellos métodos de vecinos cercanos basados en los ítems.

Finalmente, en la sección de experimentos se muestra que el modelo supera los baselines de Most Popular y Item-KNN. Esto me hace plantearme la pregunta: ¿Cómo podemos mejorar aún más el modelamiento de la confianza y la preferencia? Me parece que simplemente asumir que la ausencia de información implica una preferencia de 0 es limtar al modelo en cierta manera y tal vez sea posible mejorar estos supuestos.