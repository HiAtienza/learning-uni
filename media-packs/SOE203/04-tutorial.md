# SOE203 · Requirements Tutorial Clinic

## Video generation status
PENDING: source pack prepared; no cloud video has been generated or reviewed.

## Spanish video overview prompt
Explica esta unidad en español claro, paso a paso, para alguien que aprende de forma autodidacta. Usa únicamente el material incluido. Comienza con el problema motivador, presenta los conceptos, muestra un ejemplo visual fiel a las convenciones del curso, pausa para una pregunta y después explica la respuesta. Distingue práctica suplementaria de tareas oficiales y de soluciones oficiales. No inventes datos, fuentes, requisitos, capítulos pendientes, resultados de ejecución ni predicciones de examen. Conserva los límites y discrepancias indicados. Cierra con una actividad que el estudiante pueda intentar en Learning Uni. Cita el nombre del documento y su localizador cuando corresponda. Si falta evidencia, dilo; no rellenes el hueco. Mantén visibles las fórmulas y direcciones de flechas.

## Verified original file snapshots
- Week 4 - Tutorial Questions.docx · SHA-256 f284f9d3fcf3c340f0157aea122c5f0cc4dbe13d222eb3328430264d535e2d45
- Week 4 - Additional Tutorial Questions.docx · SHA-256 8ec3fcbf47af815f7116858d37b867214ea319dae9745391887885b6adb39d07
- Week 4 - Tutorial Questions w Answers.docx · SHA-256 979c7f08e22764c2347a2be8c3e39db2ebb4ab81e440035adf405f47f76b4dda
- Week 4 - Additional Tutorial Questions w Answers.docx · SHA-256 a017855aa76b38a5f380881f7623a170dd50728a245f46e5d13937b62021c00d

## Source material

### Snapshot: content/reviewed/SOE203/04-tutorial/tutor.md
SHA-256: 07323c0e1f5366403b09089ac74591522b0777364df272fd6595c11254c36957

# Requirements tutorial clinic

Source-grounded web edition: **Week 4 - Tutorial Questions.docx (six questions)** and **Week 4 - Additional Tutorial Questions.docx (eight questions)**, read in full. Use Unit 04 as the conceptual reference. Both supplied Week 4 answer sheets have now been inspected and reconciled. Collapsed solutions distinguish a faithful supplied-answer summary from local commentary; neither is an official exam marking scheme.

## Your route through this tutorial

Work through all fourteen tasks in Recall & practice. Each has an adjacent hint and complete explanation. First attempt from memory, then compare the supplied answer, its scope and unresolved criteria. Both earlier question-only files and the new answer DOCX files are preserved in Source library.

## 1. Classical Waterfall and evolving requirements

The worksheet compares an upfront approved requirements baseline with incremental Agile elaboration. Waterfall aims to reduce expensive downstream misunderstandings. Agile still performs requirements work and validation repeatedly. Avoid the absolute claim that Agile has no upfront work or Waterfall can never revisit a decision. Source: Tutorial Q1; Unit 04 notes.

## 2. Feasibility needs several kinds of evidence

The parking budget addresses only one aspect. Check technical feasibility, operational fit, time/staff capacity and relevant constraints. When answering elicitation questions, connect the challenge to a concrete technique: observation for tacit practice, prototypes for unclear interaction needs, or workshops for conflicts. Source: Tutorial Q2–3.

## 3. Convert a wish into testable behavior

Flight alerts, unusual withdrawals, approaching drivers and unlocked doors each need a trigger, defined conditions, response and acceptance criteria. User requirements express stakeholder goals; system requirements elaborate behavior. Terms such as instantly, exactly and unusual remain unresolved until criteria are agreed. The new sheets supply example values: flight 30 seconds, bank 3× average/10 seconds, driver updates every 5 seconds, and geofence/door notification within 30 seconds. Treat them as values in these supplied examples, not universal requirements; the sources leave some measurement and sensor semantics open. Source: Tutorial Q4; Additional Q1–3.

