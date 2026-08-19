# Phase 7: Install Kiosk Hotspot Equipment
## Field Learning Guide — Mount Hope Walking Trail Pilot Site

---

## What This Document Is For

This document expands on Phase 7 of the installation workflow. It explains what the kiosk hotspot equipment is, why it is being installed the way it is, what each step accomplishes, and what the finished installation should look like. Because this is a pilot site, it also captures the thinking behind the decisions made here so that H4H can apply those lessons to future community installations.

---

## Site-Specific Context That Shapes Every Decision in This Phase

Before reading the step sequence, the crew needs to understand two facts about this specific site that directly affect how Phase 7 is planned and executed.

**Fact 1: The kiosk is less than 100 yards from 704 Main Street.**

That distance is short enough that the Starlink router's Wi-Fi signal may reach the kiosk without any additional hardware at the kiosk at all. A standard Starlink router has an indoor range of 200 feet or more under ideal conditions. Outdoors, with clear line of sight, that range can extend considerably further. Under 100 yards is approximately 270 feet — at the outer edge of what a Starlink router might cover outdoors under favorable conditions, and well within range if the router is positioned near a window or exterior wall facing the kiosk.

**Fact 2: There is a two-story building between the kiosk and 704 Main Street.**

This changes everything about Fact 1. A two-story building in the signal path between the router and the kiosk is a significant obstruction. Wi-Fi signals, particularly the 5 GHz band that Starlink routers favor for performance, do not pass cleanly through masonry, brick, or dense wood-frame construction. The 2.4 GHz band penetrates solid structures better but still loses substantial signal strength through two exterior walls and the interior mass of a full building. Whether the kiosk receives a usable signal from the Starlink router depends on what that building is made of, where the router is placed inside 704 Main Street, and whether there is any partial line of sight around the edges of the building rather than directly through it.

**What this means for the Phase 7 equipment list:**

The Raspberry Pi, the MicroSD card, the power supply, and the display cable are on the current parts list because they were planned as the mechanism for delivering hotspot service at the kiosk. But if the Starlink router's signal reaches the kiosk reliably without any additional hardware — which is possible given the short distance, even with the obstruction — none of that equipment is needed. The public simply connects to the Starlink router's network from the kiosk, the same way they would from inside the building.

**This means a signal test must happen before the equipment decision is final.**

The signal test is Step 2 of this phase. It is the decision point that determines whether Steps 5 through 7 — which involve the Raspberry Pi — are performed at all, or whether an alternative approach is used instead. Do not order or stage the Raspberry Pi equipment until the signal test result is known, or be prepared to hold that equipment if the test shows it is not needed.

---

## What Phase 7 Covers

Phase 7 installs the public-facing hotspot equipment at the existing kiosk structure on the Mount Hope walking trail. This is the point in the installation that the public will actually interact with. Every other phase installs infrastructure that supports this location. This phase makes the service visible and accessible to the people the project is designed to serve.

**The equipment installed in this phase depends on the signal test result described in Step 2.**

If the Starlink router signal reaches the kiosk reliably:
- Wi-Fi hotspot sign (mounted at the kiosk for public visibility)
- Outdoor power cable run is not needed for hotspot function, though it may still be needed for the LoRa node
- No enclosure, no Raspberry Pi, no power supply, no MicroSD card

If the signal does not reach the kiosk reliably, one of two paths is taken:

**Path A — Outdoor Wi-Fi access point:**
- Outdoor weatherproof Wi-Fi access point (TP-Link EAP225-Outdoor or equivalent)
- Outdoor-rated PoE Ethernet cable run from the indoor switch to the access point
- PoE injector or PoE-capable switch port at the indoor end
- Mounting hardware for the access point at or near the kiosk
- Wi-Fi hotspot sign

**Path B — Raspberry Pi acting as a wireless bridge and access point:**
- Raspberry Pi (installed inside the weatherproof outdoor enclosure)
- MicroSD storage card (pre-imaged before site visit)
- Raspberry Pi power supply
- Short HDMI or display adapter cable (for diagnostic use if needed)
- Outdoor weatherproof enclosure (Sixfab IP65 or equivalent)
- Outdoor power cable (Southwire 12/3 SJTW or equivalent)
- Exterior cable glands
- Wi-Fi hotspot sign

