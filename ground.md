# GROUND — Establish Reality

> The first phase of every Council session. Before we can judge, constrain, stress-test, or imagine — we must know what is actually true, what led here, and what mechanism is at work. Without reality, every other seat operates on fantasy.

---

## Seat 1: Truth / Evidence

> This seat kills confusion.

**Phase:** GROUND
**Focus:** What is objectively true
**Core question:** "What do we actually know?"

---

### Standard Questions

These 4 questions are asked in EVERY mode (A, B, and C). They form the minimum analysis for this seat.

<!-- SYNC: must match SKILL.md Seat 1 core question + standard questions -->

1. What happened?
2. What do we know vs. assume?
3. What is assumption, rumor, emotion, or interpretation?
4. What evidence exists?

---

### Extended Questions (Mode B/C)

These questions deepen the analysis beyond the standard set. Use in Mode B (select 2-3 most relevant) and Mode C (all).

5. What data or documentation supports the claims being made?
6. Who is the source of each claim, and what is their reliability and potential bias?
7. What would we need to verify before acting on this information?
8. If we are wrong about the key facts, what changes about the entire analysis?

---

### How to Apply This Seat

**The discipline of Truth is separation.** Separate what happened from what people say happened. Separate what is documented from what is remembered. Separate data from narrative. Separate observation from interpretation.

When analyzing a situation through this seat:

1. **Start with first-hand evidence.** What can be directly observed, measured, or documented? Logs, records, screenshots, timestamps, quotes — anything that exists independent of anyone's interpretation.

2. **Identify the claims.** Every situation comes wrapped in claims. "The system is slow." "She was hostile." "The market is shifting." Strip each claim to its factual core. "The system is slow" might mean "page load time increased from 200ms to 3.2s after Tuesday's deploy" — or it might mean "one user complained once."

3. **Tag each piece of information:**
   - **Fact:** Directly observable, documented, measurable
   - **Inference:** Logically derived from facts, but not directly observed
   - **Assumption:** Taken as true without verification
   - **Interpretation:** A meaning assigned to facts (could be wrong)
   - **Rumor:** Unverified claim from an unverified source
   - **Emotion disguised as fact:** "Everyone knows..." "It's obvious that..." "Clearly..."

4. **Test the load-bearing claims.** Which facts, if wrong, would change the entire analysis? These are the ones worth verifying before proceeding. Not every claim needs verification — only the ones the decision rests on.

5. **State what is NOT known.** Gaps in knowledge are findings too. "We don't know why the error rate spiked between 2am and 4am" is as important as any fact.

---

### Domain Adaptation

How this seat's questions manifest across domains:

| Question | Technical | Legal | Personal | Business |
|----------|-----------|-------|----------|----------|
| What happened? | What do logs, metrics, and stack traces show? What is the reproduction path? | What is documented in the record? What is on file vs. alleged? | What actually occurred? What did someone literally say or do? | What do the numbers show? What does the data say? |
| What do we know vs. assume? | Which behavior is confirmed by tests vs. assumed from docs? | Which facts are established vs. stipulated? | What did I observe vs. what am I filling in? | Which metrics are measured vs. estimated? |
| What is assumption, rumor, emotion, or interpretation? | Is "the system is slow" measured or felt? Is the root cause confirmed or guessed? | Is the witness reliable? Is the evidence authenticated? | Am I reacting to what happened or my story about it? | Is "the market is declining" data or fear? |
| What evidence exists? | Logs, tests, profiling data, git history, monitoring dashboards | Documents, contracts, communications, witness statements, records | Texts, emails, specific events with dates, observable behavior | Financial reports, market data, customer data, competitive intelligence |

---

### Depth Scaling

**Mode B (Full Council):** 3-5 findings. Focus on the standard questions. Select 2-3 extended questions most relevant to this specific situation. Each finding should be a substantive paragraph with specific evidence cited — not a vague bullet point.

**Mode C (Full Pipeline):** Exhaustive analysis. All standard AND extended questions. Each finding should include:
- The evidence itself (what we know)
- The confidence level (how sure we are)
- The implications (what this means for the analysis)
- Cross-references to other seats where relevant
- Aim for 5-8 findings with full evidence chains. Hard cap ~1,200 words — overflow becomes one-line entries in the handoff.

---

### Anti-Patterns

This seat should NOT:

- **Make value judgments.** "The deployment was reckless" is Ethics territory. Truth says: "The deployment bypassed the staging environment and had no rollback plan."
- **Speculate about causes.** "The outage was caused by poor architecture" is Systems territory. Truth says: "The outage occurred at 2:14am when service X lost connection to database Y."
- **Assess risk or impact.** "This could bring down the whole system" is Risk territory. Truth says: "The affected service handles 40% of user requests."
- **Propose solutions.** "We should add monitoring" is Execution territory. Truth says: "No monitoring exists for this failure mode."
- **Editorialize.** "Clearly, management dropped the ball" is interpretation. Truth says: "The project had no executive sponsor after March 15."
- **Accept emotional framing as fact.** When someone says "everyone is upset," Truth asks: "How many people? What specifically did they say? When?"

---

### Cross-Seat Awareness

**Feeds into:**
- **Systems / Root Cause (Seat 3):** Facts are the raw material for root cause analysis. Systems cannot diagnose without Truth's evidence.
- **Rules / Constraints (Seat 5):** Facts determine which constraints are triggered. A confirmed data breach triggers different rules than a suspected one.
- **Risk / Fragility (Seat 8):** Accurate facts determine which risks are real vs. imagined.

**Watch for overlap with:**
- **Context / Pattern (Seat 2):** Truth asks "what IS true right now" — a snapshot. Context asks "what WAS true before that changes the meaning." They're complementary: Truth establishes the current state, Context provides the timeline. If you find yourself explaining history, hand it to Context.

---

### Solomon Handoff

When passing findings to Solomon, structure as:

```
SEAT 1 — TRUTH / EVIDENCE:
LOAD-BEARING FACT: [the single fact this entire analysis rests on, or NONE — analysis is opinion-only]
IF FALSE: [what becomes invalid downstream if the load-bearing fact is wrong]
Signal strength: [strong/moderate/weak — based on quality and quantity of evidence]
Key findings:
1. [Factual finding with evidence cited]
2. [Factual finding with evidence cited]
3. [Factual finding with evidence cited]
Confidence: [high/medium/low — high = multiple independent sources; medium = single reliable source; low = inference from limited data]
Critical flag: [yes/no — yes if a key "fact" the situation rests on is actually unverified]
Knowledge gaps: [What important information is missing]
```

**Note (mirrors SKILL.md Mode A output rule):** Seat 1 output MUST begin with the LOAD-BEARING FACT and IF FALSE lines. If no load-bearing fact can be named, emit `LOAD-BEARING FACT: NONE — analysis is opinion-only`. When NONE is emitted, Solomon caps the verdict at REVISE (cannot return PROCEED). This applies to Modes A, B, and C.

---
---

## Seat 2: Context / Pattern

> This seat prevents shallow judgment.

**Phase:** GROUND
**Focus:** What led to this
**Core question:** "What led here? What does the pattern say?"

---

### Standard Questions

These 4 questions are asked in EVERY mode (A, B, and C). They form the minimum analysis for this seat.

<!-- SYNC: Seat 2 has no SKILL.md compact definition (not in Mode A); must match the SKILL.md Quick Reference Card row for Seat 2 -->

1. How did we get here?
2. Is this a pattern or a one-time event?
3. What happened before that changes the meaning now?
4. What precedent matters?

---

### Extended Questions (Mode B/C)

These questions deepen the analysis beyond the standard set. Use in Mode B (select 2-3 most relevant) and Mode C (all).

5. What cycles or recurring dynamics are at play?
6. What has been tried before, and why did it succeed or fail?
7. What broader trends (industry, cultural, organizational) shape this situation?
8. If this is a pattern, what is the pattern's trajectory — escalating, stable, or declining?

---

### How to Apply This Seat

**The discipline of Context is depth.** Every situation looks different when you zoom out in time. A "sudden crisis" is often the latest episode of a long-running pattern. A "unique opportunity" may be the third time this offer has been made. Context adds the timeline that Truth's snapshot lacks.

When analyzing a situation through this seat:

1. **Trace the timeline.** When did this situation begin? Not when it became visible — when did the conditions that created it first appear? The real start date is often months or years before the presenting event.

2. **Look for recurrence.** Has this happened before? If so, how many times? What was done about it? Did the response work? Recurring problems are structural (hand to Systems), but the pattern itself is Context's finding.

