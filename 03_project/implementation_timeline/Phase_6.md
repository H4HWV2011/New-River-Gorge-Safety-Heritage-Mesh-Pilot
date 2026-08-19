# Phase 6: Install Solar and Outdoor Support Hardware
## Field Learning Guide — Mount Hope Walking Trail Pilot Site

---

## What This Document Is For

This document expands on Phase 6 of the installation workflow. It explains not just what to do, but why each step is done in the order it is done, what can go wrong if the order is skipped, and what a correctly completed phase looks like when the crew is finished. Because this is a pilot site, this document is also intended to serve as a learning record so that H4H and future crews can apply these lessons to future installations without repeating avoidable mistakes.

---

## What Phase 6 Covers

Phase 6 installs the power infrastructure that the entire outdoor network depends on. Every device mounted outside the building — the kiosk hotspot, the LoRa backup node, and any outdoor Starlink receive point — needs power to function. That power comes from the solar system installed in this phase. If the solar system is incomplete, incorrectly wired, or inadequately protected, every device downstream of it will either fail or be at risk.

The equipment installed in this phase:

- 200W solar panel (Rich Solar MEGA 200 or equivalent)
- Adjustable aluminum mounting brackets for the panel
- Pole or support frame for the panel and associated hardware
- 20A MPPT solar charge controller
- 12V 100Ah LiFePO4 battery in a Group 24–31 battery box
- Fuse block or DC bus bar for electrical protection
- DC wiring connecting all components
- Weatherproof electronics enclosure for the controller and wiring
- Grounding hardware if required by site conditions

---

## The Step Sequence and the Reason for Each Step

### Step 1: Mount the support frame or pole

**What to do:** Set the pole or support frame in its confirmed location. Secure it fully before attaching any hardware to it. If the frame uses ground stakes or anchors, drive them to the depth required for the soil conditions at this site. If it attaches to an existing structure, confirm the attachment point is rated for the combined weight and wind load of the panel plus any additional hardware.

**Why first:** Everything else mounts to this frame. If the frame is not solid, every bracket, enclosure, and panel mounted to it is at risk of movement, tipping, or failure. Discovering that the frame is insufficient after the panel and enclosure are already attached means unloading and reloading everything to fix the base. Getting the base right first costs five minutes. Fixing it after everything is loaded costs an hour.

**What to check before moving on:** Push and pull the frame in all directions. It should not move. If it moves, it is not ready.

**Lesson for future sites:** Soil conditions at this site are specific to this location. At other sites in the region, soil composition may be different — clay, rock, loose fill. The depth and anchor type required may change. Document the anchor method used here and note whether it held without adjustment. That record helps future crews make faster decisions at new sites.

---

### Step 2: Install the panel mounting brackets

**What to do:** Attach the adjustable aluminum tilt brackets to the support frame. Set the tilt angle to approximately 37–40 degrees, which is close to the latitude of Fayette County, West Virginia. This angle maximizes average annual solar production. Tighten all fasteners.

**Why before the panel:** Brackets must be in their final adjusted position before the panel is attached. Trying to adjust bracket angle with the panel already on the bracket adds weight, torque stress, and the risk of dropping the panel. Adjust first, then load.

**Why this tilt angle:** Solar panels produce the most power over the course of a year when they face due south and are tilted at an angle roughly equal to the local latitude. At approximately 38 degrees latitude, a 37–40 degree tilt is a practical target. The difference between optimal and a few degrees off is small in daily output terms. The difference between a fixed tilt and a panel laid flat or near-vertical is significant. Get it close to the target. Exact precision is not required.

**What to check before moving on:** Verify the brackets are at the same angle on both sides. Uneven brackets cause the panel to rack and stress the frame. Confirm all bracket fasteners are tight enough that the bracket does not shift when pushed.

**Lesson for future sites:** If a future site is shaded during part of the day — by a building, trees, or terrain — the optimal tilt angle may differ from latitude, and panel placement becomes more important than angle. Note the shading conditions at this site for comparison. At this location, note the direction the panel faces and whether any seasonal shadows affect it.

---

### Step 3: Mount the solar panel to the brackets

**What to do:** Lift the panel into position on the brackets. Attach it using the hardware specified for the bracket type. Do not overtighten fasteners against the panel frame — the panel frame is aluminum and will deform under excessive force. Snug and firm is correct. Crank and strip is damage.

**Why at this stage:** The panel is the heaviest single component in this phase. Mounting it after the brackets are set and confirmed means the crew is handling the panel once, in a controlled environment, rather than repositioning it multiple times.

**What to check before moving on:** The panel should be solidly on the brackets with no rocking or shifting. Verify that the panel cable (the pigtail that comes from the back of the panel) is accessible and not pinched against the bracket or the frame.

