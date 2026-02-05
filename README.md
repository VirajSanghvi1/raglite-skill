# raglite-skill

Minimal OpenClaw skill wrapper for **RAGLite**.

This repo intentionally contains only the smallest set of files needed for an OpenClaw/ClawHub skill bundle.

Security posture:
- No credential handling
- No background daemons
- Install script only installs `raglite` from PyPI (or TestPyPI) and executes the `raglite` CLI

See `skills/raglite/SKILL.md` for the user-facing pitch and usage.
