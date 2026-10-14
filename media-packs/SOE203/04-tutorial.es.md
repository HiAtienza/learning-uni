# SOE203 · Taller de requisitos

## Estado de generación del vídeo
PENDIENTE: material preparado; no se ha generado ni revisado ningún vídeo nuevo.

## Instrucciones
Explica la unidad en español siguiendo únicamente este material. Cita las fuentes y distingue práctica complementaria, respuestas suministradas y comentarios locales. Conserva fórmulas, identificadores, discrepancias y límites de evidencia. No inventes contenido, requisitos, resultados, dominio del estudiante ni predicciones de examen.

## Fuentes originales
- Week 4 - Tutorial Questions.docx (original en inglés) · SHA-256 f284f9d3fcf3c340f0157aea122c5f0cc4dbe13d222eb3328430264d535e2d45
- Week 4 - Additional Tutorial Questions.docx (original en inglés) · SHA-256 8ec3fcbf47af815f7116858d37b867214ea319dae9745391887885b6adb39d07
- Week 4 - Tutorial Questions w Answers.docx (original en inglés) · SHA-256 979c7f08e22764c2347a2be8c3e39db2ebb4ab81e440035adf405f47f76b4dda
- Week 4 - Additional Tutorial Questions w Answers.docx (original en inglés) · SHA-256 a017855aa76b38a5f380881f7623a170dd50728a245f46e5d13937b62021c00d

## Edición española derivada
El hash indicado para cada documento identifica la fuente inglesa; el contenido mostrado es la traducción española. Los originales se conservan en la biblioteca.

### content/reviewed/SOE203/04-tutorial/tutor.md
Hash de fuente inglesa: 07323c0e1f5366403b09089ac74591522b0777364df272fd6595c11254c36957

# Requisitos clínica tutorial

Edición web basada en fuentes: **Semana 4: Preguntas del tutorial.docx (seis preguntas)** y **Semana 4: Preguntas del tutorial adicionales.docx (ocho preguntas)**, lea en su totalidad. Utilice la Unidad 04 como referencia conceptual. Ambas hojas de respuestas proporcionadas para la Semana 4 ya han sido inspeccionadas y conciliadas. Las soluciones colapsadas distinguen un resumen fiel de respuestas proporcionadas de un comentario local; tampoco lo es un sistema oficial de calificación de exámenes.

## Tu ruta a través de este tutorial

Realice las catorce tareas en Recordar y practicar. Cada uno tiene una pista adyacente y una explicación completa. Primero intente de memoria, luego compare la respuesta proporcionada, su alcance y los criterios no resueltos. Tanto los archivos anteriores de solo preguntas como los nuevos archivos DOCX de respuestas se conservan en la biblioteca de origen.

## 1. Cascada clásica y requisitos en evolución

La hoja de trabajo compara una línea base de requisitos aprobada inicialmente con una elaboración ágil incremental. Waterfall tiene como objetivo reducir los costosos malentendidos posteriores. Agile todavía realiza trabajo de requisitos y validación repetidamente. Evite la afirmación absoluta de que Agile no tiene trabajo inicial o que Waterfall nunca podrá revisar una decisión. Fuente: Tutorial Q1; Notas de la unidad 04.

## 2. La viabilidad necesita varios tipos de evidencia

El presupuesto de aparcamiento aborda sólo un aspecto. Verifique la viabilidad técnica, la idoneidad operativa, la capacidad de tiempo/personal y las limitaciones relevantes. Al responder preguntas de elicitación, conecte el desafío con una técnica concreta: observación para la práctica tácita, prototipos para necesidades de interacción poco claras o talleres para conflictos. Fuente: Tutorial Q2–3.

## 3. Convertir un deseo en un comportamiento comprobable

