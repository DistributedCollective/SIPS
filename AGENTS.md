# Agent instructions

Standing rules and the project knowledge base live in the sovryn-spec KB:
`~/sovryn/remake-money/sovryn-spec/AGENTS.md` (branch `tyrone-work`). Read it
first — it governs this repo too (project isolation, commits on / pushes off,
no AI-attribution trailers, commit as Tyrone Johnson, session logging into the
KB, read-only-by-default signing boundary).

Repo role: governance SIP documents. Current branch: `SIP-0096-perimeter-delay`
(`SIP-0096.md`). Final text, revision and SHA256 are byte-pinned into both
sipArgs builders only after all address rows are filled and the text is final
(KB runbook §5.2); the ExitDelayQueue proxy row fills after rollout step 5.
Rollout entry point: KB `sovryn-perimeter/docs/ops/ROLLOUT_CHECKLIST.md`.
