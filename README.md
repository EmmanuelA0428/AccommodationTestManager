# Accommodation Test Manager

Windows 11 x64 accommodation testing app. **Synthetic/dummy tests only; not a secure production exam kiosk.**

## Download Beta 3 — one setup file

[Download AccommodationTestManager-Setup-Beta3.exe](https://github.com/EmmanuelA0428/AccommodationTestManager/releases/download/v1.0.0-beta.3.1/AccommodationTestManager-Setup-Beta3.exe)

[Release notes and all assets](https://github.com/EmmanuelA0428/AccommodationTestManager/releases/tag/v1.0.0-beta.3.1) · [Installer SHA-256](https://github.com/EmmanuelA0428/AccommodationTestManager/releases/download/v1.0.0-beta.3.1/AccommodationTestManager-Setup-Beta3.exe.sha256)

Public download: no GitHub sign-in required. The setup installs the app, private .NET runtime and protected helper together. No separate PowerShell installation or folder assembly. Install from the standard testing account, using separate administrator credentials when prompted; run the installed app normally afterward. **The first Beta 3 install needs this EXE; old Beta 2 update checks do not switch channels.**

Unsigned beta: Windows may show Unknown Publisher/SmartScreen warnings. Do not disable Windows protections.

## Important: older Beta 2 helper

Older restriction writers could erase unrelated registry values. Do not run old restriction/restore actions. Preserve old snapshots. Their recorded values are incomplete; the Beta 3 installer cannot reconstruct unrecorded erased values. Affected devices require independent baseline review/repair by a qualified Windows administrator; new controls stay gated until review is confirmed.

## Beta 3 status

[Changes and limitations](BETA3.md) · [Successful Windows validation](https://github.com/EmmanuelA0428/AccommodationTestManager/actions/runs/37958905869)

Passed: isolated native registry tests in both PowerShell versions, installer build/install/PIN/uninstall checks, synthetic WPF UI, app/mock regressions, and live public configuration/cache validation. Installer was anonymously downloaded and hash-verified after publication.

Still required: dummy-exam testing of real Word saves/recovery/export, actual Edge policy exports and AI UI, Canvas/Posit sign-in/project dependencies, USB/network/UAC and interruption recovery on the testing laptop. Full-screen/app PIN is not OS lockdown; in-site AI and protected exam storage are not implemented.

## Configuration and source

- [Beta 3 global configuration](global-config-beta3) — versioned manifest and separate allowlists; validated offline cache.
- [Verified build source ZIP](AccommodationTestManager-Beta3.zip) · [Source checksum](AccommodationTestManager-Beta3.zip.sha256).
- [Validation workflow](.github/workflows/build-beta3.yml) builds/test artifacts only; public releases are a separate action.

The source archive preserves the build-time documentation snapshot; the release notes/validation link above give the current post-build status. No student data, runtime sessions, PINs, credentials or protected recovery snapshots belong in this repository. Old Beta 2 files/releases remain historical only.
