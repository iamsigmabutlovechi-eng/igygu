# THE ASHEN CROWN

This repository is the GitHub workspace for **THE ASHEN CROWN**.

## Current handoff

The full Unreal Engine 5.8 migration project and retained web-game source are delivered separately in the source archive attached to the project handoff:

`THE_ASHEN_CROWN_UNREAL_5_8_0.8.1_SAVE_HARDENING.zip`

The archive contains the complete project tree. Extract it before opening Unreal Editor. Its top-level directory is `THE_ASHEN_CROWN_UNREAL_5_8/`.

> The complete source tree has not yet been mirrored into this GitHub repository. The repository currently contains this project overview. Do not treat the presence of this README as evidence that the Unreal source has been pushed.

## Project target

- Unreal Engine 5.8 C++ migration vertical slice.
- Legacy browser game version 0.7.1 retained as the reference implementation.
- 16 world regions, nine restorable city districts, third-person movement, procedural NPC prototype, and campaign data.
- SaveGame schema v2 with legacy-save validation and safer save-slot handling.

## Validation performed on the delivered source archive

- Unreal source validator: **54 PASS / 0 FAIL**.
- Python migration/validation script syntax: PASS.
- Legacy web source `npm run check`: PASS.
- Legacy web source `npm test`: PASS.

These are source-level checks only. UnrealHeaderTool/MSVC compilation, Play-In-Editor validation, cooking and Windows packaging still require a Windows development machine with Unreal Engine 5.8 installed. No Unreal executable is included.
