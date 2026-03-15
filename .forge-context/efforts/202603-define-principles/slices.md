# Stories: Define Principles

Stories of work identified from this epic. Candidates
are reviewed, then spawned as stories in
`.forge-context/slices/YYYYMM-{slug}/`.

---

## Summary

| Status | Count |
|--------|-------|
| Pending Review | 0 |
| Accepted | 1 |
| Spawned | 0 |
| Completed | 1 |
| **Total** | **2** |

---

## Pending Review

_Candidates under review. Once approved, move to
Accepted. From there, spawn via `/forge:work`._

---

## Accepted (Ready to Spawn)

_Reviewed and approved, ready to spawn via
`/forge:work new`._

### SL-002: Add Diagrams to Principles Page

**Status:** `accepted`

**Summary:** Add four Mermaid diagrams inline in principles.md: one overview flow (Principles → Concepts → Platform Implementation) and one per principle (Reproducibility, Efficiency, Simplicity).

**Stories:** ST-003

**Acceptance Criteria:**
- [ ] Mermaid flowchart showing Principles → Concepts → Platform Implementation
- [ ] Mermaid diagram for Reproducibility: same inputs → same outputs on multiple machines
- [ ] Mermaid diagram for Efficiency: work done once → cached → reused many times
- [ ] Mermaid diagram for Simplicity: common tasks (setup, change, share, rollback) all being simple
- [ ] All diagrams are inline in principles.md
- [ ] Diagrams reinforce the text rather than duplicating it
- [ ] All diagrams render correctly on GitHub

**Approach:** Add Mermaid flowcharts inline in principles.md. Overview diagram near the intro/outro, per-principle diagrams alongside their respective sections.

**Blockers:** None

**Estimated Scope:** `Small`
**Priority:** `Medium`
**Depends on:** None (SL-001 already merged)

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
| SL-001 | Write the Principles Page | 2026-03-15 | Completed | ST-001, ST-002 | PR #2 (merged) |

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
