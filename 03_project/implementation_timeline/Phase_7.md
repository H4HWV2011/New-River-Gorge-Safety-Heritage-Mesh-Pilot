# Phase 7: Public Hotspot and Kiosk Access Layer

## Field Planning and Learning Guide — Mount Hope Pilot

---

## Document Status

**Status:** Working implementation-planning document
**Current site:** Mount Hope, West Virginia
**Project phase:** Proposed first-phase implementation
**Purpose:** Site testing, network-path selection, public-access planning, commissioning, and evidence capture

This document does **not** constitute:

* a final network design;
* a procurement specification;
* a construction drawing;
* authorization to run electrical or communications cabling;
* an approved cybersecurity architecture;
* a final public-Wi-Fi configuration;
* a structural determination for the existing kiosk;
* a privacy or acceptable-use policy; or
* authorization to install equipment on property without the applicable site approval.

Final equipment selection, network architecture, mounting method, cable routing, power source, network segmentation, authentication, logging, administration, security controls, signage, and commissioning criteria must be based on:

* actual field measurements;
* final project scope;
* site conditions;
* approved equipment;
* manufacturer instructions;
* applicable technical requirements;
* privacy and cybersecurity review;
* site permissions; and
* qualified technical review where required.

Where this document conflicts with an approved design, applicable requirement, manufacturer instruction, site agreement, or qualified technical determination, the controlling requirement governs.

---

## What This Document Is For

Phase 7 addresses the **public-facing connectivity layer** at or near the existing Mount Hope Historic Walking Trail kiosk.

This is an important transition in the project.

Earlier phases prepare infrastructure.

Phase 7 asks whether that infrastructure can actually deliver a public service at the point where residents and visitors are expected to use it.

The objective is therefore not:

> install a Raspberry Pi or outdoor access point because that equipment appeared in an early parts list.

The objective is:

> determine the simplest safe, reliable, maintainable, and governable way to provide the approved public-access service at the kiosk area, then document what actually worked.

Because this is the first implementation environment, Phase 7 should generate evidence that can guide future community sites.

---

# Site-Specific Planning Context

The current planning materials identify two important Mount Hope conditions:

1. the kiosk is relatively close to the proposed indoor connectivity source; and
2. a substantial building lies between the two locations.

Those facts create uncertainty.

Distance alone does not establish whether the kiosk will receive usable service.

An obstruction alone does not establish that an additional access point will be required.

The actual result must be measured.

That makes **field testing the decision point** for Phase 7.

---

# Phase 7 Decision Principle

The architecture should become more complex only when field evidence shows that the simpler option is inadequate.

```text
approved public-access objective
        ↓
site and structural review
        ↓
baseline connectivity test
        ↓
does existing coverage meet the defined service need?
        ↓
     yes / no
      ↓     ↓
simplest   evaluate
adequate   additional
path       architecture
      ↓     ↓
technical and security review
        ↓
approved installation
        ↓
commissioning
        ↓
public release
        ↓
evidence and evaluation
```

This approach protects project funds and reduces unnecessary maintenance.

---

# Candidate Connectivity Architectures

The current project has considered several possible approaches.

These should be treated as **candidate architectures**, not predetermined installation paths.

## Candidate A — Existing coverage is sufficient

If field testing demonstrates that the approved public-use area receives adequate service directly from the existing network configuration, additional kiosk networking hardware may not be necessary.

Potential benefits include:

* fewer devices;
* lower capital cost;
* lower maintenance burden;
* fewer weather-exposed components;
* fewer power requirements;
* simpler troubleshooting; and
* less operational complexity.

This outcome should only be selected after actual testing demonstrates that the service meets the project's defined acceptance criteria.

---

## Candidate B — Purpose-built outdoor access equipment

If the existing service does not adequately cover the kiosk area, a purpose-built outdoor access point or similar network device may be considered.

The final device should be selected based on:

* required coverage;
* environmental rating;
* network compatibility;
* power architecture;
* mounting conditions;
* management capabilities;
* security features;
* maintainability;
* availability;
* warranty;
* cost; and
* technical review.

A previously identified model may remain useful as a planning reference, but the repository should not treat one named product as the approved final device until procurement and technical review occur.

---

## Candidate C — Small-computer or bridge configuration

The project has also considered a Raspberry Pi or similar small-computer approach as a possible bridge, access, or application-support device.

That architecture may be useful where the project needs capabilities beyond those provided by a standard access point.

However, it introduces additional responsibilities involving:

