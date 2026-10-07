# Accommodation Test Manager

Windows accommodation testing beta. **Public download; synthetic testing only.**

## Install with one setup file

[**Download the Beta 2 Hotfix 1 setup EXE**](https://github.com/EmmanuelA0428/AccommodationTestManager/releases/download/v1.0.0-beta.2.1/AccommodationTestManager-Setup-Beta2-Hotfix1.exe)

1. Download the EXE (no GitHub sign-in needed).
2. Double-click it, approve Windows administrator authorization, and follow the short wizard. App, helper and required .NET runtime are bundled together; no ZIP extraction or manual PowerShell installation.
3. Close setup, sign in to the **standard shared testing account**, and open the Beta 2 desktop shortcut normally (not Run as administrator).
4. Register laptop/staff settings and run the installed synthetic test checklist before any supervised trial.

Requires Windows 11 x64, Edge, and desktop Word for Word mode. The runtime is bundled per app, not installed system-wide. Setup does not apply test restrictions; starting/restoring restricted tests still needs separate administrator authorization.

**Unsigned beta:** Windows may show Unknown Publisher or SmartScreen warnings. Have IT review/approve deployment. Do not disable security requirements to make it run. This is a GitHub download, not a Microsoft Store-certified app.

## Updates and uninstall

Close the app normally and restore unresolved machine controls first. Setup refuses pending/corrupt restriction snapshots. Existing local configuration, exam sessions and protected helper snapshots are preserved. No automatic updater is included.

## Important limitations

No OS app lockdown, protected student-data storage, secure staff identity, comprehensive in-site AI prevention, central configuration sync or online portal. A silent install/uninstall smoke test passed on GitHub’s Windows runner. Windows 11 laptop/UAC/Word/browser acceptance testing and IT review remain required. Use personal laptops only for unenforced UI/Word checks; restriction tests belong on dedicated approved equipment. No real student records in this beta yet.

## Developer files

The complete Visual Studio project remains inside **AccommodationTestManager-Beta2-Hotfix1.zip** under Releases. GitHub's automatic Source code ZIP is not the full app project. Normal staff installation should use the EXE above.

Never upload student documents, runtime sessions, browser profiles, saved staff PIN configuration or credentials to this repository.
