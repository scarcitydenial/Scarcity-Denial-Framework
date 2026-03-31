# Drift Detection Analysis

## DDA v1.6

### Purpose

Determine whether the actual denial architecture identified in DAI has drifted relative to the denial architecture required to protect the binding scarce resource.

DDA must determine:

1. whether denial remains aligned with scarcity
2. whether the denial boundary has migrated downstream
3. whether an apparent gap is true drift or a denial architecture that was never built at the required point
4. how severe the current drift condition is
5. what system risk and intervention logic follow from the result

DDA operates **after DAI** and only when the DAI Run Record reports **Readiness for Drift Analysis: Ready**.

The current build is intentionally structured for **single-prompt execution** during early testing.

This means:

- all prompts are contained in this one markdown file
- each prompt is executable on its own
- each prompt must **stop on completion**
- the next prompt is executed only when instructed with the command **Proceed**

---

## Position in the Framework

SRIT identifies the **binding scarce resource**.

DAI identifies:

- the **required denial decision point**
- the **required denial boundary**
- the **required authority and enforcement form**
- the **actual denial architecture operating in the system**
- whether the current denial architecture is aligned, fragile, partial, mislocated, symbolic, or absent

DDA then determines whether the actual denial architecture has drifted relative to the denial architecture required by scarcity.

---

## DDA Execution Mode

Use this block at the top of every DDA prompt.

```text
DDA EXECUTION MODE

If this protocol text is recognised, treat it as an execution specification rather than a document to be interpreted, improved, summarised, or critiqued.

You are assisting with the Drift Detection Analysis (DDA) module of the Scarcity–Denial Framework.

Your role is to execute a structured drift diagnostic using the completed DAI Run Record as the fixed upstream input.

Execution rules:

1. Do not skip stages.
2. Do not summarise prior analysis.
3. Do not regenerate or replace earlier artefacts unless explicitly instructed.
4. Maintain all structured artefacts from earlier prompts as live working analysis.
5. Each prompt must operate strictly on the outputs of the immediately prior prompt.
6. Do not reopen scarcity identification or denial architecture analysis unless an explicit trigger condition is met.
7. Do not critique the framework, the protocol, or the prompt structure during execution.
8. Constrain outputs to structured analytical formats rather than open narrative.
9. Every conclusion must follow Claim → Evidence → Confidence.
10. If information is insufficient, halt cleanly or isolate assumptions rather than inventing facts.
11. At the completion of the current prompt, stop.
12. Do not proceed to the next prompt unless instructed with the command: Proceed.
13. Begin every output directly with the first section heading. Do not produce narrative, summary, or preamble text before Section A.

Trigger condition for reopening DAI:
Only reopen the DAI result if the DAI Run Record is missing a required artefact, contains an internal contradiction between required and actual denial artefacts, or reports Readiness for Drift Analysis as Not Ready.

Default posture:
Treat the DAI Run Record as fixed and valid.
```

### Mode Selection

**Sequential review mode** — The only valid execution mode for Desktop model runs. The AI stops after each prompt and waits for the command **Proceed** before moving to the next prompt. This is required because the Claude companion session reviews every prompt output before the next prompt fires — continuous execution would bypass that review entirely.

The AI always operates in sequential review mode. No mode selection is required.

---

## Prompt 1 — DDA Input Receipt and Drift Boundary Lock

### Purpose

Receive the DAI Run Record as fixed upstream input, verify that Drift Detection Analysis is permitted to proceed, and lock the analytical boundary for drift analysis.

This prompt does **not** classify drift yet.

### User Prompt