* operating-system maintenance;
* storage reliability;
* software configuration;
* security updates;
* credentials;
* remote administration;
* device hardening;
* power;
* enclosure design;
* logging;
* recovery procedures; and
* long-term support.

It should therefore be selected because the required function justifies that complexity — not merely because the hardware appeared on an earlier parts list.

---

# Before Phase 7 Begins

Before public-access equipment is installed, the project should confirm that the applicable prerequisites have been satisfied.

These may include:

* site permission;
* kiosk condition review;
* approved mounting location;
* available internet service;
* approved power architecture where required;
* final network objective;
* administrative ownership of the network;
* privacy and cybersecurity review;
* public-access policy decisions;
* applicable signage requirements; and
* technical responsibility for commissioning and maintenance.

Phase 7 should not proceed merely because equipment is available.

---

# Step 1: Assess the Existing Kiosk

The current kiosk is an existing community heritage asset and should be assessed before any new hardware is attached.

The purpose of the assessment is not to produce an engineering certification.

It is to determine whether the proposed mounting location appears suitable for continued planning or whether additional structural review or repair is necessary.

## Review areas

Document, as applicable:

* posts and supports;
* mounting surfaces;
* roof or canopy condition;
* visible moisture damage;
* visible decay;
* fasteners;
* existing signage;
* accessibility;
* maintenance access;
* nearby pedestrian movement;
* potential impact of added hardware;
* pest or wildlife conditions;
* drainage;
* vandalism exposure; and
* any historic or visual-design considerations.

### Stop-and-review conditions

Conditions such as visible deterioration, movement, damaged mounting surfaces, significant moisture intrusion, unsafe access, or other uncertainty should trigger further review before hardware is attached.

The field team should not improvise structural repairs outside the approved scope.

---

## Kiosk Evidence Record

Capture:

* general photographs;
* mounting-area photographs;
* visible defects;
* existing signage;
* date of assessment;
* person conducting the assessment; and
* any repair or follow-up decision.

The record should describe what was actually observed rather than assigning an unsupported remaining service life.

---

# Step 2: Define the Public-Service Acceptance Criteria

Before testing the network, define what counts as adequate service.

The project should not rely on a universal rule such as:

* a certain number of Wi-Fi bars; or
* one fixed download-speed threshold.

Those measurements may be useful observations, but they are device-dependent and do not by themselves define a successful public service.

Acceptance criteria should instead reflect the actual intended use.

Possible criteria include:

* network discoverability;
* reliable association;
* successful internet access;
* acceptable page-load performance;
* access to the project's public information resources;
* connection stability;
* coverage across the intended public-use area;
* adequate performance on representative devices;
* reasonable latency for the intended use;
* accessibility of required web resources;
* repeatable results across multiple test periods; and
* absence of persistent dead zones in the designated service area.

The final criteria should be documented before the architecture decision is made.

---

# Step 3: Perform the Baseline Connectivity Test

With the proposed source network operating in its intended configuration, test service throughout the kiosk area.

The field test should record more than one measurement.

Where practical, document:

* date;
* time;
* weather;
* source-network configuration;
* router or access-device placement;
* test device;
* test locations;
* network visibility;
* connection success;
* received signal information where the test device exposes it;
* download performance;
* upload performance;
* latency where useful;
* stability;
* disconnects;
* page-load behavior; and
* ability to reach the intended public resources.

Testing should occur across the area people are actually expected to use, not at only one point.

---

## Repeatability

A single successful connection is not enough to establish that the site is ready.

Where practical, repeat testing:

* at multiple positions;
* with more than one representative device;
* at different times; or
* after any source-network configuration change.

The purpose is to determine whether the result is reproducible enough to support public use.

---

# Step 4: Evaluate the Baseline Result

The project should compare the observed performance with the acceptance criteria established before testing.

Possible outcomes are:

| Result                                                | Meaning                                              | Next action                                                    |
| ----------------------------------------------------- | ---------------------------------------------------- | -------------------------------------------------------------- |
| Existing coverage meets the approved service criteria | Additional kiosk network hardware may be unnecessary | Proceed with security, public-access, and commissioning review |
| Coverage is usable but inconsistent                   | Configuration or placement may require adjustment    | Adjust and retest                                              |
| Existing coverage does not meet the defined criteria  | Additional network architecture is required          | Evaluate candidate equipment and routing                       |
| Results are inconclusive                              | More testing is needed                               | Do not procure permanent hardware based on guesswork           |

The decision and supporting evidence should be retained.

---

# Step 5: Evaluate Additional Architecture Only If Needed

