# soarqin-MechaDronesTweaks

Handle both value and address reads for drone-speed display while preserving native research state and energy behavior.

The analysis and proposed fixes in this handoff were developed with assistance from the GPT 6.1 Sol model. English documentation accompanies the code to explain what changed, why it changed, and the available validation results.

[Review map](REVIEW_GUIDE.md) · [Related mods and code references](RELATED_MODS.md) · [Detailed changes](CHANGELOG.md) · [Build/review notes](BUILD.md) · [Assembly metadata](metadata.json)

Prepared for maintainer review on 15 October 2026. This is a local modified build, not an official upstream release, published package or pull request.

Installed plugin version(s): **1.1.5**. Existing package manifest version: **1.1.4**. Manifest, plugin and assembly versions are separate; the original manifest is retained.

## Package layout

- `InstalledPackage/`: actual installed mod files and companion preloader when present.
- `Source/Reconstructed/`: full projects reconstructed from the exact installed assemblies.
- `Source/EarlierWorkingSource/`, `PortedWorkingSource/`, `UpstreamSnapshot/`: source snapshots when available; provenance is recorded separately.
- `Evidence/`: development helpers, focused check sources and structured validation/installation records.
- `Diffs/`: source-port patches and normalized structural IL comparison.
- `Baselines/`: previous binary and its provenance for review, not an automatic rollback.

## Plugin identifiers and declared dependencies

- `org.soardev.mechadronestweaks` — MechaDronesTweaks 1.1.5; dependencies: com.dkoppstein.plugin.DSP.FastDrones | soft.

## Installed assembly hashes

| Recorded path | SHA-256 |
|---|---|
| `plugins/soarqin-MechaDronesTweaks/MechaDronesTweaks.dll` | `28aafb514adcb0083230fba46bea637d933d532460f18de78865bac027c84aed` |

## Scope and limitations

Not every source project has been rebuilt. Historical compile/test evidence is limited to its recorded hashes. Headless/embedded-Mono checks do not establish real Unity UI, the user's world, all-mod startup, multiplayer or sustained-memory acceptance.

## Independent review package

Send this entire directory, with all subdirectories, to this mod's maintainer. No sibling maintainer directory or parent-level report is required for code review. There are **0** related-mod reference copies under `RelatedMods/`. Read `RELATED_MODS.md` for direct dependencies, concrete compiled member calls, shared native integration points and source snippets. Required installed dependencies of a copy are flattened into this directory; no recursive RelatedMods trees are produced.

Uninstalled optional declarations are listed explicitly; no nonexistent mod is claimed to be included. The actual game/Unity/BepInEx SDK remains an external build prerequisite. Historical test/build scripts may need path adaptation; this is a complete review package, not a guaranteed one-command clean rebuild. See `STANDALONE_VERIFICATION.json` and `PACKAGE_SHA256SUMS.txt` for the local package check.
