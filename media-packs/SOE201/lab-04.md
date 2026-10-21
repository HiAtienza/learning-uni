# SOE201 · Lab 04: Query Evaluation Clinic

## Video generation status
PENDING: source pack prepared; no cloud video has been generated or reviewed.

## Spanish video overview prompt
Explica esta unidad en español claro, paso a paso, para alguien que aprende de forma autodidacta. Usa únicamente el material incluido. Comienza con el problema motivador, presenta los conceptos, muestra un ejemplo visual fiel a las convenciones del curso, pausa para una pregunta y después explica la respuesta. Distingue práctica suplementaria de tareas oficiales y de soluciones oficiales. No inventes datos, fuentes, requisitos, capítulos pendientes, resultados de ejecución ni predicciones de examen. Conserva los límites y discrepancias indicados. Cierra con una actividad que el estudiante pueda intentar en Learning Uni. Cita el nombre del documento y su localizador cuando corresponda. Si falta evidencia, dilo; no rellenes el hueco. Mantén visibles las fórmulas y direcciones de flechas.

## Verified original file snapshots
- Lab4-Tutorial.pdf · SHA-256 6797714de0ab97a1d504fef33730b697c97ca617ceeadc48ab3ecbadfa328ced

## Source material

### Snapshot: content/reviewed/SOE201/lab-04/tutor.md
SHA-256: a508d499abc4379187f013c5ebf9b9e2ba19d74e70d85acd9f0744c32ce55dc4

---
course: SOE201
language: en
study_status: untested
---

# Lab 04: Query Evaluation Clinic

## In 60 Seconds

This clinic maps every Lab4-Tutorial question and subquestion to local worked reasoning. It uses the verified eight-page PDF from the12 October archive, not a newly downloaded answer key. The live answer-key resource42127 is visible but has not been acquired; these solutions are not represented as official answers. The main risks are mixing tuple/block counts, forgetting seeks, assuming unspecified selectivity and combining incompatible output conventions.

## Q1: Indexed Versus Repeated Scans

Lab4 p.2 gives customer:1,000,000 records/8,000 blocks and depositor:500,000/1,000. With depositor outer and the lecture height bound for n=100 pointers, h=4 and a key lookup needs h+1=5 accesses. Indexed nested loops gives2,501,000 transfers and seeks, hence10,254,100ms with0.1ms transfer/4ms seek. Tuple nested loops gives4,000,001,000 transfers and501,000 seeks, costing402,004,100ms. One-outer-block BNL gives8,001,000 transfers/2,000 seeks, costing808,100ms. Under these cold source assumptions, BNL wins among those three algorithms. No memory-fit or caching benefit is assumed.

## Q2: Identify Missing and Conflicting Assumptions

Lab4 pp.3–4 gives customer:5,000 tuples/500 blocks and transaction:80,000/7,000. It describes transaction as sorted by its key, yet also supposes a sparse primary index on customer_Number, which is not its stated key transaction_ID. A sparse clustered access plan needs physical ordering consistent with the indexed customer_Number; this must be clarified rather than silently inferred.

Conditionally assume that ordering, use N=7 and the lecture minimum-occupancy height bound h=7. For customer outer, BNL transfers3,500,500 blocks and makes1,000 seeks, costing354,050ms. Let b be the matching transaction blocks per customer lookup. Clustered INL costs $B=500+5000(7+b)$ and $S=500+5000(7+1)=40500$, hence $T=165550+500b$ ms. A uniform packed estimate of16 matches/customer and80,000/7,000 tuples/block suggests b≈2, giving166,550ms; it is an explicit estimate, not an exact conclusion from total counts. Index height is an upper-bound convention, not a measured shape. Confirm ordering and match distribution before presenting a definitive plan comparison.

## Q3: The Twelve-Block External Sort

Lab4 p.5 and Lecture5a pp.20–22 give b=12,M=3,b_b=1. Initial runs:4; fan-in:2; run counts4→2→1; merge passes:2. With the source's final-output-write omission, B=60,S=44. If the output must be stored, add12 transfers/12 seeks, giving72/56. Both conventions describe the same run structure; do not change the number of passes to adjust for output writing.

## Q4: Declare Where the Sorted Results Go

