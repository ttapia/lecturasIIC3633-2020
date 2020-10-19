# Deep learning based recommender system: A survey and new perspectives (hasta 3.4)

## Resumen

Este trabajo, publicado el año 2019 por Zhang, S., Tao, L. & Tay, Y., busca resumir los diferentes enfoques que se le ha dado a los sistemas de recomendación basados en técnicas de aprendizaje profundo. En particular, las secciones que corresponden a la lectura de esta semana buscan entregar un *overview* de las principales técnicas utilizadas en recomendación y en aprendizaje profundo, sus ventajas respecto a otros tipos de sistemas de recomendación, sus principales limitaciones; y, finalmente, una descripción de 4 tipos de recomendación con diferentes técnicas de aprendizaje profundo.

## Sobre *Deep Learning*

Me parece que lo más destacable de este punto tiene que ver con la capacidad que tienen los modelos de aprendizaje profundo de procesar información en bruto (raw) sin la necesidad de un preprocesamiento, el cual es muy costoso para los investigadores. Con estos modelos, se puede simplemente entregar como input la imagen o el texto, y generar vectores de características de estos elementos que son comparables.

Asimismo, me parece relevante también que estos modelos sean capaces de modelar información secuencial. Como se menciona en el trabajo, se ve que puede ser de suma utilidad para modelar las preferencias cambiantes de los usuarios de estos sistemas, por lo que se presenta como una herramienta valiosa.

Respecto a las potenciales limitaciones que tienen estos modelos: por un lado son válidas respecto a los modelos comúnmente (y comercialmente) usados. Sin embargo, existen potenciales avances en todos estos puntos en el estudio de modelos de inteligencia artificial. La investigación avanza rápidamente, y redes como MAC (Hudson, D., Manning, C., 2018) o (Graves et. al., 2016) logran generalizar muy bien con menos datos, y logran ser más transparentes en su proceso de razonamiento.

## Deep Learning + RecSys

Respecto al uso de MLP en recomendaciones, me parece más relevante la aplicación que tiene en la representación de features que en su uso como estimador de una representación más tradicional (e.g. CF). Algunos aspectos planteados en los primeros trabajos en recomendación como FunkSVD utilizaban un método de descenso de gradiente para encontrar factores latentes, y aprendizaje profundo es excelente para este tipo de problemas.

Respecto al uso de autoencoders, inicialmente habría considerado difícil de aplicar estas estructuras en tareas de recomendación, por lo que me llama la atención la variedad de tareas en las que se pueden utilizar. La tarea principal habría pensado que era la de feature extraction, pero me parece que la reconstrucción de factores de usuarios e ítems para tareas de collaborative filtering es muy creativa y un buen acercamiento a esta tarea. Sin embargo, me parece que las tareas de extracción de características siguen siendo las más relevantes en este punto.

Finalmente, respecto al uso de redes convolucionales, claramente su fuerte está en la extracción de features (información implícita) de los ítems. Sean estos imágenes, audio, video o incluso texto, las redes convolucionales tienen la capacidad de extraer features de estos ítems y en base a esto se pueden generar métricas de similaridad en el espacio de características final.

## Bibliografía

- Hudson, D. A., & Manning, C. D. (2018). Compositional attention networks for machine reasoning. arXiv preprint arXiv:1803.03067.
- Graves, A. et. al. (2016). Hybrid computing using a neural network with dynamic external memory. Nature, 538(7626), 471-476.