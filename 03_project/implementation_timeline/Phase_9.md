# Phase 9: System Integration and Pre-Commissioning Review

## Field Planning and Learning Guide — Mount Hope Pilot

---

## Document Status

**Status:** Working implementation-planning document
**Current site:** Mount Hope, West Virginia
**Project phase:** Proposed first-phase implementation
**Purpose:** System integration review, connection verification, discrepancy resolution, commissioning readiness, and evidence capture

This document does **not** constitute:

* an electrical wiring diagram;
* an engineered power design;
* a network construction drawing;
* an approved energization procedure;
* a universal startup sequence;
* a final Starlink, Raspberry Pi, LoRa, or Meshtastic architecture;
* a substitute for manufacturer instructions;
* a substitute for qualified electrical or network review;
* or authorization for unqualified personnel to perform electrical work.

The final connection, inspection, energization, and startup procedures must follow:

* the actual approved system architecture;
* final equipment;
* manufacturer instructions;
* applicable electrical and technical requirements;
* site-specific design;
* qualified technical review where required;
* commissioning procedures;
* and applicable permissions or inspections.

Where this guide conflicts with an approved design, manufacturer instruction, applicable requirement, inspection condition, or qualified professional determination, the controlling requirement governs.

---

# What This Document Is For

Phase 9 is the point where the Mount Hope pilot stops being viewed as a collection of individually installed components and begins being reviewed as **one integrated system**.

Earlier phases may address:

* power;
* public connectivity;
* outdoor equipment;
* candidate resilient communications;
* enclosures;
* network paths;
* mounting;
* and supporting infrastructure.

Phase 9 asks:

> Do the components that were actually approved and installed fit together correctly, safely, maintainably, and consistently with the final design before commissioning begins?

That is the purpose of this phase.

---

# Why Phase 9 Exists as Its Own Gate

The original workflow correctly identified that a system-level review is different from checking components individually.

A cable may appear acceptable when viewed only at one enclosure.

A power component may appear correct when viewed only within one phase.

A network device may appear configured correctly when tested by itself.

But integration problems often occur **between** those components.

Phase 9 therefore serves as a formal boundary:

```text id="goj4p7"
individual components installed
            ↓
actual as-built architecture identified
            ↓
system-wide review
            ↓
discrepancies resolved
            ↓
pre-commissioning approval
            ↓
Phase 10 commissioning
```

Phase 9 should not be treated merely as the last wiring step.

It is a **readiness gate**.

---

# What Phase 9 Covers

The exact system reviewed in Phase 9 depends on what earlier phases ultimately approved and installed.

The review may include:

* indoor power equipment;
* backup power;
* internet equipment;
* routers or gateways;
* network switches;
* local computing equipment;
* public-access equipment;
* outdoor communications equipment;
* solar or other outdoor power infrastructure;
* low-bandwidth radio equipment if retained after Phase 8 evaluation;
* wired network paths;
* wireless network paths;
* enclosures;
* cable routing;
* physical protection;
* grounding or bonding documentation where applicable;
* network segmentation;
* administrative interfaces;
* and monitoring systems.

Not every candidate component described in earlier planning documents must exist in the final system.

Phase 9 reviews the **as-built system**, not the original parts list.

---

# Phase 9 Integration Principle

The system should be reviewed according to the architecture that actually exists.

```text id="l7o3r8"
planned architecture
        ↓
approved design
        ↓
installed configuration
        ↓
as-built record
        ↓
integration review
```

If the installed configuration differs from the approved design, the discrepancy should be identified and resolved before commissioning.

---

# Step 1: Establish the As-Built Configuration

Before reviewing connections, document what was actually installed.

The Phase 9 record should identify, as applicable:

* internet source;
* gateway or router;
* network switches;
* public-access equipment;
* administrative equipment;
* local computing equipment;
* outdoor power system;
* energy storage;
* solar equipment;
* communications nodes;
* enclosures;
* cable paths;
* network paths;
* public and private network boundaries;
* monitoring components;
* and any equipment originally proposed but ultimately omitted.

The first question is:

> What system are we actually about to commission?

That answer should not be inferred from an old shopping list.

---

# Step 2: Compare As-Built to Approved Design

Review the installed configuration against the latest approved project documentation.

Identify:

* approved components that were installed;
* approved components that were not installed;
* substitutions;
* changed locations;
* altered cable routes;
* changed power sources;
* changed network topology;
* changed mounting methods;
* changed enclosures;
* changed antenna arrangements;
* and any other material deviation.

Each material deviation should be:

* documented;
* explained;
* technically reviewed where necessary;
* and accepted before commissioning.

The purpose is not to punish field adaptation.

The purpose is to ensure the actual system has a traceable design basis.

---

# Step 3: Review Power-System Readiness

Power-system review should be performed against the **final approved electrical design and equipment instructions**.

This guide intentionally does not prescribe:

* a universal UPS arrangement;
* surge-protector placement;
* conductor connections;
* fuse sizes;
* polarity conventions;
* solar-controller wiring;
* battery wiring;
* energization sequence;
* disconnect sequence;
* or startup order.

Those depend on the actual equipment and design.

The review should instead confirm that appropriate qualified review has addressed, as applicable:

* source power;
* equipment ratings;
* conductors;
* polarity;
* overcurrent protection;
* disconnects;
* battery protection;
* solar inputs;
* controller configuration;
* grounding and bonding;
* surge protection;
* enclosure conditions;
* labeling;
* and manufacturer requirements.

---

## Power readiness evidence

Retain, as appropriate:

* approved power diagram;
* equipment schedule;
* protection-device record;
* inspection information;
* installer or reviewer information;
* manufacturer documentation;
* photographs appropriate for the project record;
* and any correction made before commissioning.

The public repository does not need to publish sensitive infrastructure detail merely because it is retained internally.

---

# Step 4: Review Network-System Readiness

The network review should establish whether the installed components match the approved network architecture.

Confirm, as applicable:

* upstream internet path;
* gateway;
* switching;
* public-access layer;
* private or administrative network;
* outdoor access equipment;
* wired backhaul;
* wireless backhaul;
* local computing systems;
* monitoring;
* and any experimental communications layer.

The review should verify that the actual physical connections correspond to the documented logical architecture.

---

# Step 5: Verify Network Segmentation

Phase 7 establishes that public access should not automatically share the same trust zone as administrative or infrastructure systems.

Phase 9 should confirm that the installed network implements the approved separation.

Review, as applicable:

* public network;
* administrative network;
* infrastructure-management network;
* device-management interfaces;
* local servers or computing equipment;
* and experimental communications services.

The evidence should answer:

> Can a public user reach anything they were not intended to reach?

Any unresolved segmentation problem should block public commissioning.

---

# Step 6: Verify Administrative Ownership

Every managed device should have an identified administrative owner.

Document:

* who administers the gateway;
* who administers the public-access equipment;
* who administers local computing equipment;
* who administers any resilience node;
* how credentials are controlled;
* where configuration backups are stored;
* who performs updates;
* and who responds when equipment fails.

A device with no responsible administrator is not operationally ready simply because it powers on.

---

# Step 7: Review Physical Cable and Connection Protection

Phase 9 should include a system-wide physical inspection of installed cabling.

Review the actual installation for:

* secure routing;
* strain relief;
* abrasion protection;
* environmental suitability;
* UV exposure;
* physical impact exposure;
* trip hazards;
* pinch points;
* excessive tension;
* unsupported transitions;
* enclosure entry;
* weather protection;
* building penetrations;
* public accessibility;
* and maintenance access.

The exact acceptable method depends on the installed cable system and approved design.

This document does not prescribe universal:

* cable type;
* fastening interval;
* bend radius;
* conduit method;
* gland type;
* sealant;
* penetration detail;
* or burial approach.

---

# Step 8: Review Outdoor Enclosures

Each outdoor enclosure should be reviewed as part of the complete system.

Confirm, as applicable:

* correct equipment is inside;
* enclosure is appropriate for the installed environment;
* penetrations are complete;
* unused openings are addressed;
* cable entries are protected;
* internal equipment is secure;
* drainage or condensation concerns have been considered;
* enclosure can be serviced;
* labels are appropriate;
* and the enclosure closes as designed.

Any enclosure opened during Phase 9 should be restored to its approved final condition before commissioning.

---

# Step 9: Review Structural and Mounting Interfaces

Where equipment has been mounted to:

* kiosks;
* poles;
* frames;
* walls;
* existing structures;
* or purpose-built supports,

confirm that the mounting condition remains consistent with the approved installation.

Look for:

* movement;
* loose hardware;
* visible damage;
* interference between components;
* obstructed maintenance access;
* cable stress caused by mounting location;
* and changes created by later phases.

Phase 9 does not certify structural adequacy.

It verifies that no obvious integration problem has appeared after all components are in place.

---

# Step 10: Review Environmental Protection as One System

Earlier phases may each address weather protection within their own scope.

Phase 9 examines the complete installation.

Review:

* exposed electronics;
* cable transitions;
* enclosure interfaces;
* exterior penetrations;
* moisture paths;
* drainage;
* condensation risk;
* solar exposure;
* temperature exposure;
* and any location where one installation phase meets another.

This system-level review is valuable because integration problems often appear at boundaries.

---

# Step 11: Review Grounding, Bonding, and Protection Documentation

Where the final design includes grounding, bonding, surge protection, or related protective systems, Phase 9 should confirm that the approved requirements have been addressed and documented.

This phase does not independently determine:

* electrode requirements;
* conductor sizing;
* bonding method;
* surge-device selection;
* or system grounding.

Those remain matters for the applicable design, manufacturer requirements, and qualified review.

Phase 9 verifies that unresolved protective-system questions do not remain hidden before commissioning.

---

# Step 12: Review Software and Firmware Readiness

Physical integration is only part of the system.

For any managed or programmable equipment, verify that the project has recorded, as applicable:

* firmware version;
* operating-system version;
* configuration version;
* administrative ownership;
* update responsibility;
* configuration backup;
* security settings;
* network settings;
* and recovery method.

Candidate devices removed from the final architecture should not remain connected merely because they were configured earlier.

---

# Step 13: Review Privacy and Logging Configuration

Where the installed system collects operational data, Phase 9 should confirm that the configuration is consistent with the project's privacy decisions.

Review, as applicable:

* connection logs;
* device identifiers;
* access logs;
* telemetry;
* location information;
* administrative logs;
* retention;
* access control;
* and public notice.

The controlling project guidance remains:

[Privacy and Data Stewardship Statement](../../07_privacy/Privacy_and_Data_Stewardship.md)

Phase 9 should identify any configuration that collects more information than the approved service requires.

---

# Step 14: Review Security Readiness

Before commissioning, verify that obvious security gaps have been addressed.

This may include:

* removal of default credentials;
* administrative-password controls;
* management-interface restrictions;
* network segmentation;
* firmware currency;
* disabled unused services;
* secure configuration storage;
* configuration backup;
* remote-access controls;
* and recovery procedures.

Sensitive credentials must not be stored in the public repository.

---

# Step 15: Confirm Monitoring and Failure Visibility

The project should know how it will determine whether the system is working after installation.

For each important component, identify how failure becomes visible.

Possible mechanisms may include:

* device status;
* controller status;
* connectivity checks;
* application health;
* remote monitoring;
* scheduled inspection;
* user reports;
* or another approved method.

The project should be able to distinguish, where practical, among:

* upstream internet failure;
* local network failure;
* access-point failure;
* local computing failure;
* power failure;
* solar or battery failure;
* and experimental communications-node failure.

Without that distinction, maintenance becomes guesswork.

---

# Step 16: Create a Discrepancy List

Any issue discovered during Phase 9 should be captured before commissioning.

Possible statuses include:

* corrected;
* accepted as-is with documented rationale;
* awaiting technical review;
* awaiting parts;
* awaiting site approval;
* deferred outside current scope;
* or commissioning blocker.

A simple discrepancy record may contain:

| Item    | Observation                      | Required Action                         | Owner          | Status      |
| ------- | -------------------------------- | --------------------------------------- | -------------- | ----------- |
| Example | As-built route differs from plan | Update as-built record and review route | Assigned party | Open/Closed |

The actual project record should contain real findings only.

---

# Step 17: Resolve Commissioning Blockers

Not every imperfection has to prevent Phase 10.

But unresolved issues involving safety, architecture, security, privacy, required approvals, or basic system function should not simply be carried forward.

Potential commissioning blockers may include:

* unresolved electrical concern;
* unresolved structural concern;
* exposed or damaged conductor;
* incorrect equipment rating;
* unresolved water intrusion;
* incomplete required inspection;
* unknown administrator credentials;
* public/private network crossover;
* unapproved field substitution;
* missing critical protection;
* or an architecture that no longer matches its documentation.

