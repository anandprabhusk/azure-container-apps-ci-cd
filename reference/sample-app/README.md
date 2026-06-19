# Sample App Reference

This folder contains a minimal reference Python application used by the Azure Container Apps CI/CD guide.

## Files

- `app.py` - Minimal Flask application
- `requirements.txt` - Python package dependencies
- `Dockerfile` - Container image build definition

## Important behavior

- The application listens on port `8080`
- The container exposes port `8080`
- The startup command binds Gunicorn to `0.0.0.0:8080`
- The root path `/` returns a JSON response

## Run locally

Install dependencies:

```bash
pip install -r requirements.txt
```

Run locally with Flask for quick testing:

```bash
python app.py
```

Or run with Gunicorn:

```bash
gunicorn --bind 0.0.0.0:8080 app:app
```
