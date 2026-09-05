# Repo Guardian Template

**Repository Governance & Quality Standards für fr4iser90 Projekte.**

Dieses Repo ist **kein normales Projekt** — es definiert die Standards und Konfigurationen, die alle Repositories von fr4iser90 verwenden sollten. Es kann als GitHub-Template genutzt werden oder per `repo-auditor` in bestehende Repos migriert werden.

## Struktur

```
repo-guardian-template/
├── .github/           # CI-Pipelines, Templates, Dependabot
├── config/            # Linter, Type-Checker Konfigurationen
│   ├── python/        # Python-spezifisch (ruff, mypy)
│   └── javascript/    # JS/TS-spezifisch (eslint, prettier)
├── docs/              # Standards-Dokumentation
│   ├── NAMING_CONVENTIONS.md
│   ├── REPOSITORY_STANDARDS.md
│   └── PULL_REQUEST_TEMPLATE.md
├── templates/         # Projekt-Boilerplate Templates
│   ├── python/        # Python-Projekt Boilerplate
│   ├── javascript/    # JS/TS-Projekt Boilerplate
│   └── general/       # Allgemeine Dateien (LICENSE, etc.)
├── scripts/           # Hilfs-Skripte für den Auditor
├── .editorconfig      # Editor-unabhängige Formatierung
├── .pre-commit-config.yaml  # Pre-commit Hook Definitionen
├── SECURITY.md        # Security-Policy Vorlage
└── CONTRIBUTING.md    # Contributing-Guide Vorlage
```

## Nutzung

### Als Template (Neues Projekt)
1. Klicke auf **"Use this template"** auf GitHub
2. Gib deinem neuen Repo einen Namen
3. Kopiere die benötigten Dateien aus `templates/python/` oder `templates/javascript/`
4. Folge der Checkliste in `docs/REPOSITORY_STANDARDS.md`

### Migration bestehender Repos (repo-auditor)
Der `repo-auditor` scannt bestehende Repos und erstellt Migration-PRs für:
- Fehlende CI-Pipelines
- Veraltete Dependencies
- Fehlende Dokumentationsdateien
- Nicht konforme Namenskonventionen

## Standards

| Bereich | Werkzeug | Minimum-Qualität |
|---------|----------|-------------------|
| Linting (Python) | ruff | 0 errors |
| Linting (JS/TS) | eslint + prettier | 0 errors |
| Type Checking | mypy / tsc | Strict mode |
| Test-Coverage | pytest-cov / jest | ≥ 70% |
| Security Scan | gitleaks + semgrep | 0 High/Critical |
| Commit Messages | Conventional Commits | enforced |

## Repository Status

[![CI](https://github.com/fr4iser90/repo-guardian-template/actions/workflows/ci.yml/badge.svg)](https://github.com/fr4iser90/repo-guardian-template/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python 3.11+](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/downloads/)

## Lizenz

MIT — siehe [LICENSE](LICENSE)
