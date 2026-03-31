# Scarcity–Denial Framework — User Manual

## Version 1.2

*Covering SRIT v2.2 · DAI v2.1 · DDA v1.6*

---

## How to Use This Manual

This manual covers all three analytical instruments in the Scarcity–Denial Framework — SRIT, DAI, and DDA. It is a reference document. It does not contain operational instructions for running the tools — those are in the nine standalone session documents listed below.

**Operational documents — use these to run the tools (Desktop model):**

| Purpose | Document |
|---------|----------|
| Open companion session, construct SDS, initialise full-run companion role | `SDS_Claude_Construction_Desktop_v05.md` |
| SRIT → DAI boundary check | `DAI_Claude_BoundaryCheck_v0_4_0.md` |
| DAI → DDA boundary check | `DDA_Claude_BoundaryCheck_v0_4_2.md` |
| SRIT Prompt 6 Stage 1 review | `SRIT_Claude_Review_v0_3_6.md` |
| DAI Prompt 5 Stage 1 review | `DAI_Claude_Review_v0_4_1.md` |
| DDA Prompt 5 Stage 1 review | `DDA_Claude_Review_v0_4_5.md` |

The Runtime Guide (`SDF_Runtime_Guide_Desktop`) specifies exactly when each document is uploaded and in what order.

**This manual — use this to understand what the tools produce:**

Read the relevant module section before your first run. Return to it when interpreting outputs, handling unexpected results, or deciding whether to rerun.

---

## Contents

**Part 1 — The Framework**
1. The Scarcity–Denial Canon
2. The Three-Instrument Pipeline
3. Platform and Model Requirements

**Part 2 — SRIT: Scarce Resource Identification Tool**
4. What SRIT Does
5. The System Definition Statement
6. The Boundary Audit
7. Interpreting the SRIT Run Record
8. Interpreting Contested Declarations
9. Adjacent System Signals
10. When to Rerun SRIT

**Part 3 — DAI: Denial Architecture Interrogation**
11. What DAI Does
12. The Canonical Extensions
13. The Evidence Register
14. Interpreting the Required Denial Specification
15. Interpreting the Actual Denial Mapping
16. Interpreting the Denial Authority Matrix
17. Interpreting the Denial Architecture Judgement
18. The DAI to DDA Handoff

**Part 4 — DDA: Drift Detection Analysis**
19. What DDA Does
20. Interpreting the Drift Signal Register
21. Interpreting the Boundary Displacement Test
22. Interpreting the Drift Severity Matrix
23. Interpreting the Drift Detection Judgement
24. The Minimum Intervention Logic

**Part 5 — Reference**
25. Common Mistakes Across All Three Modules
26. Platform-Specific Notes
27. Version History

---

# Part 1 — The Framework

---

## 1. The Scarcity–Denial Canon

The canon is the intellectual foundation of the entire framework. Every analytical decision made by every instrument in this framework traces back to one of these four sentences.

> *Every system is constrained by a scarce resource.*
>
> *Denial is the mechanism by which that constraint is enforced.*
>
> *System stability depends on denial being applied at a decision point consistent with the scarcity of that resource.*
>
> *Drift occurs when the denial boundary migrates downstream of the decision point required to protect that scarcity.*

SRIT operationalises the first sentence — identifying the binding scarce resource.

DAI operationalises the second and third sentences — determining whether denial exists, whether it is authoritative, and whether it is positioned at the correct decision point.

DDA operationalises the fourth sentence — detecting whether the denial boundary has migrated and how far.

When in doubt during any run, return to the canon. The canon is not background reading. It is the reason every analytical decision in every instrument is made the way it is.

---

## 2. The Three-Instrument Pipeline

The three instruments form a sequential pipeline. Each receives the prior module's Run Record as its fixed upstream input.

```
System description
      ↓
   SRIT v2.2
      ↓
SRIT Run Record → Binding Scarce Resource Declaration
      ↓
   DAI v2.1
      ↓
DAI Run Record → Denial Architecture Status
      ↓
   DDA v1.6
      ↓
DDA Run Record → Drift Detection Judgement + Minimum Intervention Logic
```

