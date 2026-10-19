# Beta 3.4 — visual supports and session-window candidate

Synthetic testing only. Not a production kiosk or a claim that every requested feature is complete.

## Implemented
- Three opt-in supports: pointer-following reading guide, gentle warm screen tint, larger student controls. Saved with the local session; old sessions default off. Guide/tint support Word and online tests; larger controls support all modes. Choices do not enter Firebase metadata.
- Student switches for guide/tint. Click-through, non-activating overlays follow test-window bounds. No document/site formatting or Windows-wide setting changes. Staff mode hides overlays; ending a session removes them.
- Best-effort foreground persistence for the intended Word document / exact online test profile. Accessibility tools and authorized staff interaction remain available. Windows may decline foreground activation: this is convenience focus assistance, NOT keyboard/application/data lockdown.
- Staff PIN suspends focus assistance before revealing the staff screen. Returning to an active test hides staff controls without resetting time or reapplying restrictions.
- Exact-profile session Edge launch/window lookup/normal close. Ownership is checked against process command line, Windows session, creation time and executable. Unreadable ownership pauses restoration. No process killing or automated dismissal of save/download prompts.
- Online completion closes that test browser after staff verifies actual website submission, before machine restoration. Explicit PIN-authorized abandonment closes the browser and restores controls without recording successful submission. Local records/profile remain archived. Failures preserve the unfinished session for retry.
- Existing Firebase anonymous metadata directory, offline queue and ordinary central defaults retained. No cloud file storage, no production Firebase schema/rule changes.

## Still outstanding
- Automatic Canvas/Posit effective-policy verification: manual browser preflight remains. Word automatic startup remains available when enabled. No verification silently bypassed.
- PIN-only privileged machine controls: installed helper still requires administrator consent; constrained privileged broker is not included.
- Central staff/PIN publishing and a web editor: staff/PIN remain local. Firebase central defaults currently cover timing/recovery settings only.
- OS kiosk/Assigned Access, all-app blocking, reliable in-site AI blocking, remote file opening or student-data cloud storage.

## Laptop acceptance
1. Synthetic Word and online tests: select approved supports, toggle guide/tint, check larger controls, confirm original content/settings unchanged. Check Voice Access/Narrator and save prompts remain accessible.
2. Click another app: exam returns when Windows permits. Student Staff → cancel PIN: staff screen stays hidden; authorize PIN: focus assistance pauses. Return using student-controls action without restarting time.
3. Complete existing browser preflight. Finish online test, verify actual website submission, complete: only its profile closes normally. Test abandonment separately; never treat it as submission.
4. Simulate save/close refusal and restoration failure: keep unfinished records and restoration status. Never delete snapshots/legacy review records to clear a failure.
5. Test interruption/recovery, multiple monitors/DPI, actual Word/Edge and accessibility. CI fixtures do not certify these combinations.
6. Verify two-laptop/offline sync. Student data, identifying paths, documents and accommodation selections remain local.

Installation still needs administrator approval; run the app itself as the standard testing user. Do not upgrade with unfinished tests or unresolved restoration. Windows CI/installer results are reported separately after validation.
