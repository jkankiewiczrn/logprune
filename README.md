# logprune

Opinionated log housekeeping tool with dry-run support

## Install

```bash
pip install -r requirements.txt
python -m logwash --help
```

## Usage

```bash
# show what would be cleaned, change nothing
logwash ./logs --older-than 30 --dry-run

# archive logs older than 30 days
logwash ./logs --older-than 30 --archive ./backup
```

## Features

- Filter by age (--older-than) or size (--larger-than)
- Scan directories for log files by glob pattern
- Exit codes friendly for cron and CI
- Dry-run mode shows what would happen, touches nothing
- Archive matched logs into a timestamped .tar.gz

## Project structure

```text
├── .github/
│   ├── dependabot.yml
│   └── pull_request_template.md
├── docs/
│   ├── faq.md
│   └── usage.md
├── logwash/
│   ├── __init__.py
│   ├── __main__.py
│   ├── cli.py
│   ├── errors.py
│   └── utils.py
├── tests/
│   └── test_cli.py
├── .editorconfig
├── .gitignore
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── pyproject.toml
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```

## 说明

个人练习项目, 谨慎用于生产环境。

## License

MIT. Do whatever you want.