Path A is the preferred option if the signal does not reach the kiosk. A purpose-built outdoor access point is more reliable, easier to maintain, and produces better coverage than a Raspberry Pi configured to replicate the same function. Path B is the fallback if Path A is not feasible for cost or procurement reasons at the time of installation.

H4H makes the path decision after the signal test result is reported. The crew does not make this call independently.

---

## Before Phase 7 Begins: What Must Already Be True

Phase 7 cannot start until the following conditions from earlier phases are confirmed:

- The existing kiosk structure has been inspected and confirmed structurally sound (Phase 4).
- The solar power system is installed and the charge controller shows the system is live (Phase 6).
- The indoor Starlink internet connection is confirmed active (Phase 5).
- The outdoor power cable path from the power source to the kiosk location has been confirmed clear and safe if a cable run is required by the signal test outcome.

If any of these conditions are not met, stop and report to H4H before proceeding.

---

## The Step Sequence and the Reason for Each Step

### Step 1: Inspect the existing kiosk structure

**Context for this site:** This kiosk has been standing on the Mount Hope walking trail for five years. That is not a reason to skip this inspection — it is the reason the inspection is mandatory. Five years of Fayette County winters, freeze-thaw cycling, summer humidity, UV exposure, and seasonal rainfall is enough time to degrade wood joinery, corrode metal fasteners, soften post bases where they contact soil or concrete, and create surface conditions that look intact from a distance but are not sound enough to carry additional hardware. A structure that was solid at installation is not assumed to be solid five years later. It is verified.

**What to do:** Before attaching any hardware to the kiosk, perform the following inspection systematically:

**Posts and base:**
Push each structural post from multiple directions with firm, deliberate pressure. A sound post does not move. Any movement at the base — rocking, shifting, or soft give — indicates that the post base has degraded, whether from rot, heaved concrete, or corrosion of any metal anchor hardware. Check the post bases visually at ground level. Probe any area where the post contacts soil or a concrete pad with a pocket knife or a screwdriver tip. Sound wood resists the probe. Rotted wood yields to it.

**Mounting surfaces:**
Press firmly on the surfaces where any enclosure or access point will be mounted. Solid surfaces do not flex or give. A surface that moves under hand pressure is not structurally adequate for mounted hardware, regardless of how it looks. If the kiosk is wood-framed, check the grain direction and surface condition of the proposed mount panel. Check for delamination on plywood panels — five-year-old exterior plywood in a high-humidity environment may have edge delamination that is not visible from the face.

**Roof or canopy:**
Confirm the roof is intact, that there are no gaps or warped sections that would allow direct rainfall onto the equipment area, and that the roof attachment points are secure. Check the underside of the roof for water staining, which indicates past infiltration and may indicate ongoing risk.

**Existing hardware and signage:**
Any fasteners, brackets, or signs already on the kiosk should be checked for security. A loose sign that falls onto newly mounted electronics is a preventable equipment damage event.

**Biological occupants:**
Five-year-old outdoor structures in West Virginia frequently house wasps, mud daubers, paper wasps, and occasionally rodents. Check enclosed spaces, underside cavities, and any hollow structural elements before beginning work. Do not reach into enclosed spaces without looking first.

**Why this level of inspection is required on a structure H4H knows:**
Knowing a structure's history is not the same as knowing its current condition. H4H installed this kiosk and has maintained the surrounding trail area, but the kiosk itself has not necessarily been assessed for mounting load readiness. Problems visible from a few feet away during a trail walk may not have triggered concern. Problems that appear when a crew member puts their hand on the post and feels it shift require immediate action.

**What counts as a stop-and-report condition:**
- Any post that moves under firm pressure.
- Any mounting surface that flexes under hand pressure.
- Any visible rot in structural members or mounting surfaces — probe anything suspicious.
- Roof damage that would expose the equipment area to direct rainfall.
- Any metal fastener at a load-bearing point that shows active corrosion (rust that flakes or powders, not surface discoloration).
- Active wasp or rodent activity that has not been cleared.

