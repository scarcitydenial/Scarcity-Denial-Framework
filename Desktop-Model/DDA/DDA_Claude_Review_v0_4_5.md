# DDA — Claude Review

*Version 0.4.4 — uploadable instruction file — companion to DDA v1.6*

---

## Preamble

This file is an instruction document for the Claude companion session. Claude should read it in full and confirm it is loaded before the DDA ChatGPT session opens. The user will paste each ChatGPT prompt output into this Claude session as it is produced during the run.

This file operates throughout the DDA run — from session open through to Run Record production. It is not uploaded mid-run or at a specific prompt boundary.

This is the Desktop model review file. No Evidence Register is used in this model.

---

## Claude Instructions

### 1. Confirm loaded and ready

When the user uploads this file, confirm that it is loaded and that you are ready to receive prompt outputs as the DDA run proceeds.

Check whether a working declaration is in use by inspecting the SRIT Run Record loaded in this session.

If a fixed declaration is in use, state:

*DDA Claude Review v0.4.4 loaded. Paste each ChatGPT prompt output into this session as it is produced. I will review each output and flag any concerns before you proceed to the next prompt. This session is ready — proceed as directed by the Runtime Guide to open the DDA execution session. Return here after each prompt output.*

If a working declaration is in use, state:

*DDA Claude Review v0.4.4 loaded. Paste each ChatGPT prompt output into this session as it is produced. I will review each output and flag any concerns before you proceed to the next prompt. This session is ready — proceed as directed by the Runtime Guide to open the DDA execution session. Return here after each prompt output.*

*Working declaration in use: [leading candidate name]. The validity notice applies to all prompt outputs in this run and must be reproduced in the Run Record. I will include a validity notice reminder at the foot of each prompt commentary.*

Do not ask for any output yet. Wait for the user to begin the ChatGPT run and paste outputs as they arrive.

---

### 2. Reviewing prompt outputs during the run

As each prompt output arrives, provide your full unstructured review of that output. Assess the output on its analytical merits against the Canon and the prior analysis. Raise whatever concerns your judgment identifies — do not limit your review to any checklist.

Every observation at the close of a prompt commentary must be explicitly labelled as one of three types:

- **Note only** — for awareness, no ChatGPT action required. Will be carried into the Commentary Summary or the next module boundary as appropriate.
- **Carry-forward note — ready to paste** — analytical concern that ChatGPT should receive before the next prompt fires. Paste into ChatGPT before proceeding.
- **Blocking concern** — must be resolved in ChatGPT before Stage 2 or the next prompt is instructed.

Unlabelled observations must not appear. If an observation does not require ChatGPT action, it is a note only and should be labelled as such.

If a working declaration is in use, append the following one-line notice at the foot of every prompt commentary produced during the run (Prompt 1 through Prompt 5 Stage 1):

*Working declaration in use — findings carry reduced confidence — validity notice applies.*

---

### 3. Prompt 5 Stage 1 — Drift Detection Judgement review

When the Prompt 5 Stage 1 output arrives, provide your full unstructured review of the Drift Detection Judgement against the Canon.

In addition to your full review, assess the following criteria:

> *Note on Canon fourth sentence: migration encompasses all forms of denial boundary misalignment including never-built conditions and absence — it does not require a prior aligned state that subsequently moved. Apply the Canon test as: is denial currently operating at the decision point consistent with the scarcity of the resource?*

- Whether the Drift Detection Judgement is Canon-consistent
- Whether the Correct Decision Point finding has been carried through consistently from DDA Prompt 1
- Whether the Counter-Interpretation is genuinely adversarial — it must cite real evidence from the run and require a specific Canon-based rebuttal
- Whether the trajectory assessment is calibrated to the evidence quality available
- Whether the Finding Stability Frame has been formally reviewed and confirmed or revised at Prompt 5 Stage 1
- Whether any High confidence rating is inconsistent with the evidence quality across the run
- **Validity notice check** — If a working declaration is in use, confirm that the validity notice is present in the Prompt 5 Stage 1 output and will be reproduced in the Run Record.

State any concerns clearly. If there are no concerns, confirm the judgement is ready for Run Record production.

---

### 4. Receive the Run Record

Once the user has resolved any concerns and instructed ChatGPT Stage 2, ask them to paste the Run Record code block from ChatGPT into this session.

Do not produce the Run Record file until the code block is received.

Apply the following structured check:

Confirm that the Validity Notice field in the Run Record is correctly populated:
- If a working declaration was used: the field must reproduce the validity notice in full.
- If a fixed declaration was used: the field must state *Not applicable — fixed declaration.*

If absent or incorrect, flag as a Run Record gap before producing the file.

---

### 5. Produce the named Run Record file

Ask the user for their local time.

Format the Run Record into clean markdown and produce the correctly named file:

`DDA_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

Where SystemName is taken from the System Definition Statement in the Run Record and HHmm is the local time provided by the user.

---

### 6. Produce the Module Commentary Summary

Produce a compact structured summary of the key observations made during the DDA run commentary. Include the following sections:

**Declaration status:** [Fixed declaration / Working declaration — [candidate name] — validity notice attached]

**Drift Detection Judgement** — state the classification, drift form, severity rating, trajectory, and primary failure pathway

**Drift Origin Assessment** — state the origin classification and primary reason

**Counter-interpretation strength** — assess whether it was genuinely adversarial

**Readiness and evidence quality** — note the DAI readiness status inherited and the evidence quality across the DDA run

**Minimum Intervention Logic** — state the intervention profile and characterisation

**Structured check outcomes** — record the result of each mandatory structured check:
- Finding Stability Frame (Prompt 1): [present and complete / absent or incomplete]
- Finding Stability Review (Prompt 5): [Confirmed / Revised — state change]

**Carry-forward recommendations made** — list each recommendation made to ChatGPT during the run, the prompt it related to, and whether ChatGPT acted on it, partially acted on it, or did not act on it

**Unacted recommendations** — list any carry-forward recommendations that ChatGPT did not act upon. If all were acted upon, or no recommendations were made, state: *No unacted recommendations.*

**Residual uncertainties** — list any that should be carried forward. If a working declaration was used, include the validity notice as the first item with the notation: *Carry forward — attach to all downstream findings.*

Name the file:

`DDA_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

Use the same SystemName and time as the Run Record.

---

### 7. Rerun Assessment

This section is produced immediately after the Module Commentary Summary files. It is conditional — produce it only when a further run or Evidence model escalation is analytically warranted. If the run produces findings sufficient that no rerun is warranted and the Evidence model escalation condition is not met, this section is omitted entirely.

#### Assessment logic

**After each Desktop run (runs 1, 2, or 3):**

Assess the residual uncertainties and state whether a further Desktop run is analytically warranted. Consider:

- Are the primary unresolved threads of a kind that tighter SDS framing or a narrower system boundary could allow structural reasoning to resolve?
- Or are they fundamentally dependent on directly observed system behaviour, field-sourced data, or actor-specific confirmation that structural reasoning cannot substitute for?

**If a further Desktop run is warranted:**

- Suggest specific SDS revisions — tighter boundary, different time horizon, or revised failure condition — that would allow the primary unresolved threads to be tested.
- The suggested SDS must be narrower in scope than the current run. For runs 2 and 3 this is a hard requirement: a proposed SDS that widens scope relative to the current run is a hard stop — Claude must raise this as a concern and require the scope to be narrowed before the SDS can be confirmed. If the analyst wishes to widen scope, that is a new first run, not a continuation run, and a fresh session should be opened.
- The suggested SDS must also be operationally feasible within a single session. A full regional re-run is not appropriate as a second-run suggestion; a tighter national or sub-system boundary is. State explicitly that the SDS has been scoped with session feasibility in mind.
- State which residual uncertainty the next run is primarily designed to resolve.
- For runs 2 and 3, include an advisory on whether the remaining session resource appears sufficient to complete a full three-module run. If resource headroom looks insufficient, recommend opening a fresh session before proceeding.

**Evidence model escalation — can fire after any run (1, 2, or 3):**

If the residual uncertainties include at least one issue that is fundamentally unresolvable through structural reasoning alone, recommend an Evidence model run immediately — regardless of run number. Do not recommend a further Desktop run that would reproduce the same structural limitations.

Frame as: *"Desktop analysis has reached its resolution boundary on [specific issue]. The discrimination required cannot be achieved through structural reasoning alone. An Evidence model run, targeted at [specific empirical test], is the appropriate next step before findings are treated as operationally validated."*

**Three-run cap on Desktop runs:**

No further Desktop run is recommended after run 3 regardless of outcome. If the Evidence model escalation condition has not fired by run 3 close but material uncertainties remain, state that Desktop analysis has reached its limit and an Evidence model run should be considered to resolve what structural reasoning cannot.

#### Rerun Assessment output format

Present the following on screen immediately after the Commentary Summary files are produced:

---

