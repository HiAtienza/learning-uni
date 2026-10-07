# SOE203 · Requirements Tutorial Clinic

## Video generation status
PENDING: source pack prepared; no cloud video has been generated or reviewed.

## Spanish video overview prompt
Explica esta unidad en español claro, paso a paso, para alguien que aprende de forma autodidacta. Usa únicamente el material incluido. Comienza con el problema motivador, presenta los conceptos, muestra un ejemplo visual fiel a las convenciones del curso, pausa para una pregunta y después explica la respuesta. Distingue práctica suplementaria de tareas oficiales y de soluciones oficiales. No inventes datos, fuentes, requisitos, capítulos pendientes, resultados de ejecución ni predicciones de examen. Conserva los límites y discrepancias indicados. Cierra con una actividad que el estudiante pueda intentar en Learning Uni. Cita el nombre del documento y su localizador cuando corresponda. Si falta evidencia, dilo; no rellenes el hueco. Mantén visibles las fórmulas y direcciones de flechas.

## Verified original file snapshots
- Week 4 - Tutorial Questions.docx · SHA-256 f284f9d3fcf3c340f0157aea122c5f0cc4dbe13d222eb3328430264d535e2d45
- Week 4 - Additional Tutorial Questions.docx · SHA-256 8ec3fcbf47af815f7116858d37b867214ea319dae9745391887885b6adb39d07

## Source material

### Snapshot: content/reviewed/SOE203/04-tutorial/tutor.md
SHA-256: 01c46130041486c351e7ddbc2a11176697ef926e9e69219c436b69472ed099bf

# Requirements tutorial clinic

Source-grounded web edition: **Week 4 - Tutorial Questions.docx (six questions)** and **Week 4 - Additional Tutorial Questions.docx (eight questions)**, read in full. Use Unit 04 as the conceptual reference. These answer explanations are local teaching reasoning, not an official marking scheme.

## Your route through this tutorial

Work through all fourteen tasks in Recall & practice. Each has an adjacent hint and complete explanation. First attempt from memory, then compare the scope, unresolved criteria and reasoning. Original DOCX files are preserved in Source library.

## 1. Classical Waterfall and evolving requirements

The worksheet compares an upfront approved requirements baseline with incremental Agile elaboration. Waterfall aims to reduce expensive downstream misunderstandings. Agile still performs requirements work and validation repeatedly. Avoid the absolute claim that Agile has no upfront work or Waterfall can never revisit a decision. Source: Tutorial Q1; Unit 04 notes.

## 2. Feasibility needs several kinds of evidence

The parking budget addresses only one aspect. Check technical feasibility, operational fit, time/staff capacity and relevant constraints. When answering elicitation questions, connect the challenge to a concrete technique: observation for tacit practice, prototypes for unclear interaction needs, or workshops for conflicts. Source: Tutorial Q2–3.

## 3. Convert a wish into testable behavior

Flight alerts, unusual withdrawals, approaching drivers and unlocked doors each need a trigger, defined conditions, response and acceptance criteria. User requirements express stakeholder goals; system requirements elaborate behavior. Terms such as instantly, exactly and unusual remain unresolved until criteria are agreed. Suggested criteria in solutions are proposals, not supplied instructor values. Source: Tutorial Q4; Additional Q1–3.

## 4. Separate functions and quality expectations

Search, filtering, workout sync and offline downloading describe functions. Timing expectations constrain them under agreed conditions. FURPS Performance covers those timing concerns; security is grouped under Functionality in the supplied course framework; concurrent-save integrity concerns Reliability. FURPS categories do not replace functional/quality analysis. Source: Tutorial Q5; Additional Q4–8.

## 5. Reason about interactions

The 500 ms signed-answer problem is a possible resource/latency conflict. Mark the interaction, explain a concrete mechanism, propose a design and identify what needs testing. Deferring signing changes what acceptance means and requires agreed semantics; it cannot silently weaken the original requirement. Source: Tutorial Q6.

## Review

Explain one requirement without using vague speed or accuracy language. Identify at least one criterion still requiring stakeholder agreement. Compare your complete fourteen attempts with the local worked reasoning, then revisit the cards marked for review. No official thresholds or exam predictions are supplied here.



