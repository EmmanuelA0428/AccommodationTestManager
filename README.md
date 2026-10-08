# Accommodation Test Manager

Windows accommodation testing beta. **Public download; synthetic testing only.**

## Install with one setup file

[**Download the Beta 2 Update 2 setup EXE**](https://github.com/EmmanuelA0428/AccommodationTestManager/releases/download/v1.0.0-beta.2.3/AccommodationTestManager-Setup-Beta2-Update2.exe)

1. Download the EXE (no GitHub sign-in needed).
2. Double-click it, approve Windows administrator authorization, and follow the short wizard. App, helper and required .NET runtime are bundled together; no ZIP extraction or manual PowerShell installation.
3. Close setup, sign in to the **standard shared testing account**, and open the Beta 2 desktop shortcut normally (not Run as administrator).
4. Register laptop/staff settings and run the installed synthetic test checklist before any supervised trial.

Requires Windows 11 x64, Edge, and desktop Word for Word mode. The runtime is bundled per app, not installed system-wide. Setup does not apply test restrictions; starting/restoring restricted tests still needs separate administrator authorization.

**Unsigned beta:** Windows may show Unknown Publisher or SmartScreen warnings. Have IT review/approve deployment. Do not disable security requirements to make it run. This is a GitHub download, not a Microsoft Store-certified app.

## Update 2: navigation and layout

Continue now allows draft setup navigation while showing an explicit recovery warning. **Start Test still requires unresolved sessions and machine controls to be resolved.** Recovery status is rechecked after staff actions; no old exam is deleted to enable a button. The staff dropdown is full-width and 44 DIP high, and settings/theme icons align with the other toolbar buttons.

**Already on Update 1?** Open **Settings → Updates → Check for updates**. It should offer **v1.0.0-beta.2.3**. Download/install between tests only: the updater refuses current/unfinished sessions and pending machine controls. The new release was checked with the actual released Update 1 updater for detection, checksum/digest download, Internet-origin marking and rejection of tampered bytes before launch.

## Retained Update 1 improvements

Word save/recovery file sharing and stable-capture checks; compact one-row student controls; dark-mode fixes and quick theme toggle; Security summary merged into Review; editable auto-filled asset tag; administrator-authorized forgotten-PIN reset; Settings > Updates for later compatible Beta 2 releases. Staff names remain manually entered.

Update 1 must first be installed with its EXE. Older versions do not have the new update button. See the release notes for preserving/recovering an unfinished session when the old Finish is broken. Never delete a session just to update.

Windows automated tests use mock Word; actual Word COM, device-specific WPF visuals and the real standard-account/separate-admin PIN reset must be checked with a dummy exam on Windows 11.

## Updates and uninstall

Close the app normally and restore unresolved machine controls first. Setup refuses pending/corrupt restriction snapshots. Existing local configuration, exam sessions and protected helper snapshots are preserved. A manual Check for updates section is included in Settings. It verifies download integrity, retains Windows Internet-origin marking, and requires staff/admin approval. No silent automatic updates.

## Important limitations

No OS app lockdown, protected student-data storage, secure staff identity, comprehensive in-site AI prevention, central configuration sync or online portal. Silent install/uninstall and native WPF synthetic navigation/layout/update-button checks passed on GitHub’s Windows runner. Windows 11 laptop/UAC/Word/browser acceptance testing and IT review remain required. Use personal laptops only for unenforced UI/Word checks; restriction tests belong on dedicated approved equipment. No real student records in this beta yet.

## Developer files

The complete Visual Studio project remains inside **AccommodationTestManager-Beta2-Update2.zip** under Releases. GitHub's automatic Source code ZIP is not the full app project. Normal staff installation should use the EXE above.

Never upload student documents, runtime sessions, browser profiles, saved staff PIN configuration or credentials to this repository.
