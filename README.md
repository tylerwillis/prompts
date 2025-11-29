# Prompts

A collection of LLM prompts by Tyler Willis.

---

## Deck Review

> Get a thorough critique of a presentation deck using best practices from consulting, investor pitches, and sales decks.

**Models:** Tested on Claude Opus 4.5 and GPT-5.1 Pro. Both deliver strong results and should be considered somewhat interchangable. I prefer Opus for speed, but would consider running both if I wanted comprehensive review notes.

**Usage:** Attach your deck (PDF or images) along with this prompt.

<details>
<summary>View prompt</summary>

```
Critique the attached deck using the following principles. When you give me feedback, assume that I'm not familiar with these principles and that I no longer have access to this document, so you likely have to explain the concepts to me in your feedback instead of just referencing them.

# Presentation Mastery: A Complete Ruleset

A unified guide for creating high-impact presentations—consulting decks, pitch decks, sales presentations, and internal communications.

---

## How to Use This Document

**Before building slides:** Complete Phase 1 (Pre-Work)—this determines everything else.

**While building:** Reference Phase 2 (Core Principles) and Phase 3 (Slide Construction).

**For specific deck types:** See Phase 4 for tailored rules.

**Before finalizing:** Run the Validation Checklist in Phase 5.

---

## Phase 1: Pre-Work (Complete Before Any Slides)

The quality of your deck is determined before you open your presentation software. Skip this phase, and no amount of polish will save you.

### 1.1 Define the Audience

Answer these questions explicitly:

| Question | Why It Matters |
|----------|----------------|
| **Who are they?** | Determines baseline knowledge and language |
| **What do they already know?** | Never explain what they know; never assume what they don't |
| **What do they care about?** | Same content, different framing for different audiences |
| **What's their default skepticism?** | Determines your evidence burden |
| **Who's the real decision-maker?** | In groups, structure for the person whose opinion matters most |

> **Example:** A Series A pitch to a healthcare-focused VC can skip "healthcare is a large market." A pitch to a generalist fund cannot.

### 1.2 Define the Objective

**The ONE takeaway:** If they remember nothing else, what must stick? Write it as a single sentence. If you can't, you don't have clarity yet.

> **Weak:** "Our company is doing interesting things in AI."

> **Strong:** "We've built the only AI solution that reduces insurance claim processing time by 80% while improving accuracy."

**The desired action:** What do you want them to *do* after this presentation?

> **Examples:** "Approve the $2M budget" / "Schedule a technical follow-up" / "Sign the LOI this quarter"

**The mindset shift:** What belief are you changing?

> **From:** "This market is too risky."

> **To:** "The risk is managed, and the opportunity is urgent."

### 1.3 Know Your Delivery Format

The format fundamentally changes how you build.

| Format | Word Density | Visual Emphasis | Standalone Clarity |
|--------|--------------|-----------------|-------------------|
| **Live presentation** | Low (25–50 words) | High—visuals carry message | Low—you provide context |
| **Read-ahead / Email** | Moderate (75–100 words) | Moderate—supports text | High—must stand alone |
| **Hybrid** | Moderate with appendix | High in main, detailed in backup | Must work both ways |

**The "Read Alone Test":** If you leave the room, can the reader understand the slide 100% on their own? Read-aheads must pass this test.

**Critical:** Pitch decks are frequently forwarded internally at firms. The partner you present to shares it with others who weren't in the room. Build for standalone clarity.

### 1.4 Know Your Time Constraint

**Rule of thumb:** 1–2 minutes per slide for presented decks.

**Back-time from Q&A:** A 30-minute meeting with no Q&A is a monologue, not a conversation.

> **Example:** 45-minute meeting → 15 minutes for Q&A → 30 minutes of presentation → 15 slides maximum.

### 1.5 Anticipate Objections

If you can't name the top 3 objections your audience will have, you don't know your audience well enough.

For each objection, decide:
- Address proactively in the main flow?
- Prepare a backup slide?
- Handle verbally if raised?

### 1.6 Design the Emotional Journey

Logic gets consideration. Emotion gets action. Great decks need both.

**How should they feel at start vs. end?**

> **Pitch deck:** Curious → Excited → Confident → Urgent

> **Consulting deck:** Concerned → Understood → Relieved → Aligned

**Earned vs. Manufactured Emotion**

There's a critical difference:
- **Earned emotion:** The evidence genuinely warrants the reaction
- **Manufactured emotion:** The content doesn't support the claim

> **Manufactured:** Title says "A catastrophic failure in customer service" but the stat is "average hold time increased to 4 minutes." Longer holds are annoying, not catastrophic.

> **Earned:** Title says "Customer churn has reached emergency levels" supported by "38% of customers churned in Q2; $4.2M monthly revenue lost to competitors."

Sophisticated readers—investors, executives—feel manipulated when emotion is manufactured. They've seen hundreds of decks.

---

## Phase 2: Core Principles (Universal Rules)

These apply to every deck, regardless of type.

### 2.1 The Storyline Test

**Read only your slide titles in sequence. They must form a coherent, persuasive argument.**

If someone can't understand your recommendation from titles alone, the deck fails. This is the single most important test.

> **Failing the test:**
> 1. Introduction
> 2. Market Overview
> 3. Our Solution
> 4. Team
> 5. Ask
>
> *These are labels, not a story.*

> **Passing the test:**
> 1. Enterprise security teams waste 40% of time on false positives
> 2. Existing solutions trade accuracy for speed—teams must choose
> 3. Our AI triages alerts with 95% accuracy in real-time
> 4. Three enterprise pilots reduced alert fatigue by 60%
> 5. We'll reach $15M ARR and profitability in 18 months
>
> *Now you understand the pitch without seeing a single slide body.*

**How to do this:**
1. Write slide titles first—before any content
2. Read them aloud in sequence
3. Ask: "Does this flow logically? Is there a narrative arc?"
4. Revise until titles alone tell your story

**Redundancy check:** If two titles make essentially the same point, you have one slide too many.

### 2.2 Pyramid Structure

Structure from the top down: answer first, then evidence.

```
                    [Governing Thought]
                    Your main conclusion
                           ↓
        ┌──────────────────┼──────────────────┐
        ↓                  ↓                  ↓
   [Key Argument 1]   [Key Argument 2]   [Key Argument 3]
        ↓                  ↓                  ↓
   [Evidence]         [Evidence]         [Evidence]
