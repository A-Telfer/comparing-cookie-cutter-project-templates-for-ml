# Cookie Cutter Data Science (CCDS)
Source: https://cookiecutter-data-science.drivendata.org    
Version: 86152dd   

```
{{ repo name }}
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

## Programming Language & Environment
- **Python 3.10** (specified in `pyproject.toml` and `Makefile`)
- Uses `pyproject.toml` for project configuration and dependency management

## Core Dependencies
- **loguru**: For logging
- **mkdocs**: For documentation
- **pip**: For package management
- **pytest**: For testing
- **python-dotenv**: For environment variable management
- **ruff**: For linting and code formatting
- **tqdm**: For progress bars
- **typer**: For CLI applications

## Build & Task Automation
- **Makefile**: For automating common tasks like:
  - Installing dependencies (`make requirements`)
  - Cleaning compiled Python files (`make clean`)
  - Linting and formatting code (`make lint`, `make format`)
  - Running tests (`make test`)
  - Creating a Python virtual environment (`make create_environment`)
  - Generating datasets (`make data`)

## Other Notable Configurations
- **ruff**: Configured for linting and formatting with specific rules (e.g., import sorting)
- **GitHub Actions** (implied by `.github/` directory, though not inspected in detail)

