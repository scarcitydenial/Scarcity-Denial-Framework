# Scarcity–Denial Framework — Runtime Guide (Desktop Model)

*Version 0.6.0*

\---

## Purpose

This document sequences a complete three-module Desktop model pipeline run from first session to final artefact. It covers the Desktop model only — pure structural analysis, no Evidence Register, no PRRP pre-run research package required.

For the Evidence-informed model, a separate Runtime Guide will be produced once that model is in production.

Read this document before beginning any run. Keep it open alongside the module operational documents during the run.

\---

## The Two-Platform Architecture

Every run uses two platforms operating in parallel throughout:

**Claude Sonnet 4.6** — one session, opened before the run begins, kept open for the entire three-module run. Handles system description preparation, active commentary on every ChatGPT prompt output, Stage 1 review at each module boundary, Run Record formatting and naming at each module close, and Module Commentary Summary production.

**ChatGPT GPT-5.4 Thinking Extended** — three separate sessions, one per module. Handles analytical execution only.

\---

## How the Two Platforms Are Instructed

The two platforms require different instruction methods by design. This is intentional, not an inconsistency.

### Claude — uploadable instruction files

Claude-facing documents are uploaded directly to the Claude companion session. Claude reads and executes them. The user does not need to interpret these documents — Claude manages the step and tells the user what to do next.

After reviewing each prompt output, Claude will either provide commentary only, or commentary plus a **carry-forward note** — a reasoned recommendation for ChatGPT's consideration before the next prompt fires. Carry-forward notes are recommendations, not overrides. ChatGPT may accept them, partially accept them, or proceed without acting on them. Any recommendation that ChatGPT does not act upon will be recorded in the Unacted Recommendations section of the Module Commentary Summary.

Documents used this way, in run order:

* `SDS_Claude_Construction_Desktop_v05.md` — uploaded to open the session. Phase 1 constructs the System Definition Statement (or confirms a carry-over SDS artefact from a prior run); Phase 2 initialises the full-run companion role
* `SRIT_Claude_Review_v0_3_6.md` — uploaded after SRIT ChatGPT Prompt 6 Stage 1
* `DAI_Claude_BoundaryCheck_v0_4_0.md` — uploaded at the SRIT → DAI boundary
* `DAI_Claude_Review_v0_4_1.md` — uploaded at the SRIT → DAI boundary, immediately after the Boundary Check confirms Ready, before the DAI ChatGPT session opens
* `DDA_Claude_BoundaryCheck_v0_4_2.md` — uploaded at the DAI → DDA boundary
* `DDA_Claude_Review_v0_4_5.md` — uploaded after DDA ChatGPT Prompt 5 Stage 1

### ChatGPT — drag-and-drop files plus copy-paste opening instruction

ChatGPT-facing documents use a two-part approach:

**Drag and drop** — the Canon and Prompt architecture files are dragged into the ChatGPT session as document context. ChatGPT reads them as the governing framework and execution protocol.

**Copy-paste opening instruction** — each ChatGPT RunSetup document contains an opening instruction block that must be pasted as direct user text. This is intentional. The opening instruction establishes the behavioural constraints, model and thinking mode requests, and session framing before ChatGPT begins processing. An uploaded file cannot do this — ChatGPT would treat it as a document to analyse rather than as a governing instruction. The copy-paste method ensures the instruction is received as a direct command.

Do not attempt to upload the opening instruction block as a file. Copy and paste it exactly as written in the RunSetup document.

\---

## Note on the Canon

The Canon is loaded multiple times during a full 3 module run — once into the Claude companion session during Phase 2 initialisation of `SDS_Claude_Construction_Desktop_v05.md`, and once into each fresh ChatGPT session at the start of each new module run. This is correct and necessary. Claude and ChatGPT are independent sessions — each requires the Canon as its governing context.

\---

## Session Overview

|#|Platform|Session|Opens|Closes|
|-|-|-|-|-|
|1|Claude Sonnet 4.6|Companion session|Before SRIT begins|After DDA Commentary Summary is saved|
|2|ChatGPT GPT-5.4|SRIT execution|Full Run Step 2|After SRIT Run Record pasted to Claude|
|3|ChatGPT GPT-5.4|DAI execution|Full Run Step 12|After DAI Run Record pasted to Claude|
|4|ChatGPT GPT-5.4|DDA execution|Full Run Step 21|After DDA Run Record pasted to Claude|

The Claude companion session is never closed between modules. The three ChatGPT sessions are each opened fresh and closed after the Run Record is handed to Claude.

\---

## Model Selection

