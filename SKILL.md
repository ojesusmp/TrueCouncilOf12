---
name: TrueCouncilOf12
description: "Universal 12-lens analysis with Solomon coordinator. Invoke only when the user asks for the council ('council of 12', 'TrueCouncilOf12', 'c12', 'solomon'); do not auto-fire."
aliases: [council, solomon, c12, council-of-12, true-council, tco12]
author: "Orlando Molina - TruePointAgents.com"
argument-hint: "<situation, deliverable, decision, or problem to analyze>"
level: 3
---

# Council of 12 and the Solomon Seat

## Purpose

The Council of 12 is a universal analysis framework that forces every situation through
12 distinct lenses before any decision is made. It is built on a Japanese engineering
philosophy: design for the worst case first, then let the structure hold under any force.
Most failures — in code, in organizations, in life — come from a missing perspective,
not a missing solution. The Council guarantees that no critical angle is left unexamined.

Solomon sits above the 12 seats. He is not a thirteenth perspective — he is the
integrator, the judge, the one who hears all voices and then *decides*. Solomon applies
three meta-lenses (Behavioral, Strategic, Meaning) that no individual seat carries,
synthesizes convergence and tension across seats, and delivers a verdict with a named
tradeoff. Solomon never says "it depends." Solomon decides.

---

## Quick Reference Card

| # | Seat | Core Question | Kills | Phase |
|---|------|---------------|-------|-------|
| 1 | Truth / Evidence | "What do we actually know?" | Confusion | GROUND |
| 2 | Context / Pattern | "What led here? What does the pattern say?" | Shallow judgment | GROUND |
| 3 | Systems / Root Cause | "What is the real mechanism at work?" | Repetition | GROUND |
| 4 | Ethics / Conscience | "Is this right?" | Clever evil | BOUND |
| 5 | Rules / Constraints | "What are the hard boundaries?" | Avoidable damage | BOUND |
| 6 | Human / Emotional | "How will people actually feel and behave?" | Blind spots about people | BOUND |
| 7 | Adversarial / Attack | "How would someone break this on purpose?" | Naivete | STRESS |
| 8 | Risk / Fragility | "What goes wrong by accident?" | Preventable catastrophe | STRESS |
| 9 | Resource / Tradeoff | "What does this cost, including what we give up?" | Hidden costs | STRESS |
| 10 | Execution / Feasibility | "Can we actually do this?" | Fantasy plans | ELEVATE |
| 11 | Voiceless / Absent | "Who is affected but has no voice?" | Invisible harm | ELEVATE |
| 12 | Innovation / Possibility | "What better option are we not seeing?" | Missed breakthroughs | ELEVATE |
| S | **Solomon** | *Weighs all seats, applies meta-lenses, delivers verdict with named tradeoff* | Indecision | — |

**The 4 Phases:**
- **GROUND** (Seats 1-3): Establish reality. What is true, what is the pattern, what is the mechanism.
- **BOUND** (Seats 4-6): Establish constraints. What is right, what is allowed, what is human.
- **STRESS** (Seats 7-9): Pressure-test. What breaks intentionally, accidentally, and at what cost.
- **ELEVATE** (Seats 10-12): Expand options. What is feasible, who is missing, what is possible.

---

## Activation Conditions

**This skill never auto-fires.** The frontmatter governs: the Council convenes only when the user explicitly asks for it. The phrase lists below are recognition vocabulary for what counts as an explicit ask — they are not permission to self-activate.

### Explicit Triggers
These phrases, when the user directs them at Claude as a request, activate the Council:
- "council", "council of 12", "12 seats", "solomon"
- "run the council", "convene the council"
- "what do the 12 say", "all seats"
- "essential five", "quick council"

### Inherited Triggers (from stakeholder-audit)
These legacy phrases also count as explicit asks when the user directs them at the current work:
- "run the audit", "stakeholder review", "POV check"
- "multi-perspective", "reconcile this"
- "best move right now", "strategist lens"
- "what else can this do", "pressure-test this"
- "find the blind spots"
- "before I send this", "before I ship this"

### Escalation Suggestions (inside an already-convened session only)
Once the Council is already running, Solomon may recommend a deeper mode when detecting:
- **High-stakes deliverables**: Legal filings, financial decisions, public-facing communications,
  documents being handed off to others who will act on them
- **Accountability situations**: Anything the user will be held accountable for, where a missed
  perspective could cause real damage
- **Complex tradeoffs**: Situations where multiple valid paths conflict and the user needs
  structured reasoning to choose
- **Irreversible decisions**: Actions that cannot be easily undone once taken

Solomon presents the escalation recommendation and waits for user confirmation before
switching modes. Never escalate without consent. Outside a council session, Claude may at
most mention in one sentence that the Council is available for a high-stakes deliverable —
never convene it unasked.

**Mechanics of a confirmed mid-session escalation** (e.g., A→B): keep the seat outputs
already produced — never re-pay for them. Load the phase files, run the not-yet-run seats
at the deeper depth, deepen an already-run seat only if Solomon judges its compact
finding decision-critical (it names the load-bearing fact, the primary risk, or the
dominant tension — Solomon states which, in one line), then Solomon synthesizes over the
combined set.

---

## Solomon Triage Protocol

Solomon reads every situation BEFORE any seat speaks. This is the intake process.

**Null-situation rule:** if the invocation carries no situation and none is inferable from
the conversation, ask one question — "What should the Council analyze?" — and stop.
Triage cannot run on a null situation.

### Step 1: Situation Assessment

Solomon evaluates four dimensions:

**Stakes:**
- `LOW` — Reversible, limited impact, affects only the immediate actor
- `MEDIUM` — Affects multiple people or has moderate consequences
- `HIGH` — Significant consequences, difficult to reverse, affects many
- `CRITICAL` — Irreversible, life-altering, legal/financial/safety implications

**Complexity:**
- `SIMPLE` — One clear issue, few variables, obvious stakeholders
- `MODERATE` — Multiple interacting issues, several stakeholders
- `COMPLEX` — Many variables, unclear causation, systemic factors
- `SYSTEMIC` — Deeply interconnected, spans multiple domains, emergent behavior

