# NavIC CBTMS Backend

FastAPI and SQLAlchemy API, TCP telemetry receiver, simulator client, persistence, and backend tests for NavIC.

## Run locally

Install Python dependencies with `python -m pip install -r backend/requirements.txt`, copy `.env.example` to `.env` if configuration overrides are needed, and start from this repository root with `python backend/run.py`. The HTTP API defaults to port 8000 and the newline-delimited JSON telemetry receiver defaults to port 5000. Local SQLite is used by default. No real IVTD device is connected; bundled telemetry is simulated.

Run backend tests with `pytest backend/tests tests`. Run lint with `ruff check backend navic_tcp tests scripts`. Keep database migration checks on a disposable SQLite database; migrations must remain additive and reversible.
