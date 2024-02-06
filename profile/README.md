![wakapi badge](https://wakapi.simulatan.me/api/badge/SIMULATAN/interval:any/label:ContestSubmission?label=Time%20Spent)

# ContestSubmission
A school project all about managing contests, submissions and participants.

## Repositories
- [Frontend](https://github.com/ContestSubmission/Frontend)
- [Backend](https://github.com/ContestSubmission/Backend)
- [GitOps](https://github.com/ContestSubmission/GitOps)
  - contains the kubernetes manifests for the project
  - the configs in this repo are deployed by [ArgoCD](https://argoproj.github.io/cd/)

## Deployment
The production backend instance runs in my own kubernetes cluster and is deployed by [ArgoCD](https://argoproj.github.io/cd/).

On the other hand, the frontend is deployed on [CloudFlare Pages](https://pages.cloudflare.com/). The reason is that it has to stay online even in high-pressure situations. The backend will be the bottleneck in that case, however, the impact is reduced by showing fancy loading screens in the frontend to reduce the perceived load time.