**The pipeline is strictly sequential.** DAI cannot begin until SRIT has produced a complete nine-section Run Record. DDA cannot begin until DAI has produced a Run Record with Readiness for Drift Analysis: Ready.

**Upstream declarations are locked.** DAI does not reopen scarcity identification. DDA does not reopen the denial architecture assessment. Each instrument takes the prior instrument's output as fixed and valid and asks only the question its canonical mandate requires.

**Run Records travel downstream.** Every Run Record must be saved immediately and carried into the next module. The naming convention is:

- `SRIT_Run_[SystemName]_[YYYY-MM-DD_HHMM].md`
- `DAI_Run_[SystemName]_[YYYY-MM-DD_HHMM].md`
- `DDA_Run_[SystemName]_[YYYY-MM-DD_HHMM].md`

---

## 3. Platform and Model Requirements

**ChatGPT — GPT-5.4 Thinking Extended**

Primary execution platform for all three modules. Pin the model version manually before beginning any run. Do not use auto mode — version switching between prompts compromises artefact consistency. Enable Thinking Extended mode. Standard mode produces shallower analytical output.

**Claude — Sonnet 4.6**

Used throughout the Desktop model pipeline as the persistent companion session. Handles System Definition Statement construction (Phase 1), full-run companion initialisation (Phase 2), active commentary on every ChatGPT prompt output across all three modules, boundary checks at the SRIT → DAI and DAI → DDA transitions, declaration and judgement review at each module's Stage 1, Run Record formatting and naming, Module Commentary Summary production, and Rerun Assessment with carry-over SDS artefact production at the close of DDA. One session is opened before the run begins and kept open for the entire three-module run.

**Free tier models**

Not recommended for analytical work. Known failure modes: protocol inversion at Prompt 1, boundary drift, premature convergence. A declaration produced by a protocol-deviant run should not be used for downstream module analysis.

**Session discipline**

Begin every Prompt module execution run in a new chat. Accumulated context from prior conversations influences analytical outputs in ways that are difficult to detect. Each run must be independently auditable.

---

# Part 2 — SRIT: Scarce Resource Identification Tool

---

## 4. What SRIT Does

SRIT identifies the binding scarce resource in a system.

That matters because the Scarcity–Denial Framework only works if the correct scarcity is identified first. If the scarcity is wrong, everything after it — the denial architecture assessment, the drift detection — can be analytically precise and still be wrong.

SRIT forces two disciplines that prevent the most common analytical failures:

**Premature narrative convergence** — reaching a plausible conclusion before the candidate field has been properly tested. The six-prompt sequence is designed to prevent this by generating breadth first and testing candidates against structural criteria before any candidate is favoured.

**Domain bias** — allowing prior knowledge, expert opinion, or the AI's training data to steer the analysis toward the most familiar answer rather than the most structurally defensible one. The boundary audit enforces this — analytical merit does not override boundary compliance.

The output of SRIT is a **Binding Scarce Resource Declaration** embedded in a nine-section **SRIT Run Record**.

---

## 5. The System Definition Statement

The System Definition Statement is produced in Prompt 1 and anchors every subsequent decision in the run. If it is imprecise, the entire downstream analysis will be correspondingly imprecise.

It has four components:

**System** — the name and brief description of what is being analysed.

**Boundary** — what is included and what is explicitly excluded. Both matter equally. The excluded elements prevent scope creep at the boundary audit. A boundary that only states inclusions is incomplete.

**Time Horizon** — the specific window over which stability is being assessed. Use a bounded window (6–12 months, 12–24 months, 3–5 years), not a vague description. The binding scarcity may differ across time horizons — a resource that cannot be substituted within 12 months may be substitutable within 3 years.

**Failure Condition** — the operationally specific condition that constitutes system collapse. Avoid generic statements. Throughput failure, insolvency, coordination collapse, service outage, loss of governability — these are useful. "The system stops working" is not.

Use `SDS_Claude_Construction_Desktop` to develop these four components before beginning the ChatGPT run. The five minutes spent on boundary precision prevents hours of analytical drift.

