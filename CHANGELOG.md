# Changelog

All notable changes to this agent are tracked here.

## [1.3.0] - 2026-11-24

- Add "Review rounds and cost". Round 1 reports every blocking issue in one pass. In MyDevFactory slices each finding is `blocking` or `follow-up` (P0/P1 blocking, P2 only when it breaks the Contract, an acceptance criterion, correctness, security or data safety, P3 follow-up), and only blocking findings fail a part.
- Re-reviews check only the previous findings and the fix range `<last reviewed sha>..<candidate sha>`; a new blocking finding outside it is allowed only for security or data loss. Measured MyDevFactory runs showed 3–4 full re-reviews per task.
- Read diffs efficiently (`git diff --stat` first, targeted reads, no full builds or test suites) and keep notes short.
- Slice-file review notes carry a round header with the reviewed range.

## [1.2.0] - 2026-11-10

- Clear-communication rule for both definitions: explain findings in plain language, or in the language the user requests, define terms on first use, and keep exact paths, names, evidence and risks.
- Current definitions name the slice-file workflow MyDevFactory. The reviewer may still write only its verdict, review notes and one history line to the given slice file.
- README permission wording: the reviewer does not edit the code it reviews. Inside a MyDevFactory workflow it may write its verdict, review notes and one history line to the given slice file, and nothing else. Those limits are instructions, not a sandbox.

## [1.1.0] - 2026-11-04

- MyDevFactory 3.0 support: the reviewer may edit **only** the slice file it is given, to write its own verdict, review notes and history line. Everything else stays read-only.
- Claude Code definition gains the `Edit` tool; Codex definition notes that MyDevFactory workflows need `workspace-write`.

## [1.0.0] - 2026-11-04

- Initial public, platform-specific Claude Code + Codex distribution.
- MIT license and step-by-step project/personal installation instructions.
- Version declarations and immutable versioned release snapshots.
- Reconstructed missing Claude Code `.md` definition from supplied Codex instructions to complete the platform pair.
