# Phase 8: Resilient Low-Bandwidth Communications Layer

## Field Planning and Learning Guide — Mount Hope Pilot

---

## Document Status

**Status:** Working implementation-planning document
**Current site:** Mount Hope, West Virginia
**Project phase:** Proposed first-phase implementation
**Purpose:** Resilience-use-case definition, technical evaluation, radio-path testing, candidate-system commissioning, and evidence capture

This document does **not** constitute:

* a public emergency-communications plan;
* an emergency-services communications system;
* a guaranteed backup communications capability;
* a final radio-frequency design;
* authorization to operate any specific radio configuration;
* a final Meshtastic architecture;
* a procurement specification;
* an approved antenna system;
* a final power-system design;
* a coverage guarantee;
* or a representation that Harmony for Hope currently operates a regional communications mesh.

Any low-bandwidth radio or mesh system considered for the Mount Hope pilot must be evaluated according to:

* the actual resilience use case;
* applicable radio and equipment requirements;
* final hardware;
* approved firmware and configuration;
* antenna characteristics;
* power design;
* site conditions;
* privacy and governance requirements;
* security;
* technical review;
* and observed field performance.

A successful experiment should be described as a successful experiment.

It should not be represented as emergency infrastructure unless later evidence and appropriate institutional arrangements support that claim.

---

# What This Document Is For

Phase 8 evaluates whether the Mount Hope pilot should include an **independent, low-power, low-bandwidth communications layer** in addition to ordinary internet access.

The original project concept identified LoRa and Meshtastic as a possible approach because they can support small-message communications using comparatively little power.

That concept remains worth testing.

The planning question, however, is not:

> How do we install the LoRa node already selected?

The planning question is:

> Does a low-bandwidth radio layer provide enough demonstrable resilience value at Mount Hope to justify its technical, governance, maintenance, and user-adoption requirements?

That question must be answered with evidence.

---

# The Resilience Hypothesis

The working hypothesis for Phase 8 is:

> A low-power communications system that does not depend on the public internet may provide a useful secondary communications path during some local connectivity disruptions.

That hypothesis contains several unresolved questions:

* What specific problem would it solve?
* Who would actually use it?
* What devices would users need?
* What range is achievable at the Mount Hope site?
* Are other compatible nodes already reachable?
* Does one node provide meaningful utility?
* Is a second or third node necessary to test the idea?
* What information should travel over the system?
* What information should **not** travel over it?
* How would privacy be handled?
* Who would administer it?
* How would firmware and configuration be maintained?
* What happens when nodes become unavailable?
* Does independent power materially improve resilience?
* Does the benefit justify additional infrastructure?

Phase 8 exists to answer those questions.

---

# What LoRa and Meshtastic May Provide

LoRa is a low-power radio technology designed for relatively small data payloads over distances that can exceed conventional short-range wireless technologies under suitable conditions.

Meshtastic is one software ecosystem that can use compatible LoRa hardware to exchange low-bandwidth messages among participating devices.

For this project, such a system might potentially support:

* short text messages;
* node-status information;
* limited location or position information where appropriate;
* project test messages;
* infrastructure-status signals;
* volunteer coordination during controlled exercises;
* or other narrowly defined low-bandwidth uses.

It is **not** a substitute for ordinary broadband internet.

It should not be described as capable of providing:

* general web browsing;
* ordinary public Wi-Fi;
* voice replacement;
* 911 replacement;
* guaranteed emergency communications;
* public-safety radio interoperability;
* or universal communications coverage.

Those are materially different capabilities.

---

# Experimental Resilience Layer vs. Emergency Communications

This distinction is central to Phase 8.

```text id="9jvpxx"
experimental low-bandwidth node
            ≠
public emergency communications system
```

A technically functioning node may establish that:

* two devices can exchange messages;
* radio coverage exists between certain locations;
* a node can operate without the internet;
* solar or battery power can sustain it;
* or a mesh path can be formed under certain conditions.

That does **not** establish that:

* residents possess compatible devices;
* the public knows how to use the system;
* messages will reach emergency responders;
* the network will remain available during a disaster;
* emergency agencies monitor the system;
* the system satisfies public-safety requirements;
* the network has sufficient geographic coverage;
* or the project should be marketed as emergency infrastructure.

Any future emergency-management role would require a separate institutional, operational, legal, technical, and partnership pathway.

---

# Phase 8 Decision Sequence

The correct sequence begins with the use case.

```text id="gx7dao"
define resilience problem
        ↓
identify intended users
        ↓
define permitted message types
        ↓
evaluate candidate technologies
        ↓
radio / regulatory / technical review
        ↓
bench test
        ↓
field propagation test
        ↓
does the approach provide useful value?
        ↓
     yes / no
      ↓     ↓
pilot       document
design      finding
      ↓
approved hardware and configuration
        ↓
installation
        ↓
commissioning
        ↓
operating exercise
        ↓
evidence and evaluation
```

Hardware should follow this sequence.

The sequence should not be reversed simply because inexpensive radio boards are available.

---

# Step 1: Define the Resilience Use Case

Before selecting hardware, document the exact problem Phase 8 is intended to address.

Candidate use cases may include:

* maintaining limited project-to-project communication during an upstream internet outage;
* exchanging short messages among authorized pilot participants;
* testing whether low-power nodes can maintain a communications path between defined locations;
* sending infrastructure status information;
* evaluating a community-controlled communications technology;
* or demonstrating a technically independent communications layer.

The pilot should identify **one or more explicit testable use cases**.

For each use case, document:

* intended sender;
* intended recipient;
* message type;
* expected distance;
* required availability;
* expected frequency of use;
* device required by each participant;
* privacy considerations;
* and what constitutes success.

---

# Step 2: Define Who Would Actually Use the System

A communications network has little practical value if nobody expected to use it has access to compatible equipment or understands its purpose.

Phase 8 should identify potential user categories such as:

* Harmony for Hope project staff;
* Community Champions;
* technical testers;
* facility personnel;
* volunteers;
* partner organizations;
* or other specifically authorized pilot participants.

A public-facing use case should not be assumed merely because the underlying technology can support multiple users.

Document:

* who is part of the pilot;
* what device they would use;
* whether they require training;
* whether equipment is organization-owned or personally owned;
* how access is granted;
* and who supports users when the system does not work.

---

# Step 3: Define the Governance Boundary

Before deploying a shared radio or mesh environment, establish what the network is for and what it is not for.

The pilot should determine:

* who administers the configuration;
* who can add or authorize nodes;
* who may participate;
* what channel or logical network is used;
* whether the network is private, shared, or public;
* whether messages are encrypted by the selected system;
* how keys or credentials are managed where applicable;
* whether location information is enabled;
* whether messages are logged;
* how long any logs are retained;
* and how an individual or device is removed from the pilot.

The project should avoid collecting or transmitting sensitive information simply because the technology allows it.

---

# Step 4: Establish the Privacy Boundary

Low-bandwidth radio systems can still create privacy implications.

Depending on the selected system and configuration, information may include:

* node identifiers;
* message content;
* location;
* telemetry;
* timestamps;
* network relationships;
* device information;
* or other operational metadata.

Before field use, determine:

* which information is necessary;
* what should remain disabled;
* who can access message content;
* whether location sharing is appropriate;
* whether historical records are retained;
* and what participants should be told before using the system.

The controlling portfolio guidance is:

[Privacy and Data Stewardship Statement](../../07_privacy/Privacy_and_Data_Stewardship.md)

---

# Step 5: Evaluate Candidate Technologies

LoRa/Meshtastic remains a candidate architecture, but Phase 8 should not assume it is the only possible approach.

Evaluation criteria should include:

* independence from primary internet service;
* power consumption;
* achievable range;
* terrain;
* obstruction sensitivity;
* equipment availability;
* device cost;
* maintainability;
* firmware support;
* security;
* participant usability;
* interoperability;
* antenna requirements;
* power requirements;
* administrative complexity;
* and long-term support.

If Meshtastic is selected, the project should document **why it was selected**.

