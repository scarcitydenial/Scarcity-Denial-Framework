# SRIT Run Record

## Run Metadata
- **System:** West Africa regional electricity grid
- **Run Date/Time:** 2026-03-31 10:22
- **AI Model:** GPT-5.4 Thinking
- **Thinking Mode:** enabled
- **SRIT Version:** 2.2
- **Scarcity Type (optional):** capacity resource

---

## System Definition Statement

**System:** West Africa regional electricity grid

**Boundary:** Includes generation assets (thermal, hydro, and renewable), transmission infrastructure, grid interconnections between member states, system operators and dispatch functions, and the regional coordination body (WAPP — West Africa Power Pool). Excludes upstream fuel supply chains (gas extraction, coal mining), downstream end-user consumption, national energy policy and regulatory bodies, and financing and procurement functions.

**Time Horizon:** 18–36 months

**Failure Condition:** The grid cannot meet regional electricity demand at sufficient reliability and volume to sustain industrial, commercial, and residential load — evidenced by sustained load shedding, chronic under-supply, or interconnection collapse across two or more member states.

---

## Boundary Audit Table

| Candidate | Boundary Status | Reason |
|-----------|-----------------|--------|
| Dispatchable generation capacity in available form | In scope | Generation assets are explicitly inside the boundary. |
| Frequency-control reserve margin | In scope | Real-time operating reserve sits inside system operators, dispatch functions, and connected grid operation. |
| Interconnector transfer capacity | In scope | Grid interconnections between member states are explicitly inside the boundary. |
| Transmission network integrity | In scope | Transmission infrastructure is explicitly inside the boundary. |
| Reactive power and voltage support reserve | In scope | Voltage-support capability is part of operating the included transmission and generation system. |
| Protection-system coordination integrity | In scope | Protection operation is part of maintaining operable transmission and interconnected grid behaviour within the boundary. |
| Dispatch and control-room coordination bandwidth | In scope | System operators and dispatch functions are explicitly inside the boundary. |
| System visibility and telemetry quality | In scope | Operational visibility is part of included dispatch and system-operator functions. |
| Skilled grid operations labour | In scope | The labour required to run included system-operator and grid-operating functions resides inside the named system. |
| Maintenance execution capacity | In scope | Preserving operability of included generation and transmission assets falls inside the operational system boundary. |
| Outage restoration capability | In scope | Restoration of included grid assets and interconnections is part of operating the named system. |
| Spare parts availability for critical grid components | Adjacent system signal | This candidate depends materially on procurement and replenishment pathways, and financing/procurement functions are explicitly excluded. |
| Hydrological availability for hydro generation | Adjacent system signal | This is an environmental feeder resource external to the defined operating grid boundary. |
| Delivered fuel continuity to thermal generation | Adjacent system signal | Upstream fuel supply chains are explicitly excluded from the boundary. |
| Cross-border operating trust and compliance | In scope | This sits inside coordination between included operators and the included regional coordination body. |
| Regional operating authority over member-state actions | In scope | This candidate is tied to the included regional coordination layer rather than the excluded national policy/regulatory bodies as such. |
| Time available for redispatch and contingency response | In scope | Response-time margin is part of included dispatch and operating functions. |
| Black-start and system restoration capability | In scope | Restoration capability for the included grid and interconnections sits inside the operating system. |

---

## Mechanism Gate Table

