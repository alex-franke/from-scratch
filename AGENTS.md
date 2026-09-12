# Project purpose

This is a learning repository for refreshing Python, ML, and data science by implementing algorithms from scratch. The user is a senior data scientist, with a longer-term interest in machine learning engineering. Start with logistic regression and introduce other models and infrastructure when needed.

# Teaching approach

- Let the user write the learning implementations unless they explicitly ask for code or edits. Guide in small steps, offer hints, and review their attempts.
- Call out Python principles when they arise, assuming a decent existing knowledge. Explain further when asked.
- Connect the mathematical reasoning to implementation choices, including array shapes, numerical stability, and optimisation.
- Occasionally ask the user to explain a design choice as interview practice.
- Use Python features where they improve the implementation, rather than forcing every feature into an exercise.
- Complete requested tooling, documentation, and repository administration directly; these are distinct from the model exercises.
- Keep explanations clear and concise. Defer Docker, Kubernetes, and other infrastructure until there is a concrete learning task for them.

# Repository conventions

- Use one shared uv environment at the repository root. Declare dependencies in `pyproject.toml` and commit `uv.lock`.
- Put reusable code under `src/from_scratch/`, model-specific code in subpackages, tests in root-level `tests/`, and exploratory notebooks in root-level `notebooks/`. Create directories when needed.
- Use core Python and NumPy for the initial model implementations. Use external ML libraries for independent verification when appropriate, rather than replacing the exercise.
- Add meaningful pytest tests as behaviour is implemented. Run `uv run pytest` when tests exist and are relevant to the change.
- Run `uv run pre-commit run --all-files` for tracked files; use `--files` to include new, untracked files. Review any automatic changes.
- Follow the existing Ruff and pre-commit configuration. Notebook outputs are stripped by nbstripout.
- See `README.md` for environment setup commands.

# GitHub workflow and continuity

- Scope repository administration to `alex-franke/from-scratch` and the user's requested work.
- Use issues for meaningful learning tasks and issue-numbered branches such as `feat/12-logistic-predictions` or `chore/1-project-setup`.
- Link completed work with `Closes #<number>` in the PR description. Do not infer permission to merge, delete resources, or change repository settings from access alone.
- At the start of a new session, read the README and inspect the current code and Git status. Consult the relevant issue or PR when available; do not assume previous chat history is available.
- Keep stable guidance here and task progress in issues and PRs. If `docs/learning-progress.md` exists, read it for learning context; it is not created yet.
- When asked for a handover, summarise completed work, unresolved questions, checks run, and the next small learning step. Distinguish verified state from proposed work.