If any of these conditions exist, stop and contact H4H before mounting anything. The kiosk may need repair work before the installation continues. That work is not the crew's job to improvise — it is H4H's decision to authorize and scope.

**What healthy condition looks like at five years:**
A well-sited outdoor kiosk at five years in a protected trail location should still be fundamentally sound, with surface weathering — fading, minor surface checking in wood, some UV discoloration — that is cosmetic rather than structural. The inspection is not expected to find catastrophic failure, but it is designed to catch the specific degradation that five-year-old outdoor structures in this climate do develop and that matters for a mounted electronics installation.

**Lesson for future sites:** At any future site where H4H installs equipment on an existing structure, this inspection happens first regardless of how well H4H knows that structure. Age the inspection to the structure: a two-year-old kiosk gets a lighter check than a five-year-old one. Document the inspection result, including observations about remaining service life, so H4H can plan maintenance on the right timeline.

---

### Step 2: Signal test — determine whether the kiosk receives usable Wi-Fi from 704 Main Street

**What to do:** With the Starlink system active indoors at 704 Main Street, take a smartphone or laptop to the kiosk location and check the following:

1. Can the Starlink router's Wi-Fi network be detected at the kiosk?
2. If detected, what is the signal strength reading? On most devices, one or two bars is marginal. Three or more bars is usable.
3. With the device connected to the Starlink network at the kiosk location, run a speed test. A result of at least 5 Mbps download is the minimum for a functional public hotspot. Below that, the connection is technically present but practically unreliable for general public use.
4. Walk the full area around the kiosk that the public would occupy — not just the spot directly in front of it. If signal drops to one bar or disconnects at any point in that area, the coverage is inadequate.

**Why this test must happen before any hardware at the kiosk is committed:**
The two-story building between the kiosk and 704 Main Street may block the signal entirely, partially, or not at all depending on its construction and the router's placement. There is no way to know without testing. Ordering and installing a Raspberry Pi or an outdoor access point at the kiosk without first testing whether the router already reaches it is spending money and time on a problem that may not exist.

**What the building between the sites means for signal behavior:**
The two-story structure sitting in the signal path is the dominant factor in this test. Wi-Fi signal at 5 GHz — which Starlink routers favor for speed — loses roughly half its strength passing through a single standard interior wall, and significantly more through exterior walls and the mass of a full building. At 2.4 GHz the signal penetrates somewhat better but still degrades substantially. The likely outcome is that the signal is detectable at the kiosk but at reduced strength. Whether that reduced strength is adequate for public use is what the speed test determines, not the signal strength reading alone.

**Router placement at 704 Main Street matters:**
If the Starlink router is placed on the side of the building that faces away from the kiosk, the signal must travel through the full building width before reaching the kiosk. If it is placed near a window or on the wall closest to the kiosk, the signal path through the building is shorter and the result may be significantly better. Before concluding that additional hardware is required, confirm where the router is placed and whether moving it closer to the kiosk-facing side of the building changes the signal test result.

**Possible test outcomes and what each means:**

| Test result | What it means | What happens next |
|-------------|---------------|-------------------|
| Strong signal, speed test passes at kiosk | Router reaches the kiosk without additional hardware | No enclosure, no Pi, no power run needed for hotspot. Mount sign and proceed to Phase 8. |
| Weak signal, speed test marginal | Signal reaches the kiosk but is unreliable | Try moving the router closer to the kiosk-facing wall first. Retest. If still marginal, additional hardware is required. |
| No signal or unusable signal | Building is blocking effectively | Additional hardware is required. Report to H4H for path decision before proceeding. |

**What additional hardware options look like:**

If additional hardware is required, the preferred option is a purpose-built outdoor Wi-Fi access point — such as a TP-Link EAP225-Outdoor or equivalent — mounted at or near the kiosk and connected via a weatherproof Ethernet cable run from the indoor switch at 704 Main Street. This runs Power over Ethernet (PoE) so only a single cable is needed. No enclosure, no Raspberry Pi, no separate power supply at the kiosk. The access point is designed for outdoor use, handles weather independently, and is straightforward to maintain.

