## BPR: Bayesian Personalized Ranking from Implicit Feedback

BPR: Bayesian Personalized Ranking from Implicit Feedback es un paper de Rendle et al., publicado el año 2009. En este, se plantea un criterio de optimización genérico que apunta a generar un ranking personalizado de ítems. Este criterio es aplicable sobre métodos de recomendación utilizados en el estado del arte (Factorización matricial y adaptive kNN).

Los autores inician su trabajo poniendo un claro énfasis en el cambio de enfoque que hay desde la perspectiva que busca caracterizar cada ítem individualmente versus su posición en un ranking personalizado. En este caso, no interesa generar una predicción absoluta sobre un solo ítem, sino una predicción relativa de un ítem respecto al resto. Este cambio en el enfoque genera la necesidad de definir nuevos métodos de optimización que busquen resolver este problema.

En base a lo anterior, en la sección 3 se formalizan las características que debe cumplir el ranking personalizado. Estas incluyen propiedades de orden para cada par de ítems que generan finalmente un ranking ordenado. La formulación hasta este punto es muy clara y metódica.

El método es explicado a cabalidad y con una formulación muy formal, para luego llegar a sus potenciales aplicaciones en otros métodos ya existentes. Este es uno de los puntos más relevantes de este trabajo, pues la posibilidad de combinar este método con diferentes modelos abre paso a la posibilidad de obtener mejores resultados a partir de la combinación de diferentes herramientas.