# [Project Name] - Implementation Phase

**Phase:** Implementation
**Status:** In Progress
**Started:** [Date]
**Last Updated:** [Date]

This document guides AI agents through the implementation phase of this project using Documentation Driven Development (DDD).

**IMPORTANT:** All design decisions have been documented as Design Records (DRs) in `docs/design/design-records/`. Implementation must follow these decisions.

---

## Project Overview

**Project Name:** [Project Name]
**Type:** [CLI tool / web application / library / API service / etc.]
**Languages:** [Programming language(s)]
**Description:** [1-2 sentence description]

## Implementation Phase Objectives

The implementation phase translates design decisions into working code. You will:

1. **Read all DRs** to understand design decisions and rationale
2. **Implement according to DRs** - Follow the decisions that were made
3. **Reference DRs in code** - Link code to the decisions that drove it
4. **Flag design gaps** - Identify when implementation needs a decision that wasn't made
5. **Deliver working software** - Build the system as designed

## How to Work in Implementation Phase

### Your Role as Implementation Agent

You are here to:

- **Implement the design** - Write code that realizes the DRs
- **Follow decisions** - Don't second-guess design choices (they're in DRs)
- **Ask when unclear** - If a DR is ambiguous, ask for clarification
- **Reference DRs** - Add comments linking code to relevant DRs
- **Identify gaps** - If you need a decision that wasn't made, flag it
- **Write tests** - Follow the testing strategy from DRs
- **Maintain quality** - Follow code style and best practices from DRs

### Implementation Session Workflow

1. **Read design context**
   - Review all DRs before starting
   - Understand the complete system design
   - Identify key decisions that affect your current task

2. **Plan implementation**
   - Break down into implementable units
   - Identify dependencies
   - Determine implementation order

3. **Implement**
   - Write code following DR decisions
   - Add comments referencing relevant DRs (e.g., `// See DR-042 for rationale`)
   - Follow established patterns from DRs

4. **Test**
   - Write tests according to testing strategy DRs
   - Ensure tests cover decision points

5. **Review against DRs**
   - Verify implementation matches design decisions
   - Check that all DR requirements are met

6. **Update status**
   - Mark tasks complete in this PROJECT.md
   - Document any new DRs if implementation reveals needed decisions
   - Keep PROJECT.md current for next session

### When Design Doesn't Cover Something

If you encounter a situation where:
- No DR exists for a needed decision
- Existing DR is ambiguous or incomplete
- Implementation reveals a design gap

**Do this:**

1. **Stop implementation** of that specific part
2. **Document the question** - What decision is needed?
3. **Ask the user** - Present the question and options
4. **Create a DR** - Document the decision (even in implementation phase)
5. **Resume implementation** - Continue with the new decision

**Note:** Small implementation details don't need DRs. Only create new DRs for decisions with alternatives, trade-offs, or lasting impact.

## Design Decisions Reference

### All Design Records

See `docs/design/design-records/README.md` for complete index.

**Critical DRs for Implementation:**

| DR # | Title | Category | Why Critical |
| ---- | ----- | -------- | ------------ |
| -    | -     | -        | -            |

_Update this table to highlight DRs that are especially important for implementation_

### Design Summary by Area

#### Architecture
- **DR-XXX:** [Key architectural decision]
- **DR-XXX:** [Key architectural decision]

#### Technology Stack
- **DR-XXX:** [Framework/library choice]
- **DR-XXX:** [Database/storage choice]
- **DR-XXX:** [Build/tooling choice]

#### Core Models/Entities
- **DR-XXX:** [Data model decision]
- **DR-XXX:** [Entity relationship decision]

#### Key Workflows
- **DR-XXX:** [Main workflow design]
- **DR-XXX:** [Error handling strategy]

#### Testing Strategy
- **DR-XXX:** [Testing approach]
- **DR-XXX:** [Test coverage goals]

#### Deployment
- **DR-XXX:** [Deployment strategy]
- **DR-XXX:** [Environment setup]

_Update these sections with actual DR numbers and titles as you populate this document_

## Implementation Status

### Setup and Infrastructure

- [ ] Development environment setup
- [ ] Project structure created
- [ ] Dependencies installed
- [ ] Build system configured
- [ ] CI/CD pipeline setup (if applicable)
- [ ] Testing framework setup

### Core Implementation

**Module/Component:** [Component Name]
- [ ] Task 1
- [ ] Task 2
- [ ] Task 3

**Module/Component:** [Component Name]
- [ ] Task 1
- [ ] Task 2
- [ ] Task 3

_Organize by components/modules/features as appropriate for your project_

### Testing

