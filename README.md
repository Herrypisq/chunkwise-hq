# chunkwise-hq

Minimal RAG over a folder of markdown notes, no vector DB

## Examples

```bash
python rag.py ./notes "how do I rotate logs?"
```

## Getting started

```bash
pip install -r requirements.txt
```

## What it does

- Prints sources with scores for transparency
- Chunk markdown with overlap, keep source paths
- TF-IDF retrieval: zero external services needed
- Swap in any LLM for the answer step

## Project structure

```text
├── .github/
│   ├── workflows/
│   │   └── ci.yml
│   └── dependabot.yml
├── data/
│   └── sample.md
├── docs/
│   ├── configuration.md
│   ├── faq.md
│   └── usage.md
├── tests/
│   └── test_smoke.py
├── .gitignore
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
├── rag.py
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```

## Notes

- mostly stable, edge cases remain

## License

MIT licensed, see LICENSE.
