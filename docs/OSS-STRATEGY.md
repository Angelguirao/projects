# OSS strategy — macro problems × personal fit

Living map for **where to contribute upstream** vs **what to build in the sibling stack**.

**Sources (read, don’t approximate):**

- [80,000 Hours — problem profiles](https://80000hours.org/problem-profiles/) — official ordering and framing
- [VISION.md](./VISION.md) — compose OSS, own the glue
- [money/README.md](../money/README.md) — Bitcoin ops layer (not Core source)

**Framework:** 80k uses **scale × neglectedness × tractability**. This doc adds a fourth column for software engineers: **OSS tractability** — can a skilled contributor plausibly help via open-source code?

| OSS tractability | Meaning |
|------------------|---------|
| **High** | Mature repos, active maintainers, clear PR paths |
| **Medium** | Real OSS, but niche, academic, or needs domain partners |
| **Low** | Mostly policy, orgs, or no welcoming maintainer community |

**80k caveat (April 2025):** they are focused on navigating AGI; non-AI rankings are **less actively maintained**. Personal fit can outweigh rank. Not everyone should work on #1.

---

## List A — 80,000 Hours problems → OSS projects

Mapped to **their current ranked list**, not a generic “world problems” grab bag.

### Core problems (ranks 1–3)

| Rank | 80k problem | Profile | OSS tractability | Best OSS to work on |
|------|-------------|---------|------------------|---------------------|
| 1 | Power-seeking AI | [risks-from-power-seeking-ai](https://80000hours.org/problem-profiles/risks-from-power-seeking-ai/) | **High** | **LM Evaluation Harness**, **Inspect** (UK AISI), **Garak**, **TransformerLens**, **nnsight**, **vLLM**, open eval/benchmark repos |
| 2 | Extreme power concentration | [extreme-power-concentration](https://80000hours.org/problem-profiles/extreme-power-concentration/) | **High** | **Bitcoin** (see [§ Bitcoin](#bitcoin)), **Signal**, **Tor**, **Matrix**, **WireGuard**, **Nextcloud**, **Keycloak**, **Let's Encrypt** |
| 3 | Engineered pandemics | [preventing-catastrophic-pandemics](https://80000hours.org/problem-profiles/preventing-catastrophic-pandemics/) | **Medium** | **Nextstrain**, **Galaxy Project**, **Biopython** ecosystem, **OHDSI/HADES**, **OpenMRS**; dual-use screening often academic/gov repos |

### Emerging priorities (rank 4 — entrepreneurial)

High upside; fewer paved roads. 80k groups these under [#4 Emerging priorities](https://80000hours.org/problem-profiles/).

| Sub-problem | Profile | OSS tractability | Best OSS to work on |
|-------------|---------|------------------|---------------------|
| Moral status of digital minds | [moral-status-digital-minds](https://80000hours.org/problem-profiles/moral-status-digital-minds/) | **Low** | Research + governance; almost no mature contributor communities |
| Gradual disempowerment | [gradual-disempowerment](https://80000hours.org/problem-profiles/gradual-disempowerment/) | **Medium** | Human-in-the-loop agent patterns, provenance, memory — **OpenClaw**, agent memory OSS; your glue stack |
| S-risks | [s-risks](https://80000hours.org/problem-profiles/s-risks/) | **Low** | Niche research repos |
| AI-enhanced decision making | [ai-enhanced-decision-making](https://80000hours.org/problem-profiles/ai-enhanced-decision-making/) | **Medium** | **Pol.is**, **Decidim**, **Loomio**, **Consul**, **Yjs**, **Automerge**, forecasting OSS |
| Space governance | [space-governance](https://80000hours.org/problem-profiles/space-governance/) | **Low** | Minimal OSS surface |
| Catastrophic AI misuse | [catastrophic-ai-misuse](https://80000hours.org/problem-profiles/catastrophic-ai-misuse/) | **Medium** | **Garak**, secure sandboxes, biosecurity + AI screening tooling |

### Remaining ranked problems (5–9)

| Rank | 80k problem | Profile | OSS tractability | Best OSS to work on |
|------|-------------|---------|------------------|---------------------|
| 5 | Great power conflict | [great-power-conflict](https://80000hours.org/problem-profiles/great-power-conflict/) | **Medium** | **Tor**, **Signal**, **OSM**, crisis/open data tooling; **Bitcoin** (censorship-resistant settlement) |
| 6 | Factory farming | [factory-farming](https://80000hours.org/problem-profiles/factory-farming/) | **Low** | **Open Food Facts**, traceability libs; most impact is not “join a GitHub repo” |
| 7 | Wild animal suffering | [wild-animal-welfare](https://80000hours.org/problem-profiles/wild-animal-welfare/) | **Low** | Academic ecology/simulation repos; few welcoming communities |
| 8 | Global health | [health-in-poor-countries](https://80000hours.org/problem-profiles/health-in-poor-countries/) | **High** | **DHIS2**, **OpenMRS**, **ODK**, **OpenG2P** |
| 9 | Climate change | [climate-change](https://80000hours.org/problem-profiles/climate-change/) | **Medium** | **PyPSA**, **OpenClimateFix**, **OpenEnergyPlatform**, **OSM** |

### Other 80k profiles (not on main ranked list)

| Topic | Profile / article | OSS tractability | Best OSS |
|-------|-------------------|------------------|----------|
| Science policy & infrastructure | [science-policy-and-infrastructure](https://80000hours.org/article/science-policy-and-infrastructure/) | **High** | **Jupyter**, **Galaxy**, **Zarr**, **DVC**, **Renku**, **RO-Crate** |
| Governance for global public goods | (related articles) | **Medium** | Wikimedia stack, **Decidim**, **Pol.is** |
| Civilisational resilience | [civilisational-resilience](https://80000hours.org/problem-profiles/civilisational-resilience/) | **Medium** | **Linux**, **Sigstore**, archive tooling; **Bitcoin** full-node ecosystem |
| Nuclear weapons | [nuclear-security](https://80000hours.org/problem-profiles/nuclear-security/) | **Low** | **OpenMC** (niche); mostly policy/orgs |
| Stable totalitarianism | [stable-totalitarianism](https://80000hours.org/problem-profiles/stable-totalitarianism/) | **Medium** | Overlaps #2 — sovereign comms, **Bitcoin**, privacy OSS |

### Engineer-specific summary (rank ≠ OSS ease)

**Best OSS leverage on 80k’s list:**

1. Power-seeking AI → evals, monitoring, interpretability
2. Extreme power concentration → **Bitcoin**, Signal, Tor, self-hosted stacks
3. Engineered pandemics → bioinformatics / health data pipelines
4. AI-enhanced decision making → deliberation & collective intelligence
5. Catastrophic AI misuse → red-team / screening tooling

**High moral rank, poor OSS homes:** factory farming, wild animal suffering, space governance, moral status of digital minds.

---

## Bitcoin

80,000 Hours does **not** have a dedicated “Bitcoin” problem profile. It fits their framework primarily as infrastructure for **#2 extreme power concentration** and **#5 great power conflict** — censorship-resistant money, settlement without permission, and resilience when institutions or rails fail.

| 80k problem | How Bitcoin OSS helps |
|-------------|----------------------|
| Extreme power concentration | Permissionless value transfer; harder to freeze or deplatform than platform money |
| Great power conflict | Neutral settlement layer; full nodes as civic infrastructure |
| Civilisational resilience | Reproducible protocol, thousands of independent node operators |
| Gradual disempowerment (emerging) | Self-custody vs handing financial agency to opaque platforms |

### OSS projects (upstream)

| Layer | Project | Upstream | Notes |
|-------|---------|----------|-------|
| Protocol / node | **Bitcoin Core** | [bitcoin/bitcoin](https://github.com/bitcoin/bitcoin) | Highest bar; read in lab before contributing |
| Lightning | **LND**, **Core Lightning (CLN)**, **Eclair** | [lightningnetwork/lnd](https://github.com/lightningnetwork/lnd), [ElementsProject/lightning](https://github.com/ElementsProject/lightning) | Payments layer; different skill surface than Core |
| Libraries | **rust-bitcoin**, **libsecp256k1**, **btcd** | Various | Good on-ramp for smaller PRs |
| Indexing / explorer | **electrs**, **mempool** tooling | [romanz/electrs](https://github.com/romanz/electrs) | Ops-adjacent; pairs with `money/` compose |
| Ecash / federated | **Fedimint**, **Cashu** | Community custody experiments | Emerging; higher risk |

**OSS tractability:** **High** for protocol-adjacent infra (electrs, libs, Lightning); **Medium** for Core (excellent community, steep ramp).

### This workspace (compose, don’t fork)

| Concern | Owner | Path |
|---------|-------|------|
| Run bitcoind, pins, regtest | **money/** | [money/README.md](../money/README.md), [vendor.yaml](../money/vendor.yaml) |
| Read Core source (time-boxed) | **lab/play/bitcoin-core/** | Disposable; promote patterns into money runbooks |
| Theory — what is money, why Bitcoin | **brain/** | `raw/` → compile → wiki |
| Product billing (fiat) | **holzen/** | Separate from personal Bitcoin stack |

**Contribution path:** operate regtest → testnet → optional mainnet node in `money/` → file issues/PRs from real friction (docs, tooling, electrs compose) → only then consider Core/Lightning upstream.

---

## List B — personal: your repos × 80k problems

**Thesis (one sentence):** agent-native knowledge infrastructure — fleeting thought → durable, inspectable knowledge, with AI as librarian; plus sovereign money ops in `money/`.

### Primary anchors (5-year depth)

| Priority | Where | Your repo | 80k problems served | OSS tractability |
|----------|-------|-----------|---------------------|------------------|
| 1 | Your glue | **brain**, **personal-agent**, **lab** → promote | Gradual disempowerment, AI-enhanced decision making | N/A (you own it) |
| 2 | Personal agent ecosystem | **OpenClaw** upstream | Gradual disempowerment, power-seeking AI (practical control) | **High** |
| 3 | Knowledge + AI search | **Khoj** or **Zotero** (pick one after quality gate) | AI-enhanced decision making | **High** |
| 4 | Sovereign money | **Bitcoin** ecosystem via **money/** | Extreme power concentration, great power conflict | **High** (infra) / **Medium** (Core) |

### Secondary (depth after anchors)

| Project | Fit | 80k angle |
|---------|-----|-----------|
| **OpenHands** | Agent engineering apprenticeship | Power-seeking AI, gradual disempowerment |
| **Pol.is / Decidim / Yjs** | Year 2+ coordination | AI-enhanced decision making |
| **Signal / Nextcloud / Matrix** | If you run them daily | Extreme power concentration |
| **Hugging Face evals** | If `lab` ships benchmarks | Power-seeking AI |
| **Jupyter / Quarto** | If brain outputs go reproducible-research grade | Science infrastructure |

### Watch from lab (don’t lead yet)

| Area | Projects |
|------|----------|
| Collective intelligence | Pol.is, Metaculus-adjacent tools |
| Climate | OpenClimateFix, PyPSA |
| Global health | DHIS2, ODK |
| Factory farming / wild animals | Poor OSS fit despite moral weight |

### Personal ranked plan

| Rank | Effort | Why |
|------|--------|-----|
| 1 | **50%** — brain + personal-agent + lab promote | Nobody else builds your exact seam |
| 2 | **15%** — OpenClaw upstream | Daily use; memory, skills, hooks |
| 3 | **10%** — Khoj or Zotero | External credibility on epistemic infra |
| 4 | **10%** — Bitcoin (`money/` ops → upstream from pain) | Sovereignty; 80k #2/#5; already in stack |
| 5 | **10%** — small extracts to OSS | Skills, provenance patterns, compose recipes |
| 6 | **5%** — holzen when real users | Product; not identity |

---

## Decision rules

### Weekly filter

- **Macro:** Does this help humans know, decide, trust systems, or hold agency at scale? (80k scale/neglect/solve)
- **Personal:** Am I using it in capture → brain → Claw **or** operating it in `money/` this month?

| Both yes | Personal only | Macro only |
|----------|---------------|------------|
| Prioritize | Still OK if it ships quality gate | `lab` experiment, ≤10% time |

### Sequence (first 12 months)

| Phase | Focus |
|-------|-------|
| Months 1–2 | VPS + [quality gate](../personal-agent/deploy/quality-gate.md); capture → brain round-trip |
| Months 3–4 | First OpenClaw upstream PR (docs, skill, or hook from deploy pain) |
| Months 5–6 | Pick Khoj **or** Zotero; integrate with brain/library |
| Months 5–6 | Bitcoin: regtest fluent → [TESTNET](../money/docs/TESTNET.md); optional electrs in `money/compose/` |
| Months 7–12 | Extract one generalizable pattern (skill, compile, or money runbook) → upstream or lab module |

### Anti-patterns

- Linux kernel / random agent framework because it’s famous
- New “Life OS” product repo (see [VISION.md](./VISION.md))
- Bitcoin Core PRs before operating a node in `money/`
- Spreading across six macro problems at once

---

## Cross-map (sweet spot)

```
                    HIGH civilization leverage (80k)
                              │
         Power-seeking AI     │     Gradual disempowerment
         (evals, if lab)      │     (brain + OpenClaw)  ◄── YOU
                              │
    ──────────────────────────┼──────────────────────────► HIGH personal fit
                              │
         Climate / biosecurity│     Bitcoin + money/
         (weak fit)           │     (sovereignty fit)
                              │
                    LOWER personal fit
```

**Sweet spot:** upper-right — **OpenClaw + knowledge infra + your glue**, with **Bitcoin** as the sovereignty/money leg.

---

## Changelog

| Date | Change |
|------|--------|
| 2026-06-23 | Initial doc — faithful to 80k problem-profiles ordering; Bitcoin section; personal stack mapping |
