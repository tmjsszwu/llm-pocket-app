# llm-pocket-app

Minimal LLM CLI: stdin in, streamed answer out

Built for my own use; public in case it helps someone.

## Examples

```bash
chatsh explain this error < error.log
cat diff.patch | chatsh review this diff
```

## Highlights

- Streams tokens as they arrive
- Works with any OpenAI-compatible endpoint
- Model and system prompt via flags or env
- Reads the prompt from args or stdin

## Installation

```bash
pip install -r requirements.txt
export OPENAI_API_KEY=sk-...
```

## Project structure

```text
├── .github/
│   └── workflows/
│       └── ci.yml
├── docs/
│   ├── configuration.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── tests/
│   └── test_smoke.py
├── .gitignore
├── CONTRIBUTING.md
├── LICENSE
├── SECURITY.md
├── chatsh.py
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```

## Changelog

- `0.1.1` - fix edge case in argument parsing
- `0.1.0` - first working version

## License

MIT. Do whatever you want.
