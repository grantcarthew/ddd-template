# [Project Name] - Design Phase

Phase: Design
Started: [Date]
Last Updated: [Date]

This document guides AI agents through the design phase of this project using Documentation Driven Development (DDD).

IMPORTANT: Read `docs/design/dr-writing-guide.md` before continuing. That guide defines how to write Design Records (DRs).

---

## Project Overview

Project Name: [Project Name]
Type: [CLI tool / web application / library / API service / etc.]
Languages: [Programming language(s)]
Description: [1-2 sentence description]

## Design Phase Objectives

The design phase is the most important part of DDD. Through interactive creation of Design Records, you will:

1. Think deeply about the project by answering design questions
2. Make explicit decisions about architecture, technology, and approach
3. Document the "why" behind each decision
4. Identify dependencies and decision order
5. Build a complete design before (or alongside) implementation

## How to Work in Design Phase

### Your Role as Design Agent

You are here to:

- Ask probing questions that uncover design decisions
- Challenge assumptions to ensure decisions are well-thought-out
- Suggest alternatives the user may not have considered
- Create DRs for each significant decision
- Maintain the DR index as decisions are made
- Identify gaps in the design that need decisions

### Design Session Workflow

1. Identify next design decision - What needs to be decided?
2. Gather context - What information is needed to make this decision?
3. Explore alternatives - What are the options?
4. Discuss trade-offs - What are the pros/cons of each option?
5. Make decision - User chooses an approach
6. Document as DR - Create a Design Record following dr-writing-guide.md
7. Update DR index - Add to docs/design/design-records/README.md
8. Identify follow-up decisions - What new questions does this decision raise?
9. Repeat - Continue until design is complete (or MVP ready)

When a decision supersedes an earlier one:
- Create the new DR documenting the new decision
- Move the old DR file to docs/design/design-records/superseded/
- Update the DR index (docs/design/design-records/README.md) to show the superseding relationship
- The new DR should reference the old DR in its "Related Decisions" section

### When to Create a Design Record

Create a DR when the decision:

- Affects architecture - System structure, component relationships
- Has alternatives - Multiple valid approaches were considered
- Involves trade-offs - Choosing one thing means giving up another
- Has long-term impact - Will be hard to change later
- Needs explanation - Future developers will ask "why did we do it this way?"

Don't create DRs for:

- Trivial implementation details (variable names, file organization)
- Decisions with only one reasonable option
- Temporary/experimental code
- Standard practices (following language conventions)

### Question Types to Ask

Architecture Questions:
- How should the system be structured?
- What are the major components?
- How do components communicate?
- What are the boundaries?

Technology Questions:
- Which framework/library should we use?
- What database/storage approach?
- What build/deployment tools?
- What testing strategy?

Design Questions:
- What are the main entities/models?
- What are the key workflows?
- How should errors be handled?
- What are the extension points?

Process Questions:
- What's the development workflow?
- How do we ensure quality?
- What's the release process?
- How do we handle versioning?

Security Questions:
- How will authentication work?
- What authorization model should we use?
- How do we protect sensitive data?
- How are secrets/credentials managed?
- What are the security requirements?

Performance/Scalability Questions:
- What are the performance requirements?
- How will this scale?
- What are the known/potential bottlenecks?
- What caching strategy should we use?
- How do we handle high load?

Data Questions:
- What's the data lifecycle?
- How do we handle data privacy?
- What's the backup/recovery strategy?
- How do we handle data migrations?
- What's the data retention policy?

Integration Questions:
- What external services do we integrate with?
- How do we handle third-party APIs?
- What happens when dependencies are unavailable?
- How do we manage API versioning?
- What are the integration failure modes?

## Current Design Status

### Design Records

See `docs/design/design-records/README.md` for complete index of all design decisions.

### Open Design Questions

Priority 1 (Must decide before implementation):

- [ ] _Question that needs answering_

Priority 2 (Should decide soon):

- [ ] _Question that needs answering_

Priority 3 (Can decide later):

- [ ] _Question that needs answering_