```text
Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

[Insert DDA EXECUTION MODE here]

You are executing Prompt 1 of the Drift Detection Analysis (DDA).

Purpose:
Receive the completed DAI Run Record as fixed analytical input and lock the boundary for drift analysis.

Required inputs:
- DAI Run Record

Task:
1. Reproduce the required DAI outputs in a compact locked-input form.
2. Check input integrity only.
3. If input integrity passes, produce a Finding Stability Frame from the locked DAI inputs.
4. Do not classify drift yet.
5. Do not reopen DAI unless a formal inconsistency trigger is met.

Input integrity tests:
- Is the system clearly stated?
- Is the system boundary clearly stated?
- Is the time horizon present?
- Is the failure condition present?
- Is the Binding Scarce Resource Declaration present?
- Is the Required Denial Specification Table present?
- Is the Actual Denial Mapping Table present?
- Is the Denial Authority Matrix present?
- Is the Denial Architecture Comparison Table present?
- Is the Denial Architecture Judgement present?
- Is the Binding Reality Summary present?
- Is the Readiness for Drift Analysis status present?
- Is the Readiness for Drift Analysis status Ready?

If all required inputs are present and coherent, produce a DDA Input Receipt Table, a Drift Boundary Lock Statement, and a Finding Stability Frame.

If any required input is missing, internally inconsistent, or the readiness status is Not Ready, halt and return:

**DDA Input Integrity Halt**

Missing or inconsistent input:
- [item]

Reason drift analysis cannot proceed:
- [reason]

Required action:
- Return to the DAI Run Record and correct the missing or inconsistent element before restarting DDA Prompt 1.

Output structure:

## Section A — DDA Input Receipt Table

| Variable | Locked Input |
|----------|--------------|
| System | |
| Boundary | |
| Time Horizon | |
| Failure Condition | |
| Binding Scarce Resource | |
| Binding Level | |
| Required Denial Decision Point | |
| Required Denial Boundary | |
| Denial Architecture Status | |
| Readiness for Drift Analysis | |
| Admitted Evidence Register Status | |

## Section B — Drift Boundary Lock Statement

Return this exact format:

**Drift Boundary Lock Statement**

For the purpose of Drift Detection Analysis, the following elements are now treated as fixed analytical inputs:
- System boundary: [text]
- Time horizon: [text]
- Failure condition: [text]
- Binding scarce resource: [text]
- Required denial decision point: [text]
- Required denial boundary: [text]
- Denial Architecture Status: [text]

DAI re-opening status: [Closed / Triggered]

Reason:
- [one line]

## Section C — Finding Stability Frame

Return this exact format:

**Finding Stability Frame**

Most important unresolved dimension carried from DAI:
- [text]

Primary rival interpretation to test:
- [text]

Preliminary rerun trigger conditions:
- [condition]
- [condition]
- [condition if required]

Opening trajectory posture:
- [Worsening / Stable / Recovering / Unknown]

Why:
- [one sentence]

Prompt 1 Finding Stability Frame note:
The Finding Stability Frame is a live analytical frame derived from the locked DAI inputs. It does not change the DAI result and does not constitute a drift judgement. It establishes the principal unresolved dimension, rival interpretation, preliminary rerun triggers, and opening trajectory posture that must later be reviewed explicitly at Prompt 5 Stage 1.

When this Prompt 1 has successfully completed, stop and wait for the explicit instruction: **Proceed**.
```

---

## Prompt 2 — Drift Signal Register

### Purpose

Identify and register the observable signals that may indicate denial drift, denial-boundary non-construction, or drift-enabling architecture.

This prompt does **not** make the final drift judgement.

### User Prompt

