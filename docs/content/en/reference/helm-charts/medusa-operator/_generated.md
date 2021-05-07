

![Version: 0.29.0](https://img.shields.io/badge/Version-0.29.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.1.0](https://img.shields.io/badge/AppVersion-0.1.0-informational?style=flat-square)

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| K8ssandra Team | k8ssandra-developers@googlegroups.com | https://github.com/k8ssandra |

## Source Code

* <https://github.com/k8ssandra/medusa-operator>
* <https://github.com/k8ssandra/k8ssandra/tree/main/charts/medusa-operator>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| file://../k8ssandra-common | k8ssandra-common | 0.28.1 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| nameOverride | string | `""` | Replaces the chart name which is used in the metadata.name of objects created by this chart. |
| fullnameOverride | string | `""` | Replaces the value used for metadata.name in objects created by this chart. The default value has the form releaseName-chartName. |
| commonLabels | object | `{}` | Labels to be added to all deployed resources |
| replicaCount | int | `1` | Sets the number of medusa-operator pods. |
| image.repository | string | `"docker.io/k8ssandra/medusa-operator"` | Container repository where the medusa-operator resides |
| image.pullPolicy | string | `"IfNotPresent"` | Pull policy for the operator container |
| image.tag | string | `"v0.2.0"` | Tag of the medusa-operator image to pull from image.repository |
| imagePullSecrets | list | `[]` | References to secrets to use when pulling images. ref: https://kubernetes.io/docs/tasks/configure-pod-container/pull-image-private-registry/ |
| serviceAccount.annotations | object | `{}` | Annotations for the medusa-operator service account. |
| podAnnotations | object | `{}` | Annotations for the medusa-operator pod. |
| podSecurityContext | object | `{}` | PodSecurityContext for the medusa-operator pod. |
| securityContext.readOnlyRootFilesystem | bool | `true` | Mark root filesystem as read only |
| securityContext.runAsNonRoot | bool | `true` | Run medusa-operator container as non-root user |
| securityContext.runAsGroup | int | `65534` | Group for the user running the medusa-operator container / process |
| securityContext.runAsUser | int | `65534` | User for running the medusa-operator container / process |
| resources | object | `{}` | Resources requests and limits for the cass-operator pod. We usually recommend not to specify default resources and to leave this as a conscious choice for the user. This also increases chances charts run on environments with little resources, such as Minikube. If you do want to specify resources, uncomment the following lines, adjust them as necessary, and remove the curly braces after 'resources:'. limits: cpu: 100m memory: 128Mi requests: cpu: 100m memory: 128Mi |