# Scarce Resource Identification Tool

## SRIT v2.2

*Desktop model — receives pre-prepared System Definition Statement from Claude at Prompt 1.*

### Purpose

Identify the binding scarce resource governing the stability of a system so that the Denial–Scarcity Framework can be applied correctly.

SRIT operates before the Denial Architecture Interrogation (DAI) module.

SRIT is designed to prevent the two biggest risks:

- premature narrative convergence
- domain bias from experts or training data

The structure forces candidate enumeration → structured testing → mechanism screening → elimination → evidence verification → final declaration → human judgement.

The tool is intended to be operational rather than descriptive.

Its core output is a **Binding Scarce Resource Declaration** suitable for downstream denial-alignment analysis.

SRIT operates under the Scarcity–Denial Canon:

- Every system is constrained by a scarce resource.
- Denial is the mechanism by which that constraint is enforced.
- System stability depends on denial being applied at a decision point consistent with the scarcity of that resource.
- Drift occurs when the denial boundary migrates downstream of the decision point required to protect that scarcity.

---

### Architecture Overview

The tool runs through six structured AI interactions.

Each interaction uses a specific prompt structure and produces a defined output.

The AI is used as an interrogation engine, not as the originator of the framework.

The intellectual structure resides in the prompt sequence and output discipline.

#### Execution Rule

- Each prompt must operate strictly on the outputs produced by the previous prompt.
- The AI must not regenerate, summarise, or replace earlier artefacts unless explicitly instructed.
- All structured tables produced in earlier prompts must remain part of the working analysis.
- The resource/mechanism distinction must be resolved inside SRIT before Prompt 6. A candidate that cannot demonstrate resource character must not survive to final declaration merely because it is important, upstream, or governance-related.

### Workflow

1. System Declaration
2. Candidate Scarcity Generation
3. Scarcity Pyramid Interrogation
4. Boundary Audit, Mechanism Gate, and Elimination Matrix
5. Evidence Verification
6. Binding Scarcity Declaration

Human judgement is required only at the final stage.

---

## SRIT Execution Mode

If the protocol text is recognised, treat it as an **execution specification rather than a document to be interpreted or improved**.

The Prompts constitute the operational sequence of the Scarce Resource Identification Tool (SRIT).

When executing these prompts:

- Do **not** analyse or critique the protocol
- Do **not** propose improvements or alternative structures
- Do **not** summarise or restate the framework

Your role is strictly to **execute the prompts sequentially as an analytical interrogation engine**.

Each prompt must operate **only on the outputs generated in the previous stage**.

#### Sequential Execution

SRIT executes one prompt at a time. After each prompt is complete, stop and wait for the command: **Proceed** before moving to the next prompt. The Claude companion session reviews each output before the next prompt fires — do not proceed without that instruction.

#### Mode Selection

**Sequential review mode** — The only valid execution mode for Desktop model runs. The AI stops after each prompt and waits for the command **Proceed** before moving to the next prompt. This is required because the Claude companion session reviews every prompt output before the next prompt fires — continuous execution would bypass that review entirely.

The AI always operates in sequential review mode. No mode selection is required.

#### Boundary Audit Note

The Boundary Audit in Prompt 4 applies three tests to every candidate. On rare occasions a candidate may be difficult to classify definitively as in scope, out of scope, or adjacent system signal. If genuine ambiguity exists, assign the candidate the most conservative boundary status — out of scope — and log the ambiguity reason in the Boundary Audit Table. Do not allow boundary ambiguity to stall execution. Proceed with the in-scope candidates that are clearly compliant.

The prompts that follow initiate the structured interrogation used to identify the binding scarce resource governing system stability.

Execution will begin with **Prompt 1 — System Declaration**.

---

## Prompt 1 — System Declaration

**User input required:** Paste the confirmed System Definition Statement produced by the SDS_Claude_Construction procedure in the Claude companion session. The SDS must be confirmed and locked in Claude before this session opens.

### Purpose

Define the analytical boundary.

Without correct boundaries scarcity identification becomes impossible.

The objective of SRIT is to identify the binding scarce resource that governs system stability, not merely resources that are important or valuable.

### User Prompt

Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

You are assisting with the Scarce Resource Identification Tool (SRIT).