```text
Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

[Insert DDA EXECUTION MODE here]

You are executing Prompt 2 of the Drift Detection Analysis (DDA).

Purpose:
Identify the material signals that may indicate denial drift, non-built denial architecture, or drift-enabling conditions.

Use only:
- the DDA Input Receipt Table
- the Drift Boundary Lock Statement
- the Required Denial Specification Table
- the Actual Denial Mapping Table
- the Denial Authority Matrix
- the Denial Architecture Comparison Table
- the Binding Reality Summary
- the Final Admitted Evidence Register if one exists

Do not classify overall drift yet.
Do not judge overall system risk yet.

Task:
Identify every material signal in the record that bears on whether denial remains aligned with scarcity.

At minimum, test for signals relating to:
1. decision-point displacement
2. level mismatch
3. override exercise or override permeability
4. enforcement weakening
5. consequence deferral, waiver, or reduction
6. visibility asymmetry
7. revalidation weakness
8. unknown required mechanism
9. actor misalignment
10. denial boundary absence at the required point
11. countervailing aligned evidence — signals that protective mechanisms remain real and operative, providing evidence against overstatement of drift severity. Direction classification: counter-drift.

Signal source categories may include:
- comparison variance
- unknown row
- override route
- evidence-status weakness
- authority weakness
- visibility gap
- revalidation gap
- consequence weakness
- explicit case fact

Direction categories may include:
- downstream drift signal
- non-built architecture signal
- drift-enabling condition
- mixed signal
- indeterminate
- counter-drift

Signal strength categories:
- Low
- Moderate
- High
- Critical

Rules:
- Override permeability is a primary drift signal and must be tested first.
- Unknown rows are valid drift inputs and must not be ignored.
- Visibility asymmetry may be a drift-enabling condition even where direct drift is not yet evidenced.
- Do not collapse non-built architecture into drift unless the record supports actual migration from a previously more protective boundary.
- Do not infer override exercise frequency if the record only supports override permeability.
- Where a signal's source and direction classifications point to different origins — for example a comparison variance source suggesting downstream drift but an unknown row source suggesting never-built architecture — classify the signal as mixed and note the specific tension. Do not force resolution of a mixed signal into a single direction.
- Every row must contain Claim → Evidence → Confidence.

Output structure:

## Section A — Drift Signal Register

| Signal | Source Artefact | Dimension | Direction | Signal Strength | Claim | Evidence | Confidence |
|--------|-----------------|-----------|-----------|-----------------|-------|----------|------------|

## Section B — Drift Signal Summary

Return this exact format:

**Drift Signal Summary**

Primary drift-relevant signal:
- [text]

Strongest non-built architecture signal:
- [text]

Most important drift-enabling condition:
- [text]

Most uncertain signal:
- [text]

When this Prompt 2 has successfully completed, stop and wait for the explicit instruction: **Proceed**.
```

---

## Prompt 3 — Boundary Displacement and Origin Test

### Purpose

Determine whether the observed gap is true downstream drift, denial architecture that was never built at the required point, a mixed condition, or an indeterminate case.

### User Prompt

```text
Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

[Insert DDA EXECUTION MODE here]

You are executing Prompt 3 of the Drift Detection Analysis (DDA).

Purpose:
Determine whether the observed denial gap is due to downstream migration, non-construction of the required denial boundary, a mixed condition, or indeterminacy.

Use only:
- the DDA Input Receipt Table
- the Drift Boundary Lock Statement
- the Drift Signal Register
- the Drift Signal Summary
- the Required Denial Specification Table
- the Actual Denial Mapping Table
- the Denial Authority Matrix
- the Denial Architecture Comparison Table

Do not grade overall severity yet.
Do not judge overall system risk yet.

Task:
For each critical dimension bearing on boundary location and boundary integrity, determine whether the current condition is:
- aligned
- downstream migrated
- never built at the required point
- mixed
- indeterminate

At minimum, test:
1. denial decision point
2. denial level
3. override resistance
4. consequence execution
5. visibility
6. revalidation

Rules:
- Do not classify a local weakness as drift unless it shifts where denial effectively fires.
- A required market-level or system-level gate that is absent from the actual architecture may be a never-built boundary rather than downstream drift.
- Frequent or structurally open override pathways that displace effective denial downstream are valid drift evidence.
- Deferred, waived, or reduced consequences are drift only if they shift the effective denial boundary downstream or render the nominal boundary non-binding.
- Where the Drift Signal Register contains mixed signals for a dimension, carry the dimension forward as mixed unless the record supplies clear evidence resolving the tension.
- When a dimension remains mixed, note the specific tension in the Claim or Evidence field. Do not force the Origin Classification into downstream migrated or never built.
- Every row must contain Claim → Evidence → Confidence.

Output structure:

## Section A — Boundary Displacement Test Table

| Dimension | Required State | Actual State | Origin Classification | Effective Boundary Shift | Claim | Evidence | Confidence |
|----------|----------------|-------------|-----------------------|--------------------------|-------|----------|------------|

## Section B — Drift Origin Statement

Return this exact format:

**Drift Origin Statement**

Relative to the denial architecture required to protect [binding scarce resource], the current architecture is assessed as:
- [Aligned / Drifted downstream / Never built at the required point / Mixed / Indeterminate]

Primary reason:
- [text]

Most important supporting dimension:
- [text]

Most important unresolved dimension:
- [text]

When this Prompt 3 has successfully completed, stop and wait for the explicit instruction: **Proceed**.
```

