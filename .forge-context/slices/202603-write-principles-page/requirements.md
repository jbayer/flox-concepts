# Requirements: Write the Principles Page

## Summary

Create a principles.md file that establishes the foundational reasoning behind the platform. The page presents three principles -- Reproducibility, Efficiency, and Simplicity -- in plain language for stakeholders involved in managing custom software. It serves as the entry point to the three-layer documentation structure (Principles, Concepts, Flox Specifics) and as a conversation anchor at conferences.

## Success Criteria

- [ ] principles.md exists in the project and is linked from README
- [ ] Three principles are clearly presented with heading, one-line summary, and "why this matters" expansion
- [ ] No technology names (Flox, Nix, Docker, etc.) appear in the content
- [ ] Language is plain-spoken with no undefined jargon
- [ ] Each principle is memorable and explainable in one sentence
- [ ] Total length is no more than one page
- [ ] Intro frames principles as deeply held beliefs that shaped the platform
- [ ] Outro transitions to the Concepts layer
- [ ] File location supports the three-layer content structure

## Scope

### In Scope

- Writing principles.md with intro, three principles, and outro
- Deciding file placement in the project structure
- Updating README to link to the principles file

### Out of Scope

- Writing the Concepts layer (separate epic)
- Writing the Flox Specifics layer (separate epic)
- Visual diagrams (separate story ST-003)
- Building a documentation site or framework

## Affected Components

| Component | Impact | Reviewer |
|-----------|--------|----------|
| README.md | Update to link to principles | @jbayer |
| principles.md (new) | New file | @jbayer |

## Approach

### High-Level Strategy

Write a single markdown file containing an intro paragraph, three principle sections (each with heading + one-line summary + "why this matters" expansion), and an outro paragraph. Place the file in a location that scales as Concepts and Flox Specifics content is added later.

### Key Technical Decisions

#### Decision: Principle Count and Selection
- **Options:** Keep original 5 principles, consolidate to 3, consolidate to 4
- **Chosen:** 3 principles (Reproducibility, Efficiency, Simplicity)
- **Rationale:** Three is more memorable and avoids overlap. Verification folds into Reproducibility. "Skip unnecessary work" and "automate toil" merge into Efficiency. "Upgrades and rollbacks" broadens into Simplicity.

#### Decision: Principle Definitions
- **Reproducibility** -- Same inputs, same results -- and you can prove it
- **Efficiency** -- Do work early and repeatably reuse the results
- **Simplicity** -- Managing the software you work with should be straightforward

## Open Questions

- Where should principles.md live? Root level or a content directory? (TH-002 from epic)

---

## Source

**Effort:** `.forge-context/efforts/202603-define-principles/`
**Stories:** ST-001, ST-002
