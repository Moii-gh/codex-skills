---
name: student-homework-builder
description: Use this skill whenever the user asks Codex to complete, improve, structure, or prepare a school/college programming assignment, lab work, homework project, database task, web assignment, Android task, ASP.NET task, Python task, C# task, SQL task, or educational project. The skill ensures the result follows the teacher's requirements, stays understandable for a student, avoids unnecessary overengineering, and is easy to explain during defense.
---

# Student Homework Builder

## Goal

Complete educational programming tasks accurately, clearly, and in a way that can be explained by a student. Satisfy the assignment requirements without turning the work into an overcomplicated enterprise project.

## Main Priorities

1. Follow the assignment exactly.
2. Do not skip any required item.
3. Keep the solution understandable.
4. Avoid unnecessary complexity.
5. Use clean and correct code.
6. Make the project easy to run and demonstrate.
7. Make the result look like competent student work.

## Important Rule

Do not overengineer.

Avoid advanced architecture, complex patterns, unnecessary libraries, CI/CD, cloud deployment, authentication, Docker, or large abstractions unless the assignment specifically asks for them. The solution should be simple enough for a student to explain during defense.

## Workflow

Before implementing:

1. Read the full assignment carefully, including attached files.
2. Extract all explicit requirements.
3. Identify the required technology, language, framework, database, and project type.
4. Identify required tables, classes, pages, forms, fields, screens, functions, buttons, queries, and output formats.
5. Check whether the assignment has multiple parts or hidden deliverables.
6. Determine what must be created, changed, demonstrated, or explained.
7. Make a simple implementation plan.
8. Implement only what is required plus minimal helpful structure.

If the assignment is ambiguous, make a reasonable student-level assumption and state it. Ask a question only when a missing detail can seriously change the solution.

## Requirement Tracking

Create an internal checklist from the assignment. For every requirement, make sure it is:

- implemented;
- documented; or
- clearly impossible due to environment limitations.

Do not ignore small details such as required field names, page names, class separation, database queries, buttons, forms, sample data, output format, screenshots, or demonstration steps.

## Code Style

Code should be correct, readable, simple, consistent, easy to explain, and not artificially complicated.

Prefer:

- Clear variable names.
- Simple functions.
- Direct logic.
- Minimal abstraction.
- Standard library tools when enough.
- Existing project conventions.

Avoid:

- Huge unreadable files.
- Unnecessary design patterns.
- Excessive comments.
- Clever code that is hard to defend.
- Advanced features not covered by the assignment.
- Fake complexity to look professional.
- Hardcoded logic except where appropriate for sample data or a small exercise.

## Student-Friendly Implementation

For student projects:

- Keep structure clean but not excessive.
- Use realistic sample data.
- Keep naming understandable.
- Separate logic only where it helps.
- Avoid hiding important logic behind too many abstractions.
- Make sure the student can explain how the project works.
- Do not introduce tools the teacher did not ask for unless necessary.

The result should look like a strong student completed it carefully.

## UI Tasks

If the assignment includes UI:

- Make the interface clean and readable.
- Keep controls and navigation obvious.
- Do not overload the design.
- Make layouts usable on the expected screen sizes.
- Include required buttons, forms, pages, and navigation.
- Preserve educational simplicity.

If the `universal-premium-ui-style` skill is available and relevant, use it carefully. Do not make the UI so visually complex that it distracts from the assignment.

## Programming Tasks

For programming exercises:

- Solve the exact task.
- Use the requested language, platform, and input/output style.
- Handle basic invalid input when appropriate.
- Keep code understandable.
- Avoid unnecessary frameworks.

If the user asks for beginner-style code, use simpler syntax, avoid advanced abstractions, keep logic direct, and make the result look natural for a student.

## ASP.NET Core / Razor Pages / MVC

For ASP.NET Core assignments:

- Follow the requested project type: Razor Pages, MVC, Web API, or another specified style.
- Keep pages/controllers simple.
- Use Models for entities.
- Use Services or repositories only if useful, required, or already present.
- Use Dependency Injection when required or when the project already uses it.
- Create realistic sample data when needed.
- Do not build a full enterprise architecture unless required.

For Razor Pages:

- Keep PageModel focused.
- Display exactly the required data.
- Validate basic form input.
- Keep navigation simple.

## C# / WinForms / WPF

For C# desktop assignments:

- Keep forms clear.
- Name controls reasonably.
- Separate database access if the task requires it or the form becomes messy.
- Keep event handlers understandable.
- Use simple classes where useful.
- Do not introduce unnecessary architecture.

## Python

For Python homework:

- Keep scripts simple and readable.
- Use functions when they clarify the task.
- Avoid unnecessary packages.
- Handle input/output clearly.
- Keep console messages understandable.
- Avoid advanced Python features unless appropriate for the course level.

## SQL / Database Tasks

For database assignments:

- Design tables according to the task.
- Use required fields.
- Create primary keys where appropriate.
- Add relationships when needed.
- Include sample data if useful.
- Write required queries clearly.
- Avoid reserved words as table names.
- Choose reasonable data types.
- Do not delete important data unless the task asks for delete queries.

For Microsoft Access tasks:

- Keep tables import-friendly.
- Use clear field names.
- Prepare Excel import files if `.accdb` cannot be created.
- Include separate sheets for separate tables when exporting to `.xlsx`.
- Preserve the structure expected by Access.

## Android Tasks

For Android assignments:

- Follow the existing project style.
- Use Kotlin if the project uses Kotlin.
- Use Jetpack Compose only if the project already uses it or the task asks for it.
- Do not migrate XML to Compose unless requested.
- Keep screens simple and understandable.
- Keep state handling clear.
- Avoid putting everything into MainActivity when the task grows.

## Web Tasks

For HTML/CSS/JS homework:

- Keep file structure simple.
- Make layout responsive if relevant.
- Use semantic HTML.
- Keep CSS readable.
- Avoid unnecessary frameworks.
- Implement required interactions clearly.
- Do not add a backend unless the task asks for it.

## Reports and Explanation

If the user needs to defend or explain the work, prepare a short explanation:

- What the project does.
- Which files are important.
- How the data is stored.
- How the main logic works.
- How to run the project.
- Which requirements were completed.

Keep explanation simple and teacher-friendly.

## Verification

After implementation, check:

- The project builds if possible.
- The app runs if possible.
- Required pages, screens, forms, classes, fields, tables, and queries exist.
- Required sample data is present.
- Required operations work.
- No unrelated files were changed.
- Instructions are clear.

Do not claim successful testing if it was not actually performed. If verification cannot be run, state why clearly.

## Final Response Format

Use this format unless the user asks for another one:

```text
Done.

Completed:
- ...

Files:
- ...

How to run/check:
- ...

Notes:
- ...
```
