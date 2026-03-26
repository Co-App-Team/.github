# Sprint 3 Release

In this sprint we release:
- Feature 3: Application Filtering/Search
- Feature 5:  Interview Calendar
- Feature 6: AI Resume Helper


For detail information about each feature. Please see our [proposal](../docs/ProjectProposal.md#core-functional-featuresuser-stories).

## Test plan

Our `test plan` for sprint 3 can be found [here](../docs/Testing%20Plan.pdf). We update the existing testing plan for sprint 2 with additional information:

1. Unit tests for feature 3,5,6
2. Acceptance tests for feature 3,5,6
3. Mutation tests for all features
4. Integration tests for feature 3,5,6

## Sequence diagram

We provided detailed sequence diagrams for each features [here](../architecture/sequenceDiagrams/).

- [Sequence diagrams for Feature 3.](../architecture/sequenceDiagrams/feature3/SequenceDiagram.md)

- [Sequence diagrams for Feature 5.](../architecture/sequenceDiagrams/feature5/SequenceDiagram.md)

- [Sequence diagrams for Feature 6.](../architecture/sequenceDiagrams/feature6/SequenceDiagram.md)


## TA Evaluation note

### Live demo

We are using [Render](https://render.com/) for hosting both frontend and backend. 

**Our application is available on:** https://coapp-suite.onrender.com/

In the case you need to test backend (through `Postman`), you can access it at: https://coapp-backend.onrender.com/

> \[!IMPORTANT\]
> Since we are using free service from `Render`, you may need to wait for 1-10 min for backend to spin up for the first query. After the first query, any follow up query should be at normal speed.

> \[!TIP\]
> Since we are using free service from `Render`, we need to set a third cookie for session management. Please ensure to [enable third-party cookie](https://support.google.com/chrome/answer/95647?hl=en&co=GENIE.Platform%3DDesktop) for our application to function properly.

### Frequent meeting (Scrum)

We meet on weekly basis, our meeting minute for each meeting can be found [here](https://github.com/Co-App-Team/.github/wiki/Meeting-Minutes).

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


### Mutation test

Our mutation test can be found [here](https://github.com/Co-App-Team/backend/tree/dev/src/test/java/com/backend/coapp/mutation). For further description about our mutation tests and the report can be found in our [Testing plan](../docs/Testing%20Plan.pdf).

### CI pipeline

Our CI pipelines are triggered for every push/commit/PR to main and development branches. You can find CI pipeline for [backend](https://github.com/Co-App-Team/backend/tree/main/.github/workflows) and [frontend](https://github.com/Co-App-Team/frontend/tree/main/.github/workflows)


### Feature and bug tracking

We track our features and user stories on [.github repository](https://github.com/Co-App-Team/.github/issues).
- Issue for feature 3 can be found [here](https://github.com/Co-App-Team/.github/issues/16). 
- Issue for feature 5 can be found [here](https://github.com/Co-App-Team/.github/issues/24).
- Issue for feature 6 can be found [here](https://github.com/Co-App-Team/.github/issues/28).

Bug and dev tasks for each feature is tracked independently on [frontend repo](https://github.com/Co-App-Team/frontend/issues) and [backend repo](https://github.com/Co-App-Team/backend/issues)

### Run our application locally

To build and run our application locally, please follow the instructions:
- For frontend: [CONTRIBUTING.md](https://github.com/Co-App-Team/frontend?tab=contributing-ov-file#setup-instructions)
- For backend: [CONTRIBUTING.md](https://github.com/Co-App-Team/backend?tab=contributing-ov-file#setup-instructions)