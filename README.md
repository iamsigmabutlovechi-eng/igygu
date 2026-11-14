# THE ASHEN CROWN

This repository is the GitHub workspace for **THE ASHEN CROWN**.

## Current handoff — source version 0.8.2

The complete Unreal Engine 5.8 migration project and preserved 0.7.1 browser-game source are delivered in the source archive:

`THE_ASHEN_CROWN_UNREAL_5_8_0.8.2_AI_NAVMESH.zip`

Extract the archive before opening Unreal Editor. Its top-level directory is `THE_ASHEN_CROWN_UNREAL_5_8/`.

> Important: the complete source tree is delivered separately and has **not** been mirrored into this GitHub repository. This repository currently contains the project handoff README only; the archive is the source of truth for the 0.8.2 code.

## Unreal Engine 5.8 vertical slice

- 8 × 8 km procedural terrain prototype, 16 world regions and nine restorable city districts.
- Third-person movement and camera.
- Citizen AI using `ACharacter`, `AAIController`, pathfinding requests and a city-bounded Recast NavMesh.
- In-game 24-hour schedule for rest, work and social routines; one game day lasts 90 real seconds.
- Restoration tiers change citizen population, speed, visual status and evening social hours.
- SaveGame schema v2, legacy JSON importer and protection against overwriting undecodable or newer-version saves.
- Original campaign content retained from the 0.7.1 reference project.

## Validation performed on the 0.8.2 source archive

- Unreal source static validator: **68 PASS / 0 FAIL**.
- Python migration and validation script syntax: PASS.
- Legacy browser source `npm run check`: PASS.
- Legacy browser source `npm test`: PASS.
- ZIP integrity check: PASS.

These checks do **not** replace UnrealHeaderTool/MSVC compilation, Play-In-Editor testing, cooking or Windows packaging. Those require a Windows development machine with Unreal Engine 5.8 installed. No Unreal executable is included or claimed as built.

See `README_VI.md` and `Docs/AI_NPC_0.8.2_IMPLEMENTATION_VI.md` inside the archive for setup and runtime acceptance steps.
