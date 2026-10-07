# SOE201 · Lab 02: Released Query Timing Task

## Video generation status
PENDING: source pack prepared; no cloud video has been generated or reviewed.

## Spanish video overview prompt
Explica esta unidad en español claro, paso a paso, para alguien que aprende de forma autodidacta. Usa únicamente el material incluido. Comienza con el problema motivador, presenta los conceptos, muestra un ejemplo visual fiel a las convenciones del curso, pausa para una pregunta y después explica la respuesta. Distingue práctica suplementaria de tareas oficiales y de soluciones oficiales. No inventes datos, fuentes, requisitos, capítulos pendientes, resultados de ejecución ni predicciones de examen. Conserva los límites y discrepancias indicados. Cierra con una actividad que el estudiante pueda intentar en Learning Uni. Cita el nombre del documento y su localizador cuando corresponda. Si falta evidencia, dilo; no rellenes el hueco. Mantén visibles las fórmulas y direcciones de flechas.

## Verified original file snapshots
- Lab2-JDBCandIndex-tasks.pdf · SHA-256 e8a35be4b5025a10b7cdfa4717df49671e10a689e14f1e10acf9732b76a65d35

## Source material

### Snapshot: content/reviewed/SOE201/lab-02-timing/tutor.md
SHA-256: db43b72d9454c3a3b85ac6aed12809d8508c65d2ae3707db6d2961cde533c644

---
course: SOE201
type: tutor-notes
language: en
---
# Lab 02 — Measure the Released Task 2

This web supplement reflects the released `Lab2-JDBCandIndex-tasks.pdf`, PDF p.3. The older imported Tutor Mode setup notes describe Task 2 as pending; that statement is superseded by this release. The original university files remain unchanged.

## In 60 Seconds

Run the same Task 1 query with and without an index and print the time spent in **only** `rs = stmt.executeQuery(sql);`. Connection setup, creating an index and consuming results belong outside the timed interval. Compare logical results and inspect the index state separately. Source: tasks PDF pp.1–3 and the updated reference lab's Released Task 2 section.

## Before You Start

Complete the preceding JDBC setup practical. Use an isolated, intended lab database with valid configuration. These web activities explain the task and do not connect to the university database or execute Java. Required university server and JDK versions remain unconfirmed by the task sheet.

## 1. Keep the query fixed

Both Task 1 source programs select `SELECT * FROM Orf_Motif WHERE num=7`. The indexed version makes an index on `num` available before submitting that query. Do not compare different predicates, tables, or result interpretations and call that an index experiment. Source: tasks PDF pp.1–2; official `JDBC.java` and `JDBCandIndex.java`.

## 2. Place the timer around exactly one call

The updated reference solution uses:

```java
long startNanos = System.nanoTime();
ResultSet resultSet = statement.executeQuery(SELECT_SQL);
long elapsedNanos = System.nanoTime() - startNanos;
```

