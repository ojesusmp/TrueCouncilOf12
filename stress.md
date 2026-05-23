# STRESS — Pressure Test

> The third phase. Reality is established (GROUND) and constraints are drawn (BOUND). Now we break things. This phase assumes the worst — intentional attack, accidental failure, hidden costs. If a plan survives STRESS, it deserves to exist. If it doesn't, better to know now.

---

## How to Read This Phase

STRESS contains three seats, each with a distinct mandate:

- **Seat 7 (Adversarial)** assumes an intelligent, motivated enemy. Threats here are purposeful.
- **Seat 8 (Risk)** assumes nothing is trying to break you — things just break. Failures here are accidental.
- **Seat 9 (Resource)** asks what everything truly costs, including what you never get to do because you chose this.

The boundary between Seats 7 and 8 is one of the most important distinctions in the Council. A flood that takes out your server is Risk. A competitor who discovers your server location and triggers that outage is Adversarial. Same outcome, completely different response. The Council keeps these seats separate because the mitigation strategies are different: you build redundancy for Risk, you build detection and deterrence for Adversarial.

Seat 9 operates somewhat independently — it cuts across everything. Even a plan that survives adversarial attack and has no meaningful accidental failure modes might still be the wrong choice because the resources it consumes were needed elsewhere. Resource is always relative.

---

## Phase Prerequisites

Before STRESS runs, GROUND (Seats 1-3) and BOUND (Seats 4-6) should be complete. STRESS assumes:

- The core claim has been validated or challenged (GROUND)
- The rules, constraints, and human dimensions are understood (BOUND)
- There is something concrete enough to attack, break, and cost-assess

If the plan is still at the "vague idea" stage, STRESS will produce noise, not signal. Ensure some minimum viable specificity exists before loading this phase.

---

## Seat 7: ADVERSARIAL

**Tagline:** This seat assumes enemies exist.
**Phase:** STRESS (Seats 7-9)
**Focus:** Intentional exploitation and weaponization
**Core Question:** How would someone break this on purpose?

---

### The Adversarial Mindset

Most planning assumes goodwill. This seat removes that assumption entirely.

An adversary is any intelligent actor with both motive and means to undermine the plan. Adversaries are not just competitors or hackers. They include:

- **External actors**: competitors, hostile regulators, bad-faith counterparties, short-sellers, trolls
- **Internal actors**: disgruntled employees, misaligned partners, people who feel threatened by the plan's success
- **Systemic actors**: institutions that benefit from the status quo the plan disrupts
- **Indirect actors**: people who don't oppose the plan but whose actions, if the plan affects them negatively, become opposition
- **Future actors**: adversaries who don't exist yet but will emerge once the plan gains visibility or value

The adversary is not stupid. This seat requires you to model a sophisticated opponent who reads your documentation, understands your systems, and has time to find the weakness you overlooked. Assuming a naive adversary gives false comfort.

---

### Standard Questions (4)

These four questions run in all modes (A, B, and C). They are non-negotiable.

**Q7.1 — Weakest Point First**
*What is the single weakest point an adversary would attack first?*

The adversary does not need to overcome your strongest defenses — they only need to find the weakest link. Ask: if someone had 24 hours to undermine this plan, where would they spend their time? Not where you are strongest. Not where you have the most documentation. The weakest point is often:

- The thing you haven't finished building yet
- The assumption you've never tested
- The handoff between two systems where neither team "owns" security
- The person with the most access and the least oversight
- The process that works when everyone follows it but breaks when someone doesn't

Probe this explicitly. Name the weakest point. The act of naming it is itself protective — unnamed vulnerabilities stay invisible.

**Q7.2 — Weaponization of Context**
*Can any element be taken out of context and used against the creator?*

Good-faith artifacts are routinely weaponized. This question asks you to look at every document, statement, action, and structure with adversarial eyes:

- What does this email look like if the relationship goes sour and it ends up in discovery?
- What does this policy look like if someone wants to prove discriminatory intent?
- What does this code comment look like if a journalist screenshots it?
- What does this financial projection look like if investors claim they were misled?
- What does this private conversation look like if someone leaks it selectively?

The test is not whether the thing is defensible in full context. The test is whether it can be made to look bad in a 30-second clip or a one-paragraph excerpt. If it can, assess whether that matters and whether the artifact needs to change.

**Q7.3 — Assumption Challenge**
*What assumption could an adversary challenge or disprove?*

Every plan rests on assumptions. An adversary who disproves a foundational assumption can collapse the plan's rationale entirely, even if the plan itself is still operationally sound. Identify:

- The technical assumptions (this technology works at this scale, this API behaves this way)
- The market assumptions (customers want this, the pricing is competitive)
- The legal assumptions (this is compliant, this jurisdiction applies)
- The relational assumptions (this person is aligned, this partnership will hold)
- The temporal assumptions (this will happen by this date)

For each assumption, ask: if an adversary could prove this assumption false — even partially — what damage does that do? Which assumption, if disproved, is most damaging? That is the one to harden first.

**Q7.4 — Credibility Attack**
*What would an adversary say to discredit this?*

This is the narrative attack. Assume an adversary writes the hostile press release, the critical forum post, the damning review, the competing analysis. What is their best argument?

Do not write a weak strawman. Write the strongest version of the critique. A good adversarial critique will:
- Find the real tension or contradiction in the plan
- Reframe costs as larger than presented
- Question the motivation of the creator
- Cite real facts selectively
- Appeal to an audience that already has doubts

Once you've written the strongest hostile narrative, assess: is any of it true? What parts require a response? What would you do differently if you knew this critique was coming?

---

### Extended Questions (Modes B and C)

**Q7.5 — Actor Mapping**
*Who has motive to undermine this, and what resources do they have?*

Move from abstract adversary to concrete actors. Build a brief threat model:

| Actor | Motive | Resources | Likely Vector |
|---|---|---|---|
| Competitor A | Market share loss | Legal team, PR budget | Regulatory challenge |
| Former partner | Grievance | Insider knowledge | Reputation damage |
| Regulator | Policy enforcement | Subpoena power | Compliance audit |
| Internal dissenter | Career threat | Access, relationships | Leak, slow sabotage |

This is not paranoia — it is preparation. The goal is not to identify every conceivable actor but to surface the two or three most credible threats. Credibility = motive × means. An actor with strong motive and no means is not a priority. An actor with even weak motive and significant means warrants attention.

**Q7.6 — Maximum Damage Leak**
*What information, if leaked, would cause the most damage?*

Information asymmetry is often the plan's most valuable asset. An adversary who removes that asymmetry can neutralize a competitive advantage, trigger a crisis, or create legal exposure. Ask:

- What do we know that we do not want known?
- What has been committed to writing that we would not want distributed?
- Who currently has access to that information?
- What controls exist if that person becomes an adversary?

The goal is not to create perfect secrecy — that is often impossible. The goal is to understand exactly where the highest-value information sits, ensure it is not casually accessible, and have a plan for what happens if it leaks anyway.

**Q7.7 — Weaponized Good Faith**
*How could someone weaponize good-faith actions against us?*

Some of the most dangerous adversarial moves exploit behavior that was genuinely well-intentioned:

- Transparency becomes evidence of admission
- Helpfulness becomes proof of capability (and therefore liability)
- Apologies become proof of fault
- Documentation becomes discovery material
- Openness becomes an invitation to bad-faith actors

This question asks you to trace a path from "we did the right thing" to "and that's now being used against us." The answer shapes communication strategy, documentation practices, and which good-faith impulses need to be filtered through legal review.

**Q7.8 — The Sophisticated Attack We Haven't Considered**
*What would a sophisticated attacker do that we haven't considered?*

This is the free-form adversarial imagination question. After running the structured questions above, remove the constraints and ask: what attack vectors have we not touched? Common categories the structured questions miss:

- **Long-game attacks**: adversaries who wait, accumulate leverage, and strike only when positioned to do maximum damage
- **Coalition attacks**: multiple actors with separate motives who align opportunistically
- **Legitimacy attacks**: using official channels (lawsuits, audits, complaints) to impose cost even without a winning case
- **Time attacks**: stalling, delay tactics, and forcing timeline slippage until conditions change
- **Dependency attacks**: targeting suppliers, partners, or infrastructure the plan depends on rather than the plan itself
- **Narrative attacks that aren't false**: criticisms that are technically accurate but framed to do maximum reputational damage

The question is not "what is most likely?" It is "what is most damaging, even if unlikely?" That is where preparation time is best spent.

---

### Domain Adaptation Matrix

| Question | Technology | Legal | Personal | Business |
|---|---|---|---|---|
| Q7.1 Weakest point | Unpatched endpoint, weak auth, unmonitored API | Procedural gap, missing statute of limitations defense, key witness availability | The relationship I haven't reinforced, the promise I made that I can't keep | Key person dependency, single customer concentration, IP not protected |
| Q7.2 Weaponization | Code comment, commit message, internal Slack export | Discovery document, deposition transcript, email chain | Private message screenshot, out-of-context quote, gift that looks like a bribe | Memo, board presentation, investor deck with wrong projection |
| Q7.3 Assumption challenge | "This scales" — disprove with load test; "This API is stable" — disprove with changelog | "This jurisdiction applies" — disprove with choice-of-law argument; "This clause means X" — disprove with competing interpretation | "They won't tell anyone" — disprove by asking who they talk to; "We still trust each other" — disprove by listing recent friction | "The market exists" — disprove with survey; "The price is right" — disprove with competitor pricing |
| Q7.4 Credibility attack | "It doesn't work at scale, and here's a benchmark"; "The architecture has this known vulnerability" | "The legal theory is novel and the precedents cited are distinguishable"; "Counsel missed this recent ruling" | "This person has a pattern of behavior I can document"; "They said X and then did Y" | "The unit economics don't work, and here's the math"; "This has been tried and here's what happened" |
| Q7.5 Actor mapping | Former employee, security researcher, nation-state APT, platform owner | Opposing party, plaintiff's bar, regulatory agency, amicus filer | Ex-partner, mutual friend with loyalty conflict, person you wronged | Competitor, former employee with equity grievance, short-seller, disgruntled customer with platform |
| Q7.6 Information leak | API keys, architecture diagram, customer data, vulnerability disclosure | Settlement terms, legal strategy memo, privileged communication | Medical/financial/relationship information, private conversations, plans not yet announced | Revenue figures, customer list, cap table, product roadmap, M&A interest |
| Q7.7 Weaponized good faith | Helpful bug disclosure becomes "you knew and didn't fix fast enough" | Voluntary compliance disclosure becomes admission of past violation | Apology becomes admission of fault in future dispute | Performance improvement plan becomes evidence of discriminatory management |
| Q7.8 Sophisticated attack | Dependency on open-source library whose maintainer is turned; supply chain compromise | Friendly jurisdiction shopping by adversary; strategic use of discovery process to impose cost | Building a relationship to gather intelligence before using it | Regulatory capture by competitor; strategic acqui-hire to disassemble team |

---

### Depth Scaling

**Mode A (compact):** Answer Q7.1 and Q7.4 only. Name the weakest point. Write the hostile narrative. Two paragraphs maximum.

**Mode B (standard):** Answer all four Standard Questions with 2-4 sentences each. Add Q7.5 (actor map, top 2-3 actors only). Total output: one page or less.

**Mode C (exhaustive):** Answer all eight questions with full analysis. Build complete actor map. Write the actual hostile press release or forum post. Run the Domain Adaptation Matrix for relevant domains. Identify which attack vectors require immediate remediation vs. monitoring vs. acceptance. Total output: no fixed limit — until coverage is complete.

---

### Anti-Patterns

**Do not create vague dread.** "Someone could hack us" or "competitors might copy this" are not adversarial analyses — they are undifferentiated worry. Every finding must be specific: who, what vector, what damage. Vague threat awareness is not preparation.

**Do not conflate Adversarial with Risk.** Risk = accidental failure. Adversarial = intentional attack by a motivated actor. This distinction is not semantic — it determines your entire response. Accidental failures are mitigated with redundancy, monitoring, and recovery plans. Adversarial attacks are mitigated with detection, deterrence, and response capacity. Mixing these produces plans that are neither.

**Do not assume all threats are external.** Insider threats are adversarial. Someone inside the organization who has access, grievance, and motive is often a higher-priority threat than an outside actor. The most damaging breaches are typically inside jobs or facilitated by insiders. Ask explicitly: who on the inside could become an adversary?

