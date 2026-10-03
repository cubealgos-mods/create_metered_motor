---
title: "create_metered_motor spec — release engineering and distribution"
type: "spec"
category: "create_metered_motor"
---

# Release engineering, distribution and support (`REL`, sheet §7)

| Item | Position |
|---|---|
| Version scheme | `<mod>+<mc>`, SemVer on the mod part over `contracts/public-surface.md`: `1.0.0+26.2` |
| Branches | `development`, `production`; releases are tags on `production` |
| Channels | Modrinth only; CurseForge deferred, as `create_brass_compass` |
| CI | None: `just check` is run locally before every merge: lint, unit tests, game tests. There is no CI service; the repository's home is GitHub (`https://github.com/cubealgos-mods/create_metered_motor`), which carries the public issue tracker. |
| Always a playable build | `just client` boots with Create Fly at every merge |
| Support | Issue tracker only; no SLA; a `SUPPORT.md` says so |
| Ports | A new Minecraft version is a new `+<mc>` build from a port branch; the component version does not change with the game version |

`REL-REQ-001`: every release jar is built by `just release` from a clean checkout at a tag.
`REL-REQ-002`: the release notes list the component version and the Create Fly version tested.
`REL-REQ-003`: the release notes state the tier table in force (`domains/trade.md` §3).