A confirmed System Definition Statement has been produced by the Claude companion session and will be provided in the next message. Your role at Prompt 1 is to receive and confirm it — not to reconstruct it, interrogate the analyst, or ask the four boundary questions. Do not request the SDS or ask any questions before it arrives — state that you are ready to receive the SDS and wait.

Confirm receipt by stating the four fields back to the analyst. Then confirm internal consistency using the following three checks:

1. The boundary inclusions support the failure condition — the mechanisms that could produce failure are within the boundary
2. The time horizon is appropriate for the system and failure condition described
3. The system identity and boundary describe the same system — the inclusions and exclusions correspond to the system named

If all three checks pass: state *System Definition Statement confirmed.* Stop and wait for the explicit instruction: **Proceed**.

If any check fails: state the specific inconsistency and instruct the analyst to return to the Claude companion session to resolve it. Do not proceed to Prompt 2 until the SDS is internally consistent.

Do not ask the four boundary questions. Do not propose amendments to the SDS. Do not offer alternative boundary framings. The SDS has been constructed and validated by Claude. Your role is confirmation only.

### Expected AI Behaviour

- On receipt of this file, state readiness to receive the System Definition Statement. Do not request the SDS — simply state that you are ready and wait for it to be provided. Do not produce any output beyond the readiness statement until the SDS arrives.
- Receive the pre-prepared System Definition Statement and confirm its four fields back to the analyst
- Apply the three internal consistency checks
- If checks pass: confirm and stop. Wait for the explicit instruction: **Proceed**.
- If any check fails: state the specific inconsistency and instruct the analyst to return to Claude for resolution
- Do not ask the four boundary questions
- Do not propose candidate scarcities
- Do not begin analysis of scarcity
- Do not interpret system behaviour

### Output

A structured **System Definition Statement**.

Example format:

> **System:** Global container shipping network
>
> **Boundary:** Shipping lines, port infrastructure, logistics networks
>
> **Time Horizon:** 12–24 months
>
> **Failure Condition:** Inability to maintain continuous flow of goods

---

## Prompt 2 — Candidate Scarcity Generation

### Purpose

Generate a wide candidate list.

The objective is breadth, not accuracy.

The candidate field should be deliberately broader than first intuition.

### User Prompt

Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

Before generating candidate scarcities, construct at least two alternative system definitions with different boundaries or time horizons.

Using the system definitions above, generate a list of possible scarce resources that could govern the stability of this system.

Rules:

1. Produce between 12 and 20 candidates.
2. Include physical, economic, organisational, informational, behavioural, temporal, institutional, relational, environmental, and composite resources where relevant.
3. Do not select or rank any candidate yet.
4. Where useful, identify the scarcity class of each candidate.

This stage is only for generating possible candidates.

When this Prompt 2 has successfully completed, stop and wait for the explicit instruction: **Proceed**.

### Output Example

**Candidate Scarce Resources**

1. Financial capital — Economic — May constrain continuity of operations and investment capacity
2. Skilled labour — Organisational — May constrain execution and replenishment capability
3. Operational capacity — Composite — May be a headline scarcity requiring later decomposition
4. Trust between actors — Behavioural / Relational — May constrain coordination and participation
5. Energy supply — Physical — May constrain throughput directly
6. Logistics throughput — Physical / Organisational — May determine whether the system can continue operating under load
7. Information quality — Informational — May constrain control and decision accuracy
8. Regulatory permission — Institutional — May constrain whether activity can legally continue
9. Political tolerance — Behavioural / Institutional — May constrain whether the system retains room to operate
10. Infrastructure resilience — Composite — May constrain capacity under disruption
11. Communication bandwidth — Informational / Physical — May constrain coordination
12. Attention of decision makers — Behavioural / Organisational — May constrain prioritisation and intervention

The preferred output format is:

| Candidate | Scarcity Class | Production Requirement | Failure Pathway |
|-----------|---------------|----------------------|-----------------|

---

## Prompt 3 — Scarcity Pyramid Interrogation

### Purpose

Test each candidate against structural scarcity criteria.

This stage is evaluative, not eliminative.

### User Prompt

Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

Evaluate each candidate scarce resource using the Scarcity Pyramid interrogation tests.

For each candidate assess:

1. **Reproduction Requirement** — Does the system depend on continual reproduction, preservation, renewal, or replenishment of this resource?
2. **Failure Causality** — If this resource is depleted or misallocated, does the system destabilise directly?
3. **Substitution Resistance** — Can other resources substitute for this resource for long periods?
4. **System Level** — At what level does the resource operate? (asset, task, team, function, firm, market, state, ecosystem)

Provide a short evaluation for each candidate.

Do not eliminate candidates yet.

When this Prompt 3 has successfully completed, stop and wait for the explicit instruction: **Proceed**.

### Output

A candidate evaluation table.

Example:

| Resource | Reproduction | Failure Impact | Substitution | Level |
|----------|-------------|----------------|--------------|-------|

The preferred artefact is a **Scarcity Evaluation Matrix**.

---

## Prompt 4 — Boundary Audit, Mechanism Gate, and Elimination Matrix

### Purpose

Reduce the long list of plausible candidates to the few that still survive structural testing.

This is where the tool stops being exploratory and starts becoming selective.

This prompt must also prevent mechanism candidates from surviving as resource finalists merely because they are important, upstream, coordinating, supervisory, allocative, or governance-related.

### User Prompt

Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

**Before elimination begins, perform a Boundary Audit.**

Return to the System Definition Statement produced in Prompt 1.

For each candidate in the evaluation table, apply the following three boundary tests:

- Does this candidate reside within the system boundary as defined in Prompt 1?
- Does this candidate operate at a layer explicitly excluded from that boundary?
- Is this candidate a resource of an adjacent system that feeds into, but is not part of, the defined system?

Assign each candidate one of three boundary statuses:

- **In scope** — the candidate operates within the defined system boundary and proceeds to the next test
- **Out of scope** — the candidate operates outside the boundary and is removed from the elimination process; provide a single boundary reason statement
- **Adjacent system signal** — the candidate is out of scope but its presence suggests it may be the binding scarcity in a system that feeds this one; log it as a candidate for a separate SRIT run and remove it from this elimination process

A candidate that is out of scope must not be retained regardless of how strongly it scores on the Scarcity Pyramid tests. Analytical strength does not override boundary compliance.

Record all candidates in a **Boundary Audit Table**:

| Candidate | Boundary Status | Reason |
|-----------|----------------|--------|
| [Name] | In scope / Out of scope / Adjacent system signal | [one line reason] |

---

**Shortlist Viability Check**

After completing the Boundary Audit Table, apply the following viability test before proceeding:

Count the number of in-scope candidates that scored meaningfully on at least two of the four Scarcity Pyramid tests in Prompt 3.

**If 3 or more viable in-scope candidates exist:** proceed to the Mechanism Gate below.

**If fewer than 3 viable in-scope candidates exist:** do not proceed to the Mechanism Gate or elimination matrix. The run cannot produce a defensible declaration from the current in-scope candidate field.

Halt the run and return the following halt statement:

> **Boundary Viability Halt**
>
> The in-scope candidate field contains fewer than 3 candidates with sufficient Scarcity Pyramid scores to support a defensible declaration.
>
> Probable cause: [select one]
> - The system boundary is drawn too narrowly — the binding scarcity likely resides in an adjacent layer
> - The system boundary is misaligned with the failure condition defined in Prompt 1
> - The system boundary excludes the operational layer where scarcity actually bites
>
> Required action: Return to Prompt 1 and redefine the system boundary before restarting the run.
>
> Adjacent system signals identified in this run that may warrant a separate SRIT analysis:
> - [candidate] — [reason it may be binding in adjacent system]

---

**Mechanism Gate**

The Scarcity–Denial Canon requires a binary distinction between scarce resource and mechanism.

A scarce resource is depleted, withheld, misallocated, or failed in the production of service.

A mechanism operates by governing whether some other resource is protected, released, directed, allocated, or mobilised.

Apply the Mechanism Gate to every **in-scope viable candidate**.

### Step 1 — Mechanism Flag Test

Ask:

> If this candidate were fully adequate — present, available, and functioning — while one or more other viable candidates were absent or depleted, would the defined failure condition still occur?

Apply the following routing rule:

- **If no:** the candidate proceeds directly to the elimination matrix as a **resource candidate**. Step 2 is not applied.
- **If yes:** the candidate is flagged for possible mechanism character and **must** proceed to Step 2. Step 2 cannot be waived for a flagged candidate.

### Step 2 — Standalone Failure Test

For every candidate flagged in Step 1, ask:

