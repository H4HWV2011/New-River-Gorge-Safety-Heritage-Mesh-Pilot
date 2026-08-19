# Phase 8: Install Backup Communications Node
## Field Learning Guide — Mount Hope Walking Trail Pilot Site

---

## What This Document Is For

This document expands on Phase 8 of the installation workflow. It explains what the LoRa backup communications node is, why it is part of this installation at all, how it is installed, what can go wrong, and what a correctly completed installation looks like. As a pilot site document, it also captures the reasoning behind decisions made here so H4H and future crews can apply those lessons to other sites.

---

## What Is a LoRa Node and Why Does This Installation Include One

LoRa stands for Long Range. It is a radio communication technology that transmits small amounts of data over distances of one to several miles using very low power. It is not a replacement for internet access and cannot carry the data volume needed for general web browsing. What it can do is carry short messages — notifications, status updates, basic location information, emergency signals — between nodes in a network, even when the primary internet connection is unavailable.

In the context of this installation, the LoRa node serves as a resilience layer. When the Starlink internet connection is functioning normally, the LoRa node is a secondary system running quietly in the background. If the primary internet goes down — due to a power outage, a hardware failure, a service interruption, or a weather event — the LoRa network remains active as long as battery power holds. Community members with compatible devices can use the LoRa mesh network for basic communications even when conventional connectivity is unavailable.

For a community organization serving rural Appalachian residents, where cellular coverage can be limited and where power outages during severe weather are not rare, this backup layer has practical value that is distinct from what the main hotspot provides.

The Meshtastic protocol is the software layer used on these devices. Meshtastic is open-source, actively maintained, and designed specifically for LoRa mesh networking at the community scale. The LILYGO T-Beam or Heltec LoRa32 class devices supported by Meshtastic are the hardware used in this installation.

---

## What Phase 8 Covers

The equipment installed in this phase:

- LoRa node device (LILYGO T-Beam or Heltec LoRa32 class)
- LoRa antenna (external, matched to the node's frequency band)
- Small solar support kit for the node (panel, small charge controller, and small battery if separate from the main solar system)
- Weatherproof enclosure for the node (Sixfab or equivalent small outdoor enclosure)
- Pole clamps or mount straps to attach the enclosure to the support structure

---

## Before Phase 8 Begins: What Must Already Be True

Phase 8 can begin after Phase 6 (solar infrastructure) is complete and confirmed. The LoRa node does not depend on the main internet connection — it is intentionally independent. However, it does depend on power. If the node is drawing from the main solar system, that system must be confirmed operational before the node is connected to it. If the node has its own dedicated small solar kit, that kit is installed as part of this phase.

The main outdoor hardware — the frame, the weatherproof electronics enclosure, the solar panel — should already be in place. The LoRa node typically mounts on the same pole or frame, below or beside the main enclosure, and shares the mounting structure. Attempting to mount the LoRa node before the main frame is in place creates a sequencing problem where the crew is working around uninstalled primary hardware.

---

## The Step Sequence and the Reason for Each Step

### Step 1: Confirm the flash and configuration of the LoRa node before arrival

**What to do:** Before the site visit, confirm that the LoRa node device has been flashed with the correct Meshtastic firmware version and configured with the correct channel settings, region code (US for this installation), and node name. This is a software step that should happen at a desk, not in the field.

**Why pre-configuration matters:** A LoRa node that arrives on site without firmware is hardware, not a communications device. Flashing firmware and configuring the device in the field requires a laptop, a USB cable, and time. It also introduces risk — if something goes wrong during flashing (an interrupted connection, a wrong firmware file), the device may need to be recovered, which requires additional tools and technical knowledge. Pre-configuring the device eliminates that risk from the field installation entirely.

**Minimum configuration to verify before the site visit:**

- Firmware: Meshtastic, correct version for the specific hardware.
- Region: US (required by FCC regulations for the correct frequency band).
- Node name: Something identifiable to H4H's network — for example, MHHWT-01 for Mount Hope Historic Walking Trail node 1.
- Channel: Match the channel configuration used by any other nodes H4H has deployed or plans to deploy, so this node can communicate with them.

**Lesson for future sites:** At this pilot site, document the firmware version, the channel configuration, and the node name in H4H's records. Every additional node deployed at future sites should use the same channel configuration so that the network operates as a mesh rather than a collection of isolated devices.

---

### Step 2: Attach the antenna to the node

**What to do:** Connect the external LoRa antenna to the node's SMA antenna connector before the node is placed inside the enclosure. Hand-tighten the SMA connector — do not use tools, which can overtighten and damage the connector threads. Verify the antenna is the correct type for the node's frequency band. In the United States, Meshtastic operates on 915 MHz. The antenna must be rated for 915 MHz. An antenna rated for a different frequency (such as 433 MHz or 2.4 GHz) will significantly reduce the node's range.

**Why the antenna connects before the node is enclosed:** Once the node is inside the enclosure with the antenna exiting through a cable gland or connector port, adjusting the antenna connector requires reopening the enclosure. Connecting the antenna outside the enclosure, confirming it is seated correctly, and then placing the node inside avoids that extra step.

**Why antenna selection matters:** A LoRa node running without an antenna, or with an incorrectly matched antenna, transmits and receives at a fraction of its rated capability. In a mesh network, a node with poor antenna performance may not be able to reach other nodes in the network, rendering it ineffective as a relay. At this site, the goal is to create a node that can reach other H4H nodes in the surrounding area and potentially link to the regional Meshtastic mesh. Antenna selection is not a detail — it is a primary factor in whether the node serves its purpose.

**Note on antenna placement inside versus outside the enclosure:** Some LoRa node builds use a small antenna inside the enclosure. This works at short ranges but significantly reduces performance for a node intended to serve as a community mesh relay. At this installation, the antenna should exit the enclosure through a weatherproof SMA bulkhead connector or a sealed antenna port so that the antenna is outside the enclosure and in clear air.

---

### Step 3: Prepare the weatherproof enclosure for the node

**What to do:** Install a bulkhead SMA connector in the enclosure wall at the point where the antenna cable will exit. Seal around the bulkhead fitting with outdoor sealant. Install cable glands for any power cables entering the enclosure. Confirm the inside of the enclosure has mounting provisions for the node — standoffs, a DIN rail, or a mounting plate.

**Why a bulkhead SMA connector rather than running the antenna cable through a gland:** An SMA antenna cable routed through a cable gland compresses the cable jacket but may not seal cleanly around the connector body. A bulkhead SMA connector mounted in the enclosure wall creates a sealed pass-through that the antenna screws onto directly on the outside, with the corresponding internal connector secured to the node. This is the standard practice for weatherproof enclosures housing antenna-connected devices.

**Why not use the same enclosure as the main solar electronics:** The LoRa node and the main solar electronics (charge controller, fuse block, wiring terminals) serve different functions and have different maintenance access patterns. Placing them in the same enclosure means opening the solar electronics enclosure to service the communications node, which introduces unnecessary exposure risk to the wiring. Separate enclosures are the correct approach for this installation size.

**What to check before moving on:** The bulkhead SMA connector is installed and sealed. Cable glands for power are in place. The inside of the enclosure has a solid mounting surface for the node.

---

### Step 4: Mount the node inside the enclosure

**What to do:** Place the LoRa node inside the enclosure and secure it to the mounting surface using standoffs or the appropriate fasteners for the enclosure design. Connect the internal SMA cable from the node's antenna connector to the inside of the bulkhead SMA connector. Connect the power cable from the enclosure entry gland to the node's power input.

**Powering the node:** The LoRa node requires 5V DC power. This can be provided by a USB power adapter connected to the solar system's AC output (if an inverter is used), by a dedicated 5V DC step-down converter connected to the 12V battery system, or by the node's onboard battery if it has one (the LILYGO T-Beam has an onboard 18650 battery slot). For a permanent outdoor installation, powering from the solar system is preferable to relying on the onboard battery, which has limited capacity.

**Why the onboard battery is not sufficient alone:** The LILYGO T-Beam's onboard 18650 cell provides enough power for portable or temporary use — hours to a day of operation. For a permanent installation intended to provide backup communications during multi-day power outages, the node must be connected to the main solar battery system or its own dedicated solar kit with sufficient capacity to sustain operation through cloudy periods.

**What to check before moving on:** The node is secured inside the enclosure, the antenna connection is made, and the power connection is made. The enclosure is not yet closed.

---

### Step 5: Install the small solar support kit if separate from the main system

**What to do:** If the LoRa node is powered by its own dedicated small solar kit rather than the main solar system, install that kit now. A typical small solar kit for a LoRa node consists of a 10W to 30W panel, a small PWM or MPPT charge controller, and a small LiFePO4 battery (10Ah to 20Ah is typically sufficient for a LoRa node's power draw).

Mount the panel on the same support frame as the main panel, oriented in the same direction (south-facing at the correct tilt angle). Wire the kit using the same principles applied in Phase 6: fuse between battery and controller, battery connected before panel, weatherproof enclosure for the charge controller and battery.

**Why a separate small kit might be used instead of drawing from the main system:** Drawing the LoRa node's power from the main solar system simplifies the installation but creates a dependency. If the main solar system requires service or experiences a fault, the LoRa node loses power at the same time as the main equipment. A dedicated small kit for the node means the backup communications layer remains independent of the main system — which is the point of having a backup communications layer.

**The tradeoff:** A separate kit adds cost, adds hardware to install and maintain, and adds complexity to the power architecture. At this pilot site, H4H should document which approach was used and whether the independent power architecture justified the additional complexity. That evaluation informs the decision at future sites.

---

### Step 6: Mount the enclosure on the pole or structure

**What to do:** Attach the node enclosure to the support pole or frame using pole clamps or mount straps. Position the enclosure so that:

- The antenna, once connected on the outside, points upward or at a slight angle — vertical orientation is standard for omnidirectional LoRa antennas.
- The enclosure door faces a direction that allows it to be opened without obstruction.
- The enclosure is high enough off the ground that it is not subject to direct water splash from rainfall at the base.
- The power cable entry is not facing upward.

Tighten the pole clamps or straps firmly. Use stainless steel straps or clamps rather than galvanized, as the Appalachian humidity and rainfall will corrode galvanized hardware within a few seasons.

**Why antenna vertical orientation:** LoRa antennas in omnidirectional configurations transmit and receive best when the antenna element is vertical. Tilting the antenna significantly reduces performance in one or more directions. At this site, the goal is to reach nodes in multiple directions — toward Mount Hope, toward other potential H4H sites in the region, and toward any community members who may have compatible handheld devices. Vertical orientation serves all of those directions equally.

**What to check before moving on:** The enclosure is solidly mounted, the antenna is pointing upward or is in the correct orientation for the antenna type, and the enclosure door opens without obstruction.

---

### Step 7: Connect the external antenna, seal the enclosure, and close up

**What to do:** 

1. Screw the external LoRa antenna onto the outside of the bulkhead SMA connector. Hand-tighten only.
2. Verify all cable glands are tightened against their respective cable jackets.
3. Apply outdoor sealant to any entry point that is not fully sealed by the gland.
4. Close the enclosure door and confirm it latches.
5. Apply a small amount of outdoor sealant around the bulkhead SMA fitting where it meets the enclosure wall, to reinforce the weather seal at that point.

**Why the antenna is the last thing connected before closing:** The antenna connector is the most mechanically exposed part of this assembly. Connecting it last, after everything inside is secured, means there is no risk of bumping or stressing the connector during the installation of other components. Once the antenna is on and the enclosure is closed, the assembly is complete.

**What to check before moving on:** The enclosure is closed and latched. The antenna is secured and upright. All cable entry points are sealed. The power cable and any network cables exit the enclosure cleanly with no sharp bends at the gland.

---

### Step 8: Confirm physical security of the full assembly

**What to do:** With all hardware installed and sealed, perform a final physical check:

- Push and pull the enclosure. It should not move on the pole.
- Push and pull the pole. It should not move in its mount or anchoring.
- Pull lightly on the antenna. It should not rotate or pull away from the connector.
- Pull lightly on the power cable at the enclosure entry. It should not move inside the gland.

**Why this check:** A loose connection that is identified before Phase 10 testing can be tightened in seconds. A loose connection discovered after a failure — or not discovered at all until a field maintenance visit months later — requires a return trip and potential downtime of the backup communications system.

---

## What a Correctly Completed Phase 8 Looks Like

The LoRa node enclosure is mounted solidly on the support structure. The antenna is pointing upward, external to the enclosure, with no kinks in any coaxial cable between the node and the antenna. The enclosure is latched and sealed at all cable entry points. Power is connected to the node. The assembly does not shift when pushed. No wires hang freely from any connection point.

At this point the node has not been powered on yet — that happens in Phase 10 as part of the full system test sequence.

---

## What Happens If This Phase Is Rushed or Skipped in Part

**Antenna not pre-matched to frequency:** A LoRa node installed with a 2.4 GHz antenna (a common mismatch when antenna types are mixed up in a parts bin) operates at severely reduced range — sometimes less than 100 meters versus the 1–5 kilometer range the hardware is capable of. The node appears to be working because it powers on and transmits, but it cannot reach other nodes in the network. Diagnosing this requires RF testing equipment or a second node within short range for comparison.

**Firmware not pre-loaded:** A node installed without firmware will power on but transmit nothing useful. Discovering this during Phase 10 requires either flashing the device in the field (possible but slow and technically demanding) or removing the node, returning it to a desk environment for flashing, and reinstalling. This is a full return trip that could have been avoided by pre-configuring the device before the site visit.

**Enclosure not sealed at the SMA bulkhead:** Moisture infiltration through the SMA bulkhead pass-through corrodes the connector over months. The corrosion increases resistance at the antenna connection, reducing transmitted power and received sensitivity. The failure is gradual and shows up as declining network range rather than a complete failure, making it harder to diagnose without physically inspecting the connection.

**Node powered from onboard battery only:** A node relying only on the onboard 18650 battery will operate for hours to a day without sun. During extended overcast or winter conditions in West Virginia — where multiple consecutive cloudy days are common — the battery depletes and the backup communications layer goes offline exactly when it is most likely to be needed: during weather events.

---

## What to Record When Phase 8 Is Complete

Before moving to Phase 9, record and photograph the following:

- LoRa node model and serial number.
- Meshtastic firmware version loaded on the node.
- Node name and channel configuration.
- Antenna model and frequency rating.
- Photograph of the node inside the open enclosure before closing.
- Photograph of the sealed and closed enclosure with antenna in place.
- Photograph of the full assembly on the pole.
- Power architecture used: main solar system tap or dedicated small solar kit.
- Note of any deviation from the planned installation and the reason for it.

---

## Carrying These Lessons Forward

At future sites, the core lessons from this phase are:

1. The LoRa node must be flashed and configured before the site visit. There is no field shortcut that is as reliable as desk preparation.
2. Antenna type must match the node's operating frequency. Confirm this before the site visit, not during.
3. The antenna belongs outside the enclosure for a mesh relay node. Internal antenna installations are for short-range applications.
4. The node needs reliable power from the solar system, not just from an onboard battery, for a permanent installation.
5. The backup communications layer is most valuable precisely when other systems are failing. Power architecture that makes the node independent of the main system preserves that value.
6. Documenting firmware version and channel configuration at each site is the foundation for building a regional mesh over time. Without consistent records, the network cannot be managed as a network.
