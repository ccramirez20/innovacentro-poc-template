# innovacentro-poc-template

Python starter for LLM proof-of-concept projects: typed, linted, tested and CI-checked from the first commit.

## What's included
- Python 3.11+, `pyproject.toml` with `anthropic`, `pydantic`, `python-dotenv`
- `ruff` (lint + format), `mypy --strict`, `pytest` + coverage
- `pre-commit` hooks (ruff, mypy)
- GitHub Actions CI: ruff, mypy, pytest on every push and PR
- `.env.example` for API keys (never commit a real `.env`)

## Structure
```
src/        package code (mypy strict)
tests/      pytest tests (smoke test included)
.github/    CI workflow
```

## Use it
```bash
git clone https://github.com/ccramirez20/innovacentro-poc-template.git my-poc
cd my-poc
python -m venv .venv && source .venv/bin/activate
pip install -e ".[dev]"
pre-commit install
cp .env.example .env   # add your key
pytest
```

## Limitations
Only a skeleton: no sample app, no deployment config, one smoke test. Rename the package (`poc-base`) when you fork it.

## License
MIT
