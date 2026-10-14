## Requisiti

- Python **3.10 – 3.12** (consigliato 3.12; il 3.13+ non è supportato dal progetto)
- [Poetry](https://python-poetry.org/) 2.x

## Installazione

Se sul sistema hai una versione di Python più recente (es. 3.14), installa la 3.12 e indica a Poetry di usarla:

```bash
brew install python@3.12
poetry env remove --all          # rimuove eventuali ambienti creati con un'altra versione
poetry env use $(brew --prefix python@3.12)/bin/python3.12
poetry install
```

### Dipendenze principali

fastapi, uvicorn, openai, langchain-openai, langchain-community, langgraph, pydantic, python-dotenv, google-search-results

### Nota

Il vincolo su Python è definito in `pyproject.toml` (`requires-python = ">=3.10,<3.13"`). Se Poetry segnala
`Current Python version ... is not allowed by the project`, l'ambiente virtuale sta usando una versione non supportata:
ripeti i comandi `poetry env remove --all` e `poetry env use` indicati sopra.