| Candidate | Step 1 Result | Standalone Failure Pathway | Governed Resource (if applicable) | Gate Result |
|-----------|---------------|----------------------------|-----------------------------------|-------------|
| Dispatchable generation capacity in available form | Triggered | Insufficient callable generation alone directly produces regional under-supply and sustained load shedding. | | Resource candidate |
| Frequency-control reserve margin | Triggered | Insufficient reserve alone directly permits frequency instability, trips, and cascading disruption. | | Resource candidate |
| Interconnector transfer capacity | Triggered | Insufficient transfer capacity alone directly prevents regional balancing across states and can produce multi-state shortage or separation. | | Resource candidate |
| Transmission network integrity | Triggered | Failure of core transmission operability alone directly isolates generation or load and fractures regional delivery continuity. | | Resource candidate |
| Reactive power and voltage support reserve | Triggered | Insufficient voltage-support reserve alone directly causes voltage instability or collapse and loss of deliverability. | | Resource candidate |
| Protection-system coordination integrity | Triggered | Miscoordination alone can directly trip healthy assets or fail to contain faults, removing service production paths. | | Resource candidate |
| Dispatch and control-room coordination bandwidth | Triggered | Failure acts mainly by not directing reserve, redispatch, and transfers in time. | Frequency-control reserve margin / interconnector transfer capacity | Mechanism — eliminate |
| System visibility and telemetry quality | Triggered | Failure acts mainly by leaving other operating resources wrongly mobilised, delayed, or unprotected. | Frequency-control reserve margin / interconnector transfer capacity | Mechanism — eliminate |
| Skilled grid operations labour | Triggered | Insufficiency of competent operating labour can directly disable safe dispatch, protection, and live grid operation. | | Resource candidate |
| Maintenance execution capacity | Triggered | Failure acts mainly by leaving generation and transmission resources unreproduced or unprotected across the horizon. | Dispatchable generation capacity / transmission network integrity | Mechanism — eliminate |
| Outage restoration capability | Triggered | Failure acts mainly by delaying return of failed assets and corridors to usable service. | Transmission network integrity / dispatchable generation capacity | Mechanism — eliminate |
| Cross-border operating trust and compliance | Triggered | Failure acts mainly by withholding coordinated use of transfer paths and reserve-sharing. | Interconnector transfer capacity / frequency-control reserve margin | Mechanism — eliminate |
| Regional operating authority over member-state actions | Triggered | Failure acts mainly by not securing compliance needed to mobilise reserve, generation, and flows. | Frequency-control reserve margin / interconnector transfer capacity | Mechanism — eliminate |
| Time available for redispatch and contingency response | Triggered | Failure acts mainly by leaving reserve and redispatch unmobilised before instability overtakes response. | Frequency-control reserve margin | Mechanism — eliminate |
| Black-start and system restoration capability | Triggered | Failure acts mainly by governing remobilisation of service after collapse rather than by direct first-order production failure. | Dispatchable generation capacity / transmission network integrity | Mechanism — eliminate |

---

## Adversarial Challenge Record(s)

None.

---

## Candidate Mechanism-Layer Items for DAI

- **Dispatch and control-room coordination bandwidth** — governs frequency-control reserve margin / interconnector transfer capacity — allocates and directs stabilising and balancing actions rather than being the resource consumed.
- **System visibility and telemetry quality** — governs frequency-control reserve margin / interconnector transfer capacity — shapes whether operating resources are mobilised correctly and in time.
- **Maintenance execution capacity** — governs dispatchable generation capacity / transmission network integrity — preserves other resources rather than constituting the direct operating resource itself.
- **Outage restoration capability** — governs transmission network integrity / dispatchable generation capacity — restores failed resources rather than being the primary scarce resource consumed in service production.
- **Cross-border operating trust and compliance** — governs interconnector transfer capacity / frequency-control reserve margin — conditions whether regional operating resources are actually shared and used.
- **Regional operating authority over member-state actions** — governs frequency-control reserve margin / interconnector transfer capacity — secures or fails to secure compliant mobilisation of other resources.
- **Time available for redispatch and contingency response** — governs frequency-control reserve margin — determines whether stabilising reserve is mobilised in time.
- **Black-start and system restoration capability** — governs dispatchable generation capacity / transmission network integrity — remobilises service after collapse rather than directly producing ongoing service.

---

## Adjacent System Signals

- **Spare parts availability for critical grid components** — may be binding in the excluded asset-support / procurement / replenishment layer; may warrant a separate SRIT run.
- **Hydrological availability for hydro generation** — may be binding in an external environmental feeder system; may warrant a separate SRIT run.
- **Delivered fuel continuity to thermal generation** — may be binding in the excluded upstream fuel-supply system; may warrant a separate SRIT run.

---

## Provisional Shortlist

The strongest remaining scarce resources are:

1. Dispatchable generation capacity in available form
2. Frequency-control reserve margin
3. Interconnector transfer capacity
4. Transmission network integrity
5. Reactive power and voltage support reserve

**Why these remain:**
- Each is clearly in scope under the locked Prompt 1 boundary.
- Each has a direct standalone service-production failure pathway under the Prompt 4 gate.
- Each scored meaningfully on reproduction requirement, failure causality, and substitution resistance in the Prompt 3 matrix.
- None survives merely by being important, upstream, or governance-related; the mechanism-like candidates were removed at Prompt 4.
- Together they define the strongest remaining field at the regional operating layer.

**Outstanding ambiguity:**
The unresolved issue is whether the binding scarcity at the regional level is primarily available supply, real-time stabilising reserve, cross-border transfer capability, broader transmission operability, or location-specific voltage-support reserve. That discrimination is deferred to Prompt 5 evidence testing.

---

## Prompt 5 Late-Catch Retest Log

- **Candidate:** Dispatchable generation capacity in available form — Late-catch check applied — no mechanism character identified in weakening evidence — Remains on ranking — Ranking recomputed: Not applicable
- **Candidate:** Frequency-control reserve margin — Late-catch check applied — no mechanism character identified in weakening evidence — Remains on ranking — Ranking recomputed: Not applicable
- **Candidate:** Interconnector transfer capacity — Late-catch check applied — no mechanism character identified in weakening evidence — Remains on ranking — Ranking recomputed: Not applicable
- **Candidate:** Transmission network integrity — Late-catch check applied — no mechanism character identified in weakening evidence — Remains on ranking — Ranking recomputed: Not applicable
- **Candidate:** Reactive power and voltage support reserve — Late-catch check applied — no mechanism character identified in weakening evidence — Remains on ranking — Ranking recomputed: Not applicable

