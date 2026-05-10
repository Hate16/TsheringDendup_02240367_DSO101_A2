# Assignment 2 — CI/CD with Jenkins

## How I Configured the Pipeline

1. Installed Jenkins on Windows and configured the NodeJS plugin (v20 LTS).
2. Created a GitHub PAT and added it as credentials in Jenkins.
3. Wrote a `Jenkinsfile` with 4 stages: Checkout, Install, Build, and Test.
4. Configured Jest with `jest-junit` to produce JUnit-compatible test reports.
5. Created a Pipeline job in Jenkins pointing to this repository.

## Pipeline Stages
- **Checkout** – pulls code from GitHub
- **Install** – runs `npm install`
- **Build** – runs `npm run build`
- **Test** – runs Jest and publishes results to Jenkins

## Challenges Faced
- On Windows, `sh` commands don't work in Jenkins; replaced with `bat`.
- Had to configure `jest-junit` output path to match what Jenkins expects (`junit.xml`).

## GitHub Repository
https://github.com/Hate16/DSO_Assignment2.git