If another architecture performs better for the defined use case, the project should be free to use that instead.

---

# Step 6: Complete Radio and Technical Review

Before field deployment, the selected radio architecture should be reviewed against:

* the operating region;
* approved hardware;
* radio configuration;
* antenna compatibility;
* output and equipment limits;
* firmware settings;
* manufacturer documentation;
* site conditions;
* and applicable regulatory requirements.

This document intentionally does **not** establish a universal:

* frequency configuration;
* transmit-power setting;
* channel setting;
* antenna gain;
* antenna type;
* duty cycle;
* modem preset;
* or firmware configuration.

Those values depend on the actual approved system.

The final configuration should be documented in the technical record.

---

# Step 7: Bench-Test the Candidate Node

Before permanent installation, assemble and test the candidate system in a controlled environment.

The bench test should confirm, as applicable:

* device boots normally;
* firmware loads;
* configuration is retained;
* antenna system is appropriate;
* power consumption is understood;
* messages can be transmitted;
* messages can be received;
* intended security or encryption settings function;
* administration works;
* configuration can be backed up;
* device can recover after power loss;
* and firmware or configuration versions can be identified later.

### Evidence record

Capture:

* manufacturer;
* model;
* serial number where appropriate;
* firmware version;
* configuration version;
* antenna model;
* test date;
* power source;
* and test result.

Preconfiguration is useful.

But the goal is **reproducibility**, not merely convenience.

---

# Step 8: Conduct a Controlled Field Propagation Test

Before calling the Mount Hope installation a resilience node, test the actual radio path.

Use at least two compatible test endpoints where necessary to establish communication behavior.

Record:

* test locations;
* approximate distance;
* terrain;
* buildings or obstructions;
* antenna arrangement;
* weather if relevant;
* hardware;
* firmware;
* configuration;
* successful and failed messages;
* observed link information made available by the system;
* repeatability;
* and areas where communication fails.

Testing should answer:

> What can this system actually reach from this site?

It should not attempt to prove a desired range.

---

# Step 9: Evaluate Whether One Node Provides Meaningful Value

A single installed device is not automatically a mesh.

The project should determine whether:

* another compatible node is already reachable;
* a controlled second pilot node is required;
* multiple nodes are necessary to evaluate routing;
* existing community nodes are relevant;
* or the installation is functioning only as an isolated radio endpoint.

The repository should distinguish among:

```text id="6afg2j"
one configured node
        ↓
one reachable radio link
        ↓
multiple participating nodes
        ↓
demonstrated mesh routing
        ↓
operationally useful network
```

Those are different evidence stages.

---

# Step 10: Decide Whether Permanent Installation Is Justified

After bench and field testing, determine whether permanent installation adds enough value to proceed.

Possible decisions include:

### Proceed

Testing demonstrates enough utility to justify a permanent pilot node.

### Modify

The concept appears useful but requires:

* a different location;
* different antenna;
* different power architecture;
* another node;
* different hardware;
* or different configuration.

### Continue as temporary research

The technology is worth studying but permanent installation is premature.

### Do not deploy

Testing does not demonstrate sufficient value for the current Mount Hope scope.

A decision not to install is still a valid pilot result.

---

# Step 11: Finalize the Approved Hardware

If permanent installation proceeds, select the final hardware after testing.

Candidate devices may include hardware from the general classes previously considered, such as:

* LoRa-capable embedded devices;
* Meshtastic-compatible hardware;
* integrated outdoor nodes;
* or another approved low-power radio platform.

The final selection should account for:

* radio compatibility;
* environmental rating;
* antenna interface;
* power consumption;
* battery support;
* maintenance;
* firmware support;
* security;
* supply availability;
* price;
* and long-term replacement.

Previously named devices such as LILYGO or Heltec hardware may remain **planning references**, not mandatory procurement selections.

---

# Step 12: Finalize the Antenna System

The antenna should be selected as part of the final radio design.

The review should consider:

* operating band;
* equipment compatibility;
* antenna gain;
* polarization;
* placement;
* cable loss;
* connector type;
* weather protection;
* mounting;
* nearby structures;
* height;
* terrain;
* and applicable technical requirements.