The Raspberry Pi path is a fallback option when the outdoor access point is not feasible for procurement or cost reasons. It requires more hardware, more installation steps, and more software configuration, and produces a result that is functionally similar but operationally more complex to maintain.

**Report the test result to H4H before any additional hardware is installed.** The crew does not select the path independently.

---

### Step 3: If additional hardware is required — run the outdoor cable to the kiosk

**What to do:** If the signal test confirmed that additional hardware is needed at the kiosk, run the appropriate cable from 704 Main Street to the kiosk before mounting any hardware at the kiosk end.

**For the outdoor access point path (Path A):**
Run a single outdoor-rated Cat6 Ethernet cable from the indoor network switch at 704 Main Street to the kiosk location. This cable carries both data and power via PoE. Use direct-burial rated or UV-jacketed outdoor Cat6 for any section that is exposed to weather or sunlight. Secure the cable along its run with UV-rated clips or cable ties spaced no more than 24 inches apart. Protect any section crossing pedestrian areas by routing above head height, below grade in conduit, or along a structure that keeps it out of the path of trail users.

**For the Raspberry Pi path (Path B):**
Run an outdoor-rated 12/3 SJTW power cable from the solar system's AC output (via inverter) or from an appropriate DC power source to the kiosk. Additionally, if the Pi will connect to the indoor network via wired Ethernet rather than wireless, run an outdoor Cat6 cable as described above. If the Pi connects wirelessly, the power cable is the only run required.

**Why cable runs happen before hardware is mounted at the kiosk:**
Cable length is determined by the actual route the cable takes, not the straight-line distance. The route around structures, along surfaces, and through any conduit sections may be significantly longer than 100 yards of straight-line distance. Running the cable first establishes how much is needed and confirms the route is clear before the crew commits hardware to the kiosk end.

**What to check before moving on:** The cable is routed and secured along its full length. No section crosses a pedestrian area without protection. The cable end at the kiosk has enough slack to reach the intended hardware mount point without pulling tight.

---

### Step 4: Mount the hardware at the kiosk

**This step varies by path.**

**If the signal test showed the router reaches the kiosk (no additional hardware needed):**
There is nothing to mount in this step. Proceed to Step 7 — the sign.

**Path A — Outdoor access point:**
Mount the outdoor access point at the kiosk at a height and orientation that maximizes coverage of the area where trail users will stand. Most outdoor access points have a preferred orientation marked in their installation guide — follow it. Use stainless steel fasteners. Connect the PoE Ethernet cable to the access point's port. The access point will power on when the other end of the cable is connected to the PoE switch port or injector indoors.

**Path B — Raspberry Pi in outdoor enclosure:**
Mount the weatherproof outdoor enclosure (Sixfab IP65 or equivalent) to the kiosk mounting surface using stainless steel wood screws long enough to reach solid wood. Mount the enclosure at a height that is within the protected area of the kiosk canopy, reachable for maintenance without a ladder, and not so low that it risks direct water contact at its base.

Install cable glands in the enclosure entry ports before running any cables through them. Each cable entering the enclosure needs its own gland. Tighten the gland body to the enclosure wall first, route the cable through it, and tighten the gland against the cable jacket last. Any unused ports must be plugged with the included blanking plug and sealed with outdoor sealant.

**Why stainless fasteners at a five-year-old wood kiosk:**
The existing fasteners in this kiosk have had five years of corrosion exposure. Any new fasteners added now should be stainless, both because the outdoor environment requires it and because mixing stainless with corroded zinc or galvanized hardware at the same location creates a galvanic corrosion situation that accelerates degradation of the non-stainless material. Use stainless throughout.

---

### Step 5: Prepare and install the Raspberry Pi (Path B only)

**Skip this step if Path A or the direct-signal outcome applies.**

**What to do:** Outside the enclosure, in a clean and protected environment — the interior of a vehicle, a table inside 704 Main Street, or a staging area shielded from wind and moisture — complete the following:

- Confirm the MicroSD card was imaged with the correct operating system and hotspot configuration before arriving on site. If it was not pre-imaged, this must happen before the Pi is placed in the enclosure.
- Insert the MicroSD card into the Raspberry Pi.
- Inspect the Pi board for physical damage — bent pins, cracked components, or missing connectors.
- Connect the short HDMI adapter if a diagnostic display will be used during initial startup.

Place the Pi into the enclosure on the mounting standoffs. Secure it with the appropriate fasteners. Connect the power supply to the outdoor power cable. Connect the power supply output to the Pi's USB-C power input. If a wired network connection is being used, connect the Ethernet cable to the Pi's Ethernet port and route it through its own cable gland. Do not power on yet.

**Why the Pi is handled outside the enclosure:**
The Pi board is small and its mounting hardware — standoffs, screws — requires careful alignment. Handling these components in a protected environment reduces the risk of dropping the board, losing small fasteners, or incorrectly seating the MicroSD card. Once mounted, the Pi should not need to be removed unless there is a hardware failure.

**Why not power on yet:**
All connections must be complete before power is applied. The sequence is managed in Phase 10.

---

### Step 6: Confirm indoor network configuration supports the kiosk path chosen

**What to do:** Before closing up any hardware at the kiosk, confirm the following at the indoor network equipment:

**For Path A (outdoor access point):** Confirm the PoE switch port or PoE injector that the access point's cable connects to is active and that the access point receives power (its indicator light should be on). Confirm the access point is broadcasting a network with the correct name and password.

**For Path B (Raspberry Pi):** Confirm the indoor network the Pi is connecting to — either via Ethernet or wireless — is active and that the Pi's configured network name matches it.

**For the direct-signal outcome (no additional hardware):** Confirm the Starlink router's network name and password are what will be communicated to the public via the sign. The network name should be something recognizable as belonging to H4H and the trail project, not the default Starlink network name.

**Why this step exists:** A hotspot sign pointing the public to a network that does not exist, or that requires a password the public does not have, is worse than no sign at all. It creates a failed expectation at the exact moment a community member tries to use the service for the first time. Confirm the network is correctly named and accessible before the sign goes up.

---

### Step 7: Mount the hotspot sign at the kiosk

**What to do:** Mount the Wi-Fi hotspot sign at the kiosk in a location that is:

- Visible to a person approaching the kiosk from the walking trail.
- At eye level or close to it for an adult standing in front of the kiosk.
- Not obstructed by any other signage, hardware, or structural element.
- Secured with stainless fasteners appropriate for the kiosk surface.

The sign should include the network name the public will connect to. A generic Wi-Fi symbol without a network name leaves people guessing. A sign that says "Free Wi-Fi — connect to [network name]" tells them exactly what to do.

Apply outdoor-rated sealant over any fastener holes drilled through the kiosk canopy or roof to prevent water infiltration at those points.

**Why the sign is the last item in this phase:** All hardware is in place and the network is confirmed before the sign goes up. The sign tells the public the service is here. If the service is not yet confirmed ready, the sign creates a promise that cannot be kept. That damages community trust in the project and in H4H. The sign goes up when the service is ready, and not before.

**Lesson for future sites:** Note how trail users respond to the sign in the first weeks of operation. Does the network name make sense to someone who knows nothing about the project? Do people understand it is free? That feedback shapes how signage is designed at future sites. The sign is the first interaction the public has with this service.

---

### Step 8: Secure and protect all exposed wiring

**What to do:** Walk the full cable run from 704 Main Street to the kiosk and confirm:

- Every section of exposed cable is secured to a surface or structure.
- No cable hangs freely where wind, foot traffic, or equipment contact could pull it.
- All connections at both ends of every cable are covered with appropriate strain relief.
- Any cable passing through a hole in wood or metal is protected by a grommet or sealed cable gland — not resting against the raw edge of the hole.
- All cable glands on any enclosure are tightened against the cable jackets.
- Outdoor sealant is applied to any cable entry point not fully sealed by the gland alone.

