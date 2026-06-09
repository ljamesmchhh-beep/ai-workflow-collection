# AI Workflow Collection

A personal collection of AI-powered workflows for software development and career exploration. Built with Claude, Codex, and Hermes Agent.

## What's in here

### 🔧 Code Change Workflow
A strict 11-step plan-test-implement-review-commit-push workflow for making safe code changes.

Designed to prevent the most common mistakes:
- Coding before defining success criteria
- Skipping regression tests
- Pushing without CI follow-up

Originally a Hermes Agent skill, adapted for use with Claude Projects and Codex.

→ [`workflows/code-change-workflow.md`](workflows/code-change-workflow.md)

### 🎨 Claude Design → Claude Code Redesign Workflow
A 6-step workflow for redesigning an existing app with AI while keeping backend logic safe.

Core idea: Claude handles design judgment, Claude Code handles safe implementation.

→ [`workflows/claude-design-workflow.md`](workflows/claude-design-workflow.md)

### 🧭 Career Exploration Workflow (Claude Project Prompt)
A Claude Project instruction set that acts as a career direction analyst.

Through natural conversation, it tracks your interests, strengths, blind spots, and skill gaps — then maps them to concrete job titles with honest gap analysis.

→ [`workflows/career-exploration-prompt.md`](workflows/career-exploration-prompt.md)

## How to use

Each workflow is a standalone markdown file. You can:
- Drop it into a **Claude Project** as Instructions
- Use it as a **Hermes Agent skill**
- Reference it manually when working with any AI coding assistant

## Background

Built while figuring out how to actually use AI tools in a real workflow — not just chat, but structured, repeatable processes that produce consistent results.

## License

MIT
