# Fresh machine — clone the stack

This repo is the **meta-map** only (`README.md`, `LEGACY.md`, docs). Sibling repos share the **same parent folder** and are ignored by this git checkout.

## Layout (typical)

```
C:\Users\angel\projects\     ← meta-repo root AND sibling parent
├── README.md              ← tracked
├── LEGACY.md
├── docs/
├── legacy/README.md
├── brain/                 ← own git repo (ignored here)
├── library/
├── money/
├── lab/
├── tbd/
├── holzen/
├── auto/
└── personal-agent/
```

## 1. Create parent + meta-repo

```powershell
mkdir C:\Users\angel\projects -Force
cd C:\Users\angel\projects
git clone https://github.com/Angelguirao/projects.git .
```

If the folder is not empty, clone to a temp dir and copy `README.md`, `LEGACY.md`, `docs/`, `legacy/README.md`, `.gitignore` into the parent, then `git init` and set remote — or clone into empty parent only.

## 2. Active siblings (same parent)

```powershell
cd C:\Users\angel\projects

git clone https://github.com/Angelguirao/brain.git
git clone https://github.com/Angelguirao/library.git
git clone https://github.com/Angelguirao/money.git
git clone https://github.com/Angelguirao/lab.git
git clone https://github.com/Angelguirao/tbd.git
git clone https://github.com/Angelguirao/holzen.git
git clone https://github.com/Angelguirao/auto.git
git clone https://github.com/Angelguirao/personal-agent.git
```

`personal-agent` is **private** — authenticate with `gh auth login` or SSH first.

## 3. Legacy (optional)

Only if mining LifeOS patterns — see [../LEGACY.md](../LEGACY.md). Do not run Core parallel to brain.

```powershell
mkdir legacy -Force
git clone https://github.com/Angelguirao/LifeOS-Protocol.git  legacy\LifeOS-Protocol
git clone https://github.com/Angelguirao/LifeOS-Core.git        legacy\LifeOS-Core
git clone https://github.com/Angelguirao/LifeOS-plugin-sdk.git  legacy\LifeOS-plugin-sdk
```

## 4. First-run pointers

| Task | Where |
|------|--------|
| Stack map | [README.md](../README.md) |
| brain | [github.com/Angelguirao/brain](https://github.com/Angelguirao/brain) |
| Claw / OpenClaw | [github.com/Angelguirao/personal-agent](https://github.com/Angelguirao/personal-agent) |
| OpenClaw scripts | [lab/play/openclaw](https://github.com/Angelguirao/lab/tree/master/play/openclaw) |

Secrets (`.env`, API keys) live in sibling repos or `~/.openclaw/` — never in this meta-repo.
