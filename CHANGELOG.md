# TrueCouncilOf12 — Changelog

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
