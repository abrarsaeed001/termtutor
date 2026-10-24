# TermTutor Python prototype

This directory contains the Python experiments and glossary data for TermTutor. The agent is an early command-line prototype, not a production service or HTTP API.

## Requirements

- Python 3.13 or newer
- [uv](https://docs.astral.sh/uv/)
- [Ollama](https://ollama.com/) with the `gemma4-local:latest` model available locally

## Setup

From the repository root, sync the dependencies pinned by `uv.lock`:

```bash
uv sync --project api
```

## Run the agent experiment

From the repository root, run:

```bash
uv run --project api python api/code/agent-01.py
```

The script prompts for a question and sends it to the configured Ollama model. Its weather tool is only a placeholder and always returns a sunny forecast; it does not fetch real weather data.

## Project files

- `app/main.py` — minimal Python entry point that currently prints a greeting.
- `code/agent-01.py` — LangChain agent experiment.
- `data/glossary.json` — starter AI glossary with explanations and quiz examples.

The glossary identifies its source and retrieval date in the data file. Review and verify definitions before using them as authoritative educational material.
