# Syria PvP Persistent Campaign Mission

## Why a new mission?
Because it is trying to solve the following problems:
Yes. This design solves these problems:

* **Infinite-aircraft mindset**
  Limited airframes make aircraft preservation important. Players must RTB instead of treating jets as disposable missiles with cockpits.

* **Infinite-weapons feeling**
  No constant weapon warehouse refill. Aircraft weapons become scarce and replenished slowly, probably weekly.

* **Fuel being meaningless**
  Refineries and fuel stock become strategic assets. Fuel supports flying, airfield operation, and airframe replacement.

* **Static front-line boredom**
  Large POI zones create natural campaign objectives in the middle of the map.

* **Whole-map chaos**
  Red and Blue start in limited areas, with a central contested belt. The fight has shape.

* **Too many tiny objectives**
  Fewer, larger zones reduce noise and make each objective worth planning around.

* **Single truck captures an entire refinery nonsense**
  High `numCap` and `numKeep` values force proper ground commitment.

* **Easy ownership flipping**
  `easyContest = false` makes captured POIs harder to neutralize or steal back casually.

* **Air-only gameplay dominance**
  Ground commanders, convoys, armor, IFVs, SHORAD, and helicopters all matter.

* **Ground commanders having no real job**
  They assemble produced units, reinforce POIs, move convoys, protect logistics, and support captures.

* **Factories all producing generic stuff**
  Specialized factories make specific places strategically valuable: tank factory, IFV factory, SHORAD factory, radar factory, etc.

* **No reason to fight over specific areas**
  Each POI gives a specific benefit. Teams will fight over what they need, not just whatever is nearby.

* **Airfields being captured just for map painting**
  Airfields are consumers. They are useful only if supplied and protected.

* **Forward bases becoming magical self-sustaining islands**
  A captured airfield without fuel, aircraft, and logistics is a liability, not a win button.

* **Home-base rush cheese**
  Home bases are heavily defended and strategically important, but not easy capture targets.

* **Parked aircraft being irrelevant scenery**
  `StopGap` + `SittingDucks` makes parked aircraft real targets. Ramp strikes can reduce enemy airpower.

* **No consequence for bad pilot decisions**
  Losing aircraft affects the whole coalition inventory.

* **No recovery path after aircraft losses**
  Fuel-for-airframes allows recovery, but only through strategic fuel surplus and delayed delivery.

* **Instant replacement arcade behavior**
  Purchased aircraft arrive later, not instantly.

* **Refineries being decorative map objects**
  They become fuel-production nodes and indirectly airpower-recovery nodes.

* **Recon being optional fluff**
  Recon Mode makes helicopters, scouts, and recon aircraft valuable for finding convoys, defenses, and weak POIs.

* **Helicopters having no strategic role**
  Chinooks, Hueys, Kiowas, etc. become useful for capture support, troop movement, recon, and logistics.

* **SHORAD and radar assets appearing magically**
  They are produced slowly by specific factories, making air-defense buildup deliberate.

* **Too much message spam**
  Live messages stay minimal. Deeper status can be queried via F10.

* **Overbuilding with custom static objects**
  Existing Syria map assets can be used. DML zones provide the game logic.

* **Mission becoming script soup too early**
  DML handles ownership, factories, recon, parked aircraft, and messaging. Only the fuel-for-airframes mechanic likely needs a small custom script.

* **Lack of campaign economy**
  The design creates separate economies: fuel, airframes, ground vehicles, and strategic factories.

* **Lack of strategic choice**
  Teams must decide whether to spend fuel on flying, save fuel for aircraft replacement, attack refineries, defend factories, or push for airfields.

* **PvP becoming just CAP vs CAP**
  CAP still matters, but now it supports actual strategic goals: protecting convoys, enabling captures, defending refineries, and stopping strikes.

* **Small squadron spread too thin**
  Fewer large objectives focus combat into understandable areas.

* **Mission progress feeling abstract**
  Progress is visible: captured POIs produce resources, airfields become usable, aircraft inventories shrink or recover.

* **Lack of operational identity**
  The mission becomes a combined-arms logistics war, not just random sorties on a large map.


A persistent multiplayer PvP mission for **DCS World** on the **Syria** map.

The mission is designed as an operational campaign, not a simple front-line brawl. Red and Blue begin with limited but well-equipped home areas. Between them sits a contested belt of major economic and military points of interest: refineries, ports, vehicle factories, radar production sites, armored depots, SHORAD depots, and forward airfields.