---

## Prompt 4 — Drift Severity and Denial Durability Assessment

### Purpose

Grade the severity of the current drift condition and test whether the denial architecture remains durable under ordinary and stress conditions.

### User Prompt

```text
Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

[Insert DDA EXECUTION MODE here]

You are executing Prompt 4 of the Drift Detection Analysis (DDA).

Purpose:
Assess the severity of the current drift condition and the durability of the denial architecture.

Use only:
- the Drift Signal Register
- the Drift Signal Summary
- the Boundary Displacement Test Table
- the Drift Origin Statement
- the Denial Authority Matrix
- the Denial Architecture Comparison Table
- the Binding Reality Summary

Do not make the final drift judgement yet.
Do not set final intervention logic yet.

Task:
Assess the current drift condition against both a severity scale and a denial durability test.

Severity scale:
- D0 — No drift: actual denial remains materially aligned with the required architecture
- D1 — Minor drift: local or intermittent weakening without active structural non-protection
- D2 — Material drift: repeated or multi-dimensional weakening that makes protection unreliable
- D3 — Severe drift: denial is frequently displaced, bypassed, or rendered non-binding under ordinary conditions
- D4 — Structural non-protection: the required denial boundary is absent, never built, or routinely overridden such that protection of the scarce resource cannot be relied upon

Durability tests:
1. binding force
2. override resistance
3. consequence execution
4. visibility adequacy
5. revalidation adequacy
6. stress resistance

Rules:
- The strongest aligned dimension should be identified and preserved explicitly.
- A system may have D4 structural non-protection without classical downstream migration if the required denial boundary was never built.
- A dimension rated Critical in DAI should be treated as a presumptive driver of severity unless contradicted by stronger evidence.
- Where the Boundary Displacement Test Table carries a mixed origin classification, assess severity on the basis of the observed protection weakness without forcing the mixed condition into a single origin.
- Preserve the specific tension from mixed signals in the Claim or Evidence field of the relevant severity row.
- Every row must contain Claim → Evidence → Confidence.

Output structure:

## Section A — Drift Severity Matrix

| Dimension | Current Condition | Severity Contribution | Claim | Evidence | Confidence |
|----------|-------------------|-----------------------|-------|----------|------------|

## Section B — Denial Durability Table

| Durability Test | Result | Weakness | Claim | Evidence | Confidence |
|----------------|--------|----------|-------|----------|------------|

## Section C — Preserved Aligned Mechanisms

Return this exact format:

**Preserved Aligned Mechanisms**

Most important still-functioning aligned mechanism:
- [text]

Why it matters:
- [text]

Overall severity rating:
- [D0 / D1 / D2 / D3 / D4]

When this Prompt 4 has successfully completed, stop and wait for the explicit instruction: **Proceed**.
```

---

