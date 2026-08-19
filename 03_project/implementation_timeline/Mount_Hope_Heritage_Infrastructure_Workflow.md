# Installation Workflow for Crew

## Purpose

This document is a field guide for the crew installing the public equipment at 704 Main Street and the Mount Hope walking trail kiosk location. It explains what equipment is being installed, how materials are staged, the order of work, what must be tested, and what must be documented before the installation is complete.

Every phase in this guide includes a reason for the steps described. That reason is there so crew members understand the thinking behind the work — not to invite debate in the field. If something in this guide does not make sense or seems wrong for site conditions, stop and bring the question back to H4H before making a decision independently. On-the-fly changes that seem reasonable in the moment have a history of creating problems that are harder to fix after the fact.

---

## Project Scope

This installation covers equipment located at 704 Main Street and the public kiosk location serving the Mount Hope walking trail. The installed system includes an indoor internet and equipment point at 704 Main Street and an outdoor public-use location with its own power and communications hardware.

---

## Equipment Covered by This Workflow

The crew should plan around the following equipment groups:

- Starlink internet hardware for the main building.
- Local network equipment for distribution at the main building.
- One small edge computer or mini PC at the main building.
- One existing outdoor kiosk location used as a hotspot point.
- One outdoor Starlink receiver point with solar power support.
- One LoRa backup communications node with solar support.
- Supporting parts such as brackets, enclosures, poles, cable runs, anchors, conduit, weather protection, and power accessories.

---

## Responsibilities

| Area | Responsible party |
|------|-------------------|
| Equipment ownership | H4H |
| Site access and placement approval | H4H |
| Power and internet service | H4H |
| Monthly internet cost | H4H |
| Equipment records after install | H4H |
| Physical maintenance after install | H4H |
| Optional outside technical help | Only if separately contracted by H4H |

---

## Installation Order

The crew should complete the work in the following order:

1. Complete procurement and staging.
2. Verify all site kits and parts.
3. Confirm the install points.
4. Inspect hardware before field placement.
5. Prepare the building and kiosk locations.
6. Install internet equipment and local network hardware.
7. Install solar hardware and weatherproof enclosures.
8. Mount the kiosk and related field equipment.
9. Connect power and network lines.
10. Start and test all equipment.
11. Photograph, label, and log each completed install.
12. Report any missing, unsafe, or incomplete work before leaving the site.

**Why this order matters:** Each phase depends on the one before it. Outdoor equipment cannot be tested until indoor internet is confirmed live. Solar hardware must be secure before kiosk equipment is closed up. Testing cannot happen until all connections are made. Working out of order often means discovering a problem after hardware is already mounted and sealed, which creates extra work and potential damage.

---

## Step-by-Step Workflow

### Phase 1: Procurement and Staging

**Why this phase exists:** Equipment that arrives incomplete, damaged, or mismatched to the install location creates field delays that cannot be recovered without a return trip. This phase prevents that. A crew that arrives on site with every part in hand, pre-sorted by location, can focus entirely on installation. A crew that arrives with missing or wrong parts will spend the day improvising or waiting — both of which cost more time and produce worse results than taking the extra day before deployment to verify everything is correct.

#### 1. Define Equipment by Location

The crew lead or project lead should assign every item to a specific install point before ordering.

Location groups for this project:

- 704 Main Street indoor equipment point.
- Walking trail kiosk location.
- Outdoor solar and communications mounting point.

**Why:** Assigning items to locations before ordering prevents the common problem of buying the right quantity of a product but not having the right configuration at the right place. A surge protector bought for the indoor rack that ends up at the kiosk is not useful to either location.

#### 2. Parts List for Procurement and Staging

The following list is the working procurement and staging list for the crew. Where a real product page has already been confirmed, it is linked directly. Where no exact product has been locked yet, an example link is provided for discussion and later final source selection. Example links are not purchase approvals — H4H must confirm compatibility, pricing, and sourcing before any order is placed.

