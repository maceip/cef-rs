# navigator example

`navigator` is a direct fork of the `examples/osr` crate, intended to evolve into an automated web agent runtime.

## Current state

- Tracks the OSR rendering path from `examples/osr` (wgpu + windowless CEF).
- Keeps the same process model and render handler plumbing as the source example.
- Supports startup URL override via `NAVIGATOR_START_URL`.

## Planned integration direction

This crate is intended to target:

1. A modified CEF build from `maceip/cef` on the branch with `journal` in its name.
2. Agent-specific C APIs exposed by that CEF variant.
3. Eventual API compatibility with Vercel Agent Browser:
   <https://github.com/vercel-labs/agent-browser/blob/main/README.md#L92>

## Notes for next iterations

- Gate journal-branch C API wiring under the `journal_agent_c_api` feature.
- Add a thin compatibility layer that maps navigator actions to the future Agent Browser-compatible surface.
