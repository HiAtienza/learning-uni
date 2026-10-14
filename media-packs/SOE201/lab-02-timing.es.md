# SOE201 · Laboratorio 02: Tarea de sincronización de consultas publicada

## Estado de generación del vídeo
PENDIENTE: material preparado; no se ha generado ni revisado ningún vídeo nuevo.

## Instrucciones
Explica la unidad en español siguiendo únicamente este material. Cita las fuentes y distingue práctica complementaria, respuestas suministradas y comentarios locales. Conserva fórmulas, identificadores, discrepancias y límites de evidencia. No inventes contenido, requisitos, resultados, dominio del estudiante ni predicciones de examen.

## Fuentes originales
- Lab2-JDBCandIndex-tasks.pdf (original en inglés) · SHA-256 e8a35be4b5025a10b7cdfa4717df49671e10a689e14f1e10acf9732b76a65d35

## Edición española derivada
El hash indicado para cada documento identifica la fuente inglesa; el contenido mostrado es la traducción española. Los originales se conservan en la biblioteca.

### content/reviewed/SOE201/lab-02-timing/tutor.md
Hash de fuente inglesa: db43b72d9454c3a3b85ac6aed12809d8508c65d2ae3707db6d2961cde533c644

---
course: SOE201
type: tutor-notes
language: en
---
# Laboratorio 02: Medir la tarea liberada 2

Este suplemento web refleja el documento publicado `Lab2-JDBCandIndex-tasks.pdf`, PDF p.3. Las notas de configuración del Modo Tutor importadas más antiguas describen la Tarea 2 como pendiente; esa declaración es reemplazada por este comunicado. Los archivos originales de la universidad permanecen sin cambios.

## En 60 segundos

Ejecute la misma consulta de Tarea 1 con y sin índice e imprima el tiempo empleado **solo** en `rs = stmt.executeQuery(sql);`. La configuración de la conexión, la creación de un índice y el consumo de resultados pertenecen fuera del intervalo de tiempo. Compare los resultados lógicos e inspeccione el estado del índice por separado. Fuente: PDF de tareas, páginas 1 a 3 y la sección Tarea publicada 2 del laboratorio de referencia actualizado.

## Antes de comenzar

Complete la práctica de configuración de JDBC anterior. Utilice una base de datos de laboratorio aislada y prevista con una configuración válida. Estas actividades web explican la tarea y no se conectan a la base de datos de la universidad ni ejecutan Java. Las versiones requeridas del servidor universitario y JDK aún no están confirmadas en la hoja de tareas.

## 1. Mantenga la consulta fija

Ambos programas fuente de la Tarea 1 seleccionan `SELECT * FROM Orf_Motif WHERE num=7`. La versión indexada hace que esté disponible un índice sobre `num` antes de enviar esa consulta. No compare diferentes predicados, tablas o interpretaciones de resultados y llámelo experimento de índice. Fuente: tareas PDF páginas 1–2; `JDBC.java` y `JDBCandIndex.java` oficiales.

## 2. Coloque el cronómetro exactamente en una llamada

La solución de referencia actualizada utiliza:

```java
long startNanos = System.nanoTime();
ResultSet resultSet = statement.executeQuery(SELECT_SQL);
long elapsedNanos = System.nanoTime() - startNanos;
```

