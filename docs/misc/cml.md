# Iterative CML
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

## Programming Language & Environment
- **Node.js** (>=16.0.0, specified in `package.json`)
- Uses **npm** for package management

## Core Dependencies
- **@actions/core, @actions/github**: For GitHub Actions integration
- **@octokit/core, @octokit/graphql, @octokit/rest**: For GitHub API interactions
- **node-fetch, node-ssh**: For HTTP requests and SSH operations
- **simple-git**: For Git operations
- **winston**: For logging
- **yargs**: For CLI argument parsing

## Development & Quality Tools
- **eslint**: For linting
- **prettier**: For code formatting
- **jest**: For testing
- **husky**: For Git hooks
- **lint-staged**: For running linters on staged files

## Build & Task Automation
- **Docker**: Containerization (Dockerfile and .dockerignore)
- **GitHub Actions**: For CI/CD (implied by `.github/` directory)

## Project Structure
- **src/**: Source code
- **tests/**: Test files
- **bin/**: Executable scripts
- **assets/**: Static assets

## Other Notable Configurations
- **GitHub**: The project is designed to work with GitHub (implied by GitHub Actions and Octokit)
- **CLI Tool**: The project is a CLI tool (`cml`) for CI/CD in data science and machine learning projects
