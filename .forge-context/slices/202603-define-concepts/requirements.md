# Requirements: Define Concepts

## Summary

Create a concepts.md file that introduces the primary Flox concepts -- environments, packages, dependencies, and upgrades -- in simple, plain language with Mermaid diagrams. This is the second layer of the three-layer documentation structure, building on the Principles page and connecting to Flox Specifics.

## Success Criteria

- [ ] concepts.md exists at project root and is linked from README
- [ ] Covers four concepts: environments, packages, dependencies, upgrades
- [ ] Each concept explained in plain language
- [ ] Mermaid diagrams accompany concepts where they aid understanding
- [ ] Content builds on the Principles page (references back to principles where relevant)
- [ ] Language is plain-spoken with no undefined jargon
- [ ] Principles page outro link to concepts.md works

## Scope

### In Scope

- Writing concepts.md with four concept sections
- Mermaid diagrams for concepts
- Updating README to link to concepts page
- Ensuring principles.md link to concepts.md works

### Out of Scope

- Writing the Flox Specifics layer
- Technology-specific implementation details (those belong in Flox Specifics)
- Detailed tutorials or how-to guides

## Affected Components

| Component | Impact | Reviewer |
|-----------|--------|----------|
| concepts.md (new) | New file | @jbayer |
| README.md | Update to link to concepts | @jbayer |

## Approach

### High-Level Strategy

Follow the same pattern as principles.md: a single markdown file at the project root. Each concept gets a heading, plain-language explanation, and a Mermaid diagram. The page should feel like a natural continuation from principles.md.

## Open Questions

- Should concepts reference Flox by name, or stay technology-neutral like principles? (Principles page intro/outro already mentions Flox, so likely yes)
- What level of detail per concept? Brief overview or deeper explanation?

---

## Source

**Origin:** Standalone story, follows completed Define Principles epic