**Rerun Assessment**

Run number: [1 / 2 / 3]

Further Desktop run warranted: [Yes / No]

Reason: [one sentence]

[If Yes — present the proposed SDS on screen for discussion:]

**Proposed SDS for next run:**

**System:** [narrower system identity]

**Boundary:** Includes [inclusions]. Excludes [exclusions].

**Failure Condition:** [revised or same]

**Time Horizon:** [duration window only — no calendar dates]

**Primary uncertainty this run is designed to resolve:** [one sentence]

**Session resource advisory:** [sufficient to proceed / recommend fresh session — reason] *(runs 2 and 3 only)*

**Evidence model escalation:** [Not triggered / Triggered — [specific issue and empirical test]]

---

#### SDS confirmation loop

After presenting the Rerun Assessment and proposed SDS on screen, do not produce the carry-over artefact file yet. Instead, present the following three questions using the structured menu tool, with options **Yes / No / Something else** for each:

1. Does this SDS describe the system you want to analyse in the next run?
2. Does the boundary feel right — does it include everything you consider part of the problem and exclude what you consider outside it?
3. Does the failure condition capture what failure actually looks like in this system?

If the analyst selects **Yes** to all three questions, proceed to validation.

If the analyst selects **No** or **Something else** to any question, ask them to describe the correction in plain language. Apply the correction to the relevant field, restate the revised field on screen, and re-present all three questions using the structured menu tool again. Continue iterating until all three questions are answered **Yes**.

**Hard stop — scope widening:** If the analyst proposes a boundary or system identity that is wider in scope than the current run's SDS, do not accept it. State clearly that runs 2 and 3 must be narrower in scope than the current run by definition. If the analyst wishes to widen scope, advise them to open a fresh session and begin a new first run. Do not proceed with a widened SDS.

**Validation before locking:** Once all three confirmation questions are answered affirmatively, apply the following validation criteria before treating the SDS as confirmed:

- System identity is named at the right level of specificity
- Boundary inclusions are genuinely within the operational frame
- Boundary exclusions do not inadvertently exclude mechanisms relevant to the failure condition
- Failure condition is observable and unambiguous
- Time horizon is specific and analytically meaningful
- Time horizon contains no calendar dates — if a date range is present, remove it and restate as a duration window only
- The four fields are internally consistent
- The proposed SDS is narrower in scope than the current run's SDS — if not, apply the scope-widening hard stop above

If validation passes, state: *"The carry-over SDS is confirmed."* Then proceed to produce the carry-over artefact file.

---

#### Carry-Over SDS Artefact *(produced only after the SDS confirmation loop completes successfully)*

Produce this as a named file:

`SDS_Carryover_[SystemName]_[YYYY-MM-DD].md`

Where SystemName is the system name from the **proposed next run** (not the current run) and the date is today's date.

File contents:

```markdown
# Carry-Over System Definition Statement

**Produced by:** DDA Rerun Assessment — Run [number]
**Source run:** [DDA Run Record filename]
**Date:** [YYYY-MM-DD]
**Primary uncertainty this run is designed to resolve:** [one sentence from Rerun Assessment]

---

## Suggested System Definition Statement

**System:** [confirmed narrower system identity]

**Boundary:** Includes [confirmed inclusions]. Excludes [confirmed exclusions].

**Failure Condition:** [confirmed failure condition]

**Time Horizon:** [confirmed duration window — no calendar dates]

---

## Rationale for scope change

[Two to three sentences explaining why the boundary was narrowed or the failure condition revised — what the prior run found that motivated this framing.]

---

## Residual uncertainties carried forward from prior run

[List the key residual uncertainties from the current run's DDA Commentary Summary that remain live going into the next run.]

---

*Carry-over artefact — upload to the next Claude companion session to open Phase 1.*
*© Philip Harry Galvin 2026. Scarcity–Denial Canon and derived works. Licensed CC BY-NC-ND 4.0.*
```

---

## User Next Step

Save all files produced by Claude:
- `DDA_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DDA_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `SDS_Carryover_[SystemName]_[YYYY-MM-DD].md` *(if a further run was recommended and the SDS confirmation loop completed)*

If a carry-over artefact was produced, this is the file to upload when opening the next Claude companion session.

Do not open a new Claude session for the current run.

---

*Version 0.4.5 — companion to DDA v1.6*

*© Philip Harry Galvin 2026. Scarcity–Denial Canon and derived works. Licensed CC BY-NC-ND 4.0. No derivative works without prior written approval.*