**Why this step is its own item:** Exposed cables in a public outdoor location face forces that indoor cables do not. Wind causes repeated flexing at stress points. Curious hands pull at accessible cables. Rodents investigate cables at accessible heights. Rain infiltrates any unsealed opening. A cable run that is clean and fully protected at the time of installation is the difference between a system that runs for years and one that fails in its first season.

**What a correctly completed Phase 7 looks like:** Regardless of which path was taken, the kiosk area has a visible, legible hotspot sign. Any hardware added — whether an outdoor access point or a Raspberry Pi enclosure — is solidly mounted on the inspected and confirmed kiosk structure. All cables are secured along their runs without hanging sections or sharp bends. All outdoor penetrations and enclosure entries are sealed. The kiosk looks maintained, intentional, and ready for public use.

---

## What Happens If This Phase Is Rushed or Skipped in Part

**Signal test skipped, hardware ordered blind:** At under 100 yards with a two-story building in the path, the signal result is genuinely uncertain. If the test is skipped and hardware is ordered and installed based on an assumption, there is a meaningful probability that the hardware was unnecessary — or that the wrong hardware was chosen. Either outcome wastes money and crew time on a return visit.

**Structural inspection skipped on an aged structure:** Five-year-old outdoor wood structures in high-humidity Appalachian climates develop rot at post bases, fastener points, and anywhere water can pool or wick into end grain. A post base that has lost structural integrity may hold the original kiosk sign without visible problem and still fail under the additional load of mounted electronics in a wind event. Familiarity with the kiosk is not a substitute for probing the posts.

**Network name not confirmed before sign goes up:** A sign pointing to a default Starlink network name, or to a network that requires a password the public does not have, produces a failed first impression that is difficult to walk back once community members have encountered it.

**Cable glands not fully tightened:** Moisture infiltration through a loose gland causes gradual hardware degradation that presents as intermittent failures months after installation, not at the time the problem was created.

**MicroSD not pre-imaged (Path B):** Imaging a card in the field on an outdoor site consumes hours and typically requires a return trip for the testing phase.

---

## What to Record When Phase 7 Is Complete

Before moving to Phase 8, record the following:

- Signal test result: signal strength reading and speed test result at the kiosk location.
- Router placement at 704 Main Street at the time of the signal test.
- Path selected (direct signal / Path A / Path B) and the reason.
- If Path A or B: hardware model and serial number of the access point or Raspberry Pi.
- If Path B: MicroSD card image version.
- Photograph of the kiosk structural inspection — post bases, mounting surface, roof underside.
- Photograph of any hardware mounted at the kiosk before any enclosure is closed.
- Photograph of sealed enclosure or mounted access point in final position.
- Photograph of the hotspot sign in its installed position.
- Photograph of the cable run from 704 Main Street to the kiosk.
- Note of any deviation from the planned installation and the reason for it.

---

## Carrying These Lessons Forward

At future sites, the core lessons from this phase are:

1. Test the signal before ordering hardware. A short distance and a known building obstruction produce an uncertain result that only a field test resolves. Assuming the answer costs money either way — either hardware bought unnecessarily, or a return trip to add hardware that was skipped.
2. A two-story building between a router and a public hotspot location is a meaningful obstruction at 5 GHz and a partial obstruction at 2.4 GHz. Never assume signal passes through a building without testing it.
3. Router placement inside the building matters. Closer to the wall facing the hotspot location means less building material in the signal path.
4. A purpose-built outdoor access point is operationally simpler than a Raspberry Pi performing the same function. Prefer it when the budget allows.
5. Structural inspection is especially necessary on a structure you know. Familiarity creates assumptions. Five years of Appalachian weather changes a structure. Assess it with your hands, not your memory.
6. The network name on the sign must be the network name that actually works at the kiosk. Confirm this before the sign goes up.
7. The sign goes up after the service is confirmed ready. Not before.
8. This kiosk is the public face of the project. How it looks, how clear the signage is, and whether the service works on first contact all shape the community's trust in H4H and in everything that comes after this installation.