**Why the cable matters now:** The panel cable needs a clear path to the charge controller inside the enclosure. If the cable is pinched or routed in a direction that creates a sharp bend, it can fail from abrasion or fatigue over time. Route the cable loosely along the frame with enough slack that wind movement does not stress the connection point.

**Safety note during this step:** A solar panel in daylight is generating voltage as soon as it is uncovered. Do not touch the bare cable connectors with bare hands while the cable is exposed. Keep the panel covered with an opaque material — a piece of cardboard, a moving blanket, or the panel's original packaging — until the cable is safely connected to the charge controller. This is not optional. This is how panels are handled in field conditions.

**Lesson for future sites:** Panel handling in the field is a two-person job. One person holds the panel in position; the other drives the fasteners. A panel dropped on uneven ground or against a mounting pole is damaged and must be replaced. Do not rush this step.

---

### Step 4: Install the weatherproof electronics enclosure

**What to do:** Mount the weatherproof enclosure to the support frame or to the structure designated for it. The enclosure will house the charge controller, the fuse block, and the DC wiring terminals. Mount it with the cable entry ports facing down or to the side, never up. Confirm the enclosure door opens fully without obstruction so the charge controller can be accessed after installation.

**Why at this stage:** The enclosure must be mounted and its position confirmed before any wiring is run, because the wire lengths are determined by the distance between the panel, the battery, and the enclosure. Running wires before the enclosure is in its final location may result in wires that are too short or excessively long.

**Why the entry port direction matters:** Enclosures with cable entry ports facing up collect water at the entry point. Water follows the wire into the enclosure over time, even with cable glands installed. Ports facing down or sideways allow any water that reaches the entry point to drain away rather than pool. At this site specifically, Appalachian precipitation patterns include heavy rain, ice, and driven precipitation. Plan accordingly.

**What to check before moving on:** The enclosure is mounted solidly, the door opens fully, and the proposed cable entry points are accessible from the direction the wires will come from.

**Lesson for future sites:** Enclosure placement is often treated as a secondary decision. At this site, establish the habit of treating it as a primary decision. Where the enclosure goes determines where every wire goes. Getting that right first makes the wiring phase faster and cleaner.

---

### Step 5: Install the charge controller inside the enclosure

**What to do:** Mount the MPPT charge controller inside the enclosure on the mounting surface provided. Most MPPT controllers are designed for DIN rail or direct screw mounting. Follow the controller's mounting instructions. Confirm there is clearance above and below the controller for any required ventilation — MPPT controllers generate heat during charging and need airflow even inside an enclosure.

**Why before wiring:** The controller must be in its final position before any wires are run to it, for the same reason as the enclosure — wire length is determined by the distance between the endpoints. Mounting the controller first establishes that endpoint.

**What to check before moving on:** The controller is secure, the display or indicator lights are visible with the door open, and the terminal blocks are accessible for wiring.

**Why the display matters:** The charge controller's display is the primary diagnostic tool for the solar system. If a problem occurs after installation — the battery not charging, the system showing low voltage, an overload fault — the crew or a technician will need to read the display to understand what is happening. If the display is inaccessible with the enclosure closed, or obscured by other hardware, diagnosing problems becomes significantly harder. Mount the controller so its display is readable with the enclosure door open and at eye level if possible.

**Lesson for future sites:** At this pilot site, note the specific MPPT controller model used and document what each indicator light and display reading means. That documentation does not exist in a form H4H can use unless the crew captures it here.

---

### Step 6: Install the battery in its battery box

**What to do:** Place the 12V 100Ah LiFePO4 battery into the NOCO BG31 or equivalent battery box. Secure the box lid or strap according to the battery box instructions. Position the battery box in its designated location — typically at the base of the support frame or in a secure outdoor location adjacent to it. Confirm the battery terminals are accessible for wiring.

**Why the battery goes in the box before wiring:** A battery outside its box is an exposed electrical hazard. The terminals of a 12V 100Ah battery can deliver enough current to cause severe burns, start fires, and damage tools if a wrench or other metal object bridges the positive and negative terminals. The battery box is not decoration — it is protection. The battery does not come out of its box once it is in, except for service.

**Why LiFePO4 specifically:** LiFePO4 chemistry is more stable, longer-lived, and safer than lead-acid or standard lithium alternatives in outdoor applications. It handles partial states of charge without damage, which is important in a solar application where the battery may not reach full charge every day. It also handles cold temperatures better than lead-acid. For a location in Fayette County that will see winter temperatures below freezing, LiFePO4 is the correct chemistry.