> Can insufficiency, depletion, withholding, or misallocation of this candidate alone — while the other viable shortlisted resources are treated as notionally adequate and available — produce the defined failure condition through direct failure of service production?

State the pathway explicitly.

Do **not** count as a direct standalone pathway any explanation that relies mainly on another shortlisted resource being:

- leaked
- delayed
- withheld
- misallocated
- left unmobilised
- left unprotected
- not directed to the failure point

Apply the following rule:

- **If yes:** classify the candidate as **Resource candidate** and allow it to proceed to the elimination matrix.
- **If no:** proceed to Step 3.

### Step 3 — Reframe Test

For every candidate failing Step 2, ask:

> Does this candidate’s failure pathway operate mainly by causing another shortlisted resource to be leaked, delayed, withheld, misallocated, left unmobilised, or left unprotected?

Apply the following rule:

- **If yes:** classify the candidate as **Mechanism — eliminate** and record the resource candidate it most plausibly governs.
- **If the answer remains contested after initial testing:** place the candidate **under adversarial challenge within Prompt 4 only**.

### Adversarial Challenge Rule

Adversarial challenge is a temporary Prompt 4 process state, not a stable category.

If a candidate is placed under adversarial challenge, the AI must attempt to prove direct standalone resource character using:

- the Prompt 1 system boundary and failure condition
- the Prompt 3 Scarcity Evaluation Matrix
- any decomposition already completed inside Prompt 4

The challenge must close **within Prompt 4**.

Apply the following closure rule:

- **If direct standalone resource character is demonstrated:** classify the candidate as **Resource candidate** and allow it to proceed to the elimination matrix.
- **If direct standalone resource character is not demonstrated by the end of Prompt 4:** classify the candidate as **Mechanism — eliminate** under **R6**.

Do not carry unresolved adversarial challenge into Prompt 5.

Record all in-scope viable candidates in a **Mechanism Gate Table**:

| Candidate | Step 1 Result | Standalone Failure Pathway | Governed Resource (if applicable) | Gate Result |
|-----------|---------------|----------------------------|-----------------------------------|-------------|
| [Name] | Triggered / Not triggered | [one line pathway or reason] | [resource or blank] | Resource candidate / Mechanism — eliminate |

For every candidate actually placed under adversarial challenge after Step 3 remains contested, produce an **Adversarial Challenge Record** immediately below that candidate's row in the Mechanism Gate section.

The Adversarial Challenge Record is **not** required for every candidate where Step 1 is triggered.

Use this format:

> **Adversarial Challenge Record — [Candidate Name]**
> - **Challenge argument:** [State the strongest case that this candidate is a scarce resource rather than a mechanism.]
> - **Counter-argument:** [State why that case fails or survives under the Canon's second sentence. Explicitly identify what governs what, and whether the candidate's failure pathway runs through direct depletion or failure of service production, or through mobilisation, protection, allocation, release, direction, or governance of another resource.]
> - **Disposition:** [Retained as resource candidate / Eliminated under R6] — [one sentence stating what element of the reasoning was decisive]

No Adversarial Challenge Record is required for:

- candidates eliminated under R1–R5 without entering adversarial challenge
- candidates that pass the Gate without triggering Step 1
- candidates that trigger Step 1 but resolve at Step 2 or Step 3 without adversarial challenge

Any candidate classified as **Mechanism — eliminate** must also be logged as a **candidate mechanism-layer item for DAI**.

---

Only candidates confirmed as **Resource candidate** by the Mechanism Gate proceed to the elimination matrix below.

Using the evaluation table above, eliminate candidates that fail the Scarcity Pyramid tests.

Eliminate candidates where:

- failure impact is indirect rather than primary
- substitution is easy or durable
- continual reproduction is not necessary for system stability
- the resource operates only as a local bottleneck rather than a system-level constraint

For each candidate assign one of the following status labels where useful:

- retain
- reclassify
- decompose
- merge
- reject

Do **not** use adversarial challenge as a final status label. It is a temporary Prompt 4 process state only.

If a surviving candidate represents a composite or umbrella concept (e.g., capacity, resilience, capability, confidence, liquidity, throughput), you must decompose it into its underlying component resources.

Re-run the Scarcity Pyramid evaluation on the decomposed components before allowing the composite term to remain on the shortlist.

Reduce the list to the 3–5 strongest candidates.

