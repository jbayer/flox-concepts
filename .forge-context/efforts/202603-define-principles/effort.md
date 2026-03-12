# Epic: Define Principles

This is a living document. Update it as understanding evolves.

---

## Problem Space

### Problem Statement

Newcomers to Flox have no simple, technology-neutral explanation of *why* reproducible environments matter. When the team talks to users at conferences, they jump into technical details too early because there is no foundational "principles" layer to start from. Without this layer, conversations lose people before they ever get to concepts or tooling.

The project needs a principles.md file that establishes the foundational reasoning -- why reproducibility, why automation, why verification -- so that the Concepts and Flox Specifics layers have solid ground to build on.

### Why Now?

- **Conference conversations:** The team is actively talking to users and needs a simple starting point that does not require technical background. The gap is felt in real conversations today.
- **Content foundation:** The three-layer structure (Principles, Concepts, Flox Specifics) is defined but empty. Principles must come first because the other layers reference it.
- **Team principle alignment:** The team's own working principles ("lead with principles", "concepts before technology details") demand this layer exists before other content is written.

### Current State

- The project README describes three content layers but no content files exist yet.
- The team has an intuitive sense of the principles but they are not written down in plain language.
- Conference conversations currently require improvisation -- there is no shared reference document the team can point to or build from.
- Five candidate principles have been identified at a rough level but not yet articulated for a newcomer audience.

### Success Vision

A reader with no knowledge of Flox, Nix, or reproducible environments can read the principles page and understand *why* these ideas matter to them. The page serves as the natural starting point for the documentation and as a conversation anchor at conferences. Each principle is clear enough that a reader could explain it to someone else in their own words.

---

## Stakeholders

### Who is affected?

| Stakeholder | Needs | Impact |
|-------------|-------|--------|
| Newcomers to Flox | Understand why reproducible environments matter before encountering technical details | Primary audience -- the content is written for them |
| Flox team (conference conversations) | A simple reference to anchor technical conversations | Enables more effective outreach and onboarding |
| Content authors (future) | A stable principles layer to build Concepts and Flox Specifics on top of | Unblocks the next two content layers |

### Who has context?

- **@jbayer**: Product vision, conference conversation experience, candidate principles list

---

## Scope Coverage

_Dashboard view: what's been addressed by stories
vs what's still open._

| Capability | Status | Resolution |
|------------|--------|------------|
| ST-001: Draft principles content | draft | -- |
| ST-002: Determine file placement | draft | -- |
| ST-003: Visual diagrams for principles | draft | -- |

**Status values:**
- `draft` / `refined` / `ready` -- Still exploring
- `in-story` -- Story underway
- `completed` -- Story shipped
- `deferred` -- Not pursuing now

---

## Item Status Values

**Stories and Requirements:**
- `draft` - Initial capture, needs refinement
- `refined` - Discussed and clarified
- `ready` - Ready for story or implementation
- `in-story` - Spawned to a story
- `completed` - Work finished

**Threads:**
- `Investigating` - Active research
- `Blocked` - Waiting on external input
- `Ready to resolve` - Answer known, needs docs
- `Resolved` - Moved to Resolved Threads section

---

## Stories

_User stories discovered during epic._

### ST-001: Draft Principles Content

**Status:** `draft`

**As a** newcomer with no Flox or Nix background,
**I want to** read a plain-language explanation of why reproducible environments matter,
**So that** I understand the motivation before encountering any specific technology.

**Acceptance Criteria:**
- [ ] Covers all five candidate principles: reproducibility, skip unnecessary work, trust through verification, automate toil, simple upgrades and rollbacks
- [ ] Each principle is explained without referencing Flox, Nix, or any specific tool
- [ ] Language is plain-spoken and brief (team writing principles)
- [ ] A reader with no technical background can understand each principle
- [ ] Principles connect logically -- reading order makes sense

**Notes:**
- The five candidate principles from @jbayer are a starting point, not necessarily final
- Each principle needs a clear "why this matters to you" angle
- See TH-001 for open question on principle granularity

### ST-002: Determine File Placement

**Status:** `draft`

**As a** content author,
**I want to** know where principles.md lives in the project structure,
**So that** the file is discoverable and the project structure scales as Concepts and Flox Specifics are added.

**Acceptance Criteria:**
- [ ] File location is decided and documented
- [ ] README is updated to link to the principles file
- [ ] Location supports the three-layer content structure without reorganization later

**Notes:**
- Currently the project root has only README.md and config files
- Options include: root-level principles.md, a docs/ directory, or a content/ directory
- See TH-002 for investigation

### ST-003: Visual Diagrams for Principles

**Status:** `draft`

