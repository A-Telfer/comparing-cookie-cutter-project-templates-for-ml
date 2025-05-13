# MLOpsPython Microsoft
Source: https://github.com/microsoft/MLOpsPython
Version: 98a610f

```
MlOpsPython
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

## Programming Language & Environment
- **Python 3.7.5** (specified in `Dockerfile`)
- Uses **Conda** for environment and dependency management

## Core Dependencies
- **Azure CLI**: For Azure cloud services
- **Conda**: For environment management and dependency installation

## Build & Task Automation
- **Docker**: Containerization (Dockerfile and docker-image-pipeline.yml)
  - Uses `conda/miniconda3` as the base image
  - Installs Python 3.7.5 and dependencies from `ci_dependencies.yml`
- **Azure Pipelines**: For CI/CD (`.pipelines/` directory)
- **Infrastructure as Code (IaC)**:
  - **ARM Templates**: For Azure Resource Manager deployments
  - **Terraform**: For infrastructure provisioning (implied by `tf-templates/` directory)

## Project Structure
- **ml_service/**: Contains ML pipelines and utilities
- **experimentation/**: Jupyter notebooks for ML experimentation
- **environment_setup/**: Docker, IaC, and environment configuration
- **docs/**: Project documentation
- **diabetes_regression/**: Example ML project
- **charts/**: Likely for Helm charts or similar
- **data/**: Data storage
- **bootstrap/**: Initialization scripts or configurations

## Other Notable Configurations
- **Azure Cloud**: The project is designed to work with Azure services (implied by ARM templates and Azure CLI)
- **Jupyter Notebooks**: Used for ML experimentation and training
