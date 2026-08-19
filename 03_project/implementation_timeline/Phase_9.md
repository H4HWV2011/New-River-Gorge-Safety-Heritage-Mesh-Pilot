# Phase 9: Connect Power and Network
## Field Learning Guide — Mount Hope Walking Trail Pilot Site

---

## What This Document Is For

This document expands on Phase 9 of the installation workflow. It explains what happens in this phase, why it happens in the specific sequence described, what each connection accomplishes, and what a correctly completed phase looks like. It also explains what can go wrong and how to recognize it before Phase 10 testing begins. As a pilot site document, it is written to serve as a learning reference for H4H and future crews at other locations.

---

## What Phase 9 Is and Why It Exists as Its Own Phase

Phases 5 through 8 installed hardware. Every device is now physically mounted in its correct location. Phase 9 is the phase where those devices become a connected system.

The reason Phase 9 is separated from the installation phases rather than performed inline as each device is mounted is that finalizing all connections at once — after all hardware is confirmed in place — allows the crew to verify the complete circuit before power is applied to anything. This prevents a common class of field error in which a device is connected and powered on before the downstream equipment it depends on is ready, causing startup failures that can look like hardware defects but are actually sequencing errors.

It also concentrates the connection work into a single focused review. Each connection made in isolation during installation may seem fine. The complete picture — every cable, every terminal, every gland, every strain relief point — is only visible when viewed as a system. Phase 9 is when that system-level review happens.

---

## What This Phase Covers

Phase 9 finalizes and confirms the following connections:

- Indoor equipment to power and UPS (Starlink, router, switch, mini PC).
- Outdoor kiosk equipment to its power source (Raspberry Pi power supply to the solar system or the indoor power circuit).
- All internet and local network lines between the indoor equipment and the kiosk Pi.
- Cable strain relief and weather sealing at every outdoor connection point.
- Wire protection for any exposed wiring at all locations.

---

## The Connection Sequence and the Reason for It

### Group 1: Indoor power connections

**What to do:** Starting at the UPS, confirm the UPS is not yet plugged into wall power. Working from the UPS outward, connect the following in order:

1. Surge protector to the UPS battery-backed outlets.
2. Starlink power supply to the surge protector.
3. Router power supply to the surge protector.
4. Network switch power supply to the surge protector.
5. Mini PC power supply to the surge protector.

Once all connections are made, plug the UPS into the wall outlet.

**Why this specific order within the indoor group:** The UPS is the source of protected power for all indoor equipment. Connecting equipment to the UPS while the UPS is unplugged prevents any device from accidentally powering on during the connection process due to residual charge or contact voltage. All downstream connections are made first. The UPS connects to wall power last, at which point the sequence is controlled and deliberate.

**Why the surge protector sits between the UPS and the equipment:** A UPS provides battery backup and voltage regulation. A surge protector adds a secondary layer of transient protection for equipment connected to it. Stacking these two layers of protection is correct for this installation because the UPS's own surge rating covers large events, while the surge protector catches smaller transient spikes that may pass through the UPS's regulation circuit.

**A note on the UPS specifically:** Do not plug the UPS into a surge protector instead of directly into the wall outlet. UPS units use battery management circuits that detect the quality of incoming power and switch to battery when the power falls outside normal range. A surge protector between the wall outlet and the UPS can cause the UPS to interpret the protector's voltage clamping behavior as a power quality event and switch to battery unnecessarily. The UPS goes directly into the wall outlet. Devices connect to the UPS.

**What to check before moving on:** All indoor devices are connected but not yet powered on. The UPS is connected to wall power and its indicator shows it is online. No devices are switched on at this step.

---

### Group 2: Outdoor power connections

**What to do:** At the solar system enclosure, confirm the following terminal connections are made correctly:

- Solar panel positive and negative to the charge controller PV input terminals.
- Charge controller battery output to the fuse block input (positive) and common negative bus (negative).
- Fuse block output to battery positive terminal.
- Battery negative terminal to common negative bus.

