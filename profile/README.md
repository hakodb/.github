# hakodb organization

**Building local-first, zero-deploy data infrastructure — one engine, 13 deliverables, zero services to operate.**

---

## Mission

The `hakodb` org ships a complete embedded document database ecosystem:

- **Core engine** (`hakodb/hakodb`) — Rust, in-process, vector + graph search, encryption, multi-plane sync
- **Flat C ABI** (`hakodb.h`) — 179 functions, opaque handles, stable across versions
- **Language SDKs** — Go, TypeScript/Node/Bun, Pascal, Tauri (Rust + TS)
- **Operational tooling** — CLI, HTTP gateway, cloud hub, cluster dispatcher, balancer, MCP server
- **Documentation & site** — hakodb.github.io + llms.txt for AI assistants

Every repo is a thin wrapper over the same engine. No duplicated logic, no fragmented APIs.

---

## Repositories

| Repo | Role |
|------|------|
| [`hakodb`](https://github.com/hakodb/hakodb) | Core engine (Rust) |
| [`hakobackend`](https://github.com/hakodb/hakobackend) | HTTP gateway + pluggable DB drivers |
| [`hakocli`](https://github.com/hakodb/hakocli) | Terminal REPL + mesh/cloud networking |
| [`hakogo`](https://github.com/hakodb/hakogo) | Go SDK (cgo) |
| [`hakojs`](https://github.com/hakodb/hakojs) | JS/TS SDK (koffi FFI) |
| [`hakotauri`](https://github.com/hakodb/hakotauri) | Tauri gateway crate (Rust) |
| [`hakotaurits`](https://github.com/hakodb/hakotaurits) | Tauri TS client (`@hakodb/tauri`) |
| [`hakopascal`](https://github.com/hakodb/hakopascal) | Lazarus/Free Pascal wrapper + components |
| [`hakocloudserver`](https://github.com/hakodb/hakocloudserver) | Cloud-sync hub + admin console |
| [`hakocluster`](https://github.com/hakodb/hakocluster) | In-process replica dispatcher |
| [`hakobalancer`](https://github.com/hakodb/hakobalancer) | L7 balancer for hakobackend (early) |
| [`hakomcp`](https://github.com/hakodb/hakomcp) | MCP server over stdio |
| [`hakobackend-ts`](https://github.com/hakodb/hakobackend-ts) | TS client for hakobackend (`@hakodb/backend`) |
| [`hakodb.github.io`](https://github.com/hakodb/hakodb.github.io) | Docs site & manual |

---

## Governance

- **Single maintainer** — core engine decisions by @hakodb; SDKs and tooling follow engine API
- **Versioning** — engine on `0.x` (pre-1.0, breaking changes in minor); SDKs pin to engine versions in their READMEs
- **Security** — report privately via GitHub Security Advisory

---

## Contributing

1. **Start with the engine** — if it touches storage, query, sync, or C ABI, open an issue in `hakodb/hakodb` first
2. **SDK changes** — match the engine's new surface; add tests in the SDK repo
3. **Tooling changes** — `hakobackend`, `hakocli`, `hakocluster`, `hakobalancer`, `hakomcp` follow engine releases
4. **Style** — Rust: `cargo fmt --all` + `cargo clippy`; TS: `biome check`; Pascal: `fpc -S2 -Cn`
5. **Tests** — every non-trivial change needs a test (unit for engine, integration for SDKs/tooling)

See individual repos for `CONTRIBUTING.md` where present.

---

## Community

- **Discussions** — per-repo (engine → `hakodb/hakodb/discussions`)
- **Issues** — per-repo; cross-cutting concerns get a tracking issue in the engine repo
- **Chat** — none yet; open a discussion if you'd like one
- **Docs** — <https://hakodb.github.io/> (manual, llms.txt, API reference)

---

## License

All repositories are **MIT licensed** — see each repo's `LICENSE-MIT`.

---

## Contact

- **Org:** <https://github.com/hakodb>
- **Security:** GitHub Security Advisory (private)
- **General questions:** open a discussion in any repo