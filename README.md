# prompt-automation-demo
Demo project for AI prompt-driven workflow automation

## Overview
In large engineering teams:
- Bugs and feature requests are often discussed informally
- Context is lost across chats, meetings, emails
- Jira tickets are created late, incosistently or with missing information

This leads to:
- Poor visibilty
- Delayed work
- Increased rework

---

## Solution Approach
This project simulates an **AI-assisted entry point into Jira workflows** by:

- Allowing developers to describe bugs or features using simple Markdown prompts
- Automatically processing these prompts using GitHub Actions
- Generating structured issue summaries that resemble Jira tickets

---

## How the Workflow works
1. A developer adds a Markdown file (`.md`) inside the `prompts/` directory
2. A GitHub Actions workflow is triggered automatically on commit
3. The workflow parses the Markdown file to extract:
   - **Issue Title**
   - **Context**
   - **Instructions**
   - **Priority**
   - **Assignee**
4. A structured issue summary is generated in the workflow logs  
5. In a real enterprise setup, this output would be sent to Jira using an AI agent via Atlassian MCP

---

## Example Prompt Format

```markdown
# Feature Request

## Context
Users want a dark mode for better night-time usage.

## Instructions
- Create a feature request issue
- Priority: Medium
- Label: enhancement

```
## Example Output

Issue Title: Feature Request
Context:
Users want a dark mode for better night-time usage.

Instructions:
- Create a feature request issue
- Priority: Medium
- Label: enhancement

Assigned to: developer1
Priority: Medium