**Time Pressure:**
- `URGENT` — Decision needed now, delay itself causes harm
- `NORMAL` — Reasonable timeline, no penalty for deliberation
- `DELIBERATE` — High-stakes enough to warrant extended analysis

**Domain:**
- `TECH` — Software, systems, architecture, infrastructure
- `LEGAL` — Law, compliance, regulation, contracts
- `PERSONAL` — Relationships, career, health, life decisions
- `BUSINESS` — Strategy, operations, finance, management
- `CREATIVE` — Writing, design, product, art
- `MEDICAL` — Health decisions, treatment, care
- `MIXED` — Spans multiple domains

### Step 2: Mode Selection

Based on the assessment, Solomon recommends one of three modes:

| Mode | Name | Seats | Depth | When |
|------|------|-------|-------|------|
| **A** | Essential Five | 5 seats (1,3,6,7,11) | 1-2 findings each | Quick check, low-medium stakes, time pressure |
| **B** | Full Council | 12 seats | 3-5 findings each | Standard analysis, medium-high stakes |
| **C** | Full Pipeline | 12 seats + extended | Exhaustive | Critical stakes, systemic complexity, deliberate timeline |

**Selection logic:**
- Stakes LOW + Complexity SIMPLE → Mode A
- Stakes LOW + Complexity MODERATE → Mode A
- Stakes LOW + Complexity COMPLEX/SYSTEMIC → Mode B
- Stakes MEDIUM + any complexity → Mode B
- Stakes HIGH + Complexity SIMPLE/MODERATE → Mode B
- Stakes HIGH + Complexity COMPLEX/SYSTEMIC → Mode C
- Stakes CRITICAL + any complexity → Mode C
- Time Pressure URGENT → downgrade one mode (C→B, B→A)
- Time Pressure DELIBERATE → upgrade one mode if stakes warrant (A→B, B→C)
- Any Stakes × Complexity combination not listed above → Mode B (the default)

### Step 3: Shortcut Detection

Certain phrases bypass triage and go directly to a mode:
- "essential five" or "quick council" → **Mode A** (no triage needed)
- "all seats" or "full council" → **Mode B** (no triage needed)
- "full pipeline" or "deep analysis" → **Mode C** (no triage needed)

Shortcuts bypass Steps 1-2 and the confirmation — **never Step 4**: the band capability
check always runs, and a user-named mode that exceeds the running model's band downgrades
per Conflict Resolution (tell the user). Before executing, make a silent one-line Step 1
assessment so the report's Stakes field is real, not blank. The **null-situation rule
outranks shortcuts**: with no situation to analyze, ask the one question and stop,
whatever mode was named.

### Step 4: Model Capability Check

Solomon checks the current model against mode requirements (see Model Compatibility
section below). If the recommended mode exceeds model capability, Solomon downgrades
with an explanation.

### Step 5: Present Recommendation

Solomon presents to the user:

```
SOLOMON TRIAGE
Situation: [one-line summary]
Stakes: [level] | Complexity: [level] | Time: [level] | Domain: [type]
Recommended Mode: [A/B/C] — [reason]
[If downgraded: "Note: Mode [X] recommended but current model supports up to Mode [Y]."]

Proceed? (yes / change mode / adjust)
```

Wait for user confirmation before executing. The responses mean:

- **yes** → execute the recommended mode.
- **change mode** → execute the mode the user names (band capability check still applies).
- **adjust** → the user corrects stakes/complexity/time/domain; re-run Steps 1-4 once with
  the corrected inputs and present again. ONE re-triage maximum — after that, execute
  whichever mode the user picks (default: the latest recommendation).
- **decline** ("no", "cancel", "not now", or any refusal) → stand down; do not run the
  Council and do not re-ask.
- **a question** → answer it, then re-present the same recommendation (this does not
  consume the re-triage).

**Explicit-proceed exception:** if the user's invocation already named a mode (Step 3
shortcuts) or explicitly told the Council to proceed without asking, skip the confirmation
and execute directly.

---

## Essential Five: Compact Definitions

These 5 seats are the minimum viable council. They cover the most critical analytical
gaps that cause real-world failures: not knowing the facts, not seeing the system,
not accounting for human behavior, not anticipating attack, and not hearing the voiceless.

Mode A executes ONLY from these definitions. No file loading. No Read tool calls.
Everything needed for Mode A is contained in this section.

---

### Seat 1: Truth / Evidence
<!-- SYNC: must match ground.md Seat 1 core question + standard questions -->

**Phase:** GROUND
**Focus:** What is objectively true — separated from interpretation, emotion, assumption, and narrative.
**Core Question:** "What do we actually know?"

**Standard Questions:**
1. What happened? (Observable facts only — strip adjectives, strip emotion, strip framing)
2. What do we know vs. what do we assume? (Draw a hard line between verified and unverified)
3. What is assumption, rumor, emotion, or interpretation being treated as fact?
4. What evidence exists? (Documents, data, direct observation, corroborated testimony)

**How to analyze:**
Examine the situation and extract only what can be verified. Separate hard evidence from
soft signals. Identify the single most important fact that changes the analysis if wrong.
Flag any "known unknowns" — things we know we do not know.

**Output (Mode A):** Seat 1 output MUST begin with two tagged lines, in this order:

```
LOAD-BEARING FACT: [the single fact this entire analysis rests on].
IF FALSE: [what becomes invalid downstream if this fact is wrong].
```

Then proceed with 1-2 key findings in natural language. Lead with the strongest fact and the most dangerous assumption.

If no single load-bearing fact can be named, emit: `LOAD-BEARING FACT: NONE — analysis is opinion-only`. When this is emitted, Solomon caps the verdict at REVISE (cannot return PROCEED).

**Tagline:** *This seat kills confusion.*

---

### Seat 3: Systems / Root Cause
<!-- SYNC: must match ground.md Seat 3 core question + standard questions -->

**Phase:** GROUND
**Focus:** Structure, process, and hidden drivers — the mechanism beneath the surface event.
**Core Question:** "What is the real mechanism at work?"

**Standard Questions:**
1. Is this a symptom or the real problem? (Trace backward from the visible issue)
2. What mechanism keeps recreating this? (Feedback loops, incentive structures, structural flaws)
3. What incentives are causing this behavior? (Follow the rewards — money, status, safety, convenience)
4. What would fix the system instead of patching the event? (Structural intervention vs. band-aid)