**What to check before moving on:** The battery is in the box, the box is secure, and the terminals are accessible. Do not connect any wires yet.

**Why not connect yet:** Fuses are not installed yet. Connecting wires to an unfused battery creates a direct short-circuit path through any wiring error. The next step installs the fuse protection that makes it safe to complete the circuit.

**Lesson for future sites:** Document the battery model, serial number, and installation date here at this pilot site. LiFePO4 batteries have a cycle life that should be tracked. Knowing when the battery was installed and what conditions it has operated in helps H4H plan for eventual replacement before the battery fails unexpectedly.

---

### Step 7: Install the fuse block or DC bus bar

**What to do:** Mount the fuse block or bus bar inside the weatherproof enclosure. Connect the positive wire from the battery to the input of the fuse block first. Do not connect the panel or any loads until the fuse block is in place and the fuse or breaker is rated correctly for the system.

**Fuse sizing for this system:** The charge controller in this build is rated at 20A. The fuse between the battery and the controller should be sized at or slightly above the controller's maximum current rating — in this case, a 25A or 30A fuse is appropriate. Do not use a fuse significantly larger than the rated current, as an oversized fuse defeats the purpose of fuse protection.

**Why the fuse goes in before any connections are completed:** A fuse between the battery and the rest of the system is the only thing that stops a wiring fault from becoming a fire. If a wire is incorrectly connected, abraded through to a metal surface, or accidentally shorted during a future maintenance visit, the fuse opens the circuit before current can build up to the level that causes heat, melting, or ignition. Without a fuse, the battery will deliver as much current as the fault demands until something burns.

**What to check before moving on:** The fuse block is mounted, the fuse is correctly rated, and the connection from the battery positive terminal to the fuse block input is made. Nothing else is connected yet.

**Lesson for future sites:** Fuse sizing is a calculation, not a guess. For any future site, document the panel wattage, the controller rating, and the load current draw. The fuse should protect the wiring, not the equipment. Size the fuse to the lowest-rated wire in the circuit, not to the equipment.

---

### Step 8: Run and connect the DC wiring

**What to do:** Run all DC wiring between the panel, the charge controller, the fuse block, and the battery. Follow this connection sequence:

1. Connect the solar panel cable to the PV input terminals on the charge controller. Keep the panel covered during this step.
2. Connect the output terminals of the charge controller to the battery side of the fuse block.
3. Connect the fuse block output to the battery positive terminal.
4. Connect the battery negative terminal to the common negative bus.
5. Remove the panel cover and confirm the controller powers on and recognizes the panel.

**Why this specific sequence:** The charge controller must see the battery before it sees the panel. Most MPPT controllers initialize by reading battery voltage first. If the panel is connected before the battery, the controller may fault, misread the system voltage, or fail to initialize correctly. Follow the sequence in the controller's installation manual if it differs from what is described here, as different controllers have different initialization requirements.

**Wire routing:** All DC wires should run inside conduit or along protected surfaces where possible. Any wire that runs outdoors between the panel and the enclosure must be rated for UV exposure and outdoor use. Secure wires every 18–24 inches with UV-rated cable ties or clips. Do not allow wires to rest against sharp edges, corners of the frame, or the panel mounting hardware.

**Why wire routing matters:** A wire that abrades through its insulation against a sharp edge does not fail immediately. It fails weeks or months later when corrosion and movement have worn through the insulation. By that point, the fault is hard to trace and may have already caused intermittent power problems that look like equipment failures. Route wires cleanly the first time.

**Heat shrink and terminal protection:** All crimp connections must be covered with heat shrink tubing after the connection is made. All terminals exposed to the outdoor environment must be covered or sealed. The outdoor sealant (Dicor 501LSW-1 or equivalent) is appropriate for sealing any point where a wire passes through the enclosure wall.

**What to check before moving on:** All connections are made, all terminals are covered, all wires are secured, and the charge controller display shows battery voltage and panel input. If the controller shows a fault code, consult the controller manual before proceeding.

**Lesson for future sites:** At this pilot site, photograph every wire run before the enclosure is closed. The photographs should show where each wire enters and exits the enclosure, how it is routed along the frame, and where it terminates. Those photographs are the wiring diagram for this site. A written wiring diagram produced after the fact from memory is less reliable than a photograph taken at the time of installation.

---

### Step 9: Install grounding hardware if required

**What to do:** If site conditions require grounding — which they do at any site where the system is mounted on a conductive pole, near trees, or in an exposed location — drive the copper grounding rod into the ground adjacent to the support frame. Connect the grounding wire from the frame to the rod using the included clamp. Connect the system's negative bus to the ground rod.