## 4. Separate functions and quality expectations

Search, filtering, workout sync and offline downloading describe functions. Supplied targets are search 2 seconds/95%, workout sync completion 2 seconds, product filtering 1.5 seconds/95%, and download initiation with visible progress within 1 second. Completion and initiation are distinct events; normal load still needs definition. FURPS Performance covers those timing concerns; security is grouped under Functionality in the supplied course framework; concurrent-save integrity concerns Reliability. FURPS categories do not replace functional/quality analysis. Source: Tutorial Q5; Additional Q4–8.

## 5. Reason about interactions

The 500 ms signed-answer problem is a possible resource/latency conflict. Mark the interaction, explain a concrete mechanism, propose a design and identify what needs testing. The supplied Q6 answer proposes acknowledging receipt before signing completes, then asynchronous signing/audit. Preserve that proposal while distinguishing receipt from signed acceptance and requiring explicit failure/recovery semantics; it cannot silently weaken the original requirement. Source: Tutorial Q6.

## Review

Explain one requirement without using vague speed or accuracy language. Identify at least one criterion still requiring stakeholder agreement. Compare your complete fourteen attempts with the local worked reasoning, then revisit the cards marked for review. Supplied example thresholds are now visible; they are not measured results, official exam marks or predictions.

## Week 4 supplied answers — Boundaries worth checking

[[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Tutorial Questions w Answers.docx|Main answer sheet]]: six unchanged questions with new answers. [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Additional answer sheet]]: eight unchanged questions with new answers. Their numbers are answer-example requirements; the original question text did not prescribe them.

- Main Q4: the answer reacts to departure-time changes, not only delays; it combines an Interactor need with a Domain data trigger.
- Main Q6: a −1 matrix entry indicates a likely conflict, not measured impossibility. Its asynchronous-signing trade-off needs explicit acknowledgement semantics.
- Additional Q6: one second applies to starting the download with progress, not finishing an entire episode.
- Additional Q7: “more than 5” consecutive failures within 10 minutes triggers a 30-minute lock plus identity re-verification; preserve the strict boundary and the supplied Functionality label.
- Additional Q8: Reliability is the source category; preserving all edits is an acceptance property, not proof that a merge algorithm has been implemented.

Use the fourteen original practice identities to revisit saved answers. Existing ratings and written attempts remain your records; revised source explanations do not reset them or establish new mastery.



### Snapshot: content/reviewed/SOE203/04-tutorial/practice.md
SHA-256: e6700efa8940974d2ba6601f533706c7b089b6d3bbee83b3e9019d602bc5e346

# Requirements tutorial clinic: recall and practice

Web tutor edition. The fourteen original tasks now include **SUPPLIED COURSE ANSWER — not an exam marking scheme**, followed by separately labelled local commentary. Atomic recall retains its earlier source lines and IDs. No official marks or learner mastery are inferred. Sources: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes. Attempt before opening help.

## Atomic Recall

### Card 01 — Why does a user requirement need elaboration?
> [!success]- Answer
> Stakeholder goals must be translated into observable behavior, triggers, conditions and agreed acceptance criteria.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, tutorial Q4; additional Q1–3.

### Card 02 — Is a budget alone a feasibility argument?
> [!success]- Answer
> No. Technical capability, operational fit, schedule and constraints must also be assessed.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, tutorial Q2.

### Card 03 — Does Agile avoid requirements work?
> [!success]- Answer
> No. It revisits requirements incrementally; classical Waterfall invests earlier to reduce costly downstream misunderstanding.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, tutorial Q1.

### Card 04 — Is an unmeasured quality adjective testable?
> [!success]- Answer
> No. Define an agreed measure, conditions and threshold; do not silently invent official values.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, tutorial Q5; additional Q4–6.

