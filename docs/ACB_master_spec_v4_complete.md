# ACB MASTER SPEC v4.0 — COMPLETE MERGED PROJECT SPECIFICATION
# Gold Coast LGA — UE5 Open World + Game Pipeline
# Date: April 2026 | Author: ACB
# Paste as message 1 in every new ACB or ACA session.
# Read entirely before responding. Confirm version targets before any output.
# No gap-filling. Unspecified details must be raised with user before proceeding.

---

## SECTION 1 — AGENT ROSTER

```
ACB = Claude — Master Planner / Spec Keeper
      All confirmed decisions logged here. This document is law.
      No pipeline decision confirmed until ACB logs it here.

ACA = Claude separate thread — Lead Programmer
      Executes scripts and code. Must state version targets before
      any output. Must not alter fixed parameters without ACB approval.

GCB = Gemini AI Studio Pro — Research only
      Web research, doc retrieval, version checking.
      Not a spec authority. Not a decision maker.

OGA = ChatGPT-4o — Fallback on token exhaustion only
PPA = Perplexity Pro — Fast version and API lookup only
GCC = Gemini Standard — Basic search only
```

---

## SECTION 2 — ENGINE AND SOFTWARE STACK

```
TARGET ENGINE    : Unreal Engine 5.7
                   CONFIRM 5.7 before producing any output.
                   5.4 and 5.5 are prior test stages only.
                   5.7 is confirmed target for all production work.

CITY SAMPLE      : Compatibility with 5.7 requires verification.
                   City Sample was originally built for UE5.0/5.1.
                   Migration pipeline: open in 5.7, convert, package test.
                   Flag any 5.7 incompatibilities before proceeding.

QGIS             : 4.0
                   SAGA removed — do not reference any SAGA tool.
                   GdalWarp is confirmed smoothing method.

PYTHON           : CPython 3.11 standard (python.org install)
                   NOT OSGeo4W bundled Python.
                   Execution: standard CMD or PowerShell only.
                   Command: python script.py

GDAL / NUMPY     : pip install gdal numpy (PyPI wheels for Python 3.11)

HOUDINI          : Apprentice (free) — primary tutorial track
                   Indie (paid) — parallel documented track
                   Confirm current stable version before referencing
                   any node names, HDAs, or export formats.

BLENDER          : Latest stable
GIMP             : Latest stable
```

---

## SECTION 3 — PROJECT IDENTITY

```
Name        : Gold Coast LGA — UE5 Real-World Open World + Game Pipeline
Scale       : 36km x 36km at 1:1 real-world scale
Area        : Gold Coast LGA, Queensland, Australia
Purpose     : Free community pipeline tutorial + working game project
Audience    : Community users — explicit idiot-proof documentation standard

FREE PIPELINE PRIORITY:
  All software free where possible.
  Paid parallel tracks documented with clear fork points.
  Assets: all owned via Fab/Epic Launcher (purchase or free monthly).
  Exception: TPS Kit v2.2 — purchased outright, not freely available.
  Users may substitute their own shooter framework.
```

---

## SECTION 4 — GAME MODES (ALL MODES REQUIRE LANDSCAPE FIRST)

Landscape pipeline is prerequisite for all modes.
No game mode development begins until landscape import is validated.