---

## 6. The Boundary Audit

The boundary audit runs at the opening of Prompt 4, before any elimination begins. It enforces one rule: **analytical strength does not override boundary compliance.**

Every candidate receives one of three statuses:

**In scope** — operates within the system boundary. Proceeds to the elimination matrix.

**Out of scope** — operates outside the boundary. Removed with a single reason statement.

**Adjacent system signal** — out of scope, but its presence suggests it may be the binding scarcity in a system that feeds the defined system. Removed from this run but logged as a candidate for a separate SRIT analysis.

The adjacent system signal is analytically important. It is not a rejection — it is a lead. In the air cargo analysis conducted during SRIT development, aircraft maintenance technician touch-time was correctly flagged as an adjacent system signal: out of scope for the infrastructure analysis, but potentially the binding scarcity in the airline operations layer that feeds the infrastructure. That signal was more valuable than a simple removal.

After the boundary audit table is complete, the AI runs a **shortlist viability check**: are there at least three in-scope candidates that scored meaningfully on at least two Scarcity Pyramid tests? If no, the run halts with a **Boundary Viability Halt**. Return to Prompt 1 and redefine the boundary — the boundary was drawn too narrowly or misaligned with the failure condition.

---

## 7. Interpreting the SRIT Run Record

The Run Record has nine sections. This is how to read each one.

**Run Metadata** — model, thinking mode, SRIT version, run date. Essential for comparative analysis across platforms. If two runs on the same system produce different declarations, the metadata tells you whether thinking mode, model version, or protocol version may explain the divergence.

**System Definition Statement** — the analytical anchor for the run. Review it against what you intended. If it does not reflect your boundary intent, the downstream analysis cannot be trusted.

**Boundary Audit Table** — the most important quality assurance artefact in the run. Check that all three statuses were used correctly and that no out-of-scope candidates were retained on analytical merit. This is where boundary drift is most commonly detected.

**Adjacent System Signals** — leads for subsequent SRIT runs, not rejections. Treat them as a research agenda.

**Provisional Shortlist** — the 3–5 candidates that survived elimination. Read the outstanding ambiguity statement — it documents what was not resolved and what evidence would resolve it.

**Binding Scarce Resource Declaration** — the formal declaration and selection rationale. Read the rationale carefully. A declaration with a thin or generic rationale is weak regardless of how confidently it is phrased.

**Strongest Alternative Rejected** — the candidate that came closest to winning. For downstream denial analysis this section is as important as the declaration itself — it identifies the second-order risk if the primary declaration is wrong.

**Confidence Rating and Residual Uncertainty** — the confidence score out of 10, the specific uncertainties that remain, and the alternative scarcity that would explain the system if the declaration were wrong.

| Rating | Meaning |
|--------|---------|
| 8–10 | Strong convergence. Proceed to DAI. |
| 6–7 | Moderate confidence. Note the outstanding ambiguity before proceeding. |
| 5 or below | Weak declaration. Resolve the Stage 1 test questions before proceeding to DAI. |

**Stage 1 Test Questions** — specific empirical questions that would confirm or challenge the declaration. These are the opening questions of DAI and should be carried forward directly.

---

## 8. Interpreting Contested Declarations

Different declarations on the same system typically fall along a consistent analytical fault line — usually a levels-of-abstraction difference rather than a fundamentally different understanding of the system.

In the air cargo analysis conducted during SRIT development, multiple runs split between:
- Skilled/certified ground handling labour
- Cargo terminal processing capacity

Both are defensible. Labour is the most operationally visible constraint. Terminal processing capacity is the structural container within which labour operates — its fixity determines the ceiling regardless of labour availability.

**When two declarations reverse across runs** — where the binding scarcity in run one becomes the strongest alternative rejected in run two — this is the signature of a genuine tightly coupled co-binding condition. The condition is present when all three of the following are true:

- The confidence rating is 7 or below
- The residual uncertainty statement explicitly describes the top two candidates as tightly coupled, co-binding, or difficult to disentangle
- The outstanding ambiguity statement names both candidates as representing different chokepoints in the same causal pipeline