Las alertas de vuelo, las retiradas inusuales, los conductores que se aproximan y las puertas abiertas necesitan cada uno de ellos un disparador, condiciones definidas, respuestas y criterios de aceptación. Los requisitos del usuario expresan los objetivos de las partes interesadas; Los requisitos del sistema elaboran el comportamiento. Términos como instantáneamente, exactamente e inusual permanecen sin resolver hasta que se acuerden los criterios. Las nuevas hojas proporcionan valores de ejemplo: vuelo de 30 segundos, inclinación 3 veces promedio/10 segundos, actualizaciones del conductor cada 5 segundos y notificación de geocerca/puerta dentro de los 30 segundos. Trátelos como valores en los ejemplos proporcionados, no como requisitos universales; las fuentes dejan abierta alguna semántica de medición y sensor. Fuente: Tutorial Q4; P1-3 adicionales.

## 4. Funciones separadas y expectativas de calidad.

Las funciones de búsqueda, filtrado, sincronización de ejercicios y descarga sin conexión se describen. Los objetivos proporcionados son búsqueda en 2 segundos/95 %, finalización de sincronización del entrenamiento en 2 segundos, filtrado de productos en 1,5 segundos/95 % e inicio de descarga con progreso visible en 1 segundo. La culminación y la iniciación son eventos distintos; La carga normal aún necesita definición. FURPS Performance cubre esas preocupaciones sobre el tiempo; la seguridad se agrupa en Funcionalidad en el marco del curso proporcionado; La integridad de guardado concurrente preocupa la confiabilidad. Las categorías FURPS no reemplazan el análisis funcional/de calidad. Fuente: Tutorial Q5; Adicional Q4–8.

## 5. Razón sobre las interacciones

El problema de la respuesta firmada de 500 ms es un posible conflicto de recursos/latencia. Marque la interacción, explique un mecanismo concreto, proponga un diseño e identifique qué necesita ser probado. La respuesta Q6 proporcionada propone acusar recibo antes de que se complete la firma y luego firma/auditoría asincrónica. Preservar esa propuesta al mismo tiempo que se distingue la recepción de la aceptación firmada y se requiere una semántica explícita de falla/recuperación; no puede debilitar silenciosamente el requisito original. Fuente: Tutorial Q6.

## Revisión

Explique un requisito sin utilizar lenguaje vago de velocidad o precisión. Identifique al menos un criterio que aún requiera el acuerdo de las partes interesadas. Compare sus catorce intentos completos con el razonamiento trabajado localmente y luego revise las tarjetas marcadas para su revisión. Los umbrales de ejemplo proporcionados ahora son visibles; no son resultados medidos, notas de exámenes oficiales ni predicciones.

## Respuestas proporcionadas en la semana 4: límites que vale la pena verificar

[[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Tutorial Questions w Answers.docx|Hoja principal de respuestas]]: seis preguntas sin cambios con nuevas respuestas. [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Hoja de respuestas adicional]]: ocho preguntas sin cambios con nuevas respuestas. Sus números son requisitos de respuesta-ejemplo; el texto original de la pregunta no los prescribía.

- Pregunta principal 4: la respuesta reacciona a los cambios en el horario de salida, no solo a los retrasos; combina una necesidad de Interactor con un disparador de datos de Dominio.
- P6 principal: una entrada de matriz −1 indica un conflicto probable, no una imposibilidad medida. Su compensación de firma asincrónica necesita una semántica de reconocimiento explícita.
- P6 adicional: se aplica un segundo para iniciar la descarga con el progreso, no para finalizar un episodio completo.
- P7 adicional: "más de 5" fallas consecutivas dentro de 10 minutos desencadenan un bloqueo de 30 minutos más una nueva verificación de identidad; preservar el límite estricto y la etiqueta de funcionalidad proporcionada.
- P8 adicional: La confiabilidad es la categoría de origen; Preservar todas las ediciones es una propiedad de aceptación, no una prueba de que se haya implementado un algoritmo de combinación.

Utilice las catorce identidades de práctica originales para revisar las respuestas guardadas. Las calificaciones existentes y los intentos escritos siguen siendo sus registros; Las explicaciones de las fuentes revisadas no las restablecen ni establecen un nuevo dominio.


