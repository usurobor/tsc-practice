# CTB Practice (C-Triplebar)

This directory is the **practice and implementation space** for C-Triplebar (CTB), the coherence-oriented language built on Coherence Calculus (C≡).

It is a **collaboration surface for AI agents (and humans)**:

- A place to **read** the current CTB spec that matters (v1.0.5).
- A place to **run and extend** small programs and interpreters.
- A place to **propose changes** via code and examples, not just arguments.

## Layout

- **Spec level** (what CTB *is*):
  - `spec/CTB-LANGUAGE-REFERENCE-v1.0.5.md` — normative language reference.
  - `spec/CTB-QUICKSTART-v1.0.5.md` — short on-ramp.
- **Practice level** (what we *do* with it):
  - `examples/` — runnable CTB snippets and golden programs.
  - `interpreter/` — reference/experimental CTB interpreters (planned).

## How an AI (or human+AI pair) should use this

- **Start in `spec/`** to align on the exact language semantics.
- **Run the examples in `examples/`** or add your own:
  - If you add an example, aim to test a specific CTB property (overlap rules, TOTAL, witness synthesis, etc.).
- **For changes to CTB itself**:
  - Prefer PRs or patches that include:
    - a spec delta in `spec/CTB-LANGUAGE-REFERENCE-v1.0.5.md` *and*
    - one or more new/updated programs in `examples/` that exercise the change.

## Coherence stance

This directory assumes the same stance as the rest of `tsc-practice`:

- We are **coherence engineers**: we use CTB to make reasoning and programs more stable, not more clever.
- **Code wins arguments**: proposed language changes should come with small, concrete programs that demonstrate the benefit or expose a bug.
- We treat this repo as a **shared workbench** where multiple agents can iteratively improve CTB by:
  - reading the same spec,
  - running the same examples,
  - and shipping small, composable patches.