When this condition is present, both declarations are analytically valid. The three appropriate responses are:

1. Proceed with the most recent declaration into DAI, flagging the co-binding condition explicitly and ensuring the analysis addresses both candidates
2. Gather the Stage 1 empirical evidence and rerun SRIT — the declaration should stabilise once the empirical question is resolved
3. Run DAI twice — once for each declaration. If the same denial gaps appear in both runs, those gaps are robust regardless of which scarcity is primary

---

## 9. Adjacent System Signals

When a candidate is classified as an adjacent system signal, it means the candidate may be the binding scarcity in a system that feeds the system being analysed. This matters for two reasons:

The binding scarcity in the adjacent system may be creating the constraint that manifests as scarcity inside the defined boundary. Denial module interventions applied to the defined system may be ineffective if the true binding scarcity sits outside it.

Run SRIT on each adjacent system separately, using the signal candidate as the starting hypothesis for Prompt 2. The resulting Run Record can then be read alongside the primary declaration to understand the full constraint structure.

---

## 10. When to Rerun SRIT

Rerun SRIT when:

- The analysis produced a Boundary Viability Halt — always requires a return to Prompt 1
- The confidence rating is below 6 and Stage 1 empirical evidence is now available
- Adjacent system signals were identified that appear to be the actual binding scarcity
- The system has changed materially since the last run
- A different time horizon is needed for downstream denial analysis
- The declaration's strongest candidate operates adjacent to but not inside the defined boundary

Do not rerun SRIT without modifying at least one analytical input — boundary, time horizon, or failure condition. The protocol will normally converge on the same declaration with identical inputs.

---

# Part 3 — DAI: Denial Architecture Interrogation

---

## 11. What DAI Does

DAI takes the Binding Scarce Resource Declaration as its fixed input and determines whether a real, binding, authority-backed denial architecture exists to protect that resource — and whether it is positioned at the correct decision point.

It addresses the canon's second and third sentences. Denial is the mechanism by which the constraint is enforced — but enforcement only protects the scarcity if the denial boundary is positioned at the right point in the system. DAI tests both conditions simultaneously.

DAI does not reopen scarcity identification. The Binding Scarce Resource Declaration is treated as fixed and valid throughout. DAI's mandate is to interrogate the denial architecture, not the scarcity.

The output of DAI is a **Denial Architecture Status** embedded in a **DAI Run Record**. The six possible statuses are:

| Status | Meaning |
|--------|---------|
| Aligned and binding | Denial operates at the correct point with sufficient authority, enforcement, and consequence |
| Aligned but fragile | Correctly positioned but lacks enforcement strength or override resistance to hold under stress |
| Partially aligned | Exists and is partially effective but mislocated, under-enforced, or incomplete |
| Mislocated | Denial exists but operates at the wrong point in the system |
| Symbolic | Nominal denial exists but practical binding force is too weak to constrain demand |
| Absent | No credible denial mechanism can be identified |

**Mislocated is the most analytically significant status for downstream DDA.** It means denial is real but displaced — the denial boundary has already migrated away from the correct decision point. This is precisely the condition the canon's fourth sentence describes as the precursor to drift.

---

## 12. The Canonical Extensions

Two operational statements give the canon's second and third propositions executable form within DAI. These are not additions to the canon — they are analytical instruments for DAI execution only:

> *Denial exists only where access to the binding scarce resource is constrained by an authority capable of applying a binding rule, gate, threshold, or consequence at a decision point consistent with protection of that resource.*

> *Drift exists where the actual denial architecture is later, weaker, more permeable, mislocated, or less enforceable than the denial architecture required to protect the binding scarce resource.*

These two sentences operationalise the what and where of denial. The first defines what counts as real denial — not nominal policy, not theoretical authority, but a binding constraint at a specific decision point. The second defines what counts as drift — any condition where actual denial falls short of required denial on any material dimension.

---

## 13. The Evidence Register

*This section describes the Evidence-informed model only. The Desktop model has no Evidence Register — DAI proceeds directly from Prompt 2 to Prompt 3 on structural inference. If you are running the Desktop model, skip this section.*

