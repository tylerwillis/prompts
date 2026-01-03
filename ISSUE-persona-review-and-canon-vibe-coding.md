# Add persona-review skill and canon-based-vibe-coding prompt chain

## Overview

Add two new capabilities to the prompts collection:

1. **Persona Review Skill** - A prompt for reviewing and refining AI personas/characters
2. **Canon-Based Vibe Coding Prompt Chain** - A multi-step workflow for generating code that matches an established codebase's style and conventions

---

## 1. Persona Review Skill

### Purpose
A structured prompt for evaluating and improving AI persona definitions, similar to how `review_deck.md` evaluates presentation decks.

### Potential Framework

| Phase | Focus | Key Questions |
|-------|-------|---------------|
| **Pre-work** | Context | What's this persona for? Who interacts with it? In what contexts? |
| **Core Review** | Fundamentals | Is it consistent, distinctive, and fit for purpose? |
| **Deep Dive** | Quality | How does it handle edge cases, conflict, ambiguity? |
| **Validation** | Completeness | What's missing? What's overdone? |

### Detailed Framework

**Phase 1: Pre-Work**
- Purpose definition: What job does this persona do?
- Audience mapping: Who will interact with it?
- Context awareness: Where/when/how will interactions happen?
- Success criteria: What makes this persona "working"?

**Phase 2: Core Principles**
- **Consistency Check**: Does the persona behave consistently across different contexts?
- **Voice & Tone Audit**: Is the persona's voice distinctive and appropriate for its purpose?
- **Knowledge Boundaries**: Are the persona's areas of expertise and limitations clearly defined?
- **Personality Coherence**: Do traits, behaviors, and responses align with the stated personality?
- **Authenticity Assessment**: Does the persona feel genuine or overly scripted?
- **Goal Alignment**: Does the persona's behavior serve its intended purpose?

**Phase 3: Edge Case & Stress Testing**
- Unexpected inputs: How does the persona respond to off-topic or challenging questions?
- Conflict handling: How does the persona manage disagreement or pushback?
- Emotional range: Can the persona express appropriate emotions without breaking character?
- Recovery: How does the persona handle mistakes or confusion gracefully?

**Phase 4: Calibration**
Where LLMs might **over-correct**:
- Making personas too friendly/helpful (losing distinctive edge)
- Excessive hedging and disclaimers
- Over-explaining persona motivations

Where LLMs might **under-index**:
- Maintaining consistent quirks over long conversations
- Handling conflict without breaking character
- Subtle personality traits that don't fit neat categories

**Phase 5: Validation Checklist**

| Severity | Type | Meaning |
|----------|------|---------|
| 🔴 Error | Critical | Breaks the persona - immediate fix required |
| 🟡 Warning | Significant | Weakens the persona - should address |
| 🟢 Suggestion | Enhancement | Could make persona stronger |

---

## 2. Canon-Based Vibe Coding Prompt Chain

### Purpose
A multi-step prompt workflow for generating code that matches an existing codebase's "vibe" - its patterns, conventions, naming styles, and architectural decisions.

### The Problem
When LLMs generate code, they often produce:
- Generic patterns that don't match the existing codebase
- Inconsistent naming conventions
- Different architectural approaches than what's established
- Code that "works" but doesn't "fit"

### Proposed Chain Structure

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  Step 1:        │     │  Step 2:        │     │  Step 3:        │     │  Step 4:        │
│  Canon          │────▶│  Pattern        │────▶│  Vibe           │────▶│  Generation     │
│  Extraction     │     │  Recognition    │     │  Synthesis      │     │  with Canon     │
└─────────────────┘     └─────────────────┘     └─────────────────┘     └─────────────────┘
```

**Step 1: Canon Extraction**
- Input: 3-5 representative files from the codebase
- Extract: naming conventions, file structure, comment style, error handling, abstraction levels
- Output: Raw observations about the codebase's patterns

**Step 2: Pattern Recognition**
- Identify recurring architectural patterns (composition vs inheritance, DI patterns, etc.)
- Note preferred libraries, utilities, and idioms
- Map the control flow and state management approaches
- Output: Structured pattern documentation

**Step 3: Vibe Synthesis**
- Distill extracted patterns into a coherent "coding persona"
- Create example transformations: generic code → canon-compliant code
- Define what "feels right" vs "feels off" for this codebase
- Output: A "vibe document" that captures the essence

**Step 4: Generation with Canon Awareness**
- Use synthesized vibe to generate new code
- Self-review against extracted canon
- Flag any intentional deviations with reasoning
- Output: Canon-compliant code with confidence notes

### Why a Chain?
This is inherently multi-step: you need to understand before you can replicate. A single prompt would be too context-heavy; a chain allows each step to focus on its purpose and build incrementally.

### Example Canon Dimensions

| Dimension | Questions to Answer |
|-----------|---------------------|
| **Naming** | camelCase vs snake_case? Verbose vs terse? Prefixes/suffixes? |
| **Structure** | File organization? Module boundaries? Import patterns? |
| **Abstraction** | When to abstract? How deep? Interface vs implementation? |
| **Error Handling** | Exceptions vs results? Where to handle? How verbose? |
| **Comments** | When to comment? Doc style? TODOs allowed? |
| **Testing** | Test file location? Naming? Coverage expectations? |

---

## Open Questions

- [ ] Should persona-review include prompts for *creating* personas, or just reviewing existing ones?
- [ ] For canon-based-vibe-coding, should Step 1 be a separate standalone tool for reuse?
- [ ] What's the right format for the vibe synthesis output? (structured data vs prose vs both?)
- [ ] Should these be Claude Code skills (`.claude/skills/`) or standalone prompts in this repo?
- [ ] Is there value in a "persona-from-canon" prompt that generates a coding persona from a codebase?

---

## Implementation Notes

### For Persona Review
- Follow the same structure as `review_deck.md`: phases, calibration, validation checklist
- Include worked examples showing good vs weak personas
- Consider severity levels similar to deck review (errors/warnings/suggestions)

### For Canon-Based Vibe Coding
- Each step should be a separate prompt that can be run independently
- Step 3 output should be reusable across multiple generation tasks
- Consider caching the "vibe document" for repeated use on the same codebase

---

## Related Work

- The `review_deck.md` prompt provides an excellent template for the persona-review skill
- The phased approach (Pre-work → Core → Validation) could apply to both new prompts
- The calibration pattern (where LLMs over/under-correct) is valuable for both use cases
