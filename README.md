# TermTutor

TermTutor is an early-stage project for helping people learn artificial intelligence concepts through clear explanations and practical examples. The repository currently contains a Next.js web starter, an AI glossary, and a small LangChain/Ollama command-line experiment.

> **Project status:** The web app is still the default Next.js starter screen, and the Python agent is a prototype. The web app is not connected to the Python experiment yet.

## Project structure

```text
termtutor/
├── api/
│   ├── app/          # Python application entry point
│   ├── code/         # LangChain/Ollama agent experiment
│   └── data/         # AI glossary data
├── notebooks/        # Exploration notebooks
└── web/              # Next.js web app
```

## Requirements

- [Node.js](https://nodejs.org/) and npm
- [Python 3.13 or newer](https://www.python.org/)
- [uv](https://docs.astral.sh/uv/) for Python dependency management
- [Ollama](https://ollama.com/) and a locally available model matching the name configured in `api/code/agent-01.py` to run the agent experiment

## Run the web app

```bash
cd web
npm ci
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser. For an optimized production build, run `npm run build` followed by `npm start` from the `web/` directory.

## Run the Python examples

Install the locked Python dependencies from the repository root:

```bash
uv sync --project api
```

Run the current command-line agent experiment:

```bash
uv run --project api python api/code/agent-01.py
```

The experiment uses Ollama model `gemma4-local:latest` and includes a placeholder weather tool that always returns a sunny forecast. Make the matching model available in Ollama before running it. The separate `api/app/main.py` file currently prints a greeting; it does not start an HTTP API.

## Development

- Run the web linter with `npm run lint` from `web/`.
- Keep API credentials and local environment files out of Git. Use `api/.env.example` as a starting point for environment variables if the project adds them.
- Glossary entries live in `api/data/glossary.json`.
- Follow the setup and conventions documented in each subproject's README before making changes.

## License

No license has been specified yet. Until one is added, all rights are reserved by the respective copyright holders.