**Why grounding matters at this site specifically:** The Mount Hope walking trail installation is an outdoor site in an elevated area of West Virginia. Lightning strikes to trees and structures are not uncommon. A grounded system provides a low-resistance path for lightning-induced surge current to follow into the earth rather than through the electronics. It also reduces the risk of dangerous voltage buildup on the metal frame in the event of a wiring fault.

**Why this is listed as conditional:** Grounding requirements depend on local electrical code, the mounting surface (grounded structure versus isolated frame), and the specific equipment used. At this pilot site, confirm with H4H whether the installation location requires formal grounding under local ordinance. Document that decision here so future sites can reference it.

**What to check before moving on:** If grounding is installed, the rod is driven to at least 18 inches of depth, the clamp is tight against a clean metal surface (not painted or corroded), and the grounding wire is secure at both ends.

---

### Step 10: Verify weather protection and close the enclosure

**What to do:** Before closing the enclosure permanently, verify the following:

- All cable glands are tightened against the cables passing through them.
- No wire is pinched by the enclosure door or its gasket.
- The enclosure gasket is clean and seated properly around its full perimeter.
- The enclosure latches close firmly.
- No wire exits the enclosure through a hole that is not sealed with a gland or sealant.

Apply Dicor 501LSW-1 or equivalent outdoor sealant to any entry point that is not fully sealed by a cable gland. Allow sealant to skin over before the installation is considered sealed.

**Why this step cannot be skipped:** An enclosure that is mounted but not properly sealed is not weatherproof. Moisture ingress into the enclosure will corrode connections, damage the charge controller, and eventually cause failures that are difficult to diagnose because the damage accumulates over months. The gasket and cable glands are not cosmetic features — they are the primary protection for everything inside.

**What a correctly completed Phase 6 looks like:** The charge controller display is showing battery voltage and solar input. The battery box is closed and secured. All wires are routed cleanly along the frame with no sharp bends or exposed terminations. The enclosure is latched and sealed. The panel is clean and oriented toward the south at the correct tilt angle. No wires hang loosely from any connection point. The support frame does not move when pushed.

---

## What Happens If This Phase Is Rushed or Skipped in Part

The following are documented failure modes from similar installations, included here as learning references:

**Fuse omitted:** A wiring fault during a maintenance visit at a similar site caused a direct short that melted DC wiring inside the enclosure and required replacement of the charge controller and wiring harness. The fuse would have opened the circuit before any damage occurred. Cost of adding a fuse correctly during installation: under ten dollars and fifteen minutes. Cost of the repair: several hundred dollars and a multi-day service outage.

**Enclosure cable glands not tightened:** Water infiltration over a single winter season caused corrosion on the charge controller terminals at a comparable outdoor installation. The failure appeared as intermittent charging rather than complete system failure, making it difficult to diagnose remotely. The enclosure had to be opened, cleaned, and resealed. All of that work was avoidable.

**Panel tilt not set correctly:** A panel mounted near-flat (less than 10 degrees tilt) at a northern latitude produced 30–40 percent less energy over a year than the same panel would have produced at the correct tilt. In a solar-powered remote system, that difference determines whether the battery stays charged through cloudy periods or depletes and leaves the connected devices without power.

**Wire routing against frame edges:** A wire run without protection against the metal edge of a mounting bracket abraded through its insulation over six months of wind movement. The resulting ground fault caused the charge controller to fault and shut down the system. The fault was not visible from the outside and required opening the enclosure and inspecting each wire to locate.

---

## What to Record When Phase 6 Is Complete

Before moving to Phase 7, the crew should record and photograph the following:

- Charge controller model, serial number, and firmware version if displayed.
- Battery model, serial number, voltage reading at time of installation, and state of charge if indicated by the controller.
- Panel model and serial number.
- Photograph of the complete assembled frame with panel in place.
- Photograph of the open enclosure showing controller, fuse block, and wiring.
- Photograph of the sealed enclosure with all cables exiting cleanly.
- Photograph of the grounding rod installation if applicable.
- Note of any deviation from the planned installation and the reason for it.

These records are the permanent reference for this site. They should be kept in H4H's installation records, not only on a crew member's phone.

---

## Carrying These Lessons Forward

At future sites, the core lessons from this phase are:

1. The support frame must be solid before anything is attached to it.
2. Brackets before panel. Enclosure before wiring. Fuse before connection.
3. Weather protection is not a finishing step — it is a requirement at every point where wiring enters or exits an enclosure.
4. The charge controller display is the primary diagnostic tool. Mount it where it can be read.
5. Photograph the wiring before the enclosure is closed. That photograph is the wiring diagram.
6. Document the specific equipment used at each site. Battery chemistry, controller model, and fuse rating all matter for future maintenance decisions.