```
MODE 1 — Basic explorable environment
  Full 36km landscape, explorable at real-world scale.
  Vehicles: cars, plane, boats, helicopter, drone.
  Character: third person controller (GASP + Metahuman).
  No gameplay objectives or logic.
  Target: functional open world traversal demo.

MODE 2 — Basic gameplay layer
  All of Mode 1 plus:
  Basic interaction and objective logic via Mountea Framework.
  Territory control system (region capture, alert levels).
  Economy layer via Pawn Shop System + Mountea Inventory.

MODE 3 — GTA-style third person shooter
  All of Mode 2 plus:
  Full weapon and combat system via TPS Kit v2.2 (stripped).
  Dynamic narrative progression via Mountea Dialogue.
  Animal mounts via Horse Starter Kit.
  Full GTA-style commandeer / vehicle theft system.
  This is the primary game target.

MODE 4 — Archvis interactive visualisation
  Standalone level within same project.
  Based on UE5 Archvis Explorer template.
  3D viewer with camera controls, area layers, detail data, images.
  Also targeted as menu state within Mode 1 / Mode 3.
  Implementation: runtime menu system with 3D camera and layer toggle.
  If City Sample incompatibility: branch as separate build,
  replace City vehicles with alternative systems.
  Future intent: merge Mode 4 viewer into Mode 1 as menu feature
  or as integrated visualisation component within game systems.

MODE 5 — Networked multiplayer third person shooter
  Extends Mode 3 with multiplayer via EOS.
  Built on rebuilt source engine (UE5.7 from GitHub source).
  Expands Lyra game modes and gameplay abilities.
  3D environment and assets migrated from Mode 3.
  City Sample full environment not replicated — 3D and environment only.
  DEPENDENCIES:
    Epic GitHub source access confirmed
    Visual Studio 2022 required
    Full engine compile required (2-4 hours first time)
    EOS developer account required
  STATUS: Significant independent branch.
          Not touched until core modes validated.
          Previous working build exists at UE5.2-5.5.
          5.7 source build required from scratch.
          Last stage of development.

MODE 6 — UEFN compatible twin environment
  6.0: UEFN twin of the full UE5 stack.
       Optimised and conformed to UEFN limitations.
       Runs in parallel with UE5 development as validation track.
       Assets tested for UEFN compatibility at intervals during
       UE5 development — not left until end.
  6.1, 6.2 etc: Individual game modes published via Fortnite.
       Reduced area versions of Gold Coast environment.
       Published via UEFN island system.

  UEFN ASSET STRATEGY — TWO PERMANENT VERSIONS:
    Assets that conform cleanly: single version shared both platforms.
    Assets incompatible with UEFN: two independent versions maintained.
    UE5 source: full fidelity originals kept intact.
    UEFN version: best available conforming replacement found.

    Known splits (examples, not exhaustive):
      Triplanar mapping       -> UE5 keeps, UEFN gets replacement
      Custom material expr    -> UE5 keeps, UEFN gets replacement
      3D widgets              -> UE5 keeps, UEFN gets replacement
      Standard PBR meshes     -> single version, shared
      Basic landscape mats    -> validate per material, decide per case

  UEFN validation runs at intervals throughout UE5 development.
  Flag incompatible assets early, not at project end.
  Branch for UEFN fork created when UE5 stack is sufficiently stable.
```

---

## SECTION 5 — CONFIRMED ASSET STACK

All assets owned. Obtained via Fab / Epic Launcher.

```
ASSET                           SOURCE          STATUS
─────────────────────────────────────────────────────────────────
Game Animation Sample (GASP)    Epic Launcher   Verified, packaged
City Sample + Small_City_LVL    Epic Launcher   Verified, packaged
                                                Migrated to GASP project
MW Landscape Auto Material      Fab             Verified, packaged
                                                Migrated to GASP + City
Aziel Arts Landscape (ORD/ORM)  External DL     Verified in packaged build
                                                Non-PCG working correctly
Aziel Arts Landscape (PCG)      External DL     Migrated to City Sample
                                                BUG: PCG fails packaged build
                                                PIE only — debugging deferred
TPS Kit v2.2                    Fab (purchased) Not yet integrated
  (by Marcin Matuszczyk)                        Updated April 12 2026
                                                Uses Motion Matching (GASP compat)
                                                Create new project, test build first
Metahumans                      Epic Launcher   Planned integration
Mountea Framework               Engine plugin   Installed, untested
                                                Max listed compat: 5.6
                                                5.7 use expected with potential fixes
                                                Can install 5.5 version to test
                                                and follow 5.5->5.7 upgrade pipeline
                                                via Epic Launcher (max install 5.5)
Horse Starter Kit               Fab             Owned, not yet integrated
Pawn Shop System                Fab             Owned, not yet integrated
```

---

## SECTION 6 — CHARACTER AND ANIMATION FOUNDATION