Convert nanoseconds to milliseconds by dividing by `1_000_000.0`. Keep the `while (resultSet.next())` loop after the timer. The task defines its interval as the API call; The driver can retrieve and buffer rows during executeQuery; moving the iteration loop afterward does not isolate server execution from transfer time. Supplementary technical reference: [Connector/J implementation notes](https://dev.mysql.com/doc/connector-j/en/connector-j-reference-implementation-notes.html), ResultSet section, checked 2026-10-07. Streaming configurations can change that boundary. Source: tasks PDF p.3; reference `03 Lab.md`, Released Task 2 timing lines.

## 3. Record index state and the chosen plan

An index existing, an optimiser choosing it, and an elapsed time are three different observations. Record the intended before/after index state and inspect a plan separately. The local reference solution records `numIndex`; do not recreate a named index blindly on every rerun. A duplicate-index error can stop the intended experiment before the SELECT. Source: official `JDBCandIndex.java`, index creation; updated reference lab's execution procedure.

## 4. Establish equal results

Consume both result sets outside the timer and compare them without assuming row order. Keep duplicates when comparing multisets rather than changing query semantics. The reference run compared `(acc_num, orf)` multisets with 607 rows in each run. This is recorded local evidence, not a promised row count for every import. Source: updated reference lab's Task 2 logical comparison.

## 5. Explain a measurement honestly

The existing reference records one local pair, 8.723 ms and 2.083 ms. It supports a difference in that controlled run. Cache state, load, statistics, data size and configuration can change the result. These values are not newly measured by this web import and do not establish a universal speedup or university-server behaviour. Source: updated reference lab's observed local execution and limits.

## Review

Point to the exact three timer lines. Identify the operations excluded from the interval. Explain how you would show equal logical results and actual plan selection, then name one condition that could change the timings. Use the local cost activity to separate a theoretical estimate from an actual JDBC interval.



### Snapshot: content/reviewed/SOE201/lab-02-timing/practice.md
SHA-256: fca73c4d812fc2de60dbdca24f5561c49ffc90cde8f2b9756daeabaddc3608f6

# JDBC query timing: recall and practice

Web tutor edition. New practice below is **SUPPLEMENTARY PRACTICE**, not an official assignment or marking scheme. Sources: Lab2-JDBCandIndex-tasks.pdf and Labs/Lab 02 - JDBC and Index/03 Lab.md. Attempt before opening help.

## Atomic Recall

### Card 01 — Which operation does released Task 2 time?
> [!success]- Answer
> Only rs = stmt.executeQuery(sql); with timestamps immediately before and after that call.
>
> Source: Lab2-JDBCandIndex-tasks.pdf and Labs/Lab 02 - JDBC and Index/03 Lab.md, Task sheet PDF p. 3.

### Card 02 — Where must the result-iteration loop be placed, and does that exclude all row transfer from executeQuery timing?
> [!success]- Answer
> Place the application’s ResultSet.next() loop and printing after the ending timestamp. The driver may already retrieve and buffer rows inside executeQuery, so this does not exclude all data transfer from the measured call.
>
> Source: Lab2-JDBCandIndex-tasks.pdf and Labs/Lab 02 - JDBC and Index/03 Lab.md, Task sheet PDF p. 3; lab reference Task 2.

### Card 03 — How are nanoseconds converted to milliseconds?
> [!success]- Answer
> Subtract nanoTime timestamps and divide by 1_000_000.0.
>
> Source: Lab2-JDBCandIndex-tasks.pdf and Labs/Lab 02 - JDBC and Index/03 Lab.md, Task sheet PDF p. 3; lab reference timing code.

### Card 04 — Which query stays constant?
> [!success]- Answer
> SELECT * FROM Orf_Motif WHERE num=7, for both index states.
>
> Source: Lab2-JDBCandIndex-tasks.pdf and Labs/Lab 02 - JDBC and Index/03 Lab.md, Task sheet PDF p. 3.

### Card 05 — Why compare multisets rather than row order?
> [!success]- Answer
> Without ORDER BY row order is not guaranteed; repeated keys/rows still require counts, so plain set equality can hide duplicates.
>
> Source: Lab2-JDBCandIndex-tasks.pdf and Labs/Lab 02 - JDBC and Index/03 Lab.md, Lab reference Task 2 validation.

### Card 06 — Do historical faster timings prove indexing always wins?
> [!success]- Answer
> No. The recorded local result is a single environment observation with its own plan/data/cache/driver boundary.
>
> Source: Lab2-JDBCandIndex-tasks.pdf and Labs/Lab 02 - JDBC and Index/03 Lab.md, Lab reference Task 2 results and limitations.

## Progressive Practice

### Practice 1 — Repair the timer

**SUPPLEMENTARY PRACTICE.** A student starts the timer before connection setup and stops after printing every row. Is that Task 2? Show the required boundary.

> [!tip]- Hint
> Put only executeQuery between the two timestamps.

> [!success]- Solution
> It is not the specified boundary.
> ```java
> long start = System.nanoTime();
> rs = stmt.executeQuery(sql);
> long end = System.nanoTime();
> double elapsedMs = (end - start) / 1_000_000.0;
> ```
> Connection setup, index creation, iteration and printing remain outside. Driver buffering may still be included in the call itself.
>
> Source: Lab2-JDBCandIndex-tasks.pdf and Labs/Lab 02 - JDBC and Index/03 Lab.md, Task sheet PDF p. 3; lab reference Task 2.

### Practice 2 — Index experiment checklist

**SUPPLEMENTARY PRACTICE.** What should remain equal and what evidence supports comparison before/after creating an index on num?

> [!tip]- Hint
> Separate controlled inputs, optimizer evidence and result equality.

> [!success]- Solution
> Use the same data/query and comparable connection/environment; record index state and EXPLAIN separately; record the actual chosen index/plan; compare result multisets including duplicate counts; repeat with cache/warmup conditions noted. A created index need not be selected by the optimizer. Do not time DDL inside executeQuery.
>
> Source: Lab2-JDBCandIndex-tasks.pdf and Labs/Lab 02 - JDBC and Index/03 Lab.md, Task sheet PDF p. 3; lab reference Task 2.

### Practice 3 — Interpret the historical run

**SUPPLEMENTARY PRACTICE.** The source reference records 8.723 ms without and 2.083 ms with the index, equal 607-row multisets. What can you claim?

> [!tip]- Hint
> Constrain the claim to this recorded local run.

> [!success]- Solution
> The source reports a lower executeQuery elapsed time in that local run with equal results and numIndex selected. It does not establish a universal speedup, server-only execution time, university-host connectivity, or a fresh run performed by this web app.
>
> Source: Lab2-JDBCandIndex-tasks.pdf and Labs/Lab 02 - JDBC and Index/03 Lab.md, Lab reference Task 2 recorded results.