At the kiosk enclosure, confirm the Raspberry Pi power supply is connected to the outdoor power cable. Confirm the outdoor power cable is connected to the appropriate power output from the solar system.

At the LoRa node enclosure, confirm the node's power input is connected to its power source — either the main solar system or the dedicated small solar kit.

**Why review these connections now even though they were made in earlier phases:** Connections made during installation in Phases 6, 7, and 8 were made one at a time as hardware was mounted. By the time Phase 9 begins, it has been hours since some of those connections were made. Tools, cables, and materials have moved through the work area. This review catches anything that may have been displaced, disconnected accidentally, or connected incorrectly in the course of the installation work.

**What to look for during the review:**

- Positive and negative terminals correctly matched — red to positive, black to negative, consistently throughout the system.
- No terminal connections that are finger-tight but not mechanically secure. Every terminal should require deliberate effort to release.
- No wires where the insulation has been stripped back so far that bare conductor is exposed beyond the terminal block.
- No wires under mechanical stress at the point of connection — the wire should curve gently into the terminal, not pull straight and tight.
- Fuse is present and correctly rated in the fuse block.

**Why polarity is listed explicitly:** A DC system wired with reversed polarity at one or more connections will damage or destroy connected electronics. The charge controller, the Raspberry Pi power supply, and the LoRa node all have polarity-sensitive inputs. A reversed connection may produce no visible sign of a problem until power is applied, at which point the damage is instantaneous. Verify polarity at every connection point before power is applied.

**What to check before moving on:** All outdoor power connections are confirmed correct and mechanically secure. The fuse is in place. The system has not been powered on yet.

---

### Group 3: Internet and local network connections

**What to do:** Confirm all Ethernet connections between the indoor network equipment and any outdoor equipment that receives network service via cable:

- Starlink router to the network switch (via the router's LAN port or the switch's uplink port).
- Network switch to the mini PC (via a switch port and the mini PC's Ethernet port).
- Network switch or router to the outdoor cable run toward the kiosk, if the kiosk Pi receives a wired connection.
- At the kiosk, the outdoor Ethernet cable to the Raspberry Pi's Ethernet port.

For any wireless network connections — such as the kiosk Pi connecting to the indoor network wirelessly — confirm that the Pi's wireless configuration is correct by verifying the network name and password match what was configured on the indoor router or access point.

**Why network connections come after power connections in the sequence:** A network device that is connected to the network but not yet connected to power is harmless — it simply does not communicate. A power device that is connected to power but not to the network will either sit idle or attempt to operate without the connection it needs, potentially entering a fault or retry loop that complicates the startup sequence. Power infrastructure is confirmed first; then network connections are finalized.

**Why cable routing matters for Ethernet connections:** Ethernet cable that is sharply bent, kinked, or compressed at any point along its run may function at reduced performance or intermittently. The category rating of Ethernet cable (CAT6 in this installation) specifies a minimum bend radius — typically four times the outer diameter of the cable. A cable sharply bent beyond that radius may still transmit, but at reduced speeds or with increased error rates that only appear under heavy traffic. Route cables along gentle curves and avoid sharp corners without the use of appropriate conduit elbows or right-angle adapters.

**What to check before moving on:** All Ethernet cables are connected at both ends and run without sharp bends or kinks. Any outdoor Ethernet cable has been routed through its cable gland and the gland is tightened. Any indoor Ethernet cable is secured along its run without pinch points.

---

### Group 4: Confirm cable strain relief and weather sealing

**What to do:** Walk through all four installation locations in sequence — the indoor building point, the solar hardware location, the kiosk, and the LoRa node — and perform the following check at each:

**At each cable-to-device connection point:**

Pull gently on the cable at the point where it enters the device or enclosure. It should not move. If it moves, the cable is not secured with adequate strain relief and the connection is at risk of pulling loose under the mechanical stress of weather, thermal expansion, or incidental contact.

**At each enclosure with cable glands:**

Confirm the gland nut is tightened against the cable jacket. The cable should not rotate or slide when twisted or pulled. If it does, tighten the gland. Recheck after tightening.

**At each outdoor penetration point:**

Confirm outdoor sealant has been applied to any cable entry that is not fully sealed by a gland alone. This includes any point where a cable exits through a hole in wood, metal, or an enclosure wall that does not have a gland installed. The sealant should form a continuous bead around the full perimeter of the cable at the penetration point.

**Why strain relief is listed separately rather than assumed to be part of the connection steps:** Strain relief is consistently the most frequently missed step in field installations of this type. It is invisible once cable management covers are installed, it does not affect performance at the moment of testing, and its importance is only apparent when a cable fails — which may not happen for months or years. By making strain relief confirmation its own explicit step in Phase 9, this workflow ensures it is checked deliberately rather than assumed to have been done.

**Why weather sealing is re-confirmed here even though it was addressed in earlier phases:** Each earlier phase sealed its own enclosures and penetrations in the context of that phase's work. By the time Phase 9 is reached, all of those seals have been made in isolation and may not have been cross-checked. This phase is the first time the full system can be reviewed as a complete installation. A seal that looked complete in Phase 6 may have been disturbed by subsequent work in Phase 7 or 8. The Phase 9 review catches that.

**What to check before moving on:** Every cable at every location is strain-relieved so that it cannot be dislodged by mechanical stress. Every outdoor cable entry point is sealed against water infiltration. No cable hangs freely at any transition between protected and unprotected environments.

---

### Group 5: Confirm all exposed wiring is protected

**What to do:** Walk the full installation from indoors to the furthest outdoor point and identify any section of cable or wire that is:

- Running along a surface without being secured to it.
- Exposed to potential physical contact in a public area.
- Crossing a transition from protected to unprotected environment without appropriate conduit, gland, or housing.
- Subject to UV exposure without UV-rated jacketing or conduit protection.
- Within reach of where pedestrian traffic, maintenance equipment, or wildlife could contact it.

Address each identified issue before moving to Phase 10. This may mean adding cable ties or clips, adding a section of conduit, or applying additional sealant at a penetration point.

**Why this walkthrough happens here:** Phases 5 through 8 each addressed exposed wiring within their own scope. Phase 9 is the first time the complete installation can be viewed as a single cable system. Problems that exist at the boundary between two phases — a wire that leaves one phase's protected run and enters another phase's territory without adequate protection — are only visible when the whole run is examined from end to end.

**What counts as adequately protected:** A cable is adequately protected when it cannot be dislodged by normal forces in the environment where it is installed, its insulation is protected from UV and abrasion along its full length, it cannot be contacted by pedestrian traffic or maintenance equipment, and any penetration through a structural element is sealed against water infiltration.

**What to check before moving on:** The complete installation has been walked from the indoor equipment point to each outdoor device. Every cable is secured, protected from environmental exposure, and sealed at every penetration point. No cable requires additional work.

---

## What a Correctly Completed Phase 9 Looks Like

At the conclusion of Phase 9, the installation is in the following state:

- All indoor equipment is connected to power through the UPS and surge protector, but the UPS has not yet been switched on.
- All outdoor equipment is connected to the solar power system with correct polarity, mechanical security at every terminal, and a correctly rated fuse in the circuit.
- All Ethernet network cables are connected at both ends, routed without sharp bends, and secured along their runs.
- Every cable entering an outdoor enclosure passes through a sealed cable gland or a sealed penetration.
- Every outdoor cable run is secured to a surface and protected along its full length.
- No terminal is under mechanical stress. No cable hangs freely. No penetration is unsealed.

Nothing is powered on yet. Phase 10 powers on and tests the system. Phase 9 confirms the system is ready to be powered on safely.

---

## What Happens If This Phase Is Rushed or Performed Out of Sequence

**Powering on during connection work:** When devices are powered on while other connections are still being made, the risk of a short circuit from a tool or a momentarily exposed conductor is highest. A short circuit at a powered terminal can damage the connected equipment, trip a breaker, or in a DC system without a fuse, cause a fire. Phase 9 keeps everything unpowered until all connections are confirmed correct.

**Polarity not verified:** A reversed polarity connection in a DC system that is not caught before power is applied destroys the connected device. The failure is immediate and silent — the device simply does not work and does not show any sign of damage from the outside. Identifying reversed polarity after the fact requires disconnecting the device, testing the circuit, correcting the wiring, and replacing the damaged component. The replacement cost and return trip time are entirely avoidable by verifying polarity during Phase 9.

**Strain relief skipped:** A cable that is not strain-relieved at its connection point will eventually pull loose. In an indoor environment, this typically happens when the cable is accidentally stepped on or caught on equipment. In an outdoor environment, it happens from thermal cycling — cables expand and contract with temperature changes, and over dozens of cycles the motion at an unsecured termination point is enough to work the connector loose. This failure is invisible until the device loses connectivity or power, and diagnosing it requires a physical inspection of every connection point.

**Weather sealing incomplete:** Water infiltration at an incompletely sealed enclosure entry point does not cause an immediate failure. It causes a gradual failure — increased connector resistance, intermittent contact, and eventually corrosion of the terminal itself. The failure timeline depends on rainfall, humidity, and the size of the gap, but in Fayette County's climate, damage from water infiltration can be expected within one to two years if the sealing is inadequate. The repair cost is always higher than the sealing cost.

**Outdoor cable not UV-rated:** Standard Ethernet cable and power cable using PVC insulation not rated for UV exposure will begin to degrade in direct sunlight within one to two seasons. The insulation becomes brittle, develops micro-cracks, and eventually loses its dielectric and mechanical properties. The cable appears intact from a distance but is physically compromised. Replacing outdoor cable runs requires reopening enclosures, pulling cables, and re-routing — a full day of labor that could have been avoided by using UV-rated jacketing at the time of installation.

---

## What to Record When Phase 9 Is Complete

Before beginning Phase 10, record the following:

- Confirmation that polarity was verified at all DC connection points. Note who performed the verification.
- Confirmation that strain relief was checked at all connection points. Note who performed the check.
- Confirmation that all outdoor cable entry points are sealed. Note who performed the check.
- Note of any connection point that required adjustment or rework during Phase 9, and what was done.
- Note of any outdoor cable section that required additional protection and what was added.
- Photograph of the indoor equipment area showing all cables connected and routed.
- Photograph of the solar enclosure interior showing wiring, terminals, and fuse block.
- Photograph of any connection point that required rework, showing the corrected state.

These records close out the physical installation. Phase 10 begins with the system in a confirmed-ready state.

---

## Carrying These Lessons Forward

At future sites, the core lessons from this phase are:

1. All power connections are made before power is applied to anything. This prevents short circuit risk during connection work.
2. Polarity in DC systems is not assumed to be correct. It is verified at every terminal before power is applied.
3. The UPS connects directly to the wall outlet. Equipment connects to the UPS. Do not put a surge protector between the wall and the UPS.
4. Strain relief is not cosmetic. It is the mechanical protection that keeps a connection from being pulled loose over months of thermal cycling, weather movement, and incidental contact.
5. Weather sealing is confirmed as a complete system, not assumed to be complete because each phase addressed it in isolation.
6. The Phase 9 walkthrough is the last opportunity to catch problems before the system is powered on. A problem found here costs minutes to fix. A problem found during Phase 10 testing may cost hours.
7. UV-rated cable jacketing for all outdoor runs is not optional in an installation that is expected to last more than two seasons.
