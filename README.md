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
Source: https://github.com/ukgovdatascience/cookiecutter-data-science-gds
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


### MLOpsPython Microsoft
Source: https://github.com/microsoft/MLOpsPython
Version: 98a610f

```
├── LICENSE
├── README.md
├── bootstrap
│   ├── README.md
│   └── bootstrap.py
├── charts
│   ├── abtest-istio
│   │   ├── Chart.yaml
│   │   ├── templates
│   │   │   └── istio-canary.yaml
│   │   └── values.yaml
│   ├── abtest-model
│   │   ├── Chart.yaml
│   │   ├── templates
│   │   │   ├── deployment.yaml
│   │   │   └── service.yaml
│   │   └── values.yaml
│   └── load_test.sh
├── data
│   ├── README.md
│   ├── data_test.py
│   ├── diabetes.csv
│   ├── diabetes_bad_dist.csv
│   ├── diabetes_bad_schema.csv
│   └── diabetes_missing_values.csv
├── diabetes_regression
│   ├── ci_dependencies.yml
│   ├── conda_dependencies.yml
│   ├── conda_dependencies_scorecopy.yml
│   ├── conda_dependencies_scoring.yml
│   ├── evaluate
│   │   └── evaluate_model.py
│   ├── parameters.json
│   ├── register
│   │   └── register_model.py
│   ├── scoring
│   │   ├── deployment_config_aci.yml
│   │   ├── deployment_config_aks.yml
│   │   ├── inference_config.yml
│   │   ├── parallel_batchscore.py
│   │   ├── parallel_batchscore_copyoutput.py
│   │   ├── score.py
│   │   ├── scoreA.py
│   │   └── scoreB.py
│   ├── training
│   │   ├── R
│   │   │   ├── r_train.r
│   │   │   ├── train_with_r.py
│   │   │   ├── train_with_r_on_databricks.py
│   │   │   └── weight_data.csv
│   │   ├── test_train.py
│   │   ├── train.py
│   │   └── train_aml.py
│   └── util
│       ├── __init__.py
│       └── model_helper.py
├── docs
│   ├── canary_ab_deployment.md
│   ├── code_description.md
│   ├── custom_container.md
│   ├── custom_model.md
│   ├── development_setup.md
│   ├── getting_started.md
│   └── images
│       ├── ADO-CD-pipeline-to-webapp.png
│       ├── aci-in-azure-portal.png
│       ├── appservice-webapp-deploymentcenter.png
│       ├── batch-child-run-scoringstep.png
│       ├── batchscoring-ci-result.png
│       ├── batchscoring-pipeline.png
│       ├── build-connect.png
│       ├── ci-build-pipeline-configure.png
│       ├── container-registry-webapp-image.png
│       ├── create-rm-service-connection.png
│       ├── created-resources.png
│       ├── custom-container-variables.png
│       ├── deploy-aci.png
│       ├── deploy-aks.png
│       ├── library_variable_groups.png
│       ├── ml-lifecycle.png
│       ├── ml-ws-svc-connection.png
│       ├── model-artifact-cd-trigger.png
│       ├── model-artifact.png
│       ├── model-deploy-configure.png
│       ├── model-deploy-get-artifact-logs.png
│       ├── model-deploy-result.png
│       ├── model-train-register-artifacts.png
│       ├── model-train-register.png
│       ├── multi-stage-aci-aks.png
│       ├── multi-stage-aci.png
│       ├── multi-stage-webapp.png
│       ├── release-task-createimage.PNG
│       ├── release-task-webappdeploy.PNG
│       ├── release-webapp-pipeline.PNG
│       ├── run-iac-pipeline.png
│       ├── scoring_image.png
│       ├── select-iac-pipeline.png
│       ├── trained-model.png
│       └── training-pipeline.png
├── environment_setup
│   ├── Dockerfile
│   ├── arm-templates
│   │   └── cloud-environment.json
│   ├── docker-image-pipeline.yml
│   ├── iac-create-environment-pipeline-arm.yml
│   ├── iac-create-environment-pipeline-tf.yml
│   ├── iac-remove-environment-pipeline.yml
│   ├── install_requirements.sh
│   └── tf-templates
│       ├── backend.tf
│       └── main.tf
├── experimentation
│   ├── Diabetes Ridge Regression Experimentation Pipeline.ipynb
│   ├── Diabetes Ridge Regression Parameter Experimentation.ipynb
│   ├── Diabetes Ridge Regression Scoring.ipynb
│   └── Diabetes Ridge Regression Training.ipynb
└── ml_service
    ├── __init__.py
    ├── pipelines
    │   ├── __init__.py
    │   ├── diabetes_regression_build_parallel_batchscore_pipeline.py
    │   ├── diabetes_regression_build_train_pipeline.py
    │   ├── diabetes_regression_build_train_pipeline_with_r.py
    │   ├── diabetes_regression_build_train_pipeline_with_r_on_dbricks.py
    │   ├── load_sample_data.py
    │   ├── run_parallel_batchscore_pipeline.py
    │   └── run_train_pipeline.py
    └── util
        ├── __init__.py
        ├── attach_compute.py
        ├── create_scoring_image.py
        ├── create_scoring_image.sh
        ├── env_variables.py
        ├── manage_environment.py
        └── smoke_test_scoring_service.py
```

