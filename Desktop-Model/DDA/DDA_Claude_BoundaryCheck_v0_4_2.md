# DDA — Claude Boundary Check

*Version 0.4.2 — uploadable instruction file — companion to DDA v1.5*

---

## Preamble

This file is an instruction document for the Claude companion session. Claude should read it in full and execute the instructions below. The user has uploaded this file at the DAI → DDA module boundary.

---

## Claude Instructions

### 1. Confirm session continuity

Confirm that this is the same Claude session used for the SRIT and DAI run commentary. If this appears to be a new session with no prior context, state this clearly and ask the user to confirm before proceeding.

### 2. Receive the DAI Run Record

Ask the user to upload or paste the DAI Run Record produced at the close of the DAI module. The filename will follow the convention:

`DAI_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

Do not proceed until the Run Record is received.

### 3. Check the Readiness for Drift Analysis gate

Locate the Readiness for Drift Analysis field in the DAI Run Record.

If the status is **Not Ready**: halt. Inform the user that DDA cannot proceed. State the missing requirement as recorded in the Run Record. The user must resolve the gap — typically by rerunning DAI with Evidence Register data — before DDA can begin.

If the status is **Qualified Ready**: DDA may proceed. State the qualification notice verbatim from the DAI Run Record and instruct the user to carry it into the DDA ChatGPT session for attachment to all findings.

If the status is **Ready**: proceed.

### 4. Check input completeness

Verify the following fields are present in the DAI Run Record:

- System Definition Statement
- Binding Scarce Resource Declaration
- Denial Architecture Status
- Required Denial Decision Point
- Denial Architecture Judgement
- Binding Reality Summary
- Readiness for Drift Analysis
- Admitted Evidence Register Status

Note any absent fields and flag them in your readiness output.

### 5. Check validity notice carry-forward

Locate the Validity Notice field in the DAI Run Record.

**If the field states Not applicable — fixed declaration:** no action required. Proceed with existing checks.

**If the field records a working declaration:**

1. Reproduce the validity notice in full in the boundary check output
2. State explicitly that all DDA findings must carry this notice
3. Ask the user to confirm they understand before the DDA ChatGPT session opens
4. Do not allow the validity notice to be silently dropped at the DAI → DDA boundary

**If the Validity Notice field is absent from the DAI Run Record:** flag this as a Run Record gap. Ask the user to confirm whether a working declaration or fixed declaration was used in the DAI run before proceeding. Do not assume fixed declaration by default.

### 6. Note and state the Denial Architecture Status

Locate and state the Denial Architecture Status. This determines the DDA starting posture:

- **Mislocated** — drift is the primary hypothesis
- **Aligned but fragile** — drift risk and boundary erosion are the primary concern
- **Partially aligned** — test which dimensions are drifting and which are holding
- **Symbolic or Absent** — test whether denial ever existed at the required point

State the status and its DDA starting posture clearly so the user carries this into the DDA ChatGPT session.

### 7. Confirm context files loaded

Confirm that the following files are loaded as context in this session. If any are missing, ask the user to upload them before proceeding:

- `Scarcity_Denial_Canon.md`
- `DDA_Prompts_v1_5.md`

---

## Claude Output Format

Produce a single structured response in the following format:

**DDA Boundary Check — [SystemName]**

Readiness gate: [Ready / Not Ready — reason]

Input completeness: [Complete / Incomplete — list missing fields]

Denial Architecture Status: [status] — [DDA starting posture]

Validity notice: [Not applicable — fixed declaration /
                  Present — working declaration on [candidate name] — carried forward — user confirmed /
                  Gap — Validity Notice field absent from DAI Run Record — user confirmation pending]

Context files: [Confirmed / Missing — list missing files]

Readiness: [Ready to proceed to DDA / Not ready — reason]

If Ready: state the Binding Scarce Resource Declaration verbatim from the DAI Run Record so the user can confirm it is correct before the DDA ChatGPT session opens.

---

## User Next Step

When Claude confirms Ready, note the Denial Architecture Status and its DDA starting posture. Proceed as directed by the Runtime Guide to open the DDA execution session.

Note: DDA Prompt 1 will produce three outputs — the DDA Input Receipt Table, the Drift Boundary Lock Statement, and a Finding Stability Frame. The Finding Stability Frame records the principal unresolved dimension carried from DAI, the primary rival interpretation to test, preliminary rerun trigger conditions, and the opening trajectory posture. It does not constitute a drift judgement. It will be formally reviewed and confirmed or revised at Prompt 5 Stage 1.

If Claude confirms Not Ready, address the identified gaps before proceeding.

---

*Version 0.4.2 — companion to DDA v1.5*

*© Philip Harry Galvin 2026. Scarcity–Denial Canon and derived works. Licensed CC BY-NC-ND 4.0. No derivative works without prior written approval.*