The project should not assume that:

* an external antenna is always required;
* one antenna orientation is correct for every site;
* maximum possible range is the correct objective;
* or a particular connector arrangement is automatically appropriate.

The proper configuration is the one that safely and lawfully meets the pilot use case.

---

# Step 13: Finalize the Power Architecture

A resilience node requires a power strategy consistent with the resilience objective.

Candidate approaches may include:

* approved connection to the primary solar system;
* independent solar and battery power;
* building-supplied power with battery backup;
* integrated device battery;
* or another approved source.

The design should evaluate:

* actual measured load;
* required runtime;
* environmental conditions;
* battery characteristics;
* charging requirements;
* winter performance;
* maintenance;
* overcurrent protection;
* isolation;
* and whether independence from the primary system provides meaningful additional resilience.

This document intentionally does **not** prescribe:

* a 10–30 W solar panel;
* a 10–20 Ah battery;
* a particular controller;
* battery chemistry;
* wiring sequence;
* fuse rating;
* or fixed power topology.

Those decisions belong in the final power design and should remain consistent with the principles established in Phase 6.

---

# Step 14: Finalize the Outdoor Enclosure and Mount

If the node is installed outdoors, the enclosure and mounting approach should account for:

* precipitation;
* condensation;
* temperature;
* UV exposure;
* insects;
* corrosion;
* drainage;
* antenna connection;
* cable entry;
* vandalism;
* maintenance access;
* mounting loads;
* and equipment manufacturer requirements.

Communications equipment should be physically separated from other systems where separation improves:

* safety;
* maintenance;
* security;
* or serviceability.

However, this document does not prescribe one universal enclosure architecture.

---

# Step 15: Install the Approved Configuration

Permanent installation should proceed only after:

* use case approval;
* technical review;
* field testing;
* hardware selection;
* power design;
* mounting design;
* site permission;
* and governance configuration are complete.

Installation should follow:

* approved plans;
* manufacturer instructions;
* final hardware configuration;
* approved power architecture;
* antenna design;
* mounting requirements;
* and site-specific constraints.

Unapproved field substitutions should be documented and reviewed rather than improvised.

---

# Step 16: Commission the Node

Commissioning should establish what the installed system actually does.

Test, as applicable:

* startup;
* shutdown;
* recovery after power loss;
* message transmission;
* message reception;
* known-node communication;
* routing behavior where multiple nodes are available;
* power stability;
* battery operation;
* radio performance;
* configuration retention;
* administration;
* and security settings.

Commissioning should produce a repeatable test record.

---

# Step 17: Conduct a Controlled Resilience Exercise

If the objective of Phase 8 is to test independence from ordinary internet service, that independence should be demonstrated.

A controlled exercise may include:

1. establish normal operation;
2. confirm designated pilot devices can communicate;
3. intentionally remove or isolate the primary internet dependency where technically appropriate;
4. repeat the defined communications test;
5. observe what still functions;
6. restore normal service; and
7. document results.

The exercise should not interfere with unrelated public services.

The result should answer:

> What functionality remained available without the primary internet connection?

That is much more useful than simply saying the node is “backup communications.”

---

# What a Completed Phase 8 Should Mean

A correctly completed Phase 8 should mean that:

* a resilience use case was defined;
* intended users were identified;
* governance and privacy boundaries were documented;
* a candidate technology was evaluated;
* appropriate technical and radio review occurred;
* the system was bench-tested;
* actual field propagation was measured;
* permanent installation was justified by evidence;
* final hardware and power architecture were documented;
* the node was installed and commissioned;
* independence from the primary internet path was tested where relevant;
* limitations were documented;
* and evidence exists showing exactly what the system can and cannot do.

It should **not** mean merely that a LoRa board powers on.

---

# Evidence Classification

Phase 8 should preserve the distinction among:

| Evidence                                | What It Demonstrates                                                               |
| --------------------------------------- | ---------------------------------------------------------------------------------- |
| Device purchased                        | Hardware exists                                                                    |
| Firmware installed                      | Device software was prepared                                                       |
| Bench test passed                       | Device worked in controlled testing                                                |
| Two devices exchanged a message         | A radio link was demonstrated                                                      |
| Multiple nodes exchanged routed traffic | Mesh behavior was demonstrated under those conditions                              |
| Internet-independent test passed        | Defined functions operated without the primary internet path                       |
| Controlled exercise completed           | The pilot behavior was tested under a defined scenario                             |
| Long-term field record                  | Reliability evidence exists over time                                              |
| Partner agreement                       | Institutional role exists within the actual agreement                              |
| Public-safety integration               | Requires separate evidence and should never be inferred from ordinary mesh testing |

---

# Do Not Overstate Coverage

Radio range varies substantially with:

* terrain;
* antenna;
* height;
* obstructions;
* configuration;
* interference;
* hardware;
* weather;
* and receiving-node conditions.

The repository should therefore avoid statements such as:

> This node covers several miles.

unless actual testing demonstrates the supported area under documented conditions.

A better evidence statement is:

> During the Mount Hope test on [date], configuration [X] successfully exchanged messages between [documented locations].

That is reproducible evidence.

---

# Do Not Overstate Community Availability

A node may technically be reachable while still offering little practical public benefit.

Practical use depends on:

* compatible devices;
* participant awareness;
* training;
* configuration;
* governance;
* power;
* network availability;
* and operational support.

The project should therefore distinguish between:

```text id="nmbwce"
radio signal exists
        ≠
community communications capability
```

---

# Do Not Overstate Emergency Capability

The pilot should use terms such as:

* resilience experiment;
* low-bandwidth communications layer;
* backup communications research;
* independent communications path;
* mesh-network test;
* or radio resilience pilot

unless stronger claims are later supported.

Avoid representing the Mount Hope node as:

* emergency communications infrastructure;
* disaster-response communications;
* public-safety communications;
* 911 backup;
* first-responder communications;
* or guaranteed communications during emergencies

without the additional evidence and partnerships required for those claims.

---

# Risk and Learning Categories

## Radio-range risk

The actual range may be substantially different from theoretical expectations.

**Learning objective:** Map what the installed configuration actually reaches.

---

## Network-density risk

A mesh requires useful participating nodes.

**Learning objective:** Determine whether the Mount Hope environment has enough nodes or test endpoints to demonstrate meaningful mesh behavior.

---

## Power-dependency risk

A supposed backup layer may depend on the same power system as the primary infrastructure.

**Learning objective:** Determine whether power independence materially improves resilience.

---

## User-adoption risk

Compatible devices may not be widely available among intended participants.

**Learning objective:** Determine who can realistically use the system.

---

## Governance risk

A loosely governed shared communications environment can create confusion about:

* ownership;
* administration;
* privacy;
* responsibility;
* and appropriate use.

**Learning objective:** Establish a clear operating boundary before broadening participation.

---

## Security risk

Firmware, configuration, administrative access, credentials, and message protection require ongoing management.

**Learning objective:** Determine whether H4H can sustainably maintain the selected architecture.

---

## Environmental risk

Outdoor equipment may be affected by:

* water;
* temperature;
* battery limitations;
* corrosion;
* UV exposure;
* antenna damage;
* wildlife;
* and physical movement.

**Learning objective:** Track actual field performance rather than assuming outdoor reliability.

---

# What to Record When Phase 8 Is Complete

## Use-case record

Document:

* resilience problem being tested;
* intended participants;
* allowed use;
* prohibited or unsupported use;
* and defined success criteria.

---

## Hardware record

Record:

* manufacturer;
* model;
* serial number where appropriate;
* radio hardware;
* antenna;
* enclosure;
* power system;
* installation date;
* and responsible maintainer.

---

## Software and configuration record

Maintain:

* firmware version;
* configuration version;
* logical node identifier;
* relevant radio configuration;
* security configuration;
* update method;
* backup configuration;
* and administrator.

Sensitive keys or credentials should not be committed to the public repository.

---

## Bench-test record

Document:

* date;
* devices tested;
* test messages;
* startup behavior;
* recovery behavior;
* configuration persistence;
* and test result.

---

## Propagation-test record

Document:

* locations;
* approximate distances;
* terrain;
* obstructions;
* hardware;
* antenna arrangement;
* successful exchanges;
* failed exchanges;
* and repeatability.

---

## Installation record

Capture:

* approved installation location;
* node placement;
* enclosure;
* antenna placement;
* power architecture;
* photographs appropriate for release;
* and deviations.

Security-sensitive infrastructure details may remain internal.

---

## Commissioning record

Document:

* commissioning date;
* defined tests;
* result;
* participating nodes;
* internet-dependent functions;
* internet-independent functions;
* faults;
* corrections;
* and final pilot status.

---

# Mount Hope Pilot Learning Questions

After sufficient testing, Phase 8 should be able to answer:

* What resilience problem were we actually trying to solve?
* Did LoRa/Meshtastic prove suitable?
* What alternatives were considered?
* What range was actually demonstrated?
* Which locations were reachable?
* Which were not?
* Did terrain matter?
* Did buildings matter?
* Did antenna placement materially change performance?
* Was one node useful?
* How many nodes were needed to demonstrate actual mesh behavior?
* Did the system work when the primary internet connection was unavailable?
* How long could the node operate from its selected power source?
* Did independent power materially improve resilience?
* Who actually used the system?
* Did participants understand it?
* Was configuration maintenance manageable?
* Were updates manageable?
* Did privacy settings prove adequate?
* Did any security concerns appear?
* What did the system cost to install and maintain?
* What should be standardized?
* What should remain site-specific?
* Does the resilience value justify replication?

Those answers should determine whether the architecture moves forward.

---

# Relationship to the Mount Hope First Phase

Phase 8 is part of the **Mount Hope evidence-building process**.

Its purpose is not to prove that Harmony for Hope already operates a regional communications mesh.

Its purpose is to test whether a governed, independent, low-bandwidth layer has enough real utility to become part of the broader model.

The evidence sequence is:

```text id="7q0f8k"
hypothesis
    ↓
bench test
    ↓
field test
    ↓
installation decision
    ↓
commissioning
    ↓
resilience exercise
    ↓
operating evidence
    ↓
replication decision
```

That sequence is consistent with the portfolio's larger principle:

> proposed capability does not become demonstrated capability merely because hardware exists.

---

# Relationship to Future Sites

If Mount Hope produces useful evidence, the results may inform later deployments.

A future site should still evaluate:

* use case;
* terrain;
* distance;
* local participants;
* available nodes;
* institutional partners;
* power;
* governance;
* privacy;
* security;
* and actual field performance.

Mount Hope's configuration should not simply be copied.

---

# Thurmond Boundary

Thurmond remains a **future federal-phase implementation opportunity**.

Any future radio or mesh deployment at Thurmond would require its own:

* defined federal project purpose;
* funding;
* National Park Service review;
* site-specific authorization;
* preservation and cultural-resource review where applicable;
* technical and radio review;
* equipment approval;
* privacy and information-governance review;
* cybersecurity review;
* power design;
* antenna and mounting review;
* operating responsibility;
* and final agreements.

A successful Mount Hope experiment may provide useful evidence for those discussions.

It does not authorize a Thurmond deployment.

---

## Phase 8 Completion Boundary

Phase 8 should be considered complete only when the proposed Mount Hope resilience layer has been:

```text id="ke6dcs"
defined
    ↓
evaluated
    ↓
tested
    ↓
reviewed
    ↓
installed if justified
    ↓
commissioned
    ↓
exercised
    ↓
documented
```

A configured node is not a mesh.

A mesh is not automatically a community communications system.

A community communications system is not automatically emergency infrastructure.

The purpose of Phase 8 is to determine, with evidence, **what resilience value this technology actually provides**.

---

*Harmony for Hope, Inc. — New River Gorge Safety & Heritage Mesh Pilot*
*Phase 8 | Mount Hope Resilient Low-Bandwidth Communications Planning Guide*
