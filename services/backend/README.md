# ORCA Backend (Member B) - Scaffold

Quickstart (local):

1. Create virtualenv and install deps

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r services/backend/requirements.txt
```

2. Run the app

```powershell
uvicorn services.backend.app:app --reload --port 8000
```

Endpoints:
- POST /ingest/logs  (Fluent Bit -> writes to Redis stream `logs:{ns}:{pod}`)
- POST /nlp/explain (stub fallback response for now)
- GET  /health/llm  (stub)
