## Eser Kelleci

I build infrastructure for AI coding agents: MCP gateways, agent harnesses, and
verification that decides whether an agent's output is acceptable, instead of
letting the agent grade its own work.

Before this: C# and .NET from 2009 to 2017, then freelance in 2020 and 2021.
Mostly ERP and systems integration, including Dynamics AX e-invoice and e-ledger
integrations with the Turkish Revenue Administration, bank and customs
integrations, and a lead role at Avnet Technology Solutions. Scientific
programming at NYU Langone Medical Center.

**How to read these repos.** Python I write myself. The Rust and TypeScript here
was written by coding agents under my direction: I own the requirements, the
design decisions, the testing and the failure analysis, and I do not claim
hands-on fluency in either language. That division is the subject of the work
itself. If I am not the one writing the code, the verification layer has to be
real.

### MCP infrastructure

- **[mcp-proxy](https://github.com/thexmeta/mcp-proxy)**, fork of
  [joshrotenberg/mcp-proxy](https://github.com/joshrotenberg/mcp-proxy): lazy
  backend spawning with a persistent warm tool catalog (list requests answered
  with zero processes running), a shared backend pool, endpoint groups with
  namespace-isolated capability filtering, and MCP 2026-07-28 protocol support.
  Design decisions are written up in `docs/adr/`.

- **[avalonia-ui-mcp-rs](https://github.com/thexmeta/avalonia-ui-mcp-rs)**:
  five-crate Rust workspace on crates.io, MIT, MSRV 1.85. 18+ MCP tools for
  AvaloniaUI development. A Rust rewrite of
  [decriptor/AvaloniaUI.MCP](https://github.com/decriptor/AvaloniaUI.MCP),
  specified and tested by me, implemented by agents.

- **Rust support in mcp-migration-check**
  ([merged PR](https://github.com/AlpayC/mcp-migration-check/pull/6)): rule
  MCP010 reads `Cargo.toml` and flags Rust SDKs that cannot serve MCP
  2026-07-28, with remediation for `rmcp`, `rust-mcp-sdk` and the `tower-mcp`
  `protocol-2026-07-28` feature.

### Other work

- **[autopacx](https://github.com/thexmeta/autopacx)**: GitHub-release package
  manager for Linux (Electron, React, TypeScript).

### Upstream

- **[microsoft/vscode#319592](https://github.com/microsoft/vscode/issues/319592)**,
  reported and diagnosed: Copilot Chat discarded valid generated text when a
  custom endpoint returned `finish_reason: "length"`, treating a truncated
  completion as a hard failure. Fixed in VS Code by the maintainers.

### Currently

Agent harness design, guardrails and verification. The idea I keep returning to:
the agent that reports a verdict must never be the agent that computes it.
Looking for remote work on agent infrastructure, developer tooling and systems
integration.

## Contact

- Email: eserkelleci@gmail.com
- LinkedIn: https://www.linkedin.com/in/eserkelleci
