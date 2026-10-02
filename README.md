# brrain

brrain is a local-first, git-backed second-brain plugin for Claude Code and
Codex. It keeps knowledge in a portable plain-Markdown repository and provides
skills for setup, capture, trust-gated synthesis, recall, elicitation, and
consistency auditing.

The plugin contains the engine, skills, hooks, and an empty brain template. It
does not contain anyone's personal knowledge, credentials, or configured brain
repository.

## Included skills

- `brrain:setup` - create, register, clone, select, or inspect a brain.
- `brrain:remember` - capture a provenance-tagged note into staging.
- `brrain:remember-gateless` - write an explicitly approved note directly to
  the canonical corpus.
- `brrain:refine` - synthesize staged captures behind a human trust gate.
- `brrain:recall` - answer questions from canonical pages and pending captures.
- `brrain:interview` - identify and elicit high-value knowledge gaps.
- `brrain:audit` - check the corpus for contradictions, drift, and structural
  problems.

## Storage boundary

Per-device registry state lives under `~/.brrain/`. Brain content lives in a
separate repository selected by the user. The plugin never ships personal brain
content and does not require a hosted service.

## Plugin packaging

This repository is a standalone plugin root and includes manifests for both
Claude Code and Codex. A marketplace can reference this repository directly
instead of embedding a copy of the plugin.
