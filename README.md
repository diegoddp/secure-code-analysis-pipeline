# Daily Dependency and Code Analysis Pipeline

This repository contains a CI/CD pipeline designed to perform daily dependency scanning and code (JAVA and Javascript) analysis using CodeQL. The pipeline is scheduled to run every day at 21:00 PM GMT on the `gas-scan-testing` branch.

## Pipeline Overview
The pipeline is defined in the azure-pipelines.yml file and includes the following steps:

1. Checkout Code: Fetches the latest code from the repository.
2. Initialize CodeQL: Sets up CodeQL for code analysis.
3. Cache Maven and npm Dependencies: Caches dependencies to speed up builds.
4. Build and Test: Runs Maven and npm build and test commands.
5. Dependency Scanning: Scans for vulnerabilities in dependencies.
6. CodeQL Analysis: Analyzes the code for security and quality issues.
7. Publish SARIF Files: Publishes the results of the CodeQL analysis.

## Pipeline Schedule
The pipeline is scheduled to run daily at 21:00 PM GMT on the gas-scan-testing branch.

## Environment Variables
Ensure that the following environment variables are securely stored in the pipeline settings:

- MAVEN_CACHE_FOLDER
- MAVEN_OPTS
- npm_config_cache

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.
