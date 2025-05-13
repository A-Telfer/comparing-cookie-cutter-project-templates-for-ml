# Cookie Cutter MLOPs fmind
Source: https://github.com/fmind/cookiecutter-mlops-package    
Version: b930d91

```
{{ repo name }}
├── CHANGELOG.md
├── Dockerfile
├── LICENSE.txt
├── README.md
├── confs
│   ├── inference.yaml
│   ├── training.yaml
│   └── tuning.yaml
├── data
├── docker-compose.yml
├── docs
├── justfile
├── mlops-project.code-workspace
├── mlruns
├── notebooks
├── outputs
├── pyproject.toml
├── src
│   └── {{ project_name }}
│       ├── __init__.py
│       ├── __main__.py
│       └── scripts.py
├── tasks
│   ├── check.just
│   ├── clean.just
│   ├── commit.just
│   ├── doc.just
│   ├── docker.just
│   ├── format.just
│   ├── install.just
│   ├── mlflow.just
│   ├── package.just
│   └── project.just
└── tests
    ├── conftest.py
    └── test_scripts.py
```


## Programming Language & Environment
- **Python 3.13** (specified in multiple config files)
- Uses `pyproject.toml` for project configuration and dependency management

## Core Dependencies
- **mlflow**: For experiment tracking and ML lifecycle management
- **hatchling**: For Python packaging and build backend

## Development & Quality Tools
- **pytest** (+ plugins: pytest-cov, pytest-mock, pytest-xdist): For testing
- **mypy**: Static type checking
- **ruff**: Linting and code formatting
- **bandit**: Security linter for Python
- **coverage**: Code coverage measurement
- **pre-commit**: Framework for managing and maintaining multi-language pre-commit hooks
- **commitizen**: For conventional commit messages and versioning

## Documentation & Notebooks
- **pdoc**: For generating project documentation
- **ipykernel, nbformat**: For Jupyter notebook support

## Build & Task Automation
- **just**: Task runner (via `justfile`)
- **Docker**: Containerization (Dockerfile and docker-compose)
  - Uses a custom Python 3.13 image from `ghcr.io/astral-sh/uv`
  - Docker Compose runs an `mlflow` server container

## Other Notable Configurations
- **.pre-commit-config.yaml**: Pre-commit hooks for code quality and security
- **GitHub Actions** (implied by `.github/` directory, though not inspected in detail)
- **MLflow server**: Exposed via Docker Compose on port 5000

