---
model: claude-haiku-4-5-20251001 
allowed-tools: Bash(git add:*), Bash(git status:*), Bash(git commit:*)
description: Create a git commit in angular convention
---

## Context

- Current git status: !`git status`
- Current git diff (staged and unstaged changes): !`git diff HEAD`
- Current branch: !`git branch --show-current`
- Recent commits: !`git log --oneline -2`

## Your task

Based on the above changes, create a single git commit following the Angular convention.

**IMPORTANT**: The commit message must NOT include:
- "Co-Authored-By: Claude <noreply@anthropic.com>"
- "🤖 Generated with [Claude Code](https://claude.com/claude-code)"
- Any other attribution or semantic phrases

The commit message should only contain the commit type, scope (if applicable), and description of the changes.

You have the capability to call multiple tools in a single response. Stage and create the commit using a single message. Do not use any other tools or do anything else. Do not send any other text or messages besides these tool calls.