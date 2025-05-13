# Cookie Cutter Project Scaffolds Comparison

## Existing Cookie Cutter Templates

### Cookie Cutter Data Science (CCDS)
Source: https://cookiecutter-data-science.drivendata.org   
Version: 86152dd   
```
├── LICENSE
├── Makefile
├── README.md
├── data
│   ├── external
│   ├── interim
│   ├── processed
│   └── raw
│
├── docs
├── models
├── notebooks
├── pyproject.toml
├── references
├── reports
│   └── figures
│
├── requirements.txt
├── setup.cfg
└── {{ cookiecutter.module_name }}
    ├── __init__.py
    ├── config.py
    ├── dataset.py
    ├── features.py
    ├── modeling                
    │   ├── __init__.py 
    │   ├── predict.py
    │   └── train.py
    │
    └── plots.py
```

#### Programming Language & Environment
- **Python 3.10** (specified in `pyproject.toml` and `Makefile`)
- Uses `pyproject.toml` for project configuration and dependency management

#### Core Dependencies
- **loguru**: For logging
- **mkdocs**: For documentation
- **pip**: For package management
- **pytest**: For testing
- **python-dotenv**: For environment variable management
- **ruff**: For linting and code formatting
- **tqdm**: For progress bars
- **typer**: For CLI applications

#### Build & Task Automation
- **Makefile**: For automating common tasks like:
  - Installing dependencies (`make requirements`)
  - Cleaning compiled Python files (`make clean`)
  - Linting and formatting code (`make lint`, `make format`)
  - Running tests (`make test`)
  - Creating a Python virtual environment (`make create_environment`)
  - Generating datasets (`make data`)

#### Other Notable Configurations
- **ruff**: Configured for linting and formatting with specific rules (e.g., import sorting)
- **GitHub Actions** (implied by `.github/` directory, though not inspected in detail)


### Cookie Cutter MLOPs fmind
Source: https://github.com/fmind/cookiecutter-mlops-package
Version: b930d91
Local: [ccds_fmind_example](./projects/ccds_fmind_example/)
```
/{{ repo name}}
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


#### Programming Language & Environment
- **Python 3.13** (specified in multiple config files)
- Uses `pyproject.toml` for project configuration and dependency management

#### Core Dependencies
- **mlflow**: For experiment tracking and ML lifecycle management
- **hatchling**: For Python packaging and build backend

#### Development & Quality Tools
- **pytest** (+ plugins: pytest-cov, pytest-mock, pytest-xdist): For testing
- **mypy**: Static type checking
- **ruff**: Linting and code formatting
- **bandit**: Security linter for Python
- **coverage**: Code coverage measurement
- **pre-commit**: Framework for managing and maintaining multi-language pre-commit hooks
- **commitizen**: For conventional commit messages and versioning

#### Documentation & Notebooks
- **pdoc**: For generating project documentation
- **ipykernel, nbformat**: For Jupyter notebook support

#### Build & Task Automation
- **just**: Task runner (via `justfile`)
- **Docker**: Containerization (Dockerfile and docker-compose)
  - Uses a custom Python 3.13 image from `ghcr.io/astral-sh/uv`
  - Docker Compose runs an `mlflow` server container

## Other Notable Configurations
- **.pre-commit-config.yaml**: Pre-commit hooks for code quality and security
- **GitHub Actions** (implied by `.github/` directory, though not inspected in detail)
- **MLflow server**: Exposed via Docker Compose on port 5000


### Cookie Cutter MLOPs Chim-50
Source: https://github.com/Chim-SO/cookiecutter-mlops
Version: 526751d
```
{{ cookiecutter.repo_name }}/
├── LICENSE
├── README.md
├── Makefile
├── configs
│   └── model1.yaml
├── data
│   ├── external
│   ├── interim
│   ├── processed
│   └── raw
├── docs
├── models
├── notebooks
├── references
├── reports
│   └── figures
├── requirements.txt
└── src
    ├── __init__.py
    ├── data
    │   ├── build_features.py
    │   ├── cleaning.py
    │   ├── ingestion.py
    │   ├── labeling.py
    │   ├── splitting.py
    │   └── validation.py
    ├── models
    │   └── model1
    │       ├── dataloader.py
    │       ├── hyperparameters_tuning.py
    │       ├── model.py
    │       ├── predict.py
    │       ├── preprocessing.py
    │       └── train.py
    └── visualization
        ├── evaluation.py
        └── exploration.py
```

#### Programming Language & Environment
- **Python 3** (specified in `Makefile`)
- Uses `requirements.txt` for dependency management

#### Core Dependencies
- **pip, setuptools, wheel**: For package management
- **flake8**: For linting

#### Build & Task Automation
- **Makefile**: For automating common tasks like:
  - Installing dependencies (`make requirements`)
  - Generating datasets (`make data`)
  - Cleaning compiled Python files (`make clean`)
  - Linting code (`make lint`)
  - Syncing data to/from S3 (`make sync_data_to_s3`, `make sync_data_from_s3`)
  - Creating a Python virtual environment (`make create_environment`)
  - Testing the Python environment (`make test_environment`)

#### Other Notable Configurations
- **AWS S3**: For data syncing (optional, requires AWS CLI and bucket configuration)
- **Conda/Virtualenv**: For environment management (detected automatically)


### UK Gov fork of CCDS
Source: https://ukgovdatascience.github.io/cookiecutter-data-science-gds/
Version: 76841b5 - Not maintained
```
├── LICENSE
├── Makefile
├── README.md
├── CONTRIBUTING.md
├── .env
├── .gitignore
├── test_environment.py
├── data
│   ├── external
│   ├── interim
│   ├── processed
│   └── raw
├── docs
│   └── pull_request_template.md
├── models
├── notebooks
├── references
│   ├── aqa_plan.md
│   └── assumptions_log.md
├── reports
│   └── figures
├── requirements.txt
├── setup.py
└── src
   ├── __init__.py
   ├── make_data
   ├── make_features
   ├── make_models
   ├── make_visualisations
   └── tools
```

#### Programming Language & Environment
- **Python 3** (specified in `Makefile`)
- Uses `requirements.txt` and `requirements-dev.txt` for dependency management

#### Core Dependencies
- **click**: For CLI applications
- **Sphinx**: For documentation
- **coverage**: For code coverage measurement
- **awscli**: For AWS S3 data syncing
- **flake8**: For linting
- **python-dotenv**: For environment variable management

#### Development Dependencies
- **detect-secrets**: For detecting secrets in code
- **pre-commit**: For managing pre-commit hooks

#### Build & Task Automation
- **Makefile**: For automating common tasks like:
  - Installing dependencies (`make requirements`)
  - Generating datasets (`make data`)
  - Cleaning compiled Python files (`make clean`)
  - Linting code (`make lint`)
  - Syncing data to/from S3 (`make sync_data_to_s3`, `make sync_data_from_s3`)
  - Creating a Python virtual environment (`make create_environment`)
  - Testing the Python environment (`make test_environment`)

#### Other Notable Configurations
- **AWS S3**: For data syncing (optional, requires AWS CLI and bucket configuration)
- **Conda/Virtualenv**: For environment management (detected automatically)