This Runtime Guide covers the Desktop model only. The Desktop model is the default execution path — pure structural analysis, SDS constructed by Claude, no pre-run research required.

If you intend to run the Evidence-informed model, a separate Runtime Guide is required. Do not use this document for Evidence-informed model runs.

\---

## System Definition Statement — Pre-Run Requirement (Both Models)

Before the SRIT ChatGPT session opens, a confirmed System Definition Statement must exist. The SDS is constructed by Claude in the companion session — not by ChatGPT.

**Step 0** (before Step 1 below): In the Claude companion session, Claude will first ask whether a carry-over SDS artefact exists from a prior run. If one exists, upload it — Claude will confirm the four fields and lock it directly. If not, present your plain language problem statement and Claude will construct the SDS, confirm all four fields, and lock it. In either case, copy the confirmed SDS block — it will be pasted into ChatGPT at Step 5.

Do not open the SRIT ChatGPT session until the SDS is confirmed and locked in Claude.

\---

### Before the run

**1.** Open a new Claude Sonnet 4.6 session. Upload `SDS_Claude_Construction_Desktop_v05.md`.

Submit.

Claude will read the file and open Phase 1. Claude will first ask whether a carry-over SDS artefact exists from a prior run. If one exists, upload it and Claude will confirm the four fields with a brief three-question loop before locking. If not, present your plain language problem statement and Claude will construct the SDS in full. In either case, once locked, Claude will reproduce the confirmed SDS block inline — copy it directly from Claude's response for use at Step 5. This is **Step 0** of the run — the SDS must be confirmed before the SRIT ChatGPT session opens.

When the SDS is locked, Claude will transition automatically into Phase 2. In Phase 2, drag the following four files into the session when Claude requests them:

- `Scarcity_Denial_Canon.md`
- `SRIT_Prompts_v2_2.md`
- `DAI_Prompts_v2_1.md`
- `DDA_Prompts_v1_6.md`

Submit.

Claude will confirm receipt, state its companion role, and signal readiness. Do not close this session for the remainder of the run.

---

### SRIT module

**2.** Open a fresh ChatGPT session. Pin model to GPT-5.4 Thinking Extended manually — do not use auto mode.

**3.** Drag and drop into ChatGPT in this order:

- `Scarcity_Denial_Canon.md`
- `SRIT_Prompts_v2_2.md`

Submit.

**4.** Copy the opening instruction block from `SRIT_ChatGPT_RunSetup_v0.1.txt` and paste it into ChatGPT. ChatGPT will confirm its execution mode and state that it is ready to receive the System Definition Statement. It will wait silently — it will not request the SDS or produce any further output until it arrives.

Submit.

**5.** Paste the confirmed System Definition Statement produced by Claude in Phase 1 and Submit. ChatGPT will confirm receipt and apply the three internal consistency checks. If all checks pass, ChatGPT will stop and wait for the explicit instruction `Proceed.` — it does not advance to Prompt 2 automatically. If any check fails, ChatGPT will state the inconsistency and instruct you to return to the Claude companion session to resolve it before proceeding.

**6.** After each prompt output, use **Copy response** from ChatGPT and paste it to the Claude companion session. Read Claude's commentary carefully. Claude will label every observation as one of three types:

- **Note only** — for awareness; do not paste to ChatGPT. Type `Proceed.` alone.
- **Carry-forward note — ready to paste** — paste this to ChatGPT alongside `Proceed.` before the next prompt fires.
- **Blocking concern** — resolve this in ChatGPT before proceeding. Do not type `Proceed.` until Claude confirms the concern is resolved.

If Claude provides no labelled observation, type `Proceed.` alone.

Submit.

**7.** After Prompt 5 output has been reviewed by Claude, type `Proceed.` in ChatGPT to run Prompt 6 Stage 1. ChatGPT will produce the complete declaration output and stop before the Run Record.

**8.** Use **Copy response** from ChatGPT to copy the complete Prompt 6 Stage 1 output and paste it to the Claude companion session. Before submitting, confirm that the SRIT Claude Review file (`SRIT_Claude_Review_v0_3_6.md`) has already been uploaded to this session. If it has not been uploaded, upload it now before submitting the Prompt 6 Stage 1 output. Submit.

Claude will review the declaration against the Canon, assessing: resource/mechanism distinction, selection rationale grounding, strongest alternative rejection, confidence rating consistency, DAI entry test question quality, and whether the Protectable Resource Form (Prompt 6 Section B) is present and operationally specific — specifying what must be preserved, in what state, at what level, and what substitution would fail (absence or imprecision will be flagged as a concern; an adequate form will be confirmed as pre-populating the DAI Prompt 2 Required Denial Specification Table).