The campaign revolves around capturing, holding, supplying, defending, and destroying these assets.

The guiding principle is simple:

> Airpower wins battles, logistics wins campaigns, and careless pilots turn expensive aircraft into aluminum confetti.

---

## Mission Concept

Red and Blue start with a small, secure part of the map. The central area contains large strategic POI zones. These zones are not just decorative objectives. They drive fuel supply, ground vehicle production, airfield usefulness, and campaign momentum.

Players and ground commanders must fight to control these assets and then use them to expand across the map.

The mission is intended to run continuously on a multiplayer server.

---

## Design Goals

- Create a persistent PvP campaign on the Syria map.
- Avoid full-map chaos by using a limited number of large strategic zones.
- Make aircraft and pilots valuable through finite airframes and vulnerable parked aircraft.
- Make logistics and ground commanders matter.
- Encourage planning, reconnaissance, convoy assembly, interdiction, escort, SEAD, CAS, and strategic strikes.
- Avoid infinite-weapons and magic-warehouse behavior.
- Use DML zones and map-native assets wherever possible, rather than hand-building every site with static objects.
- Keep messages and player feedback useful, but not spammy.
- Build a playable v1 first, then expand persistence and automation later.

---

## Core Gameplay Loop

```text
Players fly missions
        ↓
Recon identifies enemy units and weak points
        ↓
Strikes, CAS, and ground commanders shape the battle
        ↓
Ground forces capture large strategic zones
        ↓
Owned factories and refineries begin producing resources
        ↓
Convoys and logistics sustain airfields and forward positions
        ↓
Coalitions expand only where they can support operations
```

---

## Main Campaign Mechanics

### 1. Limited Airframes

Both coalitions have a finite pool of available aircraft.

Aircraft availability is based on the number of squadron members who own each module, not only on who is expected to fly on a given Sunday.
The numbers can be taken from the MyModules discord channel

Example starting inventory concept:

| Airframe | Example count |
|---|---:|
| F-16C | 56 |
| F/A-18C | 48 |
| F-4E | TBD |
| F-5E | TBD |
| Mirage 2000C | TBD |
| Mirage F1 | TBD |
| UH-1H | TBD |
| AH-64D | TBD |
| CH-47F | TBD |
| OH-58D | TBD |

Saving aircraft is central to the air campaign.

Aircraft are not disposable. A successful mission is not only about destroying targets, but also about bringing aircraft home.

---

### 2. Parked Aircraft and Airbase Vulnerability

The mission should use:

- `StopGap`
- `SittingDucks`
- `Valet`

The intent:

| DML module | Intended use |
|---|---|
| `StopGap` | Fill empty client slots with visible parked aircraft stand-ins. |
| `SittingDucks` | Make parked stand-ins vulnerable so destroyed aircraft can block corresponding slots. |
| `Valet` | Provide airbase/FARP entry, departure, greeting, and base-status behavior. |

This allows airbases to become meaningful targets without requiring artificial scoring rules.

A successful ramp strike can reduce the enemy's available airframes.

Home bases are heavily defended and well equipped, but they are not meant to be completely immune to enemy action.

---

### 3. Strategic POI Zones

The central belt of the map contains large strategic zones.

These are not small circles around single objects. A refinery zone may include:

- refinery
- tank farm
- harbor
- loading area
- nearby road/rail access
- associated defensive positions

The coalition must control the whole operational area, not merely park one vehicle next to a fuel tank.

Example strategic zones:

| Zone type | Example effect |
|---|---|
| Oil refinery + port | Produces fuel for owned and supported airfields. |
| APC factory | Produces APCs or troop carriers. |
| IFV factory | Produces infantry fighting vehicles. |
| Tank factory | Produces tanks at a slower rate. |
| SHORAD factory | Produces short-range air defense units. |
| Radar factory | Produces EWR/search radar assets very slowly. |
| Forward airfield | Becomes useful only if supplied. |

---

### 4. Zone Capture Rules

Capturing a POI should require a serious ground force.

Recommended starting values:

| Zone type | `numCap` | `numKeep` |
|---|---:|---:|
| Factory / depot | 8-10 | 4-5 |
| Refinery + port complex | 10 | 5 |
| Forward airfield | 12-16 | 6-8 |
| Home base | Not normally capturable | N/A |

Recommended DML behavior:

```text
easyContest = false
```

