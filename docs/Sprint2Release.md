# Sprint 2 Release

In this sprint we release:
- Feature 1: User authentication
- Feature 2: Log Job Applications
- Feature 4: Company Wiki ("Rate My Co-op") 


For detail information about each feature. Please see our [proposal](../docs/ProjectProposal.md#core-functional-featuresuser-stories).

## Test plan

Our `test plan` for sprint 2 can be found [here](../docs/Testing%20Plan.pdf).

## Sequence diagram

We provided detailed sequence diagrams for each features [here](../architecture/sequenceDiagrams/).

- [Sequence diagrams for Feature 1.](../architecture/sequenceDiagrams/feature1/SequenceDiagram.md)

- [Sequence diagrams for Feature 2.](../architecture/sequenceDiagrams/feature2/SequenceDiagram.md)

- [Sequence diagrams for Feature 4.](../architecture/sequenceDiagrams/feature4/SequenceDiagram.md)


## TA Evaluation note

### Live demo

We are using [Render](https://render.com/) for hosting both frontend and backend. 

**Our application is available on:** https://coapp-suite.onrender.com/

In the case you need to test backend (through `Postman`), you can access it at: https://coapp-backend.onrender.com/

> \[!IMPORTANT\]
> Since we are using free service from `Render`, you may need to wait for 1-10 min for backend to spin up for the first query. After the first query, any follow up query should be at normal speed.

> \[!TIP\]
> Since we are using free service from `Render`, we need to set a third cookie for session management. Please ensure to [enable third-party cookie](https://support.google.com/chrome/answer/95647?hl=en&co=GENIE.Platform%3DDesktop) for our application to function properly.

### CI pipeline

Our CI pipelines are triggered for every push/commit/PR to main and development branches. You can find CI pipeline for [backend](https://github.com/Co-App-Team/backend/tree/main/.github/workflows) and [frontend](https://github.com/Co-App-Team/frontend/tree/main/.github/workflows)


### Frequent meeting (Scrum)

We meet on weekly basis, our meeting minute for each meeting can be found [here](https://github.com/Co-App-Team/.github/wiki/Meeting-Minutes).

### Feature and bug tracking

We track our features and user stories on [.github repository](https://github.com/Co-App-Team/.github/issues).
- Issue for feature 1 can be found [here](https://github.com/Co-App-Team/.github/issues/2). 
- Issue for feature 2 can be found [here](https://github.com/Co-App-Team/.github/issues/7)
- Issue for feature 4 can be found [here](https://github.com/Co-App-Team/.github/issues/20)

Bug and dev tasks for each feature is tracked independently on [frontend repo](https://github.com/Co-App-Team/frontend/issues) and [backend repo](https://github.com/Co-App-Team/backend/issues)

