# Saltstack Helm

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 3004](https://img.shields.io/badge/AppVersion-3004-informational?style=flat-square)

A Helm chart to run Salt Master on Kubernetes.

## What is Salt?

Salt is a configuration management tool / orchestration platform.

This image contains a running salt-master and salt-api process, which can be used to control other salt-minions.

## Values

| Key                                                                           | Type   | Default                                    | Description |
|-------------------------------------------------------------------------------|--------|--------------------------------------------|-------------|
| fullnameOverride                                                              | string | `""`                                       |             |
| master.affinity                                                               | object | `{}`                                       |             |
| master.config.ext_pillar.git[0].branch                                        | string | `"master"`                                 |             |
| master.config.ext_pillar.git[0].remote                                        | string | `"https://github.com/mazzy89/archnux.git"` |             |
| master.config.ext_pillar.git[0].root                                          | string | `"saltstack/pillar"`                       |             |
| master.config.gitfs_remotes[0]                                                | string | `"https://github.com/mazzy89/archnux.git"` |             |
| master.config.gitfs_root                                                      | string | `"saltstack/salt"`                         |             |
| master.config.log_level                                                       | string | `"info"`                                   |             |
| master.fullnameOverride                                                       | string | `""`                                       |             |
| master.image.pullPolicy                                                       | string | `"IfNotPresent"`                           |             |
| master.image.repository                                                       | string | `"docker.io/mazzy/salt"`                   |             |
| master.image.tag                                                              | string | `"3004-alpine3.14"`                        |             |
| master.imagePullSecrets                                                       | list   | `[]`                                       |             |
| master.ingress.annotations."traefik.ingress.kubernetes.io/router.entrypoints" | string | `"web"`                                    |             |
| master.ingress.className                                                      | string | `""`                                       |             |
| master.ingress.enabled                                                        | string | `"enabled"`                                |             |
| master.ingress.hosts[0].host                                                  | string | `"saltstack-api.hzk8s.k3s.mazzarino.cz"`   |             |
| master.ingress.hosts[0].paths[0].path                                         | string | `"/"`                                      |             |
| master.ingress.hosts[0].paths[0].pathType                                     | string | `"ImplementationSpecific"`                 |             |
| master.ingress.tls                                                            | list   | `[]`                                       |             |
| master.name                                                                   | string | `"master"`                                 |             |
| master.nameOverride                                                           | string | `""`                                       |             |
| master.nodeSelector                                                           | object | `{}`                                       |             |
| master.persistence.accessMode                                                 | string | `"ReadWriteOnce"`                          |             |
| master.persistence.annotations                                                | object | `{}`                                       |             |
| master.persistence.enabled                                                    | string | `"enabled"`                                |             |
| master.persistence.name                                                       | string | `"pki"`                                    |             |
| master.persistence.path                                                       | string | `"/etc/salt/pki"`                          |             |
| master.persistence.size                                                       | string | `"60Mi"`                                   |             |
| master.podAnnotations                                                         | object | `{}`                                       |             |
| master.podSecurityContext                                                     | object | `{}`                                       |             |
| master.replicaCount                                                           | int    | `1`                                        |             |
| master.resources                                                              | object | `{}`                                       |             |
| master.securityContext                                                        | object | `{}`                                       |             |
| master.serviceAccount.annotations                                             | object | `{}`                                       |             |
| master.serviceAccount.create                                                  | bool   | `true`                                     |             |
| master.serviceAccount.name                                                    | string | `""`                                       |             |
| master.services.api.annotations                                               | object | `{}`                                       |             |
| master.services.api.port                                                      | int    | `8000`                                     |             |
| master.services.api.type                                                      | string | `"ClusterIP"`                              |             |
| master.services.salt.annotations                                              | object | `{}`                                       |             |
| master.services.salt.type                                                     | string | `"LoadBalancer"`                           |             |
| master.tolerations                                                            | list   | `[]`                                       |             |
| nameOverride                                                                  | string | `""`                                       |             |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.7.0](https://github.com/norwoodj/helm-docs/releases/v1.7.0)