### Snapshot: content/reviewed/SOE203/04-tutorial/practice.md
SHA-256: 8f4f3232fc2f2fb7a27b619a23112d1ab4ba959c96df39a6c84b89f4a5760f76

# Requirements tutorial clinic: recall and practice

Web tutor edition. New practice below is **SUPPLEMENTARY PRACTICE**, not an official assignment or marking scheme. Sources: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes. Attempt before opening help.

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

**ORIGINAL COURSE EXERCISE — supplementary worked reasoning.**

Chapter 3 studied Agile, where requirements evolve sprint by sprint. Chapter 4 studies Waterfall, where an entire Requirements Engineering phase is completed and approved before design begins. Explain, in your own words, why Waterfall requires this upfront investment while Agile does not, and what risk Waterfall is trying to avoid by doing so.

Source: Week 4 - Tutorial Questions.docx, Question 1.

> [!tip]- Hint
> Ask when misunderstanding becomes expensive and when requirements are revisited.

> [!success]- Solution
> Classical Waterfall completes and approves a broad requirements baseline before downstream design, reducing the risk of building against misunderstood/incomplete needs and expensive later rework. Agile still elicits, specifies and validates requirements, but revisits and elaborates them in increments/sprints using feedback. Neither model guarantees that change disappears. The worksheet phrasing is a comparison of approaches, not a claim that all real projects follow strict one-pass phases.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, tutorial Q1.

### Practice 2 — Feasibility gap

**ORIGINAL COURSE EXERCISE — supplementary worked reasoning.**

A Feasibility Report for a new campus parking-reservation system concludes: “The budget covers a two-semester development team, so the project should proceed.” Identify what's missing from this feasibility judgment.

Source: Week 4 - Tutorial Questions.docx, Question 2.

> [!tip]- Hint
> Test technical, operational and schedule feasibility as well as finance.

> [!success]- Solution
> Check whether the technology/integration/data access can support the functions; whether users/processes can adopt it; whether staffing and milestones fit two semesters; and relevant constraints/risks. Having funding does not establish these. State evidence needed for each and assess before a proceed decision.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, tutorial Q2.

### Practice 3 — Elicitation challenge

**ORIGINAL COURSE EXERCISE — supplementary worked reasoning.**

Name and explain one elicitation challenge, and explain how a specific technique helps resolve that challenge.

Source: Week 4 - Tutorial Questions.docx, Question 3.

> [!tip]- Hint
> Connect the technique to the cause, not just its name.

> [!success]- Solution
> Example: stakeholders describe the formal process but omit tacit workarounds. Observation/ethnography of actual parking operations reveals interruptions and exceptions; interviews then validate the inferred needs. Alternative: conflicting stakeholder priorities can be clarified in a facilitated workshop with explicit scenarios and negotiated trade-offs. These are labelled answer examples.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, tutorial Q3.

### Practice 4 — Flight delay and viewpoints

**ORIGINAL COURSE EXERCISE — supplementary worked reasoning.**

A stakeholder says: “I want to know instantly if my flight gets delayed.” Write one User Requirement and one corresponding System Requirement derived from it. Then state which of the three VOA viewpoints — Interactor, Indirect, or Domain — each requirement primarily represents, and why.

Source: Week 4 - Tutorial Questions.docx, Question 4.

> [!tip]- Hint
> Keep stakeholder goal separate from system detail; delivery thresholds need agreement.

> [!success]- Solution
> User: The passenger shall be notified when their flight is delayed. System proposal: WHEN an authoritative flight-status update changes a subscribed flight to delayed, the app shall send the subscribed passenger an alert identifying the flight and updated departure information within an agreed maximum latency. The passenger goal is an interactor view. The system behavior primarily serves that view; a system requirement is not automatically a domain viewpoint. Domain constraints would include authoritative airline status rules, and indirect interests could include operations/compliance. Instant is unresolved until measurable criteria and source freshness are agreed.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, tutorial Q4.

### Practice 5 — Course search and FURPS

**ORIGINAL COURSE EXERCISE — supplementary worked reasoning.**

A stakeholder statement blends a feature with a quality expectation: “The mobile app should let me search for a course and get results back right away.” Split this into a Functional Requirement and a Non-Functional Requirement, and identify which FURPS+ category the NFR belongs to. Then, in one or two sentences, explain why FURPS+'s F category is not simply a synonym for a Functional Requirement.

