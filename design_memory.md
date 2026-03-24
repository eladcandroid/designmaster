# Design Memory

## Purpose

This document stores validated design decisions, patterns, and failures.

It improves future design generation by:
- reinforcing effective design patterns
- preventing repetition of weak or generic structures
- evolving a distinct design language over time

This is not inspiration.

Only store designs that provide clear, reusable insight.

---

## Core Principles

1. Only store high-signal design outcomes
2. Every entry must include reasoning
3. Avoid vague aesthetic descriptions
4. Prefer specific, reproducible patterns
5. Remove outdated or irrelevant entries

---

## Memory Categories

---

### 1. Proven Layout Patterns

[LAYOUT]

Name:
- Asymmetrical Hero with Staggered Sections

Structure:
- Left-aligned hero content
- Offset visual element (not centered)
- Sections alternate alignment (left/right stagger)
- Irregular spacing rhythm

Why It Worked:
- Breaks predictable scanning patterns
- Creates visual tension and hierarchy
- Feels intentional and designed, not templated

When to Use:
- SaaS alternatives
- portfolios
- AI tools with personality

[LAYOUT]

Name:
- Editorial Split Layout

Structure:
- 60–70% text column
- 30–40% supporting visual column
- strong vertical rhythm
- no centered hero

Why It Worked:
- prioritizes content readability
- avoids "landing page" feel
- mimics high-end editorial design

When to Use:
- blogs
- long-form product explanations
- storytelling pages

[VISUAL]

Style:
- Brutalist Minimal

Key Elements:
- hard edges
- visible grid
- minimal color palette (1–2 colors)
- system fonts or mono fonts

Why It Worked:
- aggressively non-generic
- stands out immediately
- communicates confidence and clarity

Avoid When:
- corporate clients
- highly trust-sensitive industries

[VISUAL]

Style:
- Dark high-contrast with accent color restraint

Key Elements:
- near-black background (#0a0a0a range)
- single accent color used sparingly
- minimal gradients
- sharp typography contrast

Why It Worked:
- feels premium and intentional
- avoids noisy "AI gradient spam"
- focuses attention on content

Avoid When:
- playful brands
- youth-focused products

[INTERACTION]

Pattern:
- Subtle Hover Elevation with Delayed Response

Behavior:
- elements slightly lift on hover
- 100–150ms delay before animation
- soft easing curve

Impact:
- feels responsive but not twitchy
- adds polish without distraction

Constraints:
- avoid on dense layouts
- avoid stacking multiple hover effects

[INTERACTION]

Pattern:
- Scroll-Based Section Reveal

Behavior:
- sections fade/slide in on scroll
- staggered timing between elements

Impact:
- improves perceived smoothness
- guides user attention

Constraints:
- avoid excessive animation
- ensure performance on mobile

[ANTI-PATTERN]

Pattern:
- Centered Hero + 3 Feature Cards

Why It Failed:
- overused across SaaS and AI-generated sites
- no differentiation
- predictable scanning behavior

What It Looked Like:
- headline (centered)
- subtext
- CTA button
- 3 equal columns below

Replacement Strategy:
- asymmetrical hero
- staggered or single-column feature flow

[ANTI-PATTERN]

Pattern:
- Overuse of Gradients

Why It Failed:
- reduces visual clarity
- creates generic "AI aesthetic"
- weakens hierarchy

What It Looked Like:
- gradient backgrounds everywhere
- gradient buttons + cards

Replacement Strategy:
- use solid base colors
- apply gradients only for emphasis

[ANTI-PATTERN]

Pattern:
- Card Grid Overload

Why It Failed:
- turns content into undifferentiated blocks
- kills hierarchy
- feels like a template

What It Looked Like:
- repeated rectangular cards
- uniform spacing
- no variation

Replacement Strategy:
- mixed layout sections
- varied component sizing
- narrative flow instead of grids

[COMPONENT]

Component:
- Buttons

Observation:
- identical button styles across site reduce perceived quality

Impact:
- lowers visual hierarchy clarity
- feels templated

Rule Going Forward:
- define primary, secondary, and tertiary button styles
- vary emphasis intentionally

[COMPONENT]

Component:
- Typography

Observation:
- default sans-serif (Inter-style) leads to generic appearance

Impact:
- reduces brand identity
- blends with typical SaaS UI

Rule Going Forward:
- use distinct type pairing
- introduce contrast (serif + sans or mono + sans)

[COMPONENT]

Component:
- Section Spacing

Observation:
- uniform spacing creates mechanical feel

Impact:
- reduces rhythm and visual interest

Rule Going Forward:
- introduce spacing variation
- use compression and expansion intentionally

## Entry Rules

Must be specific (no vague descriptions)
Must include cause and effect
Must be reusable
Must not duplicate design_system.md rules


## Update Triggers

Update this file when:

a design feels clearly differentiated
a layout performs consistently well
a UI pattern improves usability
a design repeatedly fails or feels generic
Integration

## Works with:

design_system.md → enforces rules
design_variation_engine.md → enforces diversity
system_memory.md → broader system learning
prompt_optimizer.md → improves generation quality


## Final Rule

If it cannot improve the next design decision, it does not belong here.