Between Prompts 2 and 3, DAI provides an opportunity to inject system-specific empirical evidence. The Evidence Register is optional — a DAI run without it is valid and honest. Structural inference is legitimate analysis. The register is an enhancement for users with real operational data, not a requirement for users who do not.

### Why it is tightly controlled

The DAI analytical sequence is built on tightly bound channels — each prompt operates strictly on structured artefacts from the prior prompt. Unstructured data introduced into this channel creates three failure modes: the AI treats user data as more authoritative than the structured analysis warrants; the AI uses data to retrospectively rationalise conclusions already reached; or the AI shifts from interrogation mode into narrative synthesis mode.

The Evidence Register prevents all three failure modes through format control, a validation stage, and strict directionality — evidence flows downstream into Prompt 3 only. It cannot flow upstream to change the Required Denial Specification from Prompt 2.

### How to complete it

At the end of Prompt 2, the AI produces a pre-populated Evidence Register table as Section D. Complete the blank cells for any evidence items you wish to submit. Leave unused rows blank. Paste the completed table back into the chat.

Each evidence item requires three fields:

**Evidence Type** — behavioural, structural, stress, or explicit case fact.

**Evidence Statement** — one sentence, factual, no interpretation. State what you observed or what the document says. Do not explain what it means.

**Source** — document name, observation reference, or interview note. No narrative.

### The one-sentence rule

| Non-compliant | Compliant |
|---------------|-----------|
| The ground handling manager said labour shortages are causing delays, which shows the denial system isn't working | Ground handler operations manager stated in March 2026 that three of five ramp shifts at Hub X were understaffed |
| The acceptance restriction exists but it's only used in emergencies, suggesting it's not a real denial mechanism | Cargo acceptance was restricted on four occasions at Hub Y in Q4 2025 according to the operations log |

### The four exclusion tests

Self-screen against these before submitting:

**Test 1 — Narrative contamination.** Does the Evidence Statement contain interpretive language — suggests, indicates, shows that, because, therefore? If yes, rewrite as a pure factual statement.

**Test 2 — Scope violation.** Does the item relate to a system layer excluded in the SRIT boundary? If yes, remove it — cannot be corrected.

**Test 3 — Scarcity reopening.** Does the item implicitly challenge the Binding Scarce Resource Declaration? If yes, remove it — cannot be corrected.

**Test 4 — Composite assertion.** Does the Evidence Statement contain more than one factual claim? If yes, split into two items.

Items failing Tests 1 or 4 may be corrected and resubmitted (maximum two rounds). Items failing Tests 2 or 3 are permanently excluded. Maximum fifteen items total.

If you have no evidence, type `SKIP` — DAI proceeds directly to Prompt 3 on structural inference.

---

## 14. Interpreting the Required Denial Specification

The Required Denial Specification is the most important output of Prompt 2. It is derived — not inherited from SRIT. It names the denial architecture that must exist to protect the binding scarce resource.

**The Required Denial Decision Point** is the critical row. It identifies the last point in the system at which denial can still protect the scarce resource before the failure condition is triggered. If this point is abstract or vague — if it describes a general process rather than a specific point, moment, and condition — the entire downstream analysis will be imprecise.

The **Protectable Resource Form** should always be more specific than the SRIT declaration. The SRIT declaration names the scarce resource. Prompt 2 names the specific form in which it can be protected. These are different things.

Rows with Medium-High or lower confidence identify where Prompt 3's actual mapping will need to do the most work. Treat them as priority investigation targets.

---

## 15. Interpreting the Actual Denial Mapping

The **Evidence Status** column is the first thing to check. A realistic system will produce a mix of Evidenced and Inferred mechanisms. Uniform Evidenced ratings suggest overconfidence — challenge them. Uniform Inferred ratings are acceptable if honestly rated — it means the analysis was conducted without empirical data, which is legitimate.

If the Evidence Register was used, admitted items should appear with Evidence Status marked as Explicit Case Fact. Check that explicit case facts are not over-interpreting the evidence — the one-sentence rule applies to what was submitted, not to how Prompt 3 uses it.