Source: Week 4 - Tutorial Questions.docx, Question 5.

> [!tip]- Hint
> One statement describes a function; the other constrains response time.

> [!success]- Solution
> FR: The app shall allow users to search the course catalog using defined criteria. NFR proposal: Under an agreed load/dataset/network condition, search results shall be returned within an agreed latency threshold. Category Performance. FURPS Functionality groups functional capabilities and associated feature/security concerns; it does not make every concern in F a behavior specification or replace FR/NFR analysis. No official numeric threshold is supplied.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, tutorial Q5.

### Practice 6 — Signing versus 500 ms

**ORIGINAL COURSE EXERCISE — supplementary worked reasoning.**

Two requirements are proposed for an online exam system: (1) “Every submitted answer shall be recorded with a tamper-evident cryptographic signature,” and (2) “The system shall accept and confirm a submitted answer within 500 milliseconds.” Using a Matrix-Based Interaction Analysis approach, explain whether these two requirements are likely to conflict, and if so, suggest one architectural trade-off that could resolve it.

Source: Week 4 - Tutorial Questions.docx, Question 6.

> [!tip]- Hint
> Separate a plausible resource conflict from a demonstrated impossibility.

> [!success]- Solution
> Matrix entry: possible negative interaction because signing/persistence consumes the same latency budget; conflict is not inevitable without measurements. A proposed design uses efficient signing/key management and durable transactional recording before acknowledgement, then moves nonessential work asynchronously. If signing is deferred, define whether acknowledgement means durable accepted or merely queued; that change requires stakeholder agreement and may violate the original signed-record requirement. Benchmark under specified load; do not remove tamper evidence to meet latency silently.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, tutorial Q6.

### Practice 7 — Unusual bank withdrawal

**ORIGINAL COURSE EXERCISE — supplementary worked reasoning.**

A stakeholder says: "I want to be alerted the moment there's a large, unusual withdrawal from my account." Write one User Requirement and one corresponding System Requirement derived from it.

Source: Week 4 - Additional Tutorial Questions.docx, Question 1.

> [!tip]- Hint
> Large/unusual need defined rules; the event source and latency matter.

> [!success]- Solution
> User: The account holder shall be alerted to withdrawals meeting the agreed unusual/large criteria. System proposal: WHEN a withdrawal satisfies configured, approved amount/anomaly rules, the system shall notify the holder via agreed channels with relevant transaction details within an agreed latency. Amount threshold, anomaly rule, false-positive policy, channel and latency remain to be agreed.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, additional Q1.

### Practice 8 — Driver location

**ORIGINAL COURSE EXERCISE — supplementary worked reasoning.**

A stakeholder says: "I want to see exactly where my driver is before they arrive." Write one User Requirement and one corresponding System Requirement derived from it.

Source: Week 4 - Additional Tutorial Questions.docx, Question 2.

> [!tip]- Hint
> A sampled location is not infinitely accurate or continuously fresh.

> [!success]- Solution
> User: The customer shall view the approaching driver location. System proposal: The app shall show the latest authorized driver position and its update timestamp on a map, refreshing under agreed frequency/accuracy conditions before arrival. Define stale/offline behavior and permission boundaries. Exactly requires an agreed accuracy tolerance; no particular GPS precision is promised by the source.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, additional Q2.

### Practice 9 — Unlocked door

**ORIGINAL COURSE EXERCISE — supplementary worked reasoning.**

A stakeholder says: "I want to know right away if my front door is left unlocked after I leave the house." Write one User Requirement and one corresponding System Requirement derived from it.

Source: Week 4 - Additional Tutorial Questions.docx, Question 3.

> [!tip]- Hint
> Departure and unlocked detection both need reliable defined evidence.

> [!success]- Solution
> User: The resident shall be notified if the door remains unlocked after departure. System proposal: WHEN the agreed departure signal is detected AND the door sensor reports unlocked after an agreed grace period, the system shall notify the resident within agreed latency and identify the door. Departure signal, sensor error/offline handling, grace period and latency remain unresolved.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, additional Q3.

### Practice 10 — Workout sync

**ORIGINAL COURSE EXERCISE — supplementary worked reasoning.**

