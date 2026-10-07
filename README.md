# Accommodation Test Manager


Private distribution repository for Windows accommodation testing beta packages.


## Download


Open **Releases**, select **Beta 2 — Hotfix 1**, and download **AccommodationTestManager-Beta2-Hotfix1.zip** under Assets.


Do not use GitHub’s automatically generated “Source code (zip)” download: the complete Visual Studio project, published Windows app, installer and test guides are inside the named release asset.


This repository is private. Downloads require an authorized GitHub account; download through a staff Windows account, not a shared student browser session.


## Installation


1. Use a dedicated, IT-approved Windows 11 x64 testing laptop with .NET 10 Desktop Runtime x64, Microsoft Edge, and desktop Word for Word mode.
2. Extract the entire release ZIP locally. Read README.md and TEST-CHECKLIST.md in the package.
3. Close the existing app normally and preserve any unfinished work. Run Install-Beta2.ps1 with administrator authorization and according to institutional script policy.
4. Run the installed desktop shortcut normally under the standard testing account. Only the helper receives separate administrator authorization.
5. If upgrading after a failed adapter attempt, follow HOTFIX-RECOVERY.md and verify the protected snapshot reports Restored before starting another test.


## Important limits


**Synthetic testing only; not a production-secure exam kiosk.** Scoped network/USB/Edge controls do not provide OS application lockdown, protected student-data storage, secure staff identity, or comprehensive in-site AI blocking. Native Windows acceptance testing and IT review remain required.


Use personal laptops for unenforced UI/Word workflow checks; reserve restriction tests for dedicated approved equipment. No automatic updates, online configuration sync, or student-data portal is included.


Never upload student documents, runtime sessions, browser profiles, saved staff PIN configuration or credentials to this repository.