### content/reviewed/SOE203/04-tutorial/practice.md
Hash de fuente inglesa: e6700efa8940974d2ba6601f533706c7b089b6d3bbee83b3e9019d602bc5e346

# Requisitos de la clínica tutorial: recordar y practicar.

Edición de tutores web. Las catorce tareas originales ahora incluyen **RESPUESTA DEL CURSO SUMINISTRADA, no un esquema de calificación de examen**, seguida de comentarios locales etiquetados por separado. El repaso activo atómico conserva sus líneas fuente e ID anteriores. No se infieren calificaciones oficiales ni dominio del alumno. Fuentes: Semana 4: Preguntas del tutorial.docx / Semana 4: Preguntas del tutorial adicionales.docx; La Unidad 04 revisó notas. Inténtelo antes de abrir la ayuda.

## Repaso activo atómico

### Tarjeta 01: ¿Por qué es necesario elaborar un requisito de usuario?
> [!success]- Respuesta
> Los objetivos de las partes interesadas deben traducirse en comportamientos observables, desencadenantes, condiciones y criterios de aceptación acordados.
>
> Fuente: Semana 4 - Preguntas del tutorial.docx / Semana 4 - Preguntas del tutorial adicionales.docx; Unidad 04 notas revisadas, tutorial Q4; Q1-3 adicionales.

### Tarjeta 02: ¿Es el presupuesto por sí solo un argumento de viabilidad?
> [!success]- Respuesta
> No. También se deben evaluar la capacidad técnica, la idoneidad operativa, el cronograma y las limitaciones.
>
> Fuente: Semana 4 - Preguntas del tutorial.docx / Semana 4 - Preguntas del tutorial adicionales.docx; Unidad 04 notas revisadas, tutorial Q2.

### Tarjeta 03: ¿Funciona Agile para evitar requisitos?
> [!success]- Respuesta
> No. Revisa los requisitos de forma incremental; La cascada clásica invierte antes para reducir los costosos malentendidos posteriores.
>
> Fuente: Semana 4 - Preguntas del tutorial.docx / Semana 4 - Preguntas del tutorial adicionales.docx; Unidad 04 notas revisadas, tutorial Q1.

### Tarjeta 04: ¿Es comprobable un adjetivo de calidad no medido?
> [!success]- Respuesta
> No. Definir una medida, condiciones y umbral acordados; No inventemos silenciosamente valores oficiales.
>
> Fuente: Semana 4 - Preguntas del tutorial.docx / Semana 4 - Preguntas del tutorial adicionales.docx; Unidad 04 notas revisadas, tutorial Q5; Q4-6 adicionales.

### Tarjeta 05: ¿Qué significan los puntos de vista del interactor, indirecto y de dominio?
> [!success]- Respuesta
> Interactor utiliza/interface directamente; indirecto tiene intereses sin uso directo; El dominio aporta reglas o restricciones del dominio de la aplicación.
>
> Fuente: Semana 4 - Preguntas del tutorial.docx / Semana 4 - Preguntas del tutorial adicionales.docx; Unidad 04 notas revisadas, tutorial Q4.

### Tarjeta 06: ¿En qué se diferencian las clasificaciones funcionales y FURPS?
> [!success]- Respuesta
> Funcional versus calidad separa el comportamiento de sus limitaciones; Las categorías FURPS agrupan preocupaciones y no son sinónimos uno a uno de esa separación.
>
> Fuente: Semana 4 - Preguntas del tutorial.docx / Semana 4 - Preguntas del tutorial adicionales.docx; Unidad 04 notas revisadas, tutorial Q5; Q7-8 adicionales.

## Práctica progresiva

### Práctica 1: requisitos iniciales

**EJERCICIO ORIGINAL DEL CURSO: respuesta proporcionada con comentarios locales.**

