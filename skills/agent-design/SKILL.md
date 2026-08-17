---
name: agent-design
description: Plan an AI agent before writing code — define its goal, tools, state, and failure handling. Use when starting any new agent project, before implementation.
---

# Agent Design Planner

## When to use
- Before building any new agent (LangGraph, custom loop, etc.).
- When an existing agent feels messy and needs a redesign.

## Instructions
Answer these questions and write the result as a short design doc before coding:

1. **Goal** — What exact task does the agent complete? What does "done" look like?
2. **Inputs/Outputs** — What does it receive, what does it produce?
3. **Tools** — Which tools does it need? Keep the list minimal.
4. **State** — What must be remembered between steps?
5. **Control flow** — Single loop, graph, or multi-agent? Draw the flow.
6. **Failure handling** — What happens on tool errors, bad outputs, infinite loops?
7. **Evaluation** — How will you know it works? Define 3–5 test cases.

## Conventions / Rules
- Start with the simplest design that could work (single agent, few tools).
- Only add multi-agent orchestration when a single agent clearly fails.

## TODO
- Add a design-doc template file in `references/`.
