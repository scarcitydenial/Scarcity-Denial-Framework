# DAI — Claude Boundary Check

*Version 0.4.0 — uploadable instruction file — companion to DAI v2.0 (Desktop model)*

---

## Preamble

This file is an instruction document for the Claude companion session. Claude should read it in full and execute the instructions below. The user has uploaded this file at the SRIT → DAI module boundary.

This is the Desktop model boundary check. No Evidence Register is used in this model. The DAI run proceeds directly from the SRIT Run Record to denial architecture analysis without an evidence admission stage.

---

## Claude Instructions

### 1. Confirm session continuity

Confirm that this is the same Claude session used for the SRIT system description and run commentary. If this appears to be a new session with no prior context, state this clearly and ask the user to confirm before proceeding.

### 2. Receive the SRIT Run Record

Ask the user to upload or paste the SRIT Run Record produced at the close of the SRIT module. The filename will follow the convention:

`SRIT_Run_[SystemName]_[YYYY-MM-DD]_[HHmm].md`

Do not proceed until the Run Record is received.

### 3. Check input completeness

Verify the following fields are present in the SRIT Run Record:

- System Definition Statement (system, boundary, time horizon, failure condition)
- Binding Scarce Resource Declaration
- Binding level
- Strongest Alternative Rejected
- Confidence Rating
- Residual Uncertainty
- Stage 1 Test Questions

If the Binding Scarce Resource Declaration is absent, halt and inform the user — DAI cannot proceed without it.

If other fields are absent, note each gap but proceed. Flag the missing fields in your readiness output.

### 4. Check confidence rating

If the Confidence Rating is 5 or below, advise the user that the declaration is weak and that DAI analysis built on it will carry that weakness forward. Ask the user to confirm they wish to proceed before continuing.

If the Confidence Rating is 6 or above, proceed.

### 5. Check for tightly coupled co-binding condition

Review the Residual Uncertainty and Strongest Alternative Rejected sections. If both of the following are true, flag the co-binding condition:

- Confidence Rating is 7 or below
- The residual uncertainty statement explicitly describes the top two candidates as tightly coupled, co-binding, or difficult to disentangle

If flagged, note that DAI must address both candidates and that the strongest alternative rejected is not merely an alternative — it may become primary under different demand conditions.

### 6. Check for ambiguous declaration with leading candidate

If the Binding Scarce Resource Declaration is ambiguous but a leading candidate is named in the SRIT Run Record, apply the following:

1. State that DAI Prompt 1 will return a Conditional Continuation Available halt rather than a full hard stop
2. Reproduce the leading candidate name from the SRIT Run Record
3. Reproduce the current leading Protectable Resource Form verbatim from the SRIT Run Record
4. State the validity notice in full (see below) so the user sees it before the ChatGPT session opens
5. Advise the user that if they proceed, the validity notice will be attached to all DAI and downstream DDA outputs
6. Ask the user to confirm they wish to proceed on this basis before the DAI ChatGPT session opens

**Validity notice — reproduce verbatim in the boundary check output:**

> *"This DAI run proceeds on a working declaration rather than a fixed Binding Scarce Resource Declaration. The SRIT run returned an ambiguous result at Prompt 6. The leading candidate [candidate name] has been adopted as the working scarce resource for denial architecture mapping purposes. All findings in this run — and any downstream DDA findings — carry reduced confidence commensurate with the ambiguity at the scarcity identification stage. A re-run with a fixed declaration is required before findings are treated as operationally validated."*

---

### 7. Confirm context loaded

Confirm that the following files are loaded as context in this session. If any are missing, ask the user to upload them before proceeding:

- `Scarcity_Denial_Canon.md`
- `DAI_Prompts_v2_0.md`

---

## Claude Output Format

Produce a single structured response in the following format:

**DAI Boundary Check — [SystemName]**

Input completeness: [Complete / Incomplete — list missing fields]

Confidence rating: [rating] — [Proceed / Proceed with caution / Weak — confirm to proceed]

Co-binding condition: [Not present / Present — [brief description]]

Validity notice: [Not applicable — fixed declaration /
                  Present — working declaration on [candidate name] — user confirmed /
                  Present — working declaration on [candidate name] — user confirmation pending]

Context files: [Confirmed / Missing — [list missing files]]

Readiness: [Ready to proceed to DAI / Not ready — [reason]]

If Ready: state the Binding Scarce Resource Declaration verbatim from the Run Record so the user can confirm it is correct before the DAI ChatGPT session opens.

---

## User Next Step

When Claude confirms Ready:

1. Upload `DAI_Claude_Review_v0_4_0.md` to this Claude session. Claude will confirm it is loaded and ready. Do not open the ChatGPT session until Claude confirms the Review file is loaded.

2. Once Claude confirms the Review file is loaded, proceed to `DAI_ChatGPT_RunSetup_v0_1` and open a fresh ChatGPT session. Paste each prompt output into this Claude session as it is produced during the run.

Note that if the required denial actor's authority over the required decision point is uncertain or disputed, the Prompt 2 Authority Reachability Test will produce a conditional specification and generate additional authority-basis test questions at Prompt 5 Stage 1. No action is required here — this is for your awareness before the run opens.

If Claude confirms Not Ready, address the identified gaps before proceeding.

---

*Version 0.4.0 — companion to DAI v2.0 (Desktop model)*

*© Philip Harry Galvin 2026. Scarcity–Denial Canon and derived works. Licensed CC BY-NC-ND 4.0. No derivative works without prior written approval.*
