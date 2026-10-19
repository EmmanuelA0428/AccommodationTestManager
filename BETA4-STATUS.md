# Beta 4 — source draft, not a published release

Version: 1.0.0-beta.4.0. Published release remains Beta 3.4.
Do not install this source as a production-ready release.

## Implemented in this draft
- Restricted Windows service for PIN-authorized Apply/Restore/ExportAccess; one-time administrator installation/enrollment. Fixed helper/actions only, interactive local pipe clients, protected PIN verifier, short-lived grants, throttling, and administrator PIN reset. No plaintext PINs in cloud.
- Update shutdown handles secondary windows; installer waits up to 30 seconds for app exit, never force-kills it, preserves snapshots and previous files, and attempts rollback on service/setup failure.
- Automatic Word/online startup checks instead of ordinary manual developer preflight. Browser checks validate scoped registry configuration and an owned browser window, not independently exported effective policies or full lockdown.
- Direct cancellation from recovery without reopening the document. Restore failures remain RecoveryRequired with cancellation pending; saved work and snapshots retained.
- Combined local/cloud test directory with timestamps, current laptop display name, contextual actions, and metadata-only remote records. Advanced damaged-metadata recovery remains available separately.
- Compact single-row student toolbar with staff icon; optional larger targets. Developer feature/preview entry points hidden. Shorter prompts.
- Sync indicator with last sync/pending count and retry. Offline staff outbox, stable staff IDs, add/edit/deactivate, idle-only activation, explicit conflict resolution, and current-device label syncing.
- Strict proposed Firestore staff-field rules. No document/file upload added.

## Checks performed locally
- App, broker and Windows UI harness compile with zero warnings/errors using .NET 10 Windows targeting on Linux.
- 263 portable application/coordinator checks pass (mock Word/browser/restrictions).
- Firebase emulator run: 276 application/integration checks and 50 Firestore rule checks pass.
- 21 setup guards pass (filesystem/mocked process polling, not an actual Windows install).
- 23 mocked network checks and 3 early-failure diagnostic checks pass.
- PowerShell scripts and proposed Windows workflow parse successfully.

## Release blockers / not done
- Not uploaded or committed to GitHub; no Beta 4 release or installer published.
- Production Firebase rules have NOT been deployed. Existing production rules will not permit the new staff collection/owner label writes until reviewed deployment.
- Proposed Windows workflow has NOT run: native installation/uninstallation, service lifecycle, and WPF UI execution remain unverified.
- Real standard-user PIN start/finish/cancel, administrator PIN reset, popup/update handoff, failed-upgrade rollback, reboot/crash recovery, Word COM, USB reconnect and browser behavior require Windows laptop validation.
- Full Windows kiosk/application lockdown, protected exam storage, and comprehensive AI/site-feature blocking are NOT implemented.
- PIN synchronization between laptops is not included. Machine-control PIN enrollment/reset is local and protected; shared staff roster does not carry PINs.

Historical install/state paths are intentionally retained for upgrades. Do not delete legacy snapshots or clear review gates to force installation.