---

## Binding Scarce Resource Declaration

In the West Africa regional electricity grid, at the regional fleet/system level, over an 18–36 month horizon, the binding scarce resource is **dispatchable generation capacity in available form**, because depletion, misallocation, or failed protection of this resource causes primary system instability and cannot be durably substituted.

### Protectable Resource Form

The resource that must actually be preserved is **regionally usable dispatchable generating output in operationally callable form**.

That means:
- sufficient megawatt output must remain technically operable, synchronisable, and dispatchable into the regional grid
- it must exist in a state that system operators can actually call on within operating timeframes relevant to sustaining load
- it must remain usable at the regional fleet/system layer, not merely present as installed nameplate capacity at isolated assets
- nominal presence is inadequate where capacity is derated, unavailable, forced out, unsynchronised, stranded, or otherwise not callable into service when load must be met
- apparent substitutes such as reserve margin, interconnector support, or voltage-support capability fail if callable generation volume itself is insufficient, because those alternatives can stabilise or redistribute supply but cannot durably replace missing available megawatts across the defined failure condition

### Selection Rationale

- The locked Prompt 1 boundary explicitly includes generation assets, transmission infrastructure, interconnections, system operators, dispatch functions, and WAPP. Within that boundary, dispatchable generation capacity in available form is a direct in-scope operating resource rather than an adjacent feeder or governance mechanism.
- The locked Prompt 1 failure condition gives explicit weight to sustained load shedding and chronic under-supply across two or more member states. Of the surviving candidates, dispatchable generation capacity in available form is the most direct fit with that failure signature over an 18–36 month horizon.
- In Prompt 4 it survived the Mechanism Gate as a true resource candidate because insufficiency of callable generation alone can produce the defined failure condition through direct failure of service production.
- In Prompt 5 it ranked first because it best explains persistent inability to meet regional demand at sufficient reliability and volume, while still remaining hard to substitute durably within the locked boundary.
- The alternative surviving candidates remain important, but on the present record they explain narrower aspects of the failure condition more strongly than they explain the whole of it.

---

## Strongest Alternative Rejected

**Candidate:** Frequency-control reserve margin

**Why rejected:**
- It is the strongest rival because it best explains abrupt instability, cascading trips, and interconnection collapse.
- On the current record, however, it is less complete than dispatchable generation capacity in available form for explaining the explicit Prompt 1 pattern of sustained load shedding and chronic under-supply over an 18–36 month horizon.
- Its explanatory strength depends on dynamic instability being the first-order and dominant failure signature. That remains plausible, but not sufficiently dominant on the present record to displace the lead candidate.
- It therefore remains the most likely alternative scarcity if the present declaration proves wrong, but it does not currently stand above the selected resource.

---

## Confidence Rating and Residual Uncertainty

**Confidence rating:** 7/10

**Residual uncertainty:**
- The main unresolved issue is whether the system's primary failure signature is fundamentally volume scarcity of callable generation or real-time stability scarcity in the form of reserve margin, with chronic under-supply then emerging downstream.
- A second unresolved issue is whether some observed generation shortfall is actually nominal-capacity illusion — that is, installed generation appears adequate on paper but collapses into non-availability at the callable-operating layer.
- A third unresolved issue is whether transmission/interconnection weakness is acting mainly as a separate rival scarcity or as the pathway through which available generation fails to become regionally usable.
- If this declaration is incorrect, the most likely alternative scarcity is frequency-control reserve margin.

---

## DAI Entry Test Questions

- Does the actual denial architecture protect callable dispatchable generation availability at the regional operating layer, or does it mainly react after shortfall has already appeared?
- When major regional failures occur, do they begin with insufficient available megawatts or with reserve exhaustion / instability events on otherwise nominally available supply?
- What evidence distinguishes installed generation capacity from generation capacity in operationally callable form across the member-state system?
- To what extent is chronic under-supply a direct consequence of missing callable generation, versus a downstream consequence of instability, voltage limitation, or corridor failure?
- Are there binding regional mechanisms that preserve generation availability before shortfall appears, or is protection left to fragmented national or asset-level action?
- Where callable generation appears nominally present but demand still cannot be met, what specific condition makes that capacity non-usable: outage, derating, synchronisation failure, dispatch non-availability, transmission isolation, or stability limitation?

---

*SRIT Version 2.2 — West Africa regional electricity grid — 2026-03-31*

*© Philip Harry Galvin 2026. Scarcity–Denial Canon and derived works. Licensed CC BY-NC-ND 4.0.*
