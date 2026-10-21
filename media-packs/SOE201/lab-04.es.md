# SOE201 · Laboratorio 04: Clínica de evaluación de consultas

## Estado de generación del vídeo
PENDIENTE: material preparado; no se ha generado ni revisado ningún vídeo nuevo.

## Instrucciones
Explica la unidad en español siguiendo únicamente este material. Cita las fuentes y distingue práctica complementaria, respuestas suministradas y comentarios locales. Conserva fórmulas, identificadores, discrepancias y límites de evidencia. No inventes contenido, requisitos, resultados, dominio del estudiante ni predicciones de examen.

## Fuentes originales
- Lab4-Tutorial.pdf (original en inglés) · SHA-256 6797714de0ab97a1d504fef33730b697c97ca617ceeadc48ab3ecbadfa328ced

## Edición española derivada
El hash indicado para cada documento identifica la fuente inglesa; el contenido mostrado es la traducción española. Los originales se conservan en la biblioteca.

### content/reviewed/SOE201/lab-04/tutor.md
Hash de fuente inglesa: a508d499abc4379187f013c5ebf9b9e2ba19d74e70d85acd9f0744c32ce55dc4

---
course: SOE201
language: en
study_status: untested
---

# Laboratorio 04: Clínica de evaluación de consultas

## En 60 segundos

Esta clínica asigna cada pregunta y subpregunta del Lab4-Tutorial al razonamiento trabajado localmente. Utiliza el PDF verificado de ocho páginas del archivo del 12 de octubre, no una clave de respuestas recién descargada. El recurso de clave de respuesta en vivo 42127 está visible pero no se ha adquirido; Estas soluciones no se presentan como respuestas oficiales. Los principales riesgos son mezclar recuentos de tuplas/bloques, olvidar búsquedas, asumir una selectividad no especificada y combinar convenciones de salida incompatibles.

## P1: escaneos indexados versus escaneos repetidos

Lab4 p.2 proporciona al cliente: 1.000.000 de registros/8.000 bloques y al depositante: 500.000/1.000. Con el depositante exterior y la altura de la conferencia limitada a n=100 punteros, h=4 y una búsqueda de claves necesita h+1=5 accesos. Los bucles anidados indexados dan 2.501.000 transferencias y búsquedas, por lo tanto, 10.254.100 ms con 0,1 ms de transferencia/4 ms de búsqueda. Los bucles anidados de tupla dan 4.000.001.000 transferencias y 501.000 búsquedas, con un coste de 402.004.100 ms. BNL de un bloque externo ofrece 8.001.000 transferencias/2.000 búsquedas, con un costo de 808.100 ms. Según estos supuestos de fuente sin caché, BNL gana entre esos tres algoritmos. No se asume ningún beneficio de ajuste de memoria o almacenamiento en caché.

## P2: Identificar supuestos faltantes y conflictivos

Lab4 pp.3–4 proporciona cliente: 5000 tuplas/500 bloques y transacción: 80 000/7000. Describe la transacción ordenada por su clave, pero también supone un índice primario escaso en customer_Number, que no es su clave indicada transaction_ID. Un plan de acceso agrupado disperso necesita un orden físico coherente con el customer_Number indexado; Esto debe aclararse en lugar de inferirse silenciosamente.

Supongamos condicionalmente que ese orden físico, utilice N=7 y el límite de altura de ocupación mínima de la conferencia h=7. Para el cliente externo, BNL transfiere 3.500.500 bloques y realiza 1.000 búsquedas, con un costo de 354.050 ms. Sean b los bloques de transacciones coincidentes por búsqueda de cliente. El INL agrupado cuesta $B=500+5000(7+b)$ y $S=500+5000(7+1)=40500$, por lo tanto, $T=165550+500b$ ms. Una estimación uniforme de 16 coincidencias/cliente y 80.000/7.000 tuplas/bloque sugiere b≈2, lo que da 166.550 ms; es una estimación explícita, no una conclusión exacta del recuento total. La altura del índice es una convención de límite superior, no una forma medida. Confirma el orden físico y la distribución de coincidencias antes de presentar una comparación definitiva del plan.

