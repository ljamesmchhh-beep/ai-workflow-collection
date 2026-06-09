---
name: claude-design-workflow
description: A 6-step workflow for redesigning an existing app with AI while keeping backend logic, auth, billing, and core behavior safe.
version: 1.0.0
author: ljamesmchhh-beep
license: MIT
---

# Claude Design → Claude Code Redesign Workflow

## Overview

A two-prompt workflow for redesigning an existing production app with AI while keeping product logic safe.

Core split: Claude handles design judgment (taste, UX, visual direction, components). Claude Code handles safe implementation (branch, tests, build checks, PR).

Core rule:

> Do not let implementation choose the taste. Design first, code second.

## When to Use

Use when you want to redesign an existing app's UI/UX while preserving all backend behavior.

Do not use for:
- Greenfield projects with no existing codebase
- Backend/API changes
- One-off style tweaks that don't need a full redesign branch

## The 6-Step Workflow

### 1. Prepare app context
Collect the repo link, current screenshots, pain points, design inspiration, and constraints Claude must preserve.

### 2. Run Claude Design
Audit the current UI, explore style directions, define design tokens and components, and create a page-by-page redesign plan.

Style directions to choose from:
- **Evolutionary** — improves current product while meaningfully changing layout and hierarchy
- **Strong-fit bold** — best balanced recommendation for the product's audience and workflow
- **Revolutionary** — more distinctive and opinionated; changes composition and storytelling while preserving behavior

### 3. Pick or refine the direction
React in natural language: "warmer," "less generic," "more editorial," "more serious developer tool."

### 4. Download the Claude Design ZIP
Download and unzip the approved design export into the app repo. Do not rely only on a share link — Claude Code needs real local files to inspect and compare.

### 5. Hand off to Claude Code
Use the redesign handoff prompt. Claude Code should:
- Create a dedicated redesign branch
- Implement in stages: tokens → shared components → pages
- Preserve all backend/API/auth/billing behavior unless explicitly approved otherwise
- Run lint, typecheck, and build checks

### 6. Verify and open PR
- Open the rendered app in a browser
- Compare actual UI against the approved design export
- Check responsive states
- Check browser console for errors
- Capture screenshots when possible
- Push branch and open PR for human review

## Safety Rules

- Do not change backend, API, auth, billing, or core product flows without explicit approval
- Important flows, permissions, errors, legal content, and destructive actions must remain visible and working
- Redesign is not a product rewrite

## Verification Checklist

- [ ] Approved design export is local
- [ ] Dedicated redesign branch created
- [ ] Backend/API/auth/billing behavior preserved
- [ ] Tokens and shared components implemented before pages
- [ ] Lint, typecheck, and build pass or caveats documented
- [ ] Rendered app opened in browser
- [ ] Actual UI compared against design export
- [ ] Responsive states checked
- [ ] Browser console checked
- [ ] Branch pushed and PR opened for human review

## Mental Model

Think of this as a relay race, not one giant prompt:

Context → Claude Design → Approved ZIP → Claude Code → PR Review