Reason:

A zone should not become neutral just because a single enemy scout enters it. Once a coalition captures a refinery, factory, or port complex, the enemy must bring enough force to actually take it.

The preferred capture model is:

```text
Enough attacking ground units enter the zone
No sufficient defending force remains
Zone changes owner
The new owner must leave enough units behind to hold it
```

Tanks, IFVs, APCs, infantry, and other ground units can all contribute to capture, but the defense layout should make proper force composition necessary.

---

### 5. Refineries and Fuel

Oil refineries are major strategic assets.

Fuel should be produced continuously and delivered periodically.

Recommended rule:

```text
Oil refinery owned by coalition
        ↓
Fuel is added every 2 hours
        ↓
Only airfields owned and supported by the same coalition receive fuel
```

If the refinery is neutral or unsupported, fuel flow stops.

Suggested logic:

| Refinery owner | Effect |
|---|---|
| Blue | Blue-supported airfields receive fuel. |
| Red | Red-supported airfields receive fuel. |
| Neutral | No coalition receives fuel. |

Airfields are consumers. They become valuable only when the coalition can support them.

---

### 6. Factories Instead of Generic Warehouses

This mission does not use a generic warehouse that produces every type of unit.

Instead, factories are specialized.

The intent is to make specific geographic locations strategically valuable.

Example:

| Factory | Produces |
|---|---|
| APC Factory | APCs / troop transports |
| IFV Factory | BMP / Bradley-type vehicles |
| Tank Factory | Main battle tanks |
| SHORAD Factory | Short-range air defense |
| Radar Factory | EWR/search radar assets |
| Logistics Depot | Trucks and support vehicles |

This creates natural focal points for combat.

A coalition that wants tanks must capture and hold the tank factory. A coalition that wants better mobile air defense must capture and hold the SHORAD factory.

Ground commanders then assemble convoys from the vehicles produced by different factories.

---

### 7. Production Tempo

Production should be slow enough to matter.

Suggested starting values:

| Asset type | Suggested production interval |
|---|---:|
| Infantry / trucks | 1-2 hours |
| APCs | 2 hours |
| IFVs | 3-4 hours |
| Tanks | 6-12 hours |
| SHORAD | 6-12 hours |
| Radar assets | 24-48 hours |
| Aircraft weapons | Weekly delivery, not continuous |

Aircraft weapons should not regenerate every 2 hours. That creates an infinite-weapons feeling.

Instead:

```text
Fuel = continuous logistical flow
Ground vehicles = industrial production
Aircraft weapons = scarce strategic stock, replenished weekly
```

---

### 8. Ground Commanders

Ground commanders are expected to matter.

They should:

- assemble convoys
- decide where produced units go
- protect logistics movements
- reinforce captured POIs
- prepare attacks on enemy POIs
- request air support
- coordinate with helicopter transport and reconnaissance assets

The campaign should encourage actual combined arms coordination.

---

### 9. Airfields as Consumers

Airfields are not automatically useful just because they are captured.

An airfield becomes operationally valuable only when it has:

- fuel
- aircraft
- ground security
- supply route
- air defense
- usable logistics link
- sufficient reason to expand in that direction

Recommended rule:

```text
Airfield owned + supplied = usable forward base
Airfield owned + unsupported = vulnerable liability
```

This should prevent teams from capturing airfields just to paint the map.

---

### 10. Home Bases

Home bases start well equipped and heavily defended.

They should have:

- aircraft inventory
- fuel stock
- weapon stock
- SAM/SHORAD protection
- CAP support
- EWR/GCI coverage
- parked aircraft vulnerability
- strong defensive ground units

They should be possible to attack, but militarily expensive and risky.

Home base ownership should probably not be flipped easily, if at all.

---

### 11. Reconnaissance

Reconnaissance is an important mission role.

The mission should use DML `Recon Mode`.

Recommended recon-capable assets:

- OH-58D
- UH-1H
- CH-47F
- scout ground vehicles
- possible special recon aircraft roles

Recon should help identify enemy ground units, factory outputs, convoy movement, and weakly defended POIs.

Recon should not replace tactical flying. It should give just enough information to make planning meaningful.

---

### 12. Player Messaging

Messages should be restrained.

During development and debugging, verbose messages are acceptable.

During live play, messages should be minimal:

- POI captured
- POI lost
- POI neutralized
- factory production completed
- fuel delivery completed
- major airfield supply state changed

