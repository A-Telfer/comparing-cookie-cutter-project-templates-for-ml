# Cookie Cutter MLOPs Chim-50
Source: https://github.com/Chim-SO/cookiecutter-mlops
Version: 526751d
```
{{ repo_name }}
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

## Programming Language & Environment
- **Python 3** (specified in `Makefile`)
- Uses `requirements.txt` for dependency management

## Core Dependencies
- **pip, setuptools, wheel**: For package management
- **flake8**: For linting

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