For each eliminated candidate, provide a criteria-based elimination statement from one of the following Elimination Reason Codes:

- **R1:** No reproduction requirement
- **R2:** Indirect failure pathway
- **R3:** Durable substitution available
- **R4:** Local bottleneck only
- **R5:** Composite abstraction
- **R6:** Mechanism — candidate operates primarily by allowing another resource to leak, be delayed, withheld, misdirected, left unmobilised, or left unprotected; no direct standalone service-production failure pathway through this candidate alone has been demonstrated within the defined boundary

For each surviving candidate, explain exactly why it remains viable.

Do not yet declare a final scarce resource.

When this Prompt 4 has successfully completed, stop and wait for the explicit instruction: **Proceed**.

### Full Output Structure

The AI should produce five sections.

#### Section A — Boundary Audit Table

Format:

> **Boundary Audit**
>
> | Candidate | Boundary Status | Reason |
> |-----------|----------------|--------|
> | [Name] | In scope / Out of scope / Adjacent system signal | [one line reason] |
>
> **Shortlist Viability Check**
> In-scope candidates with 2+ Scarcity Pyramid scores: [count]
> Result: [Proceed / Halt]
>
> Adjacent system signals for separate SRIT consideration:
> - [candidate] — [reason]

#### Section B — Mechanism Gate Table and Adversarial Challenge Records

Format:

> **Mechanism Gate**
>
> | Candidate | Step 1 Result | Standalone Failure Pathway | Governed Resource (if applicable) | Gate Result |
> |-----------|---------------|----------------------------|-----------------------------------|-------------|
> | [Name] | Triggered / Not triggered | [one line pathway or reason] | [resource or blank] | Resource candidate / Mechanism — eliminate |
>
> **Adversarial Challenge Record — [Candidate Name]**
> - **Challenge argument:** ...
> - **Counter-argument:** ...
> - **Disposition:** ...
>
> **Candidate Mechanism-Layer Items for DAI**
> - [candidate] — governs [resource] — [one line reason]
> - [candidate] — governs [resource] — [one line reason]

Where no candidate enters adversarial challenge, omit individual challenge records and proceed directly to Candidate Mechanism-Layer Items for DAI.

#### Section C — Eliminated Candidates

Format:

> **Eliminated Candidates**
>
> 1. [Candidate Name]
>
>    Reason for elimination:
>    - [specific reason]
>    - [specific reason]
>    - [specific reason]
>
>    Elimination Reason Code: [R1 / R2 / R3 / R4 / R5 / R6]
>    Status: [reject / reclassify / decompose / merge / mechanism — eliminate]

Example:

> **Eliminated Candidates**
>
> 1. Financial capital
>
>    Reason for elimination:
>    - Important to the system, but not always the first point of destabilisation
>    - Can often be substituted temporarily through borrowing, guarantees, or state support
>    - Appears more as an enabling resource than the most binding operating constraint in this case
>
>    Elimination Reason Code: R2 / R3
>    Status: reject
>
> 2. Information quality
>
>    Reason for elimination:
>    - Relevant to performance, but not necessarily the core system stability constraint
>    - System can continue operating with degraded information for meaningful periods
>
>    Elimination Reason Code: R2
>    Status: reject
>
> 3. Accountability enforcement
>
>    Reason for elimination:
>    - Influences whether maintenance cash is protected and released rather than being the resource consumed in restoration
>    - No direct standalone service-production failure pathway was demonstrated once operational resources were treated as adequate and available
>    - Functions primarily by governing another resource
>
>    Elimination Reason Code: R6
>    Status: mechanism — eliminate

#### Section D — Surviving Candidates

Format:

> **Surviving Candidates**
>
> 1. [Candidate Name]
>
>    Reason it survives:
>    - [specific reason]
>    - [specific reason]
>    - [specific reason]
>
>    Status: [retain / decompose]

Example:

> **Surviving Candidates**
>
> 1. Skilled labour
>
>    Reason it survives:
>    - Requires continual reproduction and replenishment
>    - Failure directly impairs system continuity
>    - Cannot be substituted quickly without structural degradation
>
>    Status: retain
>
> 2. Logistics throughput
>
>    Reason it survives:
>    - Directly determines whether the system can keep functioning under load
>    - Substitution is limited and usually shifts the bottleneck elsewhere
>
>    Status: retain

