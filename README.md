# THE ASHEN CROWN

**Development target:** Unreal Engine 5.8 · source version 0.8.1  
**Legacy playable baseline:** Web/Three.js 0.7.1

A fantasy RPG project about restoring a fallen capital and rebuilding a kingdom.

## Source bundle

The complete source project, including the Unreal C++ migration, the preserved browser-game implementation, game data, tests, scripts and Vietnamese documentation, is stored at:

`releases/THE_ASHEN_CROWN_UNREAL_5_8_0.8.1_SAVE_HARDENING.zip`

Extract the archive before opening the project. Its top-level directory is `THE_ASHEN_CROWN_UNREAL_5_8/`.

## Unreal Engine project

- 8 × 8 km procedural terrain blockout and 16 imported region records.
- Third-person movement and camera.
- Nine restorable city districts with adjacency unlocks, staged costs and daily yields.
- Procedural placeholder buildings and scheduled citizen prototypes.
- SaveGame schema v2, validated legacy JSON importer, bounded resources/player coordinates, and protection against overwriting undecodable or newer-version saves.
- Campaign data retained for factions, characters, recruitable heroes, hidden questlines and endings.

## Run source validation

After extracting the bundle:

```bash
cd THE_ASHEN_CROWN_UNREAL_5_8
python Scripts/validate_project.py
python -m py_compile Scripts/Create_StartupMap.py Scripts/validate_project.py
cd LegacyWebSource
npm run check
npm test
```

A GitHub Actions workflow runs the same source-level checks against the bundle. These checks do not replace UnrealHeaderTool/MSVC compilation, Play-In-Editor testing, cooking or Windows packaging. No Unreal `.exe` is included or claimed as built.

## Build

Install Unreal Engine 5.8.x and the matching C++ toolchain, open `AshenCrown.uproject`, then follow `README_VI.md` in the source bundle to generate the World Partition map and package a Windows Development build.
