# TrueCouncilOf12 — Changelog

## v4 Hardening (2026-07-03)

Full skill-hardener pipeline pass: recon → gap analysis → rewrite → mechanical gate →
adversarial audit until dry → cross-model verification → repo sweep. Pre-edit snapshot:
`.backup/pre-v4-hardening/`. (The v3 snapshot `.backup/pre-v3-hardening/` referenced
below is no longer present locally; v3's rollback commands are therefore historical.)

### Staleness inventory (Phase 0)

- Model rules one generation stale (Opus 4.7 / Sonnet 4.6 era); the running model (Fable 5) absent from every table — capability check had no row to consult
- guide.html was a pre-v3 relic: "v1.0" badge, "Solomon — The 13th Seat" (contradicting SKILL.md), `council-of-12` paths throughout
- Dead references: `.backup/pre-v3-hardening/` missing, rollback commands unrunnable; no mechanical gate existed
- Frontmatter "do not auto-fire" contradicted the body's auto-trigger section

### Fix registry (v4)

| Area | Fix |
|------|-----|
| Models | FRONTIER / MID / COMPACT capability bands; model names isolated in ONE table (Model → Band Table); unknown-model rule: assume MID, say so, proceed |
| Cross-refs | 17 wrong seat numbers / phase names fixed across bound/stress/elevate (incl. nonexistent "FIRE" and "EXECUTE" phases) |
| Mode A | Phase files no longer define Mode A depth (contradicted the self-contained rule); Seat 7 gains a CHEAPEST TEST line; Mode A template gains LOAD-BEARING FACT / IF FALSE slots |
| Caps | Mode C hard cap ~1,200 words/seat in all 12 seats; degradation thresholds ~8k (B) / ~16k (C) with shown arithmetic for both modes; Paired Exchange caps ~100 words (tokens are unobservable) with truncate-and-move-on |
| Loops | One seat re-run max; one consensus reconsideration max; one re-triage max; rollback gate decidable per run |
| Triage | Null-situation rule (shortcuts included); decline/question branches defined; CREATIVE + MEDICAL domains added; LOW+COMPLEX/SYSTEMIC and a catch-all default → Mode B; shortcuts never bypass the band check |
| Template | Mode C deduplicated (631→417 lines, drift surface removed); missing Paired Exchanges slot added; consensus tiers aligned (Agrees / Mild dissent / Strong dissent + RECONSIDERED slot); CHEAPEST placeholders for Seats 7-9; SYNTHESIS RATIO placeholder; Stakes header field |
| Escalation | Mid-session A→B/C mechanics defined: keep prior seat outputs, run remaining seats deeper, deepen a prior seat only if decision-critical (stated in one line) |
| Fragility | Phase files load from the skill's base directory (no hardcoded install path); template-only-failure rule (proceed via handoff formats); cache-TTL claim softened; NO FINDING exempt from clause (d); Exchange 1 skip rule when LOAD-BEARING FACT is NONE |

### Audit trail (Phase 4 — independent adversarial auditors, quote-verified findings only)

| Round | Scope | Found | Fixed | Prior fixes verified |
|-------|-------|-------|-------|----------------------|
| 1 | Two auditors, disjoint classes (loops/waste/contradictions ∥ undefined/fragility) | 22 unique | 22 | — |
| 2 | Full re-verify + seam hunt | 8 | 8 | 22/22 FIXED |
| 3 | Full re-verify + seam hunt | 3 | 3 | 9/9 FIXED |
| 4 | Final sweep (round budget cap) | 1 | 1 | 3/3 FIXED |

Convergence trend 22 → 8 → 3 → 1. Round 4's single finding was a one-line missing
template placeholder (SYNTHESIS RATIO), applied and grep-verified directly rather than
spending a fifth round the pipeline's own budget forbids.

### Mechanical gate (Phases 3 + 5)

- `test/quiz.txt` — 15 regression questions, one per behavioral rule (including every rule v4 added). Expected answers live in README.md beside the run command. Never embed a copy of the skill in the gate — it pipes the live SKILL.md.
- Cross-model gate RUN 2026-07-03 on two tiers (one COMPACT-band model, one MID-band model — see the Model → Band Table in SKILL.md for the current lineup): **15/15 and 15/15** matches against the README expected answers. Identical rule readings across tiers.
- Note for future automated gates: the literal string "Seat 7 in STRESS" legitimately appears twice in `bound.md` describing the **Adversarial** seat (correct); only Voiceless-context uses of it are defects. A naive zero-hit grep on that bare string is a false failure.

### Post-verification behavioral find (2026-07-03, council self-review)

Running the hardened council ON ITSELF (Mode C) exposed a defect class all four text
audits structurally could not see: **the skill loader performs positional-argument
substitution on `$`-tokens in SKILL.md** — the file's two dollar-zero literals in the
CHEAPEST TEST lines rendered as the first word of the invocation arguments, silently
splicing user text into the standing rules. Fix: both literals replaced with "zero-cost";
a mandatory pre-ship grep tripwire added to README (zero `$`-token lines in SKILL.md).
Phase files are immune (loaded via Read, no substitution). Lesson recorded: static text
verification is not rendering verification — one live invocation is now part of the
evidence bar.

## 2026-05-10 — Renamed to TrueCouncilOf12 + first GitHub publish

- Folder renamed: `council-of-12` → `TrueCouncilOf12` (canonical: `~/.claude/skills/TrueCouncilOf12/`)
- SKILL.md `name:` field updated. Old aliases preserved (`council`, `solomon`, `c12`, `council-of-12`); new aliases added (`true-council`, `tco12`).
- Mode B/C phase-file paths updated `.../council-of-12/...` → `.../TrueCouncilOf12/...`
- Published to GitHub: `https://github.com/ojesusmp/TrueCouncilOf12` (private)
- README.md, LICENSE (MIT), .gitignore added

## v3 Hardening (2026-05-10)

Applies marketing-council v2→v3 disciplines to council-of-12 surgically. Architecture preserved: 12 lenses, 4 phases, 3 modes, Solomon synthesis. Six edits across SKILL.md, ground.md, stress.md, templates/report.md.

Pre-edit snapshot: `.backup/pre-v3-hardening/` (full files).

### Edit IDs and rollback units

| ID | Subject | Files | Failure mode addressed | Rollback unit |
|----|---------|-------|------------------------|---------------|
| E2 | $0 Cheapest-Action across STRESS Seats 7/8/9 + domain examples | stress.md | STRESS seats criticize without recommending response | Per-seat (revert one seat's line, leave others) |
| E3 | Empty-Seat Permission promoted + Solomon ceremonial discount | SKILL.md, templates/report.md | Rule #12 buried; lazy empty findings undetectable | Two-sided (Permission side / Discount side independent) |
| E4 | Collapse to 3 verdict labels: PROCEED / REVISE / STOP | SKILL.md, templates/report.md | Hedging via label proliferation | Single edit (re-add DEFER if needed) |
| E5 | Seat 1 LOAD-BEARING FACT structural tag (Rule #8 SYNC mirror) | SKILL.md (compact), ground.md (full) | Reality drift; fragile fact buried | Single edit, both mirror sides |
| E6 | Solomon synthesis ≥ 30% of total output (operationalizes Rule #11) | SKILL.md | Output asymmetry — pages of seat, paragraph verdict | Tunable threshold (30% → 20% → off) |
| E7 | Mode C only: paired exchanges (Seat 1↔7, Seat 4↔7) + Rule #3 carve-out | SKILL.md | Mode C monologue-without-confrontation | Single edit, Mode-C-local; Mode A/B unaffected |
| E8 | Model IDs updated to Claude 4.x family (Opus 4.7, Sonnet 4.6, Haiku 4.5) + extended thinking note | SKILL.md | Generic model names drift; no extended-thinking guidance | Single edit |

### Rollback order if acceptance scoring fails

1. E7 (Mode C pairing) — highest ceremony risk, Mode-C-local
2. E6 (30% threshold) — tune to 20% or revert to literal Rule #11
3. E3 Solomon-side (discount) — keep Permission side
4. E4 — re-add DEFER as 4th label
5. E2 per-seat — revert failing seat only
6. E5 — last (highest-value structural improvement)
7. E8 — model IDs revert to generic names

### Acceptance criteria

Paired-run design: 12 real situations (3 per domain: Tech/Legal/Personal/Business), 2 are adversarial-baseline (no real load-bearing fact / no real STRESS criticism applies). Each run v1 vs v2 in Mode C. Blind scorer with A/B labels. 5-criteria rubric (0/1/2) + Mode C extra rubric. Pass: v2 beats v1 by ≥1 point avg, Mode C rubric ≥1.5, no regression.

### Pre-edit baseline

Snapshot at `.backup/pre-v3-hardening/` taken before any modification. Restore via `cp .backup/pre-v3-hardening/* .` (root files) and `cp .backup/pre-v3-hardening/report.md templates/`.
