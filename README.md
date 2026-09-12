# Implementations From Scratch

A collection of algorithm implementations from the ground up, built to deepen understanding of core concepts in data science and machine learning.

## Motivation

While many frameworks offer ready-to-use implementations, building these algorithms manually is intended as a valuable learning exercise.

## Development setup

Install [uv](https://docs.astral.sh/uv/getting-started/installation/), then run these commands from the repository root:

```bash
uv sync
uv run pre-commit install
```

`uv sync` creates the shared `.venv` environment and installs the project dependencies, including development tools. The second command enables the Git hooks for this local clone.

To run all hooks on tracked files manually:

```bash
uv run pre-commit run --all-files
```

If a hook modifies files, review and stage the changes before committing again.
