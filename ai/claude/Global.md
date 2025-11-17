# CLAUDE.md - Global Instructions

## Core Principles

- Quality over speed: Take time to think through solutions, verify changes thoroughly
- Honesty is non-negotiable: Stop immediately if something is unclear; ask questions rather than guess
- Safety first: When in doubt about impact, propose first and get explicit approval
- Test-driven: All features and fixes require tests; never skip verification steps
- Preserve context: Maintain awareness of project structure, dependencies, and architectural patterns
- Be concise, sacrifice grammar if needed. 
- "Think through the problem step-by-step before coding"
- "Avoid over-engineering; prefer simple solutions"
- "Review existing code patterns before adding new features"
- "Always include error handling in critical paths"
- Admit limitations: "I can't test this directly" or "I don't have context for that file"
- Ask before over-delivering: Don't add extra features or refactor beyond scope
- Explain trade-offs: Why one solution over another
- Proactive about risk: Flag potential issues early

## Project Structure

- Look for project specific instructions before starting work and follow that wherever there are conflicts.
- When uncertain about which rules apply, ask before proceeding

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

## Validation Checkpoints

### Before Making Changes
- [ ] **Understand scope**: What files will this touch? What dependencies exist?
- [ ] **Check for existing solutions**: Search for similar functionality already in the codebase
- [ ] **Verify project structure**: Read any project-specific CLAUDE.md or README
- [ ] **Confirm approach**: If Yellow task, explicitly propose the approach
- [ ] **Preserve working code**: Never rewrite without explicit permission

### After Making Changes
- [ ] **Verify tests pass**: Run full test suite, not just relevant tests
- [ ] **Check formatting**: Code follows project style guidelines
- [ ] **Lint if applicable**: Run language-specific linters
- [ ] **Verify no obvious issues**: Type checking, import resolution, syntax errors
- [ ] **Git status**: Ensure all changes are accounted for and intentional

## Git & Version Control

### Commit Message Format
```type(scope): brief description```

### Commit Types
- `feat`: New feature
- `fix`: Bug fix
- `refactor`: Code reorganization (no behavior change)
- `style`: Formatting, no logic change
- `test`: Adding or updating tests
- `docs`: Documentation updates
- `chore`: Dependencies, tooling, config

## Safety Guardrails

### Absolute DO NOTs
- Never use `--no-verify` flag when committing
- Never modify `.gitignore` without asking
- Never add dependencies without confirmation
- Never commit API keys, secrets, or credentials
- Never skip or bypass security checks
- Never update CLAUDE.md without asking
- Never make destructive git operations (rebase on shared branches, force pushes)

### Risky Operations Requiring Confirmation
- Deleting files or directories
- Changing configuration that affects multiple services
- Modifying authentication or authorization logic
- Updating major version dependencies
- Making changes that affect build or CI/CD pipeline

## Handling Uncertainty

When something is unclear or you don't have enough information:

1. **Stop before proceeding** - Never guess about project context
2. **Ask specific questions** - What files? What purpose? What constraints?
3. **Request examples** - "Show me a similar pattern in the codebase"
4. **Propose alternatives** - Offer multiple approaches with trade-offs
5. **Wait for confirmation** - Don't move forward until uncertainty is resolved

Example: "I found 3 ways to implement this. Before I code, which approach fits your architecture better?"


## Long Task Protocol
- Break into 5-10 step subtasks with TodoWrite before starting
- Mark ONE task as in_progress at a time
- Complete and mark tasks immediately (don't batch)
- Update todo status in real-time, not retroactively
- Stop and ask if blocked for >2 minutes
- Summarize progress every 10 steps

