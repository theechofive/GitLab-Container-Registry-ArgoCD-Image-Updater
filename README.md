# ArgoCD Image Updater With GitLab Container Registry
```
  +--------------+
  |   User       |
  +--------------+
         |
         | (1) Commits code changes
         v
  +---------------------------+
  | Source Code and Image Build |
  |      (Repository #1)       |
  +---------------------------+
         |
         | (2) Triggers GitLab CI/CD pipeline for Docker image build
         v
  +-------------------------------+
  |   GitLab Container Registry   |
  |      (Image Storage)          |
  +-------------------------------+
         |
         | (3) Notification of image update
         v
  +-------------------------------+
  |   Argo CD Image Updater       |
  | (Configuration Update)        |
  +-------------------------------+
         |
         | (4) Commits updated image tags
         v
  +-------------------------------------+
  |       Configuration Repository      |
  |         (Repository #2)             |
  +-------------------------------------+
         |
         | (5) Argo CD monitors for changes
         v
  +---------------------------+
  |         Argo CD           |
  | (Cluster Synchronization) |
  +---------------------------+

```

Install
![image](https://github.com/theechofive/ArgoCD-Image-Updater-GitLab-Container-Registry/assets/32634559/3c772d44-def1-44ff-a05c-c713146ee771)
create token
....
create encode string
...
create .dockerconfigjson
...
create secret
...
apply ingress

%SCREENSHOTS%

add manifest repo to argocd