#### Section E — Provisional Shortlist Summary

Format:

> **Provisional Shortlist Summary**
>
> The strongest remaining scarce resources are:
>
> 1. [Candidate]
> 2. [Candidate]
> 3. [Candidate]
>
> Why these remain:
> - [summary reason]
> - [summary reason]
> - [summary reason]
>
> Outstanding ambiguity:
> - [what remains unresolved]

Example:

> **Provisional Shortlist Summary**
>
> The strongest remaining scarce resources are:
>
> 1. Skilled labour
> 2. Logistics throughput
> 3. Energy supply continuity
>
> Why these remain:
> - Each appears necessary for ongoing system reproduction
> - Each has a direct relationship to primary failure
> - Each is difficult to substitute for long
>
> Outstanding ambiguity:
> - The unresolved issue is whether the system fails first because trained personnel become insufficient, because throughput collapses, or because energy continuity breaks down.

---

## Prompt 5 — Evidence Verification

### Purpose

Force the AI to stop relying on plausible narrative and instead test each surviving candidate against observable system behaviour.

This prompt must also act as a late anti-drift backstop. If the evidence review shows that a surviving candidate operates mainly as a mechanism governing some other resource, that candidate must be returned to the Prompt 4 Mechanism Gate before ranking proceeds.

### User Prompt

Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

Take the surviving candidates only and test each one using three forms of evidence:

1. **Behavioural Evidence** — What actual behaviours would we expect if this were the binding scarcity?
2. **Structural Evidence** — What formal rules, queues, reserve structures, permissions, bottlenecks, or institutional arrangements would exist if this were the binding scarcity?
3. **Stress Evidence** — What would happen during crisis, overload, or disruption if this were the binding scarcity?

For each surviving candidate, provide:

- evidence that supports it
- evidence that weakens it
- what additional evidence would most help discriminate between the remaining candidates

Do not yet make a final selection unless one candidate is overwhelmingly superior.

### Mandatory Late-Catch Retest

The late-catch mechanism retest is a mandatory check applied to every candidate on the provisional shortlist at Prompt 5, regardless of whether weakening evidence raises an explicit mechanism-character concern.

For each candidate, apply the following two-step check:

**Step 1 — Review weakening evidence for mechanism character:**

Read the weakening evidence section for the candidate. Assess whether the failure pathway described in the weakening evidence runs mainly through whether another resource is correctly mobilised, governed, or protected — rather than through direct depletion or insufficiency of the candidate resource itself.

- **If yes:** mechanism character is present. Proceed to Step 2.
- **If no:** mechanism character is not present. Record an abbreviated log entry (see log format below) and move to the next candidate.

**Step 2 — Full mechanism retest:**

Apply the Mechanism Gate Step 2 test from Prompt 4. Determine whether the candidate has a direct standalone service-production failure pathway that does not run through governance or mobilisation of another resource.

- **If the candidate demonstrates direct standalone resource character:** record as **Resource candidate — remains on ranking**.
- **If the candidate collapses into mechanism character under the Step 2 test:** record as **Mechanism — eliminate under R6**. Remove from ranking and add to the Candidate Mechanism-Layer Items for DAI list with the governed resource identified.

If a candidate is removed by the late-catch retest, the comparative ranking must be recomputed before Prompt 5 closes.

Do not allow a mechanism-like candidate to remain in the ranking merely because its evidence review was framed diplomatically or because it appears important.

**Abbreviated log entry — no mechanism character identified**

Use this format for candidates where Step 1 found no mechanism character in the weakening evidence:

- **Candidate:** [name]
- **Late-catch check:** Applied — no mechanism character identified in weakening evidence
- **Result:** Remains on ranking
- **Ranking recomputed:** Not applicable

**Full log entry — mechanism character identified at Step 1, Step 2 retest conducted**

Use this format for candidates where Step 1 identified mechanism character and a full Step 2 retest was conducted:

- **Candidate:** [name]
- **Late-catch trigger:** [one line description of the weakening evidence that raised the mechanism-character concern]
- **Step 2 retest result:** [Resource candidate — remains on ranking / Mechanism — eliminate under R6]
- **Ranking recomputed:** [Yes / No / Not applicable]

When this Prompt 5 has successfully completed, stop and wait for the explicit instruction: **Proceed**.

### Full Output Structure