El capítulo 3 estudió Agile, donde los requisitos evolucionan sprint tras sprint. El capítulo 4 estudia la cascada, donde se completa y aprueba toda una fase de ingeniería de requisitos antes de que comience el diseño. Explique, en sus propias palabras, por qué Waterfall requiere esta inversión inicial mientras que Agile no, y qué riesgo intenta evitar Waterfall al hacerlo.

Fuente: Semana 4: Preguntas del tutorial.docx, Pregunta 1.

> [!tip]- Sugerencia
> Pregunte cuándo los malentendidos resultan costosos y cuándo se revisan los requisitos.

> [!success]- Solución
> **RESPUESTA DEL CURSO PROPORCIONADA (resumen fiel):** La inversión inicial reduce el retrabajo posterior porque el diseño, el código y las pruebas dependen del SRS aprobado. La comparación proporcionada describe el control inicial, de aprobación y de cambios de Waterfall versus el refinamiento incremental ágil y la retroalimentación del software en funcionamiento.
>
> Fuente: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Tutorial Questions w Answers.docx|Semana 4 - Preguntas del tutorial con respuestas.docx]], Pregunta 1.
>
> **COMENTARIO LOCAL:** La respuesta es una comparación de cursos, no una afirmación de que Agile no tiene una planificación temprana o que Waterfall nunca podrá cambiar.

### Práctica 2: Brecha de viabilidad

**EJERCICIO ORIGINAL DEL CURSO: respuesta proporcionada con comentarios locales.**

Un informe de viabilidad para un nuevo sistema de reserva de estacionamiento en el campus concluye: "El presupuesto cubre un equipo de desarrollo de dos semestres, por lo que el proyecto debería continuar". Identifique lo que falta en este juicio de viabilidad.

Fuente: Semana 4 - Preguntas del tutorial.docx, Pregunta 2.

> [!tip]- Sugerencia
> Probar la viabilidad técnica, operativa y de cronograma, así como financiera.

> [!success]- Solución
> **RESPUESTA DEL CURSO SUMINISTRADA (resumen fiel):** Verifique los objetivos organizacionales, la ingeniería con tecnología actual dentro del presupuesto y el cronograma, y la integración con la infraestructura existente/heredada. La ficha presupuestaria recoge sólo una parte de esa sentencia.
>
> Fuente: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Tutorial Questions w Answers.docx|Semana 4 - Preguntas del tutorial con respuestas.docx]], Pregunta 2.
>
> **COMENTARIO LOCAL:** Dos semestres no son por sí solos una demostración de viabilidad del cronograma; El ajuste operativo sigue siendo una elaboración local útil.

### Práctica 3 — Desafío de elicitación

**EJERCICIO ORIGINAL DEL CURSO: respuesta proporcionada con comentarios locales.**

Nombra y explica un desafío de obtención y explica cómo una técnica específica ayuda a resolver ese desafío.

Fuente: Semana 4 - Preguntas del tutorial.docx, Pregunta 3.

> [!tip]- Sugerencia
> Relacionar la técnica con la causa, no sólo con su nombre.

> [!success]- Solución
> **RESPUESTA DEL CURSO SUMINISTRADA (resumen fiel):** La hoja ofrece cuatro pares desafío/técnica: conocimiento tácito → etnografía/sombreamiento; jerga de dominio → glosario de dominio compartido; listas de deseos poco realistas → matriz de viabilidad/valor-costo; conflictos políticos → talleres multiperspectivas.
>
> Fuente: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Tutorial Questions w Answers.docx|Semana 4 - Preguntas del tutorial con respuestas.docx]], Pregunta 3.
>
> **COMENTARIO LOCAL:** Cualquier pareja elegida debe explicar cómo la técnica aborda esa causa específica.

### Práctica 4 — Retraso del vuelo y puntos de vista

**EJERCICIO ORIGINAL DEL CURSO: respuesta proporcionada con comentarios locales.**