For R6 eliminations: an adversarial challenge record is required only for a candidate that was placed under adversarial challenge after Step 3 remained contested — it is not required for every R6 elimination. If any R6 elimination was genuinely contested and an adversarial challenge record was not produced at Prompt 4, Claude will flag this as a Prompt 4 omission requiring corrective completion before Stage 2 is instructed, because Stage 2 reproduces existing records and cannot generate them retrospectively. If no R6 eliminations were contested, the Run Record will state None in the Adversarial Challenge Record(s) section and that is correct.

If Claude identifies concerns, resolve them in ChatGPT before proceeding. If Claude confirms the declaration is ready, return to ChatGPT and type `Execute Run Record`.

**9.** When ChatGPT produces the Run Record code block, use **Copy** from the top right of the code block and paste it to the Claude companion session. Claude will ask for your local time, format the Run Record, and produce both files:

- `SRIT_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `SRIT_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

**10.** Save both files.

---

### SRIT → DAI boundary

**11.** Upload `DAI_Claude_BoundaryCheck_v0_4_0.md` to the Claude companion session. Claude will check the SRIT Run Record for completeness, confirm readiness, and state the Binding Scarce Resource Declaration for confirmation.

Submit.

When Claude confirms Ready, upload `DAI_Claude_Review_v0_4_1.md` to the same Claude session. Claude will confirm it is loaded and ready. Do not open the DAI ChatGPT session until Claude confirms the Review file is loaded.

Submit.

---

**Note on SDS quality in the Desktop model:** The System Definition Statement is constructed by Claude from the analyst's plain language problem statement. For systems that Claude has encountered in prior analytical work or that are well-documented in training data, the first draft SDS will reflect absorbed prior knowledge and may be more precise than the analyst's input alone would produce. This is not contamination — it is Claude's familiarity with the system. For unfamiliar systems, the confirmation loop in Phase 1 is the mechanism for correcting imprecision. Either way, the analyst confirms the SDS before it is locked.

### DAI module

**12.** Open a fresh ChatGPT session. Pin model to GPT-5.4 Thinking Extended manually — do not use auto mode.

**13.** Drag and drop into ChatGPT in this order:

- `Scarcity_Denial_Canon.md`
- `DAI_Prompts_v2_1.md`
- The SRIT Run Record (`SRIT_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`)

Submit.

**14.** Copy the opening instruction block from `DAI_ChatGPT_RunSetup_v0.1.txt` and paste it into ChatGPT. Type `Proceed.` to begin Prompt 1.

Submit.

### Ambiguous declaration at Prompt 1

If the SRIT run returned an ambiguous result at Prompt 6, the Claude Boundary Check will have flagged this, reproduced the validity notice, and asked for your confirmation before the DAI session opened.

When DAI Prompt 1 is executed in ChatGPT, it will return a **Conditional Continuation Available** halt rather than a full hard stop. The output will contain:

- the DAI Input Integrity Halt header identifying the missing fixed declaration
- the leading candidate name and current leading Protectable Resource Form from the SRIT Run Record
- the validity notice in full
- a binary choice: confirm to continue on the working declaration, or halt and return to SRIT

Read the validity notice carefully before confirming. If you confirm continuation, ChatGPT will proceed on the working declaration with the validity notice attached to all outputs from that point forward through to and including DDA.

If you halt, return to SRIT and produce a fixed declaration before restarting DAI Prompt 1.

**15.** After each prompt output, use **Copy response** from ChatGPT and paste it to the Claude companion session. Read Claude's commentary carefully. Claude will label every observation as one of three types:

- **Note only** — for awareness; do not paste to ChatGPT. Type `Proceed.` alone.
- **Carry-forward note — ready to paste** — paste this to ChatGPT alongside `Proceed.` before the next prompt fires.
- **Blocking concern** — resolve this in ChatGPT before proceeding. Do not type `Proceed.` until Claude confirms the concern is resolved.

If Claude provides no labelled observation, type `Proceed.` alone.

Submit.

After Prompt 2 output has been reviewed by Claude, type `Proceed.` in ChatGPT to proceed to Prompt 3. There is no Evidence Register stop in the Desktop model. The run proceeds directly from Prompt 2 to Prompt 3.

**16.** After Prompt 4 output has been reviewed by Claude, type `Proceed.` in ChatGPT to run Prompt 5 Stage 1. ChatGPT will produce the complete Denial Architecture Judgement output and stop before the Run Record.

