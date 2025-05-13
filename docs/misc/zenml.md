# ZenML
Source: https://github.com/zenml-io/zenml
Version: 876bc70

```
├── CLA.md
├── CODE-OF-CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── README.md
├── RELEASE_NOTES.md
├── ROADMAP.md
├── SECURITY.md
├── alembic.ini
├── docker
│   ├── base.Dockerfile
│   ├── zenml-dev.Dockerfile
│   ├── zenml-quickstart-dev.Dockerfile
│   ├── zenml-quickstart.Dockerfile
│   ├── zenml-server-dev.Dockerfile
│   └── zenml-server-hf-spaces.Dockerfile
├── docs
│   ├── README.md
│   ├── _static
│   ├── _templates
│   ├── book
│   ├── link_checker.py
│   ├── mkdocs
│   ├── mkdocs.yml
│   ├── mkdocstrings_helper.py
│   ├── mocked_libs.json
│   └── sys_modules_mock.py
├── examples
│   ├── README.md
│   ├── e2e
│   ├── e2e_nlp
│   ├── llm_finetuning
│   ├── mlops_starter
│   └── quickstart
├── helm
│   ├── Chart.yaml
│   ├── README.md
│   ├── templates
│   └── values.yaml
├── infra
│   ├── README.md
│   ├── aws
│   ├── gcp
│   └── scripts
├── pyproject.toml
├── release-cloudbuild-nightly.yaml
├── release-cloudbuild-preparation.yaml
├── release-cloudbuild.yaml
├── scripts
│   ├── __init__.py
│   ├── add-docs-warning.py
│   ├── add-docs-warning.sh
│   ├── add-migration-test-version.sh
│   ├── check-alembic-branches.sh
│   ├── check-security.sh
│   ├── check-spelling.sh
│   ├── check_broken_links.py
│   ├── check_broken_links.sh
│   ├── check_relative_links.py
│   ├── clean.sh
│   ├── compare_profiles.py
│   ├── docstring.sh
│   ├── find_orphaned_assets.py
│   ├── find_unreferenced_docs.py
│   ├── format.sh
│   ├── generate-docs.sh
│   ├── gitbook_redirect_check.py
│   ├── install-dashboard.sh
│   ├── install-zenml-dev.sh
│   ├── lint.sh
│   ├── profile-cli.sh
│   ├── redeploy-release-prep-tenant.py
│   ├── run-ci-checks.sh
│   ├── serve_api_docs.sh
│   ├── setup_gitbook_dirs.py
│   ├── summarize_docs.py
│   ├── sync-gitbook-release-spaces.py
│   ├── test-coverage-html.sh
│   ├── test-coverage-xml.sh
│   ├── test-migrations.sh
│   ├── test_integration_pairs.py
│   ├── validate-new-version.sh
│   └── verify_flavor_url_valid.py
├── src
│   └── zenml
├── tests
│   ├── README.md
│   ├── __init__.py
│   ├── conftest.py
│   ├── harness
│   ├── integration
│   ├── test-framework-architecture.jpg
│   ├── unit
│   └── venv_clone_utils.py
├── trivy-secret.yaml
├── zen-dev
└── zen-test
```

## Programming Language & Environment
- **Python** (>=3.9, <3.13, specified in `pyproject.toml`)
- Uses **Poetry** for dependency management

## Core Dependencies
- **alembic**: For database migrations
- **bcrypt, passlib**: For password hashing
- **click**: For CLI applications
- **cloudpickle**: For serialization
- **docker**: For containerization
- **gitpython**: For Git operations
- **pydantic, pydantic-settings**: For data validation and settings management
- **sqlalchemy, sqlalchemy_utils, sqlmodel**: For database ORM
- **rich**: For terminal formatting and Jupyter integration

## Optional Dependencies
- **ZenServer**: FastAPI, uvicorn, pyjwt, etc.
- **Project Templates**: copier, jinja2-time, etc.
- **Cloud Secrets**: AWS, GCP, Azure, HashiCorp Vault
- **Cloud Connectors**: AWS, GCP, Azure, Kubernetes
- **Artifact Stores**: S3, GCS, Azure
- **Orchestrators**: Sagemaker, Vertex, AzureML

## Development & Quality Tools
- **bandit**: For security linting
- **coverage**: For code coverage measurement
- **mypy**: For static type checking
- **ruff**: For linting and formatting
- **pytest**: For testing (with plugins like pytest-mock, pytest-clarity, etc.)
- **mkdocs**: For documentation (with plugins like mkdocs-material, mkdocstrings, etc.)

## Build & Task Automation
- **Docker**: Containerization (Dockerfile and .dockerignore)
- **GitHub Actions**: For CI/CD (implied by `.github/` directory)

## Project Structure
- **src/**: Source code
- **tests/**: Test files
- **scripts/**: Utility scripts
- **docs/**: Documentation
- **examples/**: Example projects
- **infra/**: Infrastructure configurations
- **helm/**: Helm charts

## Other Notable Configurations
- **GitHub**: The project is designed to work with GitHub (implied by GitHub Actions)
- **CLI Tool**: The project is a CLI tool (`zenml`) for MLOps and production-ready ML code

