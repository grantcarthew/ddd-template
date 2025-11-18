# Documentation Driven Development (DDD) Template

A template repository for building software projects where design decisions come first, captured as Design Records before (or during) implementation. Built for collaboration between humans and AI agents.

## What is Documentation Driven Development?

Documentation Driven Development is a development approach where you:

1. **Think first, code later** - Make explicit design decisions before implementation
2. **Document the "why"** - Capture not just what you built, but why you chose that approach
3. **Create Design Records (DRs)** - Formal documents for each significant technical decision
4. **Build institutional memory** - Future developers (including AI agents) understand the reasoning behind choices

Unlike traditional "documentation after the fact," DDD makes documentation a first-class part of the design process.

## Why Use This Approach?

- **Better decisions** - Discussing alternatives and trade-offs upfront leads to more thoughtful choices
- **AI agent continuity** - Agents can pick up where previous sessions left off by reading DRs
- **Reduced churn** - Documented decisions prevent revisiting the same questions repeatedly
- **Team alignment** - Everyone understands not just what was built, but why
- **Knowledge preservation** - Critical context survives beyond the original developers

## Quick Start

1. **Copy this template to your new project:**
   ```bash
   cp -r documentation-driven-development-template/ my-new-project/
   cd my-new-project/
   rm -rf .git
   git init
   ```

2. **Start with an AI agent** using this prompt:
   ```
   I'm starting a new project using Documentation Driven Development.

   Please read PROJECT.md first, then follow the bootstrap instructions
   to help me set up the project structure.

   After that, we'll move into the design phase where we'll create
   Design Records for all major decisions.
   ```

3. **The agent will:**
   - Ask you questions about your project
   - Create appropriate directory structure
   - Update AGENTS.md with basic info
   - Guide you through Phase 0 → Phase 1 transition

4. **Begin designing:**
   - Work interactively with the agent to make design decisions
   - Each decision becomes a Design Record
   - Build up a complete design before coding

5. **Implement:**
   - Transition to Phase 2
   - Write code that follows the DRs
   - Reference decisions in your code comments

## How It Works

This template guides you through three phases:

### Phase 0: Bootstrap
Set up the project structure, gather basic information, create initial directories. Quick and minimal.

### Phase 1: Design
The most important phase. Work with an AI agent (or team) to:
- Ask probing questions about the project
- Explore alternatives for each decision
- Document decisions as Design Records
- Build a complete design before implementation

### Phase 2: Implementation
Write code guided by the design decisions:
- Reference DRs in your code comments
- Follow the decisions that were made
- Flag gaps when implementation reveals missing decisions

Each phase has its own PROJECT.md template that gets copied to the root, updated, then archived when transitioning to the next phase.

## Repository Structure

```
.
├── PROJECT.md                    # Phase 0: Bootstrap guide (gets replaced each phase)
├── AGENTS.md                     # Agent instructions (grows throughout project)
├── LICENSE                       # MIT license with template usage notice
├── docs/
│   ├── design/
│   │   ├── dr-writing-guide.md  # How to write Design Records
│   │   ├── README.md            # Design docs overview
│   │   └── design-records/      # Individual DR files go here
│   │       ├── README.md        # DR index
│   │       └── superseded/      # Replaced DRs (kept for history)
│   ├── templates/
│   │   ├── PROJECT-phase1-design.md        # Template for design phase
│   │   └── PROJECT-phase2-implementation.md # Template for implementation phase
│   ├── archive/                 # Archived PROJECT.md files from completed phases
│   └── thoughts.md              # Brainstorming and ideas
└── .gitignore
```

## Key Concepts

### Design Records (DRs)

Design Records are structured documents that capture:
- **Context** - What problem are we solving?
- **Decision** - What did we choose?
- **Alternatives** - What else did we consider?
- **Consequences** - What are the trade-offs?

See `docs/design/dr-writing-guide.md` for complete guidelines.

### PROJECT.md Lifecycle

The PROJECT.md file at the root is the "current context" for AI agents:
- **Phase 0** - Bootstrap instructions
- **Phase 1** - Design phase context and open questions
- **Phase 2** - Implementation status and DR references

After each phase completes, archive the current PROJECT.md and copy the next phase template.

### AGENTS.md Evolution

Starts minimal during bootstrap, grows naturally:
- **Bootstrap** - Just name, description
- **Design** - Add architecture decisions, key DRs
- **Implementation** - Add setup commands, code structure
- **Completion** - Fully detailed per https://agents.md/

## Working With AI Agents

This template is optimized for AI agent collaboration:

1. **Agents read PROJECT.md first** - It tells them what phase you're in and what to do
2. **DRs provide continuity** - New agent sessions can catch up by reading DRs
3. **Clear instructions** - Each phase template has explicit agent guidance
4. **Session memory** - "Next Steps" sections help agents know where to continue

## Documentation

- **DR Writing Guide**: `docs/design/dr-writing-guide.md`
- **Phase 0 Bootstrap**: `PROJECT.md` (in root after template copy)
- **Phase 1 Design**: `docs/templates/PROJECT-phase1-design.md`
- **Phase 2 Implementation**: `docs/templates/PROJECT-phase2-implementation.md`

## Examples

Want to see what a good Design Record looks like? Check `docs/design/dr-writing-guide.md` for:
- DR structure and format
- Categories (Architecture, Design, Technical, Process, Product)
- YAML frontmatter examples
- When to create vs. when to skip DRs

## Philosophy

**Documentation Driven Development is about thinking, not bureaucracy.**

Create DRs for decisions that:
- Have multiple valid approaches
- Involve trade-offs
- Will be hard to change later
- Future developers will wonder about

Don't create DRs for:
- Trivial implementation details
- Decisions with only one reasonable option
- Standard practices

The goal is to capture the "why" behind meaningful choices, not document every line of code.

## License

MIT License - See [LICENSE](LICENSE) for details.

When using this template for your own project, you may delete or replace the LICENSE file. The template's license only governs the template files themselves, not projects created from it.

## Contributing

This is a template repository. If you have improvements to the template itself, feel free to fork and adapt to your needs.

---

**Ready to build something thoughtfully?** Copy this template and start your DDD journey.