If baseline coverage is inadequate, evaluate the simplest architecture that can meet the defined service requirement.

The technical review should consider:

* network topology;
* available data path;
* required power;
* distance;
* obstructions;
* mounting;
* weather exposure;
* cable route;
* maintenance;
* cybersecurity;
* network management;
* cost;
* accessibility;
* public-area coverage;
* and future support.

The project may consider technologies including:

* outdoor access equipment;
* wired Ethernet;
* Power over Ethernet;
* point-to-point wireless links;
* mesh-capable networking;
* an approved bridge;
* small-computer-based networking;
* or another technically appropriate method.

The repository should record **why the chosen architecture was selected**.

---

# Step 6: Review Cable and Power Routing

If the selected architecture requires a cable or separate power source, the route must be reviewed before installation.

The review should address:

* property authority;
* route ownership;
* pedestrian areas;
* vehicle areas;
* trip hazards;
* accessibility;
* weather exposure;
* underground utilities;
* overhead hazards;
* burial or conduit requirements where applicable;
* building penetrations;
* strain relief;
* physical protection;
* serviceability;
* outdoor rating;
* separation from incompatible systems; and
* applicable technical or electrical requirements.

This document does **not** prescribe:

* cable type;
* cable spacing;
* fastening interval;
* burial depth;
* conduit type;
* overhead clearance;
* conductor size;
* extension-cord use;
* or a universal PoE configuration.

Those decisions depend on the approved architecture and installation requirements.

---

# Step 7: Finalize the Public Network Architecture

Before installation, document the intended network arrangement.

The record should identify:

* upstream internet source;
* network device or devices;
* public SSID strategy;
* private or administrative network separation;
* management interface;
* administrative responsibility;
* update responsibility;
* monitoring approach;
* failure recovery;
* and any approved content-access or landing-page structure.

A simple architecture diagram should be retained.

Example:

```text
internet source
      ↓
approved gateway / router
      ↓
network separation
      ↓
public access layer
      ↓
kiosk service area
```

The final diagram should reflect the real installed system.

---

# Step 8: Establish Network Segmentation and Administrative Boundaries

Public access should not automatically place members of the public on the same logical network used for:

* project administration;
* organizational devices;
* internal systems;
* infrastructure management;
* privileged interfaces;
* or other protected services.

The approved network architecture should determine how public access is separated from administrative or infrastructure access.

Document:

* which network is public;
* which networks are not public;
* who can administer the access equipment;
* how administrative access is protected;
* where credentials are maintained;
* and how access is revoked when responsibilities change.

---

# Step 9: Establish Privacy and Logging Boundaries

Before public launch, identify what the network equipment and associated systems may collect.

Depending on final architecture, this may include:

* device identifiers;
* network addresses;
* connection times;
* session information;
* bandwidth information;
* error logs;
* security logs;
* administrative logs;
* or other operational telemetry.

The project should determine:

* what is actually necessary;
* why it is collected;
* who can access it;
* how long it is retained;
* whether it is shared;
* how it is protected; and
* what public notice is appropriate.

The controlling project guidance is maintained in:

[Privacy and Data Stewardship Statement](../../07_privacy/Privacy_and_Data_Stewardship.md)

The network should not collect more information merely because the equipment is capable of collecting it.

---

# Step 10: Establish Cybersecurity and Maintenance Readiness

Before public service begins, the project should confirm responsibility for:

* device configuration;
* firmware updates;
* operating-system updates where applicable;
* password management;
* administrative credentials;
* configuration backups;
* remote administration;
* vulnerability response;
* device replacement;
* security incidents;
* network outages;
* and restoration procedures.

If a small computer is used, additional responsibilities may include:

* software-image management;
* package updates;
* storage replacement;
* configuration management;
* secure remote access;
* and recovery from corrupted storage.

The simplest maintainable architecture should be preferred where it meets the public-service objective.

---

# Step 11: Install the Approved Hardware

Only after the architecture has been selected and reviewed should physical installation proceed.

Installation should follow:

* the final site plan;
* approved mounting method;
* manufacturer instructions;
* applicable technical requirements;
* approved cable route;
* approved power architecture;
* and site authorization.

The field team should not substitute products, alter mounting locations, create new penetrations, or change network architecture without documenting and approving the deviation where appropriate.

---

# Step 12: Configure the Public Access Layer

The public network should be configured according to the approved architecture.

Configuration may address:

* public network name;
* authentication method, if any;
* landing page or captive portal, if used;
* network isolation;
* administrative access;
* bandwidth management;
* security settings;
* privacy settings;
* DNS configuration;
* content restrictions where lawfully and appropriately required;
* logging;
* and service monitoring.