Una parte interesada dice: "Quiero saber al instante si mi vuelo se retrasa". Escriba un requisito de usuario y un requisito del sistema correspondiente derivado de él. Luego, indique cuál de los tres puntos de vista de la VOA (interactor, indirecto o dominio) representa principalmente cada requisito y por qué.

Fuente: Semana 4 - Preguntas del tutorial.docx, Pregunta 4.

> [!tip]- Sugerencia
> Mantener el objetivo de las partes interesadas separado de los detalles del sistema; los umbrales de entrega necesitan acuerdo.

> [!success]- Solución
> **RESPUESTA CURSO SUMINISTRADO (resumen fiel):** UR: notificar al pasajero cuando cambia el horario de salida del vuelo reservado. SR: CUANDO la hora de salida se actualice en el sistema de operaciones de la aerolínea, envíe una notificación al dispositivo registrado dentro de los 30 segundos. La UR es Interactor; el SR satisface esa necesidad y también refleja el Dominio a través de su autorizado disparador de datos de aerolíneas.
>
> Fuente: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Tutorial Questions w Answers.docx|Semana 4 - Preguntas del tutorial con respuestas.docx]], Pregunta 4.
>
> **COMENTARIO LOCAL:** El valor de 30 segundos se encuentra en la respuesta proporcionada. Los “cambios en el horario de salida” son más amplios que solo retrasos; La actualidad de los datos y el alcance del evento previsto aún necesitan definición. Un requisito del sistema no es automáticamente un punto de vista de dominio.

### Práctica 5 — Búsqueda de cursos y FURPS

**EJERCICIO ORIGINAL DEL CURSO: respuesta proporcionada con comentarios locales.**

Una declaración de una parte interesada combina una característica con una expectativa de calidad: "La aplicación móvil debería permitirme buscar un curso y obtener resultados de inmediato". Divida esto en un requisito funcional y un requisito no funcional, e identifique a qué categoría FURPS+ pertenece el NFR. Luego, en una o dos oraciones, explique por qué la categoría F de FURPS+ no es simplemente sinónimo de Requisito Funcional.

Fuente: Semana 4 - Preguntas del tutorial.docx, Pregunta 5.

> [!tip]- Sugerencia
> Una declaración describe una función; el otro limita el tiempo de respuesta.

> [!success]- Solución
> **RESPUESTA DEL CURSO SUMINISTRADO (resumen fiel):** FR: busca por nombre o código del curso y muestra resultados coincidentes. NFR: devuelve resultados en 2 segundos para el 95% de las consultas bajo carga normal; categoría Rendimiento. La funcionalidad FURPS es un grupo de categorías; una FR es una declaración de requisitos particular.
>
> Fuente: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Tutorial Questions w Answers.docx|Semana 4 - Preguntas del tutorial con respuestas.docx]], Pregunta 5.
>
> **COMENTARIO LOCAL:** Estos números provienen de la hoja de respuestas. Defina la carga normal, la carga de trabajo de consultas y los puntos finales de sincronización antes de tratarlos como un procedimiento de aceptación ejecutable.

### Práctica 6: Firmas frente a 500 ms

**EJERCICIO ORIGINAL DEL CURSO: respuesta proporcionada con comentarios locales.**

Se proponen dos requisitos para un sistema de exámenes en línea: (1) "Cada respuesta enviada se registrará con una firma criptográfica a prueba de manipulaciones" y (2) "El sistema aceptará y confirmará una respuesta enviada dentro de 500 milisegundos". Utilizando un enfoque de análisis de interacción basado en matrices, explique si es probable que estos dos requisitos entren en conflicto y, de ser así, sugiera una compensación arquitectónica que podría resolverlo.

Fuente: Semana 4 - Preguntas del tutorial.docx, Pregunta 6.

> [!tip]- Sugerencia
> Separar un conflicto de recursos plausible de una imposibilidad demostrada.