**17.** Use **Copy response** from ChatGPT to copy the complete Prompt 5 Stage 1 output and paste it to the Claude companion session. Before pasting, confirm that the DAI Claude Review file (`DAI_Claude_Review_v0_4_1.md`) has already been uploaded to this session — Claude will have confirmed its receipt at Step 11. If it has not been uploaded, upload it now before submitting the Prompt 5 Stage 1 output. Claude will review the judgement against the Canon. If Claude identifies concerns, resolve them in ChatGPT before proceeding. If Claude confirms the judgement is ready, return to ChatGPT and type `Execute Run Record.`

**18.** When ChatGPT produces the Run Record code block, use **Copy** from the top right of the code block and paste it to the Claude companion session. Claude will ask for your local time, format the Run Record, and produce both files:

- `DAI_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DAI_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

**19.** Save both files.

---

### DAI → DDA boundary

**20.** Upload `DDA_Claude_BoundaryCheck_v0_4_2.md` to the Claude companion session. Claude will check the DAI Run Record, confirm the Readiness for Drift Analysis gate, state the Denial Architecture Status and its DDA starting posture.

Submit.

### Validity notice at the DAI → DDA boundary

If a working declaration was used in the DAI run, the validity notice will be present in the DAI Run Record. The DDA Claude Boundary Check will reproduce it and ask for your confirmation before the DDA session opens. The notice must be attached to all DDA findings and reproduced in the DDA Run Record. It must not be dropped at the DAI → DDA boundary.

---

### DDA module

**21.** Open a fresh ChatGPT session. Pin model to GPT-5.4 Thinking Extended manually — do not use auto mode.

**22.** Drag and drop into ChatGPT in this order:

- `Scarcity_Denial_Canon.md`
- `DDA_Prompts_v1_6.md`
- The DAI Run Record (`DAI_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`)

Submit.

**23.** Copy the opening instruction block from `DDA_ChatGPT_RunSetup_v0.1.txt` and paste it into ChatGPT. Type `Proceed.` to begin Prompt 1.

Submit.

Prompt 1 produces three outputs: the DDA Input Receipt Table (Section A), the Drift Boundary Lock Statement (Section B), and the Finding Stability Frame (Section C). The Finding Stability Frame records the principal unresolved dimension carried from DAI, the primary rival interpretation to test, and the opening trajectory posture. It does not constitute a drift judgement. It will be reviewed and confirmed or revised at Prompt 5 Stage 1 Section F.

**24.** After each prompt output, use **Copy response** from ChatGPT and paste it to the Claude companion session. Read Claude's commentary carefully. Claude will label every observation as one of three types:

- **Note only** — for awareness; do not paste to ChatGPT. Type `Proceed.` alone.
- **Carry-forward note — ready to paste** — paste this to ChatGPT alongside `Proceed.` before the next prompt fires.
- **Blocking concern** — resolve this in ChatGPT before proceeding. Do not type `Proceed.` until Claude confirms the concern is resolved.

If Claude provides no labelled observation, type `Proceed.` alone.

Submit.

**25.** After Prompt 4 output has been reviewed by Claude, type `Proceed.` in ChatGPT to run Prompt 5 Stage 1. ChatGPT will produce the complete Drift Detection Judgement output — Sections A through F — and stop before the Run Record.

The Prompt 5 Stage 1 section map is:

| Section | Content |
|---------|---------|
| A | Drift Detection Judgement |
| B | Drift Trajectory Assessment |
| C | Strongest Counter-Interpretation |
| D | Minimum Intervention Logic |
| E | Empirical Tests for Next Stage |
| F | Finding Stability Review |

**26.** Use **Copy response** from ChatGPT to copy the complete Prompt 5 Stage 1 output — Sections A through F — and paste it to the Claude companion session. Before submitting, confirm that the DDA Claude Review file (`DDA_Claude_Review_v0_4_5.md`) has already been uploaded to this session. If it has not been uploaded, upload it now before submitting the Prompt 5 Stage 1 output.

Submit.

Claude will review the judgement against the Canon. If Claude identifies concerns, resolve them in ChatGPT before proceeding. If Claude confirms the judgement is ready, return to ChatGPT and type `Execute Run Record.`

The DDA Run Record contains 16 sections. If the Run Record is too large for a single code block, ChatGPT will split it:
- First block: Run Metadata through Drift Signal Summary
- Second block: Boundary Displacement Test Table through Finding Stability Review

Use **Copy** from the top right of each code block. If two blocks are produced, paste them to the Claude companion session in order.

**27.** When ChatGPT produces the Run Record code block(s), paste to the Claude companion session. Claude will ask for your local time, format the Run Record, and produce both files:

- `DDA_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DDA_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