## P3: La ordenación externa de doce bloques

Lab4 p.5 y Lecture5a pp.20–22 dan b=12,M=3,b_b=1. Ejecuciones iniciales: 4; número de tramos fusionados a la vez: 2; la ejecución cuenta 4 → 2 → 1; pases de fusión:2. Con la omisión de escritura de salida final de la fuente, B=60,S=44. Si se debe almacenar la salida, agregue 12 transferencias/12 búsquedas, lo que da 72/56. Ambas convenciones describen la misma estructura de tramos; no cambie el número de pasadas para ajustar la escritura de salida.

## P4: Declarar adónde van los resultados ordenados

Lab4 p.6 le da al cliente 8000 bloques, depositante 1000, M = 100, b_b = 5, inicialmente sin ordenar. Fan-in19, tramos ordenados iniciales 80/10 y pases de fusión 2/1. Costes de ordenación totalmente materializados 48.000/4.000 transferencias y 6.560/420 búsquedas respectivamente. Un escaneo de fusión posterior agrega 9000 transferencias y 1800 búsquedas: un total de 61 000 transferencias/8780 búsquedas, omitiendo la escritura del resultado del join.

La fórmula de ordenación de origen omite las escrituras ordenadas finales. Su aplicación proporciona 40.000+3.000 transferencias y 4.960+220 búsquedas de este tipo. Agregar ciegamente un escaneo de combinación posterior por separado da 52,000/6,980, pero omite las escrituras necesarias para que esos archivos ordenados sean persistentes. Si las fusiones finales están realmente fusionadas en la unión, sus costos de lectura ya incluyen el consumo de entradas: el subtotal de transferencia ideal es 43 000, no 52 000. Vuelva a verificar la asignación simultánea de búfer y la capacidad de grupos de claves iguales antes de afirmar que una ejecución fusionada de este tipo es factible. La pregunta deja esta política sin mencionar; Las soluciones locales exponen las alternativas en lugar de reclamar un total oficial sin condiciones.

## P5: Costo de hash condicional y viabilidad del búfer

Lab4 p.7 proporciona 50 particiones y b_b=20, y pide contar bloques parcialmente llenos. La sustitución en Lecture5b p.21 da $B=3(8000+1000)+4(50)=27200$ y $S=2(400+50)+2(50)=1000$. El tiempo estimado con los pesos del Q4 es de 6.720 ms. Esta es aritmética condicional bajo la premisa establecida de un solo paso.

Si la “información de Q4” incluye M=100, la asignación simultánea propuesta requiere (50+1)×20=1020 marcos de memoria, lo que contradice ese presupuesto de memoria. Incluso la afirmación de una sola pasada de la fuente no resuelve el conflicto de asignación. Indique esa inconsistencia; Revise la memoria, los buffers, el recuento de particiones o la estructura de paso antes de tratar 6720 ms como una estimación de plan ejecutable. No se reclama ninguna ejecución de DBMS.

## P6: Materializar antes de la fusión posterior

Lab4 p.8 proporciona b_r=5,b_s=3,M=3,b_b=1 y requiere explícitamente que se escriban los resultados finales ordenados. (a) r realiza 2 tramos ordenados iniciales; s cabe en la memoria y no necesita ejecuciones externas (una secuencia ordenada en memoria). (b) r necesita 1 pase de fusión; s necesita0. (c) Materializar r cuesta2×5×(1+1)=20 transferencias. Leer, ordenar en memoria y escribir cuesta 3+3=6, aunque la ordenación por fusión externa no es necesaria. (d) El escaneo de fusión posterior lee 5+3=8 bloques bajo la condición de ajuste de grupo de la fuente. (e) Total:34 transferencias, excluyendo escrituras de resultados de unión. Tratar la ordenación en memoria como gratuita omitiría su entrada/salida de disco solicitada explícitamente.

## Mapa de origen y límites de verificación

