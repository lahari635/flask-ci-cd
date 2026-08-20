# Flask CI/CD Pipeline

A containerized Flask application with a GitHub Actions CI/CD workflow.

## Project Structure

- `app.py` - Flask application
- `requirements.txt` - Python dependencies
- `Dockerfile` - Docker image configuration
- `.github/workflows/ci-cd.yml` - GitHub Actions workflow

## Pipeline

GitHub Push -> Test -> Build Docker Image -> Push to Docker Hub

## Run Locally

```bash
pip install -r requirements.txt
python app.py
```

Open http://localhost:5000

## Docker

Build:

```bash
docker build -t flask-cicd .
```

Run:

```bash
docker run -p 5000:5000 flask-cicd
```

## GitHub Secrets

Add these repository secrets before running the workflow:

- `DOCKER_USERNAME`
- `DOCKER_PASSWORD`
