# A user-centric evaluation framework for recommender systems

## Resumen

El paper de Pu, Pearl y Chen, Li, publicado el año 2011, plantea una metodología de evaluación de sistemas recomendadores basada en la perspectiva de los usuarios y su satisfacción con estos. A diferencia de los métodos vistos previamente en clases, no se busca simplemente aumentar la precisión de la predicción en base a si el usuario interactúa o no con un ítem; sino obtener información valiosa sobre las razones por las cuales un usuario actúa frente a una recomendación que se le entrega, desde diversos puntos de vista, tomando como foco la usabilidad del sistema.

## Desarrollo del modelo

Las cualidades que son utilzadas para describir la calidad de los ítems a recomendar no presentan grandes novedades respecto a lo planteado en otras lecturas del curso, como en (1). No obstante, es destacable que estas apunten a diversos aspectos de los ítems, y no solo a si el usuario considera que los ítems están de acuerdo a sus preferencias. Esto ya que los sistemas recomendadores son utiliados en campos muy diversos, algunos de los cuales tienen características que valoran más unos aspectos que otros, y en muchos casos son aspectos que dependen mucho de cada usuario y del nivel de interacción que tiene con el sistema. 

Respecto a la evaluación sobre la interacción del usuario, me parece relevante destacar que se busca evaluar, en parte, la transparencia del sistema con los usuarios. Esto es un tema que puede causar pérdida de confianza de los usuarios con el sistema, y una buena forma de enfrentarlo parece ser la explicación de por qué los productos son recomendados y si el usuario entiende o no esta explicación.

Respecto a las características de usabilidad, me parece relevante la evaluación de la percepción de los usuarios sobre su facilidad de uso desde un inicio. Es común que usuarios sean expertos en el uso de algún sistema, y esta experiencia puede introducir un sesgo relevante en la evaluación o percepción que tienen sobre la facilidad de su uso. Asimismo, en el contexto de la recomendación, me parece relevante que esta facilidad también se evalúe desde el punto de vista de la capacidad de expresión que tiene un usario para entregar sus preferencias.

Finalmente, me parece interesante que se busca reducir el sesgo de los usuarios al responder sus preguntas utilizando la escala 1-5 Likert, y añadiendo preguntas con escala inversa. Sin embargo, me parece que de todas maneras existe este sesgo. Esto ya que las preguntas con escala inversa no son utilizadas uniformemente en todos los *constructs*. Se puede ver que las preguntas que apuntan a cuestiones más generales como actitudes y comportamientos del usuario están todos con una escala normal (preguntas planteadas en positivo).

## Conclusiones

Me parece que hay una gran ventaja en tener un sistema de evaluación de este estilo, pues permite conocer aspectos que muchas veces son pasados por alto al momento de implementar un sistema recomendador. Es importante entender que hay un alto costo asociado a realizar una evaluación con usuarios, pues se asume que este sistema está desplegado de manera online, por lo que es dificil de realizar un estudio de este estilo. Sin embargo, en caso de poder realizarse, puede haber un proceso interesante de aprendizaje sobre las características "ocultas" del sistema recomendador, aquellas asociadas a aspectos más subjetivos de la experiencia de los usuarios.

## Referencia

(1) Guy, S., & Gunawardana, A.. (2011) “Evaluating recommendation systems.” In Recommender systems handbook, pp. 257-297. Springer US, 2011.