Preferred live examples:

```text
BLUE captured Baniyas Refinery.
RED captured Hama Tank Factory.
Baniyas Refinery is neutral. Fuel production stopped.
BLUE fuel delivery completed at Incirlik.
```

Avoid constant spam.

Longer status information should be available through an F10 menu or status report, not constant automatic messages.

---

## DML Module Plan

This mission is designed around DML.

DML modules currently planned:

| Module | Purpose |
|---|---|
| `ownedZones` | Strategic POI ownership. |
| `factoryZones` | Ground vehicle production tied to zone ownership. |
| `Limited Airframes` | Coalition airpower pressure and aircraft/pilot scarcity. |
| `StopGap` | Visible empty aircraft slots. |
| `SittingDucks` | Destructible parked aircraft and slot denial. |
| `Valet` | Airbase/FARP entry and departure behavior. |
| `Recon Mode` | Reconnaissance gameplay for helos, scouts, and selected aircraft. |
| `airfield` / `baseCaptured` | Airfield ownership tracking. |
| `messenger` | Controlled player notifications. |
| `wiper` | Cleanup of destroyed units/debris for MP performance. |
| `persistence` | Later phase: save campaign state. |
| `WHpersistence` | Later phase: warehouse/resource persistence if used. |

---

## DML Zone Design

DML uses Mission Editor trigger zones with attributes.

Typical strategic POI zone:

```text
Zone name: POI_BANIYAS_REFINERY_COMPLEX

owner = neutral
numCap = 10
numKeep = 5
easyContest = false
ownedBy# = BaniyasRefineryOwner
redCap! = BaniyasRefineryRed
blueCap! = BaniyasRefineryBlue
neutral! = BaniyasRefineryNeutral
```

Typical specialized factory zone:

```text
Zone name: POI_HAMA_TANK_FACTORY

owner = neutral
numCap = 10
numKeep = 5
easyContest = false
ownedBy# = HamaTankFactoryOwner

factory = true
productionRED = <red tank group/type definition>
productionBLUE = <blue tank group/type definition>
```

Actual production attributes and templates will be defined in the mission implementation phase.

---

## Proposed v1 Scope

Start small and make the core loop work.

Recommended v1:

| Item | Count |
|---|---:|
| Blue home base | 1 |
| Red home base | 1 |
| Large strategic POI zones | 5-7 |
| Refineries | 1-2 |
| Vehicle factories | 3-4 |
| Forward airfields/FARPs | 1-2 |
| Recon roles | enabled |
| Limited airframes | enabled |
| StopGap/SittingDucks | enabled |
| Full persistence | later |
| Logistics hub repair system | skipped for v1 |
| Generic weapon warehouses | skipped for v1 |

---

## Proposed Strategic POIs

Initial candidate types:

1. Refinery + port complex
2. APC factory
3. IFV factory
4. Tank factory
5. SHORAD factory
6. Radar factory
7. Forward airfield or logistics town

The exact locations will be chosen on the Syria map based on terrain, existing map assets, road access, airfield placement, and playability.

---

## Persistence Plan

Persistence is important, but not required for the first working prototype.

Phase 1 should focus on:

- zone ownership
- capture behavior
- aircraft vulnerability
- factory production
- fuel supply
- player feedback

Later phases can persist:

- zone ownership
- aircraft losses
- blocked slots
- factory stock/output
- fuel levels
- convoy state
- warehouse/resource state

---

## Implementation Philosophy

Build the campaign in layers.

1. Make ownership work.
2. Make capture difficult and meaningful.
3. Make factories produce the correct ground unit classes.
4. Make fuel supply affect airfields.
5. Add limited aircraft and parked-aircraft vulnerability.
6. Add recon.
7. Add persistence only after the gameplay loop works.

Avoid building a giant invisible machine before the first player has fun.

---

## Current Status

Initial concept and design phase.

No final mission file structure is defined yet.

No production scripts are included in this README.

---

## Notes for Mission Designers

- Use existing Syria map assets when possible.
- Use large zones for operational complexes, not tiny capture circles.
- Do not make every POI produce everything.
- Do not over-message players.
- Keep home bases strong but not fully magical.
- Make aircraft preservation matter.
- Make logistics meaningful.
- Make ground commanders useful.
- Keep the first version playable before adding more machinery.

---

## License

TBD.

---

## Credits

Mission concept and design: Lock-On Greece

Built for DCS World using DML by cf/x.
