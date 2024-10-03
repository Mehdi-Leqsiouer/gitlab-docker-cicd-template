# linter-template

## CICD Templates
This repo implements Gitlab CI/CD templates to build and push your Dockerfile.


## Usage
```yaml
include:
- project: "badgerworks/cicd-template/docker-buildpush-template"
    ref: <version_tag>
    file: "docker-buildpush.yml"
```

You need at the root of your project, a Dockerfile



## Configuration 

It uses the following variables, variable that does not have default needs to be set. All required

| Name                  | description                               | default value |
|-----------------------|-------------------------------------------|--------------|
| `GCP_ARTIFACT_REGISTRY`        | Name of the artifact registry             | ``         ||
| `GCP_REGION`      | GCP region where is the artifact registry | ``       |
| `GCP_PROJECT_NAME` | GCP Project name                          | ``         |
| `GCP_PROJECT_ID`      | GCP project ID                            | ``                   |
| `GCP_POOL_ID`         | GCP WIF pool name                         | `orange-pool`        |
| `GCP_PROVIDER_ID`     | GCP WIF provider id configured            | `gitlab-tech-orange` |
| `GCP_SERVICE_ACCOUNT` | GCP Service account for CICD              | ``                   |
| `IMAGE_NAME` | Docker image name                         | ``                   |



