# Beta 4.1 — service identity hotfix

Fixes the Beta 4.0 `Cannot verify service identity` failure for normal testing accounts. The old client opened the SYSTEM service process to inspect it; managed Windows process permissions can deny that query before PIN authentication.

The client now queries the local Windows Service Control Manager with only QUERY_CONFIG/QUERY_STATUS, binds the connected pipe's owner PID to the running AtmMachineBroker own-process service, validates its exact installed binary and LocalSystem account, checks session zero, and rechecks the running PID before transmitting any PIN/token. It fails closed on mismatches or denied queries. No process/service ACL is weakened and no authentication or restoration checks are removed. Diagnostic errors include the failed query stage and Windows error number.

No Firebase/rules changes. PINs, session files and recovery snapshots are not reset or deleted. Install with administrator approval once, then open the app under the normal testing account. This remains an unsigned controlled-pilot prerelease.

Regression tests include spoofed/zero/mismatched PID, stopped/shared services, wrong account/path/arguments, plus a native Windows integration harness that must run as a newly created non-administrator account. It tests actual broker PIN authentication, rejection of wrong PIN and unsupported commands, and rejection of a spoofed pipe without sending credentials. The harness does not apply exam restrictions.

Real managed-laptop start/cancel/finish/restore behavior still requires a synthetic pilot on one laptop before fleet rollout. A successful Windows runner test does not validate every organizational endpoint-security policy.