```
FRAMEWORK        : GASP (Motion Matching) + Mover Component + Metahuman
BASE CLASS       : BP_GASP_Character
MESH SWAP        : Skeletal mesh -> Metahuman (m_med_nrw_body or equiv)
                   Modular parts: Face, Torso, Legs, Feet as child components
CONSTRUCTION     : Leader Pose Component for clothing motion sync
ANIMATION BRIDGE : Retarget ABP_GASP_Character to Metahuman skeleton
CAPSULE          : Adjust to Metahuman height (~180cm)
MOVER TWEAK      : Adjust Floor Check Distance to prevent Motion Matching jitter
PRODUCTION METHOD: Visual Data Retargeting — no logic rewrites

PERFORMANCE CRITICAL:
  System must maintain >60 FPS.
  Below 60 FPS breaks GASP Motion Matching — character feels heavy/laggy.
  This is the hard performance floor for all build tests.
  Every package build test must record and document frame rate.
```

---

## SECTION 7 — WORLD LOGIC, NARRATIVE, AND PROGRESSION

```
FRAMEWORK        : Mountea Framework (engine plugin)
PRODUCTION METHOD: Event-Driven Game States — zero per-frame ticking

OBJECTIVE SYSTEM:
  NPC interactions -> MounteaDialogueGraph
  World State Manager -> DT_WorldState data table
  Columns: RegionName (Name), IsCaptured (Bool), AlertLevel (Int)

TERRITORY CONTROL:
  Player eliminates NPCs in volume
  -> Triggers Mountea "Objective Completed" event
  -> Updates DT_WorldState
  -> Fires Global Blueprint Interface call
  -> Dynamically increases AlertLevel in neighbouring regions

SAVE / PERSISTENCE:
  Mountea Inventory / Interaction serialization system
  Persistent actors assigned MounteaSaveInterface
  On Begin Play: actors ping SaveGame for state, toggle mesh/collision

MOUNTEA 5.7 RISK:
  Max listed compatibility: 5.6
  5.7 use expected with potential Blueprint fixes required
  Test pipeline: install 5.5 engine -> validate in 5.5
  -> upgrade to 5.7 -> document required fixes
  -> document as tutorial known issue with fix steps
```

---

## SECTION 8 — TRANSPORTATION AND VEHICLE SYSTEM

```
FRAMEWORK: City Sample Mass AI + Chaos Vehicles + Horse Starter Kit

GTA COMMANDEER SEQUENCE (confirmed method):
  1. Player uses Mountea Interaction to detect "Vehicle" tag on Mass Entity
  2. Interaction calls OpenDoor via VehicleAnimationComponent
     (uses City Sample Animation Data Assets)
  3. Player executes "Pull Driver Out" montage
  4. Mass Entity NPC swapped instantly for standard Skeletal Mesh Actor
     executing reciprocal "Getting Pulled Out" montage
  5. Post-animation: Possess node transfers Player Controller
     from GASP Character to fully instantiated ChaosVehicle

ANIMAL MOUNTS (Horse Starter Kit):
  Mountea Interaction triggers "Mount" montage
  Custom "Riding State" added to GASP
  Disable Player Mover Component
  Attach Player to Socket on Horse Actor back
  Input parameters redirect from Player to Horse Actor

BOATS     : 0-wheeled Chaos setup, buoyancy physics
AIRCRAFT  : Standard Chaos flight model
AIR/WATER NPC: Mass Entities with Visual Proxy to High-Quality Actor swap
               on player possession (identical to car commandeer)
```

---

## SECTION 9 — COMBAT AND ECONOMY

```
COMBAT (TPS Kit v2.2 — stripped):
  DELETE all native locomotion from TPS Kit
  Bridge to GASP character for:
    Weapon inventory
    Aiming offsets
    Projectile / hit-scan firing logic
    Health and damage events
  Motion Matching version of TPS Kit required for GASP compatibility

ECONOMY (Pawn Shop System + Mountea Inventory):
  Player loots captured regions
  Trades dynamically via Pawn Shop System
  Tied into Mountea Inventory serialization
  GTA-style black market simulation
```

---

## SECTION 10 — ENVIRONMENT AND OPTIMISATION