The actual configuration should be recorded securely.

Sensitive credentials should **not** be published in the public repository.

---

# Step 13: Test the Installed Architecture

After installation, repeat field testing across the intended public-use area.

The same acceptance criteria used during baseline testing should be applied where relevant.

Record:

* network visibility;
* successful connection;
* internet access;
* stability;
* representative device behavior;
* project website or resource access;
* performance observations;
* dead zones;
* faults;
* and corrective actions.

If the architecture includes additional access equipment, compare the result with the baseline.

That comparison is part of the pilot evidence.

---

# Step 14: Complete Public-Access Readiness Review

Before signage announces that the service is available, verify that the public service is genuinely ready.

The readiness review should address:

* connectivity;
* reliability;
* network name;
* privacy notice where applicable;
* security;
* signage;
* accessibility;
* support contact;
* administrative ownership;
* monitoring;
* maintenance;
* and recovery procedures.

A hotspot sign should not be treated as decoration.

It is a public representation that the service is available.

The sign should therefore go up **after commissioning**, not before.

---

# Step 15: Install Public Signage

Once the service has passed commissioning and readiness review, install the approved public-facing signage.

The sign may identify:

* free public Wi-Fi availability;
* the approved public network name;
* basic connection instructions;
* a project information link or QR code;
* appropriate privacy information;
* accessibility information where useful;
* and a support or problem-reporting method.

Public signage should not expose:

* administrative credentials;
* private network information;
* internal infrastructure details;
* or sensitive security information.

---

# What a Completed Phase 7 Should Mean

A correctly completed Phase 7 should mean that:

* the kiosk was assessed before mounting;
* public-service acceptance criteria were defined;
* baseline connectivity was measured;
* architecture was selected from evidence rather than assumption;
* unnecessary equipment was avoided;
* required hardware was technically reviewed;
* network separation was addressed;
* privacy and logging were addressed;
* cybersecurity responsibilities were assigned;
* the approved equipment was installed;
* the public-access layer was commissioned;
* the service worked across the intended area;
* signage accurately represented the available service;
* and the resulting evidence was preserved.

It should **not** mean merely that a Wi-Fi network name appeared on a phone.

---

# Public Hotspot Evidence Record

When Phase 7 is complete, retain a structured record.

## Baseline test record

Document:

* date;
* test locations;
* source-network placement;
* test device or devices;
* connection results;
* performance observations;
* coverage observations;
* and relevant environmental conditions.

---

## Architecture decision

Record:

* candidate architectures evaluated;
* selected architecture;
* reason for selection;
* equipment selected;
* technical reviewer where applicable;
* and any architecture that was rejected and why.

---

## Equipment record

Where equipment is installed, record:

* manufacturer;
* model;
* serial number where appropriate;
* firmware or software version where useful;
* installation date;
* mounting location;
* and maintenance responsibility.

---

## Network record

Maintain securely:

* architecture diagram;
* public SSID;
* administrative ownership;
* segmentation approach;
* configuration backup location;
* privacy/logging configuration;
* update responsibility;
* and recovery procedure.

Passwords and secrets should not be committed to the public repository.

---

## Photographic record

Capture, as appropriate:

* kiosk before installation;
* structural or mounting condition;
* approved hardware location;
* completed hardware;
* cable path where suitable for release;
* final kiosk appearance;
* and installed public signage.

Detailed security-sensitive infrastructure photographs may remain internal.

---

## Commissioning record

Document:

* commissioning date;
* acceptance criteria;
* test results;
* devices tested;
* service area tested;
* faults;
* remediation;
* final status;
* and person responsible for acceptance.

---

# Risk and Learning Categories

Rather than treating planning assumptions as documented failures, the Mount Hope pilot should observe and record actual risk categories.

## Coverage risk

Potential causes include:

* obstruction;
* distance;
* interference;
* equipment placement;
* building materials;
* foliage;
* or inadequate architecture.

**Learning objective:** Determine what actually limits coverage at Mount Hope.

---

## Reliability risk

Potential causes include:

* upstream service interruption;
* power failure;
* access-point failure;
* configuration errors;
* environmental exposure;
* cable faults;
* or software failure.

**Learning objective:** Distinguish upstream internet problems from local-network problems.

---

## Maintenance risk

More complex architectures may create more:

* update requirements;
* credentials;
* failure points;
* replacement parts;
* remote-support needs;
* and specialized knowledge.

