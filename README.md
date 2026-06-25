# discovery-agent
Our first discovery agent to generate a mvp with AI


# Tarea 

## Entregables

1. [x] El proyecto completo del Discovery Agent (carpeta discoveries/<tu-caso>/ con interviews/ y outputs/, más la configuración .claude/).

2. [x] El reporte report.html generado. [report.html](discoveries/wolverine/outputs/report.html)

3. [x] Evidencia de la demo del gate: capturas (o un video corto, máx. 3 min) del bloqueo y de la resolución posterior. [Video](tarea/2026-06-24_19-49-56.mp4)

4. [x] Una reflexión breve (1 página, PDF o Markdown) que responda:

P: ¿Qué supuesto tuyo sobre el problema cambió al revisar la evidencia real?

R: En principio, realmente no tenía un "supuesto" claro; más bien, creí tener una solución sin identificar el problema/dolores. ¿Qué cambió? Ahora tengo identificado el malestar real: "agendas multicanal" y "agendas autónomas". A pesar de que mi "solución" pudo (o no) haber expuesto el dolor implícitamente, ahora existe explícitamente, lo cual es oro para la resolución del problema. Identificar claramente los problemas/dolores y exponerlos abre un abanico para el análisis y facilita la toma de decisiones.
Ahora me tomo el tiempo de identificar los problemas/dolores, en lugar de querer picar código. Actualmente, antes de picar código, me aseguro de entender el problema o dolor, pensar y diseñar posibles soluciones, y entonces ahí viene el código.


P: ¿Qué fue lo más difícil de cumplir la regla de "cero invención"?

R: Esta regla fue un punto de quiebre mental para mí.
Lo más difícil para mí fue notar que mis soluciones no sirven si ni siquiera he escuchado los problemas o dolores de los stakeholders. Antes creía saber más que ellos sobre su propio negocio. La regla me forzó a aceptar que el experto en el problema es el entrevistado, no yo. En lugar de creer que ya tengo una solución, ahora escucho, pregunto y pienso primero en el problema y, posteriormente, en la solución, y no al revés.
El ejemplo claro fue cuando el proceso me pidió hacer entrevistas, algo que antes me parecía innecesario porque creía que ya entendía el problema. Ahora entiendo que las entrevistas no son para que me den una solución, sino para escuchar dolores que yo nunca habría identificado solo.


P:¿Para qué te serviría la idea de "gobernanza ejecutable" en tu trabajo?

R: La respuesta corta es: "Serviría para tener resultados de calidad".
Actualmente, en mi trabajo no tenemos una "gobernanza ejecutable", más allá de contar con un "code review" que termina siendo un "apruébame, por favor".
Pero, si la tuviéramos, la calidad dejaría de depender de si el revisor tuvo tiempo o ganas. Un gate que bloquee el merge si los tests fallan o si la cobertura baja de cierto umbral haría que el "apruébame" dejara de ser una opción — el sistema simplemente no dejaría pasar. Eso nos daría un pipeline con capas de validación automáticas, no negociables y deterministas que, finalmente, no nos harían "orar" antes de una salida a producción