**As a** newcomer reading the principles page,
**I want to** see visual diagrams that illustrate key concepts,
**So that** I can quickly grasp ideas that are harder to convey in text alone.

**Acceptance Criteria:**
- [ ] At least one diagram accompanies the principles content
- [ ] Diagrams are renderable in standard markdown (Mermaid, inline SVG, or image references)
- [ ] Diagrams reinforce the text rather than duplicating it

**Notes:**
- Team principle: "visual diagrams are essential"
- Diagram format decision may depend on where this content is rendered (GitHub, docs site, etc.)
- See TH-003 for investigation on diagram approach

---

## Requirements

_Requirements discovered during epic._

### REQ-001: Technology-Neutral Language

**Status:** `draft`
**Category:** Functional

**Requirement:**
The principles page must not reference any specific technology (Flox, Nix, Docker, etc.). Principles describe universal ideas about software environments.

**Acceptance Criteria:**
- [ ] No technology names appear in the principles content
- [ ] Principles are applicable regardless of which tool a reader eventually uses

**Notes:**
- This is the core differentiator between the Principles layer and the Concepts/Flox Specifics layers

### REQ-002: Plain Language and Brevity

**Status:** `draft`
**Category:** Functional

**Requirement:**
Content must use simple, plain-spoken language. Jargon must be avoided or immediately explained. Sections should be brief.

**Acceptance Criteria:**
- [ ] No undefined jargon
- [ ] Each principle can be read and understood in under two minutes

**Notes:**
- Aligns with team writing principles: "write brief, plain-spoken language"

### REQ-003: Progressive Structure

**Status:** `draft`
**Category:** Functional

**Requirement:**
The principles page must serve as the entry point to the three-layer documentation structure, clearly connecting to the Concepts layer that follows.

**Acceptance Criteria:**
- [ ] Reader understands this is the starting point
- [ ] Natural transition from principles to deeper content is clear

---

## Scope Boundaries

_Refine as understanding grows. These are starting points,
not commitments._

### Likely In Scope
- Articulating the five candidate principles in plain language
- Determining where the file lives in the project
- Creating at least one supporting visual diagram
- Ensuring the content works as a conference conversation anchor

### Likely Out of Scope
- Writing the Concepts layer (separate epic)
- Writing the Flox Specifics layer (separate epic)
- Building a documentation site or framework
- Detailed technical explanations of how any principle is implemented

### Unknown / To Investigate
- Whether five principles is the right number or if some should be merged/split
- What diagram format works best given the rendering targets
- Whether the file should include a brief "what's next" section pointing to Concepts

---

## Current Understanding

_This section evolves as we learn. Date your updates._

### 2026-03-12 Initial Framing

The team has identified five candidate principles from conference conversation experience:

1. **Software should be reproducible** -- the same inputs should produce the same outputs
2. **Skip unnecessary work** -- do not rebuild or recompute what has not changed
3. **Trust through verification** -- prove that environments are what they claim to be
4. **Automate toil** -- remove repetitive manual steps from environment management
5. **Simple upgrades and rollbacks** -- changing or reverting should be low-risk and easy

These are rough framings. Discovery work will refine the language, determine the right granularity, and ensure each principle resonates with a newcomer audience.

Key assumption (team intuition): these five principles cover the essential "why" for reproducible environments. This should be validated -- are there gaps? Do conference conversations surface questions these principles do not answer?

---

## Open Threads

Active areas of investigation.

### TH-001: Principle Granularity and Completeness

**Question:** Are five principles the right number? Should any be merged (e.g., "skip unnecessary work" and "automate toil" overlap) or split? Are there missing principles that conference conversations reveal?

**Type:** Clarification

**Status:** Investigating

**Context:**
- The five candidates came from @jbayer's conference experience
- Some principles may overlap in practice (efficiency vs. automation)
- Missing angles might include: collaboration/sharing, security, or developer experience

### TH-002: File Placement in Project Structure

**Question:** Where should principles.md live? Root level, a docs/ directory, or something else? How does this choice affect the Concepts and Flox Specifics files that come later?

**Type:** Decision

**Status:** Investigating

**Context:**
- Current project root contains only README.md and config directories
- The choice affects discoverability and whether the structure needs reorganization later
- Simplest option is root-level, but a directory may be cleaner as content grows

### TH-003: Diagram Format

**Question:** What format should diagrams use? Mermaid (renders on GitHub), inline SVG, or external image files?

**Type:** Decision

**Status:** Investigating

**Context:**
- Team principle: "visual diagrams are essential"
- If content is primarily read on GitHub, Mermaid has native support
- If a docs site is planned later, other formats may be more flexible
- Simpler is better for a markdown-only project

---

## Resolved Threads

---

## References

- Project README: `/README.md`
- Product context: `.forge-context/context/product.md`
