# dummy project

An AI developed companion to manage investment decisions and portfolios

## AI-Powered Development Workflow

This project demonstrates a structured AI-assisted development workflow using specialized agents and prompts. Here's how an AI Engineer can go from story writing to implementation to verification:

### 📁 Story-Driven Development (`docs/stories/`)

Stories are the foundation of development. Each story follows a consistent format with:

- User story statement (As a... I want... So that...)
- Acceptance criteria
- Tasks and subtasks
- Dev notes with implementation guidance
- Testing requirements

### 🤖 AI Agents (`.github/agents/`)

Specialized agents handle different aspects of the development lifecycle:

| Agent                      | Purpose                                                                                                                         |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **story-writing.agent.md** | Guides creation of comprehensive user stories with proper structure, acceptance criteria, and dev notes                         |
| **architect.agent.md**     | Analyzes stories against architecture, identifies files to create/modify, validates patterns, and maintains architecture health |
| **ux-review.agent.md**     | Reviews UI/UX stories, validates against best practices, and researches correct Strato components                               |
| **code-reviewer.md**       | Reviews code changes for correctness, security, maintainability, and test coverage                                              |
| **qa-test-validator.md**   | Validates test coverage meets thresholds and ensures all tests pass                                                             |

### ⚡ Reusable Prompts (`.github/prompts/`)

Prompts orchestrate agents and define common workflows:

| Prompt                          | Purpose                                                                              |
| ------------------------------- | ------------------------------------------------------------------------------------ |
| **init.prompt.md**              | Creates/updates `AGENTS.md` with project guidelines for AI agents                    |
| **prepare-story.prompt.md**     | Prepares a story for development by running UX review → Architecture validation      |
| **instrument-logs.prompt.md**   | Adds structured logging following the `[ComponentName]` convention for observability |
| **check-final-story.prompt.md** | Runs code review → QA validation before marking story complete                       |
| **deploy.prompt.md**            | Handles build verification, version bumping, deployment, and git commit              |

### 🔄 Complete Development Workflow

```
┌─────────────────────────────────────────────────────────────────────────┐
│                        AI DEVELOPMENT WORKFLOW                          │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                         │
│  1. STORY CREATION                                                      │
│     └── Use story-writing.agent.md to create detailed story             │
│         └── Output: docs/stories/XXX-feature-name.md                    │
│                                                                         │
│  2. STORY PREPARATION (prepare-story.prompt.md)                         │
│     ├── ux-review.agent.md → Validate UI/UX, identify Strato components │
│     └── architect.agent.md → Analyze architecture, plan implementation  │
│         └── Output: Story enhanced with implementation guidance         │
│                                                                         │
│  3. IMPLEMENTATION                                                      │
│     ├── Follow story tasks and architecture guidance                    │
│     ├── Use instrument-logs.prompt.md for observability                 │
│     └── Reference AGENTS.md for coding standards                        │
│                                                                         │
│  4. VERIFICATION (check-final-story.prompt.md)                          │
│     ├── code-reviewer.md → Review code quality and security             │
│     └── qa-test-validator.md → Validate test coverage (70-90%)          │
│         └── Output: Story marked as complete                            │
│                                                                         │
│  5. DEPLOYMENT (deploy.prompt.md)                                       │
│     ├── Build verification                                              │
│     ├── Version bump (package.json, app.config.json)                    │
│     ├── Deployment to a local server                                    │
│     └── Git commit                                                      │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

### 🚀 Quick Start for AI Engineers

1. **Start a new feature**: Create a story using `story-writing.agent.md`
2. **Prepare for development**: Run `prepare-story.prompt.md` on your story
3. **Implement**: Follow the enhanced story's tasks and architecture guidance
4. **Verify**: Run `check-final-story.prompt.md` to validate code and tests
5. **Deploy**: Run `deploy.prompt.md` to ship to production
6. **Monitor**: Use `app-logs-analyzer.md` to analyze production behavior
