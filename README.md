# Etapa 2 del proyecto: Hacia una medicina preventiva en hipertensión arterial

La hipertensión arterial es uno de los principales factores de riesgo para las enfermedades cardiovasculares, las cuales, a su vez, son una de las causas principales de morbilidad y mortalidad a nivel mundial[1]. La detección temprana de esta afección representa un gran reto, ya que sus síntomas a menudo pasan desapercibidos y el diagnóstico se realiza con frecuencia en etapas avanzadas. Esta situación resalta la importancia de encontrar soluciones que apoyen en la identificación precoz de la hipertensión.

Este proyecto tiene como objetivo desarrollar modelos predictivos basados en datos que permitan estimar el riesgo de hipertensión en pacientes. La finalidad es doble: por un lado, facilitar la identificación temprana de casos y, por otro, identificar los factores clave que influyen en el desarrollo de la enfermedad. Una herramienta de este tipo sería de gran valor para los profesionales de la salud ya que les permitiría fortalecer las campañas y programas de prevención, así como diseñar estrategias de educación en salud más personalizadas.

**A. Objetivos.**

- Aplicar técnicas de clasificación basadas en árboles de decisión y K-vecinos más cercanos para construir modelos predictivos que permitan identificar el riesgo de desarrollar hipertensión.

- Identificar los factores más relevantes que influyen en el desarrollo de la hipertensión a partir del análisis de los datos.

**B. Conjunto de datos.**

El conjunto de datos incluye información demográfica, de hábitos de vida y antecedentes médicos de individuos, como edad, índice de masa corporal (BMI), consumo de tabaco, así como la presencia de enfermedad cardíaca. El conjunto de datos original se obtuvo de este 
enlace
y fue modificado para los fines de este proyecto.

**C. Actividades para realizar.**

1. Exploración y perfilamiento de los datos, utilizando las funcionalidades de la librería pandas. Recuerda que este paso es muy importante para determinar problemas de calidad (por ejemplo, valores ausentes y registros duplicados) y tomar decisiones relacionadas con la preparación de los datos para el algoritmo de aprendizaje. 

2. Construcción del pipeline de limpieza y preparación de los datos, justificando las decisiones tomadas con base en los resultados obtenidos en el paso anterior.

3. Construcción de un modelo de árboles de decisión. Utiliza la función GridSeacrhCV, con el siguiente espacio de búsqueda: {'criterion':['gini', 'entropy'],'max_depth':[4,6,8,10,12],'min_samples_split':[3, 4, 5]}. 

4. Construcción de un modelo utilizando el algoritmo K-vecinos más cercanos. Para determinar el número de vecinos utiliza los siguientes valores de K: [1, 2, 3, 4, 5].

5. Elaboración de una tabla comparativa mostrando el rendimiento sobre test de los dos modelos seleccionados (con mejores rendimientos) de las actividades 3 y 4, sobre las métricas exactitud, recall, precisión y F-score. 

6. Estimación de intervalos de confianza mediante bootstrapping. Investiga la técnica de bootstrapping y utilízala para estimar un intervalo de confianza del 95% para al menos una de las métricas (por ejemplo, exactitud) con base en el modelo de mejor desempeño. Debes explicar brevemente el procedimiento utilizado e interpretar el intervalo obtenido en el contexto del problema.

7. Utilizando el modelo de árboles de decisión, hasta con una profundidad de tres (3), genera las reglas que permitan determinar cuándo un paciente está en riesgo de sufrir hipertensión (no es necesario volver a construir el árbol).

**D. Consideraciones.**

- Al hacer la división entrenamiento – test (y en cualquier funcionalidad que lo requiera) utiliza un valor de semilla de 77 (random_state). 

- El conjunto de prueba (test) no debe utilizarse para ajustar hiperparámetros.

- Justificar todas las decisiones metodológicas tomadas durante el proceso.

**E. Análisis de resultados.**

- Una vez construido los modelos, deberías estar en capacidad de responder estas preguntas:

- ¿Qué puedes decir de los valores de las métricas recall y precisión para cada una de las clases en cada modelo? ¿Cuál de estás métricas consideras que es más importante con base en la descripción del problema?

- ¿Consideras que el rendimiento de los modelos es adecuado? Si no es así, ¿Cómo podrían mejorarse los resultados?

- ¿Cuáles son las variables más significativas según el mejor modelo basado en árboles de decisión? Reflexiona sobre cómo este nuevo conocimiento podría ayudar a tomar decisiones en el contexto del problema.

- Si ambos modelos presentan resultados similares en las métricas de desempeño, ¿Cuál seleccionarías considerando el contexto clínico del problema? Justifica tu elección.

- ¿Qué indica el intervalo de confianza estimado sobre la estabilidad y confiabilidad del modelo seleccionado?

**F. Entregable.**

Notebook (*.ipynb y *.html) por la plataforma. El Notebook debe estar documentado con las justificaciones de las decisiones tomadas en cada paso del ciclo de machine learning y las respuestas a las preguntas planteadas en el apartado E. Además, deben ser visibles las ejecuciones de cada celda. Esta entrega debe realizarse en la sexta semana, en donde encontrarás un espacio para adjuntar los dos archivos.
 