### Card 05 — What do interactor, indirect and domain viewpoints mean?
> [!success]- Answer
> Interactor uses/interfaces directly; indirect has interests without direct use; domain contributes rules or constraints from the application domain.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, tutorial Q4.

### Card 06 — How do functional and FURPS classifications differ?
> [!success]- Answer
> Functional versus quality separates behavior from its constraints; FURPS categories group concerns and are not a one-to-one synonym for that separation.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, tutorial Q5; additional Q7–8.

## Progressive Practice

### Practice 1 — Upfront requirements

**ORIGINAL COURSE EXERCISE — supplied answer with local commentary.**

Chapter 3 studied Agile, where requirements evolve sprint by sprint. Chapter 4 studies Waterfall, where an entire Requirements Engineering phase is completed and approved before design begins. Explain, in your own words, why Waterfall requires this upfront investment while Agile does not, and what risk Waterfall is trying to avoid by doing so.

Source: Week 4 - Tutorial Questions.docx, Question 1.

> [!tip]- Hint
> Ask when misunderstanding becomes expensive and when requirements are revisited.

> [!success]- Solution
> **SUPPLIED COURSE ANSWER (faithful summary):** Upfront investment reduces downstream rework because design, code and testing depend on the approved SRS. The supplied comparison describes Waterfall upfront/sign-off/change control versus Agile incremental refinement and working-software feedback.
>
> Source: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Tutorial Questions w Answers.docx|Week 4 - Tutorial Questions w Answers.docx]], Question 1.
>
> **LOCAL COMMENTARY:** The answer is a course comparison, not a claim that Agile has no early planning or Waterfall can never change.

### Practice 2 — Feasibility gap

**ORIGINAL COURSE EXERCISE — supplied answer with local commentary.**

A Feasibility Report for a new campus parking-reservation system concludes: “The budget covers a two-semester development team, so the project should proceed.” Identify what's missing from this feasibility judgment.

Source: Week 4 - Tutorial Questions.docx, Question 2.

> [!tip]- Hint
> Test technical, operational and schedule feasibility as well as finance.

> [!success]- Solution
> **SUPPLIED COURSE ANSWER (faithful summary):** Check organizational objectives, engineering with current technology within budget and schedule, and integration with existing/legacy infrastructure. The budget statement establishes only part of that judgment.
>
> Source: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Tutorial Questions w Answers.docx|Week 4 - Tutorial Questions w Answers.docx]], Question 2.
>
> **LOCAL COMMENTARY:** Two semesters is not by itself a schedule-feasibility demonstration; operational fit remains useful local elaboration.

### Practice 3 — Elicitation challenge

**ORIGINAL COURSE EXERCISE — supplied answer with local commentary.**

Name and explain one elicitation challenge, and explain how a specific technique helps resolve that challenge.

Source: Week 4 - Tutorial Questions.docx, Question 3.

> [!tip]- Hint
> Connect the technique to the cause, not just its name.

> [!success]- Solution
> **SUPPLIED COURSE ANSWER (faithful summary):** The sheet offers four challenge/technique pairs: tacit knowledge → ethnography/shadowing; domain jargon → shared domain glossary; unrealistic wish lists → feasibility/cost-value matrix; political conflicts → multi-perspective workshops.
>
> Source: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Tutorial Questions w Answers.docx|Week 4 - Tutorial Questions w Answers.docx]], Question 3.
>
> **LOCAL COMMENTARY:** Any chosen pair must explain how the technique addresses that specific cause.

### Practice 4 — Flight delay and viewpoints

**ORIGINAL COURSE EXERCISE — supplied answer with local commentary.**

A stakeholder says: “I want to know instantly if my flight gets delayed.” Write one User Requirement and one corresponding System Requirement derived from it. Then state which of the three VOA viewpoints — Interactor, Indirect, or Domain — each requirement primarily represents, and why.

