# Multilingual Civic Services and Government Scheme Navigator

Understanding application checklists without inventing eligibility rulings or active deadlines.

[Setup](#local-installation--setup-guide) · [Architecture](#architecture--system-design-diagram) · [Detailed guide](PROJECT_GUIDE.md) · [Repository standard](docs/REPOSITORY_STANDARD.md)

## Visuals

![Original project cover](<assets/cover.svg>)

Existing project visual; diagrams and illustrative graphics are not evidence of a deployed application.

## Live Link / Demo

Run the local demo using the setup guide below. No public deployment URL has been verified for this documentation update.

## Key Features

RAG • scheme navigation • source citations. TF-IDF retrieval over explicitly fictional scheme notes, with a verified government portal link; multilingual embeddings are future work.

## Tech Stack

![Python](https://img.shields.io/badge/Python-334155?style=flat-square) ![FastAPI](https://img.shields.io/badge/FastAPI-334155?style=flat-square) ![scikit-learn](https://img.shields.io/badge/scikit--learn-334155?style=flat-square) ![NumPy](https://img.shields.io/badge/NumPy-334155?style=flat-square) ![Docker](https://img.shields.io/badge/Docker-334155?style=flat-square)

Dependency versions and optional packages are defined in the repository manifests.

## Architecture / System Design Diagram

[Architecture documentation / diagram](<assets/architecture.svg>)

## Local Installation & Setup Guide

```bash
git clone https://github.com/harshakavali81-collab/Multilingual-Civic-Services-Navigator.git
cd Multilingual-Civic-Services-Navigator
```

From the project branch root:

```bash
python -m venv .venv
# Windows PowerShell: .venv\Scripts\Activate.ps1
# macOS/Linux: source .venv/bin/activate
python -m pip install -r requirements.txt
python cli.py
uvicorn app.main:app --reload
pytest -q
```

**API endpoint:** `POST /api/v1/analyze`

**Example payload:** [sample_request.json](sample_request.json). The FastAPI interactive schema is at `http://127.0.0.1:8000/docs`.

## Challenges & Solutions

The prototype must separate demonstration outputs from authoritative information. Its documented design uses synthetic examples, explicit source/provenance boundaries and project-specific validation; real operational adapters and field validation remain future work. See [the model card](docs/MODEL_CARD.md) for limits and evaluation assumptions.

## Future Improvements

- Capture a reproducible end-to-end demo with runtime versions and sample inputs.
- Expand regression checks for invalid inputs and documented edge cases.
- Record measured results, data provenance and deployment limitations alongside each release.

## Scope and supporting evidence

> **Status:** Demonstration-grade source code using synthetic examples; no real operational deployment, authorized live feed, or independently verified field impact.

**Public need / intended users:** Understanding application checklists without inventing eligibility rulings or active deadlines. **Audience:** Residents who need accessible public-service information.

**Technical evidence:** RAG • scheme navigation • source citations. TF-IDF retrieval over explicitly fictional scheme notes, with a verified government portal link; multilingual embeddings are future work.

## Repository Structure

| Location | Purpose |
| --- | --- |
| `app/` | Application package |
| `frontend/` | Frontend interface |
| `tests/` | Tests |
| `docs/` | Documentation |
| `assets/` | Visual assets |
| `.github/` | Issue forms, PR template and automated checks |

[Complete file inventory and workflow](docs/REPOSITORY_STANDARD.md). Runtime entry points retain their existing paths.

## Workflow & Tracking

Use the [bug and feature forms](https://github.com/harshakavali81-collab/Multilingual-Civic-Services-Navigator/issues/new/choose) to define work with acceptance criteria. Keep tasks in Todo → In progress → Review → Done, and link a pull request with `Closes #<number>`. See [the maintenance workflow](docs/REPOSITORY_STANDARD.md#workflow).

## License

Original project software is available under the [MIT License](LICENSE). See [licensing scope](docs/LICENSING.md) for third-party and data exclusions.