The **Primary Evidence Weakness** statement in the Actual Denial Mapping Summary is the most useful bridge to Prompt 4. It identifies exactly where the authority and enforcement analysis will encounter the most uncertainty.

---

## 16. Interpreting the Denial Authority Matrix

Do not read Practical Binding Force in isolation. A Strongly Binding mechanism that operates at the wrong decision point is a location failure, not an enforcement success. Read the Claim column for each mechanism to understand both how binding it is and whether it is binding at the right point.

Override permeability ratings should lean toward more permeable when the override route is not clearly evidenced. Unverified override resistance is not real protection.

An Inferred mechanism from Prompt 3 should not receive a Decisively Binding or Strongly Binding rating in Prompt 4. If this occurs, challenge the specific row: *Mechanism X was mapped as Inferred in Prompt 3. Please reassess its Practical Binding Force rating consistent with that evidence status.*

---

## 17. Interpreting the Denial Architecture Judgement

Read the **Comparison Table** before reading the status. The Comparison Table shows the variance between required and actual architecture across nine dimensions. The status is a summary of that variance — but the table shows where the gaps are.

**The Correct Decision Point row is the decisive row.** Severe variance at High confidence on this dimension will almost always determine the overall status. Other dimensions — authority, enforcement, consequence, override — amplify the finding but rarely override it.

The **Primary Weakness** identifies the specific gap between required and actual architecture. The **Primary Strength** identifies what is working and should be preserved.

The **Strongest Counter-Interpretation** should be genuinely adversarial. If it feels obviously weaker than the declared status, the model may not have challenged itself sufficiently. A well-constructed counter-interpretation cites real evidence from Prompts 3 and 4 and requires a specific canon-based rebuttal. If the counter-interpretation is weak, note it — it is a quality signal about the run.

The **Readiness for Drift Analysis** gate must show Ready before DDA can begin. If it shows Not Ready, review the Primary Evidence Weakness from Prompt 3 and consider whether the Evidence Register with real empirical data would produce a more complete mapping.

---

## 18. The DAI to DDA Handoff

DAI is complete when Prompt 5 Stage 1 produces a Denial Architecture Judgement with Readiness for Drift Analysis: Ready, and the Run Record has been produced and saved.

The Denial Architecture Status from DAI determines the DDA starting posture:

| DAI Status | DDA Starting Posture |
|------------|---------------------|
| Mislocated | Drift is the primary hypothesis — the module tests where the boundary currently sits relative to the required point and what drove the migration |
| Aligned but fragile | Drift risk is the primary concern — the module tests whether the boundary is eroding under demand or institutional pressure |
| Partially aligned | The module tests which dimensions are drifting and which are holding |
| Symbolic or Absent | The module tests whether denial ever existed at the required point or was always absent |

Use `DDA_Claude_BoundaryCheck` to confirm the DAI Run Record is complete and the Readiness gate is satisfied before opening ChatGPT for the DDA run.

---

# Part 4 — DDA: Drift Detection Analysis

---

## 19. What DDA Does

DDA takes the DAI Run Record as its fixed input and asks the canon's fourth sentence: has the denial boundary migrated downstream of the decision point required to protect the scarcity?

DDA does not reopen the scarcity or the denial architecture assessment. Both are fixed. DDA's mandate is to determine whether the denial boundary has drifted, how far, in which direction, and what minimum intervention would return it to the correct position.

The output of DDA is a **Drift Detection Judgement** and a **Minimum Intervention Logic** — specific actions required to realign denial with scarcity — embedded in a **DDA Run Record**.

The Drift Detection Judgement assigns one of five statuses:

| Status | Meaning |
|--------|---------|
| Drift confirmed — critical | Denial boundary has migrated to a point where scarcity protection has failed or is imminent |
| Drift confirmed — significant | Material migration detected; scarcity protection is degraded but not yet failed |
| Drift confirmed — early | Early-stage migration detected; scarcity protection is currently intact but directionally at risk |
| No drift detected | Denial boundary is at or close to the required point; scarcity protection is intact |
| Indeterminate | Insufficient evidence to classify drift direction or severity with confidence |

