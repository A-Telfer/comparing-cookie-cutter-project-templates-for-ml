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
│   ├── external
│   ├── interim
│   ├── processed
│   └── raw
├── docs
│   └── pull_request_template.md
├── models
├── notebooks
├── references
│   ├── aqa_plan.md
│   └── assumptions_log.md
├── reports
│   └── figures
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