Source: Week 4 - Tutorial Questions.docx, Question 4.

> [!tip]- Hint
> Keep stakeholder goal separate from system detail; delivery thresholds need agreement.

> [!success]- Solution
> **SUPPLIED COURSE ANSWER (faithful summary):** UR: notify the passenger when the booked flight’s departure time changes. SR: WHEN departure time is updated in the airline operations system, push a notification to the registered device within 30 seconds. The UR is Interactor; the SR serves that need and also reflects Domain through its authoritative airline-data trigger.
>
> Source: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Tutorial Questions w Answers.docx|Week 4 - Tutorial Questions w Answers.docx]], Question 4.
>
> **LOCAL COMMENTARY:** The 30-second value is in the supplied answer. “Departure time changes” is broader than only delays; data freshness and the intended event scope still need definition. A system requirement is not automatically a Domain viewpoint.

### Practice 5 — Course search and FURPS

**ORIGINAL COURSE EXERCISE — supplied answer with local commentary.**

A stakeholder statement blends a feature with a quality expectation: “The mobile app should let me search for a course and get results back right away.” Split this into a Functional Requirement and a Non-Functional Requirement, and identify which FURPS+ category the NFR belongs to. Then, in one or two sentences, explain why FURPS+'s F category is not simply a synonym for a Functional Requirement.

Source: Week 4 - Tutorial Questions.docx, Question 5.

> [!tip]- Hint
> One statement describes a function; the other constrains response time.

> [!success]- Solution
> **SUPPLIED COURSE ANSWER (faithful summary):** FR: search by course name or code and show matching results. NFR: return results within 2 seconds for 95% of queries under normal load; category Performance. FURPS Functionality is a category bucket; an FR is a particular requirement statement.
>
> Source: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Tutorial Questions w Answers.docx|Week 4 - Tutorial Questions w Answers.docx]], Question 5.
>
> **LOCAL COMMENTARY:** These numbers come from the answer sheet. Define normal load, query workload and timing endpoints before treating them as an executable acceptance procedure.

### Practice 6 — Signing versus 500 ms

**ORIGINAL COURSE EXERCISE — supplied answer with local commentary.**

Two requirements are proposed for an online exam system: (1) “Every submitted answer shall be recorded with a tamper-evident cryptographic signature,” and (2) “The system shall accept and confirm a submitted answer within 500 milliseconds.” Using a Matrix-Based Interaction Analysis approach, explain whether these two requirements are likely to conflict, and if so, suggest one architectural trade-off that could resolve it.

Source: Week 4 - Tutorial Questions.docx, Question 6.

> [!tip]- Hint
> Separate a plausible resource conflict from a demonstrated impossibility.

> [!success]- Solution
> **SUPPLIED COURSE ANSWER (faithful summary):** The sheet assigns a likely −1 interaction: signing and secure-log I/O compete with the 500 ms response budget, especially near deadlines. Its proposed trade-off acknowledges receipt before signing finishes, then computes/appends the signature asynchronously and audits that step.
>
> Source: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Tutorial Questions w Answers.docx|Week 4 - Tutorial Questions w Answers.docx]], Question 6.
>
> **LOCAL COMMENTARY:** This is the supplied proposal, not a demonstrated implementation or guarantee. Distinguish receipt from durable signed acceptance; specify pending/failure/retry/recovery behavior. Confirm the changed acknowledgement semantics against both original requirements rather than silently weakening tamper evidence.

### Practice 7 — Unusual bank withdrawal

**ORIGINAL COURSE EXERCISE — supplied answer with local commentary.**

A stakeholder says: "I want to be alerted the moment there's a large, unusual withdrawal from my account." Write one User Requirement and one corresponding System Requirement derived from it.

Source: Week 4 - Additional Tutorial Questions.docx, Question 1.

> [!tip]- Hint
> Large/unusual need defined rules; the event source and latency matter.

