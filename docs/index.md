# Project Template Comparison

This repo compares project structures for ML/AI

- CCDS: Cookie Cutter Data Science
- CML: Continuous Machine Learning
- ZenML: Zen Machine Learning
- MLOpsPython: Microsoft MLOps Python
- "-" indicates the technology is not used or not explicitly mentioned in the repository


## Technology Comparisons
| Technology | CCDS | CML | MLOpsPython | ZenML | CCDS UK Gov | CCDS MLOPs fmind | CCDS MLOPs chim50 |
|------------|------|-----|-------------|-------|-------------|-------------------|-------------------|
| **Programming Languages** | Python 3.10 | Node.js >=16.0.0 | Python 3.7.5 | Python >=3.9, <3.13 | Python 3 | Python 3.13 | Python 3 |
| **Dependency Management** | pyproject.toml | npm | Conda | Poetry | requirements.txt | pyproject.toml | requirements.txt |
| **Build Tools** | Makefile | npm scripts | Makefile | Poetry | Makefile | just | Makefile |
| **Containerization** | - | Docker (CI/CD) | Docker | Docker | - | Docker | - |
| **CI/CD** | GitHub Actions | GitHub Actions | Azure Pipelines | GitHub Actions | GitHub Actions | GitHub Actions | GitHub Actions |
| **Testing** | pytest | jest | pytest | pytest | - | pytest | - |
| **Linting** | ruff | eslint/prettier | - | ruff | flake8 | ruff | flake8 |
| **Type Checking** | - | - | - | mypy | - | mypy | - |
| **Documentation** | - | - | - | mkdocs | Sphinx | pdoc | - |
| **Cloud Services** | - | - | Azure | AWS/GCP/Azure | AWS S3 | - | AWS S3 |
| **ML Tools** | - | - | - | - | - | mlflow | - |
| **Notebooks** | - | - | Jupyter | Jupyter | - | ipykernel | - |
| **CLI Framework** | typer | yargs | - | click | click | - | - |
| **Security** | - | - | - | bandit | detect-secrets | bandit | - |
| **Git Hooks** | - | husky | - | pre-commit | pre-commit | pre-commit | - |


## Folder Structure Comparisons

| Folder | CCDS | CML | MLOpsPython | ZenML | CCDS UK Gov | CCDS MLOPs fmind | CCDS MLOPs chim50 |
|--------|------|-----|-------------|-------|-------------|-------------------|-------------------|
| **Source Code** | `{{ module_name }}/` | `src/` | `ml_service/` | `src/zenml/` | `src/` | `src/` | `src/` |
| **Tests** | - | `tests/` | - | `tests/` | - | `tests/` | - |
| **Data** | `data/` | - | `data/` | - | `data/` | `data/` | `data/` |
| **Notebooks** | `notebooks/` | - | `experimentation/` | `examples/` | `notebooks/` | `notebooks/` | `notebooks/` |
| **Documentation** | `docs/` | - | `docs/` | `docs/` | `docs/` | `docs/` | `docs/` |
| **Models** | `models/` | - | - | - | `models/` | - | `models/` |
| **Reports** | `reports/` | - | - | - | `reports/` | `outputs/` | `reports/` |
| **References** | `references/` | - | - | - | `references/` | - | - |
| **Configuration** | - | - | - | - | - | `confs/` | `configs/` |
| **Infrastructure** | - | - | `environment_setup/` | `infra/` | - | - | - |
| **Docker** | - | - | `environment_setup/` | `docker/` | - | - | - |
| **Helm Charts** | - | - | `charts/` | `helm/` | - | - | - |
| **Assets** | - | `assets/` | - | - | - | - | - |


## Entrypoints

| Type | CCDS | CML | MLOpsPython | ZenML | CCDS UK Gov | CCDS MLOPs fmind | CCDS MLOPs chim50 |
|------|------|-----|-------------|-------|-------------|-------------------|-------------------|
| **CLI Entrypoints** | `{{ module_name }}/scripts.py` | `bin/cml.js` | `ml_service/pipelines/*.py` | `src/zenml/cli/cli.py` | `src/make_*` | `src/{{ project_name }}/scripts.py` | `src/data/*.py` |
| **Task Scripts** | - | - | `scripts/` | `scripts/` | - | `tasks/*.just` | - |
| **Build Scripts** | `Makefile` | `package.json` | `Makefile` | `pyproject.toml` | `Makefile` | `justfile` | `Makefile` |
| **CI/CD Scripts** | `.github/` | `.github/` | `.pipelines/` | `.github/` | `.github/` | `.github/` | `.github/` |
| **Docker Scripts** | - | `Dockerfile` | `environment_setup/Dockerfile` | `docker/*.Dockerfile` | - | `Dockerfile` | - |
| **Infrastructure Scripts** | - | - | `environment_setup/*.yml` | `infra/` | - | - | - |
| **Utility Scripts** | - | `bin/` | `ml_service/util/` | `scripts/` | `src/tools/` | - | - |



## Separaton of Train/Test

**Separation Patterns:**

1. **Module-Based Separation:**
   - **CCDS**: Separate `train.py` and `predict.py` in `modeling/`
   - **CCDS MLOPs chim50**: Separate `train.py` and `predict.py` in `models/model1/`

2. **Directory-Based Separation:**
   - **MLOpsPython**: Separate `training/` and `scoring/` directories
   - **ZenML**: Example-based separation in `examples/`

3. **Combined Approach:**
   - **CCDS MLOPs fmind**: Combined in `scripts.py`
   - **CCDS UK Gov**: No explicit inference

4. **N/A:**
   - **CML**: CLI tool, no training/inference
