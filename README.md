# My Turn App Configuration

Files needed to deploy My Turn App on Openshift through Argo CD and Tekton Pipelines.

## This Repository

Here you'll find several YAMLs files and Dockerfiles used to deploy My Turn App over Openshift Platform through ArgoCD.
To understand the directories and files check the tree bellow:

```bash
.
|-- README.md # This documentation file in written in Markdown.
|-- deployments.yaml # List of DeploymentConfigs for Front and Back end layer.
|-- networking.yaml # List of Routes and Services for Front and Back end layer.
|-- pipelines
|   |-- dependencies-pvc.yaml # List of Routes and Services for Front and Back end layer.
|   |-- pipelines.yaml # Front and Back end tekton pipeline.
|   |-- secrets.yaml # Docker configuration to publish images built during the pipeline execution.
|   `-- triggers.yaml # List of components to generate the webhook URL.
`-- tasks
    |-- build-backend-image
    |   `-- task.yaml # Description of Backend Build Task.
    |-- build-frontend-image
    |   `-- task.yaml # Description of Frontend Build Task.
    |-- images
    |   |-- Dockerfile.npm-alpine # Dockerfile to generate an image used in some tasks steps.
    |   `-- Dockerfile.toolchain-cli-alpine # Dockerfile to generate an image used in some tasks steps.
    |-- oc-rollout-layer
    |   `-- task.yaml # Description of Openshift Deploy Task.
    `-- vue-e2e-test
        `-- task.yaml # Description of E2E Test Task.
```