```
FRAMEWORK: City Sample Base + Aziel Arts PCG + GIS landscape data

PERFORMANCE FLOOR: >60 FPS (GASP requirement — hard limit)

PCG SETTINGS:
  Aziel Arts PCG graph must use "In-Grid" spawning mode
  Required for 36km open world scale management

CULLING:
  Strict Per-Instance Custom Data enforcement
  Fade foliage and distant PCG elements dynamically
  Reserve CPU/GPU headroom for Mass AI and Mover Component calculations

STREAMING:
  World Partition required — mandatory at 36km scale
  Landscape streaming handled automatically by World Partition
  HLOD generation: build and test at small scale before full 36km

KNOWN RISKS:
  Nanite + HLOD conflict (community confirmed UE5.3-5.5, check 5.7)
  Do not enable Nanite and HLOD simultaneously without testing
  PCG on Nanite-displaced landscape: PCG ignores displacement
  Mitigation: use Nanite without tessellation for PCG compatibility
  or use RVT for accurate PCG height sampling
```

---

## SECTION 11 — HEIGHTMAP PIPELINE (FIXED — DO NOT ALTER)

```
SOURCE          : Single full-resolution GeoTIFF, UInt16
COVERAGE        : 36km x 36km Gold Coast LGA
NODATA          : 0 — excluded from normalisation calculations

PROCESSING (single script, single pass):
  Step 1: Smooth — Gaussian blur sigma 1.0
  Step 2: Normalise — global min/max, full UInt16 range (0-65535)
          GLOBAL across full raster, NOT per-tile (per-tile = seams)
  Step 3: Tile — 4033 x 4033 px, unique pixels, NO overlap
          UE5 handles internal edge duplication automatically
          PREVIOUS ERROR: shared edges used — this is wrong, never repeat
  Step 4: Export R16 — raw LE uint16, no header, no compression

OUTPUT FORMAT (FIXED):
  Encoding    : Little-endian uint16
  Header      : None
  Bytes/tile  : 4033 x 4033 x 2 = 32,530,178 exactly
  Naming      : GC_Landscape_x{col}_y{row}.r16 (0-indexed, lowercase)
  Test A      : GC_Test_Single.r16
  Test B      : GC_Landscape_x0_y0.r16

UE5 IMPORT SETTINGS (FIXED):
  Section size        : 63 quads
  Sections/component  : 1 x 1
  Components          : 64 x 64
  Resolution          : 4033 x 4033
  Z Scale estimate    : 58.6 (verify and adjust post-import)

KNOWN BUG UE5.5 (check if resolved in 5.7):
  Weightmap resolution mismatch on tiled import (UE-241268)
  Workaround: import heightmap first, add material after
```

---

## SECTION 12 — GIS DATASETS

```
DS1 : OpenStreetMap via Overpass-Turbo
      .xml / .osm | Large buildings, roads, polygons
      AUTHORITATIVE where DS1 and DS2 overlap

DS2 : VIDA / Google-Microsoft Open Buildings
      .fgb -> .osm xml | Residential buildings, POLYLINES
      MUST convert to polygons before any clip operation
      QGIS: Vector > Geometry Tools > Lines to Polygons

DS3 : Overture Maps via overture-py
      GeoJSON | Building heights for Houdini extrusion

BOUNDARY: Gold Coast Open Data (ArcGIS)
      .shp / .geojson | Clip DS2 from AUS-wide to GC LGA

CLIP SEQUENCE (FIXED — DO NOT ALTER):
  1. Convert DS2 polylines to polygons
  2. QGIS Vector > Geoprocessing > Difference
     Input: DS2 polygons | Overlay: DS1 polygons
  3. Output: DS2 with DS1 footprints punched out
  Keep DS1 / DS2 / DS3 SEPARATE — no merge
  Separate labs::osm_import node per dataset in Houdini

JOSM EXPORT (CRITICAL):
  File > Export to GPX/OSM only — generates <bounds /> tag
  Without <bounds />: Houdini geometry offset ~6000 units or microscopic

HOUDINI ALIGNMENT (CRITICAL):
  All osm_import nodes: identical centre lat/long, Scale 1.0, UTM/Mercator
  Access centre params INSIDE node, NOT top-level subnet transform
```

---

## SECTION 13 — HOUDINI CITY GENERATION

