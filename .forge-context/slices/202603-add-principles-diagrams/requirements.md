# Requirements: Add Diagrams to Principles Page

## Summary

Add four Mermaid diagrams inline in principles.md: one overview flowchart showing how Principles feed into Concepts which feed into Platform Implementation, and one diagram per principle illustrating its core idea visually.

## Success Criteria

- [ ] Mermaid flowchart showing Principles → Concepts → Platform Implementation
- [ ] Mermaid diagram for Reproducibility: same inputs → same outputs on multiple machines
- [ ] Mermaid diagram for Efficiency: work done once → cached → reused many times
- [ ] Mermaid diagram for Simplicity: common tasks (setup, change, share, rollback) all being simple
- [ ] All diagrams are inline in principles.md
- [ ] Diagrams reinforce the text rather than duplicating it
- [ ] All diagrams render correctly on GitHub

## Scope

### In Scope

- Four Mermaid diagrams added inline to principles.md
- Overview diagram near intro/outro
- Per-principle diagrams alongside their respective sections

### Out of Scope

- Changes to the principles text
- Diagrams for the Concepts or Flox Specifics layers
- Non-Mermaid diagram formats

## Affected Components

| Component | Impact | Reviewer |
|-----------|--------|----------|
| principles.md | Add diagrams inline | @jbayer |

## Approach

### High-Level Strategy

Add Mermaid flowcharts directly in principles.md. The overview diagram goes near the outro to reinforce the three-layer structure. Each principle gets a diagram below its expansion text.

## Open Questions

_None._

---

## Source

**Effort:** `.forge-context/efforts/202603-define-principles/`
**Stories:** ST-003