| Site ID | Location | Item | Description | Qty | Link |
|---------|----------|------|-------------|-----|------|
| FCCAC-01 | 704 Main Street | Starlink kit | Main Starlink internet hardware kit | 1 | [Starlink Standard 4 X kit — Home Depot](https://www.homedepot.com/p/STARLINK-Standard-4-X-High-Speed-Low-Latency-Internet-Kit-Latest-Model-02534001/329052560) |
| FCCAC-01 | 704 Main Street | Starlink mount | Roof, wall, or pole mount for Starlink dish | 1 | Example mount types at [Starlink accessories — Home Depot](https://www.homedepot.com/b/STARLINK/N-5yc1vZya4) |
| FCCAC-01 | 704 Main Street | Router | Main internet router | 1 | Included with Starlink kit |
| FCCAC-01 | 704 Main Street | Small network switch | Local wired distribution switch | 1 | Example: [TP-Link TL-SG105 5-port gigabit switch — Amazon](https://www.amazon.com/Ethernet-Splitter-Optimization-Unmanaged-TL-SG105/dp/B00A128S24) |
| FCCAC-01 | 704 Main Street | Wi-Fi access point | Indoor wireless coverage unit if needed | 1 | May not be needed until testing confirms coverage |
| FCCAC-01 | 704 Main Street | Mini PC | Small edge computer or NUC-style unit | 1 | Example: [Beelink Mini S12 Pro Intel N100 mini PC — Amazon](https://www.amazon.com/Beelink-Intel-N100-Computer-Desktop-Display/dp/B0BVFS94J5) — or browse [Intel N100 mini PC search — Amazon](https://www.amazon.com/intel-n100-mini-pc/s?k=intel+n100+mini+pc) |
| FCCAC-01 | 704 Main Street | UPS battery backup | Small battery backup for router and mini PC | 1 | Example: [APC BE600M1 600VA UPS — Amazon](https://www.amazon.com/APC-Battery-Protector-BE600M1-Back-UPS/dp/B01FWAZEIU) |
| FCCAC-01 | 704 Main Street | Surge protector | Power protection strip | 2 | Example: [Tripp Lite TLP606B 6-outlet surge protector — Amazon](https://www.amazon.com/Tripp-Lite-Protector-INSURANCE-TLP606B/dp/B000UD4LIY) |
| FCCAC-01 | 704 Main Street | Ethernet cable | Pre-made or bulk CAT6 cable | 4 runs | Indoor example: [trueCABLE 500ft CAT6 riser — Amazon](https://www.amazon.com/trueCABLE-Copper-Unshielded-Twisted-Ethernet/dp/B0BW9LMSVF) — Outdoor run example: [CAT6 direct burial 500ft — Amazon](https://www.amazon.com/Ethernet-Shielded-Resistant-Waterproof-Connectors/dp/B0D41QXTNX) |
| FCCAC-01 | 704 Main Street | Cable clips and ties | Cable management supplies | 1 lot | Example: [DRIVUU 311-piece cable management kit — Amazon](https://www.amazon.com/DRIVUU-Management-Organizer-200Fasten-Electronics/dp/B0B6VYX66N) |
| FCCAC-01 | 704 Main Street | Wall anchors and screws | Mounting fasteners | 1 lot | Example: [1110-piece stainless screws, nuts, bolts, and washers assortment — Amazon](https://www.amazon.com/Assortment-Stainless-Hardware-Assorted-Washers%EF%BC%88/dp/B0C5N5VSJ2) |
| FCCAC-01 | 704 Main Street | Conduit or raceway | Cable protection for exposed runs | 1 lot | Example: [Kable Kontrol paintable cable raceway kit — Amazon](https://www.amazon.com/Kontrol-Paintable-Self-Adhesive-Management-Concealer/dp/B08Z25B57Y) — or [StarTech solid raceway channel — Amazon](https://www.amazon.com/StarTech-com-Cable-Management-Raceway-78in/dp/B08FCRD4MX) |
| KIOSK-01 | Walking trail kiosk | Existing kiosk structure | Existing kiosk already on site | 1 | Existing asset — no purchase needed |
| KIOSK-01 | Walking trail kiosk | Hotspot sign | Small Wi-Fi sign or Wi-Fi symbol sign | 1 | Example: [My Sign Center Free Wireless Internet Hotspot sign — Amazon](https://www.amazon.com/Sign-MS-280960-polystyrene-My-Center/dp/B0F67LYHXM) — or [Wi-Fi Zone vinyl banner — Amazon](https://www.amazon.com/WI-FI-BANNER-internet-hotspot-signs/dp/B005NISMW2) |
| KIOSK-01 | Walking trail kiosk | Outdoor weatherproof enclosure | Lockable enclosure for equipment | 1 | [Sixfab IP65 Outdoor Project Enclosure — Sixfab](https://sixfab.com/product/raspberry-pi-ip65-outdoor-iot-project-enclosure/) |
| KIOSK-01 | Walking trail kiosk | Raspberry Pi | Small controller or receiver unit | 1 | Example options: [Raspberry Pi 5 desktop kit accessories — Adafruit](https://www.adafruit.com/product/5824) and [Raspberry Pi 5 starter kit bundle — Gigaparts](https://www.gigaparts.com/raspberry-pi-5-starter-kit-8gb-micro-sd-16gb-case-with-fan-hdmi-cable-psu-5-1v-5-0a-rpi5-starterkit-8g.html) |
| KIOSK-01 | Walking trail kiosk | Raspberry Pi power supply | Power adapter for Raspberry Pi | 1 | Included in [Adafruit Raspberry Pi 5 desktop kit accessories](https://www.adafruit.com/product/5824) |
| KIOSK-01 | Walking trail kiosk | MicroSD card | Storage card for Raspberry Pi | 1 | Included in [Adafruit Raspberry Pi 5 desktop kit accessories](https://www.adafruit.com/product/5824) |
| KIOSK-01 | Walking trail kiosk | Short HDMI or adapter cable | Display connection as needed | 1 | Included in [Gigaparts Raspberry Pi 5 starter kit bundle](https://www.gigaparts.com/raspberry-pi-5-starter-kit-8gb-micro-sd-16gb-case-with-fan-hdmi-cable-psu-5-1v-5-0a-rpi5-starterkit-8g.html) |
| KIOSK-01 | Walking trail kiosk | Outdoor power cable | Weather-rated power cable | 1 | Example: [Southwire Yellow Jacket 12/3 SJTW heavy-duty outdoor extension cord — Amazon](https://www.amazon.com/2883-Heavy-Duty-Contractor-Extension-Lighted/dp/B000KKLMO8) |
| KIOSK-01 | Walking trail kiosk | Exterior cable gland set | Waterproof cable pass-through fittings | 1 set | Included with some enclosures; verify against [Sixfab assembly instructions](https://docs.sixfab.com/page/raspberry-pi-ip54-outdoor-project-enclosure-assembly-instructions) |
| SOLAR-01 | Outdoor solar point | Solar panel | 200W solar panel | 1 | [Rich Solar MEGA 200 — Rich Solar](https://richsolar.com/products/mega-200-200-watt-12-volt-solar-panel) |
| SOLAR-01 | Outdoor solar point | Solar charge controller | Charge controller sized for panel and battery | 1 | Example: [ExpertPower 20A MPPT solar charge controller — ExpertPower](https://www.expertpower.us/products/20a-mppt-solar-charge-controller-2) |
| SOLAR-01 | Outdoor solar point | Battery | 12V 100Ah battery | 1 | Example options: [LiTime 12V 100Ah battery family — LiTime](https://www.litime.com/collections/12v-100ah-batteries) or [Battle Born 100Ah 12V LiFePO4 — Battle Born](https://battlebornbatteries.com/products/100ah-12v-lifepo4-deep-cycle-battery) |
| SOLAR-01 | Outdoor solar point | Battery box | Weather-protected battery housing | 1 | Example: [NOCO BG31 Snap-Top Group 24–31 battery box — Amazon](https://www.amazon.com/NOCO-Snap-Top-Battery-Automotive-Batteries/dp/B0CSTDNC2F) |
| SOLAR-01 | Outdoor solar point | Pole or mounting frame | Support for solar panel and radio hardware | 1 | Example: [Solar panel pole mount double-arm bracket kit — Amazon](https://www.amazon.com/Solar-Universal-Bracket-Adjustable-Mounting/dp/B07NK8YCLL) |
| SOLAR-01 | Outdoor solar point | Panel mounting brackets | Hardware for securing solar panel | 1 set | Example: [Adjustable aluminum solar panel tilt mount brackets 2-set — Amazon](https://www.amazon.com/Adjustable-Solar-Panel-Mount-Brackets/dp/B0CGDQJ9QF) — see also [Rich Solar panel family](https://richsolar.com/collections/solar-panels) for panel-specific hardware context |
| SOLAR-01 | Outdoor solar point | Weatherproof electronics enclosure | Sealed box for power and communication parts | 1 | Example outdoor enclosure family: [Sixfab enclosure category — Sixfab](https://sixfab.com/product-category/development-tools/enclosures/) |
| SOLAR-01 | Outdoor solar point | Fuse block or inline fuses | Electrical protection hardware | 1 set | Example: [RVBOATPAT 12V 150A bus bar power distribution block — Amazon](https://www.amazon.com/RVBOATPAT-400A-600A-Bus-Bar/dp/B0FD9LK2J4) |
| SOLAR-01 | Outdoor solar point | DC wiring set | Power wire, terminals, and connectors | 1 lot | Final gauge and connector type depends on locked battery and controller selection; search [solar DC wiring kit — Amazon](https://www.amazon.com/solar-dc-wiring/s?k=solar+dc+wiring+kit) as a starting point |
| SOLAR-01 | Outdoor solar point | Grounding hardware | Ground rod, clamp, and wire if required | 1 set | Example: [THE CIMPLE CO 4-ft copper grounding rod with clamp — Amazon](https://www.amazon.com/CIMPLE-CO-Grounding-Diameter-Satellite/dp/B07WL7X8BS) — or [CYANTEKOMS 3-pack grounding rods with clamps — Amazon](https://www.amazon.com/CYANTEKOMS-Grounding-Electrical-Satellite-Generator/dp/B0CJX5VSSG) |
| SOLAR-01 | Outdoor solar point | Starlink receiver point hardware | Hardware needed at outdoor receive point | 1 set | Depends on final mount and enclosure layout; see [Starlink accessories — Home Depot](https://www.homedepot.com/b/STARLINK/N-5yc1vZya4) |
| LORA-01 | Outdoor communications point | LoRa node | LILYGO T-Beam or Heltec LoRa32 class device | 1 | Example hardware guidance: [Meshtastic LoRa hardware notes — Meshtastic](https://meshtastic.org/docs/hardware/antennas/lora-antenna/) |
| LORA-01 | Outdoor communications point | LoRa antenna | External or matched antenna | 1 | Example antenna guidance: [LoRa antenna selection notes — Meshtastic](https://meshtastic.org/docs/hardware/antennas/lora-antenna/) |
| LORA-01 | Outdoor communications point | Small solar support kit | Solar support for LoRa backup node | 1 | See [Rich Solar small panel options](https://richsolar.com/collections/solar-panels) paired with a small MPPT controller; the ExpertPower 20A example above applies here as well |
| LORA-01 | Outdoor communications point | LoRa enclosure | Small weatherproof box | 1 | Example enclosure family: [Sixfab enclosure category — Sixfab](https://sixfab.com/product-category/development-tools/enclosures/) |
| LORA-01 | Outdoor communications point | Pole clamps or mount straps | Hardware for mounting the node | 1 set | Example: [U-bolt antenna mast clamp aluminum 2-pack — Amazon](https://www.amazon.com/Antenna-Mount-Clamp-Bracket-Outdoor/dp/B0C8T2JLTQ) — or [stainless steel mounting straps for poles — Amazon](https://www.amazon.com/Stainless-Steel-Mounting-Strap-Diameter/dp/B00728Z170) |
| ALL-LOC | All locations | Labels | Equipment ID labels | 1 lot | Example: [Brady M210 portable label printer kit — Amazon](https://www.amazon.com/Brady-M210-Portable-Label-Printer/dp/B09WZDDGCZ) — or [Brady BMP21-PLUS kit — Amazon](https://www.amazon.com/Brady-BMP21-PLUS-KIT1-Printer-Kit/dp/B0922FZD29) |
| ALL-LOC | All locations | Photo log sheet | Install record sheet | 1 set | Internal print item |
| ALL-LOC | All locations | Spare fasteners | Spare screws, anchors, bolts, and washers | 1 lot | Example: [720-piece stainless screws, nuts, bolts, and washers assortment — Amazon](https://www.amazon.com/Bolts-Assortment-Phillips-Stainless-Washers/dp/B0CWGXD5XH) |
| ALL-LOC | All locations | Sealant | Outdoor weather sealant | 1 tube | Example: [Dicor 501LSW-1 self-leveling EPDM lap sealant — Amazon](https://www.amazon.com/Dicor-501LSW-1-Self-Leveling-Sealant-10-3-Fluid_Ounces/dp/B000BRF7QE) |
| ALL-LOC | All locations | Electrical tape and heat shrink | Wire protection supplies | 1 lot | Example: [Eventronic 600-piece heat shrink tubing assortment kit — Amazon](https://www.amazon.com/560PCS-Heat-Shrink-Tubing-Eventronic/dp/B072PCQ2LW) |

#### 3. Receive and Inspect Equipment

All equipment should be checked as soon as it arrives.

Checklist:
- Match each delivered item to the parts list.
- Inspect for broken parts, dents, cracks, or missing accessories.
- Record serial numbers for Starlink hardware, mini PC, Raspberry Pi, and radio hardware where available.
- Separate damaged or incomplete items from field-ready items.

**Why:** Damaged or missing items discovered on the day of installation mean the crew either proceeds with incomplete equipment or leaves the site unfinished. Both outcomes cost more time and money than catching the problem before loading the vehicles. Serial number records are required for warranty claims, insurance documentation, and H4H's asset inventory.

#### 4. Stage Site Kits

Each location should have its own labeled kit so the crew can load and unload efficiently.

Required site kits:
- FCCAC-01 indoor kit.
- KIOSK-01 outdoor kiosk kit.
- SOLAR-01 solar power kit.
- LORA-01 backup communications kit.

Each kit should include:
- Main device or hardware assigned to that site.
- All required fasteners and mounts.
- Power parts and adapters.
- Cables and cable protection.
- Printed copy of that site's parts list.
- Printed site notes.

**Why:** Pre-staged kits prevent the crew from digging through a common pile of parts at each location trying to figure out what belongs where. When everything for one location travels together, the crew can work through one location at a time without interruption and without accidentally using a part that was intended for a different site.

#### 5. Pre-Field Verification

Before vehicles are loaded, confirm the following:

- All site kits are complete.
- Internet hardware is in hand.
- Solar parts are complete.
- Batteries are ready for installation.
- Labels, paperwork, and tools are packed.
- Spare fasteners and spare cable are packed.

**Why:** Loading a vehicle and driving to a job site only to realize something was left behind is a preventable loss of time. This checklist takes five minutes. A return trip to retrieve a missing part takes hours.

---

### Phase 2: Confirm the Work Plan

**Why this phase exists:** Site conditions do not always match what was planned in the office. A wall that looked solid in a photograph may not support a mount. A pole position that seemed ideal may be in the wrong location once the crew is standing there. This phase gives the crew a structured moment to look at the actual site, confirm that the planned install points still make sense, and surface any problems before tools are out and hardware is being handled.

Checklist:
- Confirm 704 Main Street equipment placement.
- Confirm kiosk placement.
- Confirm solar mounting point.
- Confirm where the LoRa backup node will be attached.
- Confirm who approves final placement on site.

**Why each step:** Placement decisions made without authorization from H4H can result in equipment going in the wrong location, creating access problems, aesthetic problems, or conflicts with building structure. The crew does not make final placement calls independently. If a proposed location is not workable, the crew raises that to H4H and waits for guidance before proceeding.

---

### Phase 3: Inspect Hardware Before Placement

**Why this phase exists:** Equipment can be damaged in transport even when it looked fine at staging. Checking hardware before placement means any damage is caught before the crew spends time mounting something that will not work.

Checklist:
- Verify the correct device is in the correct site kit.
- Check that no hardware was damaged during transport.
- Check that all required power supplies, brackets, and cables are present.

**Why:** Mounting a device and then discovering it is the wrong unit — or that the required bracket did not make it into the kit — means unmounting it and starting over. Thirty seconds of verification before touching a mount saves that cycle.

---

### Phase 4: Prepare the Site

**Why this phase exists:** Mounting hardware into an unprepared surface, or routing cable through an area that has not been checked for clearance and safety, produces installations that either fail structurally or create hazards. Site preparation is the step that prevents those problems.

Checklist:
- Check walls, poles, surfaces, and install heights.
- Confirm safe cable routes.
- Confirm public safety and access.
- Confirm weather exposure and drainage.
- Confirm power access where needed.

**Why each step:** Mounting surfaces must be load-rated for what is being attached. Cable routes through walls, conduit, or outdoor runs must be clear of sharp edges, pinch points, and water infiltration paths. Equipment installed in a public location must not create trip hazards, snag points, or access barriers. Outdoor hardware must be positioned so water drains away from enclosures rather than pooling against them. Power must be confirmed present and accessible before any wired equipment is committed to a location.

---

### Phase 5: Install Internet and Indoor Equipment

**Why this phase exists:** The indoor Starlink installation is the source of the entire project's internet connectivity. Nothing else on the outdoor network functions without it. Installing this first confirms the core service is active before any outdoor work is closed up and sealed.

Checklist:
- Install the Starlink mount.
- Install the Starlink hardware.
- Route cable safely into the building.
- Install router, switch, and indoor wireless unit if used.
- Install the mini PC.
- Install UPS and surge protection.
- Confirm internet service is live.

**Why each step:**

The mount must go in before the dish so the attachment point is confirmed solid before the hardware is committed to it. Routing cable into the building before securing the interior equipment means the cable path is established and the crew knows how much slack to leave. Router and switch come after confirmed cable entry so the crew can immediately test connectivity without running to a different location. The UPS and surge protection go in at the end of the indoor sequence because they protect equipment that is already installed and confirmed working — power protection added before devices are confirmed functional could mask startup problems during testing.

Confirming internet service is live before leaving the indoor location is not optional. The outdoor equipment depends on this connection. If connectivity is not confirmed at this stage, the problem needs to be resolved before proceeding.

---

### Phase 6: Install Solar and Outdoor Support Hardware

See the detailed phase document:
[Phase 6: Install Solar and Outdoor Support Hardware](Phase%206.md)

**Why this phase exists:** The outdoor kiosk equipment and the LoRa node both depend on power from the solar system. Installing the power infrastructure before the devices that use it means those devices can be connected and tested immediately after mounting, rather than waiting for power to be sorted out after the fact.

Checklist:
- Mount the 200W solar panel.
- Install the panel brackets and support frame.
- Install the charge controller.
- Install the 12V 100Ah battery in its battery box.
- Install fuse protection and DC wiring.
- Install the weatherproof equipment enclosure.
- Confirm secure weather protection.

**Why each step:**

The panel mounts before the brackets are locked because the panel position determines the final bracket angle. Getting the angle right requires the panel to be physically present during adjustment. The charge controller comes after the panel is in place because the controller is wired to the panel, and verifying that wire run is clean is easier when both endpoints are already installed. The battery goes into its box before it is wired because a battery that is outside its housing is a safety risk — exposed terminals in a field environment can short against tools, metal parts, or fastener kits. Fuse protection is installed before any DC wiring is connected because connecting wires to an unfused battery creates a fire and shock risk. The weatherproof enclosure goes on last in this phase to confirm all interior wiring and hardware is correctly placed before the access door is closed. Confirming weather protection means checking that the enclosure seal is intact, that cable glands are tight, and that no wiring exits the enclosure without appropriate strain relief and waterproofing.

---

### Phase 7: Install Kiosk Hotspot Equipment

See the detailed phase document:
[Phase 7: Install Kiosk Hotspot Equipment](Phase%207.md)

**Why this phase exists:** The kiosk is the public-facing point of contact for people using the walking trail. It must be structurally sound, clearly marked, and fully functional before it is considered complete. Installing it after the power infrastructure is in place means the equipment inside the enclosure can be connected to power immediately and tested before the enclosure is sealed.

Checklist:
- Confirm the existing kiosk is structurally sound.
- Install the outdoor enclosure.
- Install the Raspberry Pi and storage card if used for local control or monitoring.
- Install the hotspot sign or Wi-Fi symbol sign.
- Secure and protect all exposed wiring.

**Why each step:**

The structural check happens first because an unstable kiosk is a public safety risk, and mounting additional hardware to it makes the problem worse, not better. If the kiosk is not structurally sound, stop and report to H4H before proceeding. The enclosure goes in before the Raspberry Pi because the Pi and its accessories need a protected mounting point before they are handled in an outdoor environment. The hotspot sign is installed after the enclosure so it can be positioned in relation to the final hardware placement. Wiring is secured and protected last because the exact path of every wire is not known until all hardware is in its final position.

---

### Phase 8: Install Backup Communications Node

See the detailed phase document:
[Phase 8: Install Backup Communications Node](Phase%208.md)

**Why this phase exists:** The LoRa node is the backup communication layer for the network. It is not the primary path, but it must be operational and protected independently from the main system. Installing it after the main outdoor hardware means it can share pole and mounting resources without competing for access during installation of higher-priority equipment.

Checklist:
- Install the LoRa node.
- Install the antenna.
- Install the small solar support kit if separate from the main solar hardware.
- Mount the node in the weatherproof box.
- Confirm it is secure and protected.

**Why each step:**

The node goes in before the antenna so the physical unit is stabilized before the antenna is attached, which reduces torque stress on the node's connector. The antenna is the most exposed part of this assembly and should be the last thing connected before the box is closed. Solar support for the node is installed after the node is in position so the panel angle can be optimized for the node's actual mounted location rather than a pre-planned position that may not match site conditions. The node goes into its enclosure before the final antenna connection is made so that only the antenna connector is exposed during that last step. Confirming the unit is secure means physically checking that the enclosure is latched, the pole clamps are tight, and the antenna is not under mechanical stress from the mount position.

---

### Phase 9: Connect Power and Network

See the detailed phase document:
[Phase 9: Connect Power and Network](Phase%209.md)


**Why this phase exists:** This phase is the point at which all installed hardware becomes a connected system rather than a collection of independent devices. Connections made without checking strain relief, weather sealing, and cable protection first are the most common source of failures that appear days or weeks after installation rather than immediately.

Checklist:
- Connect indoor equipment to power and UPS.
- Connect outdoor kiosk equipment to the assigned power source.
- Connect internet and local network lines as required.
- Confirm cable strain relief and weather sealing.
- Confirm exposed wiring is protected.

**Why each step:**

Indoor power connections happen first because they are the lowest-risk connections to make — the environment is controlled and the equipment is already confirmed mounted and functional. Outdoor power connections come after because they require weather sealing, which takes time to do correctly. Network lines are connected after power is confirmed because testing network function requires power to be live at both ends of the connection. Strain relief is confirmed after all connections are made because it is only possible to verify that cables are not under stress once they are routed and connected in their final positions. Weather sealing is confirmed last because it seals the installation against the environment permanently, and reopening a sealed enclosure to address a wiring problem is significantly more work than catching the problem before sealing.

---

### Phase 10: Start and Test Equipment

**Why this phase exists:** No installation is complete until every device has been confirmed operational in its installed location. A device that powers on in a staging environment may fail in the field due to a wiring error, a bad connection, an incompatible power level, or a configuration issue that only appears when the hardware is connected to the live network. This phase catches those problems while the crew is still on site and the system is accessible.

Checklist:
- Power on Starlink and confirm connection.
- Power on router, switch, and mini PC.
- Confirm indoor network access.
- Power on kiosk equipment.
- Confirm the Raspberry Pi starts correctly.
- Confirm the kiosk hotspot function works.
- Confirm the LoRa backup node powers on.
- Restart each main device once if needed to confirm stable startup.

**Why the restart step:** A device that powers on correctly the first time but fails to recover after a restart reveals a configuration or hardware problem that will manifest during a power outage or scheduled reboot. Catching that before leaving the site means it can be addressed while the crew has tools and access.

**Why the sequence:** Starlink and the indoor network are tested first because they are prerequisites for the outdoor network. There is no point testing the kiosk hotspot if the source connection is not confirmed live. The LoRa node is tested last because it is the backup layer — it does not depend on the main network to function, but testing it in sequence prevents it from being forgotten.

---

### Phase 11: Record the Installation

**Why this phase exists:** Installation records serve multiple functions that are not immediately visible during the installation itself. They provide H4H with proof that work was completed, a reference for future maintenance, documentation for insurance and grant reporting, and a starting point for any troubleshooting that happens after the crew has left the site. Records made in the field at the time of installation are always more accurate than records reconstructed later from memory.

Checklist:
- Apply equipment labels.
- Photograph each installed device.
- Photograph cable runs, enclosures, and solar hardware.
- Record the final install location.
- Record any issue, limitation, or follow-up need.

**Why photographs specifically:** A photograph of each device in its installed position documents what was installed, where it is physically located, how cable runs are routed, and what condition the site was in at the time of completion. That information is essential for any future technician who needs to maintain or replace equipment without having been present during installation.

**Why labels:** Equipment labels allow any person who encounters the hardware later — including people who were not part of the install crew — to identify what the device is, what location it belongs to, and how to cross-reference it against H4H's inventory records.

---

### Phase 12: Close Out the Site

**Why this phase exists:** The site is a public location. A clean, safe close-out is not a nicety — it is a requirement. Packaging materials left on site become litter and potential hazards. Incomplete work left without a report to H4H means the problem may not be addressed until a member of the public encounters it.

Checklist:
- Confirm the site is clean and safe.
- Remove packaging and scrap material.
- List incomplete items.
- Report any condition that prevents public use.

**Why the incomplete items list:** If any item from the installation checklist was not completed — for any reason — H4H needs to know before the crew leaves the site. An undocumented incomplete item may delay public access to the service and will create confusion for whoever is assigned to follow up. The list does not need to be long. It needs to be accurate.

---

## Minimum Acceptance Standard

A location is complete only when all of the following are true:

- The correct hardware is installed in the correct location.
- Indoor internet hardware is active.
- The mini PC is installed and powered.
- The kiosk is secure and weather protected.
- The Raspberry Pi starts correctly.
- The solar panel, controller, and battery are installed safely.
- The LoRa backup node is mounted and powered.
- Required photos and equipment records are complete.
- Any unresolved issue has been reported to H4H.

**Why a minimum acceptance standard exists:** This list defines the point at which the location is considered done. Without a clear standard, individual crew members may have different opinions about whether a location is ready. The standard removes that ambiguity. If any item on this list is not true, the location is not complete, regardless of how much else has been accomplished.

---

## Issues That Must Be Reported Immediately

The crew should stop and report to H4H if any of the following occur:

- No safe mounting surface is available.
- No usable power path is available.
- Internet service cannot be activated.
- Solar hardware cannot be mounted safely.
- Equipment arrives damaged or incomplete.
- A mounted unit cannot be secured.
- Weather or site conditions prevent safe completion.

**Why stopping matters:** Proceeding through a problem without reporting it does not make the problem go away — it makes it harder to address later. A mounting surface that is not safe becomes a liability. Equipment installed without proper power becomes a damage risk. Hardware secured with improvised substitutes may fail in ways that are not immediately visible. The crew's job is to install correctly or stop and report — not to find workarounds to keep the schedule moving.

---

## Site Kit Checklist

Each site kit should include all parts needed for one location.

### FCCAC-01 Indoor Kit
- Starlink kit.
- Starlink mount.
- Router.
- Small network switch.
- Wi-Fi unit if used.
- Mini PC.
- UPS battery backup.
- Surge protector.
- Ethernet cables.
- Cable clips, ties, anchors, and screws.
- Conduit or raceway sections.

### KIOSK-01 Outdoor Kiosk Kit
- Existing kiosk structure.
- Hotspot sign.
- Outdoor weatherproof enclosure.
- Raspberry Pi.
- Raspberry Pi power supply.
- MicroSD card.
- Short display cable or adapter.
- Outdoor power cable.
- Exterior cable glands.

### SOLAR-01 Solar Kit
- 200W solar panel.
- Solar charge controller.
- 12V 100Ah battery.
- Battery box.
- Pole or support frame.
- Panel mounting brackets.
- Weatherproof electronics enclosure.
- Fuse protection and bus bar.
- DC wiring set.
- Grounding hardware if required.

### LORA-01 Backup Communications Kit
- LoRa node.
- LoRa antenna.
- Small solar support kit.
- LoRa enclosure.
- Pole clamps or mount straps.

### ALL-LOC Shared Field Kit
- Equipment ID labels and label maker.
- Spare fasteners assortment.
- Outdoor weather sealant.
- Electrical tape and heat shrink assortment.
- Photo log sheets.
- Spare CAT6 cable.

---

## After Installation

After the crew finishes the installation, H4H remains responsible for the equipment, internet service, ongoing costs, and future upkeep. Outside technical help may be brought in later only if H4H chooses to contract for it separately.

---

## Procurement SKU Sheet

This section is appended for ordering. The links below are confirmed or example product pages for the main items identified for this build. Items marked as examples require H4H review and final selection before purchase.

| Category | Item | Model / SKU | Vendor | Purchase link | Notes |
|----------|------|-------------|--------|---------------|-------|
| Internet uplink | Starlink Standard kit | Model 02534001 / Internet #329052560 / Store SKU #1011034206 | Home Depot | [Starlink Standard 4 X kit](https://www.homedepot.com/p/STARLINK-Standard-4-X-High-Speed-Low-Latency-Internet-Kit-Latest-Model-02534001/329052560) | Confirmed retail listing. Includes dish, power supply, cables, base, and router. Monthly service plan required separately. |
| Solar panel | 200W solar panel | MEGA 200 | Rich Solar | [Rich Solar MEGA 200](https://richsolar.com/products/mega-200-200-watt-12-volt-solar-panel) | Panel only. Battery and controller ordered separately unless a full kit is selected. |
| Outdoor enclosure (kiosk) | Raspberry Pi weatherproof enclosure | Sixfab IP65 Outdoor Project Enclosure | Sixfab | [Sixfab IP65 enclosure](https://sixfab.com/product/raspberry-pi-ip65-outdoor-iot-project-enclosure/) | Compatible with Raspberry Pi and outdoor cable routing. |
| Battery — example | 12V 100Ah LiFePO4 battery | 12V 100Ah class | LiTime | [LiTime 12V 100Ah family](https://www.litime.com/collections/12v-100ah-batteries) | Example family page. Final battery selection still required. |
| Battery — example | 12V 100Ah LiFePO4 battery | 100Ah 12V | Battle Born | [Battle Born 100Ah 12V battery](https://battlebornbatteries.com/products/100ah-12v-lifepo4-deep-cycle-battery) | Premium option for comparison. Higher cost. |
| Charge controller — example | 20A MPPT charge controller | 20A MPPT | ExpertPower | [ExpertPower 20A MPPT controller](https://www.expertpower.us/products/20a-mppt-solar-charge-controller-2) | Example controller class for discussion. |
| Raspberry Pi — example | Raspberry Pi 5 accessories bundle | Desktop kit accessories | Adafruit | [Raspberry Pi 5 desktop kit accessories](https://www.adafruit.com/product/5824) | Accessory example. Pi board sold separately. |
| Raspberry Pi — example | Raspberry Pi 5 starter kit | Starter Kit 8GB | Gigaparts | [Raspberry Pi 5 starter kit bundle](https://www.gigaparts.com/raspberry-pi-5-starter-kit-8gb-micro-sd-16gb-case-with-fan-hdmi-cable-psu-5-1v-5-0a-rpi5-starterkit-8g.html) | Example bundle including Pi board, case, SD card, and PSU. |
| Network switch — example | 5-port gigabit unmanaged switch | TL-SG105 | TP-Link / Amazon | [TP-Link TL-SG105 — Amazon](https://www.amazon.com/Ethernet-Splitter-Optimization-Unmanaged-TL-SG105/dp/B00A128S24) | Example product class. Plug-and-play, no configuration required. |
| Mini PC — example | Intel N100 mini PC | Mini S12 Pro | Beelink / Amazon | [Beelink Mini S12 Pro — Amazon](https://www.amazon.com/Beelink-Intel-N100-Computer-Desktop-Display/dp/B0BVFS94J5) | Example class. Final selection should confirm RAM, storage, and port requirements. |
| UPS battery backup — example | 600VA uninterruptible power supply | BE600M1 | APC / Amazon | [APC BE600M1 600VA UPS — Amazon](https://www.amazon.com/APC-Battery-Protector-BE600M1-Back-UPS/dp/B01FWAZEIU) | Example. Confirm VA rating against actual load before purchase. |
| Surge protector — example | 6-outlet surge protector strip | TLP606B | Tripp Lite / Amazon | [Tripp Lite TLP606B — Amazon](https://www.amazon.com/Tripp-Lite-Protector-INSURANCE-TLP606B/dp/B000UD4LIY) | Example. Confirm outlet count and joule rating for actual load. |
| Ethernet cable — indoor example | 500ft bulk CAT6 riser cable | CMR rated | trueCABLE / Amazon | [trueCABLE 500ft CAT6 riser — Amazon](https://www.amazon.com/trueCABLE-Copper-Unshielded-Twisted-Ethernet/dp/B0BW9LMSVF) | For indoor runs. Cut to length on site. |
| Ethernet cable — outdoor example | 500ft outdoor direct burial CAT6 | Shielded FTP | Generic / Amazon | [Outdoor direct burial CAT6 500ft — Amazon](https://www.amazon.com/Ethernet-Shielded-Resistant-Waterproof-Connectors/dp/B0D41QXTNX) | For outdoor or buried runs. Confirm shielding and UV rating. |
| Cable management — example | 311-piece cable management kit | Mixed clips, ties, sleeves | DRIVUU / Amazon | [DRIVUU cable management kit — Amazon](https://www.amazon.com/DRIVUU-Management-Organizer-200Fasten-Electronics/dp/B0B6VYX66N) | Example all-in-one kit for indoor cable routing. |
| Cable raceway — example | Paintable self-adhesive cable raceway kit | 144-inch kit | Kable Kontrol / Amazon | [Kable Kontrol cable raceway kit — Amazon](https://www.amazon.com/Kontrol-Paintable-Self-Adhesive-Management-Concealer/dp/B08Z25B57Y) | For exposed wall runs. Paintable PVC. |
| Hotspot sign — example | Free Wi-Fi hotspot sign | MS-280960 | My Sign Center / Amazon | [My Sign Center Free Wi-Fi sign — Amazon](https://www.amazon.com/Sign-MS-280960-polystyrene-My-Center/dp/B0F67LYHXM) | Example. Pre-drilled for mounting. Weather resistant. |
| Outdoor power cable — example | 12/3 SJTW heavy-duty outdoor extension cord | Yellow Jacket 25ft | Southwire / Amazon | [Southwire Yellow Jacket 12/3 SJTW — Amazon](https://www.amazon.com/2883-Heavy-Duty-Contractor-Extension-Lighted/dp/B000KKLMO8) | Weather-rated for outdoor use. Confirm length needed on site. |
| Battery box — example | Group 24–31 snap-top battery box | BG31 | NOCO / Amazon | [NOCO BG31 battery box — Amazon](https://www.amazon.com/NOCO-Snap-Top-Battery-Automotive-Batteries/dp/B0CSTDNC2F) | Fits Group 24 through 31 12V batteries. UV and acid resistant. |
| Panel mount — example | Adjustable aluminum solar panel tilt mount brackets | 2-set adjustable tilt | Generic / Amazon | [Adjustable solar panel tilt mount brackets — Amazon](https://www.amazon.com/Adjustable-Solar-Panel-Mount-Brackets/dp/B0CGDQJ9QF) | Example. Confirm compatibility with panel frame dimensions. |
| Pole mount — example | Solar panel double-arm pole mount bracket kit | Universal double arm | Generic / Amazon | [Solar panel pole mount double-arm bracket kit — Amazon](https://www.amazon.com/Solar-Universal-Bracket-Adjustable-Mounting/dp/B07NK8YCLL) | For pole-mounted panel configuration. |
| Fuse block — example | 12V 150A DC bus bar power distribution block | 150A bus bar | RVBOATPAT / Amazon | [RVBOATPAT 12V 150A bus bar — Amazon](https://www.amazon.com/RVBOATPAT-400A-600A-Bus-Bar/dp/B0FD9LK2J4) | Example. Confirm amperage against actual system load. |
| Grounding hardware — example | 4-ft copper grounding rod with clamp | 3/8-inch diameter | THE CIMPLE CO / Amazon | [THE CIMPLE CO 4-ft grounding rod — Amazon](https://www.amazon.com/CIMPLE-CO-Grounding-Diameter-Satellite/dp/B07WL7X8BS) | Single rod with pre-installed clamp. |
| Pole clamps — example | U-bolt antenna mast clamp aluminum 2-pack | U-bolt mount | Generic / Amazon | [U-bolt antenna mast clamp 2-pack — Amazon](https://www.amazon.com/Antenna-Mount-Clamp-Bracket-Outdoor/dp/B0C8T2JLTQ) | For LoRa node pole attachment. |
| Mount straps — example | Stainless steel mounting straps for poles | 8.5-inch diameter strap | Generic / Amazon | [Stainless steel pole mounting straps — Amazon](https://www.amazon.com/Stainless-Steel-Mounting-Strap-Diameter/dp/B00728Z170) | Alternative to U-bolt for larger poles. |
| Labels — example | Portable label printer kit | M210-KIT | Brady / Amazon | [Brady M210 label printer kit — Amazon](https://www.amazon.com/Brady-M210-Portable-Label-Printer/dp/B09WZDDGCZ) | Field-ready handheld printer for equipment labeling. |
| Spare fasteners — example | 720-piece stainless screws, nuts, bolts, and washers assortment | #6-32 through 1/4-20 | SATANTECH / Amazon | [720-piece stainless hardware assortment — Amazon](https://www.amazon.com/Bolts-Assortment-Phillips-Stainless-Washers/dp/B0CWGXD5XH) | General field spare. |
| Sealant — example | Self-leveling EPDM lap sealant | 501LSW-1 | Dicor / Amazon | [Dicor 501LSW-1 self-leveling sealant — Amazon](https://www.amazon.com/Dicor-501LSW-1-Self-Leveling-Sealant-10-3-Fluid_Ounces/dp/B000BRF7QE) | Adheres to aluminum, metal, concrete, and vinyl. UV resistant. |
| Heat shrink — example | 600-piece heat shrink tubing assortment | 2:1 ratio, 5 colors, 12 sizes | Eventronic / Amazon | [Eventronic 600-piece heat shrink kit — Amazon](https://www.amazon.com/560PCS-Heat-Shrink-Tubing-Eventronic/dp/B072PCQ2LW) | For wire protection and connection sealing. |

---

## Procurement Notes

- The Starlink hardware link is a confirmed retail listing for the Standard 4 X kit. It is the identified starting point for the internet uplink portion of this project.
- All other links in this document are examples provided so H4H and the crew can review actual products before locking final selections.
- Example links are not purchase approvals. H4H must confirm compatibility, pricing, weather rating, and sourcing for each item before any order is placed.
- DC wiring gauge and connector type for the solar system cannot be finalized until the battery and charge controller are locked. Wire the system to the specifications of the confirmed equipment, not to a generic estimate.