The responsible technical or project authority should determine whether a discovered issue blocks commissioning.

---

# Step 18: Complete the Pre-Commissioning Review

Once discrepancies have been resolved or formally dispositioned, complete a final readiness review.

The review should answer:

### Physical

* Is the installed hardware secure?
* Are cable paths complete?
* Are enclosures complete?
* Are known environmental exposures addressed?
* Are maintenance areas accessible?

### Power

* Has the installed power system received the required review?
* Are protection and disconnect requirements addressed?
* Are unresolved electrical issues absent?

### Network

* Does the as-built topology match the intended architecture?
* Is public access separated appropriately?
* Are administrative interfaces controlled?

### Software

* Are required configurations loaded?
* Are versions recorded?
* Are backups available where appropriate?

### Governance

* Is administrative ownership assigned?
* Are privacy and logging decisions implemented?
* Are support and maintenance responsibilities clear?

### Evidence

* Does an as-built record exist?
* Are material deviations documented?
* Are unresolved items identified?

Only after those questions have acceptable answers should Phase 10 commissioning begin.

---

# What a Correctly Completed Phase 9 Should Mean

At the conclusion of Phase 9:

* the actual installed system has been identified;
* the as-built architecture has been documented;
* the installation has been compared against the approved design;
* material deviations have been recorded;
* power-system readiness has been reviewed;
* network topology has been reviewed;
* network segmentation has been checked;
* physical connections have been inspected;
* outdoor protection has been reviewed;
* software and firmware status has been recorded;
* privacy and logging configuration has been reviewed;
* cybersecurity readiness has been reviewed;
* administrative ownership is known;
* discrepancies have been resolved or dispositioned;
* commissioning blockers have been cleared;
* and the project has a defensible reason to proceed to Phase 10.

Phase 9 does **not** establish that the system works.

It establishes that the system is ready to be tested.

---

# Phase 9 Evidence Record

Before Phase 10 begins, retain an integration record.

## As-built architecture

Document:

* actual components;
* actual locations;
* power relationships;
* network relationships;
* public/private boundaries;
* outdoor systems;
* and experimental systems retained in the final build.

---

## Deviation record

Document:

* change;
* reason;
* date;
* approving or reviewing party where applicable;
* and effect on other project components.

---

## Physical review record

Document, as appropriate:

* mounting;
* cable routing;
* enclosure condition;
* environmental protection;
* visible damage;
* and corrections.

---

## Power review record

Retain appropriate evidence of:

* approved design;
* review;
* protection;
* inspections where applicable;
* and corrections.

---

## Network review record

Document:

* as-built topology;
* segmentation;
* public-access boundary;
* administrative interfaces;
* and management responsibility.

---

## Software/configuration record

Record:

* relevant firmware versions;
* software versions;
* configuration versions;
* update ownership;
* and backup location.

Do not publish secrets.

---

## Photographic record

Capture, as appropriate:

* indoor equipment area;
* outdoor power area;
* kiosk equipment;
* communications equipment;
* completed enclosures;
* representative cable paths;
* corrected discrepancies;
* and final overall site condition.

Security-sensitive detail may remain internal.

---

## Readiness decision

Record:

* review date;
* participants;
* unresolved items;
* commissioning blockers;
* blocker disposition;
* and final decision:

```text id="1q5jvh"
READY FOR COMMISSIONING

or

NOT READY FOR COMMISSIONING
```

That decision should be supported by the evidence record.

---

# Risk and Learning Categories

## Integration risk

Individually functional components may fail when connected into one architecture.

**Learning objective:** Identify which integration boundaries caused the most problems.

---

## Documentation drift

Field installation may differ from planning documents.

**Learning objective:** Keep the as-built record authoritative for what actually exists.

---

## Power-interface risk

Equipment may have incompatible assumptions about power, protection, startup, or environmental conditions.

**Learning objective:** Verify integration using the actual approved equipment rather than generic procedures.

---

## Network-boundary risk

Public connectivity may unintentionally expose administrative or infrastructure services.

**Learning objective:** Verify trust-zone separation before public commissioning.

---

## Environmental-boundary risk

Failures may occur where cable runs, enclosures, and mounting systems from different phases meet.

**Learning objective:** Review the installation end-to-end, not only component by component.

---

## Maintenance-ownership risk

A functioning device without a responsible maintainer can become an unmanaged failure point.

