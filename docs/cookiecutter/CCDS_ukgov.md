# UK Gov fork of CCDS
Source: https://github.com/ukgovdatascience/cookiecutter-data-science-gds    
Version: 76841b5 - Not maintained   
```
{{ repo name }}
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

## Programming Language & Environment
- **Python 3** (specified in `Makefile`)
- Uses `requirements.txt` and `requirements-dev.txt` for dependency management

## Core Dependencies
- **click**: For CLI applications
- **Sphinx**: For documentation
- **coverage**: For code coverage measurement
- **awscli**: For AWS S3 data syncing
- **flake8**: For linting
- **python-dotenv**: For environment variable management

## Development Dependencies
- **detect-secrets**: For detecting secrets in code
- **pre-commit**: For managing pre-commit hooks

## Build & Task Automation
- **Makefile**: For automating common tasks like:
  - Installing dependencies (`make requirements`)
  - Generating datasets (`make data`)
  - Cleaning compiled Python files (`make clean`)
  - Linting code (`make lint`)
  - Syncing data to/from S3 (`make sync_data_to_s3`, `make sync_data_from_s3`)
  - Creating a Python virtual environment (`make create_environment`)
  - Testing the Python environment (`make test_environment`)

## Other Notable Configurations
- **AWS S3**: For data syncing (optional, requires AWS CLI and bucket configuration)
- **Conda/Virtualenv**: For environment management (detected automatically)
