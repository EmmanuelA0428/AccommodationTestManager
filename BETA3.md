# Beta 3 — published testing prerelease

Download **AccommodationTestManager-Setup-Beta3.exe** below. It installs the app, bundled .NET runtime and protected helper together; no separate PowerShell installation. Install from the standard testing account and authorize setup with administrator credentials. Run the app normally afterward. **First Beta 3 installation uses this standalone EXE; Beta 2 update checks do not migrate release channels.**

## Changes
- Non-destructive typed registry writer; full selected-policy verification and preservation checks for unrelated values/subkeys.
- Legacy evidence archive/assessment gate; old helper must not be invoked.
- Separate narrow Canvas and Posit allowlists, with exact hosts and reviewed authentication subdomains.
- Fresh effective Edge policy export and staff live browser checks before online handoff.
- Full-screen Edge and Windows-supported, version-aware Edge AI policy plan; not in-site AI blocking.
- Beta 3 global config at global-config-beta3/, with validated last-known-good offline cache.
- Compact student controls, app-PIN staff handoff, Word saving/recovery and Check for updates retained.

## Validation passed
[Windows validation run](https://github.com/EmmanuelA0428/AccommodationTestManager/actions/runs/37958905869): developer/mocked checks, real isolated HKCU registry provider checks in PowerShell 7 and Windows PowerShell 5.1, self-contained installer build, native installation/PIN protocol/uninstall, and synthetic WPF UI tests. Live public global-config/list hashes and restart cache probe also passed.

**Still required:** real laptop Word saving/recovery/export, Edge policy/export recognition, Canvas/Posit sign-in/project dependencies, USB/network/UAC behavior and interruption recovery using dummy exams. This is not OS application lockdown or protected exam storage; full-screen/app PIN is not a Windows security boundary. No production-exam approval is implied.

## Important legacy-device warning
Older Beta 2 registry writes could erase unrelated values. Their snapshots are incomplete and cannot reconstruct unrecorded missing data. Do not repeat old restriction/restore actions. Preserve snapshots and independently review/repair affected branches from a known-good baseline with a qualified Windows administrator. This setup archives evidence and installs the corrected helper; it does not repair unrecorded erased values. New controls remain gated until independent review is confirmed.

Unsigned installer: Windows may show Unknown Publisher/SmartScreen warnings. Do not disable Windows protections. Do not upload student data, runtime sessions, PINs or credentials to GitHub.

Installer SHA-256: `5e624dfa229da179c0a799bafa1572e8383748735aea9ea67cc53b74a87a4551`
