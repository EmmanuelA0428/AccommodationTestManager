> **Beta 3 development candidate — Windows validation pending.**
> Older Beta 2 restriction helpers contain a registry-write defect that can erase unrelated values. Do not run their restriction/restore actions. Preserve existing snapshots; affected laptops need independent baseline review/repair. The Beta 3 candidate uses a corrected writer but cannot reconstruct unrecorded erased values.

## Beta 3 candidate
- [Beta 3 changes and validation status](BETA3.md)
- [Beta 3 source archive](AccommodationTestManager-Beta3.zip) — source only, not an installer.
- [Source SHA-256](AccommodationTestManager-Beta3.zip.sha256)

A validation-only Windows workflow will build a candidate installer artifact after tests pass. No Beta 3 public installer is published yet. The older releases below are historical, not a recommendation to run the defective helper.

---

# Accommodation Test Manager

Windows accommodation testing beta. **Public download; synthetic testing only.**

## Install with one setup file

[**Download the Beta 2 Update 3 setup EXE**](https://github.com/EmmanuelA0428/AccommodationTestManager/releases/download/v1.0.0-beta.2.4/AccommodationTestManager-Setup-Beta2-Update3.exe)

1. Download the EXE (no GitHub sign-in needed).
2. Double-click it, approve Windows administrator authorization, and follow the short wizard. App, helper and required .NET runtime are bundled together; no ZIP extraction or manual PowerShell installation.
3. Close setup, sign in to the **standard shared testing account**, and open the Beta 2 desktop shortcut normally (not Run as administrator).
4. Register laptop/staff settings and run the installed synthetic test checklist before any supervised trial.

Requires Windows 11 x64, Edge, and desktop Word for Word mode. The runtime is bundled per app, not installed system-wide. Setup does not apply test restrictions; starting/restoring restricted tests still needs separate administrator authorization.

**Unsigned beta:** Windows may show Unknown Publisher or SmartScreen warnings. Have IT review/approve deployment. Do not disable security requirements to make it run. This is a GitHub download, not a Microsoft Store-certified app.

## Update 3: diagnostics, staff handoff and offline configuration

- **View diagnostics** in Current session or Settings > Recovery shows actual helper failures, including early startup rejection. UAC cancellation and helper launch failures have separate messages. No PowerShell commands needed. The specific laptop's Canvas failure is not yet diagnosed: reproduce once after updating, then report Stage/Message.
- Student Finish brings up a persistent app handoff screen. Staff name/PIN is required before Current session, export/verification or resume. Cancelling PIN does not resume. **This is not Windows security lockdown**; students can know the Windows password and still access Windows/other apps. Online submission must be verified separately; no browser force-kill or automatic submission.
- **Public global configuration** lives in [global-config](https://github.com/EmmanuelA0428/AccommodationTestManager/tree/main/global-config). Startup loads validated local cache immediately and refreshes in the background with an 8-second total timeout. Manifest defaults plus separate hash-checked allowlists are atomically cached as one bundle. Offline/invalid/partial/older updates keep prior policy. Existing tests retain their own settings and URLs.
- Managed globally: starting URLs, allowlists, save/recovery defaults and optional default duration. Local: staff/PIN, identity, installed apps, export paths, theme and required controls. Settings > Global config allows local opt-out. Saving local managed fields does not publish to GitHub. Public files must never contain secrets or student/staff records. Configuration is data-only and validated, not independently signed; repository write access is policy-administrator access. Cache is user-local beta storage, not a protected broker.

## Retained Update 2: navigation and layout

Continue now allows draft setup navigation while showing an explicit recovery warning. **Start Test still requires unresolved sessions and machine controls to be resolved.** Recovery status is rechecked after staff actions; no old exam is deleted to enable a button. The staff dropdown is full-width and 44 DIP high, and settings/theme icons align with the other toolbar buttons.

**Already on Update 1?** Open **Settings → Updates → Check for updates**. It should offer **v1.0.0-beta.2.4**. Download/install between tests only: the updater refuses current/unfinished sessions and pending machine controls. The release was checked with the actual released Update 1 updater for detection, checksum/digest download, Internet-origin marking and rejection of tampered bytes before launch.

## Retained Update 1 improvements

Word save/recovery file sharing and stable-capture checks; compact one-row student controls; dark-mode fixes and quick theme toggle; Security summary merged into Review; editable auto-filled asset tag; administrator-authorized forgotten-PIN reset; Settings > Updates for later compatible Beta 2 releases. Staff names remain manually entered.

Versions before Update 1 do not have the update button; install the current Update 3 EXE directly instead. See the release notes for preserving/recovering an unfinished session when the old Finish is broken. Never delete a session just to update.

Windows automated tests use mock Word; actual Word COM, device-specific WPF visuals and the real standard-account/separate-admin PIN reset must be checked with a dummy exam on Windows 11.

## Updates and uninstall

Close the app normally and restore unresolved machine controls first. Setup refuses pending/corrupt restriction snapshots. Existing local configuration, exam sessions and protected helper snapshots are preserved. A manual Check for updates section is included in Settings. It verifies download integrity, retains Windows Internet-origin marking, and requires staff/admin approval. No silent automatic updates.

## Important limitations

No OS app lockdown, protected student-data storage, secure staff identity, comprehensive in-site AI prevention or online session portal. Global configuration does not sync student records or staff identities. Silent install/uninstall, native WPF synthetic navigation/layout/update-button/PIN-dialog checks and early-error reporting checks passed on GitHub’s Windows runner. Windows 11 laptop/UAC/Word/browser acceptance testing and IT review remain required. Use personal laptops only for unenforced UI/Word checks; restriction tests belong on dedicated approved equipment. No real student records in this beta yet.

## Developer files

The complete Visual Studio project remains inside **AccommodationTestManager-Beta2-Update3.zip** under Releases. GitHub's automatic Source code ZIP is not the full app project. Normal staff installation should use the EXE above.

Never upload student documents, runtime sessions, browser profiles, saved staff PIN configuration or credentials to this repository.
