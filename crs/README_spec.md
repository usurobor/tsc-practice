# Coherent README Spec (CRS) v1.0.0

> Changelog: v1.0.0 — initial self-CLP’d spec for what a coherent README should look like in tsc-practice-style projects.

## 1. Purpose

CRS defines what a **coherent top-level README** must contain for TSC‑aligned practice repos (like `tsc-practice`, and future siblings).

It is a **self-process** spec: used by a single author to design or review a README *before* it becomes the public entry point of a project.

## 2. Target

This spec applies to repos that:

- live in the TSC / C≡ / CTB ecosystem,
- are primarily about **practice/protocols**, not code,
- have (or will have) multiple sub-specs under them (like `clp`, `emoji-contracts`, etc.).

## 3. Required Sections

A README satisfying CRS MUST contain, in this order (names can vary slightly, but content MUST be present):

### 3.1 Purpose ("What is this repo for?")

- One short paragraph that:
  - says **what kind of thing** this repo holds (code, specs, practices, contracts, etc.), and
  - distinguishes it from neighboring repos (e.g., `tsc` = math/implementation, this = practice/protocol).

### 3.2 Audience / Scope ("Who is this for?")

- A short bullet list that makes explicit:
  - **Primary audience** (e.g., single agent, team, human+agent pair).
  - **Non-goals / out-of-scope** (e.g., org governance, multi-agent CLP) so readers don’t overgeneralize.

### 3.3 Contents Map ("What lives here?")

- A concise list of major sub-areas (subdirectories/specs), each with:
  - name of the spec or area,
  - one-line description of what it does,
  - pointers to its canonical spec file(s) (e.g., `clp/CLP.md`) and changelog if present.

### 3.4 Usage Pattern ("How do I start?")

- A short ordered list of steps that tells a new user:
  - where to begin (e.g., "read CLP"),
  - how to apply the repo’s practices to their own work (e.g., "run self‑CLP on your drafts"),
  - any tagging/versioning expectations (e.g., git tags, CHANGELOGs).

### 3.5 Closing Tagline

- A short, consistent sign-off line (e.g., `May Coherence be with you 🌀`) signaling that the README itself has been brought under the same discipline as the rest of the repo.

## 4. Coherence Checks (self-CLP prompts)

When designing or reviewing a README under CRS, run these self-CLP questions:

- **PATTERN (🧩):**
  - Does the README cleanly state what this repo is for and how it differs from neighbors?
  - Are section names and content aligned, or is there hidden behavior (e.g., scope creep)?

- **RELATION (🤝):**
  - Is the audience explicitly named, or is it pretending to speak to “everyone”?
  - Does it set honest expectations about what the repo will and won’t do for the reader?

- **EXIT (🚪):**
  - Does the README show readers how to leave or defer (e.g., “if you need org-wide governance, see other specs”)?
  - Does it avoid trapping them in an over-broad promise (e.g., claiming to solve all of alignment)?

A README that fails these checks should be revised (using CLP) before being treated as canonical.

## 5. Emoji Contract for CRS

For the README itself, CRS implies:

- PATTERN: 🧩 — README states repo purpose and contents without contradiction.
- RELATION: 🤝 — README is honest about who it serves and what it won’t cover.
- EXIT: 🚪 — README points to where to go next *and* what is out of scope.

UDHR-style shorthand:

- 📘✅🧩🤝🚪 — A project has the right (and duty) to present a README with clear Purpose, Audience, Map, and Usage.
- 📘🚫🎭 — A README should not perform as something it is not (e.g., pretending to be full spec or code when it’s practice-only).

## 6. TSC Coherence (self-assessment)

- **s_α (PATTERN):** A — required sections make the intended shape explicit.
- **s_β (RELATION):** A− — audience and non-goals are named; multi-repo relationships could be formalized further later.
- **s_γ (EXIT):** A− — usage + out-of-scope guidance present; could be extended with more explicit cross-links.

Aggregate **C_Σ(CRS v1.0.0): A** — high coherence for single-repo README design; future MINOR versions can add patterns for multi-repo suites or org-level documentation.

May Coherence be with you 🌀
