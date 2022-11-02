# Datadog Agent
Run Datadog agent as Deployment instead of DaemonSet.


## Installing

```console
$ helm upgrade --install datadog-agent $PWD
```

## Setup
1. Configure `integrations` paramter for Datadog to check.
1. See `values.yaml` for examples
1. Use references below to enable additional integrations


### References
- https://docs.datadoghq.com/integrations/
- https://github.com/DataDog/integrations-core


## Configuration

The following table lists has the configurable parameters.

| Parameter                             | Description                                      | Default                            |
| ------------------------------------- | ------------------------------------------------ | ---------------------------------- |
| `affinity`                            | Affinity                                         | `{}`                               |
| `datadog.apiKey`                      | Datadog API key                                  | `''`                               |
| `datadog.apiSecret`                   | Secret containing Datadog API key                | `''`                               |
| `datadog.logLevel`                    | Datadog log level                                | `INFO`                             |
| `extraInitContainers`                 | Add additional initContainer                     | `{}`                               |
| `extraContainers`                     | Add additional containers                        | `{}`                               |
| `extraEnvVars`                        | Add additional env vars                          | `{}`                               |
| `extraVolumes`                        | Add additional volumes                           | `{}`                               |
| `extraScripts`                        | Add additional scripts                           | `{}`                               |
| `image.pullPolicy`                    | Image pull policy                                | `IfNotPresent`                     |
| `image.repository`                    | Datadog image repository                         | `gcr.io/datadoghq/agent`           |
| `image.tag`                           | Image tag                                        | `7.39.0`                           |
| `imagePullSecrets`                    | Secret to pull from private registry             | `[]`                               |
| `integrations`                        | Datadog integrations                             | `{}`                               |
| `podAnnotations`                      | Annotations to add to  pods                      | `{}`                               |
| `podSecurityContext`                  | Pod security context                             | `{}`                               |
| `resources`                           | Container resources                              | `{}`                               |
| `serviceAccount.annotations`          | Annotations to add to Kubernetes SA              | `{}`                               |
| `serviceAccount.create`               | Create Kubernetes SA                             | `true`                             |
| `serviceAccount.name`                 | Name to use for SA                               | `''`                               |
| `securityContext`                     | Container security context                       | `{}`                               |
| `service.port`                        | Service port                                     | `5555`                             |
| `service.type`                        | Service type                                     | `ClusterIP`                        |
| `nodeSelector`                        | Node selector                                    | `{}`                               |
| `tolerations`                         | Tolerations                                      | `{}`                               |

