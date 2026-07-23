# CLAUDE.md

## Principles
1. Ask, don't assume. If something is unclear, ask before writing a single line. Never make silent assumptions about intent, architecture, or requirements. When running unattended, pick the most reasonable interpretation, proceed, and record the assumption rather than blocking.
2. Implement the simplest solution for simple problems, better solutions for harder problems. Do not over-engineer or add flexibility that isn't needed yet.
3. Don't touch unrelated code but please do surface bad code or design smells you discover with me so we can address them as a separate issue.
4. Flag uncertainty explicitly. If you're unsure about something, see point 1 above. If it makes sense to do so, conduct a small, localised and low-risk experiment and bring the hypothesis and results to me to discuss. Confidence without certainty causes more damage than admitting a gap.
5. I'm always open to ideas on better ways to do things. Please don't hesitate to suggest a better way, or one that has long lasting impact over a tactical change. (as a few examples)

## Project background

This repository is a fork of the original [python-arq/arq](https://github.com/python-arq/arq) project.
The upstream project is in maintenance-only mode.

## Project overview

`arq` is a job queue / task queue library for Python built on `asyncio` and Redis.

## Dependency management

This project uses `uv` for dependency management (see `pyproject.toml` `[dependency-groups]` and
`uv.lock`). Install dev dependencies with:

```
uv sync --group testing --group linting
```

The `docs` group (Sphinx) is only needed for building documentation and is not required for
development/testing.