**How to analyze:**
Look past the presenting problem to the structure that produces it. Ask "why" at least
three times. Identify feedback loops — where does the output of the system become its own
input? Find the incentive misalignment: what does the system reward that it should not?
What does it punish that it should not?

**Output (Mode A):** 1-2 key findings in natural language. Name the mechanism and the
incentive that feeds it.

**Tagline:** *This seat stops repetition.*

---

### Seat 6: Human / Emotional
<!-- SYNC: must match bound.md Seat 6 core question + standard questions -->

**Phase:** BOUND
**Focus:** How people will feel, react, and behave — not how they *should* behave, but how they *will*.
**Core Question:** "How will people actually feel and behave?"

**Standard Questions:**
1. Who is scared, angry, proud, ashamed, loyal, threatened, or confused? (Map the emotional landscape)
2. What will trigger defensiveness? (Identity threats, status loss, public embarrassment, feeling unheard)
3. What will build trust? (Consistency, transparency, acknowledgment, shared risk)
4. What will people actually do, not what they say they will do? (Predict real behavior, not stated intentions)

**How to analyze:**
Assume people are emotional first, rational second. Identify who has the most to lose
emotionally (not just materially). Predict defensive reactions before they happen. Look
for the gap between what people say and what they do — that gap is where the real
information lives. Consider group dynamics: how does the presence of others change
individual behavior?

**Output (Mode A):** 1-2 key findings in natural language. Name the dominant emotion
and the most likely behavioral response.

**Tagline:** *This seat sees human reality.*

---

### Seat 7: Adversarial / Attack
<!-- SYNC: must match stress.md Seat 7 core question + standard questions -->

**Phase:** STRESS
**Focus:** Intentional exploitation and weaponization — how someone with bad intent would use this situation.
**Core Question:** "How would someone break this on purpose?"

**Standard Questions:**
1. What is the single weakest point an adversary would attack first? (Find the soft underbelly)
2. Can any element be taken out of context and used against the creator? (Screenshot test, headline test)
3. What assumption could an adversary challenge or disprove? (Find the load-bearing assumption)
4. What would an adversary say to discredit this? (Construct the attack narrative)

**How to analyze:**
Adopt the mindset of someone who wants this to fail. Not a devil's advocate playing a
game — a real adversary with real motivation. What is the cheapest, easiest attack?
What is the most devastating? Consider multiple adversary types: competitors, critics,
bad-faith actors, trolls, litigators. Test every public-facing element against the
"worst headline" test: what is the worst true headline someone could write about this?

**Output (Mode A):** 1-2 key findings in natural language. Name the weakest point and
the most likely attack vector, and close with one line — `CHEAPEST TEST: [zero-cost, ≤72h
action that would falsify the attack if it is not real]`. (This satisfies the STRESS tag
requirement in Synthesis Step 2's discount scan. Wording note: never write dollar-sign
tokens like "dollar-zero" as literals in this file — the skill loader substitutes
positional arguments into $-tokens at load time and silently corrupts the rule text.)

**Tagline:** *This seat assumes enemies exist.*

---

### Seat 11: Voiceless / Absent
<!-- SYNC: must match elevate.md Seat 11 core question + standard questions -->

**Phase:** ELEVATE
**Focus:** Who is affected but has no representation — the people not in the room, not at the table, not considered.
**Core Question:** "Who is affected but has no voice?"

**Standard Questions:**
1. Who will be impacted by this decision but is not at the table? (Downstream users, dependents, communities)
2. Whose perspective are we assuming instead of asking? (Projection vs. actual consultation)
3. What downstream effects hit people we have not considered? (Second and third-order consequences)
4. Who inherits the consequences of this choice? (Future people, junior staff, end users, the public)

**How to analyze:**
Systematically expand the circle of impact beyond the obvious stakeholders. Consider
temporal voicelessness (future people who inherit this decision), power voicelessness
(people who are affected but lack standing to object), and structural voicelessness
(people the system was not designed to hear). For each voiceless group, ask: if they
were in the room, what would they say? What would they ask for?

**Output (Mode A):** 1-2 key findings in natural language. Name who is missing and
what they would say if present.

**Tagline:** *This seat speaks for the silent.*

---

## Mode A: Execution Flow

**IMPORTANT: Mode A is fully self-contained. DO NOT use the Read tool to load phase
files or templates. Execute ONLY the 5 seats defined above using the compact definitions
in this file.**

### Execution Order

1. **Truth / Evidence** (Seat 1) — Establish what is real
2. **Systems / Root Cause** (Seat 3) — Find the mechanism
3. **Human / Emotional** (Seat 6) — Account for people
4. **Adversarial / Attack** (Seat 7) — Anticipate exploitation
5. **Voiceless / Absent** (Seat 11) — Hear the unheard

### Per-Seat Process

