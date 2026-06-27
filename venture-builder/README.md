# venture-builder

**Governance for all product ventures** — holzen today, tbd and future ventures tomorrow.

Not Claw. Not daily focus. Not dispatch. Not inside `personal-agent`.

| Concern | Owner |
|---------|-------|
| Venture definitions | `ventures/*.yaml` (this repo) |
| Venture runtime memory | `{venture}/.auto/` in each product repo |
| Product code | `holzen/`, `tbd/`, … |
| Job execution | **dispatch** sibling repo |

## Target layout (when split from `auto`)

```
venture-builder/
├── portfolio.yaml       # venture ids: holzen, tbd, …
├── ventures/
│   ├── holzen.yaml
│   └── tbd.yaml         # when ready
├── constitution/        # shared law for venture jobs
└── schema/              # data model

../holzen/.auto/         # holzen cycle journal (runtime)
../dispatch/             # runs jobs using runtime plugins
../personal-agent/       # Claw + daily focus — separate
```

## Today

Venture-builder files still live in the **`auto/`** repo (`auto/ventures/`, `auto/org/`) alongside dispatch plugins. This repo is the **target home** after the split.

See [personal-agent/shared/DISPATCH-AND-VENTURES.md](../personal-agent/shared/DISPATCH-AND-VENTURES.md).

## Adding a venture

1. Create `ventures/{id}.yaml` (copy `holzen.yaml` template).
2. Add id to `portfolio.yaml`.
3. Product repo at `../{id}/` with `{id}/.auto/` for runtime memory.
4. dispatch runs jobs — venture-builder does not execute agents.

## Not ventures

brain, lab, library, personal-agent are **domains** in daily focus — not entries in venture-builder.