```

**The Governing Thought** is your single most important conclusion—appears in your executive summary and is restated at the end. (This is the same as the "ONE takeaway" from Phase 1.)

**The Executive Summary** is broader: it contains the governing thought plus the 2–4 key arguments that support it, plus your recommendation. It's a summary of the entire deck's argument, not just the conclusion.

**Key Arguments** (2–4, typically 3) are the main reasons your governing thought is true.

> **Example (Consulting):**
> - **Governing thought:** "Consolidate from 5 distribution centers to 3 to save $40M annually"
> - **Key argument 1:** "Current network has 35% redundant capacity"
> - **Key argument 2:** "Three-hub model serves 95% of customers within 2-day shipping"
> - **Key argument 3:** "Transition completes in 18 months with minimal disruption"

### 2.3 One Message Per Slide

Every slide answers one question. The title states the answer. The body proves it.

**The test:** Can you summarize the slide in one sentence without using "and"?

> **Failing:** "This slide shows our market opportunity and competitive landscape and go-to-market strategy." → This is three slides.

> **Passing:** "This slide shows we've captured 15% of our target segment in 12 months." → One clear message.

**Common violations:**
- Two charts showing different things
- A chart plus an unrelated bullet list
- The phrase "In addition..." appearing anywhere

### 2.4 Takeaway Titles, Not Labels

Slide titles must be complete sentences stating conclusions—not labels describing content.

**And the body must prove what the title claims.**

| Label (Weak) | Takeaway (Strong) |
|--------------|-------------------|
| Market Overview | The $50B security market is consolidating around AI-native solutions |
| Q3 Results | Q3 revenue grew 24% driven by enterprise expansion |
| Competitive Landscape | We're the only solution combining real-time detection with automated response |
| Team | Our team built the fraud detection systems at Stripe and Square |

**Critical: The slide body must prove the title.**

A takeaway title is a claim. Claims require evidence.

> **Example (title not supported):**
> - Title: "Warehouse teams are collapsing under impossible workloads"
> - Content: "200+ picks per hour targets, 12-hour shifts during peak"
>
> *"Collapsing" implies breakdown—turnover data, injury rates, burnout testimonials. The content shows strain, not collapse.*

> **Example (title supported):**
> - Title: "Warehouse worker burnout has reached crisis levels"
> - Content: "52% turnover rate (vs. 25% industry average), 280% increase in injury claims"

### 2.5 Evidence Standards

Every claim requires visible support. "Trust me" is not a source.

| Claim Type | Evidence Required |
|------------|-------------------|
| Market size | Third-party source (Gartner, industry report) |
| Growth rate | Your data with methodology note |
| Customer outcomes | Specific metrics with attribution |
| Technical performance | Test results, benchmarks |
| Competitive comparison | Feature-by-feature with source |

**Every statistic needs a source.** Unsourced statistics read as made up—even when accurate.

> **Weak:** "Customers love our product."

> **Strong:** "NPS of 72 across 150 enterprise customers, vs. industry average of 35."

### 2.6 Clarity Over Impression

**Confusion is the enemy.** Never use abstract language when concrete language exists.

| Abstract (Weak) | Concrete (Strong) |
|-----------------|-------------------|
| "Mechanics of engagement" | "How users actually interact with the product" |
| "Orchestration layer" | "Coordination system" |
| "Intelligence compounds" | "The system gets smarter with use" |
| "Dynamic resource allocation" | "Automatically assign tickets to available reps" |

**The jargon test:** Read each slide aloud. If you'd never say it in conversation, don't write it in a deck.

**Dressed-up language signals insecurity.** When founders use inflated language, investors assume they're compensating for weak substance.

---

## Phase 3: Slide Construction

Rules for building individual slides.

### 3.1 The 3-Second Rule

The audience should grasp the slide's point within 3 seconds. If they're still parsing the layout, redesign.

**Test:**
1. Show the slide to someone unfamiliar with it
2. After 3 seconds, hide it
3. Ask: "What was that slide about?"
4. If they can't answer, simplify

### 3.2 Text Density by Format

**The goal is always the fewest words that achieve the slide's purpose.** The numbers below are ceilings—not targets. Hitting the maximum is not a goal; it's a limit.

| Context | Maximum Words |
|---------|---------------|
| Live presentation | 50 words |
| Read-ahead main slides | 100 words |
| Executive summary | 150 words |
| Appendix/detail | As needed |

When deck-type guidance (Phase 4) conflicts with format guidance, use the lower number.

**Bullet guidelines:**
- 3–6 bullets per slide maximum
- 15–18 words per bullet maximum
- Avoid large paragraphs

### 3.3 Visual Hierarchy

The eye should know where to go first, second, and third.

**Hierarchy signals:**
- **Size:** Larger = more important
- **Position:** Top-left and center get attention first
- **Weight:** Bold and color draw the eye
- **Whitespace:** Isolation creates emphasis

**The squint test:** Step back and squint. Can you tell what's most important? If everything looks equal, you have a hierarchy problem.

### 3.4 Chart Rules

Charts must earn their place. Every chart needs a "so what."

**Chart titles are takeaways:**

| Label (Weak) | Takeaway (Strong) |
|--------------|-------------------|
| Revenue by Quarter | Revenue grew 24% driven by enterprise segment |
| Customer Satisfaction | NPS improved 15 points after feature launch |

**Rules:**
- Put numbers on bars, lines, and segments
- Minimize legends that force eye movement
- Add callout annotations pointing to what matters
- Remove gridlines, 3D effects, decorative elements

### 3.5 Consistent Visual Language

- Same colors mean the same things throughout
- Same formatting for same-level content
- Consistent slide layouts for similar content types

### 3.6 Speaker Notes Architecture

Never just repeat the slide. Structure for glanceability:

```
[TRANSITION] (1 sentence)
"Moving on from [previous concept]..."

