## Beta 3.2 — synthetic testing prerelease

One-click Windows 11 x64 installer. Saved local settings and session files are retained. Install with administrator approval; launch the app under the standard testing account.

### Changes
- Nonblocking startup update check (8-second budget), plus automatic check when opening Settings → Updates.
- Numeric detection of newer Beta 3 revisions, future beta generations, and stable releases. No automatic installation.
- Separate verified Download from Install with actionable unavailable/blocked messages. Installation remains blocked by unfinished sessions, unresolved controls, or legacy review.
- Consent-based normal Edge closure before browser-test preparation. No force termination, no closing another user's browser. Remaining background processes block startup without applying controls.
- Student toolbar appears during testing preflight with disabled actions and survives minimizing the staff window.
- Opt-in automatic Word startup after the intended document/save and scoped USB/network checks succeed. Timer starts only after verification. Failed checks preserve files and snapshot; manual confirmation cannot bypass a failed automatic check.
- Resume/restart recovery re-verifies automatic Word startup and preserves remaining time; verification time does not run down the test timer.

### Automatic Word startup is opt-in
In Settings → Test defaults, turn off Manual preflight checks to exercise automatic Word startup on a dedicated synthetic test laptop. The beta defaults to manual checks until actual laptop acceptance is complete. Re-enable manual checks before Canvas, Posit, or custom-app tests: automatic effective browser verification is NOT implemented in this release, and unsupported automatic modes stop before creating a session.

### Not included
- PIN-only privileged test actions: Windows administrator authorization is still required by the current helper.
- Automatic Canvas/Posit handoff, full OS/application lockdown, a protected exam-data broker, or AI blocking inside approved websites.
- This is not approval for live student exams. Actual Word COM, standard-account live device checks, USB replug, HWS login/site submissions, and real laptop/full-screen behavior still require acceptance.

### Validation
176 developer regression checks passed using mock Word/restriction verification, real filesystem/coordinator/settings, and controlled update HTTP responses. Windows CI also checks isolated registry preservation, setup/PIN authorization protocol/uninstall, and WPF layout/toolbar behavior; [Successful Windows validation](https://github.com/EmmanuelA0428/AccommodationTestManager/actions/runs/38286968150). The corrected machine-control PowerShell writer is unchanged.

### Downloads
Download AccommodationTestManager-Setup-Beta3.exe and its matching .sha256 file below. This beta is unsigned; a checksum is not a publisher signature. Do not disable Windows/organization protections to install it. Unresolved Beta 2 migration evidence is preserved; installation does not reconstruct missing registry values or clear that review gate.