Lab4 p.6 gives customer8,000 blocks,depositor1,000,M=100,b_b=5, initially unsorted. Fan-in19, initial runs80/10 and merge passes2/1. Fully materialised sorting costs48,000/4,000 transfers and6,560/420 seeks respectively. A subsequent merge scan adds9,000 transfers and1,800 seeks: total61,000 transfers/8,780 seeks, omitting join-result writing.

The source sort formula omits final sorted writes. Applying it gives40,000+3,000 transfers and4,960+220 seeks for the sorts. Blindly adding a later separate merge scan gives52,000/6,980, but omits the writes needed to make those sorted files persistent. If final merges are genuinely fused into the join, their read costs already include consuming the inputs: the ideal transfer subtotal is43,000, not52,000. Recheck simultaneous buffer allocation and equal-key-group capacity before claiming such a fused execution is feasible. The question leaves this policy unstated; local solutions expose the alternatives instead of claiming one unqualified official total.

## Q5: Conditional Hash Cost and Buffer Feasibility

Lab4 p.7 supplies50 partitions and b_b=20, and asks to count partially filled blocks. Substitution into Lecture5b p.21 gives $B=3(8000+1000)+4(50)=27200$ and $S=2(400+50)+2(50)=1000$. Estimated time with the Q4 weights is6,720ms. This is conditional arithmetic under the stated one-pass premise.

If “information from Q4” includes M=100, the proposed simultaneous allocation requires(50+1)×20=1,020 frames, contradicting that memory budget. Even the source's one-pass assertion does not resolve the allocation conflict. State that inconsistency; revise memory, buffers, partition count or pass structure before treating6,720ms as an executable plan estimate. No DBMS run is claimed.

## Q6: Materialise Before the Subsequent Merge Join

Lab4 p.8 gives b_r=5,b_s=3,M=3,b_b=1 and explicitly requires final sorted results to be written. (a) r makes2 initial runs; s fits in memory and needs no external runs (one sorted in-memory sequence). (b) r needs1 merge pass; s needs0. (c) Materialised r costs2×5×(1+1)=20 transfers. Reading, in-memory sorting and writing s costs3+3=6, even though external merge sort is unnecessary. (d) The subsequent merge scan reads5+3=8 blocks under the source's group-fit condition. (e) Total34 transfers, excluding join-result writes. Calling the in-memory sort “free” would omit its explicitly requested disk input/output.

## Source Map and Verification Boundaries

| Source locator | Web destination | Question parts |
|---|---|---|
| Lab4 p.2 | Problem1 / Q1 section | Transfers, seeks, time, algorithm comparison |
| Lab4 pp.3–4 | Problem2 / Q2 section | BNL/INL choice and justification; ordering/selectivity gaps |
| Lab4 p.5 | Problem3 / Q3 section | Run trace, transfers, seeks |
| Lab4 p.6 | Problem4 / Q4 section | Sorting and joining transfers/seeks; output policy |
| Lab4 p.7 | Problem5 / Q5 section | Partial-block cost; inherited memory inconsistency |
| Lab4 p.8 | Problem6 / Q6 section | Parts(a)–(e), all explicitly covered |

All arithmetic is independently recomputed from stated formulas. Source identities/hashes are in the project refresh manifest. Structural/render checks are separate from physical database execution and official answer-key review. The historical original source archives, ordinary vault notes and learner progress are preserved.



### Snapshot: content/reviewed/SOE201/lab-04/practice.md
SHA-256: 7239a329ac31e574f1d933fc5a7ce1ac6860f3a54a7efc8092f835f39c4cad04

# Recall and Practice

Source-based practice with local worked reasoning, not an official marking scheme. Original source tasks are identified individually. No database execution or student mastery is claimed.

## Atomic recall

### Card 01 — What dataset belongs to Lab4 Q1?

> [!success]- Answer
> Customer1,000,000 records/8,000 blocks; depositor500,000 records/1,000 blocks.
>
> Source: Lab4 p.2.

### Card 02 — What makes Q2 numerically underdetermined?

> [!success]- Answer
> Physical ordering and per-key matching-block distribution are not fully established by the totals.
>
> Source: Lab4 pp.3–4.

### Card 03 — How many merge passes sort12 blocks with3 frames?

> [!success]- Answer
> Two:4 initial runs become2 then1 with fan-in2.
>
> Source: Lab4 p.5.

### Card 04 — Why is an in-memory sort not necessarily free in Q6?

