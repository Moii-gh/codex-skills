---
name: codex-task-executor
description: Execute programming tasks safely and completely in existing projects or new codebases. Use when the user asks Codex to implement, fix, refactor, complete, debug, test, improve, or prepare code, including features, bugs, architecture, UI/frontend behavior, Android apps, web apps, ASP.NET/C# projects, Python projects, Telegram bots, database work, and homework or student projects.
---

# Codex Task Executor

## Goal

Complete programming tasks safely, accurately, and fully. Prioritize correctness first, preservation of existing behavior second, and clean maintainable code third.

Use this skill to implement features, fix bugs, refactor code, edit files, create project structure, debug build or runtime errors, improve UI behavior, add tests, and prepare projects for launch, review, or submission.

## Core Workflow

Before changing code, understand the project:

1. Inspect the project structure and relevant instructions such as `AGENTS.md`, README files, package files, build files, config files, source folders, tests, routes, screens, components, services, database files, and migrations.
2. Identify the exact files and architecture area where the change belongs.
3. Check existing naming, formatting, framework patterns, dependencies, state management, data access, and UI style.
4. Make a small implementation plan: files to edit, files to create, logic to add, and checks to run.
5. Implement the smallest correct change that satisfies the task.
6. Validate with the most relevant available checks.
7. Report what changed, which files changed, how to verify, and any remaining limits or failed checks.

Ask a question only when missing information can seriously break the task. Otherwise make a reasonable assumption and continue.

## Editing Rules

- Preserve existing behavior unless the user explicitly asks to replace it.
- Avoid unnecessary rewrites, broad refactors, unrelated formatting, and public API changes.
- Do not remove files, code, dependencies, settings, assets, authentication, validation, permissions, or data unless clearly required.
- Follow the existing project style and architecture. If the style is messy, improve only the touched area.
- Keep changes focused and explainable.
- Avoid heavy abstractions, patterns, frameworks, or dependencies unless they clearly improve the task.
- Do not add generated files, cache files, build artifacts, or unrelated cleanup.
- Do not hardcode secrets, credentials, private URLs, or environment-specific values.
- Do not leave TODOs instead of implementation.
- Keep UI, business logic, data access, configuration, and infrastructure separated where the project already uses boundaries.

## Implementation Quality

Write code that is correct, readable, maintainable, consistent, and safe to extend.

Avoid duplicated business logic, global mutable state when avoidable, silent failures, swallowed errors, oversized files, underimplemented placeholders, fake success behavior, and unnecessary dependencies.

For debugging tasks:

1. Read the error carefully.
2. Locate the exact failing file and line.
3. Identify the root cause.
4. Fix the root cause, not only the visible symptom.
5. Check nearby code for similar issues.
6. Rerun the relevant command if possible.

## Validation

After changes, run the most relevant available checks in this order when practical:

1. Unit tests.
2. Type checks.
3. Lint.
4. Build.
5. App-specific smoke test or manual verification.

If checks cannot run because of missing dependencies, environment limits, unavailable services, sandbox restrictions, or unrelated existing failures, say so clearly and report what was still verified. Never claim the project works if verification was not possible.

## UI Tasks

For tasks involving screens, components, layouts, dashboards, forms, modals, widgets, styling, or frontend behavior:

- Apply a polished modern premium UI direction.
- If `universal-premium-ui-style` exists, use it together with this skill.
- Preserve existing functionality and project design system where present.
- Keep layouts responsive and accessible.
- Include relevant loading, empty, disabled, error, success, hover, pressed, and focus states.
- Avoid generic default-looking components.
- Do not prioritize visual polish over working logic.

## Platform Notes

Web projects:
- Use the existing framework correctly.
- Keep components reusable and styling consistent.
- Prefer semantic HTML where possible.
- Preserve routing, hydration behavior, validation, accessibility, and responsive layout.
- Avoid unnecessary client-side complexity.

Android projects:
- Follow the project's existing architecture.
- Use Jetpack Compose only when the project already uses it or the user asks for it.
- Do not migrate XML views to Compose unless requested.
- Preserve lifecycle, navigation, permissions, themes, resources, and background behavior.
- Avoid putting all logic into `Activity` or `Fragment`.

ASP.NET, Razor, MVC, Web API, and C# projects:
- Respect the existing solution structure.
- Use dependency injection consistently.
- Keep models, services, data access, controllers, Razor Pages, and UI separated where appropriate.
- Validate input and avoid exposing internal errors.
- Use async where the project already uses async.
- Do not overbuild enterprise architecture for small homework projects.

Python projects:
- Follow the existing package structure.
- Keep functions simple and errors explicit.
- Avoid unnecessary dependencies.
- Keep configuration in environment variables where appropriate.
- Do not mix configuration, business logic, and execution code if the project separates them.

Telegram bot projects:
- Respect the existing framework and version.
- For aiogram 3, do not use aiogram 2 imports or patterns.
- Keep routers, handlers, keyboards, FSM states, services, and database logic separated when the project does.
- Validate user input, protect admin features, and avoid blocking operations inside handlers.

Database tasks:
- Inspect the existing schema first.
- Preserve existing data unless deletion is explicitly requested.
- Use migrations if the project already uses migrations.
- Avoid destructive schema changes without clear need.
- Keep naming consistent, validate relationships, handle empty results, and avoid SQL injection.

Homework or student projects:
- Complete the stated requirement exactly.
- Keep the solution understandable and easy to explain.
- Avoid unnecessary advanced features.
- Use realistic sample data only when needed.
- Make the project easy to demonstrate.

## Before Finishing

Check:

- Only relevant files were modified.
- Existing behavior was preserved.
- Edge cases and errors were handled where appropriate.
- No unnecessary dependencies were added.
- Checks were run or the reason they could not run is clear.
- Code style matches the project.
- User work was not overwritten.
- No TODOs, stubs, or fake success paths were left behind.

## Final Report

Use the user's requested language and format when provided. Otherwise report briefly:

```text
Done.

Changed:
- ...

Files:
- ...

How to check:
- ...

Notes:
- ...
```
