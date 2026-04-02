# Sprint 4 Release

In this sprint we release:
- Load test
- Bugs fixed and enhanced the robustness of the system


For detail information about each feature. Please see our [proposal](../docs/ProjectProposal.md#core-functional-featuresuser-stories).

## Test plan

Our `test plan` for sprint 4 can be found [here](../docs/Testing%20Plan.pdf). We update the existing testing plan for sprint 2 and 3 with load test report.


## TA Evaluation note

### Production environment

We are using [Render](https://render.com/) for hosting both frontend and backend, which are built from `Docker` images. 

**Our application is available on:** https://coapp-suite.onrender.com/

In the case you need to test backend (through `Postman`), you can access it at: https://coapp-backend.onrender.com/

> \[!IMPORTANT\]
> Since we are using free service from `Render`, you may need to wait for 1-10 min for backend to spin up for the first query. After the first query, any follow up query should be at normal speed.

> \[!TIP\]
> Since we are using free service from `Render`, we need to set a third cookie for session management. Please ensure to [enable third-party cookie](https://support.google.com/chrome/answer/95647?hl=en&co=GENIE.Platform%3DDesktop) for our application to function properly.

### Project package structure

Detailed information about our package structure can be found as follows:
1. Backend: https://github.com/Co-App-Team/backend/blob/main/docs/ARCHITECTURE.md
2. Frontend: https://github.com/Co-App-Team/frontend/blob/main/docs/ARCHITECTURE.md

### Coding style

Information about the coding style that we adopt can be found:
1. Backend: https://github.com/Co-App-Team/backend?tab=contributing-ov-file#coding-standard
2. Frontend: https://github.com/Co-App-Team/backend?tab=contributing-ov-file#coding-standard


### CI pipeline

Our CI pipelines are triggered for every push/commit/PR to main and development branches. You can find CI pipeline for [backend](https://github.com/Co-App-Team/backend/tree/main/.github/workflows) and [frontend](https://github.com/Co-App-Team/frontend/tree/main/.github/workflows)


### CD pipeline

Our CD pipeline is set up and can be found here:
- Frontend: https://github.com/Co-App-Team/frontend/blob/develop/.github/workflows/cd-pipeline.yml
- Backend :https://github.com/Co-App-Team/backend/blob/dev/.github/workflows/deploy.yml

On the release day, we trigger CD workflow, which builds and pushes Docker image to `DockerHub`, via `Action`:
- Frontend: https://github.com/Co-App-Team/frontend/actions/workflows/cd-pipeline.yml
- Backend: https://github.com/Co-App-Team/backend/actions/workflows/deploy.yml

After the workflows run successfully, the `Docker` images are built and pushed to:
- Frontend: https://hub.docker.com/repository/docker/ntgbao87/co-app-frontend/general
- Backend: https://hub.docker.com/repository/docker/ntgbao87/co-app-backend/general


### Load test

Our load test can be found [here](https://github.com/Co-App-Team/backend/blob/main/src/test/java/com/backend/coapp/_performance/loadtest.js). For further description about our load tests and the report can be found in our [Testing plan](../docs/Testing%20Plan.pdf).

To run load tests (and other tests in the backend), please see the instruction in [CONTRIBUTING.md](https://github.com/Co-App-Team/backend?tab=contributing-ov-file#testing)

### Security Scanner

We adopt `Sonarqube` as security scanner, which will automatically scan every new PR to default branch (`development`). 

To see the scanning status of our project, please checkout [SonarQube](https://sonarcloud.io/organizations/co-app-team/projects).

Since we set up `Sonarqube` at Sprint 3, so we have been continously fixing any new issues raised by `Sonarqube` in every PR to default branch.

For your reference, we also spent time to fixed code smells found by `Sonarqube` in the following PRs:
- https://github.com/Co-App-Team/backend/pull/176
- https://github.com/Co-App-Team/backend/pull/177
- https://github.com/Co-App-Team/backend/pull/174

### Run our application locally

To build and run our application locally, please follow the instructions:
- For frontend: [CONTRIBUTING.md](https://github.com/Co-App-Team/frontend?tab=contributing-ov-file#setup-instructions)
- For backend: [CONTRIBUTING.md](https://github.com/Co-App-Team/backend?tab=contributing-ov-file#setup-instructions)