_Update this list as questions are identified and resolved_

## Next Steps

### Immediate Next Decision

Decision needed: [What needs to be decided next?]

Why now: [Why is this the next decision to make?]

Questions to explore:
- [Question 1]
- [Question 2]
- [Question 3]

### Ready for Implementation?

Mark each area as design-complete:

- [ ] Architecture - System structure defined
- [ ] Technology Stack - Tools/frameworks chosen
- [ ] Core Models/Entities - Data structures defined
- [ ] Key Workflows - Main use cases designed
- [ ] Error Handling - Error strategy defined
- [ ] Testing Strategy - How to test defined
- [ ] Security - Auth/data protection defined (if applicable)
- [ ] Performance/Scalability - Requirements and approach defined (if applicable)
- [ ] Data Management - Lifecycle and privacy defined (if applicable)
- [ ] Integration - External dependencies defined (if applicable)
- [ ] Deployment - How to deploy defined

Design Phase Complete When:
- All Priority 1 questions answered
- All items above checked or marked as not applicable
- User agrees design is sufficient to start implementation

## Transition to Implementation

When design is complete (or at MVP readiness):

1. Archive this PROJECT.md:
   ```bash
   cp PROJECT.md docs/archive/$(date +%Y-%m-%d)-design-phase.md
   ```

2. Copy implementation template:
   ```bash
   cp docs/templates/PROJECT-phase2-implementation.md PROJECT.md
   ```

3. Update the new PROJECT.md by copying project details from this document:
   - Copy Project Name from "Project Overview" section above (replace in title and Project Overview section)
   - Copy Type from "Project Overview" section above
   - Copy Languages from "Project Overview" section above
   - Copy Description from "Project Overview" section above
   - Copy the Started date from this document
   - Set Last Updated to today's date (YYYY-MM-DD format)

4. Populate the Design Decisions Reference section:
   - Fill in "Critical DRs for Implementation" table with 3-5 most important DRs
   - Update "Design Summary by Area" sections with actual DR numbers and titles
   - Reference specific DRs that guide implementation in each area

5. Report to user:
   ```
   Design phase complete. PROJECT.md has been updated for implementation phase.

   Ready to begin implementation.
   ```

---

## Notes for AI Agents

### Reading Order

1. This document (PROJECT.md) - Current context and status
2. docs/design/dr-writing-guide.md - How to write DRs
3. docs/design/design-records/README.md - DR index
4. All DRs in docs/design/design-records/ - Design decisions made so far
5. AGENTS.md - General agent guidance and project info

### Agent Instructions

When starting a design session:
- Read all existing DRs to understand current state
- Review "Open Design Questions" section
- Ask user which area they want to focus on
- If no direction given, suggest tackling Priority 1 questions

During design discussion:
- Ask clarifying questions
- Suggest alternatives user may not have considered
- Play devil's advocate to ensure decisions are robust
- Point out implications and consequences
- Help user think through edge cases

After each decision:
- Create DR immediately while discussion is fresh
- Update DR index (docs/design/design-records/README.md)
- Identify new questions that emerged
- Add new questions to "Open Design Questions"
- Remove answered questions from "Open Design Questions"

Session continuity:
- Update "Last Updated" date at top of this document
- Update "Next Steps" section with current context
- Ensure next agent can pick up where you left off

### DR Numbering

DRs are numbered sequentially starting from 001:
- `dr-001-first-decision.md`
- `dr-002-second-decision.md`
- etc.

Always check `docs/design/design-records/` to find the next number.

### Quality Checks

Before creating a DR, ensure:
- [ ] Decision is significant (not trivial)
- [ ] Alternatives were considered
- [ ] Trade-offs are understood
- [ ] Context explains the "why"
- [ ] Consequences (both positive and negative) are documented
- [ ] Related DRs are cross-referenced

---

## Resources

- DR Writing Guide: `docs/design/dr-writing-guide.md`
- DR Index: `docs/design/design-records/README.md`
- Agent Guide: `AGENTS.md`
- Brainstorming: `docs/thoughts.md`