**Do not only think about technical attack vectors.** In most real situations, the most dangerous attacks are not technical:
- Reputation attacks (coordinated negative reviews, strategic media placement)
- Legal attacks (cease and desist as delay tactic, discovery as cost imposition)
- Social attacks (turning trusted relationships against the plan)
- Regulatory attacks (triggering audits, complaints, investigations)
- Narrative attacks (framing the plan as harmful even when it isn't)

**Do not present adversarial findings without recommended responses.** Identifying that "an adversary could challenge our core assumption" without suggesting how to harden that assumption leaves the council with nothing actionable. Every significant adversarial finding should carry a mitigation direction.

---

### Cross-Seat Awareness

**Adversarial vs. Risk (Seat 8):** The most important boundary in this phase. Keep it explicit. If the threat requires an intelligent actor to materialize, it belongs here. If it can happen with no one trying, it belongs in Risk. When a scenario has both dimensions — a threat that starts as adversarial and becomes systemic — note both, but anchor it in the seat where the primary driver lives.

**Adversarial feeds into Rules (Seat 4):** Adversarial findings often reveal gaps in the constraint architecture. An adversary who can exploit a loophole in the rules is telling you the rules need amendment. Pass specific rule vulnerabilities to Rules for remediation.

**Adversarial feeds into Human (Seat 6):** Adversaries exploit emotional vulnerabilities — they know when creators are tired, when teams are demoralized, when a founder is desperate. Human dynamics that look like internal friction at Seat 6 may be adversarially exacerbated. Cross-reference.

**Watch for overlap with Ethics (Seat 5):** Some adversarial defense postures raise ethical questions. Monitoring employees to detect insider threats. Pre-emptive legal action. Information asymmetry strategies. These are not automatically wrong, but they require explicit ethical clearance. Flag them for Seat 5.

---

### Solomon Handoff Format

At the end of Seat 7 analysis, produce a structured handoff:

```
SEAT 7 HANDOFF — ADVERSARIAL

Primary attack vectors identified:
1. [Most dangerous, with actor, vector, and damage estimate]
2. [Second most dangerous]
3. [Third]

Assumptions most vulnerable to challenge:
- [Assumption] — if disproved by [actor] using [method], impact is [X]

Strongest hostile narrative against this plan:
[2-4 sentences: the best version of the argument against this]

Immediate remediation required:
- [Item requiring action before proceeding]

Items to monitor (no immediate action):
- [Item]

Items accepted as known risks:
- [Item with rationale for acceptance]

Cross-seat flags:
- Rules: [specific rule gap]
- Human: [specific emotional vulnerability being exploited]
- Ethics: [any ethical tension from adversarial countermeasures]

CHEAPEST DISCONFIRMING TEST: [Action under $0 and 72h that, if it fails, falsifies the most dangerous attack vector named above. If no test can be named, this finding is downgraded to SPECULATIVE.]
```

---

## Seat 8: RISK / FRAGILITY

**Tagline:** This seat keeps you alive.
**Phase:** STRESS (Seats 7-9)
**Focus:** Accidental failure modes, downside exposure, fragility
**Core Question:** What goes wrong by accident?

---

### The Risk Mindset

Risk does not require an enemy. Systems fail. People make mistakes. Dependencies break. Markets shift. Events occur that no one planned for and no one could have prevented. This seat maps all of that.

The word "accidental" is key. Risk analysis assumes no malice, no stupidity, no negligence — just the ordinary entropy of complex systems operating under real conditions. This is different from adversarial analysis and different from poor execution. It is the baseline failure rate of things that are fundamentally sound.

The purpose of risk analysis is not to generate anxiety. It is to identify which failures are:
1. **Likely enough** to warrant mitigation now
2. **Severe enough** to warrant mitigation even if unlikely
3. **Recoverable** — with or without a plan
4. **Lethal** — they end the plan entirely if they occur

Most plans fail not because of clever adversaries but because of ordinary fragility — single points of failure, untested assumptions, dependencies that were never made explicit, and recovery plans that were never written. This seat makes fragility visible.

---

### Standard Questions (4)

**Q8.1 — Accidental Failure Inventory**
*What can go wrong without anyone trying to break it?*

This is a broad sweep. Generate a list, not a narrative. Think across categories:

- **Technical failures**: systems crash, data corrupts, integrations break, performance degrades
- **Human failures**: key person leaves, team burns out, handoff breaks, miscommunication cascades
- **External failures**: vendor goes down, regulation changes, economic conditions shift, partner fails
- **Process failures**: the system that works when everyone follows it, but doesn't when they don't
- **Timing failures**: things arrive out of sequence, dependencies don't align, windows close

Do not filter the list at this stage — generate it first, then prioritize. The question is "what can go wrong?" not "what is most likely to go wrong?" You will assess probability in Q8.3.

**Q8.2 — Worst-Case Outcome**
*What is the worst-case outcome?*

Given the failure inventory from Q8.1, identify the single worst-case scenario — not the most likely, but the most catastrophic. This is the scenario that ends the plan entirely, causes maximum damage, or creates lasting harm that cannot be undone.

Name it specifically. "The worst case is that our database gets corrupted with no backup" is useful. "Something goes terribly wrong" is not.

Once named, ask: is the worst case recoverable? Some worst cases are bad but survivable. Others are terminal. Understanding which category your worst case falls into shapes the entire risk mitigation strategy.

The worst case is not always financial. Consider:
- Reputational worst cases (permanent brand damage)
- Relational worst cases (relationships destroyed)
- Legal worst cases (personal liability, criminal exposure)
- Human worst cases (physical harm, psychological harm)
- Mission worst cases (the plan succeeds technically but produces an outcome you didn't want)

**Q8.3 — Probability Assessment**
*How likely is it?*

Do not produce false precision. Risk probability is usually assessed in ranges:

- **High**: Will probably happen at some point; expect it; plan for it as if certain
- **Medium**: Might happen; meaningful probability; monitor and prepare
- **Low**: Unlikely but possible; worth noting if high-impact
- **Negligible**: So unlikely that the cost of preparation exceeds the expected cost of occurrence

Apply this to each item in the failure inventory. The goal is a rough 2×2: probability × impact. The quadrant you want to focus on first is High probability × High impact. The quadrant you can mostly deprioritize is Low probability × Low impact.

Do not let "low probability" become an excuse to dismiss high-impact failures. A 2% chance of a catastrophic outcome is not low — it is unacceptable if the outcome is terminal and you had options to reduce that probability.

**Q8.4 — Backup Plan Inventory**
*What backup plan exists?*

For each high-priority risk (High probability or High impact), what is the response plan? Backup plans fall into categories:

- **Prevention**: change something to make the failure less likely
- **Detection**: build monitoring so you know fast if it happens
- **Containment**: limit the blast radius if it does happen
- **Recovery**: restore to normal or acceptable function after failure
- **Acceptance**: acknowledge the risk, decide not to mitigate, and document why

Not every risk needs a mitigation. Some risks are cheap to accept. But acceptance is a decision, not a default — it requires explicit reasoning. "We accept this risk because the mitigation would cost more than the expected harm" is valid. "We haven't thought about it" is not.

---

### Extended Questions (Modes B and C)

**Q8.5 — Single Points of Failure**
*What single point of failure exists? What has no redundancy?*

A single point of failure is any element whose removal or failure causes the entire system to fail. These are distinct from ordinary failure modes because they eliminate resilience — there is no fallback.

Common single points of failure in different contexts:
- **People**: the one person who knows how the system works, who holds the relationship, who has the password
- **Systems**: the one server, one vendor, one API, one compliance tool
- **Relationships**: the one customer, one partner, one supplier
- **Knowledge**: information held in one person's head, documented nowhere
- **Processes**: approval steps that only one person can authorize

For each single point of failure identified, the question is: what would it take to add redundancy? Sometimes the answer is "we can't yet" — which is an accepted risk. But name it.

**Q8.6 — Cascade Failure Mapping**
*What cascading failure is possible — one thing breaks, which triggers what else?*

Systems are connected. A failure in one component propagates. The question is not just "what breaks?" but "what does that failure cause?"

Walk a cascade:
1. [Component A] fails
2. Which causes [Component B] to malfunction
3. Which causes [Process C] to stall
4. Which means [Customer/partner D] is unserved
5. Which triggers [Response E] from [External party]
6. Which creates [Outcome F]

Cascades are dangerous because each individual link may look low-risk, but the chain creates an outcome that no single risk assessment would have predicted. The goal is to find the most dangerous cascade: the one where an ordinary, plausible failure leads to a disproportionately bad outcome through a series of predictable connections.

Once a dangerous cascade is identified, the question is: which link in the chain is cheapest to break? You do not need to prevent every failure — just interrupt the cascade before it reaches terminal state.

**Q8.7 — Low-Probability, High-Impact Planning**
*What low-probability, high-impact event haven't we planned for?*

These are the tail events — the things on the failure inventory that got marked "Low probability" but would be catastrophic if they occurred. Structured risk management has a name for this: tail risk. It is systematically underplanned because human psychology discounts low-probability events.

For this question, focus specifically on events that meet both criteria:
- The probability is genuinely low (not just "we hope this doesn't happen")
- The impact is disproportionately large — not just bad, but potentially terminal or severely damaging

Classic tail events by domain:
- **Technology**: zero-day vulnerability, complete infrastructure failure, data breach at scale
- **Legal**: ruling that voids the core legal structure, regulatory action that forces shutdown
- **Personal**: sudden incapacity or loss of a critical person, a relationship betrayal that turns a trusted ally into an adversary
- **Business**: a market condition change that makes the core value proposition obsolete, simultaneous loss of multiple key customers

The goal is not to plan for every tail event — that is impossible and paralyzing. The goal is to identify the three or four that would be most damaging, and ensure that at minimum a response protocol exists if they occur.

**Q8.8 — Detection and Recovery Time**
*How quickly would we detect a failure, and how long to recover?*

A failure you detect immediately is fundamentally different from a failure you detect days later. Silent failures are often the most dangerous because damage accumulates before anyone acts. Ask:

- What monitoring exists? What failure modes are unmonitored?
- What is the fastest path from failure occurrence to human awareness?
- Once detected, what is the minimum time to restore acceptable function?
- What is the maximum tolerable downtime or degradation before the failure becomes unacceptable?

Recovery time has a threshold. Below the threshold, it is an inconvenience. Above it, it is a crisis. Know where your threshold is. Know whether your current recovery capability is within that threshold.

---

### Domain Adaptation Matrix

| Question | Technology | Legal | Personal | Business |
|---|---|---|---|---|
| Q8.1 Failure inventory | Outage, memory leak, failed migration, dependency deprecation, cloud bill spike | Missed deadline, excluded evidence, adverse ruling, settlement pressure, witness availability | Misread emotional cues, wrong assumption about other person's commitment, external life event changes their availability | Market shift, competitor launch, key hire leaves, customer churn spike, payment delays |
| Q8.2 Worst case | Complete data loss with no recovery path, security breach that exposes customer PII | Case dismissed with prejudice, personal liability established, key contract voided | Trust destroyed in a relationship that is irreplaceable, my reputation damaged with people I need | Company runs out of runway without warning, acquisition target becomes competitor, product launch fails publicly |
| Q8.3 Probability | Load testing tells you scale risk; historical uptime tells you reliability risk; dependency age tells you obsolescence risk | Case law tells you precedent risk; judge assignment tells you procedural risk; opposing counsel quality tells you litigation risk | Relationship history tells you reliability; communication patterns tell you friction risk | Customer concentration tells you churn risk; burn rate tells you runway risk; team tenure tells you attrition risk |
| Q8.4 Backup plan | Backup systems, recovery procedures, fallback vendors, rollback capability | Alternative legal theories, backup witnesses, settlement floor, appeal path | Secondary relationships, documented agreements, third-party conflict resolution | Reserve capital, backup customers, cross-trained team members, pivot options |
| Q8.5 Single points | Solo maintainer, single cloud region, vendor with no SLA | One attorney who knows the case, one witness, one jurisdiction | One person who can mediate, one relationship that holds the structure together | One customer at 60% of revenue, one supplier with no alternative, one person who runs everything |
| Q8.6 Cascade | Auth service down → API fails → customers locked out → support overwhelmed → trust damaged | Key witness unavailable → case theory weakens → opposing motion strengthens → settlement pressure increases | Miscommunication → hurt feelings → withdrawal → accusation → escalation to others | Key employee leaves → knowledge gap → product stalls → customer trust erodes → other employees leave |
| Q8.7 Tail events | Undiscovered security vulnerability exploited at scale, core open-source dependency abandoned | Retroactive regulatory interpretation that voids years of compliance | Core trusted person becomes unavailable, hostile, or incapacitated | Sudden market obsolescence (new technology makes product irrelevant), macroeconomic shock freezing capital |
| Q8.8 Detection/recovery | Monitoring coverage, alerting latency, on-call rotation, mean time to recovery | Docketing systems, co-counsel backup, attorney of record substitution timeline | Communication frequency, check-ins, shared documentation of decisions | Financial dashboard frequency, customer health scoring, employee exit interview signals |

---

### Depth Scaling

**Mode A (compact):** Answer Q8.1 (list only, no analysis), Q8.2 (one sentence on worst case), and Q8.4 (one sentence on each high-priority item: backup exists or "none — accepted"). No cascade analysis.

**Mode B (standard):** All four standard questions with 3-5 sentences each. Include Q8.5 (name single points of failure). Use the probability × impact framework explicitly to sort the Q8.1 inventory. One page maximum.

**Mode C (exhaustive):** All eight questions with full analysis. Build a risk register: each failure mode gets probability rating, impact rating, detection time estimate, recovery time estimate, and mitigation status. Walk at least one full cascade. Identify all tail events and give each a stated response protocol. No fixed length — until the register is complete.

---

### Anti-Patterns

**Do not generate exhaustive lists without prioritization.** A list of 40 things that could go wrong is less useful than 5 things that will probably go wrong and 3 things that would be catastrophic if they did. Always filter by probability × impact.

**Do not confuse Risk with Adversarial.** This is the mirror image of the anti-pattern in Seat 7. Risk is about entropy, not malice. If the failure requires someone to intend it, it belongs in Seat 7. Keeping this distinction means keeping your mitigation strategies correctly targeted.

**Do not conflate probability and impact.** A high-probability, low-impact risk is an irritant. A low-probability, high-impact risk is an existential threat. They require different treatments and different urgency. Never collapse these two dimensions into a single "how bad is this?" judgment without separating them first.

**Do not skip backup plan generation.** Risk identification without mitigation is just worry. Every finding from Q8.1 that survives the probability × impact filter must be addressed in Q8.4. If you don't have a backup plan and won't create one, that is an accepted risk — say so explicitly, with reasoning.

**Do not treat recovery as binary.** Recovery is not "we're fine" or "we're done." Most recovery scenarios involve partial function, degraded service, or temporary alternatives. Ask: what does partial recovery look like? What is the acceptable degraded state while full recovery is in progress? Planning for the gradient is often more useful than planning for the endpoint.

**Do not forget the human dimension of recovery.** Technical systems can often be restored quickly. Human trust, team morale, partner relationships, and organizational confidence take much longer to recover. Factor this into recovery time estimates.

---

### Cross-Seat Awareness

**Risk vs. Adversarial (Seat 7):** See Seat 7 cross-seat notes. Maintain the boundary rigorously. Use the test: "Does this failure require someone to intend it?" If yes, Seat 7. If no, Seat 8.

**Risk feeds into Resource (Seat 9):** Risk mitigation costs resources. Backup systems cost money. Redundancy costs time to build and maintain. Monitoring costs attention. When Seat 9 assesses resources, it must account for the cost of the risk mitigations that Seat 8 identified as necessary. A plan that is resource-efficient but fragile is not actually efficient — it is deferring costs to the moment of failure.

**Risk feeds into Execution (Seats 10-12 in ELEVATE/EXECUTE phases):** Plans that come out of STRESS with identified failure modes need those failure modes built into execution plans. A plan that doesn't account for its own failure modes will fail in execution.

**Watch for overlap with Systems (Seat 3):** Systems analysis (in GROUND) asks why things are structured the way they are and where the structural flaws lie. Risk asks what specifically breaks and what the consequences are. The two are complementary — Systems gives you the structural diagnosis, Risk gives you the failure inventory. If GROUND identified systemic tensions, those tensions are candidate items for the Risk failure inventory.

---

### Solomon Handoff Format

```
SEAT 8 HANDOFF — RISK / FRAGILITY

Failure mode inventory (prioritized):
HIGH probability × HIGH impact:
- [Item with brief description]

HIGH probability × LOW impact (monitor):
- [Item]

LOW probability × HIGH impact (tail risk):
- [Item with response protocol]

Worst-case scenario:
[Specific description — terminal or recoverable?]

Single points of failure requiring immediate attention:
- [Item: what it is, what adding redundancy would require]

Dangerous cascade identified:
[Walk the chain: A → B → C → terminal state]

Backup plan status:
- [Risk item]: [Mitigation status: mitigated / partially mitigated / accepted / unaddressed]

Detection and recovery gaps:
- [Failure mode with no monitoring]
- [Recovery time exceeding acceptable threshold]

Cross-seat flags:
- Resource: [risk mitigations that require resource allocation]
- Execution: [failure modes that must be built into execution plans]

CHEAPEST DETECTION PROBE: [Action under $0 and 72h that surfaces the highest-impact unmitigated risk if it is real — e.g., grep logs for prior occurrences, check monitoring coverage, ask one person who would have noticed.]
```

---

## Seat 9: RESOURCE / TRADEOFF

**Tagline:** This seat protects resources.
**Phase:** STRESS (Seats 7-9)
**Focus:** Cost, value, efficiency, scarcity, and opportunity cost
**Core Question:** What does this cost, including what we give up?

---

### The Resource Mindset

Every decision consumes resources. Some of that consumption is visible — money paid, hours spent, effort expended. Most of it is invisible — time that didn't go elsewhere, attention that wasn't available for other things, energy that wasn't banked for future needs, opportunities foreclosed by the choice to move in this direction.

This seat insists on the full accounting.

The most common failure of resource analysis is counting direct costs and ignoring opportunity cost. "This will cost $50,000" is half an analysis. The complete analysis is: "This will cost $50,000 and 4 months of engineering time, which means we cannot also build the adjacent feature that was our second priority, which means our competitor will launch that feature first, which costs us market position worth an estimated $X." That is the resource analysis.

There is a second failure mode: counting financial resources and ignoring non-financial ones. For most individuals and many teams:
- **Attention** is more scarce than money
- **Energy** is more scarce than time
- **Reputation** is more scarce than capital, because it cannot be purchased once lost
- **Relationships** are more scarce than any of the above, and the hardest to rebuild

This seat requires the council to name all of these, not just the financial ones.

---

### Standard Questions (4)

**Q9.1 — Full Cost Inventory**
*What will this cost in money, time, attention, reputation, and energy?*

Build the complete cost register. Do not stop at the obvious categories. Work through each dimension:

**Money (direct financial cost):**
- Initial investment or expenditure
- Recurring costs (maintenance, subscriptions, salaries, infrastructure)
- Hidden financial costs (the things not in the first estimate: integration costs, support costs, technical debt accumulation)
- Cost escalation risk: under what conditions does the baseline cost double?

**Time:**
- Calendar time to implement (weeks, months, years)
- Person-hours required
- Time to value: when does the investment begin returning something?
- Time costs that don't show up on a timesheet: decision fatigue, context-switching overhead, coordination time

**Attention:**
- Whose attention, and how much of it?
- What happens to that person's other responsibilities during this?
- Attention is zero-sum — if it goes here, it doesn't go elsewhere. Name where it isn't going.
- Cognitive load: does this add persistent background complexity to the mental landscape of key people?

**Reputation:**
- Is there any reputational risk in being associated with this?
- Is there reputational cost to the people who implement it (putting their name on it)?
- Is there reputational cost in the commitment itself — "we said we'd do this, and we haven't" (commitment-then-failure cost)?

**Energy (personal and team):**
- Is this energizing or draining for the people who will do it?
- Is the team/individual currently running low on energy reserves? Can they absorb this?
- What is the cost of sustained effort: burnout risk, relationship stress, reduced capacity elsewhere

**Q9.2 — Return Assessment**
*What is the return?*

The cost analysis from Q9.1 is only meaningful relative to what it produces. Map the return:

- **Financial return**: revenue generated, cost saved, loss prevented
- **Strategic return**: market position, competitive advantage, optionality created
- **Relational return**: relationships built or strengthened, trust established
- **Knowledge return**: capabilities built, insights gained, learning accumulated
- **Options return**: what does success make possible that wasn't possible before?
- **Risk reduction return**: what risks does this eliminate or reduce?

Return must be assessed on the same timeline as cost. A large financial return in year three is not equivalent to a large financial return in year one — the intervening cost must be sustained. Ask: can we afford to sustain the cost until the return materializes?

**Q9.3 — Sustainability Assessment**
*What can we sustain?*

Cost and return only matter within the bounds of what can actually be sustained. A high-return investment that requires more cash than exists is not viable, regardless of its quality. Ask:

- At what resource level does the plan become untenable?
- What is the minimum viable resource commitment that still delivers meaningful return?
- If resources run lower than expected, what is the triage order — what gets cut first, second, last?
- What is the runway? At the current burn rate, when do resources run out?
- Is there a resource cliff: a point at which declining resources suddenly trigger non-linear failure rather than linear degradation?

Sustainability is also about non-financial resources. Sustained effort from a burned-out team is not sustainable regardless of funding. A plan that requires the founder's constant personal attention is not sustainable if that person gets sick. Ask: what happens if the primary resource — financial, human, attentional, relational — is cut by 30%? By 50%? What is the breaking point?

**Q9.4 — Opportunity Cost**
*What are we giving up by choosing this path?*

This is the most important question in Seat 9, and the one most likely to be skipped.

Every yes contains a thousand nos. Choosing this path means not choosing other paths. The question is: which paths are we foreclosing, and what is the value of what we're giving up?

Opportunity cost is real cost, even though it never appears on a balance sheet. It is the return we would have received from the alternative we didn't choose. If those alternatives were good ones, opportunity cost may be the single largest cost of this decision.

To assess opportunity cost:
1. Name the specific alternatives that exist right now (not hypothetical alternatives — real ones)
2. Assess what each alternative would produce
3. Identify which alternative, if not pursued, represents the largest foregone value
4. Compare that to the return from Q9.2

If the best alternative produces more value than this plan, the resource analysis returns a negative answer: it is a better use of resources to do the other thing.

Opportunity cost also applies to non-financial resources. The person whose attention this consumes cannot give that same attention to relationships, health, other projects, or recovery. What are those things worth?

---

### Extended Questions (Modes B and C)

**Q9.5 — Opportunity Cost Depth Analysis**
*What is the opportunity cost — what could we do instead with these resources?*

This builds directly on Q9.4 but requires making the alternatives concrete and comparable. Do not stop at "we could do other things." Name them:

- What are the top 2-3 alternatives that use similar resources?
- For each: what is the expected return, the risk profile, and the timeline to value?
- What is the relative attractiveness of this plan vs. each alternative?
- Are any of the alternatives strictly better across all dimensions, or do the tradeoffs differ?

The goal is a clear comparison table. Not to produce paralysis, but to ensure that the choice to proceed with this plan is a genuine decision, not just the first option on the table.

**Q9.6 — Hidden Costs**
*What hidden costs exist that aren't in the initial estimate?*

Initial estimates are almost always wrong on the low side. This is not fraud — it is structural. Hidden costs include:

**Downstream maintenance:** What does it cost to operate, maintain, and keep current what we're about to build or do? One-time build cost is usually a small fraction of lifetime maintenance cost.

**Integration and coordination costs:** Every new thing that connects to existing things creates interface maintenance. Someone has to manage the seam. That cost is rarely in the estimate.

**Learning curve and transition costs:** The time it takes people to become competent with the new thing, and the lost productivity during that transition, is a real cost that is almost never estimated correctly.

**Compliance and governance costs:** Regulatory compliance, legal review, documentation requirements, audit trails — these add cost that grows as the plan scales.

**Technical debt in non-technical contexts:** Every shortcut taken for speed is borrowed time. What shortcuts are we taking, and what will it cost to repay them?

**Reversibility costs:** If this doesn't work and we want to undo it, what does undoing it cost? Sunk costs are non-recoverable. Some choices are much harder to reverse than they look going in.

**Attention drag:** Once this is running, it requires ongoing attention to maintain. Even if no one is actively working on it, it occupies cognitive space. That is a cost that persists until the thing is either complete or shut down.

**Q9.7 — Diminishing Returns**
*At what point do diminishing returns kick in?*

More resources do not produce proportionally more return past a certain threshold. This question forces clarity on the inflection point:

- Where is the point of maximum efficiency — the resource level beyond which additional investment produces disproportionately less value?
- What happens to quality and output between "minimum viable" and "maximum effort" resource levels?
- Are we currently planning to operate in the zone of diminishing returns?
- If we had half the resources, what would we cut first, and how much return would we lose?

The diminishing returns question also applies to time. Past a certain duration, sustained effort on one thing produces less incremental progress per unit of effort — because of cognitive saturation, loss of external fresh perspective, and the compounding effect of sustained attention on narrow problems. When is the diminishing returns threshold on time and attention?

**Q9.8 — Renewable vs. Finite Resources**
*What resources are renewable vs. finite — and are we spending the right ones?*

Not all resources are equal in their replenishability:

- **Money** can often be raised or earned — renewable under the right conditions, but finite in the short run
- **Time** is strictly finite — no one gets more hours than they spend
- **Energy** is partially renewable but has a ceiling and degrades under sustained overload
- **Relationships and trust** are long-cycle renewable — they can be built over time, but once damaged, recovery is slow and uncertain
- **Reputation** is similar to relationships but with greater leverage: a well-established reputation opens doors; a damaged one closes them for extended periods
- **Attention** can be partially restored through rest and reduced cognitive load, but is a highly finite daily resource

The question is whether the plan spends the right resources. If the plan requires heavy expenditure of finite, irreplaceable resources (specific relationships, personal health, reputational capital built over years) for returns that are meaningful but not proportional, this is a resource warning.

A plan that spends renewable resources to build renewable or expanding assets is sound. A plan that liquidates finite assets for uncertain returns is structurally concerning regardless of the expected value calculation.

---

### Domain Adaptation Matrix

| Question | Technology | Legal | Personal | Business |
|---|---|---|---|---|
| Q9.1 Full cost | Engineer-hours, infra cost, vendor fees, tech debt accumulation, maintenance burden, team opportunity cost | Attorney fees, filing fees, discovery costs, management time, expert witness fees, reputational exposure, settlement reserves | Emotional energy, time in conflict resolution, relationship credit spent, cognitive bandwidth, financial cost of outcomes | Capital deployed, headcount cost, customer acquisition cost, marketing spend, leadership attention, opportunity cost vs. alternatives |
| Q9.2 Return | Feature value, revenue impact, cost reduction, competitive position, technical optionality, engineering capability built | Case outcome value, precedent established, avoided liability, settlement vs. award delta, deterrence of future suits | Resolution value, relationship restored or improved, clarity achieved, emotional load reduced, precedent for future interactions | Revenue growth, margin improvement, market share gained, talent retained, strategic position improved |
| Q9.3 Sustainability | Can the team maintain this at current velocity without burning out? Is the infra cost sustainable at current growth? | Can we sustain litigation costs until resolution? At what point do we run out of legal budget and must settle? | Can I sustain this level of emotional investment? What happens if this takes 3x as long as expected? | At current burn rate, what's the runway? What's the resource floor for maintaining the business while pursuing this? |
| Q9.4 Opportunity cost | What features are we not building? What tech debt is not being paid? What team capabilities are not being developed? | Could settlement be reached for less than litigation cost, preserving resources for other priorities? | What relationships am I not investing in? What opportunities am I not available for? What am I not doing with this time? | What market opportunities are we not pursuing? What product investments are on hold? What hires are we not making? |
| Q9.5 Opportunity cost depth | Build vs. buy analysis; "build this" vs. "build the next most valuable thing" with full return comparison | Litigate vs. settle vs. restructure comparison with full economic and reputational analysis | "Pursue this" vs. "invest elsewhere" with explicit naming of what "elsewhere" means and what it would produce | Strategic alternatives map: build vs. partner vs. acquire vs. pivot — each with resource profile and expected return |
| Q9.6 Hidden costs | Code maintenance (often 3-5x initial build cost over lifetime), onboarding new engineers to the codebase, security monitoring, incident response | Discovery is usually the largest cost and is unpredictable; deposition prep; expert fees; appellate reserve | Emotional spillover to other relationships; reduced capacity for other commitments; health impacts of sustained stress | Customer success overhead as product scales; regulatory compliance as revenue triggers thresholds; management tax of team growth |
| Q9.7 Diminishing returns | After core feature is built, each additional 10% of polish costs disproportionate time; second engineer often less than half as productive as first on same task | Past a certain investment level in litigation, incremental legal effort produces diminishing case improvement; recognize the "good enough to settle" threshold | Past a certain level of effort in relationship repair, additional effort can backfire — giving space is sometimes more effective than continued investment | Marketing spend has diminishing returns curves; headcount has a coordination tax that increases non-linearly; product surface area grows maintenance cost faster than feature value |
| Q9.8 Renewable vs. finite | Engineering time is a scarce resource with high renewal cost (hiring); infra cost is renewable with cash; technical debt is a finite drag on future velocity | Attorney time is renewable with money; client executive attention is finite; credibility with the court is long-cycle renewable | Personal energy and health are partially renewable but can be permanently damaged; trust in a relationship is slow to rebuild; time is strictly finite | Market timing windows are finite (first-mover advantage); founder energy is finite; brand equity is long-cycle; capital is renewable under the right conditions |

---

### Depth Scaling

**Mode A (compact):** Answer Q9.1 (one sentence per cost category), Q9.2 (return in one sentence), and Q9.4 (name the top alternative and what it would produce). Skip hidden costs, diminishing returns, and full opportunity cost analysis.

**Mode B (standard):** All four standard questions with 3-5 sentences each. Include Q9.6 (hidden costs, 2-3 items). Include explicit comparison of this plan vs. one primary alternative (Q9.5). One to two pages.

**Mode C (exhaustive):** All eight questions with full analysis. Build a complete resource ledger: every cost category, full opportunity cost comparison with at least two alternatives, hidden cost inventory, sustainability model with breaking point identified, diminishing returns curve at least estimated qualitatively, and explicit assessment of renewable vs. finite resource expenditure. No fixed length — until the ledger is complete.

---

### Anti-Patterns

**Do not count only money.** Financial cost is the easiest to quantify and the most commonly over-weighted. A plan that costs very little money but consumes six months of a key person's attention may be the most expensive decision that person makes this year. Time, attention, energy, relationships, and reputation are all resources and must be counted.

**Do not skip opportunity cost.** This is the single most commonly omitted element of resource analysis. "This costs $50K" is incomplete. "This costs $50K and forecloses the alternative that would have produced $200K" is the real analysis. Opportunity cost is not optional in Mode B or C. Name the alternatives, estimate their value, and make the comparison explicit.

**Do not present costs without context.** Raw numbers are meaningless without a reference frame. "$10K" might be trivial in one context and fatal in another. Always state cost relative to: total available resources, return on investment, and the cost of the best alternative.

**Do not assume more resources produce proportionally better outcomes.** Past the point of diminishing returns, additional investment produces declining incremental value. Identify that threshold and verify that the plan is not operating above it. Over-resourcing a project is a resource error just as under-resourcing is.

**Do not ignore the cost of reversibility.** Some commitments are easy to undo. Others lock you in permanently. The harder a decision is to reverse, the higher its effective cost — because if you're wrong, the cost of being wrong is compounded by the cost of the exit. Factor reversibility into cost estimates.

**Do not treat attention as free.** For individuals, attention is often the binding constraint. A person who has committed their attention to this project cannot give that attention elsewhere. The question "is this the best use of my attention right now, compared to everything else competing for it?" is a resource question, and it must be asked.

**Do not conflate cost efficiency with value efficiency.** A plan that is cheap may produce very little. A plan that is expensive may produce extraordinary return. The resource question is not "how cheap can we make this?" but "what is the most return per unit of scarce resource expended, compared to alternatives?"

---

### Cross-Seat Awareness

**Resource feeds into Execution (downstream phases):** Resource availability determines what execution plans are actually feasible. A plan that is strategically sound but requires resources that don't exist is not a plan — it is a wish. The resource analysis here must be handed forward to execution planning so that execution plans are built within real constraints, not assumed ones.

**Resource feeds into Solomon (Seat 12):** When the council reaches Solomon, one of the most common challenges is navigating between ethical ideals and practical constraints. Resource analysis provides Solomon with the honest accounting of what is actually affordable. An ethically ideal solution that is not resourceable is not a real option — it is a standard, not a choice.

**Watch for overlap with Risk (Seat 8):** Some risks are disguised resource problems. "We can't afford to lose this customer" is a resource dependency risk. "We have no budget for compliance work" is a resource gap that creates regulatory risk. Items that appeared in the Risk register may reappear here as resource allocation questions.

**Watch for overlap with Rules (Seat 4):** Some constraints that were framed as rules ("we can't do that") are actually resource constraints ("we can't afford to do that right now"). Seat 9 may clarify which "rule" constraints are genuinely binding vs. temporarily binding based on resource availability. This distinction changes the remediation strategy.

---

### Solomon Handoff Format

```
SEAT 9 HANDOFF — RESOURCE / TRADEOFF

Full cost inventory:
- Money: [direct cost / estimated total lifecycle cost]
- Time: [calendar time / person-hours]
- Attention: [whose, how much, what it displaces]
- Energy: [assessment of team/individual capacity]
- Reputation: [any reputational cost or risk]

Return assessment:
- Primary return: [what this produces]
- Timeline to value: [when return materializes]
- Can we sustain the cost until return materializes: [yes/no/uncertain with reasoning]

Sustainability floor:
- Resource minimum: [minimum viable resource level]
- Breaking point: [at what resource level does this become untenable]
- Runway estimate: [at current burn, time until resources exhausted]

Opportunity cost:
- Top foregone alternative: [name it, estimate its value]
- Second foregone alternative: [name it]
- Net resource verdict: [is this the best use of these resources compared to alternatives?]

Hidden costs identified:
- [Item]: [estimated impact]
- [Item]: [estimated impact]

Diminishing returns threshold:
- [At what investment level does additional resource produce declining return]

Renewable vs. finite resource flags:
- Finite resources being consumed: [list]
- Risk level: [acceptable / concerning / potentially irreversible]

Cross-seat flags:
- Risk: [resource gaps that create risk]
- Execution: [resource constraints that shape feasible execution options]
- Solomon: [resource limitations relevant to ethical ideal vs. practical choice]

CHEAPEST OPPORTUNITY-COST CHECK: [Action under $0 and 72h that reveals whether resources committed here would yield more elsewhere — e.g., list the top 3 forgone alternatives and ask if any one dominates, name the next-best use of the same week of attention.]
```

---

## STRESS Domain Examples — Cheapest $0/72h Actions

The CHEAPEST DISCONFIRMING TEST (Seat 7), CHEAPEST DETECTION PROBE (Seat 8), and CHEAPEST OPPORTUNITY-COST CHECK (Seat 9) requirements above adapt to domain. Examples by domain:

### Tech
- **Seat 7 disconfirming test:** Run the failing edge-case input in REPL. Send a single curl with the suspect payload. Check the platform's security advisory feed for the named CVE pattern.
- **Seat 8 detection probe:** Grep logs for the precondition's prior occurrences in last 30 days. Check monitoring coverage on the suspect failure mode — is there any alert that would fire?
- **Seat 9 opportunity-cost check:** Check git blame on the module being rewritten — did the last rewrite stick or get re-rewritten? Ask which other PR would close this sprint if this work were dropped.

### Legal
- **Seat 7 disconfirming test:** Read the controlling statute's plain text without commentary. Search the jurisdiction's published enforcement actions from the last 24 months for analogous fact patterns.
- **Seat 8 detection probe:** Search court docket for the opposing party's filing pattern. Check whether the deadline you're computing is in business days vs calendar days per local rules.
- **Seat 9 opportunity-cost check:** Ask whether the same hour spent on settlement negotiation has higher EV than the same hour spent on litigation prep. Estimate fee recovery probability vs. expected award.

### Personal / Career
- **Seat 7 disconfirming test:** Send one informational-interview message to someone who took the path 2 years ago and ask what they would undo. Search public reviews/complaints about the company, role, or decision pattern.
- **Seat 8 detection probe:** Write the resignation/acceptance email and let it sit 48 hours unsent — detects regret signal. Ask one trusted person what they would worry about that you haven't said.
- **Seat 9 opportunity-cost check:** List the next 3 alternatives forgone and ask whether any one dominates. Ask what you would do this week if this decision were already made — does that life look like the one you want?

### Business
- **Seat 7 disconfirming test:** Post the offer to a free channel (organic social, single email to warm list) for 24 hours and measure click-through. Search competitor complaints/refund threads for the closest analog.
- **Seat 8 detection probe:** Pull last 90 days of customer churn reasons — does the suspect risk pattern show up? Ask one frontline employee what they have been seeing that leadership has not been told.
- **Seat 9 opportunity-cost check:** Name the next-best use of the same week of founder time. Compare unit economics of this initiative against the best forgone initiative in the same time window.

These examples are illustrative, not exhaustive. The discipline is: every STRESS finding must close with a real-world action the user can take this week, with no spend, that produces real evidence about the finding. Worry without a test is not analysis.

---

## Phase Summary: STRESS Complete

### What the Three Seats Collectively Establish

After Seats 7, 8, and 9, the council has:

1. **A threat map** (Seat 7): Who could attack this, how, and where the vulnerabilities are. The plan has been subjected to red-team analysis with specific attack vectors named, assumptions hardened, and narrative attacks drafted.

2. **A fragility map** (Seat 8): What breaks by accident, what the worst case is, where the single points of failure live, and what the plan for detection and recovery is. The plan has been stress-tested against ordinary entropy.

3. **A resource accounting** (Seat 9): What this truly costs across all resource dimensions, what the return is, whether it is sustainable, and what we are giving up by choosing this path over alternatives. The plan has been evaluated not just on its own terms but in comparison to the best competing use of these resources.

### What a Plan That Survives STRESS Has Demonstrated

A plan that passes all three seats has shown that:
- It can withstand intelligent, motivated opposition
- It can survive ordinary failure without catastrophic consequence
- It is a defensible use of scarce resources compared to real alternatives

This does not make the plan correct — ELEVATE (Seats 10-12) will challenge assumptions about what options exist and whether better ones are being overlooked. But it means the plan is not naive, not fragile, and not a misuse of resources. It has earned the right to be evaluated on its merits.

### How STRESS Failures Are Handled

If a plan fails badly at any STRESS seat, the council has options:

- **Remediate and re-run**: fix the identified weakness and re-run the affected seat before proceeding
- **Scope reduction**: reduce the plan's scope to eliminate the fragile element, then re-run
- **Conditions on proceed**: document the specific conditions that must be met before the plan can safely proceed
- **Kill**: some plans fail STRESS because they are fundamentally unsound and the failure cannot be remediated within the plan's premises — in those cases, the council's job is to say so clearly and redirect resources

Solomon will be given the complete STRESS output when synthesizing a final verdict. Plans that failed STRESS seats but were conditionally approved will carry those conditions forward into Solomon's synthesis.

---

> **STRESS complete.** The plan has been pressure-tested — we know how it could be attacked, what breaks by accident, and what it truly costs. The Council now moves to ELEVATE to expand options: what can actually be done, who else is affected, and what better option exists that we haven't seen.