Convierta nanosegundos a milisegundos dividiendo por `1_000_000.0`. Mantenga el bucle `while (resultSet.next())` después del temporizador. La tarea define su intervalo como la llamada API; El controlador puede recuperar y almacenar en búfer filas durante la ejecución de Query; mover el ciclo de iteración posteriormente no aísla la ejecución del servidor del tiempo de transferencia. Referencia técnica complementaria: [Notas de implementación del conector/J] (https://dev.mysql.com/doc/connector-j/en/connector-j-reference-implementation-notes.html), sección ResultSet, revisada el 2026-10-07. Las configuraciones de transmisión pueden cambiar ese límite. Fuente: tareas PDF p.3; referencia `03 Lab.md`, Líneas de sincronización de Tarea 2 publicada.

## 3. Estado del índice de registro y el plan elegido

Un índice existente, un optimizador que lo elige y un tiempo transcurrido son tres observaciones diferentes. Registre el estado del índice antes/después previsto e inspeccione un plan por separado. La solución de referencia local registra `numIndex`; no vuelva a crear un índice con nombre a ciegas en cada repetición. Un error de índice duplicado puede detener el experimento previsto antes de SELECT. Fuente: oficial `JDBCandIndex.java`, creación del índice; Procedimiento de ejecución del laboratorio de referencia actualizado.

## 4. Establecer resultados iguales

Consuma ambos conjuntos de resultados fuera del temporizador y compárelos sin asumir el orden de las filas. Mantenga duplicados al comparar conjuntos múltiples en lugar de cambiar la semántica de la consulta. La ejecución de referencia comparó conjuntos múltiples `(acc_num, orf)` con 607 filas en cada ejecución. Se trata de evidencia local registrada, no de un recuento de filas prometido para cada importación. Fuente: comparación lógica de la Tarea 2 del laboratorio de referencia actualizada.

## 5. Explica una medida honestamente

La referencia existente registra un par local, 8,723 ms y 2,083 ms. Soporta una diferencia en esa carrera controlada. El estado de la caché, la carga, las estadísticas, el tamaño de los datos y la configuración pueden cambiar el resultado. Estos valores no se miden recientemente mediante esta importación web y no establecen una aceleración universal ni un comportamiento del servidor universitario. Fuente: límites y ejecución local observados del laboratorio de referencia actualizado.

## Revisión

Señale exactamente las tres líneas del cronómetro. Identifique las operaciones excluidas del intervalo. Explique cómo mostraría resultados lógicos iguales y la selección del plan real, luego nombre una condición que podría cambiar los tiempos. Utilice la actividad de costos local para separar una estimación teórica de un intervalo JDBC real.


### content/reviewed/SOE201/lab-02-timing/practice.md
Hash de fuente inglesa: fca73c4d812fc2de60dbdca24f5561c49ffc90cde8f2b9756daeabaddc3608f6

# Tiempo de consulta JDBC: recordar y practicar

Edición de tutores web. La nueva práctica a continuación es **PRÁCTICA COMPLEMENTARIA**, no una tarea oficial ni un esquema de calificación. Fuentes: Lab2-JDBCandIndex-tasks.pdf y Labs/Lab 02 - JDBC e Index/03 Lab.md. Inténtelo antes de abrir la ayuda.

## Repaso activo atómico

### Tarjeta 01: ¿Qué operación libera el tiempo de la Tarea 2?
> [!success]- Respuesta
> Sólo rs = stmt.executeQuery(sql); con marcas de tiempo inmediatamente antes y después de esa llamada.
>
> Fuente: Lab2-JDBCandIndex-tasks.pdf y Labs/Lab 02 - JDBC e Index/03 Lab.md, Hoja de tareas PDF p. 3.

### Tarjeta 02: ¿Dónde se debe colocar el bucle de iteración de resultados? ¿Eso excluye todas las transferencias de filas del tiempo de ejecución de la consulta?
> [!success]- Respuesta
> Coloque el bucle ResultSet.next() de la aplicación e imprima después de la marca de tiempo final. Es posible que el controlador ya recupere y almacene en búfer filas dentro de ejecutarQuery, por lo que esto no excluye toda la transferencia de datos de la llamada medida.
>
> Fuente: Lab2-JDBCandIndex-tasks.pdf y Labs/Lab 02 - JDBC e Index/03 Lab.md, Hoja de tareas PDF p. 3; referencia de laboratorio Tarea 2.

### Tarjeta 03: ¿Cómo se convierten los nanosegundos a milisegundos?
> [!success]- Respuesta
> Reste las marcas de tiempo de nanoTime y divida por 1_000_000.0.
>
> Fuente: Lab2-JDBCandIndex-tasks.pdf y Labs/Lab 02 - JDBC e Index/03 Lab.md, Hoja de tareas PDF p. 3; código de sincronización de referencia de laboratorio.

### Tarjeta 04: ¿Qué consulta permanece constante?
> [!success]- Respuesta
> SELECCIONE * DESDE Orf_Motif DONDE num=7, para ambos estados de índice.
>
> Fuente: Lab2-JDBCandIndex-tasks.pdf y Labs/Lab 02 - JDBC e Index/03 Lab.md, Hoja de tareas PDF p. 3.

### Tarjeta 05: ¿Por qué comparar conjuntos múltiples en lugar de orden de filas?
> [!success]- Respuesta
> Sin orden por fila no se garantiza el orden; Las claves/filas repetidas aún requieren recuentos, por lo que la igualdad establecida simple puede ocultar duplicados.
>
> Fuente: Lab2-JDBCandIndex-tasks.pdf y Labs/Lab 02 - JDBC e Index/03 Lab.md, validación de la Tarea 2 de referencia de laboratorio.

### Tarjeta 06: ¿Los tiempos históricos más rápidos demuestran que la indexación siempre gana?
> [!success]- Respuesta
> No. El resultado local registrado es una observación de entorno único con su propio plan/datos/caché/límite de controlador.
>
> Fuente: Lab2-JDBCandIndex-tasks.pdf y Labs/Lab 02 - JDBC e Index/03 Lab.md, resultados y limitaciones de la Tarea 2 de referencia de laboratorio.

## Práctica progresiva

### Práctica 1: reparar el temporizador

**PRÁCTICA COMPLEMENTARIA.** Un estudiante inicia el cronómetro antes de configurar la conexión y se detiene después de imprimir cada fila. ¿Es esa la Tarea 2? Muestre el límite requerido.

> [!tip]- Sugerencia
> Coloque solo ejecutarQuery entre las dos marcas de tiempo.

> [!success]- Solución
> No es el límite especificado.
> ```java
> long start = System.nanoTime();
> rs = stmt.executeQuery(sql);
> long end = System.nanoTime();
> double elapsedMs = (end - start) / 1_000_000.0;
> ```
> La configuración de la conexión, la creación de índices, la iteración y la impresión permanecen fuera. Es posible que el almacenamiento en búfer del controlador aún esté incluido en la propia llamada.
>
> Fuente: Lab2-JDBCandIndex-tasks.pdf y Labs/Lab 02 - JDBC e Index/03 Lab.md, Hoja de tareas PDF p. 3; referencia de laboratorio Tarea 2.

### Práctica 2: Lista de verificación del experimento de índice

**PRÁCTICA COMPLEMENTARIA.** ¿Qué debería permanecer igual y qué evidencia respalda la comparación antes/después de crear un índice en num?

> [!tip]- Sugerencia
> Entradas controladas separadas, evidencia optimizadora e igualdad de resultados.

> [!success]- Solución
> Utilizar los mismos datos/consulta y conexión/entorno comparable; registrar el estado del índice y EXPLICAR por separado; registrar el índice/plan realmente elegido; comparar conjuntos múltiples de resultados, incluidos recuentos duplicados; repita con las condiciones de caché/calentamiento anotadas. El optimizador no necesita seleccionar un índice creado. No programe el tiempo de DDL dentro de ejecutarQuery.
>
> Fuente: Lab2-JDBCandIndex-tasks.pdf y Labs/Lab 02 - JDBC e Index/03 Lab.md, Hoja de tareas PDF p. 3; referencia de laboratorio Tarea 2.

### Práctica 3: Interpretar la ejecución histórica

**PRÁCTICA COMPLEMENTARIA.** La referencia de origen registra 8,723 ms sin y 2,083 ms con el índice, equivalentes a conjuntos múltiples de 607 filas. ¿Qué puedes reclamar?

> [!tip]- Sugerencia
> Limitar el reclamo a esta ejecución local registrada.

> [!success]- Solución
> La fuente informa un tiempo transcurrido de ejecución de Consulta menor en esa ejecución local con resultados iguales y numIndex seleccionado. No establece una aceleración universal, un tiempo de ejecución solo del servidor, una conectividad entre la universidad y el servidor ni una nueva ejecución realizada por esta aplicación web.
>
> Fuente: Lab2-JDBCandIndex-tasks.pdf y Labs/Lab 02 - JDBC e Index/03 Lab.md, resultados registrados de la Tarea 2 de referencia de laboratorio.

