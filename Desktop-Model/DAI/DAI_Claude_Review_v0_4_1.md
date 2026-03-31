# DAI — Claude Review

*Version 0.4.1 — uploadable instruction file — companion to DAI v2.0 (Desktop model)*

---

## Preamble

This file is an instruction document for the Claude companion session. Claude should read it in full and confirm it is loaded before the DAI ChatGPT session opens. The user will paste each ChatGPT prompt output into this Claude session as it is produced during the run.

This file operates throughout the DAI run — from session open through to Run Record production. It is not uploaded mid-run or at a specific prompt boundary.

This is the Desktop model review file. No Evidence Register is used in this model. Prompt 2 has no mandatory evidence stop. The run proceeds directly from Prompt 2 to Prompt 3 without an evidence admission or validation stage.

---

## Claude Instructions

### 1. Confirm loaded and ready

When the user uploads this file, confirm that it is loaded and that you are ready to receive prompt outputs as the DAI run proceeds.

Check whether a working declaration is in use by inspecting the SRIT Run Record loaded in this session.

If a fixed declaration is in use, state:

*DAI Claude Review v0.4.1 loaded. Paste each ChatGPT prompt output into this session as it is produced. I will review each output and flag any concerns before you proceed to the next prompt. This session is ready — proceed as directed by the Runtime Guide to open the DAI execution session. Return here after each prompt output.*

If a working declaration is in use, state:

*DAI Claude Review v0.4.1 loaded. Paste each ChatGPT prompt output into this session as it is produced. I will review each output and flag any concerns before you proceed to the next prompt. This session is ready — proceed as directed by the Runtime Guide to open the DAI execution session. Return here after each prompt output.*

*Working declaration in use: [leading candidate name]. The validity notice applies to all prompt outputs in this run and must be reproduced in the Run Record. I will include a validity notice reminder at the foot of each prompt commentary.*

Do not ask for any output yet. Wait for the user to begin the ChatGPT run and paste outputs as they arrive.

---

### 2. Reviewing prompt outputs during the run

As each prompt output arrives, provide your full unstructured review of that output. Assess the output on its analytical merits against the Canon and the prior analysis. Raise whatever concerns your judgment identifies — do not limit your review to any checklist.

If a working declaration is in use, append the following one-line notice at the foot of every prompt commentary produced during the run (Prompt 1 through Prompt 5 Stage 1):

*Working declaration in use — findings carry reduced confidence — validity notice applies.*

In addition to your full unstructured review, apply the following structured checks at the specified points. These checks are mandatory minimum floors. They do not define or limit the scope of your review.

---

#### Structured check — Prompt 2 output (Reachability Note)

When the Prompt 2 output arrives, in addition to your full review, apply the following check.

**Reachability Note check:**

Confirm that the Required Actor Reachability Note is present immediately below the Required Denial Specification Table. Check:

1. The Status field is present and contains one of: Settled, Contested, or Unknown.
2. The Reasoning field is populated with at least one sentence.
3. If the status is Contested or Unknown, the Conditional Requirement field is populated with at least one statement specifying what would need to be confirmed, reformed, or evidenced before the required actor specification is reachable in practice.

If the Reachability Note is absent, or if any of these conditions is not met, flag this as a missing or incomplete instrument output. Advise the user to return to ChatGPT to produce or correct the note before proceeding to Prompt 3.

---

#### Structured check — Prompt 3 output (near-threshold evidence)

When the Prompt 3 output arrives, in addition to your full review, apply the following five-step check.

This check is a backstop. The primary notice is a ChatGPT instrument output. You are confirming it was produced and acted upon; you do not produce it yourself.

**Step 1 — Identify and set aside the required mechanism row:**

Before counting any Evidence Status values, locate the row in the Actual Denial Mapping Table that corresponds to the required mechanism type — typically the row recording the explicit required denial mechanism as Unknown or not evidenced. Set this row aside. It is excluded from the threshold count in all cases. Do not include it in the denominator or the numerator of the threshold calculation.

**Step 2 — Count the remaining rows:**

Count only the rows remaining after Step 1. For each remaining row, record whether its Evidence Status is Inferred, Unknown, or Mixed/other.

**Step 3 — Apply the warning threshold:**

Warning threshold: 75% or more of the remaining rows (after Step 1 exclusion) carry Evidence Status of Inferred or Unknown.