> [!success]- Answer
> The question requires sorted data written to disk, so include reading and writing those3 blocks.
>
> Source: Lab4 p.8.

### Card 05 — What inconsistency must Q5 report?

> [!success]- Answer
> The inherited M=100 cannot hold51 buffers of20 frames each; the one-pass premise needs clarification.
>
> Source: Lab4 pp.6–7.

## Worked practice

### Problem 1 — Q1 — Compare three join algorithms

ORIGINAL TASK. Customer1,000,000 records/8,000 blocks; depositor500,000/1,000 as outer; inner key B+ index n=100. Find transfers,seeks,time and compare NL,BNL,INL using0.1ms/4ms weights. Source: Lab4 p.2.

> [!tip]- Hint
> Use h=4 under the source bound, then5 key-lookup accesses.

> [!success]- Solution
> INL:B=S=1,000+500,000×5=2,501,000,T=10,254,100ms. NL:B=1,000+500,000×8,000=4,000,001,000,S=501,000,T=402,004,100ms. BNL:B=1,000+1,000×8,000=8,001,000,S=2,000,T=808,100ms. BNL is cheapest among these under the source model.

### Problem 2 — Q2 — Compare while exposing uncertainty

ORIGINAL TASK. Compare BNL and indexed nested loops for customer5,000 tuples/500 blocks and transaction80,000/7,000, with the stated sparse primary N=7 index on customer_Number. Source: Lab4 pp.3–4.

> [!tip]- Hint
> First resolve the ordering description, then retain matching data blocks as a parameter.

> [!success]- Solution
> Customer-outer BNL:B=3,500,500,S=1,000,T=354,050ms. Conditional clustered INL with h=7:B=35,500+5,000b,S=40,500,T=165,550+500b ms. If uniform packing suggests b=2,T=166,550ms, below BNL. But the physical-ordering inconsistency and unknown match distribution prevent an unconditional exact answer; state both assumptions.

### Problem 3 — Q3 — Count the external sort

ORIGINAL TASK. b=12,M=3,b_b=1; give transfers and seeks. Source: Lab4 p.5.

> [!tip]- Hint
> Four initial runs, two merge passes; declare final-output writing.

> [!success]- Solution
> Streamed source formula:B=12×(2×2+1)=60,S=2×4+12×(4−1)=44. Materialised output:B=72,S=56. The run trace is4→2→1.

### Problem 4 — Q4 — Audit merge-join accounting

ORIGINAL TASK. Unsorted8,000/1,000-block inputs,M=100,b_b=5. Find sorting-plus-merge transfers/seeks. Source: Lab4 p.6.

> [!tip]- Hint
> Fan-in19; sort passes2 and1. Decide whether final sorted files are materialised.

> [!success]- Solution
> Materialised sorting:48,000+4,000 transfers and6,560+420 seeks. Subsequent merge:9,000 transfers/1,800 seeks. Total61,000/8,780, result-write omitted. The source streamed-sort arithmetic plus a separate scan yields52,000/6,980 but leaves missing persistence writes. True fusion avoids rereading those final streams and requires a separate buffer-feasibility check; it must not silently combine both conventions.

### Problem 5 — Q5 — Count hash cost and flag the conflict

ORIGINAL TASK. Use50 partitions,b_b=20 and include partially filled blocks for the Q4 relations. Source: Lab4 p.7.

> [!tip]- Hint
> Apply the supplied partial-block formula, then count buffers.

> [!success]- Solution
> Conditional source cost:B=27,200,S=1,000,T=6,720ms with0.1/4ms weights. However one input and50 output buffers of20 frames require1,020 frames, exceeding Q4 M=100. This arithmetic does not establish a feasible one-pass execution. Clarify the inherited memory or revise the allocation/pass assumptions.

### Problem 6 — Q6 — Answer every materialised-sort part

ORIGINAL TASK. b_r=5,b_s=3,M=3,b_b=1; final sorted results must be written before merge join. Answer(a)–(e). Source: Lab4 p.8.

> [!tip]- Hint
> Handle the in-memory input separately and include its final write.

> [!success]- Solution
> (a)r:2 initial external runs;s:one in-memory sorted sequence,no external runs required. (b)r:1 merge pass;s:0. (c)r:20 transfers;s:6 transfers for read+write. (d)merge scan:8 transfers under group-fit assumption. (e)20+6+8=34 total transfers. Join-result writing is excluded because its size is unspecified.