> [!success]- Solution
> **SUPPLIED COURSE ANSWER (faithful summary):** UR: alert the holder about an unusually large withdrawal. SR: WHEN a withdrawal exceeds 3 times the account’s average monthly withdrawal amount, send push and SMS within 10 seconds of transaction processing.
>
> Source: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Week 4 - Additional Tutorial Questions w Answers.docx]], Question 1.
>
> **LOCAL COMMENTARY:** The supplied example fixes the multiplier, channels and latency; averaging period/calculation and zero-history behavior remain unspecified.

### Practice 8 — Driver location

**ORIGINAL COURSE EXERCISE — supplied answer with local commentary.**

A stakeholder says: "I want to see exactly where my driver is before they arrive." Write one User Requirement and one corresponding System Requirement derived from it.

Source: Week 4 - Additional Tutorial Questions.docx, Question 2.

> [!tip]- Hint
> A sampled location is not infinitely accurate or continuously fresh.

> [!success]- Solution
> **SUPPLIED COURSE ANSWER (faithful summary):** UR: show the assigned driver from ride acceptance until pickup. SR: WHILE the ride is in “driver en route”, update the position on the rider’s map every 5 seconds.
>
> Source: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Week 4 - Additional Tutorial Questions w Answers.docx]], Question 2.
>
> **LOCAL COMMENTARY:** Five-second updates are the supplied value; they do not establish exact location accuracy or define stale/offline handling.

### Practice 9 — Unlocked door

**ORIGINAL COURSE EXERCISE — supplied answer with local commentary.**

A stakeholder says: "I want to know right away if my front door is left unlocked after I leave the house." Write one User Requirement and one corresponding System Requirement derived from it.

Source: Week 4 - Additional Tutorial Questions.docx, Question 3.

> [!tip]- Hint
> Departure and unlocked detection both need reliable defined evidence.

> [!success]- Solution
> **SUPPLIED COURSE ANSWER (faithful summary):** UR: notify the homeowner about an unlocked door after leaving. SR: WHEN the homeowner’s phone exits the home geofence and the sensor reports unlocked, push a notification within 30 seconds.
>
> Source: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Week 4 - Additional Tutorial Questions w Answers.docx]], Question 3.
>
> **LOCAL COMMENTARY:** The sheet supplies the geofence trigger and latency; sensor/geofence reliability and false departure handling remain separate acceptance questions. A grace period is local commentary, not in this answer.

### Practice 10 — Workout sync

**ORIGINAL COURSE EXERCISE — supplied answer with local commentary.**

A stakeholder statement blends a feature with a quality expectation: "The fitness app should let me log a workout and have it sync to my watch without any lag." Split this into a Functional Requirement and a Non-Functional Requirement, and identify which FURPS+ category the NFR belongs to.

Source: Week 4 - Additional Tutorial Questions.docx, Question 4.

> [!tip]- Hint
> Do not discard the sync function while separating performance.

> [!success]- Solution
> **SUPPLIED COURSE ANSWER (faithful summary):** FR: log a workout and sync it to the connected smartwatch. NFR: complete sync within 2 seconds of logging; category Performance.
>
> Source: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Week 4 - Additional Tutorial Questions w Answers.docx]], Question 4.
>
> **LOCAL COMMENTARY:** This is a completion target, unlike the download-start target below. Define connectivity, data volume and failure/pending behavior separately.

### Practice 11 — Price filtering

**ORIGINAL COURSE EXERCISE — supplied answer with local commentary.**

A stakeholder statement blends a feature with a quality expectation: "The store app should let me filter products by price and show me the results without the page feeling slow." Split this into a Functional Requirement and a Non-Functional Requirement, and identify which FURPS+ category the NFR belongs to.

Source: Week 4 - Additional Tutorial Questions.docx, Question 5.

> [!tip]- Hint
> Specify results behavior separately from response time.