```
TRACK A (FREE)  : CSV export -> UE5 Blueprint city generation
TRACK B (PAID)  : Houdini Indie full procedural pipeline
TEST ZONES      : Surfers Paradise (primary), Varsity Lakes (secondary)

OUTPUTS:
  a) Low-poly extruded 3D blockout — buildings and streets
     Procedural atlas materials, UV, export to UE5
  b) Base for procedural city generation (City Sample / Houdini Engine)

HOUDINI APPRENTICE FORK POINT:
  Document clearly when Apprentice hits export format limits
  Provide Indie licence cost and link as upgrade path
  Both tracks documented in tutorial as parallel cases
```

---

## SECTION 14 — BUILD AND TEST METHODOLOGY

```
VALIDATION SEQUENCE FOR EVERY ASSET:
  1. New project in highest compatible UE version -> package build -> test
  2. If older version: open copy in 5.7 -> upgrade -> package build -> test
  3. Migrate to GASP testing project -> package build -> test
  4. Migrate to City Sample as separate level -> package build -> test
  5. Integrate with City Sample level -> full package build -> test

GASP PROJECT = primary testing environment (lighter than City Sample)
CITY SAMPLE  = core production base (heaviest, integrate last)

REBUILD EXPECTATION:
  Process expected to run minimum twice during development
  Account for core asset updates (City Sample, GASP, etc.)
  If core asset updates: attempt migration first, rebuild from new
  base only if migration fails or produces instability

INTEGRATION ORDER (confirmed):
  1. Landscape pipeline (prerequisite for all modes)
  2. GASP + Metahuman (core player controller)
  3. City Sample base (heaviest integration)
  4. Aziel Arts landscape material (after landscape validated)
  5. TPS Kit v2.2 (after core game controller stable)
  6. Mountea Framework (after core systems validated)
  7. Additional assets: Horse Kit, Pawn Shop, others
  8. Mode 5 (Lyra / EOS — last, independent branch)
  9. Mode 6 (UEFN — parallel validation, branch at stable point)
```

---

## SECTION 15 — PRODUCTION BUILD METHODOLOGY (INJECTED SCOPE PHASE 1)

```
CONFIRMED STARTING SEQUENCE:
  1. Blank GASP Animation Sample project in UE5.7
  2. Migrate BP_GASP_Character confirmed working
  3. Execute Metahuman rig retargeting and mesh swap
  4. Test locomotion on city streets — feet track pavement via
     Motion Matching without Mover Component jitter
  5. Package build — confirm >60 FPS baseline
  ONLY AFTER PHASE 1 FLAWLESSLY EXECUTING:
  6. Integrate Mountea interaction logic
  7. Integrate TPS Kit weapon states (stripped)

NOTE: This sequence runs in GASP project not City Sample initially.
City Sample integrated after GASP baseline is confirmed stable.
```

---

## SECTION 16 — DOCS AND PROJECT MANAGEMENT

```
DOCS PIPELINE:
  Entry point : GitBook visual editor (one paste per update)
  Auto-sync   : GitHub (via GitBook bidirectional sync)
  Auto-publish: GitBook public site
  Auto-update : Confluence (GitHub Markdown Sync app)
  Auto-embed  : Notion (native GitHub sync, beta)

GITHUB REPO: gc-ue5-landscape-pipeline (public)
  scripts/          Python pipeline scripts
  qgis-models/      QGIS processing models
  docs/             Tutorial markdown, manifest.md
  README.md
  CHANGELOG.md

JIRA: Kanban board, free tier
  Four columns: To Do | In Progress | Blocked | Done
  No sprints, no ceremony, no velocity tracking
  All tickets pre-populated by ACB
  User: read, verify, move card, fill close fields

GIT STRUCTURE:
  Single repo, all modes in main
  Feature branches for: Lyra/Mode 5 integration, UEFN/Mode 6 fork
  Asset library: Epic Launcher / Fab as source of record
```

---

## SECTION 17 — CURRENT STATE

