# Legacy repos — LifeOS

Prior work in [`legacy/`](legacy/). **Not part of the active stack** unless you explicitly revive them.

## What you have

| Repo | GitHub | Was |
|------|--------|-----|
| [legacy/LifeOS-Protocol/](legacy/LifeOS-Protocol/) | `Angelguirao/LifeOS-Protocol` | Open schema — `LifeEvent`, `life://` URIs |
| [legacy/LifeOS-Core/](legacy/LifeOS-Core/) | `Angelguirao/LifeOS-Core` | Self-hosted app — timeline, events, manual plugins |
| [legacy/LifeOS-plugin-sdk/](legacy/LifeOS-plugin-sdk/) | `Angelguirao/LifeOS-plugin-sdk` | Plugin SDK — Spotify, Obsidian, marketplace stubs |
| [legacy/LifeOS-Premium/](legacy/LifeOS-Premium/) | `Angelguirao/LifeOS-Premium` | Hosted SaaS — AI orchestration, connectors, cloud dashboard (commercial) |

These are **your products**, not lab play clones.

---

## Overlap with what you're building now

| LifeOS | Current stack | Overlap | Verdict |
|--------|---------------|---------|---------|
| LifeEvent JSON graph | `brain/wiki/` OKF markdown | Both = personal knowledge over time | **Pick one owner** — brain won |
| `life://` URIs | wiki links, `raw_path`, exhibits | Linking model | **Mine idea**, don't run two graphs |
| Timeline UI (Core) | brain reading room, Phase 4 graph | Visualization | **Defer** — brain Phase 4 or tbd |
| Obsidian plugin (SDK) | Obsidian → `brain/raw/` | Capture path | **Salvage pattern** → lab/adapt if needed |
| Semantic search | `npm run search`, Khoj experiments | Retrieval | brain + lab |
| Plugin / auto-sync | `auto/` dispatch, `ingest.yaml` | Automation | auto is governance; LifeOS plugins are integrations |
| Spotify / mood events | — | Life telemetry | **Out of scope** unless you care |
| Local SQLite/JSON store | git + markdown | Storage philosophy | **brain's md-first is the spine** |
| Premium SaaS orchestration | `personal-agent/` OpenClaw | Personal AI assistant | **OpenClaw won** — don't revive Premium dashboard |
| Multi-agent coordinator (LangGraph) | `auto/` dispatch, Claw skills | Agent orchestration | Mine patterns → lab; auto governs ventures |
| Connectors (GitHub, Notion, Linear, Figma) | Claw skills, auto plugins | Integrations | Salvage as skills, not a second connector manager |
| Premium / marketplace (SDK README) | holzen product | Product | holzen is the venture; LifeOS Premium is a different product line |

### Short answer

**~60% conceptual overlap** with brain (personal graph, capture, search, plugins).  
**Running LifeOS Core + brain in parallel = two sources of truth.** Don't do that.

---

## Recommendation

| Action | Repos |
|--------|-------|
| **Keep on GitHub** | All four LifeOS repos — your history and IP |
| **Don't actively develop** | Unless you choose to *revive LifeOS as a product* instead of brain |
| **Local copy** | `legacy/` (moved 2026-06-21) |
| **Mine, don't merge** | Obsidian plugin, URI linking ideas, plugin registry patterns → lab/adapt notes |
| **Do not** | Merge Core into brain, duplicate timeline UI in tbd without a decision |

### If you must pick one system for "my life + knowledge"

**Use brain** for epistemic work (notes, articles, compile, footnotes, exhibition).

**LifeOS** made sense as an event-sourced life timeline (music, calendar, mood). That is a **different layer** — closer to Quantified Self than OKF wiki. Options:

1. **Archive** — document here, stop local dev (recommended for focus)
2. **Bridge later** — LifeEvent export → `brain/raw/` as markdown (future `lab/adapt/lifeos-export`)
3. **Revive as product** — separate from brain/holzen; needs explicit decision

---

## Relationship to lab

| Type | LifeOS repos | lab/play/bitcoin |
|------|--------------|------------------|
| Ownership | **Yours** (Angelguirao) | Upstream OSS |
| Lifecycle | legacy / track | play → operate / contribute |
| Sync | normal git pull in `legacy/` | sync-learn-clones.ps1 |

See [lab/catalog.yaml](lab/catalog.yaml) entries `lifeos-*`.

---

## Salvage candidates (if mining)

| From | Idea | Where it might go |
|------|------|-------------------|
| Protocol | `life://` as optional link convention | brain frontmatter `life_uri:` experiment |
| plugin-sdk | Obsidian sync patterns | lab/adapt/obsidian-lifeos-notes |
| Core | Timeline React components | tbd or brain UI Phase 4 — only after spec |
| Core | Event import/export | brain/raw ingest adapter |
| Premium | Connector interface pattern | Claw skills or auto runtime adapters |
| Premium | Multi-repo orchestrator | lab study only — auto + personal-agent own dispatch now |

Log mining in [lab/domains/lifeos.md](lab/domains/lifeos.md).

---

## Anti-patterns

- Registering LifeOS as an `auto` venture alongside holzen without scope
- Storing holzen user data in LifeOS Core
- Replacing `brain/raw/notes/journal/` with LifeEvent JSON
- Two auto-sync loops (LifeOS plugin sync + brain watch) on the same Obsidian vault

---

## Decision log

| Date | Decision |
|------|----------|
| 2026-06-21 | Documented as **legacy**; active stack = brain + library + money + lab + tbd + holzen + auto |
| 2026-06-21 | Moved to `legacy/` folder |
| 2026-06-22 | Added **LifeOS-Premium** to legacy index; personal AI → OpenClaw / personal-agent |

Update this table if you revive LifeOS or delete local copies.