---

## 20. Interpreting the Drift Signal Register

The Drift Signal Register is produced in Prompt 2. It is the primary evidence base for the entire DDA analysis. Each signal has three classification dimensions:

**Source** — where the signal originates: comparison variance (gap between required and actual from DAI), stress observation, structural indicator, or unknown.

**Direction** — which way the boundary has moved: downstream drift (boundary has moved later than required), upstream constriction (boundary has moved earlier than required), lateral displacement (boundary has moved to the wrong system layer), counter-drift (boundary has moved toward the required point), or unknown.

**Strength** — how clearly the signal points to drift: Strong, Moderate, Weak, or Ambiguous.

**Mixed signals** — where a signal's source and direction classifications point to different origins — must be preserved as mixed rather than forced to a single resolution. A comparison variance source suggesting downstream drift combined with an unknown row source suggesting never-built architecture is a mixed signal. The specific tension should be noted and carried into Prompt 3.

The Drift Signal Summary identifies the dominant drift direction and the primary signal cluster. If the summary forces resolution of a mixed signal into a single direction, note it as a quality concern.

---

## 21. Interpreting the Boundary Displacement Test

The Boundary Displacement Test in Prompt 3 takes each signal from the Drift Signal Register and tests whether it indicates actual displacement of the denial boundary.

The test asks three questions per signal: Is the denial boundary operating at a different point than required? If yes, is that difference downstream, upstream, or lateral? What is the confidence level for that classification?

The **Drift Origin Statement** produced at the end of Prompt 3 classifies the overall origin as one of: Never built (denial never existed at the required point), Migrated (denial existed but has moved), Eroded (denial exists but is weakening in place), or Mixed (multiple origin types present in the same system).

The origin classification matters for intervention design. A Never built finding requires construction of a denial architecture. A Migrated finding requires relocation of an existing boundary. An Eroded finding requires reinforcement of a deteriorating mechanism. A Mixed finding requires multiple intervention types.

---

## 22. Interpreting the Drift Severity Matrix

The Drift Severity Matrix in Prompt 4 assesses the severity of each confirmed displacement across four dimensions: distance of displacement, rate of progression, reversibility, and systemic consequence.

Read the **Overall Drift Severity** against the individual dimension ratings. A High overall severity should be supported by High or Critical ratings on at least two individual dimensions. If Overall Drift Severity is High but all dimensions are Medium, this is a quality concern — challenge the overall rating.

The **Denial Durability Table** assesses which currently aligned mechanisms are at risk of future drift. This is forward-looking — it tells you not just where drift has occurred but where it is likely to occur next.

The **Preserved Aligned Mechanisms** section identifies what is currently working correctly and should not be disrupted by the Minimum Intervention Logic. Any intervention that targets a preserved mechanism without justification is over-reach.

---

## 23. Interpreting the Drift Detection Judgement

Read the **Drift Detection Status** against the full evidence chain: Drift Signal Register → Boundary Displacement Test → Drift Severity Matrix. The status should be traceable to specific signals and specific severity ratings. A status that cannot be traced to specific evidence is a quality concern.

The **Strongest Counter-Interpretation** in DDA, as in DAI, should be genuinely adversarial. A counter-interpretation that simply restates the null hypothesis (no drift detected) without citing specific contrary evidence is not a real counter-interpretation.

The **Empirical Tests for Next Stage** identify what would confirm or refine the drift classification. These are the opening questions for any further empirical investigation and should be recorded alongside the Run Record.

---

## 24. The Minimum Intervention Logic

The Minimum Intervention Logic specifies between three and six actions required to realign denial with scarcity. It is constrained by the canon's fourth sentence — it proposes only what is required to return the denial boundary to the correct decision point, not redesign beyond what the identified drift condition warrants.

Three tests for the Minimum Intervention Logic:

**Canon grounding** — does each action address the fourth sentence directly? Does it propose actions that would return the denial boundary to the correct decision point? If an action addresses symptoms rather than the displaced boundary, it is over-reach.