For each seat:
1. State the seat name and core question
2. Apply the standard questions to the specific situation
3. Analyze using the "How to analyze" guidance
4. Produce 1-2 key findings in natural language (concise, concrete, actionable)
5. **EMPTY-SEAT PERMISSION:** If after applying the standard questions you find nothing meaningful for this specific situation, return: `NO FINDING — would have flagged if: [X]`. The would-have-flagged clause is mandatory. A `NO FINDING` missing this clause is treated as ceremonial and discounted by Solomon (see Synthesis Protocol Step 2). Filling space with manufactured findings is the failure, not emptiness. (This operationalizes Rule #12.)

### After All 5 Seats: Solomon Rapid Synthesis

After all 5 seats have spoken, Solomon performs a compressed synthesis:
- Read all 5 outputs
- Identify convergence (where do multiple seats agree?)
- Identify the sharpest tension (where do seats conflict?)
- Apply the three meta-lenses briefly (one sentence each)
- Deliver verdict with named tradeoff

### Mode A Report Template

Use this exact format for Mode A output:

```
COUNCIL OF 12 — ESSENTIAL FIVE
Situation: [one-line summary of what is being analyzed]
Mode: A (Essential Five) | Stakes: [level] | [date]

--- GROUND ---

SEAT 1 — TRUTH / EVIDENCE
"What do we actually know?"
LOAD-BEARING FACT: [the single fact this analysis rests on, or NONE — analysis is opinion-only]
IF FALSE: [what becomes invalid downstream]
[1-2 sentences: the strongest verified fact and the most dangerous assumption]

--- GROUND ---

SEAT 3 — SYSTEMS / ROOT CAUSE
"What is the real mechanism at work?"
[1-2 sentences: the underlying mechanism and the incentive feeding it]

--- BOUND ---

SEAT 6 — HUMAN / EMOTIONAL
"How will people actually feel and behave?"
[1-2 sentences: the dominant emotion and the most likely behavioral response]

--- STRESS ---

SEAT 7 — ADVERSARIAL / ATTACK
"How would someone break this on purpose?"
[1-2 sentences: the weakest point and the most likely attack vector]
CHEAPEST TEST: [zero-cost, ≤72h action that would falsify the attack — omit this line if the seat returned NO FINDING]

--- ELEVATE ---

SEAT 11 — VOICELESS / ABSENT
"Who is affected but has no voice?"
[1-2 sentences: who is missing and what they would say]

=========================================
SOLOMON'S VERDICT
=========================================

Convergence: [where multiple seats agree]
Tension: [where seats conflict and why]

Behavioral lens: [one sentence — hidden human dynamics]
Strategic lens: [one sentence — power and leverage]
Meaning lens: [one sentence — who are we becoming]

Verdict: [PROCEED | REVISE — needs: <specific missing input> | STOP] — one clear, actionable sentence.
  PROCEED: Do the thing. Reasoning supports action.
  REVISE — needs: [X]: Do the thing AFTER named fixes/info. Name what to add or change.
  STOP: Do not do the thing. Name what would have to change for this to flip to PROCEED.
  (No DEFER, no "it depends," no "consider both options." Insufficient input routes to REVISE with a named gap.)
Tradeoff: We sacrifice [X] to protect [Y] because [Z].
Confidence: [HIGH/MEDIUM/LOW based on seat alignment]
```

---

## Solomon Synthesis Protocol

This is the heart of the Council. Solomon's synthesis is not a summary — it is a
judicial process. Solomon hears all evidence, identifies what matters most, applies
lenses no individual seat carries, and renders a verdict that the user can act on.

### Step 1: Collect All Seat Outputs

Gather findings from all active seats:
- Mode A: 5 seats, 1-2 findings each (10 data points maximum)
- Mode B: 12 seats, 3-5 findings each (60 data points maximum)
- Mode C: 12 seats, exhaustive findings (capped ~1,200 words per seat, prioritized by impact)

Do not filter or pre-judge at this stage. Every finding enters the record.

### Step 2: Pattern Recognition — Find Convergence

**Ceremonial Finding Discount (run BEFORE convergence scoring):**

Before counting convergence, Solomon scans each seat's output and tags any of:
- (a) `NO FINDING` missing its `would have flagged if: [X]` clause
- (b) findings that restate the situation without naming a specific risk, fact, or action
- (c) findings concluding only with "consider X" or "be mindful of X" without a testable claim
- (d) STRESS-phase findings (Seats 7, 8, 9 — in the modes where each runs; in Mode A only Seat 7 applies) missing their CHEAPEST [action] line — a well-formed `NO FINDING — would have flagged if: [X]` is exempt (nothing to test)

Tagged findings are excluded from convergence scoring and synthesis weight. This prevents manufactured-to-fill-space findings from inflating the convergence score and giving false confidence in the verdict.

Then proceed to convergence scoring on the surviving findings.

Scan all seat outputs for convergence: places where multiple independent lenses
identify the same issue, risk, opportunity, or dynamic.

**Convergence scoring:**
- 2 seats agree → Signal worth noting
- 3 seats agree → High-signal finding (flag explicitly)
- 4+ seats agree → Near-certain finding (this is almost certainly real)
- 5+ seats agree → Treat as ground truth for the analysis

**What convergence looks like:**
- Truth says "the data shows declining engagement" AND Systems says "the feedback loop
  punishes the behavior we want" AND Human says "people feel unheard" → These three
  are seeing the same elephant from different angles. Name it.
- Adversarial says "competitors will exploit the delay" AND Risk says "the timeline
  is the fragile element" AND Resource says "we cannot afford the time cost" → Timeline
  is the critical variable. Three seats confirm it.

**How to report convergence:**
Name the converging finding explicitly. State which seats see it and from what angle.
Assign it proportional weight in the verdict.

### Step 3: Tension Mapping — Find Conflict

Identify where seats disagree or pull in opposite directions. Tensions are not failures
of the analysis — they are the most important part. Every real decision involves
tradeoffs, and tensions reveal exactly where the tradeoffs live.

**Common tension patterns:**

*Ethics vs. Adversarial:*
Ethics says "be transparent" but Adversarial says "transparency creates attack surface."
Resolution requires asking: transparent with whom? About what? Full transparency is
rarely the answer; strategic transparency often is.

*Human vs. Systems:*
Human says "people need empathy and time" but Systems says "the structure rewards speed
over care." Resolution requires changing the system or accepting that human needs will
be systematically overridden.

*Innovation vs. Risk:*
Innovation says "this breakthrough changes everything" but Risk says "the downside is
catastrophic." Resolution requires asking: can we capture the upside while containing
the downside? If not, which matters more?

*Execution vs. Ethics:*
Execution says "this is the only feasible path" but Ethics says "this path causes harm."
Resolution is never "do the harmful thing because it is easy." Find another path or
accept the cost of doing right.

*Resource vs. Voiceless:*
Resource says "we cannot afford to include everyone" but Voiceless says "excluding them
causes harm." Resolution requires honest accounting: what is the real cost of inclusion
vs. the real cost of exclusion?

**How to report tensions:**
Name both sides. Do not resolve tensions prematurely. Present them to Solomon for
the verdict phase. Every named tension MUST be addressed in the verdict — you cannot
ignore a tension once identified.

### Step 4: Meta-Lens Application

Solomon carries three meta-lenses that no individual seat possesses. These lenses
operate at a level above the seats — they see patterns the seats cannot see because
they span the entire analysis.

---

#### Behavioral Meta-Lens

This lens sees the hidden human dynamics that drive outcomes. It draws from behavioral
psychology, cognitive science, and the understanding that humans are predictably
irrational.

**Questions Solomon asks through this lens:**

1. **Why are people really acting this way?**
   Strip away the stated reasons. What is the actual driver? Fear of loss is stronger
   than hope of gain. Status threat triggers stronger reactions than material threat.
   People protect their identity before their interests.

2. **What hidden motivations are at work?**
   - Ego: Who needs to be right? Who cannot afford to be wrong?
   - Fear: Who is afraid, and of what specifically? (Loss, exposure, irrelevance, failure)
   - Tribalism: Who is protecting their group at the expense of truth?
   - Self-preservation: Who is optimizing for personal survival over collective good?

3. **What would a behavioral psychologist see that the seats missed?**
   - Anchoring: Is the first piece of information disproportionately shaping the analysis?
   - Sunk cost: Is anyone clinging to a path because of past investment?
   - Availability bias: Are recent or vivid events being overweighted?
   - Status quo bias: Is inaction being favored simply because it is the default?
   - Groupthink: Is consensus masking suppressed dissent?

4. **What patterns of human irrationality are relevant?**
   - People overweight vivid risks and underweight statistical risks
   - People discount future consequences in favor of present comfort
   - People confuse confidence with competence
   - People resist change even when the current state is harmful

---

#### Strategic Meta-Lens

This lens sees power, leverage, positioning, and the game being played beneath the
surface. It draws from game theory, strategic thinking, and the understanding that
every situation has a power structure whether visible or not.

**Questions Solomon asks through this lens:**

1. **Who benefits from the current situation?**
   Someone always benefits from the status quo, even a bad status quo. Identify who
   gains from things staying the same. They will resist change — not openly, but
   through delay, complexity, and redirection.

2. **Who loses?**
   Identify who bears the cost. Are the people bearing the cost the same people making
   the decision? If not, expect the decision to underweight their pain.

3. **Where is the leverage?**
   What single change would shift the most? Leverage points are rarely where they
   appear. The loudest problem is usually not the most important one. Find the quiet
   variable that, if changed, cascades through the entire system.

4. **What move changes the board entirely?**
   Beyond incremental improvements, is there a move that reframes the situation? Changes
   the rules? Introduces a new player? Removes a constraint? The best strategic move
   is often not the best answer to the current question — it is a better question.

5. **What would a strategist exploit or protect?**
   Looking at this situation from a pure power perspective: what is the strategic asset?
   What is the strategic vulnerability? If you were advising the opposition, where
   would you strike?

---

#### Meaning Meta-Lens

This lens sees identity, legacy, and purpose. It asks the questions that matter in
5 years, not 5 days. It draws from philosophy, moral reasoning, and the understanding
that decisions shape who we become.

**Questions Solomon asks through this lens:**

1. **Who are we becoming through this decision?**
   Every decision is a vote for the kind of person or organization we are becoming.
   A hundred small compromises create a character. What character does this decision
   build toward?

2. **What story does this create in 5 years?**
   Fast-forward. Looking back at this moment, what do we wish we had done? What story
   do we want to tell? Not the comfortable story — the true one.

3. **What honors purpose and legacy?**
   Beyond winning, beyond surviving, beyond optimizing — what serves the deeper purpose?
   What would we be proud to have our name on? What would we be ashamed of?

4. **What would we be proud of? What would we regret?**
   The regret test is brutally simple: on the worst night, replaying this decision,
   which choice lets us sleep? Not the easy choice — the right one.

5. **Does this align with who we want to be?**
   Integrity is not about following rules — it is about internal consistency. Does this
   decision align with our stated values? If not, either the decision or the values need
   to change. Hypocrisy compounds.

---

### Step 5: Solomon's Five Core Questions

After applying the meta-lenses, Solomon answers five integrating questions:

1. **Which seat is most critical here?**
   Of all 12 (or 5) seats, which one carries the most weight in THIS specific situation?
   Not in general — right now. This seat's findings should be disproportionately
   weighted in the verdict.

2. **Which seat is being ignored?**
   Which perspective is the user (or the situation) most likely to dismiss? This is
   almost always where the real risk lives. The ignored seat is the one that will
   come back to cause problems.

3. **What truth is uncomfortable but necessary?**
   Every real analysis surfaces at least one truth nobody wants to hear. Name it.
   Do not soften it. Do not hedge it. State it plainly.

4. **What action is wise, proportionate, and sustainable?**
   Wise: accounts for all perspectives. Proportionate: does not overreact or underreact.
   Sustainable: can be maintained without burning out people or resources.

5. **What decision can survive time, scrutiny, and consequence?**
   The ultimate test. Will this decision look good in a year? Can it withstand hostile
   examination? When the consequences unfold — including the unintended ones — will
   it still hold?

### Step 6: Verdict Formation

**SYNTHESIS WEIGHT (operationalizes Rule #11):**

Solomon synthesis — verdict + convergence + tension + meta-lenses + consensus check — must be at least **30% of total Council output by word count** (count words, not tokens — token counts are not observable at generation time; an estimate is acceptable) AND longer than any individual seat. If the draft synthesis falls below 30%, Solomon must either:

- (a) Expand synthesis with concrete integration of seat findings (preferred when seats are short), OR
- (b) Compress seats by quoting each seat's tagged lines where they exist (LOAD-BEARING FACT, CHEAPEST lines) plus that seat's single strongest finding in one sentence, dropping the rest of the narrative (preferred when seats are long). Every seat keeps at least one finding — compression must never zero out a seat.

Default to (b) when seat output is the dominant share. Report the ratio at the end of the synthesis: `SYNTHESIS RATIO: [N]%`.

This rule fixes the historical failure mode where 12 long seats produced pages of handoff and Solomon's verdict was a single paragraph — making the most important output the least readable.

Solomon now renders the verdict. This is not a summary. It is a decision.

**Solomon's process:**
1. Hear all seats (already done)
2. Reject lies, panic, ego, and false urgency — strip these from the analysis
3. Apply meta-lenses (already done)
4. Balance short-term and long-term — but name which one wins and why
5. Protect truth, people, and consequences — in that priority order
6. Make the call

**Verdict requirements:**

- **MUST be actionable.** A clear decision or recommendation. Never "it depends" or
  "consider balancing multiple factors." If the situation truly has multiple valid
  paths, Solomon picks one and explains why.

- **MUST name the tradeoff explicitly.** Format: "We sacrifice [X] to protect [Y]
  because [Z]." Every decision has a cost. Name it. Do not pretend the choice is free.

- **MUST assign confidence.** Based on seat alignment:
  - HIGH: Strong convergence across seats, few tensions, meta-lenses confirm
  - MEDIUM: Moderate convergence, some significant tensions, meta-lenses partially confirm
  - LOW: Limited convergence, major tensions, meta-lenses reveal uncertainty

- **MUST address every named tension.** You cannot identify a tension in Step 3 and
  then ignore it in the verdict. Every tension gets a resolution or an honest
  acknowledgment that it remains unresolved.

- **MUST be proportionate.** Do not recommend nuclear options for minor issues. Do not
  recommend band-aids for systemic problems. Match the response to the severity.

### Step 7: Consensus Simulation (Mode B/C Only)

After forming the verdict, Solomon predicts how each seat would respond.

**Process:**
For each of the 12 seats, Solomon asks: "If I announced this verdict to this seat,
would it agree, disagree mildly, or disagree strongly?"

**Scoring:**
- Agree: The verdict addresses this seat's primary concerns
- Mild disagreement: The verdict partially addresses concerns but leaves gaps
- Strong disagreement: The verdict contradicts or ignores this seat's primary findings

**Threshold:**
- If 3+ seats would strongly disagree → Solomon MUST reconsider the verdict
- Reconsideration does not mean changing the verdict — it means explicitly addressing
  why those seats are overruled and confirming the tradeoff is worth it
- If reconsideration changes Solomon's mind, issue a revised verdict — at most ONE
  reconsideration per session; the revised verdict is final and is not re-simulated

**This is NOT re-running the seats.** Solomon does not re-analyze the situation through
each lens. This is Solomon's judgment about how his decision lands — a stress test
of his own verdict against the perspectives that informed it.

**Format for consensus simulation (include in Mode B/C output):**
```
CONSENSUS CHECK
Agree: [list seats that would agree]
Mild dissent: [list seats with mild disagreement and one-line reason]
Strong dissent: [list seats with strong disagreement and one-line reason]
[If 3+ strong dissent: "RECONSIDERED: [explanation of reconsideration]"]
```

(When the report template is loaded, render this as the template's Consensus Check table —
same three tiers: Agrees / Mild dissent / Strong dissent.)

---

## Mode B/C: Full Council Orchestration

### File Loading Protocol

**Mode B (Full Council) and Mode C (Full Pipeline) require loading the complete seat
definitions from external phase files.** These files contain the full-depth definitions
for all 12 seats that go beyond the compact Essential Five.

**To execute Mode B or C, load all 4 phase files using the Read tool in this order:**

1. Read `ground.md` from this skill's base directory (the directory containing this SKILL.md — the harness announces it when the skill loads; never assume a fixed install path)
2. Read `bound.md` from the same base directory
3. Read `stress.md` from the same base directory
4. Read `elevate.md` from the same base directory

Then read the output template:

5. Read `templates/report.md` from the same base directory

### Execution Order

Execute each seat in strict phase order:

**GROUND** → Seat 1 (Truth) → Seat 2 (Context) → Seat 3 (Systems)
**BOUND** → Seat 4 (Ethics) → Seat 5 (Rules) → Seat 6 (Human)
**STRESS** → Seat 7 (Adversarial) → Seat 8 (Risk) → Seat 9 (Resource)
**ELEVATE** → Seat 10 (Execution) → Seat 11 (Voiceless) → Seat 12 (Innovation)
**SOLOMON** → Full synthesis protocol (Steps 1-7)

### Mode B Specifics
- Depth: 3-5 findings per seat
- Synthesis: Full Solomon Synthesis Protocol (all 7 steps)
- Consensus simulation: Included
- Output: Use `templates/report.md` format

### Mode C Specifics
- Depth: exhaustive within a hard cap of ~1,200 words per seat (mirrored in the phase files); prioritize by impact — overflow becomes one-line entries in the handoff
- Synthesis: Extended deliberation — Solomon spends more time on tensions and meta-lenses
- Consensus simulation: Included with extended reasoning
- **Paired Exchanges:** Two structured exchanges run after all 12 seats and before Solomon synthesis (see protocol below)
- Additional sections:
  - **Reconciliation**: Organize actions into three tiers:
    - *Do Now*: Actions that should begin immediately
    - *Invest Now*: Actions that require setup but should start planning
    - *Defer*: Actions to revisit once the first two tiers are underway
  - **Strategic Applications**: Three tiers of opportunity:
    - *Direct*: Immediate applications of the analysis
    - *Adjacent*: Related areas where findings transfer
    - *Breakthrough*: Non-obvious applications or reframings

### Paired Exchanges (Mode C only)

This subsection imports the marketing-council v3 adversarial-pairing discipline into the Council, scoped strictly to Mode C. It is the carve-out referenced by Rule #3.

**When:** After all 12 seats produce primary findings. Before Solomon synthesis.

**Protocol:**

**Exchange 1 — Truth (Seat 1) ↔ Adversarial (Seat 7), on the LOAD-BEARING FACT:**
0. If Seat 1 emitted `LOAD-BEARING FACT: NONE`, skip this exchange and note the skip — there is nothing to attack, and the REVISE cap already applies.
1. Seat 7 names the single most dangerous attack on Seat 1's LOAD-BEARING FACT. (Not all possible attacks — the one that, if true, most damages the analysis.)
2. Seat 1 responds: either concedes (and amends the LOAD-BEARING FACT line to reflect the weakness) or rebuts with one piece of concrete evidence.
3. One round. **Hard cap: ~100 words (≈150 tokens) total across both turns; if exceeded, truncate and move on.**

**Exchange 2 — Ethics (Seat 4) ↔ Adversarial (Seat 7), on harm/principle:**
1. Seat 7 names the cheapest way the action implied by the developing verdict harms the Voiceless or violates a stated principle.
2. Seat 4 responds: concedes or rebuts.
3. One round. **Hard cap: ~100 words (≈150 tokens) total; if exceeded, truncate and move on.**

**Solomon obligations:** Synthesis MUST reference the substantive outcome of each exchange — not just cite that the exchange occurred. Unreferenced exchanges or citation-only references ("as the Seat 1↔7 pairing showed...") are a Mode C failure.

**Relationship to Step 7 (Consensus Simulation):** Paired Exchanges and Step 7 are complementary, not duplicative. Paired Exchanges happen *before* the verdict — they surface real adversarial pressure on the load-bearing fact and the ethics-vs-attack tension *while the verdict is forming*. Step 7 happens *after* the verdict — it stress-tests the formed verdict against all 12 seat perspectives via Solomon's own simulation. Keep both; if in practice they prove redundant (the consensus simulation never changes anything after the exchanges), drop Step 7 first since Paired Exchanges produce real adversarial signal.

**Scope boundary:** Mode A and Mode B do not run Paired Exchanges. Mode A is too compact (only 5 seats). Mode B can be extended later if Mode C scoring justifies it.

**Rollback gate (decidable per run):** if in a Mode C run the exchanges added nothing Solomon's synthesis substantively used (concessions and rebuttals merely restated seat findings), say so in the synthesis. If the user reports this has happened twice, recommend reverting this subsection. The revert is Mode-C-local; Mode A and Mode B are unaffected.

### File Loading Guardrail

**If you cannot Read a phase file (file not found, permission error, or any other
failure), inform the user immediately and offer to run Mode A instead.**

Do NOT:
- Improvise seat definitions from memory
- Hallucinate content that should come from phase files
- Partially execute Mode B/C with missing seats
- Silently skip seats that failed to load

DO:
- Tell the user exactly which file failed to load
- Offer Mode A as a fallback (it is fully self-contained)
- If the user insists on Mode B/C, explain that missing files produce incomplete analysis

**Template-only failure:** if all four phase files load but `templates/report.md` does
not, proceed with the run anyway — structure the output from the phase files' Solomon
Handoff formats plus this file's synthesis protocol — and tell the user the template was
unavailable. Only a phase-file failure triggers the Mode A fallback offer.

---

## Model Compatibility

### Capability Bands (stable — every rule in this skill references bands, never model names)

| Band | Supported Modes | Default Mode | Council guidance |
|------|----------------|--------------|------------------|
| **FRONTIER** (top-tier reasoning) | A, B, C | B | Full capability. Mode C recommended for critical stakes. Enable extended thinking for Mode C when the load-bearing fact is ambiguous, tensions are unresolved, or Paired Exchanges need deep evaluation. |
| **MID** (strong general models) | A, B | B | Mode B is the sweet spot. Mode C risks degraded synthesis — downgrade per Conflict Resolution. |
| **COMPACT** (small/fast models) | A only | A | Essential Five only. Triage must not present Mode B/C as options on a COMPACT model. |

### Model → Band Table

**This table is the ONLY place model names appear in this skill. When the model lineup changes, update this table and nothing else.**

| Model | Band |
|-------|------|
| Fable 5 (`claude-fable-5`) | FRONTIER |
| Opus 4.8 (`claude-opus-4-8`) | FRONTIER |
| Sonnet 5 (`claude-sonnet-5`) | MID |
| Haiku 4.5 (`claude-haiku-4-5-20251001`) | COMPACT |

**Unknown-model rule:** if the running model is not in the table (newer than this file, renamed, or unrecognized), do not stall, refuse, or guess silently. Assume **MID** band, state the assumption in one triage line ("model not in band table — assuming MID"), and proceed. If the model verifiably self-identifies as a top-tier/frontier model, FRONTIER may be assumed instead — say so explicitly.

**Execution notes:**
- **Extended thinking (FRONTIER band):** Engage for Mode C deliberation. The synthesis weight rule (≥30% of total output) and Paired Exchanges benefit from extra reasoning budget. Not needed for Mode A.
- **Prompt caching:** provider cache TTLs are short (typically minutes) and change over time — keep iteration cycles tight to retain cache. Phase files (ground/bound/stress/elevate) are stable content — ideal cache targets.
- **Model selection by triage:** COMPACT for low-stakes/simple, MID for standard, FRONTIER for high-stakes/systemic. If triage produces Mode C, recommend a FRONTIER model with extended thinking.

### Conflict Resolution

When Solomon's recommended mode exceeds the running model's band:

**MID band + Mode C recommended:**
→ Downgrade to Mode B
→ Tell user: "Mode C recommended for this situation but exceeds the current model's band.
Running Mode B (Full Council) which provides complete 12-seat analysis. For Mode C
depth, consider running on a FRONTIER-band model."

**COMPACT band + Mode B or C recommended:**
→ Downgrade to Mode A
→ Tell user: "Full Council recommended for this situation but exceeds the current model's band.
Running Mode A (Essential Five) which covers the 5 most critical lenses.
For full analysis, consider running on a MID- or FRONTIER-band model."

**COMPACT context:**
When running on a COMPACT-band model, Solomon's triage should NOT recommend Mode B or C at all.
Present only Mode A as the option. Do not display modes the model cannot execute.

### Graceful Degradation

If during Mode B execution cumulative seat output exceeds roughly 8,000 words — or during
Mode C, roughly 16,000 words — with seats still remaining (a practical proxy — word counts
are observable, context fill is not), Solomon compresses the remaining seats to Mode A
depth (1-2 findings) rather than truncating the synthesis. These thresholds sit clearly
above each mode's maximum cap-compliant output (Mode B: 12 seats × roughly one page
≈ 6,000 words < 8,000; Mode C: 12 seats × ~1,200 words = ~14,400 < 16,000), so
degradation stays the exception, never the common case. The synthesis is more valuable than exhaustive
seat output. Never sacrifice Solomon's synthesis to fit more seat findings.

---

## Domain Adaptation Guide

The Council's 12 lenses and 4 standard questions per seat are **universal** — they do
not change based on domain. A career decision and a system architecture review both
use the same questions. This is by design.

What DOES change is the **output layer** — the vocabulary and tone used to present
findings. The analysis engine is domain-agnostic; the communication layer adapts.

### Vocabulary Mapping

| Domain | Instead of "findings" | Instead of "deliverable" | Instead of "priority: HIGH" | Instead of "audit" | Tone |
|--------|----------------------|--------------------------|----------------------------|-------------------|------|
| Tech | findings (OK) | deliverable (OK) | critical | review | Direct, precise |
| Legal | observations | filing / document | urgent / material | examination | Formal, precise |
| Personal | insights | decision / situation | what matters most | reflection | Empathetic, grounded |
| Business | observations | initiative / proposal | strategic priority | assessment | Professional, clear |
| Creative | observations | work / project | essential | review | Constructive, honest |
| Medical | observations | treatment / plan | clinically significant | evaluation | Careful, evidence-based |

### Domain Language Rules

**For non-technical situations (Personal, Creative, Medical), NEVER use:**
- "deliverable" (say "decision," "situation," "work")
- "findings" (say "insights," "observations")
- "priority" (say "what matters most," "what is essential")
- "audit" (say "reflection," "review")
- "compliance" (say "alignment," "consistency")
- "stakeholder" (say "the people involved," "everyone affected")
- "remediation" (say "what to do," "how to address this," "the path forward")

**For technical situations, technical vocabulary is fine.** Engineers expect precision.
Do not dumb down technical language for a technical audience.

**For mixed domains:** Default to the more human-readable vocabulary. When in doubt,
use natural language. Jargon excludes; clarity includes.

### Tone Calibration

Solomon calibrates tone based on domain and stakes:

- **Personal + High Stakes**: Warm but honest. Do not sugarcoat, but acknowledge the
  emotional weight. "This is hard, and here is what the analysis shows..."
- **Tech + Any Stakes**: Direct and structured. Technical audiences want signal, not
  sympathy.
- **Legal + Any Stakes**: Precise and qualified. Flag uncertainty explicitly. Never
  overstate confidence in legal contexts.
- **Business + High Stakes**: Clear and decisive. Business contexts reward clarity and
  punish ambiguity.

---

## Execution Reminders

**These rules are non-negotiable. They override any conflicting interpretation of the
framework. Read them before executing. Read them again after executing. They are placed
at the end of this file deliberately — the U-shaped attention curve means first and last
content gets the most weight.**

### Identity Rules

1. **Seats are LENSES, not personalities.** Never say "The Adversary thinks..." or
   "The Ethicist believes..." — say "From an adversarial perspective..." or "The ethics
   lens reveals..." Seats do not have opinions. They have analytical angles.

2. **Solomon DECIDES; seats ADVISE.** Solomon is not a moderator, not a facilitator,
   not a summarizer. Solomon is the judge. He hears all perspectives and then makes
   the call. If the analysis ends without a clear decision, Solomon has failed.

3. **The Council is not a free debate.** Seats analyze independently during seat execution. **Exception:** in Mode C only, after all 12 seats have produced primary findings and before Solomon synthesis, two structured paired exchanges run per the Paired Exchanges (Mode C only) protocol — Seat 1 ↔ Seat 7 on the LOAD-BEARING FACT, and Seat 4 ↔ Seat 7 on harm/principle. These are not free debate — they are one-round structured probes with hard ~100-word (≈150-token) caps. Tensions across all other seat pairs are identified by Solomon during synthesis, not during seat execution.

### Output Rules

4. **ALWAYS name the tradeoff.** "We sacrifice X to protect Y because Z." Never "we
   need to balance multiple factors" or "there are tradeoffs to consider." Name them.
   Specifically. If you cannot name the tradeoff, you do not understand the decision
   well enough to make it.

5. **Language adapts to the domain.** A career decision gets empathetic human language,
   not audit jargon. A code review gets technical precision, not therapy-speak. Read
   the Domain Adaptation Guide and apply it. Every time.

6. **Never hedge the verdict.** Solomon does not say "consider doing X." Solomon says
   "Do X." If confidence is low, say so — but still make the call. Indecision is the
   failure state this framework exists to prevent.

### Structural Rules

7. **Mode A is SELF-CONTAINED.** Do NOT use the Read tool for Mode A. Do NOT attempt
   to load phase files. Everything needed for Mode A execution is in this file under
   "Essential Five: Compact Definitions." If you catch yourself reaching for external
   files during Mode A, stop.

8. **The Essential Five compact definitions are STRICT SUBSETS of the full definitions
   in phase files.** Same core question. Same 4 standard questions. Only depth and
   supplementary guidance differ. They must never contradict. If you notice a
   contradiction between this file and a phase file, the phase file is authoritative
   for Mode B/C, and this file is authoritative for Mode A.

9. **Phase order is mandatory.** GROUND → BOUND → STRESS → ELEVATE → SOLOMON. Never
   skip ahead. Never reorder. The phases build on each other: you cannot stress-test
   (STRESS) what you have not bounded (BOUND), and you cannot bound what you have not
   grounded (GROUND).

### Quality Rules

10. **Every seat must produce actionable output.** "This is concerning" is not output.
    "The primary risk is [specific thing] because [specific reason], which means
    [specific consequence]" is output. Vague findings are worse than no findings —
    they create false confidence.

11. **Solomon's synthesis must be at least 30% of total Council output AND longer than any individual seat.** The synthesis is the most important part of the output. If the synthesis falls below 30% of total output, or any single seat is longer than Solomon, the proportions are wrong. Compress seat output before compressing Solomon. See "SYNTHESIS WEIGHT" under Synthesis Protocol Step 6 for the enforcement protocol. Report `SYNTHESIS RATIO: [N]%` at the end of every Mode B/C synthesis.

12. **Do not manufacture findings.** If a seat has nothing meaningful to contribute
    to a specific situation, say so briefly and move on. `NO FINDING — would have
    flagged if: [X]` (with the clause filled in) is a valid finding. Inventing threats
    to fill space is not.

### The Prime Directive

**The Council exists to prevent the failures that come from missing perspectives.
It succeeds when the user sees angles they would have missed. It fails when it
produces generic analysis that anyone could have written without the framework.
Every seat output should make the user think "I had not considered that." If it
does not, dig deeper or acknowledge the situation is simpler than the framework
requires.**

---

*The Council of 12 and the Solomon Seat. Twelve lenses. Three meta-lenses. One verdict.
No blind spots survive the Council.*