> [!success]- Solución
> **RESPUESTA DEL CURSO SUMINISTRADA (resumen fiel):** La hoja asigna una interacción probable −1: la firma y la E/S de registro seguro compiten con el presupuesto de respuesta de 500 ms, especialmente cerca de las fechas límite. Su compensación propuesta acusa recibo antes de que finalice la firma, luego calcula/añade la firma de forma asincrónica y audita ese paso.
>
> Fuente: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Tutorial Questions w Answers.docx|Semana 4 - Preguntas del tutorial con respuestas.docx]], Pregunta 6.
>
> **COMENTARIO LOCAL:** Esta es la propuesta proporcionada, no una implementación demostrada ni una garantía. Distinguir el recibo de la aceptación firmada duradera; especifique el comportamiento pendiente/fallo/reintento/recuperación. Confirme la semántica de reconocimiento modificada con respecto a ambos requisitos originales en lugar de debilitar silenciosamente la evidencia de manipulación.

### Práctica 7 — Retiro bancario inusual

**EJERCICIO ORIGINAL DEL CURSO: respuesta proporcionada con comentarios locales.**

Una parte interesada dice: "Quiero recibir una alerta en el momento en que haya un retiro grande e inusual de mi cuenta". Escriba un requisito de usuario y un requisito del sistema correspondiente derivado de él.

Fuente: Semana 4: Preguntas tutoriales adicionales.docx, Pregunta 1.

> [!tip]- Sugerencia
> Necesidad grande/inusual de reglas definidas; el origen del evento y la latencia son importantes.

> [!success]- Solución
> **RESPUESTA DEL CURSO SUMINISTRADA (resumen fiel):** UR: alerta al titular sobre un retiro inusualmente grande. SR: CUANDO un retiro excede 3 veces el monto promedio de retiro mensual de la cuenta, envíe mensajes push y SMS dentro de los 10 segundos posteriores al procesamiento de la transacción.
>
> Fuente: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Semana 4 - Preguntas adicionales del tutorial con Answers.docx]], Pregunta 1.
>
> **COMENTARIO LOCAL:** El ejemplo proporcionado corrige el multiplicador, los canales y la latencia; el período/cálculo promedio y el comportamiento de historial cero permanecen sin especificar.

### Práctica 8 — Ubicación del conductor

**EJERCICIO ORIGINAL DEL CURSO: respuesta proporcionada con comentarios locales.**

Una parte interesada dice: "Quiero ver exactamente dónde está mi conductor antes de que llegue". Escriba un requisito de usuario y un requisito del sistema correspondiente derivado de él.

Fuente: Semana 4: Preguntas tutoriales adicionales.docx, Pregunta 2.

> [!tip]- Sugerencia
> Una ubicación muestreada no es infinitamente precisa ni está constantemente actualizada.

> [!success]- Solución
> **RESPUESTA DEL CURSO SUMINISTRADA (resumen fiel):** UR: muestra el conductor asignado desde la aceptación del viaje hasta la recogida. SR: MIENTRAS el viaje está en “conductor en ruta”, actualiza la posición en el mapa del pasajero cada 5 segundos.
>
> Fuente: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Semana 4 - Preguntas adicionales del tutorial con Answers.docx]], Pregunta 2.
>
> **COMENTARIO LOCAL:** Las actualizaciones de cinco segundos son el valor proporcionado; no establecen la precisión de la ubicación exacta ni definen el manejo obsoleto/fuera de línea.

### Práctica 9 — Puerta abierta

**EJERCICIO ORIGINAL DEL CURSO: respuesta proporcionada con comentarios locales.**

Una parte interesada dice: "Quiero saber de inmediato si la puerta de mi casa queda abierta después de salir de casa". Escriba un requisito de usuario y un requisito del sistema correspondiente derivado de él.

Fuente: Semana 4: Preguntas tutoriales adicionales.docx, Pregunta 3.

> [!tip]- Sugerencia
> Tanto la salida como la detección desbloqueada necesitan evidencia definida confiable.

