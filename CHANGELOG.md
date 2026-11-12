# Changelog

All notable changes to this agent are tracked here.

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