| Localizador de fuentes | Destino web | Partes de la pregunta |
|---|---|---|
| Laboratorio4 p.2 | Sección Problema 1/Q1 | Transferencias, búsquedas, tiempo, comparación de algoritmos |
| Laboratorio 4 págs. 3–4 | Sección Problema2 / Q2 | elección y justificación de BNL/INL; brechas de ordenamiento/selectividad |
| Laboratorio4 pág.5 | Sección Problema 3 / P3 | Ejecutar rastreo, transferencias, búsquedas |
| Laboratorio4 pág.6 | Sección Problema 4 / P4 | Clasificar y unir transferencias/búsquedas; política de salida |
| Laboratorio4 p.7 | Sección Problema 5 / P5 | Costo de bloque parcial; inconsistencia de la memoria heredada |
| Laboratorio4 p.8 | Sección Problema 6/P6 | Partes a) a e), todas cubiertas explícitamente |

Toda la aritmética se vuelve a calcular independientemente a partir de fórmulas establecidas. Las identidades/hashes de origen están en el manifiesto de actualización del proyecto. Las comprobaciones estructurales/de renderizado son independientes de la ejecución física de la base de datos y de la revisión oficial de la clave de respuestas. Se conservan los archivos históricos originales, las notas ordinarias de la bóveda y el progreso del alumno.


### content/reviewed/SOE201/lab-04/practice.md
Hash de fuente inglesa: 7239a329ac31e574f1d933fc5a7ce1ac6860f3a54a7efc8092f835f39c4cad04

# Recordar y practicar

Práctica basada en fuentes con razonamiento trabajado localmente, no un esquema de calificación oficial. Las tareas de origen originales se identifican individualmente. No se afirma ninguna ejecución de base de datos ni dominio del estudiante.

## Repaso activo atómico

### Tarjeta 01: ¿Qué conjunto de datos pertenece a Lab4 Q1?

> [!success]- Respuesta
> Cliente1.000.000 registros/8.000 bloques; depositante500.000 registros/1.000 bloques.
>
> Fuente: Lab4 p.2.

### Tarjeta 02: ¿Qué hace que el segundo trimestre esté numéricamente infradeterminado?

> [!success]- Respuesta
> El orden físico y la distribución de bloques coincidentes por clave no están completamente establecidos por los totales.
>
> Fuente: Lab4 págs.3–4.

### Tarjeta 03: ¿Cuántas pasadas de combinación clasifican 12 bloques con 3 marcos de memoria?

> [!success]- Respuesta
> Dos: 4 tramos ordenados iniciales se convierten en 2 y luego en 1 con fan-in2.
>
> Fuente: Lab4 p.5.

### Tarjeta 04: ¿Por qué una ordenación en memoria no es necesariamente gratuita en el sexto trimestre?

> [!success]- Respuesta
> La pregunta requiere datos ordenados escritos en el disco, así que incluya la lectura y escritura de esos 3 bloques.
>
> Fuente: Lab4 p.8.

### Tarjeta 05 — ¿Qué inconsistencia debe reportar el Q5?

> [!success]- Respuesta
> El M=100 heredado no puede contener 51 buffers de 20 marcos de memoria cada uno; la premisa de un solo paso necesita aclaración.
>
> Fuente: Lab4 págs.6–7.

## Práctica trabajada

### Problema 1 - P1 - Comparar tres algoritmos de unión

TAREA ORIGINAL. Cliente1.000.000 registros/8.000 bloques; depositante 500.000/1.000 como exterior; clave interna B+ índice n=100. Encuentre transferencias, búsquedas, tiempos y compare NL, BNL, INL usando pesos de 0,1 ms/4 ms. Fuente: Lab4 p.2.

> [!tip]- Sugerencia
> Use h=4 debajo del límite de fuente, luego 5 accesos de búsqueda de claves.

> [!success]- Solución
> INL:B=S=1.000+500.000×5=2.501.000,T=10.254.100ms. NL:B=1.000+500.000×8.000=4.000.001.000,S=501.000,T=402.004.100ms. BNL:B=1000+1000×8000=8001000,S=2000,T=808100ms. BNL es el más barato entre estos según el modelo original.

### Problema 2 - P2 - Comparar exponiendo la incertidumbre