A stakeholder statement blends a feature with a quality expectation: "The fitness app should let me log a workout and have it sync to my watch without any lag." Split this into a Functional Requirement and a Non-Functional Requirement, and identify which FURPS+ category the NFR belongs to.

Source: Week 4 - Additional Tutorial Questions.docx, Question 4.

> [!tip]- Hint
> Do not discard the sync function while separating performance.

> [!success]- Solution
> FR: Let the user record a workout and synchronize it to the paired authorized watch. NFR: Under specified connectivity/data/load conditions, sync completes within an agreed latency, with visible pending/failure state. FURPS Performance for the timing concern. No official zero-lag guarantee or threshold exists.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, additional Q4.

### Practice 11 — Price filtering

**ORIGINAL COURSE EXERCISE — supplementary worked reasoning.**

A stakeholder statement blends a feature with a quality expectation: "The store app should let me filter products by price and show me the results without the page feeling slow." Split this into a Functional Requirement and a Non-Functional Requirement, and identify which FURPS+ category the NFR belongs to.

Source: Week 4 - Additional Tutorial Questions.docx, Question 5.

> [!tip]- Hint
> Specify results behavior separately from response time.

> [!success]- Solution
> FR: Filter displayed products by a chosen price range. NFR: Under agreed dataset/device/network/load conditions, display filtered results within an agreed response-time threshold. FURPS Performance. Feeling slow needs measurable acceptance criteria, not an invented numeric requirement.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, additional Q5.

### Practice 12 — Offline episode

**ORIGINAL COURSE EXERCISE — supplementary worked reasoning.**

A stakeholder statement blends a feature with a quality expectation: "The app should let me download an episode for offline viewing and have it ready almost instantly." Split this into a Functional Requirement and a Non-Functional Requirement, and identify which FURPS+ category the NFR belongs to.

Source: Week 4 - Additional Tutorial Questions.docx, Question 6.

> [!tip]- Hint
> Offline playback and download completion are different observable events.

> [!success]- Solution
> FR: Allow an authorized user to download an eligible episode and play it offline. NFR: Under defined content-size/network/device conditions, download completes within an agreed threshold or supplies agreed progress/availability feedback. FURPS Performance for completion speed. Cannot guarantee instant transfer independent of episode size and connectivity.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, additional Q6.

### Practice 13 — Bank transfer security

**ORIGINAL COURSE EXERCISE — supplementary worked reasoning.**

A stakeholder statement blends a feature with a quality expectation: "The banking app should let customers transfer money between accounts, but there's no way anyone should be able to guess or brute-force their way into someone else's account." Split this into a Functional Requirement and a Non-Functional Requirement, and identify which FURPS+ category the NFR belongs to.

Source: Week 4 - Additional Tutorial Questions.docx, Question 7.

> [!tip]- Hint
> Security belongs to the course FURPS Functionality grouping; also define concrete controls.

> [!success]- Solution
> FR: Allow authenticated authorized customers to transfer between eligible accounts. Quality/security requirement: Resist credential guessing with agreed authentication, rate limiting and monitoring criteria under a defined threat model; verify these controls and failure behavior. In the course FURPS grouping, security is in Functionality (F); this does not mean that broad security assurance equals a single functional behavior. No absolute guarantee that compromise is impossible is justified.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, additional Q7.

### Practice 14 — Concurrent editor

**ORIGINAL COURSE EXERCISE — supplementary worked reasoning.**

A stakeholder statement blends a feature with a quality expectation: "The shared document editor should let two people edit the same page at once, but it must never silently lose one person's changes when both save around the same time." Split this into a Functional Requirement and a Non-Functional Requirement, and identify which FURPS+ category the NFR belongs to.

Source: Week 4 - Additional Tutorial Questions.docx, Question 8.

> [!tip]- Hint
> State conflict behavior and correctness properties.

> [!success]- Solution
> FR: Support simultaneous edits by two authorized users to the same document. NFR: Concurrent saves shall preserve committed changes or explicitly surface unresolved conflicts, under defined concurrent-operation and failure cases. FURPS Reliability for data integrity; implementation could also have functional conflict-resolution requirements. Never silently lose is an acceptance property requiring concurrency/failure tests, not just a fast response.
>
> Source: Week 4 - Tutorial Questions.docx / Week 4 - Additional Tutorial Questions.docx; Unit 04 reviewed notes, additional Q8.