```
[LANDSCAPE TRACK — PREREQUISITE FOR ALL MODES]
  Smoothing          : COMPLETE (GdalWarp, Gaussian sigma 1.0)
  Tiling             : COMPLETE (rebatched, single pass QGIS)
  R16 conversion     : COMPLETE
  UE5 single tile    : TESTING — result pending
                       Note: previous tiles used shared edges (wrong)
                       Confirm tile format before concluding test
  Full 81-tile import: PENDING single tile validation
  Material Test 1    : PENDING (MW Auto)
  Material Test 2    : PENDING (Aziel ORD)
  Material Test 3    : DEFERRED (Aziel PCG — packaged build bug)

[GASP / CHARACTER TRACK]
  GASP baseline      : Verified packaged in prior testing
  Metahuman retarget : PENDING
  Mover jitter fix   : PENDING
  City Sample migrate: PENDING GASP baseline stable

[GIS / HOUDINI TRACK]
  DS1+DS2 bounds     : CONFIRMED ALIGNED
  DS2 poly convert   : PENDING
  Clip operation     : PENDING
  DS3 integration    : PENDING

[ASSET VALIDATION TRACK]
  GASP               : Verified
  City Sample        : Verified, migrated to GASP project
  MW Landscape       : Verified, migrated
  Aziel ORD          : Verified in packaged build
  Aziel PCG          : Migrated, PCG bug deferred
  TPS Kit v2.2       : New project create and test required first
  Mountea Framework  : Installed, untested, 5.7 compat uncertain
  Horse Starter Kit  : Owned, not yet started
  Pawn Shop System   : Owned, not yet started
  Metahumans         : Owned, integration planned post-GASP baseline

[DOCS TRACK]
  GitHub repo        : NOT STARTED
  GitBook            : NOT STARTED
  Notion             : NOT STARTED
  Confluence         : NOT STARTED
  Jira project       : NOT STARTED
  Phase 0 doc        : DRAFTED (ready for review)

[UEFN TRACK]
  Validation         : NOT STARTED (runs parallel, begins when assets stable)
```

---

## SECTION 18 — KNOWN ISSUES LOG

```
1.  Shared edge tile format (ACA error)
    Fix: reprocess from source with unique-pixel tiling

2.  OSGeo4W Python — no tkinter
    Fix: standard Python 3.11 from CMD confirmed

3.  GUI launcher
    Status: DEFERRED — pipeline must be stable first

4.  Aziel PCG — packaged build fail (PIE only)
    Suspect: GetLandscape PCG node
    Fix: replace with explicit landscape actor reference
    Defer until after landscape material Tests 1 and 2

5.  QGIS 4.0 removed SAGA
    Fix: GdalWarp confirmed working

6.  DS2 polyline clip leaves parts not whole shapes
    Fix: convert to polygons first, then Difference

7.  UE5.5 weightmap tiled import bug (UE-241268)
    Check if resolved in 5.7 before assuming workaround needed

8.  Nanite + HLOD conflict (UE5.3-5.5 confirmed)
    Check status in 5.7. Test in sequence, not simultaneously.

9.  Mountea Framework 5.7 compatibility
    Max listed: 5.6. Expect Blueprint fixes required.
    Test via 5.5 install path then upgrade.

10. TPS Kit v2.2 April 12 update
    Assume bug fixes. Create new project, test build before merge.

11. AI-directed pipeline failure
    Root cause: GCB planned without user verification
    Fix: ACB verifies all methods before ACA executes
    Documented as tutorial warning in Phase 0
```

---

## SECTION 19 — METHODOLOGY RULES (NON-NEGOTIABLE)

```
1. AI recommends — user verifies externally — then executes
2. No workaround chains introducing new dependencies
3. Crystallise state to manifest before any agent switch
4. Pipeline stages stable before automation built on top
5. ACA states version target before any output
6. ACB holds spec truth — all others are research inputs
7. Fixed parameters are fixed — propose changes to ACB only
8. Unspecified details raised with user before any gap-filling
9. Current user input is always truth — never assume continuity
   from prior sessions without manifest confirmation
```

---

END OF ACB MASTER SPEC v4
Version: 4 | Date: April 2026 | Author: ACB
Trigger for update: any phase completion, confirmed spec change,
new asset validation result, or mode development decision
Storage: GitHub /docs/manifest.md (primary) + Claude widget (session)
