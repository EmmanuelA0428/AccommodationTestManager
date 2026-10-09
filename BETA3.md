# Accommodation Test Manager — Beta 3

**Local development build: not published, signed, or cleared for real examinations.** Windows 11 x64, .NET 10 WPF. GitHub publication is deliberately deferred.

## What changed
- Non-destructive, typed registry writes, full end-of-operation policy verification, and preservation checks for unrelated registry properties and subkeys.
- Older helper detection and a legacy-review gate. Setup can install the corrected helper in maintenance mode for known older snapshots, archiving evidence without applying or restoring restrictions.
- Separate narrow Canvas/Posit allowlists. Exact hosts are the default; subdomains require explicit wildcard entries. No broad Microsoft, Office or institutional-domain access by default.
- Online handoff requires a fresh Edge `edge://policy` JSON export, exact required effective policies, and staff live checks of off-list blocking, login, AI UI and removable storage.
- Full-screen Edge startup; compact student toolbar and staff PIN handoff retained.
- Windows-supported Edge AI policy selection based on installed Edge version. This targets Edge features only, not AI embedded inside allowed websites.
- Separate Beta 3 global configuration endpoint and last-known-good cache. Network/config errors retain local fallback. These GitHub files are staged locally, not live yet.

## Important: affected Beta 2 laptop
The old registry writer could erase unrelated values while writing selected policies. Its snapshots do **not** contain a complete prior baseline. Installing Beta 3 does not reconstruct that lost information. Do not keep running old restrictions or the old restore helper. Preserve snapshots and independently review/repair affected branches with a qualified Windows administrator and a known-good baseline. Beta 3 offers read-only assessment and selected recorded-value restoration; approval is an administrator attestation, not proof that unrecorded values were recovered.

## One installer — after Windows validation
The planned `AccommodationTestManager-Setup-Beta3.exe` installs the app, private .NET runtime and protected helper together. Open setup from the standard testing account and authorize installation with separate administrator credentials. Run the installed app normally, **not** elevated. No separate helper install or PowerShell typing is intended.

The first Beta 3 installation must use its standalone setup: older Beta 2 update checks only recognize the Beta 2 release channel. Beta 3 retains Check for updates for subsequent compatible releases. Setup preserves settings, sessions and snapshots. Old folder/product identifiers remain intentionally stable for recovery compatibility; they are not a fresh data reset.

## Browser handoff
1. Start a synthetic online session. Close Edge normally, including background instances; diagnostics show remaining processes before UAC.
2. In the exam Edge window, visit `edge://policy`, reload policies and Export to JSON.
3. Import that fresh export in the app's browser verification window.
4. Check an off-list site receives a policy block, the required login/test flow works, Edge AI controls are unavailable, and USB storage is inaccessible. Restore the exam tab and full-screen mode.
5. Staff approves handoff. A missing/ignored/mismatched policy blocks approval.

The export is staff-supplied evidence, not a signed browser attestation. Live checks are staff confirmations, not automated navigation tests. Full-screen and the PIN overlay are **not** OS application lockdown. Students knowing the Windows account password can unlock Windows; the app PIN only protects app actions.

## Configuration
Staff edits local settings and allowlists through Settings. Staged central files are in `GlobalConfiguration`; they belong at `global-config-beta3/` in the existing repository later. Never upload PINs, accounts, student data, runtime sessions or protected snapshots. New global config is validated and cached separately from the old broad Beta 2 cache. Apply changes between sessions, not mid-test. Required authentication/project dependencies still need real-laptop verification; add reviewed specific hosts rather than broad roots.

## Validation and limits
See `VALIDATION.md` and `TEST-CHECKLIST.md`. Local compilation and mocked tests passed, but native Windows registry/WPF/installer/UAC/Word/Edge tests are pending. Edge >=139 is required for the selected baseline AI policies; applicability varies by version/profile. Edge >=148 adds newer Copilot controls. Any ignored/unsupported required policy or remaining AI UI must block handoff, not be treated as success.

No OS app lockdown, protected exam-data broker, secure individual staff identity, in-site AI enforcement, or central session portal is supplied. Use dummy data only until device acceptance and institutional security review are complete.

## Development / deferred release
Open `AccommodationTestManager.sln` with .NET 10 WPF tools. `ReleasePreparation/build-beta3.yml` is a staged manual Windows CI workflow. It builds an installer artifact only after native tests; it does not automatically publish a public release. Copy the source/workflow/config to GitHub and run validation only when publication is authorized. No download link for this Beta 3 has been published yet.
