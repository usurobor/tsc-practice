# C‑Triplebar (CTB) v1.0.5 — Quickstart

**Status:** Informative (non-normative)  
**Source extension:** `.coh`  
**Normative spec:** *CTB v1.0.5 — Language Reference*

CTB is a **small, expression-only, equational** functional language. Everything is an expression; all branching happens through **pattern-matched clauses**. The core data model is a triadic term:

- `_` — **Wholeness** (the literal value *e*)
- `Atom` — any emoji/symbol token (an element of the atom set 𝔄)
- `[L|C|R]` — **tri** constructor (a 3‑position structure)

## 1) The smallest possible CTB program

```text
@Main
t = [✨|_|✨]
```

- Frames start with `@Name`
- Definitions are immutable equations (`name = expr`)
- `[` `|` `]` builds a tri term
- `_` is a **value** (Wholeness), not a wildcard

## 2) Pattern matching (and the two “empties”)

CTB distinguishes:

- `_` (underscore) — **Wholeness literal** (matches *only* Wholeness)
- `•` (bullet) — **Wildcard** (matches anything, binds nothing)

Example: “repair the center only when it is Wholeness”

```text
@Restoring
repair [l|_|r] = [l|✨|r]
repair x = x
```

## 3) Constants vs binders in patterns

In a pattern, an identifier is interpreted as:

- a **Constant** if it’s defined in scope as a nullary term (`T = ...`)
- otherwise a **Binder** (it matches anything and binds it)

```text
@Logic
T = [✅|✅|✅]
F = [🚫|🚫|🚫]

And T T = T
And • • = F
```

No capitalization rules; no explicit “pinning”.

## 4) First-match semantics + overlap safety

Clause selection is **textual first-match**. CTB also bans the dangerous cases where reordering would silently change meaning:

- ✅ allowed: **Specific → General** (“catch-all last”)
- ❌ forbidden: cross-overlap ambiguity
- ❌ forbidden: redundancy (shadowed unreachable clauses)

## 5) PARTIAL vs TOTAL

- **PARTIAL** (default): non-exhaustive functions are allowed, but should warn.
- **TOTAL**: every function must end with a universal catch-all, or the program is rejected.

A universal catch-all is syntactically easy:

```text
f x = ...
```

or

```text
f • = ...
```

(But `f x x = ...` is *not* universal: it imposes an equality constraint.)

## 6) Witness diagnostics (when TOTAL fails)

If a clause group is non-exhaustive, an implementation should try to synthesize a **witness input** that causes `MatchFailure`:

> Error: And violates Totality (arity 2).
> Witness: And T F → MatchFailure.
> Fix: Add a final Universal clause: And • • = <expr>.

The search is bounded and deterministic, so compilers terminate.

## 7) A recommended tiny Prelude

```text
@Prelude
infixr 9 .
infixl 0 |>

(.) f g x = f (g x)
(|>) x f = f x

L [l|c|r] = l
C [l|c|r] = c
R [l|c|r] = r
L x = x
C x = x
R x = x

id x = x

-- reference normalization (simple, explicit)
nf _ = _
nf [ _ | _ | _ ] = _
nf [ l | c | r ] = [ nf l | nf c | nf r ]
nf x = x
```

## Where to go next

- Read the **Language Reference** for full normative rules.
- If you’re implementing: follow the Implementer’s checklist at the end of the Language Reference.
