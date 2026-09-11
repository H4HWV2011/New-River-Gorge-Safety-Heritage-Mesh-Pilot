# Implementation Timeline

This directory contains the working implementation, integration, commissioning, and evidence-planning materials for the **Mount Hope first phase** of the New River Gorge Safety & Heritage Mesh Pilot.

Mount Hope is the project's **initial/current implementation and funding path**.

These documents are intended to move the project from approved scope through site verification, architecture selection, installation, commissioning, evidence capture, evaluation, and later replication decisions.

---

## Reading Order

### 1. `Mount_Hope_Heritage_Infrastructure_Workflow.md`

The **master implementation workflow** for the Mount Hope phase.

It establishes the full implementation sequence:

```text
scope and requirements
        ↓
site verification
        ↓
architecture decision
        ↓
technical and governance review
        ↓
approved design
        ↓
procurement and staging
        ↓
installation
        ↓
as-built documentation
        ↓
integration review
        ↓
commissioning
        ↓
public release
        ↓
evaluation and evidence
```

This document governs the relationship among the more detailed phase materials.

---

### 2. `Phase_6.md`

**Solar and Outdoor Support Hardware**

Planning, technical review, installation, commissioning, and evidence framework for any approved outdoor power and support infrastructure.

Solar and battery equipment remain subject to the final site design and are not treated as predetermined engineering.

---

### 3. `Phase_7.md`

**Public Hotspot and Kiosk Access Layer**

Field-testing and architecture-selection framework for the Mount Hope public-access point.

The phase emphasizes:

```text
test existing coverage
        ↓
select the simplest adequate architecture
        ↓
secure and govern it
        ↓
commission
        ↓
document actual public-access performance
```

---

### 4. `Phase_8.md`

**Resilient Low-Bandwidth Communications Layer**

Evaluation framework for a possible independent low-power communications layer.

LoRa and Meshtastic are treated as **candidate resilience technologies**, not as an already-demonstrated emergency communications system.

The phase distinguishes experimentation, radio-link evidence, mesh behavior, community communications capability, and emergency infrastructure as separate evidence stages.

---

### 5. `Phase_9.md`

**System Integration and Pre-Commissioning Review**

The formal integration and readiness gate.

Phase 9 reviews the **actual as-built system**, resolves discrepancies, confirms administrative and technical readiness, and determines whether the installation is ready to enter commissioning.

```text
installed
    ↓
documented
    ↓
reviewed as one system
    ↓
discrepancies resolved
    ↓
READY / NOT READY FOR COMMISSIONING
```

---

## Phase 10

Phase 10 — **Commissioning and Demonstrated Behavior** — is currently governed by the master workflow.

A separate `Phase_10.md` should be created only when the final Mount Hope architecture is sufficiently defined to support meaningful equipment- and capability-specific commissioning procedures.

Until then:

> installation does not become operational evidence merely because equipment powers on.

Commissioning must test the behavior that the approved system is actually expected to provide.

---

## Status

These are **working implementation-planning documents**.

They do not constitute:

* final engineering;
* procurement authorization;
* construction drawings;
* permits;
* site authorization;
* a final network architecture;
* a final electrical design;
* or evidence that infrastructure has already been deployed.

Dates, locations, equipment, costs, partner roles, deployment sequencing, technical architecture, and final implementation remain subject to:

* funding;
* approved scope;
* site permissions;
* field conditions;
* technical review;
* privacy and cybersecurity review;
* partner coordination;
* procurement;
* applicable approvals;
* and commissioning results.

---

## Evidence Boundary

The documents in this directory follow the project's broader evidence discipline:

```text
planned
    ≠
approved

approved
    ≠
purchased

purchased
    ≠
installed

installed
    ≠
commissioned

commissioned
    ≠
demonstrated long-term outcome
```

Mount Hope is intended to produce the evidence needed to determine what should be retained, changed, simplified, or replicated at later sites.

---

## Future Federal Phase

Thurmond remains a **future federal-phase implementation opportunity, with documented support, contingent on separate federal funding, National Park Service review/compliance, site-specific approval, technical review, and final agreements.**

The Mount Hope implementation may provide useful evidence and process lessons for that future work.

It does not pre-authorize a Thurmond deployment.

---

## Funder-Facing Starting Point

For the funder-facing project overview, begin with:

[`../pilot_scope_and_phasing/New_River_Gorge_Mesh_Pilot_Project_Brief.md`](../pilot_scope_and_phasing/New_River_Gorge_Mesh_Pilot_Project_Brief.md)

For the detailed Mount Hope implementation process, begin with:

[`Mount_Hope_Heritage_Infrastructure_Workflow.md`](Mount_Hope_Heritage_Infrastructure_Workflow.md)