3. **Identify the inflection points.** What changed? When did the situation shift from stable to unstable, from manageable to critical, from opportunity to threat? Inflection points reveal what forces are at work.

4. **Check for precedent.** Has someone else faced this situation? What happened to them? Precedent doesn't determine the answer, but ignoring it is reckless.

5. **Assess the trajectory.** Is this getting better, worse, or holding steady? The current state is Truth's domain; the direction of movement is Context's. A problem that's improving needs a different response than one that's accelerating.

6. **Surface the history that changes meaning.** "She was hostile in the meeting" means one thing in isolation. "She was hostile in the meeting, which was the third time her team's work was publicly criticized" means something different. Context finds the history that reframes the present.

---

### Domain Adaptation

How this seat's questions manifest across domains:

| Question | Technical | Legal | Personal | Business |
|----------|-----------|-------|----------|----------|
| How did we get here? | What's the git history? What architectural decisions led to this state? What previous incidents relate? | What's the procedural history? What prior filings or rulings matter? | What's the relationship history? What events preceded this moment? | What market, organizational, or strategic decisions created the current situation? |
| Is this a pattern or one-time? | Has this bug class appeared before? Is this incident type recurring? | Is this a novel legal question or settled law? Is this litigant a repeat actor? | Is this the first time or the fifteenth? Does this fight keep happening? | Is this a market cycle, a structural shift, or an anomaly? |
| What happened before that changes meaning? | Was there a recent deploy, migration, or config change? What tech debt accumulated? | What prior agreements, rulings, or communications alter the interpretation? | What trust was built or broken before this? What promises were made? | What strategic pivots, leadership changes, or competitor moves set the stage? |
| What precedent matters? | How have similar systems solved this? What do post-mortems from comparable incidents say? | What case law, regulatory guidance, or industry standard applies? | How have I handled similar situations before? What worked and what didn't? | What did competitors or peers do in analogous situations? What was the outcome? |

---

### Depth Scaling

**Mode B (Full Council):** 3-5 findings. Focus on the standard questions. Select 2-3 extended questions most relevant to this specific situation. Each finding should explain how the historical context changes the analysis — don't include history for its own sake.

**Mode C (Full Pipeline):** Exhaustive analysis. All standard AND extended questions. Each finding should include:
- The historical fact or pattern identified
- How it changes the interpretation of the current situation
- The trajectory (escalating, stable, or declining)
- Cross-references to other seats where relevant
- Aim for 5-8 findings that materially change how the situation should be understood. Hard cap ~1,200 words — overflow becomes one-line entries in the handoff.

---

### Anti-Patterns

This seat should NOT:

- **Get lost in history for its own sake.** Only include context that changes the analysis. "The company was founded in 1987" is irrelevant unless the founding story explains today's culture problem.
- **Confuse correlation with causation.** "This happened after that" is Context's finding. "This happened BECAUSE of that" is Systems territory. Context provides the timeline; Systems provides the mechanism.
- **Predict the future from patterns alone.** "This has happened three times, so it will happen again" is a Risk assessment, not a context finding. Context says: "This has happened three times, following the same trigger pattern."
- **Substitute narrative for evidence.** "Everyone knows the company has always been like this" is not context — it's folklore. Verify the narrative against facts (coordinate with Truth).
- **Bury the lead.** The most important context finding is the one that most dramatically changes how the situation should be understood. Lead with it.

---

### Cross-Seat Awareness

**Feeds into:**
- **Systems / Root Cause (Seat 3):** Patterns reveal structural drivers. If Context finds recurrence, Systems explains the mechanism.
- **Human / Emotional (Seat 6):** History shapes emotions and trust levels. A "minor slight" after a long history of slights is not minor.
- **Innovation / Possibility (Seat 12):** Understanding what has been tried before (and why it failed) prevents reinventing failed approaches.

**Watch for overlap with:**
- **Truth / Evidence (Seat 1):** Truth provides the current snapshot — what IS true now. Context adds the temporal dimension — what WAS true that matters. If you're describing present state, that's Truth. If you're describing how we got to the present state, that's Context.
- **Systems / Root Cause (Seat 3):** Context says "this keeps happening." Systems says "this keeps happening BECAUSE..." Context identifies the pattern; Systems identifies the mechanism. Don't cross into causal analysis — just document what happened and when.

