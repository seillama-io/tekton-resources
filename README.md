# Tetkon Resources

General purpose Tekton resources for DevSecOps on Kubernetes.

## Concept

The goal of this project is to provide an easy to use set of tools to implement modern DevSecOps practices on Kubernetes (or Red Hat OpenShift).

The implemented pipeline is the following:

![Pipeline design](design/pipeline.png)

## Tekton Hub Tasks

Some of the Tekton tasks we use are based on Tekton Hub to reduce maintenance cost, the following shows how to retrieve these tasks.

Prereqs:
- [Tekton CLI](https://tekton.dev/docs/cli/): `tkn`

```sh
tkn hub get task git-clone --version 0.9 > tasks/git-clone/git-clone.yaml
tkn hub get task sonarqube-scanner --version 0.4 > tasks/code-scan/code-scan.yaml
tkn hub get task hadolint --version 0.1 > tasks/dockerfile-lint/dockerfile-lint.yaml
tkn hub get task buildah --version 0.5 > tasks/img-build/img-build.yaml
tkn hub get task trivy-scanner --version 0.2 > tasks/img-scan/img-scan.yaml
```