#### Programming Language & Environment
- **Python 3.7.5** (specified in `Dockerfile`)
- Uses **Conda** for environment and dependency management

#### Core Dependencies
- **Azure CLI**: For Azure cloud services
- **Conda**: For environment management and dependency installation

#### Build & Task Automation
- **Docker**: Containerization (Dockerfile and docker-image-pipeline.yml)
  - Uses `conda/miniconda3` as the base image
  - Installs Python 3.7.5 and dependencies from `ci_dependencies.yml`
- **Azure Pipelines**: For CI/CD (`.pipelines/` directory)
- **Infrastructure as Code (IaC)**:
  - **ARM Templates**: For Azure Resource Manager deployments
  - **Terraform**: For infrastructure provisioning (implied by `tf-templates/` directory)

#### Project Structure
- **ml_service/**: Contains ML pipelines and utilities
- **experimentation/**: Jupyter notebooks for ML experimentation
- **environment_setup/**: Docker, IaC, and environment configuration
- **docs/**: Project documentation
- **diabetes_regression/**: Example ML project
- **charts/**: Likely for Helm charts or similar
- **data/**: Data storage
- **bootstrap/**: Initialization scripts or configurations

#### Other Notable Configurations
- **Azure Cloud**: The project is designed to work with Azure services (implied by ARM templates and Azure CLI)
- **Jupyter Notebooks**: Used for ML experimentation and training


### Iterative CML
Source: https://github.com/iterative/cml
Version: a3a66c7

```
├── Dockerfile
├── LICENSE
├── README.md
├── assets
│   ├── demo.tf
│   ├── logo.pdf
│   ├── logo.png
│   ├── test.md
│   ├── test.svg
│   ├── vega-lite.json
│   └── watermark.svg
├── bin
│   ├── cml
│   │   ├── asset
│   │   │   ├── publish.e2e.test.js
│   │   │   ├── publish.js
│   │   │   └── publish.test.js
│   │   ├── asset.js
│   │   ├── check
│   │   │   ├── create.e2e.test.js
│   │   │   ├── create.js
│   │   │   └── create.test.js
│   │   ├── check.js
│   │   ├── comment
│   │   │   ├── create.e2e.test.js
│   │   │   ├── create.js
│   │   │   ├── create.test.js
│   │   │   └── update.js
│   │   ├── comment.js
│   │   ├── pr
│   │   │   ├── create.e2e.test.js
│   │   │   └── create.js
│   │   ├── pr.js
│   │   ├── repo
│   │   │   ├── prepare.js
│   │   │   └── prepare.test.js
│   │   ├── repo.js
│   │   ├── runner
│   │   │   ├── launch.e2e.test.js
│   │   │   ├── launch.js
│   │   │   └── launch.test.js
│   │   ├── runner.js
│   │   ├── tensorboard
│   │   │   ├── connect.e2e.test.js
│   │   │   ├── connect.js
│   │   │   └── connect.test.js
│   │   ├── tensorboard.js
│   │   ├── workflow
│   │   │   ├── rerun.js
│   │   │   └── rerun.test.js
│   │   └── workflow.js
│   ├── cml.js
│   ├── cml.test.js
│   └── legacy
│       ├── commands
│       │   ├── ci.js
│       │   ├── publish.js
│       │   ├── rerun-workflow.js
│       │   ├── send-comment.js
│       │   ├── send-github-check.js
│       │   └── tensorboard-dev.js
│       ├── deprecation.js
│       ├── link.e2e.test.js
│       └── link.js
├── package-lock.json
├── package.json
├── src
│   ├── analytics.e2e.test.js
│   ├── analytics.js
│   ├── cml.e2e.test.js
│   ├── cml.js
│   ├── commenttarget.js
│   ├── commenttarget.test.js
│   ├── drivers
│   │   ├── bitbucket_cloud.e2e.test.js
│   │   ├── bitbucket_cloud.js
│   │   ├── github.e2e.test.js
│   │   ├── github.js
│   │   ├── gitlab.e2e.test.js
│   │   └── gitlab.js
│   ├── logger.js
│   ├── terraform.js
│   ├── terraform.test.js
│   ├── utils.js
│   ├── utils.test.js
│   ├── watermark.js
│   └── watermark.test.js
└── tests
    ├── proxy.js
    ├── setup.js
    └── teardown.js
```

#### Programming Language & Environment
- **Node.js** (>=16.0.0, specified in `package.json`)
- Uses **npm** for package management

#### Core Dependencies
- **@actions/core, @actions/github**: For GitHub Actions integration
- **@octokit/core, @octokit/graphql, @octokit/rest**: For GitHub API interactions
- **node-fetch, node-ssh**: For HTTP requests and SSH operations
- **simple-git**: For Git operations
- **winston**: For logging
- **yargs**: For CLI argument parsing

#### Development & Quality Tools
- **eslint**: For linting
- **prettier**: For code formatting
- **jest**: For testing
- **husky**: For Git hooks
- **lint-staged**: For running linters on staged files

#### Build & Task Automation
- **Docker**: Containerization (Dockerfile and .dockerignore)
- **GitHub Actions**: For CI/CD (implied by `.github/` directory)

#### Project Structure
- **src/**: Source code
- **tests/**: Test files
- **bin/**: Executable scripts
- **assets/**: Static assets

#### Other Notable Configurations
- **GitHub**: The project is designed to work with GitHub (implied by GitHub Actions and Octokit)
- **CLI Tool**: The project is a CLI tool (`cml`) for CI/CD in data science and machine learning projects


### ZenML-io 
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

#### Programming Language & Environment
- **Python** (>=3.9, <3.13, specified in `pyproject.toml`)
- Uses **Poetry** for dependency management

#### Core Dependencies
- **alembic**: For database migrations
- **bcrypt, passlib**: For password hashing
- **click**: For CLI applications
- **cloudpickle**: For serialization
- **docker**: For containerization
- **gitpython**: For Git operations
- **pydantic, pydantic-settings**: For data validation and settings management
- **sqlalchemy, sqlalchemy_utils, sqlmodel**: For database ORM
- **rich**: For terminal formatting and Jupyter integration

#### Optional Dependencies
- **ZenServer**: FastAPI, uvicorn, pyjwt, etc.
- **Project Templates**: copier, jinja2-time, etc.
- **Cloud Secrets**: AWS, GCP, Azure, HashiCorp Vault
- **Cloud Connectors**: AWS, GCP, Azure, Kubernetes
- **Artifact Stores**: S3, GCS, Azure
- **Orchestrators**: Sagemaker, Vertex, AzureML

#### Development & Quality Tools
- **bandit**: For security linting
- **coverage**: For code coverage measurement
- **mypy**: For static type checking
- **ruff**: For linting and formatting
- **pytest**: For testing (with plugins like pytest-mock, pytest-clarity, etc.)
- **mkdocs**: For documentation (with plugins like mkdocs-material, mkdocstrings, etc.)

#### Build & Task Automation
- **Docker**: Containerization (Dockerfile and .dockerignore)
- **GitHub Actions**: For CI/CD (implied by `.github/` directory)

#### Project Structure
- **src/**: Source code
- **tests/**: Test files
- **scripts/**: Utility scripts
- **docs/**: Documentation
- **examples/**: Example projects
- **infra/**: Infrastructure configurations
- **helm/**: Helm charts

#### Other Notable Configurations
- **GitHub**: The project is designed to work with GitHub (implied by GitHub Actions)
- **CLI Tool**: The project is a CLI tool (`zenml`) for MLOps and production-ready ML code

