# Source review and build notes

1. Match the installed assembly GUID/version/MVID/SHA-256 in `metadata.json` before reviewing changes.
2. `Source/Reconstructed/` contains complete ILSpy projects generated from the exact installed DLLs. These are reconstructed sources, not the author's original repository or a guarantee of a clean rebuild.
3. When present, `Source/PortedWorkingSource/` contains the later upstream port; `Source/EarlierWorkingSource/` contains earlier authoring sources. Later narrow binary-overlay sources are in `Evidence/`. Read `Source/PROVENANCE.json` and the English change report before choosing a baseline.
4. Supply your own current game Managed, BepInEx core and required mod dependencies. Adapt local HintPath values. Retain the original target framework, embedded resource names and preloader/publicized-reference build requirements. Earlier local builds used .NET Framework 4.7.2 reference assemblies, Roslyn and `/unsafe+` native-access metadata; they did not install a publicized native game DLL.
5. Historical build/patch/install scripts are retained as implementation evidence. They depend on original machine paths and starting hashes; some can install into a live profile. Inspect/adapt them before running. This documentation operation did not execute them or rebuild/install a mod.
6. Run focused checks in a separate output directory, then perform backed-up installation with the game closed and live acceptance separately. Review the Unity/LDB boundaries in test preparation: native forge/storage checks are not rendered-UI or whole-game acceptance.

The supplied source trees have not all been rebuilt for this handoff. Bit-identical reproduction and universal buildability of decompiled projects are not claimed. Merge the relevant fixes into the maintainer's original source tree and use the recorded hashes/tests to assess the resulting build. Original code identifiers, assets, licensing and functional localization data are preserved.
