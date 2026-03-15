# Stories: Define Principles

Stories of work identified from this epic. Candidates
are reviewed, then spawned as stories in
`.forge-context/slices/YYYYMM-{slug}/`.

---

## Summary

| Status | Count |
|--------|-------|
| Pending Review | 0 |
| Accepted | 0 |
| Spawned | 1 |
| Completed | 0 |
| **Total** | **1** |

---

## Pending Review

_Candidates under review. Once approved, move to
Accepted. From there, spawn via `/forge:work`._

---

## Accepted (Ready to Spawn)

_Reviewed and approved, ready to spawn via
`/forge:work new`._

### SL-001: Write the Principles Page

**Status:** `spawned`

**Summary:** Create principles.md with three principles (Reproducibility, Efficiency, Simplicity), an intro framing them as core beliefs behind the platform, and an outro transitioning to the Concepts layer.

**Stories:** ST-001, ST-002

**Acceptance Criteria:**
- [ ] principles.md created in an appropriate project location
- [ ] Intro clarifies these are deeply held beliefs that shaped the platform and understanding them helps readers see why it works the way it does and where it's headed
- [ ] Three principles presented: Reproducibility, Efficiency, Simplicity
- [ ] Each principle has a heading, one-line summary, and "why this matters" expansion
- [ ] No technology names (Flox, Nix, Docker, etc.) appear in the content
- [ ] Language is plain-spoken, no undefined jargon
- [ ] Each principle is memorable and explainable in one sentence
- [ ] Total length is no more than one page
- [ ] Outro references how principles are applied as concepts
- [ ] README updated to link to the principles file
- [ ] File location supports the three-layer content structure

**Approach:** Write a single markdown file. Place it in a location that scales as Concepts and Flox Specifics are added (likely root-level or a content directory). Structure: intro paragraph, three principle sections, outro paragraph.

**Blockers:** None

**Estimated Scope:** `Small`
**Priority:** `High`
**Depends on:** None

---

## Direct Issues

_Items addressed directly without formal stories._

| Issue | Items | Status | Notes |
|-------|-------|--------|-------|

**When to use direct issues:**
- Bug fixes, patches, quick enhancements
- Small, well-understood work (< 2 days)
- No requirements/design phase needed

---

## Spawned

_Stories created from this epic._

| ID | Story | Spawned | Status | Items | Link |
|----|-------|---------|--------|-------|------|
| SL-001 | Write the Principles Page | 2026-03-15 | Requirements | ST-001, ST-002 | `slices/202603-write-principles-page/` |

---

## Story Lifecycle

| Status | What Happens |
|--------|--------------|
| **Draft** | Candidate identified, preparing for review |
| **Under Review** | Being reviewed |
| **Accepted** | Approved, ready to spawn |
| **Spawned** | Story directory created, work begins |
| **In Progress** | Design/implementation underway |
| **Completed** | Story shipped |

---

<!--
STORY TEMPLATE - Copy to Pending Review section:

### SL-NNN: [Story Name]

**Status:** `draft`

**Summary:** [One-line description]

**Stories:** ST-NNN, ST-NNN

**Acceptance Criteria:**
- [ ] [Criterion]
- [ ] [Criterion]

**Approach:** [How this will be solved]

**Blockers:** None

**Estimated Scope:** `Medium`
**Priority:** `Medium`
**Depends on:** None

---
-->
