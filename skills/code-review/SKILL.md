---
name: code-review
description: Review code changes against my personal checklist for correctness, security, and style. Use when asked to review code, a diff, or a pull request.
---

# Personal Code Review Checklist

## When to use
- Reviewing my own changes before commit/PR.
- Reviewing someone else's PR or a diff.

## Instructions
Go through the checklist and report findings ranked by severity:

- I want you to review my codebase like a real engineer with 10 years of experience.
- If the user says to check the whole codebase, then understand and check all the code. If the user says to review my current changes, then use `git diff` and check only those changes.
- Here are some scenarios you need to check:
- Make sure the code follows best practices on every line, including error handling and good coding practices.
- Check whether the code has any security issues, and also consider what happens when this application is under load.
- If there are test cases in the project, run them and verify things work the correct way.

## Conventions / Rules
- Report only real issues — no nitpicks about formatting a formatter handles.
- For each finding: file, line, what's wrong, and a suggested fix.

## TODO
- Add stack-specific checks (Next.js, FastAPI, LangGraph) as I learn what breaks.
