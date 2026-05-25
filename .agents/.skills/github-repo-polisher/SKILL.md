---
name: github-repo-polisher
description: Use this skill whenever preparing a project, repository, homework project, prototype, library, app, bot, website, or codebase for GitHub publication. The skill improves repository structure, README quality, .gitignore, security hygiene, launch instructions, and overall presentation without breaking the project.
---

# GitHub Repo Polisher

## Goal

Prepare a project for clean, safe, and professional publication on GitHub. Make the repository understandable, runnable, and trustworthy while preserving existing behavior.

## Core Priorities

1. Do not break the project.
2. Do not delete important source files.
3. Remove or ignore only unnecessary, generated, local, or sensitive files.
4. Make the repository easy to run.
5. Make the repository easy to understand.
6. Keep the presentation appropriate for the project type.

## Workflow

Before changing files:

1. Inspect the project structure with fast file search tools.
2. Detect the main technology stack and package/build systems.
3. Find the project entry point, launch path, and expected runtime.
4. Identify install, test, lint, type-check, build, and run commands from existing configs.
5. Read existing README, .gitignore, license, package manifests, environment examples, and deployment configs.
6. Look for unnecessary generated files, local IDE files, caches, logs, build output, and dependency folders.
7. Look for secrets, credentials, private URLs, tokens, keys, database dumps, and environment files.
8. Make focused improvements and verify the project still works as far as practical.

Do not rewrite the whole project unless the user explicitly asks.

## Repository Structure

Improve structure only when needed. Prefer documenting the current layout over moving files. Move or rename files only when the existing structure is clearly confusing and the change is low-risk.

A clean repository may include:

```text
project-name/
|- README.md
|- .gitignore
|- LICENSE
|- src/
|- docs/
|- assets/
|- tests/
|- examples/
|- package.json / requirements.txt / .sln / build.gradle
`- ...
```

Do not force this structure onto every project. For small homework or prototype repositories, a clear README and sane ignore rules may be enough.

## README Improvements

Create or improve README.md with the sections that fit the project:

- Project name and short description.
- What the project does and who it is for.
- Key features, kept factual and not inflated.
- Screenshots or demo GIFs if assets already exist or can be generated safely.
- Tech stack.
- Requirements and supported versions when discoverable.
- Installation steps.
- Environment variable setup, using placeholders only.
- Run commands.
- Test, lint, type-check, and build commands.
- Project structure summary for non-trivial projects.
- API usage, CLI usage, or app workflow examples when relevant.
- Known limitations if the project is incomplete.
- License note if a license exists or the user asks to add one.

Keep README instructions truthful. Do not invent features, deployment status, badges, test coverage, benchmarks, or security claims.

## .gitignore

Create or update .gitignore based on the detected stack. Include only relevant patterns.

Common categories:

- Dependency folders: `node_modules/`, `.venv/`, `venv/`, vendor caches when not committed by convention.
- Build output: `dist/`, `build/`, `out/`, `target/`, `.next/`, `.nuxt/`.
- Caches: `.pytest_cache/`, `.mypy_cache/`, `.ruff_cache/`, `__pycache__/`, `.gradle/`.
- Logs and temp files: `*.log`, `tmp/`, `temp/`.
- Local environment files: `.env`, `.env.*`, except safe examples like `.env.example`.
- IDE/OS files: `.idea/`, `.vscode/` only when project does not intentionally share settings, `.DS_Store`, `Thumbs.db`.
- Generated secrets or keys: `*.pem`, `*.key`, `*.p12`, `*.keystore`, with care not to ignore source fixtures unintentionally.

If a sensitive file is already tracked, do not assume ignoring it is enough. Tell the user it may need removal from Git history and credential rotation.

## Security Hygiene

Search for likely secrets before publication. Use targeted patterns and inspect results manually to avoid false positives:

- `.env`, credentials, tokens, API keys, private keys, passwords, database URLs, OAuth secrets, webhook URLs.
- Hardcoded personal paths, private IPs, internal domains, usernames, emails, or machine-specific config.
- Large data dumps, exports, logs, screenshots, or documents that may contain private information.

Never print real secrets back to the user. Refer to the file and variable/key name, mask values, and recommend rotation if exposure is plausible.

## Cleanup Rules

Safe cleanup candidates:

- Generated build artifacts.
- Runtime logs and temporary files.
- Dependency folders that can be restored from lockfiles.
- OS metadata files.
- Local editor caches.
- Empty placeholder folders only when they are clearly unused.

Risky files that require caution or user approval:

- Database files, uploads, media, exports, notebooks, datasets, migrations, lockfiles, certificates, keystores, and config files.
- Any file whose purpose is unclear.

Prefer adding ignore rules over deleting files unless deletion is clearly safe and useful. Do not remove lockfiles for package managers.

## Project-Type Notes

For web apps, document package manager commands, dev server URL, build output, and environment variables.

For Python projects, document Python version, virtual environment setup, dependency install command, module entry point, tests, and formatting/lint tools if present.

For Android projects, document Android Studio/Gradle requirements, build variant, run command, SDK expectations, and whether local signing files are excluded.

For backend/API projects, document environment variables, database setup, migrations, seed data, run command, test command, and basic endpoint usage.

For bots or automation projects, document required tokens as placeholders, startup command, webhook/polling mode, and deployment caveats without exposing credentials.

For libraries, document installation, minimal usage example, public API entry point, tests, and versioning/license status.

For homework or portfolio projects, keep the README clear and modest. Explain purpose, stack, how to run, and what is implemented.

## Verification

After changes, run the most relevant available checks:

1. Unit tests.
2. Type checks.
3. Lint or formatting checks.
4. Build.
5. Minimal manual launch or smoke test.

If checks cannot be run, state why and provide concrete manual verification steps.

## Final Response

Summarize:

- What was changed.
- Which files were modified.
- Which checks were run and their results.
- Any remaining risks, especially suspected secrets, unverified commands, missing license decisions, or files that may need Git history cleanup.