[HOOK] (1 sentence)
A rhetorical question or surprising stat to grab attention

[CORE INSIGHT] (2-3 sentences)
The main point in plain English—your talk track

[SUPPORT] (1-2 items)
Stats or anecdotes NOT on the slide—adds value to listening

[BRIDGE] (1 sentence)
Sets up the next slide's title
```

**Additional guidance:**
- Mark optional content: "[If time] mention the European pilot"
- Note timing cues: "[~2 min on this slide]"
- Flag backup slides: "If they ask about methodology, see slide 24"

---

## Phase 4: Deck-Type Specific Rules

### 4.1 Consulting Deck

**Typical length:** 20–50+ slides (including appendix)

**Structure arc:**
1. **Executive Summary / Recommendation** — Main answer with 2–4 key supporting reasons
2. **Context & Problem** — What's happening and why it matters
3. **Analysis & Drivers** — Key drivers, root causes, scenarios
4. **Options / Alternatives** — Different paths and trade-offs
5. **Recommendation & Rationale** — Why this path over alternatives
6. **Implementation / Next Steps** — How to execute, risks, timing

**Requirements:**
- Executive summary within first 3 slides stating the recommendation
- Final slides must include clear next steps, owners, and timing
- Higher density acceptable (80–120 words per slide)
- Rigorous evidence; cite sources; show methodology

### 4.2 Investor Pitch Deck

**Typical length:** 10–15 slides (seed/early), 15–25 slides (growth)

**The Three Core Questions:**

Every major slide should help answer one of these:

1. **Why Now?**
   - What changed in the world (technology, regulation, behavior, cost) that makes this opportunity possible or much bigger *now*?

2. **Why Us?**
   - Why is this team uniquely positioned to win?
   - Team background, unique insight, traction, unfair advantage

3. **What Will We Achieve?**
   - What concrete milestones with this round?
   - Should set up an impressive next round OR profitability with high growth

**Structure:**
1. **Company Thesis** — Clear one-liner: "We do X for Y so they can Z"
2. **Why Now** — What changed, why this moment is special
3. **Why Us** — Team + insight + execution advantage
4. **Supporting Slides** — Problem, product, market, traction, GTM, economics
5. **Milestone Plan** — What you'll achieve with this round

**Takeaway Titles Only:**

For investor decks, label-only titles are never acceptable:

> **Not allowed:** "Problem" / "Solution" / "Team" / "Market" / "The Ask"

> **Required:** "Legacy systems force recruiters into 6–8 week hiring cycles" / "Our automation platform cuts time-to-hire from 6–8 weeks to under 10 days"

**Market Sizing — Bottom-Up Required:**

| Approach | Example |
|----------|---------|
| **Top-down (weak)** | "$500B industry; if we get 1%..." |
| **Bottom-up (strong)** | "12,000 target companies × $50K ACV × 30% penetration = $180M SAM" |

Show how your actual target segment translates to revenue with explicit assumptions.

**The Final Slide:**

Lead with what this capital will prove, not the raise amount. Investors invest in outcomes, not your need for funding.
The milestone should represent meaningful de-risking—whatever your biggest risk is today should be substantially resolved by the end of this round. That might be:

Commercial traction: "$2M ARR across 35 enterprise customers"
Technical feasibility: "Working prototype demonstrating 10x performance improvement"
Market validation: "Letters of intent from 5 of the top 20 carriers"

The implicit promise: achieving this milestone makes the next raise (at a materially higher valuation) straightforward—or, rarely, makes additional fundraising unnecessary.
For smaller raises (pre-seed, angel rounds): frame milestones as if you were raising a full seed round. The implication is that this capital gets you partway there, not that you're running a separate, smaller race.
> **Weak title:** "Raising $3M pre-seed"

> **Strong title:** "We'll reach $2M ARR across 35 enterprise customers in 12 months"

Structure:
- Title = declarative milestone statement
- Body = Explain why you can achieve that impressive milestone. You can use different proof points. One example: (1) existing traction, (2) execution readiness, (3) pipeline/momentum

**Density:** 60–90 words per slide (lighter than consulting, but rich enough to work as read-ahead)

### 4.3 Sales Deck

**Typical length:** 8–15 slides

**Structure:** Pain → Solution → Proof → Action

**Emphasis:**
- Low density, visually driven
- High emotion—pain relief, success stories
- ROI, case studies, social proof

**Key test:** Does this make them want to see a demo?

### 4.4 Internal / Update Deck

**Typical length:** 5–15 slides

**Structure:** Progress → Insights → Decisions needed

**Key test:** Does this enable a productive discussion?

---

## Phase 5: Validation Checklist

Run these checks before finalizing any deck.

**Check levels:**
- **Error** — Must fix before presenting. Will cause confusion or undermine credibility.
- **Warning** — Should fix. Won't break the deck, but weakens its impact.
- **Suggestion** — Nice to have. Polish items for when time allows.

### Structure Checks

| Check | Level |
|-------|-------|
| Executive summary within first 3 slides states main conclusion | Warning |
| Reading titles in sequence forms coherent argument | Warning |
| Final slide has clear milestones/next steps (not just "Questions?") | Warning |
| Section dividers present for decks >15 slides | Suggestion |
| No consecutive slides making essentially the same point | Warning |

### Slide-Level Checks

| Check | Level |
|-------|-------|
| Word count exceeds format target (see 3.2) | Warning |
| Word count >150 in any slide | Error |
| Multiple main ideas on single slide | Warning |
| Title is <5 words or lacks a verb | Suggestion |
| Title is generic label ("Overview," "Background," "Summary") | Warning |
| Title contains hyperbolic language body doesn't support | Warning |

### Evidence Checks

| Check | Level |
|-------|-------|
| Market size claim without third-party source | Warning |
| Statistics without attribution | Warning |
| Competitive claims without evidence | Warning |
| Strong claims ("huge opportunity") with no supporting signal | Warning |

### Language Checks

| Check | Level |
|-------|-------|
| Abstract jargon without concrete explanation | Warning |
| Would never say it this way in conversation | Suggestion |
| Title emotional intensity mismatched with content | Warning |

### Flow Checks

| Check | Level |
|-------|-------|
| Consecutive slides with no logical connection and no section divider | Warning |
| No transition language in speaker notes | Suggestion |
| 3+ consecutive slides in problem section with similar framing | Warning |

---

## Phase 6: Critique Framework

When evaluating a deck, lead with overall assessment before detailing specifics.

### Assessment Levels

| Level | When to Use | Opening Language |
|-------|-------------|------------------|
| **Fundamentally sound** | Minor polish needed | "Strong foundation—a few adjustments will sharpen the impact" |
| **Significant gaps** | Core story exists but issues undermine it | "The core story is here, but structural issues are undermining it" |
| **Materially misses** | Right ingredients, wrong execution | "You have the bones of a good story, but this deck materially misses the mark" |
| **Needs rebuild** | Fundamental strategy problems | "The current approach isn't working—let's discuss strategy before rebuilding" |

### Critique Principles

1. **Lead with overall assessment.** Don't bury critical feedback.

2. **Be specific about what's wrong and why.** "This slide is confusing" is useless. "This slide uses 'orchestration layer' without explaining what it means—readers outside your company won't know if it's software, a service, or a process" is actionable.

3. **Distinguish preference from principle.** "I would have used blue" is preference. "Using red for positive metrics violates your color system from slide 3" is principle.

4. **Prioritize ruthlessly.** Identify the 3–5 issues that matter most. Save minor issues for a secondary list.

5. **Calibrate to stakes.** A $50M Series B deck needs harsher critique than an internal update.

### Example Critique Opening

> "You have the bones of a good story here, but this deck materially misses the mark. Three issues need immediate attention:
>
> 1. **The problem section is repetitive.** Slides 2–5 all say the same thing. Compress to 1–2 slides.
>
> 2. **Statistics lack sources.** Every major claim needs attribution. Right now they read as made up.
>
> 3. **Final slide is framed as an ask instead of an outcome.** Lead with what you'll achieve, not what you're raising.
>
> The traction is real and the problem is genuine. Fix the execution and this becomes compelling."

---

## Quick Reference Card

### Before Building
- [ ] Audience defined (who, what they know, what they care about)
- [ ] ONE takeaway written as single sentence
- [ ] Desired action specified
- [ ] Format determined (live / read-ahead / hybrid)
- [ ] Top 3 objections anticipated

### While Building
- [ ] Titles read as coherent argument
- [ ] Each slide = one message
- [ ] Every title is a takeaway, not a label
- [ ] Every claim has visible evidence
- [ ] Language is concrete, not abstract

### Before Finalizing
- [ ] Executive summary in first 3 slides
- [ ] Final slide has clear next steps/milestones
- [ ] Word counts within format limits
- [ ] No redundant slides
- [ ] Speaker notes include transitions

### For Investor Decks
- [ ] "Why Now" explicitly answered
- [ ] "Why Us" clearly articulated
- [ ] Market sizing is bottom-up
- [ ] Final slide leads with milestones, not raise amount
- [ ] No label-only titles anywhere

---

## Appendix A: Title Transformation Examples

| Original (Weak) | Transformed (Strong) |
|-----------------|---------------------|
| Introduction | Enterprise security teams waste 40% of time on false positives |
| Market Opportunity | The $50B security market is consolidating around AI-native solutions |
| Problem | Legacy systems force manual reconciliation of 10+ data sources daily |
| Solution | Our platform automates reconciliation, saving 15 hours per analyst per week |
| Team | Our founders built and scaled the core detection engine at [Competitor] |
| Business Model | Land-and-expand model yields 140% net revenue retention |
| Financials | We'll reach $15M ARR and profitability by Q3 2026 |
| The Ask | This round gets us to $2M ARR across 35 enterprise customers in 12 months |

**Quantitative proof isn't always available.** Here are strong titles that don't rely on numbers:

| Original (Weak) | Transformed (Strong) |
|-----------------|---------------------|
| Technology | Our architecture is the only one built for real-time processing from day one |
| Competitive Advantage | Competitors are locked into legacy codebases they can't rewrite |
| Why Now | New regulations make the old approach illegal starting January 2026 |
| Product | We're the only platform that handles both inbound and outbound in one workflow |
| Market Timing | Enterprise buyers are actively looking to replace their legacy vendors |
| Partnership | Our exclusive distribution deal with [Partner] gives us access competitors can't get |
| Defensibility | Switching costs lock in customers once they've integrated |
| Vision | We're building the system of record for [industry] operations |

---

## Appendix B: Deck Type Comparison

| Attribute | Consulting | Investor (Seed) | Investor (Growth) | Sales |
|-----------|------------|-----------------|-------------------|-------|
| Length | 20–50+ slides | 10–15 slides | 15–25 slides | 8–15 slides |
| Density | 80–120 words | 60–90 words | 75–100 words | 25–50 words |
| Evidence rigor | Very high | High (despite limited data) | Very high | Moderate |
| Emotion | Moderate | High (but earned) | Moderate | High |
| Key test | Can partner read exec summary and understand recommendation? | Would this get forwarded with positive note? | Do numbers tell compelling growth story? | Does this make them want a demo? |
```

</details>
