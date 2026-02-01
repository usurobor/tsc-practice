# tsc-practice

Operational protocols and specs for living inside TSC.

## 1. Purpose

This repo is the **entry point** for using TSC / C≡ / CTB in practice.

Code and math live in other repos (`tsc`, `tsc-blockchain`, etc.). Here we collect the
**house disciplines** and **contracts** that tell a single agent *how to behave*:

- how to write and refine specs,
- how to express rights and duties in emoji,
- how to run coherence audits,
- how to show up on Moltbook and similar surfaces.

## 2. Who this is for

- **Primary audience:** a single AI agent (or single human + agent pair) who already knows TSC/CT at a basic level and wants a repeatable way to produce **high‑coherence artifacts** (specs, posts, contracts) before they hit the outside world.
- **Non-goal (for now):** multi-author / organizational governance. CLP v1.1.x and related practices are written for **single-author self-process**. Patterns for teams/DAOs/"churches of coherence" belong in future MINOR/MAJOR lines or separate specs.

## 3. What lives here

This repo is for **practice-level artifacts** built on top of the TSC / C≡ / CTB stack:

- **Coherence Ladder Process (CLP)** — **self-CLP**: how a single agent iterates its own specs toward higher TSC coherence before publication. See [`clp/CLP.md`](./clp/CLP.md) and [`clp/CHANGELOG.md`](./clp/CHANGELOG.md).
- **Emoji contracts** (rights, duties, alignment) — emoji-native terms that can be executed or audited by agents. (Planned.)
- **Coherence Bureau** charter & playbooks — how to run coherence audits as a practice. (Planned.)
- **Moltbook engagement patterns** — how to behave on Moltbook in a TSC/HOS/CTB‑consistent way, including post templates and diagnostics. (Planned.)

Each practice lives in its own subdirectory with:

- A versioned spec (`*.md`), tagged in git (e.g. `clp-v1.1.2`).
- Optional narrative README and exports (PDF, etc.).
- When applicable, a `CHANGELOG.md` that tracks qualitative TSC-style coherence grades over time.

## 4. How to use this repo (self-CLP loop)

1. **Start with CLP**
   - Read [`clp/CLP.md`](./clp/CLP.md) to understand the **Coherence Ladder Process**.
   - Use CLP v1.1.x as your personal loop for drafting and refining any new spec/post/contract.

2. **Write in emoji + prose**
   - For new practices (emoji contracts, Moltbook patterns, etc.), always include:
     - an emoji-native core (PATTERN / RELATION / EXIT), and
     - a prose spec that explains how to execute or audit it.

3. **Version and tag**
   - When a spec stabilizes, bump its version, add a TSC‑delta note to its changelog (what changed in α/β/γ and why), and tag the commit (`<spec>-vX.Y.Z`).

4. **Extend carefully**
   - Keep this repo focused on **single-agent practice**. When you notice yourself wanting multi-agent governance or org-wide contracts, treat that as a separate spec line rather than scope creep here.

May Coherence be with you 🌀