## Prompt 5 — Drift Detection Judgement and Intervention Logic

### Purpose

Make the final drift judgement, classify the current system condition, identify the primary failure pathway, and specify the realignment logic required.

### User Prompt

```text
Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

[Insert DDA EXECUTION MODE here]

You are executing Prompt 5 of the Drift Detection Analysis (DDA).

Purpose:
Make the final drift judgement and specify the intervention logic implied by the result.

Use only:
- the DDA Input Receipt Table
- the Drift Boundary Lock Statement
- the Finding Stability Frame
- the Drift Signal Register
- the Drift Signal Summary
- the Boundary Displacement Test Table
- the Drift Origin Statement
- the Drift Severity Matrix
- the Denial Durability Table
- the Preserved Aligned Mechanisms statement
- the Denial Architecture Judgement

Task:
Determine the current drift condition of the system relative to the denial architecture required to protect the binding scarce resource.

Then provide:
1. the overall drift classification
2. the drift form
3. the severity rating
4. the current system condition
5. the primary failure pathway
6. the drift trajectory assessment
7. the strongest counter-interpretation and why it is weaker
8. the minimum intervention logic required to realign denial with scarcity
9. the most important empirical questions that should be tested next
10. the finding stability review confirming or revising the Prompt 1 Finding Stability Frame

Overall drift classification options:
- no drift
- emerging drift
- material drift
- severe drift
- structural non-protection
- indeterminate

Drift classification equivalence:

| D-Scale | Overall Drift Classification | Typical System Condition |
|---------|------------------------------|--------------------------|
| D0 | no drift | stable |
| D1 | emerging drift | strained |
| D2 | material drift | strained or drift-active |
| D3 | severe drift | drift-active |
| D4 | structural non-protection | drift-active or failure-active |

Note: These equivalences are typical, not absolute. A system may present combinations not shown here — for example D3 severity with strained condition where stress controls are still partially holding. Use the mapping as a cross-check, not a mechanical rule.

Drift form options:
- downstream migration
- never-built denial boundary
- mixed
- no drift
- indeterminate

Current system condition options:
- stable
- strained
- drift-active
- failure-active

Trajectory status options:
- Worsening
- Stable
- Recovering
- Unknown

Trajectory status definitions:
- Worsening: Evidence or structural forces suggest the denial boundary is continuing to migrate downstream of the required decision point, or that the gap between required and actual architecture is widening.
- Stable: Evidence or structural forces suggest the denial boundary is not currently moving materially in either direction, though structural non-protection may persist.
- Recovering: Evidence or structural forces suggest the denial boundary is beginning to move back toward the required decision point, or that the gap is narrowing.
- Unknown: The current record does not support a directional assessment. This is a valid output and must be stated explicitly rather than omitted.

Rules:
- Structural non-protection is a valid final result and must not be forced into downstream migration.
- Preserve the distinction between drift signal, drift origin, and final drift judgement.
- Where mixed signals remain material after Prompt 4, preserve the final drift form as mixed and state the specific tension. Do not force the final judgement into downstream migration or never-built denial boundary.
- The trajectory assessment is an additional directional finding. It does not by itself change the drift classification or severity rating, but it must be stated explicitly.
- Every Minimum Intervention Logic action must carry an origin tag consistent with the Boundary Displacement Test Table.
- BUILD is used where the relevant mechanism was never built at the required point.
- RELOCATE is used where denial has migrated downstream and must be moved back to the required decision point.
- STRENGTHEN is used where a mechanism exists near the required point but is not yet binding, coercive, or durable enough to protect the scarce resource.
- Where the relevant Prompt 3 origin classification is mixed, use the dominant intervention logic and note the mixed basis in the action text if material.
- Do not propose redesign beyond the minimum intervention logic required by the findings.
- Every conclusion must follow Claim → Evidence → Confidence.

Output structure:

## Section A — Drift Detection Judgement

Return this exact format:

**Drift Detection Judgement**

For [system], relative to the denial architecture required to protect [binding scarce resource], the current condition is assessed as **[overall drift classification]**.

Drift form:
- [text]

Severity rating:
- [D0 / D1 / D2 / D3 / D4]

Current system condition:
- [stable / strained / drift-active / failure-active]

Primary failure pathway:
- [text]

Why:
- [reason]
- [reason]

## Section B — Drift Trajectory Assessment

Return this exact format:

**Drift Trajectory Assessment**

Trajectory status:
- [Worsening / Stable / Recovering / Unknown]

Reasoning:
- [reason]
- [reason]
- [reason if required]

Trajectory confidence:
- [Low / Medium / High]

Directional forces identified:
- [text]
- [text]
- [None identified on current record]

## Section C — Strongest Counter-Interpretation

Return this exact format:

**Strongest Counter-Interpretation**

Alternative reading:
- [text]

Why it is weaker:
- [reason]
- [reason]

## Section D — Minimum Intervention Logic

Return this exact format:

**Minimum Intervention Logic**

To realign denial with scarcity, the minimum required actions are:
- Action 1 — [BUILD / RELOCATE / STRENGTHEN]: [action]
- Action 2 — [BUILD / RELOCATE / STRENGTHEN]: [action]
- Action 3 — [BUILD / RELOCATE / STRENGTHEN]: [action]
- Action 4 — [BUILD / RELOCATE / STRENGTHEN]: [action if required]
- Action 5 — [BUILD / RELOCATE / STRENGTHEN]: [action if required]
- Action 6 — [BUILD / RELOCATE / STRENGTHEN]: [action if required]

Use between three and six actions. Use only as many as the findings require. Do not propose redesign beyond what the identified drift condition directly warrants.

**Intervention Summary**
- Intervention profile: [number] BUILD / [number] RELOCATE / [number] STRENGTHEN actions.
- Characterisation: [one sentence on the overall intervention logic]

## Section E — Empirical Tests for Next Stage

Return this exact format:

**Empirical Tests for Next Stage**

Priority tests:
- [test]
- [test]
- [test]

## Section F — Finding Stability Review

Return this exact format:

**Finding Stability Review**

Status of Prompt 1 Finding Stability Frame:
- [Confirmed / Revised]

Most important unresolved dimension:
- [text]

Primary rival interpretation tested:
- [text]

Outcome of rival interpretation test:
- [Not supported / Partially supported / Supported]

What would most change this finding if resolved:
- [one sentence]

Rerun trigger conditions:
- [condition]
- [condition]
- [condition if required]

Basis for stability assessment:
- [reason]
- [reason]

Overall confidence in drift classification:
- [High / Medium-High / Medium / Medium-Low / Low]

Change from Prompt 1 frame:
- [None / text]

**Prompt 5 — Stage 1 complete.**

When this Prompt 5 Stage 1 has successfully completed, stop. Do not produce the Run Record yet. The Drift Detection Analysis module analytical output is complete. Wait for the explicit instruction: **Execute Run Record** to proceed to Stage 2.
```

