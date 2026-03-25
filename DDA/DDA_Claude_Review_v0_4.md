# DDA — Claude Review

*Version 0.4 — uploadable instruction file — companion to DDA v1.5*

---

## Preamble

This file is an instruction document for the Claude companion session. Claude should read it in full and execute the instructions below. The user has uploaded this file after receiving the DDA Prompt 5 Stage 1 output from ChatGPT.

---

## Claude Instructions

### 1. Receive the Stage 1 output

Ask the user to paste the DDA Prompt 5 Stage 1 output from ChatGPT into this session.

Do not proceed until it is received.

### 2. Review the Drift Detection Judgement against the Canon

Assess the Stage 1 output against the Scarcity–Denial Canon. Identify any concerns with:

- Whether the Drift Status is consistent with the Drift Signal Register and Boundary Displacement findings — a Drift Confirmed status requires traceable signals pointing to actual displacement, not inference from absence alone
- Whether the Minimum Intervention Logic addresses the Canon's fourth sentence directly — each action must propose something that would return the denial boundary to the correct decision point; actions that address symptoms rather than the displaced boundary are over-reach
- Whether any mixed signals from the Drift Signal Register have been forced to a single resolution rather than preserved as mixed — forced resolution of a mixed signal is an analytical error
- Whether the Overall Drift Severity is consistent with the individual severity ratings across the Drift Signal Register — an overall High severity requires at least two individual High or Critical dimension ratings
- Whether the Strongest Counter-Interpretation is genuinely adversarial or restates the null hypothesis without evidence
- Whether the Drift Trajectory Assessment (Section B) is supported by the evidence in the Drift Signal Register and Boundary Displacement Test Table — the trajectory status must be grounded in identifiable directional forces; if the record does not support a directional assessment, the status must be stated as Unknown rather than omitted or defaulted to Stable
- Whether the Finding Stability Review (Section F) correctly confirms or revises the Prompt 1 Finding Stability Frame — specifically: is the rival interpretation result consistent with the Drift Signal Register and Boundary Displacement Test evidence, and are the rerun trigger conditions still live or resolved by the analysis?

### 3. State your assessment

State any concerns clearly with specific reference to the output. If there are no concerns, confirm the judgement is ready for Run Record production.

If concerns are present, specify exactly what needs to be resolved in ChatGPT before Stage 2 is instructed.

### 4. When the judgement is confirmed ready — receive the Run Record

Once the user has resolved any concerns and instructed ChatGPT Stage 2, ask them to paste the Run Record code block from ChatGPT into this session.

Do not produce the Run Record file until the code block is received.

### 5. Produce the named Run Record file

Ask the user for their local time.

Format the Run Record into clean markdown and produce the correctly named file:

`DDA_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

Where SystemName is taken from the System Definition Statement in the Run Record and HHmm is the local time provided by the user.

Verify that the Run Record contains all required sections, including the Finding Stability Frame (Prompt 1 Section C) and the Finding Stability Review (Prompt 5 Section F). Flag any absent sections before presenting the file.

### 6. Produce the Module Commentary Summary

Produce a compact structured summary of the key observations made during the DDA run commentary. Include the following sections:

**Drift Detection Status and primary finding** — state the status and the key finding

**Drift Trajectory Assessment** — state the trajectory status, the directional forces identified, and the trajectory confidence

**Minimum Intervention Logic** — summarise the key actions identified

**Mixed signal handling** — note any mixed signals and how they were handled

**Overall Drift Severity consistency** — assess whether the overall severity was consistent with the evidence

**Finding Stability Frame and Review** — state the opening trajectory posture and unresolved dimension from the Prompt 1 Frame; note whether the Prompt 5 Finding Stability Review confirmed or revised the Frame; note any material change between the opening and closing analytical posture

**Carry-forward recommendations made** — list each recommendation made to ChatGPT during the run, the prompt it related to, and whether ChatGPT acted on it, partially acted on it, or did not act on it

**Unacted recommendations** — list any carry-forward recommendations that ChatGPT did not act upon, with the specific concern and the prompt at which it was raised. If all recommendations were acted upon, or no recommendations were made, state: *No unacted recommendations.*

**Empirical tests for next stage** — list any identified for further investigation

Name the file:

`DDA_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

Use the same SystemName and time as the Run Record.

---

## Claude Output Format

Produce outputs in this sequence:

1. Judgement assessment — concerns or confirmation of readiness
2. *(After Stage 2 and Run Record receipt)* The formatted Run Record file
3. The Module Commentary Summary file

---

## User Next Step

Save both files produced by Claude:
- `DDA_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DDA_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

The DDA Run Record and Commentary Summary complete the three-module pipeline run. All six artefacts are now saved:

- `SRIT_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `SRIT_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DAI_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DAI_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DDA_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DDA_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

The Claude companion session may now be closed.

---

*Version 0.4 — companion to DDA v1.5*

*© Philip Harry Galvin 2026. Scarcity–Denial Canon and derived works. Licensed CC BY-NC-ND 4.0. No derivative works without prior written approval.*