**Preserved mechanism respect** — does the logic avoid disrupting mechanisms identified as Preserved in the Denial Durability Table? If it targets a preserved mechanism without justification, challenge that action.

**Proportionality** — does the number and scope of actions match the drift severity? A Critical drift finding should produce a more substantial intervention logic than an Early finding.

---

# Part 5 — Reference

---

## 25. Common Mistakes Across All Three Modules

**Accepting the first plausible answer.** The protocol is designed to prevent this — trust the sequence. The binding resource, the correct decision point, and the drift origin are rarely the most obvious answers.

**Confusing operational visibility with analytical primacy.** The most discussed issue in a system is often not the binding constraint. The most visible denial mechanism is often not the most important one. The most obvious drift signal is often a symptom of a more fundamental displacement.

**Allowing AI coherence to substitute for analytical rigour.** AI is very good at sounding coherent. A declaration, judgement, or intervention logic that arrives with a smooth, well-structured rationale should receive more scrutiny than one that arrives with visible tension — not less.

**Using a low-confidence output for downstream analysis.** A confidence rating of 5 or below at any stage means the analysis did not converge. Do not carry weak outputs downstream. Identify the empirical evidence that would resolve the ambiguity and gather it before proceeding.

**Skipping the Stage 1 Claude review.** The review step between Stage 1 and Stage 2 of each module's final prompt catches declaration and judgement quality issues before they are embedded in the Run Record that carries into the next module. Skipping it is the highest-risk single shortcut in the pipeline.

**Running in a contaminated session.** Begin every execution run in a new chat. This is not optional — it is the primary protection against accumulated context influencing outputs in ways the user cannot detect.

**Treating the Run Record as a formality.** The Run Record is the analytical contract between modules. If it is incomplete, the next module's input integrity check will flag it. If it contains weak rationale or inflated confidence, that weakness propagates downstream.

---

## 26. Platform-Specific Notes

### ChatGPT — GPT-5.4

Pin the model version manually before beginning. Do not use auto mode — version switching between prompts has been observed and compromises artefact consistency. Enable Thinking Extended mode for all three modules. Standard mode produces shallower elimination rationale, weaker evidence verification, and less precise drift signal classification.

Known behaviour: with Thinking Extended enabled, GPT-5.4 may execute multiple prompts as a single continuous output in single-pass mode. For sequential review mode, confirm the mode explicitly in the opening instruction and intervene if the model proceeds past the intended stop point.

### Claude — Sonnet 4.6

Used as the persistent companion session throughout the Desktop model pipeline. One session is opened before the run begins and kept open for the entire three-module run — it is never closed between modules.

Session discipline: do not open a new Claude session mid-run. The companion session carries full context from Phase 1 SDS construction through to the DDA Rerun Assessment. All boundary checks, Stage 1 reviews, Run Record files, and Commentary Summaries are produced within this single session. Opening a new session loses that context and will produce incomplete outputs.

### Platforms not currently validated

All platforms except for ChatGPT 5.4 and Claude Sonnet 4.6, as specified above.

---

## 27. Version History

User Manual v1.0 — 2026-03-20. First consolidated manual covering SRIT, DAI, and DDA.

User Manual v1.1 — 2026-03-21. Gemini removed as validated platform. Version history table replaced with summary entry. Session discipline wording updated. Platforms not validated consolidated to single statement.

User Manual v1.2 — 2026-03-31. Instrument versions updated to SRIT v2.2, DAI v2.1, DDA v1.6. Operational documents table replaced to reflect current Desktop instrument set. Pipeline diagram updated. Claude role description updated to reflect single persistent companion session architecture. Section 5 and Section 18 document references corrected. Section 13 Evidence Register marked as Evidence-informed model only with Desktop model skip notice. Section 26 Claude session discipline corrected — single persistent session, full context dependency throughout.

---

*© Philip Harry Galvin 2026. The Scarcity–Denial Canon, SRIT, DAI, and DDA instruments are licensed under Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0). Free use for non-commercial purposes with attribution. No derivative works. Commercial use or modification requires prior written approval from the author.*