---

## Prompt 5 — Stage 2: Run Conclusion and DDA Run Record

This section executes only when the user instructs: **Execute Run Record**.

Do not say "let me produce the Run Record", "I will now generate", or any similar preamble. Output the conclusion statement and Run Record directly in response to that instruction. Deliver the Run Record inside a fenced code block using triple backticks. Do not render the Run Record as formatted markdown.

**Conclusion statement:**

> This DDA analysis is now complete. The Drift Detection Judgement and supporting artefacts are preserved in the DDA Run Record below. Save the DDA Run Record as:
>
> `DDA_Run_[SystemName]_[YYYY-MM-DD_HHMM].md`
>
> where [SystemName] is the system name from the upstream SRIT and DAI records and [YYYY-MM-DD_HHMM] is the date and time of this run.

**DDA Run Record — output immediately below the conclusion statement:**

```markdown
# DDA Run Record

## Run Metadata
- **System:** [system name]
- **Run Date/Time:** [YYYY-MM-DD HH:MM]
- **AI Model:** [model name and version]
- **Thinking Mode:** [Standard / Extended / Not applicable]
- **DDA Version:** 1.6
- **Run Type:** [First run / Comparative run]
- **Prior Run Reference:** [filename of prior DDA run if comparative, or N/A if first run]

---

## Upstream References
- **DAI Run Record:** [DAI Run Record filename]
- **SRIT Run Record:** [SRIT Run Record filename if known]
- **DAI Version:** [version number]

---

## System Definition Statement
[Reproduce the System Definition Statement from the DAI Run Record]

---

## Binding Scarcity Declaration
[Reproduce the exact Binding Scarcity Declaration from the DAI Run Record]

---

## Denial Architecture Status
[Reproduce the Denial Architecture Status from the DAI Run Record — one of: Aligned and Binding / Aligned but Fragile / Partially Aligned / Mislocated / Symbolic / Absent]

---

## DDA Input Receipt Table
[Reproduce Prompt 1 Section A in full]

---

## Drift Boundary Lock Statement
[Reproduce Prompt 1 Section B in full]

---

## Finding Stability Frame
[Reproduce Prompt 1 Section C in full]

---

## Drift Signal Register
[Reproduce Prompt 2 Section A in full]

---

## Drift Signal Summary
[Reproduce Prompt 2 Section B in full]

---

## Boundary Displacement Test Table
[Reproduce Prompt 3 Section A in full]

---

## Drift Origin Statement
[Reproduce Prompt 3 Section B in full]

---

## Drift Severity Matrix
[Reproduce Prompt 4 Section A in full]

---

## Denial Durability Table
[Reproduce Prompt 4 Section B in full]

---

## Preserved Aligned Mechanisms
[Reproduce Prompt 4 Section C in full]

---

## Drift Detection Judgement
[Reproduce Prompt 5 Section A in full]

---

## Drift Trajectory Assessment
[Reproduce Prompt 5 Section B in full]

---

## Strongest Counter-Interpretation
[Reproduce Prompt 5 Section C in full]

---

## Minimum Intervention Logic
[Reproduce Prompt 5 Section D in full]

---

## Empirical Tests for Next Stage
[Reproduce Prompt 5 Section E in full]

---

## Finding Stability Review
[Reproduce Prompt 5 Section F in full]

---
```

