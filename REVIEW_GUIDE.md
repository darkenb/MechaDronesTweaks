# Review map for soarqin-MechaDronesTweaks

This directory is the complete review unit for this mod: its English explanation, current code, prior working sources, diffs, tests, structured results, installed binaries and related-mod reference copies. No parent-level report or sibling maintainer folder is needed to understand the local changes.

Game context: **0.10.35.29145**, Assembly-CSharp SHA-256 `b84b60df5a24947a014801f23b9b85d1e77853f42a331918e2dc85b153e50527`. Game/Unity/BepInEx SDK files are external build prerequisites and are not distributed.

1. Read CHANGELOG.md for the concrete behavior and test limits.
2. Read RELATED_MODS.md for the copies and actual code references relevant to this mod.
3. Inspect the focused port diff first when present; the broad reconstructed diff may also contain upstream/compiler differences.
4. Use Source/Reconstructed as the exact installed-code view. Source/PortedWorkingSource is a maintained port snapshot, while subsequent overlays are under Evidence.
5. Check metadata.json and PACKAGE_SHA256SUMS.txt to identify the supplied files. Historical source/check paths may need adaptation; no universal clean rebuild is claimed.

## Local evidence and development code

- `Evidence/CurrentGameAudit/`
- `Evidence/InitialPhase/`

`Tools/HistoricalHarness/` holds the shared harness sources used by the recorded work. Test/patch source for this mod is in its Evidence/Source folders. A related-mod copy is review material; it is not an instruction to load every copied DLL together or install optional/inactive compatibility plugins. Real Unity UI, full save loading, sustained memory and all-mod acceptance remain separate.
