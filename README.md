# TrueCouncilOf12

> Universal 12-lens decision analysis with Solomon coordinator. v4-hardened. Formerly named `council-of-12`.

## What it does

`TrueCouncilOf12` forces every decision through 12 distinct analytical lenses before a verdict is rendered. Solomon (the coordinator, not a 13th lens) integrates all seat findings, applies three meta-lenses (Behavioral, Strategic, Meaning), and delivers a single-label verdict: `PROCEED`, `REVISE — needs: [X]`, or `STOP`. No "it depends." No hedging.

## The 12 lenses

Organized in 4 phases:

| Phase | Seats | Question |
|-------|-------|----------|
| **GROUND** | 1 Truth · 2 Context · 3 Systems | What is real? |
| **BOUND** | 4 Ethics · 5 Rules · 6 Human | What constrains us? |
| **STRESS** | 7 Adversarial · 8 Risk · 9 Resource | What breaks or costs? |
| **ELEVATE** | 10 Execution · 11 Voiceless · 12 Innovation | What's possible? |

## Three modes

| Mode | Seats | Use when |
|------|-------|----------|
| **A — Essential Five** | 1, 3, 6, 7, 11 (compact) | Quick check, low-medium stakes, time pressure |
| **B — Full Council** | All 12 | Standard analysis, medium-high stakes |
| **C — Full Pipeline** | All 12 + Mode-C-only Paired Exchanges | Critical stakes, systemic complexity |

## v3 Hardening (2026-05-10)

Surgical adoption of marketing-council v2→v3 lessons. Architecture preserved (12 lenses, 4 phases, 3 modes, Solomon). Seven edits:

- **E2 — Cheapest $0/72h action** across STRESS seats 7, 8, 9 (no opinion without a real test)
- **E3 — Empty-Seat Permission** promoted: `NO FINDING — would have flagged if: [X]` is valid output; Solomon discounts ceremonial findings
- **E4 — Three-label verdict**: `PROCEED` / `REVISE — needs: [X]` / `STOP` (no `DEFER`, no hedging)
- **E5 — LOAD-BEARING FACT tag** opens every Seat 1 output (`LOAD-BEARING FACT: [X]. IF FALSE: [consequence].`)
- **E6 — Solomon synthesis ≥ 30%** of total output (operationalizes Rule #11); `SYNTHESIS RATIO: [N]%` reported at end
- **E7 — Mode C Paired Exchanges**: Seat 1 ↔ Seat 7 on load-bearing fact, Seat 4 ↔ Seat 7 on harm/principle (150-token cap per exchange)
- **E8 — Model IDs updated** to Claude 4.x (superseded by v4's band system — see below).

Full edit registry and rollback order: see `CHANGELOG.md`. (The v3 pre-edit snapshot `.backup/pre-v3-hardening/` is no longer present locally; the current snapshot is `.backup/pre-v4-hardening/`.)

## v4 Hardening (2026-07-03)

Full skill-hardener pipeline pass (recon → gap analysis → rewrite → gate → adversarial audit → cross-model verification). Headline fixes:

- **Capability bands replace hardcoded model rules.** All mode-capability rules now reference FRONTIER / MID / COMPACT bands; model names live in exactly ONE spot (the Model → Band Table in `SKILL.md`) with an explicit unknown-model fallback (assume MID, say so, proceed). The skill no longer breaks when the model lineup changes.
- **16 wrong cross-seat references fixed** in `bound.md`, `stress.md`, `elevate.md` (stale seat numbers and two phase names — "FIRE", "EXECUTE" — from a pre-council numbering).
- **Mode A contradictions removed from phase files** (they defined Mode A depth for seats that never run in Mode A, and one contradicted SKILL.md's all-4-questions rule). Phase files now defer to SKILL.md for Mode A entirely.
- **Mode B finding counts aligned** to 3-5 everywhere; **Mode C output hard-capped** (~1,200 words/seat) — no more "no fixed length".
- **Loop caps added**: one seat re-run max after a STRESS failure; one consensus reconsideration max; one re-triage max on "adjust" (now defined).
- **Activation contradiction resolved**: the skill never auto-fires; trigger phrases are recognition vocabulary for explicit asks only.
- **Synthesis ratio now measurable**: word count, not token count.
- **`templates/report.md` deduplicated** (Mode C no longer carries a full copy of Mode B — 631→417 lines) and the previously missing **Paired Exchanges slot added** to the Mode C template.
- **Mechanical gate added**: `test/quiz.txt` (see Testing below).

## Testing (the mechanical gate)

Pipe the LIVE skill text plus the quiz to a cheap model (never embed a copy of the skill — copies drift):

```bash
# bash
cat SKILL.md test/quiz.txt | claude -p --model haiku
```
```powershell
# PowerShell
Get-Content SKILL.md, test\quiz.txt | claude -p --model haiku
```

**Pre-ship tripwire (mandatory before committing any SKILL.md edit):**

```bash
grep -nE '\$[0-9A-Za-z{]' SKILL.md   # MUST return zero lines
```

The skill loader substitutes positional arguments into `$`-tokens in SKILL.md at load
time — a literal like a dollar amount silently becomes whatever the user typed as
arguments, corrupting the rule text per invocation. Discovered live 2026-07-03 when the
council analyzed itself. Phase files are immune (loaded via the Read tool, no
substitution); only SKILL.md needs the check.

Expected answers (any drift means an edit broke a rule):

1. No — Mode A is self-contained; never Read phase files.
2. Seats 1, 3, 6, 7, 11.
3. PROCEED / REVISE — needs: [X] / STOP.
4. REVISE (cannot return PROCEED).
5. Assume MID band, state the assumption in one triage line, and proceed.
6. Mode A only.
7. Seat 11, ELEVATE phase.
8. `NO FINDING — would have flagged if: [X]`.
9. "We sacrifice X to protect Y because Z."
10. At least 30% of total Council output by word count AND longer than any individual seat.
11. Mode C only; Seat 1↔7 and Seat 4↔7; ~100 words (≈150 tokens) per exchange.
12. Re-run triage Steps 1-4 once with corrected inputs and re-present; ONE re-triage maximum.
13. Mode B (URGENT downgrades one mode).
14. Reconsider the verdict; at most ONE reconsideration; the revised verdict is final.
15. No — never convene unasked; at most a one-sentence mention that the Council is available.

## Installation

Clone into your Claude Code skills directory:

```bash
git clone https://github.com/ojesusmp/TrueCouncilOf12.git ~/.claude/skills/TrueCouncilOf12
```

Or download the latest release and extract.

After install, restart Claude Code (or start a new chat). The skill auto-discovers via SKILL.md frontmatter.

## Usage

Invoke explicitly:

```
/TrueCouncilOf12 should I sign this contract this week?
```

Or via legacy aliases (preserved for backward compatibility):

- `council`
- `solomon`
- `c12`
- `council-of-12`
- `true-council`
- `tco12`

Auto-trigger phrases (Solomon may recommend convening on its own):

- "run the council", "convene the council", "what do the 12 say"
- "pressure-test this", "find the blind spots"
- "before I send this", "before I ship this"
- (legacy stakeholder-audit triggers also supported)

## Output contract

```
SEAT 1 — TRUTH / EVIDENCE
LOAD-BEARING FACT: [the single fact this analysis rests on]
IF FALSE: [what becomes invalid downstream]
... findings ...

... seats 2 through 12 ...

(Mode C only)
PAIRED EXCHANGE 1: Seat 1 ↔ Seat 7
PAIRED EXCHANGE 2: Seat 4 ↔ Seat 7

SOLOMON'S VERDICT
Convergence: ...
Tension: ...
Verdict: PROCEED | REVISE — needs: [X] | STOP — one clear, actionable sentence
Tradeoff: We sacrifice [X] to protect [Y] because [Z]
Confidence: HIGH | MEDIUM | LOW
SYNTHESIS RATIO: [N]%
```

## Companion skills

- **`forge-council`** — sister creation/ideation skill ("Council decides, Forge creates")
- **`TrueBusinessBuilder`** — downstream pipeline that uses `TrueCouncilOf12` for Stage 2 validation, mapping verdicts to `GO / PIVOT / NO-GO`
- **`marketing-council`** — source of the v2→v3 disciplines ported here

## Best practices for runtime model selection

| Mode | Recommended band | Why |
|------|------------------|-----|
| A | COMPACT or MID | Compact, fast, deterministic |
| B | MID | Standard balance |
| C | FRONTIER with extended thinking | Synthesis weight rule + Paired Exchanges benefit from extra reasoning budget |

Model names map to bands in exactly ONE place: the **Model → Band Table** in `SKILL.md`. When the lineup changes, update that table and nothing else. Provider prompt cache (short TTL, typically minutes) keeps phase files warm across iterations — keep iteration cycles tight.

## Author

Orlando Molina — [TruePointAgents.com](https://truepointagents.com)

## License

MIT. See `LICENSE`.

## History

- **2026-07-03** — v4 hardening: capability bands + single model table, 16 cross-seat reference fixes, Mode A/B/C contradiction cleanup, loop caps, template dedup + Paired Exchanges slot, mechanical gate (`test/quiz.txt`), guide.html refreshed.
- **2026-05-10** — Renamed from `council-of-12` to `TrueCouncilOf12`. v3 hardening (E2–E8) applied. Published to GitHub.
- **2026-04-10** — Original `council-of-12` skill authored (replaced earlier `stakeholder-audit`).
