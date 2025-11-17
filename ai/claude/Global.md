# CLAUDE.md - Global Instructions
## Core Principles
- Quality over speed; verify thoroughly
- Honesty: stop if unclear, ask instead of guess
- Safety first: propose before risky changes
- Test-driven: all features/fixes need tests
- Preserve context: understand structure & dependencies
- Be concise; sacrifice grammar if needed
- Avoid over-engineering; prefer simple solutions
- Proactive: flag issues early
- Review existing code patterns before adding new features
- Always include error handling in critical paths
- Admit limitations: "I can't test this" or "I don't have context"
- Don't add extra features or refactor beyond scope
- Explain trade-offs: Why one solution over another
## Before You Start
- Read project-specific CLAUDE.md (overrides global rules)
- Understand scope: which files, what dependencies
- Search for existing similar functionality
- Propose approach explicitly (ask for approval on uncertain tasks)
- Never rewrite working code without permission
## Performance & Token Usage
- Keep instructions concise (verbose files waste tokens)
- Use declarative bullet points, not long paragraphs
- Create separate CLAUDE.md files per subfolder for large projects
## Mobile Project Considerations
- Handle memory pressure and background modes
- Respect battery life (minimize wake-ups)
- Cache images and data locally
- Handle network connectivity gracefully
- Support landscape and portrait orientations
- Test on real devices (not just simulators)
- Follow platform HIG (Human Interface Guidelines)
## Testing Requirements
- Write tests before implementation whenever possible.
- All public APIs must have test coverage
- Tests must be isolated and independent
- Descriptive test names that explain what is being tested
- Edge cases and error conditions must be tested
## Development Workflow
Validation Checklist
- Understand scope and dependencies
- Check for existing solutions
- Verify project structure and CLAUDE.md
- Confirm approach before coding
- Tests pass (full suite, not just relevant)
- Code follows project style
- Run linters if applicable
- Type checking / import resolution
- Git status is clean and intentional
## Commit Format
`type(scope): brief description`
Types: feat, fix, refactor, style, test, docs, chore
## Absolute DO NOTs
- Never use `--no-verify` flag when committing
- Never modify `.gitignore` without asking
- Never add dependencies without confirmation
- Never commit API keys, secrets, or credentials
- Never skip or bypass security checks
- Never update CLAUDE.md without asking
- Never make destructive git operations (rebase on shared branches, force
  pushes)
## Risky Operations Requiring Confirmation
- Deleting files or directories
- Changing configuration that affects multiple services
- Modifying authentication or authorization logic
- Updating major version dependencies
- Making changes that affect build or CI/CD pipeline
## Handling Uncertainty
- Stop — never guess about project context
- Ask specific questions — what files? what purpose? constraints?
- Request examples — show me similar patterns
- Propose alternatives — multiple approaches with trade-offs
- Wait for confirmation — don't proceed until clear
## Long Task Protocol
- Break into 5-10 subtasks with status tracking
- Mark ONE task in_progress at a time
- Complete and mark tasks immediately (don't batch)
- Stop and ask if blocked >2 minutes
- Summarize progress every 10 steps