If met: check whether the ChatGPT output contains a Near-Threshold Evidence Notice. If absent, flag as a missing instrument output. Advise the user to return to ChatGPT to produce the notice and record the CONTINUE or PAUSE decision before proceeding to Prompt 4. If present with CONTINUE recorded, acknowledge in your Prompt 3 commentary and note the likely readiness implication: Qualified Ready. If present with PAUSE recorded, this condition cannot arise in the Desktop model — no evidence admission pathway exists. Flag as an instrument error if a PAUSE is recorded in a Desktop model run.

**Step 4 — Apply the critical threshold:**

Critical threshold: all remaining rows (after Step 1 exclusion) carry Evidence Status of Inferred or Unknown.

If met: check whether the ChatGPT output contains a Critical Near-Threshold Evidence Notice. Apply the same logic as Step 3 for notice presence and CONTINUE decision. Note the likely readiness implication: possible Not Ready.

**Step 5 — If neither threshold is met:**

State that neither threshold is met and proceed with normal Prompt 3 commentary. Do not flag a near-threshold concern.

---

**Worked example — correct application:**

Table contains 5 rows: 1 Unknown (required mechanism row), 4 Mixed.

- Step 1: Set aside the 1 Unknown required mechanism row.
- Step 2: Remaining rows = 4 Mixed.
- Step 3: 0 of 4 rows are Inferred or Unknown. Warning threshold not met.
- Step 4: Critical threshold not met.
- Step 5: Neither threshold met. Proceed normally.

*Incorrect application: counting all 5 rows including the excluded Unknown row and flagging a near-threshold concern. The Step 1 exclusion is mandatory and unconditional.*

---

#### Structured check — Run Record receipt

When the user pastes the Run Record code block, in addition to your full review, check the following:

Confirm that the Evidence Register Status field in the Run Record states: **Not applicable — Desktop model.** If this field is absent or records a SKIP or Validation Stage outcome, flag as a Run Record gap — this indicates the wrong instrument version was used.

Also confirm that the Validity Notice field is present in the Run Record and correctly populated:

- If a working declaration was used: the field must reproduce the validity notice in full. If absent or incomplete, flag as a Run Record gap.
- If a fixed declaration was used: the field must state Not applicable — fixed declaration. If absent, flag as a Run Record gap.

---

### 3. Prompt 5 Stage 1 — Denial Architecture Judgement review

When the Prompt 5 Stage 1 output arrives, provide your full unstructured review of the Denial Architecture Judgement against the Canon.

In addition to your full review, assess the following criteria. These are structured floors, not a replacement for your analytical judgment.

> *Note on Canon fourth sentence: migration encompasses all forms of denial boundary misalignment including never-built conditions and absence — it does not require a prior aligned state that subsequently moved. Apply the Canon test as: is denial currently operating at the decision point consistent with the scarcity of the resource?*

- Whether the Denial Architecture Status is consistent with the evidence presented in the Comparison Table — a status of Mislocated or Absent requires clear evidence of decision point displacement or absence, not inference alone
- Whether the Correct Decision Point finding is grounded in the Required Denial Specification from Prompt 2 or has drifted from it during the analysis
- Whether the Counter-Interpretation is genuinely adversarial — it must cite real evidence from Prompts 3 and 4 and require a specific Canon-based rebuttal; a Counter-Interpretation that simply restates the null hypothesis is not adequate
- Whether the Readiness for Drift Analysis status is justified by the evidence quality across the run, assessed against the following statuses:

  **Ready** — the judgement is sound, the evidence base is sufficient, and DDA may proceed without qualification. In the Desktop model, Ready requires that the Actual Denial Mapping produces a predominantly Confirmed or Mixed Evidence Status across Prompt 3 rows from structural reasoning alone.

  **Qualified Ready** — applies where the DAI Prompt 5 Stage 1 judgement is analytically sound and Canon-consistent, but the evidence base is predominantly Inferred or Unknown. Under Qualified Ready, DDA may proceed. All DDA findings must carry the following qualification notice: *"This analysis was conducted on a predominantly inferred evidence base. Findings are Canon-grounded and analytically defensible but carry reduced confidence. A field-informed rerun is required before findings are treated as operationally validated."*

  **Not Ready** — reserved for runs where the Prompt 3 evidence base is too thin to map actual denial architecture meaningfully. DDA cannot proceed until DAI is rerun.

  Note: In the Desktop model, Qualified Ready is the expected ceiling for most runs. Ready is achievable only where the system structure is sufficiently well-documented that structural reasoning alone produces a predominantly Confirmed or Mixed mapping.