---

### Solomon Handoff

When passing findings to Solomon, structure as:

```
SEAT 2 — CONTEXT / PATTERN:
Signal strength: [strong/moderate/weak — based on pattern clarity and evidence depth]
Key findings:
1. [Context finding that changes the interpretation]
2. [Pattern identified with frequency and trajectory]
3. [Precedent that informs the decision]
Confidence: [high/medium/low — high = well-documented history; medium = partial records; low = inferred from indirect evidence]
Critical flag: [yes/no — yes if a critical pattern is being ignored or a key precedent overlooked]
Pattern trajectory: [escalating/stable/declining/unknown]
```

---
---

## Seat 3: Systems / Root Cause

> This seat stops repetition.

**Phase:** GROUND
**Focus:** Structure, process, and hidden drivers
**Core question:** "What is the real mechanism at work?"

---

### Standard Questions

These 4 questions are asked in EVERY mode (A, B, and C). They form the minimum analysis for this seat.

<!-- SYNC: must match SKILL.md Seat 3 core question + standard questions -->

1. Is this a symptom or the real problem?
2. What mechanism keeps recreating this?
3. What incentives are causing this behavior?
4. What would fix the system instead of patching the event?

---

### Extended Questions (Mode B/C)

These questions deepen the analysis beyond the standard set. Use in Mode B (select 2-3 most relevant) and Mode C (all).

5. What feedback loops are reinforcing the current state?
6. Where are the leverage points — small changes that would shift the whole system?
7. What second-order effects would a fix create?
8. What structural incentives make the current (broken) state the path of least resistance?

---

### How to Apply This Seat

**The discipline of Systems is depth — going below the surface until you find the mechanism.** Most problems are symptoms. The presenting issue is what gets attention, but the generating structure is what creates the problem — and will recreate it after the symptom is patched.

When analyzing a situation through this seat:

1. **Apply the Five Whys (but don't stop at five).** Start with the visible problem and ask "why" until you reach a structural cause. The first "why" explains the symptom. The third "why" usually reaches process. The fifth "why" often reaches incentives or design.

   Example:
   - Why did the deploy fail? → The migration script had a bug.
   - Why wasn't the bug caught? → No staging environment mirrors production data.
   - Why no staging mirror? → The team doesn't have budget for a production-scale staging DB.
   - Why no budget? → Infra costs aren't allocated to teams; they come from a shared pool nobody owns.
   - Why doesn't anyone own infra costs? → The organizational incentive structure rewards feature velocity, not infrastructure reliability.

   The root cause isn't a buggy migration script. It's an incentive structure that punishes investing in reliability.

2. **Map the feedback loops.** What reinforcing cycles maintain the current state? Positive feedback loops amplify (growth begets growth, failure begets failure). Negative feedback loops stabilize (thermostats, market corrections). Identify which loops are operating and whether they're helping or trapping.

3. **Follow the incentives.** People behave rationally within their incentive system, even when the behavior looks irrational from outside. If behavior seems irrational, you haven't understood the incentives yet. Ask: "Given their actual incentives, is this behavior perfectly logical?"

4. **Distinguish proximate cause from root cause.**
   - **Proximate cause:** What triggered the event. ("The disk filled up.")
   - **Root cause:** What made the event possible and likely. ("No log rotation, no monitoring, no capacity planning.")
   - Fixing the proximate cause patches this incident. Fixing the root cause prevents the category.

5. **Look for structural analogies.** The same system dynamics appear across domains. A team with no feedback mechanism will drift the same way a thermostat with a broken sensor will. Technical debt and financial debt follow the same compound interest dynamics.

6. **Identify leverage points.** Where would a small change produce a disproportionate effect? These are usually at the level of incentives, information flows, or feedback loops — not at the level of individual actions or policies.

---

### Domain Adaptation

How this seat's questions manifest across domains:

| Question | Technical | Legal | Personal | Business |
|----------|-----------|-------|----------|----------|
| Symptom or real problem? | Is this a bug or an architecture flaw? Is the error the problem or a symptom of a deeper design issue? | Is this a legal violation or a symptom of a broken compliance process? | Am I upset about this specific thing, or is this the latest expression of a deeper pattern? | Is revenue declining because of this product, or because of market positioning? |
| What mechanism keeps recreating this? | What code path, architectural pattern, or process gap produces this class of failure? | What regulatory gap or contractual structure keeps creating liability? | What pattern in my behavior or relationships keeps producing this outcome? | What organizational design, market structure, or strategy flaw drives this? |
| What incentives cause this behavior? | Is the team incentivized to ship fast at the expense of quality? Does the reward structure encourage shortcuts? | Do the legal incentives favor settlement over litigation (or vice versa)? Who profits from the current state? | What am I getting out of maintaining the status quo? What reward keeps me stuck? | What does the compensation/promotion structure actually reward vs. what leadership says it rewards? |
| System fix vs. event patch? | Would adding a test fix this bug, or do we need a testing culture change? | Would a new policy fix this, or does the enforcement mechanism need redesigning? | Would an apology fix this, or does the relationship dynamic need restructuring? | Would a new hire fix this, or does the team structure need redesigning? |

---

### Depth Scaling

**Mode B (Full Council):** 3-5 findings. Focus on the standard questions. Select 2-3 extended questions most relevant to this specific situation. Each finding should clearly distinguish symptom from root cause and identify the mechanism — not just name it.

**Mode C (Full Pipeline):** Exhaustive analysis. All standard AND extended questions. Each finding should include:
- The symptom (what is visible)
- The mechanism (what generates the symptom)
- The incentive structure (why the mechanism persists)
- The leverage point (where to intervene for maximum effect)
- Second-order effects of intervention
- Cross-references to other seats where relevant
- Aim for 5-8 findings with full causal chains. Hard cap ~1,200 words — overflow becomes one-line entries in the handoff.

---

### Anti-Patterns

This seat should NOT:

- **Stop at the first plausible cause.** "The deploy broke because of a bad migration" is a proximate cause, not a root cause. Keep asking why.
- **Propose solutions.** "We should add monitoring" is Execution territory. Systems says: "The absence of monitoring means failures go undetected for an average of 4 hours, during which cascading damage accumulates."
- **Ignore incentive structures.** If people keep doing something that seems irrational, the incentives explain why. Don't blame individuals for structural problems.
- **Confuse map with territory.** The system model is not the system. It's a useful simplification. Acknowledge what the model doesn't capture.
- **Over-engineer the analysis.** Not every problem has a deep structural cause. Sometimes the proximate cause IS the root cause (a typo, a one-time mistake). Systems should say so when that's the case, not manufacture depth.

---

### Cross-Seat Awareness

**Feeds into:**
- **Resource / Tradeoff (Seat 9):** Systemic fixes have systemic costs. Addressing root causes usually requires more investment than patching symptoms.
- **Execution / Feasibility (Seat 10):** Understanding the mechanism determines what fix will actually work. A fix that addresses symptoms will fail if the mechanism is untouched.
- **Innovation / Possibility (Seat 12):** Seeing the real system often reveals non-obvious solutions. Once you understand the mechanism, creative interventions become visible.

**Watch for overlap with:**
- **Context / Pattern (Seat 2):** Context asks "what happened before" — the timeline. Systems asks "why does it keep happening" — the mechanism. Context identifies the pattern; Systems explains the engine that produces it. If you're documenting history, hand it to Context. If you're explaining causation, that's Systems.
- **Risk / Fragility (Seat 8):** Systems explains why things break structurally; Risk asks what specifically could break and how bad it would be. Systems diagnoses the disease; Risk predicts the symptoms.

---

### Solomon Handoff

When passing findings to Solomon, structure as:

```
SEAT 3 — SYSTEMS / ROOT CAUSE:
Signal strength: [strong/moderate/weak — based on confidence in the causal chain]
Key findings:
1. [Root cause finding: symptom → mechanism → incentive]
2. [Feedback loop identified with direction (reinforcing/balancing)]
3. [Leverage point identified with expected impact]
Confidence: [high/medium/low — high = clear causal chain with evidence; medium = plausible mechanism, needs validation; low = hypothesis based on limited data]
Critical flag: [yes/no — yes if a systemic driver is being ignored in favor of symptom-patching]
Leverage points: [List specific intervention points ranked by impact-to-effort ratio]
```

---
---

> **GROUND complete.** Reality is established — we know what is true, what led here, and what mechanism is at work. The Council now moves to BOUND to identify constraints: what is right, what is allowed, and how people will actually respond.
