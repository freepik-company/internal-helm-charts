# cog-ai-model

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

A Helm chart to install an IA model with Cog

## Values

| Key                                        | Type   | Default                                          | Description |
|--------------------------------------------|--------|--------------------------------------------------|-------------|
| affinity                                   | object | `{}`                                             |             |
| autoscaling.enabled                        | bool   | `false`                                          |             |
| autoscaling.maxReplicas                    | int    | `100`                                            |             |
| autoscaling.minReplicas                    | int    | `1`                                              |             |
| autoscaling.targetCPUUtilizationPercentage | int    | `80`                                             |             |
| config.modelLocalDir                       | string | `"/var/model/<model-name>"`                      |             |
| config.modelRepo                           | string | `"https://huggingface.co/THUDM/cogvlm-chat-hfnv"` |             |
| config.modelRepo                           | string | `"https://the-repository-of-the-model"`          |             |
| fullnameOverride                           | string | `""`                                             |             |
| image.pullPolicy                           | string | `"IfNotPresent"`                                 |             |
| image.repository                           | string | `"your-docker-repo/image-name"`                  |             |
| image.tag                                  | string | `""`                                             |             |
| imagePullSecrets                           | list   | `[]`                                             |             |
| ingress.annotations                        | object | `{}`                                             |             |
| ingress.className                          | string | `""`                                             |             |
| ingress.enabled                            | bool   | `false`                                          |             |
| ingress.hosts[0].host                      | string | `"chart-example.local"`                          |             |
| ingress.hosts[0].paths[0].path             | string | `"/"`                                            |             |
| ingress.hosts[0].paths[0].pathType         | string | `"ImplementationSpecific"`                       |             |
| ingress.tls                                | list   | `[]`                                             |             |
| initContainer.enabled                      | string | `"true"`                                         |             |
| nameOverride                               | string | `""`                                             |             |
| nodeSelector                               | object | `{}`                                             |             |
| podAnnotations                             | object | `{}`                                             |             |
| podLabels                                  | object | `{}`                                             |             |
| podSecurityContext                         | object | `{}`                                             |             |
| replicaCount                               | int    | `1`                                              |             |
| resources                                  | list   | `[]`                                             |             |
| securityContext                            | object | `{}`                                             |             |
| service.port                               | int    | `5000`                                           |             |
| service.targetPort                         | int    | `5000`                                           |             |
| service.type                               | string | `"NodePort"`                                     |             |
| serviceAccount.annotations                 | object | `{}`                                             |             |
| serviceAccount.automount                   | bool   | `true`                                           |             |
| serviceAccount.create                      | bool   | `true`                                           |             |
| serviceAccount.name                        | string | `""`                                             |             |
| tolerations                                | list   | `[]`                                             |             |
| apiGateway.enabled                         | bool   | `false`                                          |             |
| apiGateway.parentRefs                      | object | `{}`                                             |             |
| apiGateway.parentRefs.name                 | string | `stable`                                         |             |
| apiGateway.parentRefs.namespace            | string | `gw-ns`                                          |             |
| apiGateway.annotations                     | object | `{}`                                             |             |
| apiGateway.hostnames                       | object | `{}`                                             |             |
| routes                                     | object | `{}`                                             |             |
| routes.routeName                           | object | `{}`                                             |             |
| routes.rules.matches                       | list   | `[]`                                             |             |
| routes.rules.matchesExtra                  | list   | `[]`                                             |     https://gateway-api.sigs.k8s.io/reference/spec/#gateway.networking.k8s.io/v1.HTTPRouteMatch        |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.8.1](https://github.com/norwoodj/helm-docs/releases/v1.8.1)
