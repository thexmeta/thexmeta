## Eser Kelleci

I build the infrastructure that lets AI agents write code without being trusted
to grade their own work: MCP gateways, agent harnesses, and verification that
comes from exit codes rather than a model's opinion.

Nine years of .NET and C# before that, mostly ERP integration delivered at
customer sites. Now working in Rust and TypeScript, directed rather than
hand-written, which is exactly why the verification layer matters to me.

### MCP infrastructure

- **[mcp-proxy](https://github.com/thexmeta/mcp-proxy)** — fork of
  [joshrotenberg/mcp-proxy](https://github.com/joshrotenberg/mcp-proxy) adding
  lazy backend spawning with a persistent warm tool catalog (list requests
  answered with zero processes running), a shared backend pool, endpoint groups
  with namespace-isolated capability filtering, and MCP 2026-07-28 protocol
  support. Design decisions are written up in `docs/adr/`.

- **[avalonia-ui-mcp-rs](https://github.com/thexmeta/avalonia-ui-mcp-rs)** —
  five-crate Rust workspace published on crates.io
  ([core](https://crates.io/crates/avalonia-mcp-core),
  [services](https://crates.io/crates/avalonia-mcp-services),
  [tools](https://crates.io/crates/avalonia-mcp-tools),
  [resources](https://crates.io/crates/avalonia-mcp-resources),
  [server](https://crates.io/crates/avalonia-mcp-server)), MIT, MSRV 1.85.
  18+ MCP tools for AvaloniaUI development; a full Rust rewrite of
  [decriptor/AvaloniaUI.MCP](https://github.com/decriptor/AvaloniaUI.MCP).

- **Rust support in mcp-migration-check**
  ([merged PR](https://github.com/AlpayC/mcp-migration-check/pull/6)) — rule
  MCP010: reads `Cargo.toml` and flags Rust SDKs that cannot serve MCP
  2026-07-28, with remediation for `rmcp`, `rust-mcp-sdk`, and the `tower-mcp`
  `protocol-2026-07-28` feature.

### Upstream

- **[microsoft/vscode#319592](https://github.com/microsoft/vscode/issues/319592)**
  — reported and diagnosed: Copilot Chat threw away valid generated text when a
  custom endpoint returned `finish_reason: "length"`, treating a truncated
  completion as a hard failure instead of rendering the partial response. Fixed
  in VS Code.

### Currently

Writing about why the agent that reports a verdict must never be the agent that
computes it, and looking for remote work on MCP servers, agent harnesses, and
AI infrastructure.

[LinkedIn](https://www.linkedin.com/in/eserkelleci)
