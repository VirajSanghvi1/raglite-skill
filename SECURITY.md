# Security review notes

This repository intentionally contains a minimal skill wrapper.

## What it does
- Creates a local venv under `skills/raglite/.venv`
- Installs the `raglite` Python package from PyPI (or TestPyPI if `RAGLITE_PIP_INDEX_URL` is set)
- Executes `raglite` CLI

## What it does NOT do
- No credential scraping
- No hidden network tunnels
- No background services
- No filesystem deletes

## Review checklist
- `scripts/install.sh`: only calls `python -m pip install ... raglite`
- `scripts/raglite.sh`: only runs `raglite` and injects default `--engine openclaw`
- `scripts/openclaw.plugin.json`: only points to the wrapper script