The DDA Commentary Summary will include a **Rerun Assessment** section if a further Desktop run or Evidence model escalation is analytically warranted. If present, this section states whether a second Desktop run is recommended, provides a suggested revised SDS scoped for session feasibility, identifies which residual uncertainty the next run is designed to resolve, and advises whether remaining session resource is sufficient to proceed. Read this section before closing the session.

**28.** Save all files produced by Claude. If the Rerun Assessment recommended a further run, Claude will also produce a carry-over SDS artefact:

- `DDA_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DDA_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `SDS_Carryover_[SystemName]_[YYYY-MM-DD].md` *(if a further run was recommended)*

If a carry-over artefact was produced, upload it when opening the next Claude companion session.

---

### End of run

**29.** The six artefacts are the complete auditable output of the pipeline:

- `SRIT_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `SRIT_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DAI_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DAI_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DDA_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`
- `DDA_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

The Claude companion session may now be closed.

---

Claude produces all Run Record and Commentary Summary files. The naming convention is:

```
SRIT_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md
SRIT_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md
DAI_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md
DAI_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md
DDA_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md
DDA_Commentary_[SystemName]_[YYYY-MM-DD]_[HHmm].md
```

Time is local time at point of file creation. Claude will ask for local time before producing each file.

\---

## Module Boundary Decisions

### SRIT → DAI

**Proceed if:** Confidence rating is 6 or above and the Run Record contains all nine sections.

**Do not proceed if:** Confidence rating is 5 or below. Gather the Stage 1 Test Questions empirical evidence and rerun SRIT.

**Proceed with caution if:** A tightly coupled co-binding condition is present — confidence 7 or below, two candidates explicitly described as co-binding in the residual uncertainty section. Claude will flag this at the boundary check. Ensure it is carried into the DAI run.

### DAI → DDA

**Proceed if:** Readiness for Drift Analysis shows Ready.

**Do not proceed if:** Readiness for Drift Analysis shows Not Ready. Review the Primary Evidence Weakness from DAI Prompt 3 and determine whether a second DAI run with Evidence Register data would resolve it.

**Note** the Denial Architecture Status confirmed by Claude at the boundary check — it determines the DDA starting posture.

\---

## What to Do When a Module Produces an Unexpected Result

**Boundary Viability Halt in SRIT** — boundary drawn too narrowly. Close the ChatGPT session. Return to the Claude companion session and instruct Claude to reopen the SDS from Phase 1 to redefine the boundary. Claude will revise the System Definition Statement and relock it. Begin the SRIT run again with the revised SDS.

**Scarcity re-opening triggered in DAI Prompt 1** — DAI has identified an inconsistency in the SRIT Run Record. Read the trigger reason. If genuine, return to the SRIT Run Record and correct it. If incorrect, instruct: *The scarcity is closed. Treat the declaration as fixed.*

**Not Ready at DAI Prompt 5** — do not proceed to DDA. Review DAI Prompt 3 evidence status. In the Desktop model this means the structural inference base was insufficient. Consider whether running the Evidence-informed model with a completed PRRP pre-run package would produce a stronger mapping.

**Indeterminate at DDA Prompt 5** — record the Run Record as provisional. The Empirical Tests for Next Stage identify what would resolve the indeterminacy.

**Claude review identifies a material concern** — do not instruct Stage 2 until resolved in ChatGPT. If the concern cannot be resolved within the session, note it in the Run Record as a known limitation.

\---

## Session Discipline

* The Claude companion session opens once and stays open for the full three-module run
* Upload `SDS_Claude_Construction_Desktop_v05.md` to open the session — this is the only session-opening file for the Desktop model
* Every ChatGPT execution session starts fresh — new chat, model pinned manually to GPT-5.4 Thinking Extended
* Paste every ChatGPT prompt output to Claude before instructing the next prompt
* Upload the relevant Claude instruction file at each Stage 1 and boundary point — do not skip these steps
* Do not close a ChatGPT session between Stage 1 and Stage 2 of the final prompt
* The six artefacts produced by Claude are the complete auditable record of the run

\---

*Version 0.6.0 — Desktop model only — companion to SDF_User_Manual_v0.3 · SRIT v2.2 · DAI v2.1 · DDA v1.6*

*© Philip Harry Galvin 2026. The Scarcity–Denial Canon, SRIT, DAI, and DDA instruments are licensed under Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0). Free use for non-commercial purposes with attribution. No derivative works. Commercial use or modification requires prior written approval from the author.*