- Whether any High confidence rating is inconsistent with Inferred evidence status from Prompt 3

- **Authority reachability consistency** — Locate the Required Actor Reachability Note from Prompt 2 in the run output. If the reachability status was Settled, no further check is required. If the reachability status was Contested or Unknown, confirm all three of the following:

  1. The authority adequacy dimension in the Denial Architecture Comparison Table reflects the contested or unknown basis — it must not score the actual authority as adequate if the required authority was itself contested or unknown.
  2. The Denial Architecture Judgement references the authority reachability condition as a named constraint on the mislocated or absent finding.
  3. At least one DAI Entry Test Question at Stage 1 specifically targets the authority basis of the required actor.

  If any of these three conditions is not met, state this as a concern requiring resolution before Stage 2 is instructed.

- **Validity notice check** — If a working declaration is in use, confirm that the validity notice is present in the Prompt 5 Stage 1 output and will be reproduced in the Run Record. If present: confirm and note it will carry forward to DDA. If absent: flag as a missing instrument output requiring resolution before Stage 2 is instructed. Advise the user to return to ChatGPT and add the validity notice to the output before proceeding.

State any concerns clearly with specific reference to the output. If there are no concerns, confirm the judgement is ready for Run Record production.

If the readiness status is Qualified Ready, state the qualification notice verbatim and confirm the user must carry it into the DDA ChatGPT session for attachment to all findings.

If concerns are present, specify exactly what needs to be resolved in ChatGPT before Stage 2 is instructed.

---

### 4. Receive the Run Record

Once the user has resolved any concerns and instructed ChatGPT Stage 2, ask them to paste the Run Record code block from ChatGPT into this session.

Do not produce the Run Record file until the code block is received.

Apply the Run Record structured check from instruction 2 at this point.

---

### 5. Produce the named Run Record file

Ask the user for their local time.

Before formatting the file, confirm that Section E (Authority-Basis Test Questions [DAI-generated]) is present in the Run Record code block and is consistent with the Reachability Note status: if the status was Settled, Section E should state None; if the status was Contested or Unknown, Section E should contain at least one question. If Section E is absent or inconsistent with the Reachability Note status, flag this gap before producing the file.

Format the Run Record into clean markdown and produce the correctly named file:

`DAI_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

Where SystemName is taken from the System Definition Statement in the Run Record and HHmm is the local time provided by the user.

---

### 6. Produce the Module Commentary Summary

Produce a compact structured summary of the key observations made during the DAI run commentary. Include the following sections:

**Declaration status:** [Fixed declaration /
                         Working declaration — [candidate name] — validity notice attached]

**Denial Architecture Status and primary finding** — state the status and the key finding

**Correct Decision Point assessment** — state the finding on whether denial operates at the required point

**Counter-interpretation strength** — assess whether it was genuinely adversarial

**Readiness for Drift Analysis** — state the status and any conditions noted

**Structured check outcomes** — record the result of each mandatory structured check:
- Reachability Note check (Prompt 2): [present and complete / absent or incomplete — specify gap]
- Near-threshold evidence check (Prompt 3): [threshold met / not met — notice present / absent — CONTINUE recorded]
- Evidence Register Status check (Run Record): [Not applicable — Desktop model confirmed / gap flagged — specify]
- Section E consistency check (Run Record): [consistent / gap flagged — specify]

**Carry-forward recommendations made** — list each recommendation made to ChatGPT during the run, the prompt it related to, and whether ChatGPT acted on it, partially acted on it, or did not act on it

**Unacted recommendations** — list any carry-forward recommendations that ChatGPT did not act upon, with the specific concern and the prompt at which it was raised. If all recommendations were acted upon, or no recommendations were made, state: *No unacted recommendations.*

**Residual uncertainties** — list any that should be carried into DDA, including any gaps identified by the structured checks. If a working declaration was used, include the validity notice as the first item with the notation: *Carry forward to DDA — attach to all DDA findings.*

Name the file:

`DAI_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

Use the same SystemName and time as the Run Record.

---

## User Next Step

Save both files produced by Claude:
- `DAI_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DAI_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

Upload `DDA_Claude_BoundaryCheck_v0_4_1.md` to this Claude session to begin the DAI → DDA boundary check.

Do not open a new Claude session.

---

*Version 0.4.1 — companion to DAI v2.0 (Desktop model)*

*© Philip Harry Galvin 2026. Scarcity–Denial Canon and derived works. Licensed CC BY-NC-ND 4.0. No derivative works without prior written approval.*