> [!success]- Solución
> **RESPUESTA DEL CURSO SUMINISTRADA (resumen fiel):** UR: notificar al propietario sobre una puerta abierta después de salir. SR: CUANDO el teléfono del propietario sale de la geocerca de la casa y el sensor informa que está desbloqueado, envíe una notificación dentro de los 30 segundos.
>
> Fuente: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Semana 4 - Preguntas adicionales del tutorial con Answers.docx]], Pregunta 3.
>
> **COMENTARIO LOCAL:** La hoja proporciona el activador y la latencia de la geocerca; La confiabilidad del sensor/geocerca y el manejo de salidas falsas siguen siendo cuestiones de aceptación separadas. Un período de gracia es un comentario local, no en esta respuesta.

### Práctica 10: sincronización del entrenamiento

**EJERCICIO ORIGINAL DEL CURSO: respuesta proporcionada con comentarios locales.**

Una declaración de una parte interesada combina una característica con una expectativa de calidad: "La aplicación de fitness debería permitirme registrar un entrenamiento y sincronizarlo con mi reloj sin ningún retraso". Divida esto en un requisito funcional y un requisito no funcional, e identifique a qué categoría FURPS+ pertenece el NFR.

Fuente: Semana 4: Preguntas tutoriales adicionales.docx, Pregunta 4.

> [!tip]- Sugerencia
> No descarte la función de sincronización mientras separa el rendimiento.

> [!success]- Solución
> **RESPUESTA DEL CURSO SUMINISTRADA (resumen fiel):** FR: registra un entrenamiento y sincronízalo con el reloj inteligente conectado. NFR: complete la sincronización dentro de los 2 segundos posteriores al inicio de sesión; categoría Rendimiento.
>
> Fuente: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Semana 4 - Preguntas adicionales del tutorial con Answers.docx]], Pregunta 4.
>
> **COMENTARIO LOCAL:** Este es un objetivo de finalización, a diferencia del objetivo de inicio de descarga que aparece a continuación. Defina la conectividad, el volumen de datos y el comportamiento de falla/pendiente por separado.

### Práctica 11 — Filtrado de precios

**EJERCICIO ORIGINAL DEL CURSO: respuesta proporcionada con comentarios locales.**

Una declaración de una de las partes interesadas combina una característica con una expectativa de calidad: "La aplicación de la tienda debería permitirme filtrar productos por precio y mostrarme los resultados sin que la página se sienta lenta". Divida esto en un requisito funcional y un requisito no funcional, e identifique a qué categoría FURPS+ pertenece el NFR.

Fuente: Semana 4: Preguntas tutoriales adicionales.docx, Pregunta 5.

> [!tip]- Sugerencia
> Especificar el comportamiento de los resultados por separado del tiempo de respuesta.

> [!success]- Solución
> **RESPUESTA DEL CURSO SUMINISTRADA (resumen fiel):** FR: filtrar la lista de productos por rango de precio especificado. NFR: muestra resultados en 1,5 segundos para el 95% de las solicitudes de filtro bajo carga normal; categoría Rendimiento.
>
> Fuente: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Semana 4 - Preguntas adicionales del tutorial con Answers.docx]], Pregunta 5.
>
> **COMENTARIO LOCAL:** Mantenga el percentil así como la latencia. Los puntos finales de conjuntos de datos, dispositivos, cargas y eventos aún necesitan un procedimiento de medición acordado.

### Práctica 12 — Episodio sin conexión

**EJERCICIO ORIGINAL DEL CURSO: respuesta proporcionada con comentarios locales.**

Una declaración de una de las partes interesadas combina una característica con una expectativa de calidad: "La aplicación debería permitirme descargar un episodio para verlo sin conexión y tenerlo listo casi al instante". Divida esto en un requisito funcional y un requisito no funcional, e identifique a qué categoría FURPS+ pertenece el NFR.

Fuente: Semana 4: Preguntas tutoriales adicionales.docx, Pregunta 6.

