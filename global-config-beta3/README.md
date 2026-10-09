# Public global configuration
No staff names, PINs, student data, identities, passwords, executable paths or scripts.

Edit manifest.json for save/time defaults or starting pages; increase Version for EVERY manifest/policy change. Large URL lists remain separate under allowlists/. After editing a list, calculate its SHA-256 and update the matching Sha256 in the manifest. Do not weaken a list without an exam-policy review. A small maintenance script (Rehash-GlobalConfig.ps1) is included in the full source ZIP. Commit all changed files together.

The app reads a fixed public HTTPS GitHub path, validates data only, atomically caches one combined bundle, and freezes policy in each session. Invalid/missing/offline/rolled-back updates keep the last known good version. No independent config signature; GitHub write access is policy-admin access. This beta uses user-local cache, not a protected policy broker.

Staff/PIN/device settings stay local. Disable Use global configuration in app Settings to use local edits. Automatic refresh never executes code or accepts remote helper paths.
