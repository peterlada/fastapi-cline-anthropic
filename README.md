# FastAPI Hello World

A simple FastAPI application that serves a Hello World endpoint. This project is set up with modern Python tooling including uv package manager, pytest for testing, and ruff for linting.

See all the [prompts](./PROMPT.md)

## Requirements

- Python 3.13+
- uv package manager
- Docker (optional, for containerization)

## Local Development

1. Install uv if you haven't already:

```bash
pip install uv
```

2. Install dependencies and activate it:

```bash
uv pip install .[dev]
. .venv/bin/activate
```

3. Run the development server:

```bash
uvicorn app.main:app --reload
```

The API will be available at <http://127.0.0.1:8000>

## Testing

Run tests with pytest:

```bash
pytest
```

## Linting

This project uses ruff for linting and formatting. Run:

```bash
ruff check .
ruff format .
```

## Docker

Build the container:

```bash
docker build -t fastapi-hello-world .
```

Run the container:

```bash
docker run -p 8000:8000 fastapi-hello-world
```

## Deployment

This project is configured to deploy to Digital Ocean App Platform. The deployment is automated via GitHub Actions.

### Prerequisites for Deployment

1. A Digital Ocean account
2. A repository secret named `DIGITALOCEAN_ACCESS_TOKEN` with your Digital Ocean API token
3. Update the `.do/app.yaml` file with your GitHub repository details

### Deployment Process

1. Push to the main branch
2. GitHub Actions will automatically:
   - Run tests and linting
   - Deploy to Digital Ocean App Platform if all checks pass

## API Endpoints

### GET /

Returns a Hello World message

Response:

```json
{
    "message": "Hello, World!"
}
```

## Project Structure

```
.
├── .github/workflows/    # GitHub Actions workflows
│   ├── ci.yml           # CI pipeline
│   └── deploy.yml       # Deployment pipeline
├── .do/
│   └── app.yaml         # Digital Ocean App Platform config
├── src/
│   └── app/
│       └── main.py      # FastAPI application
├── tests/
│   └── test_main.py     # Unit tests
├── Dockerfile           # Container definition
├── pyproject.toml       # Project configuration
└── README.md           # This file
```

## License

MIT