---

## Run Record Naming Convention

Recommended filename for distribution and storage:

`DDA_Run_[SystemName]_[YYYY-MM-DD_HHMM].md`

### Code Block Truncation Note

If the Run Record is too large for a single code block on the platform being used, output it in two code blocks:
- First block: Run Metadata through Drift Signal Summary
- Second block: Boundary Displacement Test Table through Finding Stability Review

---

## Build Notes

### Current execution mode

This file operates in **sequential review mode only**.

That means the model should:

- execute only the prompt explicitly invoked
- stop at the end of that prompt
- wait for the command **Proceed** before the next prompt is run
- preserve all structured artefacts for the next run

### Design notes carried forward from DAI testing

This build incorporates four important design conclusions carried forward from DAI testing:

- override permeability is a primary drift signal
- non-built denial architecture must be distinguished from downstream migration
- consequence adequacy may remain the strongest aligned dimension and should be tested for erosion rather than assumed absent
- visibility asymmetry can be a structural drift-enabling condition even before direct drift is evidenced

### Future conversion

Once the prompt set is validated, this file can be converted into:

- a continuous-run DDA script
- a DDA run record template
- a downstream case-comparison or empirical validation tool

---

## Prompt File Naming Convention

Recommended filename for distribution and storage:

`DDA_Prompts_v1_6.md`
