# Document Clustering Based On Non-negative Matrix Factorization

## Resumen 

Este artículo es de Xu W., Liu X. y Gong Y. y fue publicado en el año 2003. Se busca resolver el problema de *clustering* de documentos en torno a un mismo tópico. Para esto, se plantea un nuevo método llamado non-negativa matrix factorization (NMF) el cual consiste en obtener una factorización de la matriz *term-document* que tiene la ventaja de que cada eje del espacio semántico obtenido captura un tópico base único. Con esto, el problema de clustering se reduce únicamente a realizar esta factorización y luego buscar el eje en que el documento presenta la proyección más grande.

## Método

En este punto, la principal crítica que tengo es respecto a la comparación de la complejidad computacional del método, respecto a otros. Se afirma que el método tiene una complejidad de `O(tkn)` donde `t` es la cantidad de iteraciones realizadas en el método. Sin embargo, no se discute cuál es el número de iteraciones esperado (o deseado) por lo que es difícil hacerse una idea de la ventaja que tiene.

No obstante, al realizar la comparación con el método SVD me parece que las figuras son muy explicativas y generan una noción interesante sobre las diferencias, especialmente en NMF en que cada cluster está alineado con un solo eje.

## Resultados

La principal crítica (o duda) que tengo sobre esto es en torno a las métricas utilizadas. En particular, la métrica *Mutual Information* (MI) contiene una probabilidad de que un documento pertenezca a dos *clusters* simultáneamente. Sin embargo, al definir el dataset, los autores mencionan que quitaron de este todos aquellos documentos con categorías múltiples. Esto me hace cuestionarme si esta métrica es útil al contener este valor.

## Conclusiones

En conclusión, me parece que el artículo logra explicar de buena manera el método nuevo. También creo que logra respaldar de buena manera sus resultados y sus conclusiones. A pesar de esto, creo que al ser un artículo viejo (del año 2003) no e difícil encontrar otros métodos más modernos para el problema de clustering de documentos, principalmente basados en técnicas de machine learning y NLP.