**Learning objective:** Determine the lowest-complexity architecture that reliably serves the public.

---

## Privacy risk

Public access may generate operational metadata.

**Learning objective:** Determine what information is genuinely needed to operate the service without collecting unnecessary user information.

---

## Cybersecurity risk

Public-facing networks can create exposure if they are poorly segmented or administered.

**Learning objective:** Verify that public use cannot become unauthorized administrative access.

---

## Physical risk

Outdoor hardware may experience:

* moisture;
* temperature changes;
* vandalism;
* wildlife;
* cable damage;
* UV exposure;
* or structural deterioration.

**Learning objective:** Track which protective measures actually prove necessary at the Mount Hope site.

---

# Carrying These Lessons Forward

The transferable lessons from Phase 7 should be principles rather than copied hardware recipes.

For future sites:

1. **Define what “usable public service” means before measuring it.**
2. **Test before purchasing additional hardware.**
3. **Do not infer performance from distance alone.**
4. **Obstructions matter, but only field measurements show their actual effect.**
5. **Choose the simplest architecture that meets the defined service objective.**
6. **Do not add a Raspberry Pi merely because one appeared in an early concept.**
7. **Treat public and administrative networks as separate trust zones.**
8. **Define privacy and logging before public launch.**
9. **Assign maintenance and cybersecurity responsibility before the service becomes public.**
10. **Commission the service before installing signage that promises it exists.**
11. **Record baseline and post-installation results so the pilot produces evidence.**
12. **Preserve actual field findings rather than converting assumptions into facts.**

---

# Mount Hope Pilot Learning Questions

After Phase 7 has operated long enough to produce useful evidence, the project should be able to answer:

* Did existing coverage reach the kiosk adequately?
* If not, what was the actual limiting condition?
* What architecture was selected?
* Why was it selected?
* What did it cost?
* Did the additional hardware materially improve service?
* Was the service stable across representative devices?
* Where were the actual coverage boundaries?
* Did weather materially affect performance?
* Did the public understand the signage?
* Were people able to connect without assistance?
* What support requests occurred?
* What network failures occurred?
* Were those failures upstream or local?
* What maintenance burden emerged?
* Did privacy or logging settings need adjustment?
* Were security boundaries effective?
* Was any hardware purchased that ultimately proved unnecessary?
* What would be done differently at the next site?

Those answers are more valuable for replication than a predetermined equipment list.

---

# Relationship to the Mount Hope First Phase

Phase 7 applies to the **Mount Hope first-phase implementation**.

Its purpose is to create the first real public-access evidence for the project.

The current sequence is:

```text
planning
    ↓
site testing
    ↓
architecture selection
    ↓
technical and governance review
    ↓
installation
    ↓
commissioning
    ↓
public use
    ↓
evaluation
```

The presence of a proposed hotspot in repository documents does not mean that the hotspot is already deployed.

The existence of networking equipment does not mean that public service is operational.

The service becomes evidence only when it has actually been installed, commissioned, documented, and evaluated.

---

# Relationship to Future Sites

The Mount Hope result may inform later community deployments, but its architecture should not automatically be copied elsewhere.

Future sites may differ in:

* upstream internet service;
* distance;
* building materials;
* topography;
* power;
* available structures;
* property authority;
* public use;
* cybersecurity requirements;
* maintenance capacity;
* historical context;
* and institutional requirements.

This is especially important for **Thurmond**, which remains a future federal-phase implementation opportunity.

A future Thurmond public-access design would require its own:

* federal project scope;
* National Park Service review;
* site-specific authorization;
* technical design;
* preservation review where applicable;
* cybersecurity review;
* privacy and information-governance review;
* public-access policy;
* accessibility consideration;
* equipment approval;
* and final agreements.

Mount Hope should provide evidence for that future design discussion.

It should not pre-decide it.

---

## Phase 7 Completion Boundary

Phase 7 should be considered complete only when the approved Mount Hope public-access layer has been:

```text
measured
    ↓
designed
    ↓
reviewed
    ↓
installed
    ↓
secured
    ↓
commissioned
    ↓
documented
    ↓
released for public use
```

A detected Wi-Fi signal is not a commissioned public service.

A purchased access point is not an operational hotspot.

A sign is not evidence of connectivity.

The purpose of Phase 7 is to move from **assumed coverage to demonstrated public access**.

---

*Harmony for Hope, Inc. — New River Gorge Safety & Heritage Mesh Pilot*
*Phase 7 | Mount Hope Public Hotspot and Kiosk Access Planning Guide*