**Learning objective:** Assign ownership before commissioning.

---

## Configuration-drift risk

The physical system and documented logical configuration can diverge.

**Learning objective:** Preserve a current as-built record and configuration baseline.

---

# Carrying These Lessons Forward

The transferable Phase 9 principles are:

1. **Review the system that was actually built, not the system originally imagined.**
2. **Use the approved design and actual equipment instructions as the technical authority.**
3. **Do not embed universal wiring or energization procedures in a general pilot document.**
4. **Treat physical, power, network, privacy, and security integration as one readiness problem.**
5. **Document field substitutions before they become invisible history.**
6. **Verify public/private network boundaries before public service begins.**
7. **Assign administrative and maintenance ownership before commissioning.**
8. **Treat outdoor protection as a system-wide issue, not an enclosure-by-enclosure issue.**
9. **Resolve safety and security blockers before testing.**
10. **Make Phase 9 a formal go/no-go gate for commissioning.**

---

# Mount Hope Pilot Learning Questions

After implementation, the project should be able to answer:

* How different was the final system from the original concept?
* Which candidate components were ultimately unnecessary?
* Which substitutions were made?
* Why were they made?
* Which integration boundaries caused problems?
* Were power and network designs compatible?
* Did outdoor cable and enclosure decisions hold up?
* Was public/private segmentation effective?
* Were administrative responsibilities clear?
* Did any device become difficult to maintain?
* Were configuration backups adequate?
* Did the as-built record remain accurate?
* Which discrepancies were caught before commissioning?
* Which problems escaped into Phase 10?
* What should future sites review earlier?

Those answers help convert Mount Hope from a one-time installation into a reusable implementation model.

---

# Relationship to Phase 10

Phase 9 and Phase 10 perform different functions.

```text id="f8vjem"
Phase 9
integration and readiness
        ↓
Phase 10
commissioning and demonstrated behavior
```

Phase 9 asks:

> Is this system ready to be tested?

Phase 10 asks:

> What does this system actually do when operated?

Keeping that distinction clear prevents a visual inspection from being treated as proof of operational performance.

---

# Relationship to the Mount Hope First Phase

Phase 9 applies to the **Mount Hope first-phase implementation**.

Its purpose is to create a controlled transition from installation into evidence-producing commissioning.

The sequence is:

```text id="4pf0ts"
approved design
    ↓
installation
    ↓
as-built record
    ↓
integration review
    ↓
discrepancy resolution
    ↓
commissioning readiness
    ↓
Phase 10
```

A completed installation is not automatically a tested system.

An integrated system is not automatically a successful pilot.

Those conclusions belong to later evidence.

---

# Relationship to Future Sites

Future sites should reuse the **integration discipline**, not necessarily Mount Hope's specific equipment.

Another site may have:

* different internet service;
* different power;
* different outdoor hardware;
* no solar;
* no resilient-radio layer;
* different public-access equipment;
* different property ownership;
* different cybersecurity requirements;
* different institutional partners;
* or different maintenance capacity.

Phase 9 therefore standardizes the question:

> Is the actual installation coherent and ready for commissioning?

It does not standardize one hardware topology.

---

# Thurmond Boundary

Thurmond remains a **future federal-phase implementation opportunity**.

A future Thurmond installation would require its own:

* defined federal scope;
* approved technical architecture;
* National Park Service review;
* preservation and cultural-resource compliance as applicable;
* site authorization;
* electrical and structural review;
* network and cybersecurity review;
* privacy and information-governance review;
* approved equipment;
* installation documentation;
* and pre-commissioning review.

Mount Hope can provide the **integration process**.

It cannot pre-approve the Thurmond system.

---

## Phase 9 Completion Boundary

Phase 9 should be considered complete only when the actual Mount Hope installation has been:

```text id="nkb8vk"
documented
    ↓
compared to design
    ↓
reviewed as a system
    ↓
corrected where needed
    ↓
cleared of commissioning blockers
    ↓
approved to enter Phase 10
```

Connected is not commissioned.

Powered is not validated.

Installed is not operational evidence.

Phase 9 exists to establish that the system is **ready to prove what it can actually do**.

---

*Harmony for Hope, Inc. — New River Gorge Safety & Heritage Mesh Pilot*
*Phase 9 | Mount Hope System Integration and Pre-Commissioning Review*
