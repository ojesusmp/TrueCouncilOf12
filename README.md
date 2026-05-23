# TrueCouncilOf12

> Universal 12-lens decision analysis with Solomon coordinator. v3-hardened. Formerly named `council-of-12`.

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
- **E8 — Model IDs updated** to Claude 4.x: Opus 4.7 (`claude-opus-4-7`), Sonnet 4.6 (`claude-sonnet-4-6`), Haiku 4.5 (`claude-haiku-4-5-20251001`). Extended-thinking note for Mode C on Opus 4.7.

Full edit registry, rollback order, and pre-edit backup snapshot: see `CHANGELOG.md` and `.backup/pre-v3-hardening/`.

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

| Mode | Recommended model | Why |
|------|------------------|-----|
| A | Haiku 4.5 or Sonnet 4.6 | Compact, fast, deterministic |
| B | Sonnet 4.6 | Standard balance |
| C | Opus 4.7 with extended thinking | Synthesis weight rule + Paired Exchanges benefit from extra reasoning budget |

Prompt cache (5-min TTL) keeps phase files warm across iterations — keep iteration cycles tight.

## Author

Orlando Molina — [TruePointAgents.com](https://truepointagents.com)

## License

MIT. See `LICENSE`.

## History

- **2026-05-10** — Renamed from `council-of-12` to `TrueCouncilOf12`. v3 hardening (E2–E8) applied. Published to GitHub.
- **2026-04-10** — Original `council-of-12` skill authored (replaced earlier `stakeholder-audit`).
