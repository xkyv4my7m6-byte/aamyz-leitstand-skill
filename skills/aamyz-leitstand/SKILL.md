---
name: aamyz-leitstand
description: Keep a team's local status board current while an AI agent works. Report starts, meaningful progress, waiting, blockers, evidence-backed completion, and session end. Use when the host provides a status reporter; this skill does not include a server.
metadata:
  short-description: Visible, evidence-based agent status
---

# AAMYZ Leitstand

Use this skill when an AI agent is doing work that a person needs to follow, especially work involving files, services, builds, deployments, devices, or network access.

## Find the status reporter first

1. Read the current project's `AGENTS.md`, `CLAUDE.md`, or equivalent instructions for the team's status-board command or integration.
2. Use that existing reporter exactly as documented. Do not guess command names, endpoints, paths, or credentials.
3. If there is no configured reporter, say so and provide concise progress in the conversation. Do not install a server, create a webhook, or send data to an external service unless the user explicitly asks.

## Report the work accurately

- **Start:** Before the first consequential action, state the intended result in one sentence.
- **Progress:** After a meaningful stage change, state what was done or what is being checked. Keep the update short and factual.
- **Waiting:** Say what process or input you are waiting for. Resume with an update when it changes.
- **Blocked:** Name the missing dependency or decision and who or what can provide it.
- **Complete:** Report completion only when the result has observable evidence, such as a test result, output file, checksum, or confirmed service response. Include the evidence location or concise result.
- **End:** Close the status entry using the reporter's documented end action.

Never mark an unfinished or unverified task complete. Separate observed facts from assumptions. Do not claim that a board update, test, deployment, or download happened unless the tool returned evidence.

## Protect private information

Keep passwords, API keys, tokens, authentication codes, private customer data, and personal records out of status messages. Report only what is necessary to understand the task and its state. Respect the user's restrictions on which files, systems, and services may be touched.

## Boundaries

This package contains workflow instructions only. It does not include a dashboard, status API, credentials, an AI model, AAMYZ KI, or telemetry. A compatible status reporter must already exist for updates to appear in a separate dashboard. Users choose and configure their own AI model and tools.
