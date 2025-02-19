# Project Creation Prompts

## Initial Request
```
I need a python fastapi application with a single hello world endpoint. Please use uv as a package manager. I'll need unit tests with pytest as well.

It should be built using docker.

Can you also add the github workflows for building and linting with ruff?

Can you also add the deployment to digital ocean via a container regisrty at digital ocean

Can you add a README.md with all the usual project information

please use python 3.13, and deploy to Digital Ocean's app platform instead of DOKS

can you use pyproject.toml instead of uv.json?

make sure that the pyproject.toml has a [project] section

make sure that you add the requires-python line in the pyproject.toml
```

## Additional Request
```
can you append all the promts so far into a file PROMPT.md if the file doesnt exist, make a new one
```

This document captures the evolution of requirements for this FastAPI Hello World project, showing how the specifications were refined to include:

1. FastAPI with Hello World endpoint
2. uv package manager
3. pytest for testing
4. Docker containerization
5. GitHub Actions for CI/CD
6. Digital Ocean App Platform deployment
7. Python 3.13 requirement
8. pyproject.toml configuration