> [!success]- Solution
> **SUPPLIED COURSE ANSWER (faithful summary):** FR: filter the product list by specified price range. NFR: display results within 1.5 seconds for 95% of filter requests under normal load; category Performance.
>
> Source: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Week 4 - Additional Tutorial Questions w Answers.docx]], Question 5.
>
> **LOCAL COMMENTARY:** Keep the percentile as well as the latency. Dataset, device, load and event endpoints still need an agreed measurement procedure.

### Practice 12 — Offline episode

**ORIGINAL COURSE EXERCISE — supplied answer with local commentary.**

A stakeholder statement blends a feature with a quality expectation: "The app should let me download an episode for offline viewing and have it ready almost instantly." Split this into a Functional Requirement and a Non-Functional Requirement, and identify which FURPS+ category the NFR belongs to.

Source: Week 4 - Additional Tutorial Questions.docx, Question 6.

> [!tip]- Hint
> Offline playback and download completion are different observable events.

> [!success]- Solution
> **SUPPLIED COURSE ANSWER (faithful summary):** FR: download an episode for offline viewing. NFR: begin downloading with visible progress within 1 second of the tap; category Performance.
>
> Source: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Week 4 - Additional Tutorial Questions w Answers.docx]], Question 6.
>
> **LOCAL COMMENTARY:** The supplied target is download initiation with feedback, not complete transfer within one second. Offline availability still depends on completing the download.

### Practice 13 — Bank transfer security

**ORIGINAL COURSE EXERCISE — supplied answer with local commentary.**

A stakeholder statement blends a feature with a quality expectation: "The banking app should let customers transfer money between accounts, but there's no way anyone should be able to guess or brute-force their way into someone else's account." Split this into a Functional Requirement and a Non-Functional Requirement, and identify which FURPS+ category the NFR belongs to.

Source: Week 4 - Additional Tutorial Questions.docx, Question 7.

> [!tip]- Hint
> Security belongs to the course FURPS Functionality grouping; also define concrete controls.

> [!success]- Solution
> **SUPPLIED COURSE ANSWER (faithful summary):** FR: allow an authenticated customer to transfer between their own linked accounts. NFR: IF more than 5 consecutive failed logins occur for an account within 10 minutes, THEN lock it for 30 minutes and require identity re-verification before further attempts. The sheet labels this unwanted-behavior EARS and Functionality.
>
> Source: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Week 4 - Additional Tutorial Questions w Answers.docx]], Question 7.
>
> **LOCAL COMMENTARY:** “More than 5” means the condition is met on the sixth consecutive failure within the window. This concrete security response does not establish an absolute guarantee against all compromise; retain the source’s FURPS classification.

### Practice 14 — Concurrent editor

**ORIGINAL COURSE EXERCISE — supplied answer with local commentary.**

A stakeholder statement blends a feature with a quality expectation: "The shared document editor should let two people edit the same page at once, but it must never silently lose one person's changes when both save around the same time." Split this into a Functional Requirement and a Non-Functional Requirement, and identify which FURPS+ category the NFR belongs to.

Source: Week 4 - Additional Tutorial Questions.docx, Question 8.

> [!tip]- Hint
> State conflict behavior and correctness properties.

> [!success]- Solution
> **SUPPLIED COURSE ANSWER (faithful summary):** FR: two or more users edit the same page concurrently. NFR: WHEN they save within the same editing session, preserve all users’ changes without discarding input; category Reliability.
>
> Source: [[10_UNIVERSITY_CS/Software Engineering 1/Sources/Learning Mall 2026-10-12/Week 4 - Additional Tutorial Questions w Answers.docx|Week 4 - Additional Tutorial Questions w Answers.docx]], Question 8.
>
> **LOCAL COMMENTARY:** The answer expands the prompt’s two users to two or more. The preservation property still needs conflict/failure tests and agreed resolution semantics; no specific merge algorithm is supplied.