- [ ] Unit tests for [component]
- [ ] Integration tests for [workflow]
- [ ] End-to-end tests for [feature]
- [ ] Test coverage meets goals (see DR-XXX)

### Documentation

- [ ] Code documentation (docstrings, comments)
- [ ] API documentation (if applicable)
- [ ] User guides (if applicable)
- [ ] README updated

### Deployment Readiness

- [ ] Production build tested
- [ ] Deployment scripts/configs created
- [ ] Environment variables documented
- [ ] Deployment guide written

## Current Focus

### What We're Working On Now

**Current Task:** [Specific task being implemented]

**Related DRs:**
- DR-XXX: [Title] - [Why it matters for this task]
- DR-XXX: [Title] - [Why it matters for this task]

**Progress:**
- [x] Completed step
- [ ] In progress step
- [ ] Pending step

**Blockers:**
- [Description of any blockers]

### Next Up

After current task completes:

1. [Next task]
2. [Following task]
3. [Task after that]

## Technical Setup

### Development Environment

**Prerequisites:**
- [Requirement 1]
- [Requirement 2]
- [Requirement 3]

**Setup Steps:**
```bash
# Installation commands
```

**Running in Development:**
```bash
# Development commands
```

**Running Tests:**
```bash
# Test commands
```

**Building for Production:**
```bash
# Build commands
```

### Project Structure

```
project-root/
├── src/              # [Purpose]
├── tests/            # [Purpose]
├── docs/             # Documentation
│   ├── design/       # Design Records
│   └── [other]/      # [Other doc types]
├── [other dirs]      # [Purpose]
└── README.md
```

_Update with actual project structure_

### Code Style Guidelines

**See DR-XXX for complete code style decisions**

Key points:
- [Style guideline 1]
- [Style guideline 2]
- [Style guideline 3]

## Notes for AI Agents

### Reading Order

1. **This document (PROJECT.md)** - Current implementation context and status
2. **docs/design/design-records/README.md** - Index of all design decisions
3. **All DRs in docs/design/design-records/** - Complete design (critical!)
4. **AGENTS.md** - General agent guidance and project info
5. **Existing codebase** - What's already implemented

### Agent Instructions

**When starting an implementation session:**
- Read all DRs (or at minimum, the critical ones listed above)
- Review "Current Focus" section for context
- Check "Implementation Status" to see what's done
- Ask user what to work on, or continue from "Next Up"

**During implementation:**
- Keep DRs in mind - implement according to decisions
- Add comments linking code to DRs when implementing decision points
  ```python
  # Use PostgreSQL for persistence (see DR-023)
  # Chose connection pooling to handle concurrent requests (see DR-031)
  ```
- If you discover a missing decision, document it and ask
- Write clean, maintainable code following project guidelines
- Write tests as you go (don't leave for later)

**After implementing:**
- Update "Implementation Status" checkboxes
- Update "Current Focus" section
- Update "Next Up" section
- Ensure next agent knows what to work on

**Session continuity:**
- Update "Last Updated" date at top of this document
- Ensure PROJECT.md reflects current state
- If you create new DRs (for gaps), update DR index

### Referencing DRs in Code

When implementing a decision point, add a comment:

**Good examples:**
```python
# Singleton pattern for database connection (DR-015)
class DatabaseConnection:
    _instance = None
```

```javascript
// Retry with exponential backoff for API calls (DR-028)
async function fetchWithRetry(url, maxRetries = 3) {
```

```go
// Use channels for worker pool communication (DR-041)
jobs := make(chan Job, 100)
```

**When to add DR references:**
- Architectural patterns
- Algorithm choices
- Error handling approaches
- Performance optimizations
- Security measures
- Any non-obvious choice that has a DR

### Quality Checks

Before marking a component complete:
- [ ] Implements all requirements from relevant DRs
- [ ] Follows code style guidelines from DRs
- [ ] Has tests (unit, integration as appropriate)
- [ ] Has documentation (code comments, docstrings)
- [ ] References relevant DRs in code comments
- [ ] Passes all tests
- [ ] Follows security guidelines from DRs (if applicable)

### If You Need to Deviate from a DR

Sometimes implementation reveals that a design decision needs revision. If this happens:

1. **Don't just change it** - The DR exists for a reason
2. **Discuss with user** - Explain why the decision doesn't work
3. **Create new DR** - Document the new decision and mark old one as superseded
4. **Update code** - Implement the new decision
5. **Update DR index** - Reflect the superseding relationship

---

## Resources

- **DR Index:** `docs/design/design-records/README.md`
- **DR Writing Guide:** `docs/design/dr-writing-guide.md`
- **Agent Guide:** `AGENTS.md`
- **Code:** [Link to main source directory]
- **Tests:** [Link to test directory]
