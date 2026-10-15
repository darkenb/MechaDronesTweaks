# soarqin-MechaDronesTweaks — detailed change report

Installed plugin version(s): **1.1.5**. Handle both value and address reads for drone-speed display while preserving native research state and energy behavior.

This report covers the final local build and its development history. Historical tests apply to their recorded source/game hashes; later ports supersede earlier version contracts. `metadata.json` and `InstalledPackage/` identify the actual handoff binary.

## Consistent drone-speed display — 1.1.5

Use the installed 1.1.4 source baseline and retain assembly identity 1.1.4.0. Remove duplicate `EnergyMultiplier` binding without changing its key, default or range.

The mecha/technology windows read speed with `ldflda`, while the old transpiler matched only `ldfld`; displayed speed could differ from actual modded flight. Pass both forms through the same calculation, using a temporary float where `ToString` needs an address. Do not write to native history. Test multiplier and fixed-speed modes separately.

Actual transpilers were applied to current ConstructionSystem, mecha/base drone ejection and both DroneComponent.InternalUpdate overloads in three option combinations. Speed/energy read sites and added instructions were checked. The native construction research field remains `constructionDroneSpeed`; the separate courier research field is not substituted. Retain base-drone support and native repair-energy arguments; add no second control loop without a concrete API need.

Unity ECalls prevented a full desktop-CLR Harmony runtime check, so that was left to the game. Near/far blueprints, empty energy, repair, UXAssist auto-construction and GS planet-size flight behavior remain untested live.

## Recorded source commits

- `12467b93450ac854436a1290089cdb56fcf587b6`

## Evidence locations

Structured build/API/contract/installation results and test/patch sources are under `Evidence/`. Source-port diffs and structural baseline comparisons are under `Diffs/`. `Baselines/` identifies previous DLLs and comparison scope. A structural IL difference can include compiler or upstream changes and does not prove every changed instruction is a local semantic fix.
