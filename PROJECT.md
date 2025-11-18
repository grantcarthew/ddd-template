# Documentation Driven Development (DDD) Template - Bootstrap Guide

This document guides AI agents through bootstrapping a new DDD project structure.

**IMPORTANT:** Read these documents in order before continuing:

1. `AGENTS.md` - Review the template structure you'll be populating
2. `docs/design/dr-writing-guide.md` - Understand what Design Records are

This guide defines how to bootstrap the minimal project structure to begin the design phase.

---

## Phase 0: Bootstrap Tasks

### Step 1: Gather Project Information

Have an interactive conversation with the user to understand the project. Tailor your questions based on their answers.

Start with the essentials:

- Project name
- Project type (CLI tool, library, web app, API, mobile app, etc.)
- Programming language(s)
- Brief description (1-2 sentences)

Then explore based on project type:

Depending on what kind of project this is, you'll need different information. Ask intelligent follow-up questions. For example:

- CLI tools → Command structure, subcommands, configuration
- Libraries → API surface, usage examples, integration points
- Web applications → Frontend/backend architecture, API endpoints, deployment
- APIs → Endpoints, authentication, request/response formats

Development workflow:

Ask about their development process:

- Setup/installation steps
- Running in development
- Testing approach
- Build process
- Code style preferences (if any)

Documentation needs:

Based on the project type, determine what documentation makes sense. Examples:

- User guides for end-user facing projects
- API docs for libraries/services
- Architecture docs for complex systems
- CLI reference for command-line tools

Adapt your questions as the conversation unfolds.

### Step 2: Create Project-Specific Directory Structure

The template already includes the core DDD structure:

- `docs/archive/` - For archived PROJECT.md files and historical content
- `docs/design/` - For design decisions and Design Records
- `docs/design/design-records/` - For individual DR files
- `docs/templates/` - Phase templates for PROJECT.md lifecycle
- `docs/thoughts.md` - Free-form brainstorming and ideas

Based on the conversation in Step 1, create additional directories as needed for this specific project:

```bash
# Examples based on project type:

# If CLI tool with extensive commands:
mkdir -p docs/cli

# If library or API service:
mkdir -p docs/api

# If complex system needing architecture diagrams:
mkdir -p docs/architecture

# If user-facing product needing guides:
mkdir -p docs/guides
```

Only create directories that make sense for this project. The agent and user will determine what's needed during Step 1.

### Step 3: Populate AGENTS.md (Minimally)

IMPORTANT: AGENTS.md should remain minimal during bootstrap to avoid churn. It will naturally grow and evolve throughout the design and implementation phases as the project matures. Only add what you know from Step 1.

Update only these parts:

- `[Project Name]` → Actual project name
- `TODO: Brief project description` → The 1-2 sentence description from Step 1
- Leave "Quick Reference" as TODO - it will be populated during design/implementation
- Keep everything else unchanged

The AGENTS.md document will be enriched later:

- Design phase: Add architecture decisions, design patterns, key DRs
- Implementation phase: Add setup commands, development workflow, code structure
- Near completion: Fully detailed following https://agents.md/ specification

Do NOT try to fill in details that aren't yet known. Premature detail causes unnecessary updates as decisions change.

### Step 4: Create Project-Specific Documentation Stubs

For each project-specific directory created in Step 2, create a README.md file to explain its purpose and structure.

CLI Documentation (if `docs/cli/` was created):

```markdown
# CLI Command Reference

Complete reference for all [Project Name] commands.

## Commands

TODO: List commands as they are designed/implemented

## Documentation Format

Each command will be documented with:

- Usage and syntax
- Description
- Options and flags
- Examples
- Related commands
```

API Documentation (if `docs/api/` was created):

```markdown
# API Reference

Complete reference for [Project Name] API.

## Endpoints

TODO: Document endpoints as they are designed/implemented

## Common Patterns

TODO: Authentication, error handling, request/response formats as they are decided
```

Architecture Documentation (if `docs/architecture/` was created):

```markdown
# Architecture

High-level architecture and system design for [Project Name].

## Overview

TODO: System architecture overview (add during design phase)

## Components

TODO: Major components and their responsibilities (add during design phase)

## Design Decisions

See [design/design-records/](../design/design-records/) for detailed design decisions.
```

User Guides (if `docs/guides/` was created):

```markdown
# User Guides

Guides and tutorials for using [Project Name].

## Getting Started

TODO: Quick start guide (add during implementation phase)

## Guides

TODO: Add specific guides as features are implemented
```

Adapt these templates based on what makes sense for this specific project.

### Step 5: Create Project README.md

Replace the template's README.md with a project-specific README:

1. Delete or rename the template README.md:
   ```bash
   mv README.md README-template.md
   ```

2. Create a new README.md for this project with:
   - Project name and description
   - What the project does
   - How to install/setup
   - How to use it
   - Link to documentation

3. Include a Documentation section:
   ```markdown
   ## Documentation

   Complete documentation is available in the `docs/` directory:

   - `docs/guides/` - User guides and tutorials
   - `docs/design/` - Design decisions and architecture
     [Add other relevant doc directories based on project type]

   For AI agents working on this project, see [AGENTS.md](AGENTS.md).
   ```

### Step 6: Verify Bootstrap Complete

Confirm all files are created:

Essential files (already in template):

- [x] `AGENTS.md` - Populated with project name and description
- [x] `docs/design/dr-writing-guide.md` - DR writing guidelines
- [x] `docs/design/README.md` - Design documentation intro
- [x] `docs/design/design-records/README.md` - DR index
- [x] `docs/thoughts.md` - Brainstorming space

Conditional files (based on Step 1 conversation). Some examples might be:

- [ ] `docs/cli/README.md` (if CLI project)
- [ ] `docs/api/README.md` (if API project)
- [ ] `docs/architecture/README.md` (if complex architecture)
- [ ] `docs/guides/README.md` (if user guides needed)

README updated:

- [ ] Main README.md references docs/ structure

### Step 7: Report to User and Transition

Provide summary of created structure, then transition to design phase:

```
✓ DDD project structure initialized

Template structure:
- AGENTS.md updated with project basics
- Design Records system ready (docs/design/design-records/)
- DR writing guide available (docs/design/dr-writing-guide.md)
- Thoughts document for brainstorming (docs/thoughts.md)
- Archive directory for completed phases (docs/archive/)

[List any project-specific directories created]
```

Now transition to design phase:

1. Archive this bootstrap PROJECT.md:
   ```bash
   cp PROJECT.md docs/archive/$(date +%Y-%m-%d)-bootstrap.md
   ```

2. Copy design phase template:
   ```bash
   cp docs/templates/PROJECT-phase1-design.md PROJECT.md
   ```

3. Update the new PROJECT.md with project details from Step 1:
   - Replace `[Project Name]` with actual project name (in title and Project Overview section)
   - Replace `[Type]` with project type (CLI tool, library, web app, etc.)
   - Replace `[Languages]` with programming languages
   - Replace `[Description]` with the 1-2 sentence description
   - Set `[Started]` to today's date (YYYY-MM-DD format)
   - Set `[Last Updated]` to today's date (YYYY-MM-DD format)

4. Report to user:
   ```
   Bootstrap phase complete. PROJECT.md has been updated for design phase.

   Ready to begin creating Design Records.
   ```