> [!tip]- Sugerencia
> La reproducción sin conexión y la finalización de la descarga son eventos observables diferentes.

> [!success]- Solución
> **RESPUESTA DEL CURSO SUMINISTRADA (resumen fiel):** FR: descargar un episodio para verlo sin conexión. NFR: comience la descarga con un progreso visible dentro de 1 segundo del toque; categoría Rendimiento.
>
> Fuente: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Semana 4 - Preguntas adicionales del tutorial con Answers.docx]], Pregunta 6.
>
> **COMENTARIO LOCAL:** El objetivo proporcionado es el inicio de la descarga con retroalimentación, no la transferencia completa en un segundo. La disponibilidad sin conexión aún depende de completar la descarga.

### Práctica 13 — Seguridad de transferencias bancarias

**EJERCICIO ORIGINAL DEL CURSO: respuesta proporcionada con comentarios locales.**

Una declaración de una parte interesada combina una característica con una expectativa de calidad: "La aplicación bancaria debería permitir a los clientes transferir dinero entre cuentas, pero no hay manera de que alguien pueda adivinar o ingresar por la fuerza bruta en la cuenta de otra persona". Divida esto en un requisito funcional y un requisito no funcional, e identifique a qué categoría FURPS+ pertenece el NFR.

Fuente: Semana 4: Preguntas tutoriales adicionales.docx, Pregunta 7.

> [!tip]- Sugerencia
> Seguridad pertenece al curso FURPS Agrupación de Funcionalidades; También definir controles concretos.

> [!success]- Solución
> **RESPUESTA DEL CURSO SUMINISTRADA (resumen fiel):** FR: permite que un cliente autenticado realice transferencias entre sus propias cuentas vinculadas. NFR: SI se producen más de 5 inicios de sesión fallidos consecutivos en una cuenta en un plazo de 10 minutos, ENTONCES ciérrela durante 30 minutos y solicite una nueva verificación de identidad antes de realizar más intentos. La hoja etiqueta este comportamiento no deseado como EARS y Funcionalidad.
>
> Fuente: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Semana 4 - Preguntas adicionales del tutorial con Answers.docx]], Pregunta 7.
>
> **COMENTARIO LOCAL:** “Más de 5” significa que la condición se cumple en la sexta falla consecutiva dentro de la ventana. Esta respuesta de seguridad concreta no establece una garantía absoluta contra todo compromiso; conservar la clasificación FURPS de la fuente.

### Práctica 14: editor concurrente

**EJERCICIO ORIGINAL DEL CURSO: respuesta proporcionada con comentarios locales.**

Una declaración de las partes interesadas combina una característica con una expectativa de calidad: "El editor de documentos compartidos debe permitir que dos personas editen la misma página a la vez, pero nunca debe perder silenciosamente los cambios de una persona cuando ambas guardan aproximadamente al mismo tiempo". Divida esto en un requisito funcional y un requisito no funcional, e identifique a qué categoría FURPS+ pertenece el NFR.

Fuente: Semana 4: Preguntas tutoriales adicionales.docx, Pregunta 8.

> [!tip]- Sugerencia
> Comportamiento de conflictos de estados y propiedades de corrección.

> [!success]- Solución
> **RESPUESTA DEL CURSO SUMINISTRADA (resumen fiel):** FR: dos o más usuarios editan la misma página al mismo tiempo. NFR: CUANDO guardan dentro de la misma sesión de edición, conserva los cambios de todos los usuarios sin descartar las entradas; categoría Fiabilidad.
>
> Fuente: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Semana 4 - Preguntas adicionales del tutorial con Answers.docx]], Pregunta 8.
>
> **COMENTARIO LOCAL:** La respuesta amplía los dos usuarios del mensaje a dos o más. La propiedad de preservación aún necesita pruebas de conflicto/fallo y una semántica de resolución acordada; no se proporciona ningún algoritmo de fusión específico.