#### Section A — Candidate-by-Candidate Evidence Review

Format:

> Candidate: [Name]
>
> Behavioural evidence supporting:
> - ...
>
> Behavioural evidence weakening:
> - ...
>
> Structural evidence supporting:
> - ...
>
> Structural evidence weakening:
> - ...
>
> Stress evidence supporting:
> - ...
>
> Stress evidence weakening:
> - ...
>
> Mechanism late-catch check on weakening evidence:
> - Result: [Pass / Return to Mechanism Gate Step 2]
> - Outcome: [remains on ranking / removed as mechanism — eliminate under R6]
>
> Best discriminating evidence still needed:
> - ...

#### Section B — Comparative Evidence Summary

Format:

> **Comparative Evidence Summary**
>
> Candidate 1:
> - strongest support:
> - main weakness:
>
> Candidate 2:
> - strongest support:
> - main weakness:
>
> Candidate 3:
> - strongest support:
> - main weakness:

#### Section C — Evidence-Based Ranking

Format:

> **Evidence-Based Ranking**
>
> Most strongly supported candidate:
> 1. [Candidate]
>
> Next strongest:
> 2. [Candidate]
>
> Next strongest:
> 3. [Candidate]
>
> Reason for current ranking:
> - ...
> - ...
> - ...
>
> Ranking recomputation note (only if applicable):
> - [candidate] was removed by the Prompt 5 late-catch retest and the ranking was recalculated

This is still provisional unless the lead candidate is clearly dominant.

The preferred artefact is an **Evidence Verification Review**.

---

## Prompt 6 — Binding Scarcity Declaration

### Purpose

Force final closure in a precise format that identifies Scarcity.

### User Prompt

Do not skip stages.

Do not summarise prior analysis.

Maintain all structured artefacts from earlier prompts.

Each stage must operate strictly on the outputs of the previous stage.

Using all prior analysis, determine whether one candidate now clearly stands above the others as the binding scarce resource.

If yes, produce the final Binding Scarcity Declaration in this exact format:

> In [system], at the [level] level, over a [time horizon] horizon, the binding scarce resource is [resource], because depletion, misallocation, or failed protection of this resource causes primary system instability and cannot be durably substituted.

Immediately after the Binding Scarcity Declaration, provide a required **Protectable Resource Form** statement.

The Protectable Resource Form must specify the resource in the operational form that must actually remain available for system stability.

It must state, where relevant:

1. what must be preserved
2. the operational state in which it must exist
3. the level or layer at which it must remain usable
4. the conditions under which nominal presence would still be inadequate
5. why apparent substitutes would fail under the declared failure condition

Then provide:

1. Why this resource was selected over the remaining alternatives
2. The strongest alternative candidate and why it was rejected
3. A confidence rating out of 10
4. Any residual uncertainty that should be tested in DAI

If the Protectable Resource Form cannot be specified with operational precision:

- reduce the confidence rating by at least one point from the score otherwise supportable
- explicitly state in residual uncertainty that the declaration remains imprecise at the protectable-form level
- identify the evidence required to resolve that gap

If no candidate clearly dominates, state that the result is still ambiguous and identify exactly what further evidence is needed.

If the declared scarce resource were incorrect, what alternative scarcity would most likely explain the system?

Selection rationale must reference the system boundary and failure condition defined in Prompt 1.

When this Prompt 6 has successfully completed, stop. Inform the user that the SRIT analytical output is now complete. Do not produce the Run Record yet. Wait for the explicit instruction: **Execute Run Record**.

### Full Output Structure

#### Section A — Binding Scarcity Declaration

Format:

> **Binding Scarcity Declaration**
>
> In [system], at the [level] level, over a [time horizon] horizon, the binding scarce resource is [resource], because depletion, misallocation, or failed protection of this resource causes primary system instability and cannot be durably substituted.

#### Section B — Protectable Resource Form

Format:

> **Protectable Resource Form**
>
> [Operationally specific form of the declared scarce resource that must actually be preserved]

#### Section C — Selection Rationale

Format:

> Why this resource was selected:
> - ...
> - ...
> - ...

#### Section D — Strongest Alternative Rejected

Format:

> Strongest alternative candidate: [Candidate]
>
> Why it was rejected:
> - ...
> - ...
> - ...

#### Section E — Confidence and Residual Uncertainty

Format:

> Confidence rating: [score]/10
>
> Residual uncertainty:
> - ...
> - ...
>
> DAI Entry Test Questions:
> - ...
> - ...

The final artefact is a **Binding Scarce Resource Declaration** suitable for downstream denial analysis.

When Prompt 6 Stage 1 has successfully completed, stop. Do not produce the Run Record yet. Wait for the explicit instruction: **Execute Run Record**.

---

### Run Conclusion and SRIT Run Record

This section executes only when the user instructs: **Execute Run Record**.

Do not say "let me produce the Run Record", "I will now generate", or any similar preamble. Output the conclusion statement and Run Record directly in response to that instruction. Deliver the Run Record inside a fenced code block using triple backticks. Do not render the Run Record as formatted markdown.

**Conclusion statement:**

> This SRIT analysis is now complete. The Binding Scarce Resource Declaration is ready for downstream denial-alignment analysis. Save the SRIT Run Record below as:
>
> `SRIT_Run_[SystemName]_[YYYY-MM-DD_HHMM].md`
>
> where [SystemName] is the system name from the System Definition Statement and [YYYY-MM-DD_HHMM] is the date and time of this run.

**SRIT Run Record — output immediately below the conclusion statement:**

```text id="9fweo1"
# SRIT Run Record

## Run Metadata
- **System:** [system name]
- **Run Date/Time:** [YYYY-MM-DD HH:MM]
- **AI Model:** [model name and version]
- **Thinking Mode:** [enabled / disabled / not applicable]
- **SRIT Version:** 2.2
- **Scarcity Type (optional):** [flow resource / stock resource / capacity resource / capability resource / composite — or leave blank if type cannot be determined]

---

## System Definition Statement
[Reproduce the full System Definition Statement from Prompt 1]

---

## Boundary Audit Table
[Reproduce the full Boundary Audit Table from Prompt 4 including all three status columns]

---

## Mechanism Gate Table
[Reproduce the full Mechanism Gate Table from Prompt 4 including Step 1 Result, Standalone Failure Pathway, Governed Resource, and Gate Result]

---

## Adversarial Challenge Record(s)
[Reproduce each Adversarial Challenge Record from Prompt 4 exactly as issued. If none, state None.]

---

## Candidate Mechanism-Layer Items for DAI
[List each candidate classified Mechanism — eliminate under R6, identify the governed resource if known, and state in one line why it was classified as mechanism-like; if none, state None. If a candidate was removed by the Prompt 5 late-catch retest, include it here with the notation: Identified at Prompt 5 late-catch retest.]

---

## Adjacent System Signals
[List each candidate assigned Adjacent system signal status from the Boundary Audit Table, with the reason recorded and a note that each may warrant a separate SRIT run; if none, state None]

---

## Provisional Shortlist
[Reproduce the full Provisional Shortlist Summary from Prompt 4 Section E including the outstanding ambiguity statement]

---

## Prompt 5 Late-Catch Retest Log
[The late-catch retest is applied to all surviving candidates. For each candidate, record either an abbreviated entry (no mechanism character identified) or a full entry (mechanism character identified and Step 2 retest conducted), using the two-tier format specified in Prompt 5.

Abbreviated entry format:

- **Candidate:** [name]
- **Late-catch check:** Applied — no mechanism character identified in weakening evidence
- **Result:** Remains on ranking
- **Ranking recomputed:** Not applicable

Full entry format:

- **Candidate:** [name]
- **Late-catch trigger:** [one line description]
- **Step 2 retest result:** [Resource candidate — remains on ranking / Mechanism — eliminate under R6]
- **Ranking recomputed:** [Yes / No / Not applicable]]

---

## Binding Scarce Resource Declaration
[Reproduce the exact declaration statement from Prompt 6 Section A]

**Protectable Resource Form**
[Reproduce Prompt 6 Section B in full]

**Selection Rationale**
[Reproduce the full Section C selection rationale bullet points from Prompt 6]

---

## Strongest Alternative Rejected
[Reproduce the strongest alternative candidate and the full rejection rationale from Prompt 6 Section D]

---

## Confidence Rating and Residual Uncertainty
[Reproduce Section E from Prompt 6 in full including the alternative scarcity statement]

---

## DAI Entry Test Questions
[Reproduce the DAI Entry Test Questions from Prompt 6 Section E]

---
```