TAREA ORIGINAL. Compare BNL y bucles anidados indexados para cliente 5000 tuplas/500 bloques y transacción 80 000/7000, con el índice primario disperso N=7 indicado en customer_Number. Fuente: Lab4 págs. 3–4.

> [!tip]- Sugerencia
> Primero resuelva la descripción del pedido y luego conserve los bloques de datos coincidentes como parámetro.

> [!success]- Solución
> BNL externo del cliente: B=3.500.500,S=1.000,T=354.050ms. INL agrupado condicional con h=7:B=35.500+5.000b,S=40.500,T=165.550+500b ms. Si el empaquetamiento uniforme sugiere b=2,T=166,550ms, por debajo de BNL. Pero la inconsistencia en el orden físico y la distribución de coincidencias desconocida impiden una respuesta exacta incondicional; Exponga ambos supuestos.

### Problema 3 - P3 - Cuente la ordenación externa

TAREA ORIGINAL. b=12,M=3,b_b=1; dar transferencias y busca. Fuente: Lab4 p.5.

> [!tip]- Sugerencia
> Cuatro tramos ordenados iniciales, dos pasadas de fusión; declarar escrito de salida final.

> [!success]- Solución
> Fórmula fuente transmitida:B=12×(2×2+1)=60,S=2×4+12×(4−1)=44. Salida materializada:B=72,S=56. La traza de ejecución es 4→2→1.

### Problema 4 - Q4 - Auditoría de la contabilidad de fusión y unión

TAREA ORIGINAL. Entradas de 8000/1000 bloques sin ordenar, M=100,b_b=5. Encuentre transferencias/búsquedas de ordenación y fusión. Fuente: Lab4 p.6.

> [!tip]- Sugerencia
> Fan-in19; ordenar pases 2 y 1. Decida si se materializan los archivos finales ordenados.

> [!success]- Solución
> Ordenación materializada: 48.000+4.000 transferencias y 6.560+420 búsquedas. Fusión posterior: 9.000 transferencias/1.800 búsquedas. Total 61 000/8 780, se omitió la escritura de resultados. La aritmética de ordenación de secuencias de origen más un escaneo separado arroja 52 000/6 980, pero deja escrituras de persistencia faltantes. La verdadera fusión evita la relectura de esos flujos finales y requiere una verificación de viabilidad del búfer por separado; no debe combinar silenciosamente ambas convenciones.

### Problema 5 - P5 - Cuente el costo de hash y marque el conflicto

TAREA ORIGINAL. Utilice 50 particiones, b_b=20 e incluya bloques parcialmente rellenos para las relaciones Q4. Fuente: Lab4 p.7.

> [!tip]- Sugerencia
> Aplique la fórmula de bloque parcial proporcionada y luego cuente los buffers.

> [!success]- Solución
> Costo de fuente condicional: B=27200,S=1000,T=6720ms con pesos de 0,1/4ms. Sin embargo, un buffer de entrada y 50 buffers de salida de 20 marcos de memoria requieren 1.020 marcos de memoria, lo que supera Q4 M=100. Esta aritmética no establece una ejecución factible de una sola pasada. Aclare la memoria heredada o revise los supuestos de asignación/aprobación.

### Problema 6 - P6 - Responda cada parte de ordenación materializada

TAREA ORIGINAL. b_r=5,b_s=3,M=3,b_b=1; Los resultados finales ordenados deben escribirse antes de fusionarse. Respuesta (a)–(e). Fuente: Lab4 p.8.

> [!tip]- Sugerencia
> Manejar la entrada en memoria por separado e incluir su escritura final.

> [!success]- Solución
> (a)r:2 ejecuciones externas iniciales;s:una secuencia ordenada en memoria,no se requieren ejecuciones externas. (b)r:1 pase de fusión;s:0. (c)r:20 transferencias;s:6 transferencias para lectura+escritura. (d) escaneo de fusión: 8 transferencias bajo el supuesto de ajuste grupal. (e)20+6+8=34 transferencias totales. La escritura del resultado del join se excluye porque su tamaño no está especificado.

