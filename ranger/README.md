
Apache-ranger
===========

A Helm chart for Apache Ranger Admin and Usersync


## Configuration

The following table lists the configurable parameters of the Apache-ranger chart and their default values.

| Parameter                | Description             | Default        |
| ------------------------ | ----------------------- | -------------- |
| `rangerAdmin.image.repository` | docker image repository for Ranger Admin | `"897528479702.dkr.ecr.ap-southeast-1.amazonaws.com/eda-ranger"` |
| `rangerAdmin.image.tag` | docker image tag for Ranger Admin | `"latest"` |
| `rangerAdmin.image.pullPolicy` | Kubernetes image policy for Ranger Admin | `"IfNotPresent"` |
| `rangerAdmin.installPropertiesPath` | `install.properties` file path for Ranger Admin | `"/opt/ranger/admin/install.properties"` |
| `rangerAdmin.installPropertiesSecret` | secret to use for `install.properties` file in Ranger Admin | `""` |
| `rangerAdmin.resources` | resource limits and requests for Ranger Admin | `{}` |
| `rangerAdmin.env` | environment variables to be use for Ranger Admin | `[]` |
| `rangerAdmin.envFrom` | environment variables derived from secrets or configmap to be use for Ranger Admin | `[]` |
| `rangerAdmin.nodeSelector` | node selector for Ranger Admin | `{}` |
| `rangerAdmin.tolerations` | tolerations for Ranger Admin | `[]` |
| `rangerAdmin.affinity` | affinity for Ranger Admin | `{}` |
| `rangerAdmin.annotations` | annotations for Ranger Admin | `{}` |
| `rangerAdmin.securityContext.runAsUser` | docker user code for Ranger Admin | `0` |
| `rangerAdmin.securityContext.runAsGroup` | docker user group for Ranger admin | `0` |
| `rangerUsersync.enabled` | enable Ranger Usersync | `false` |
| `rangerUsersync.image.repository` | docker image repository for Ranger Usersync | `"897528479702.dkr.ecr.ap-southeast-1.amazonaws.com/eda-ranger-usersync"` |
| `rangerUsersync.image.tag` | docker image tag for Ranger Usersync | `"latest"` |
| `rangerUsersync.image.pullPolicy` | docker image tag for Ranger Usersync | `"IfNotPresent"` |
| `rangerUsersync.installPropertiesPath` | resource limits and requests for Ranger Usersync | `"/opt/ranger/usersync/install.properties"` |
| `rangerUsersync.installPropertiesSecret` | secret to use for `install.properties` file in Ranger Usersync | `""` |
| `rangerUsersync.resources` | resource limits and requests for Ranger Usersync | `{}` |
| `rangerUsersync.env` | environment variables to be use for Ranger Usersync | `[]` |
| `rangerUsersync.envFrom` | environment variables derived from secrets or configmap to be use for Ranger Usersync | `[]` |
| `rangerUsersync.nodeSelector` | node selector for Ranger Usersync | `{}` |
| `rangerUsersync.tolerations` | tolerations for Ranger Usersync | `[]` |
| `rangerUsersync.affinity` | affinity for Ranger Usersync | `{}` |
| `rangerUsersync.annotations` | annotations for Ranger Usersync | `{}` |
| `rangerAuthorizationMatrix.enabled` | enable Ranger Authorization Matrix | `false` |
| `rangerAuthorizationMatrix.image.repository` | docker image repository for Ranger Authrorization Matrix | `"897528479702.dkr.ecr.ap-southeast-1.amazonaws.com/eda-ranger-authorization-matrix"` |
| `rangerAuthorizationMatrix.image.tag` | docker image tag for Ranger Authrorization Matrix | `"latest"` |
| `rangerAuthorizationMatrix.image.pullPolicy` | docker image tag for Ranger Authrorization Matrix | `"IfNotPresent"` |
| `rangerAuthorizationMatrix.nodeSelector` | node selector for Ranger Authrorization Matrix | `{}` |
| `rangerAuthorizationMatrix.tolerations` | tolerations for Ranger Authrorization Matrix | `[]` |
| `rangerAuthorizationMatrix.affinity` | affinity for Ranger Authrorization Matrix | `{}` |
| `rangerAuthorizationMatrix.annotations` | annotations for Ranger Authrorization Matrix | `{}` |
| `rangerAuthorizationMatrix.startupProbe.httpGet.path` |  | `"/health"` |
| `rangerAuthorizationMatrix.startupProbe.httpGet.port` |  | `"http"` |
| `rangerAuthorizationMatrix.startupProbe.initialDelaySeconds` |  | `15` |
| `rangerAuthorizationMatrix.startupProbe.timeoutSeconds` |  | `1` |
| `rangerAuthorizationMatrix.startupProbe.failureThreshold` |  | `60` |
| `rangerAuthorizationMatrix.startupProbe.periodSeconds` |  | `5` |
| `rangerAuthorizationMatrix.startupProbe.successThreshold` |  | `1` |
| `rangerAuthorizationMatrix.livenessProbe.httpGet.path` |  | `"/health"` |
| `rangerAuthorizationMatrix.livenessProbe.httpGet.port` |  | `"http"` |
| `rangerAuthorizationMatrix.livenessProbe.initialDelaySeconds` |  | `15` |
| `rangerAuthorizationMatrix.livenessProbe.timeoutSeconds` |  | `1` |
| `rangerAuthorizationMatrix.livenessProbe.failureThreshold` |  | `3` |
| `rangerAuthorizationMatrix.livenessProbe.periodSeconds` |  | `15` |
| `rangerAuthorizationMatrix.livenessProbe.successThreshold` |  | `1` |
| `rangerAuthorizationMatrix.readinessProbe.httpGet.path` |  | `"/health"` |
| `rangerAuthorizationMatrix.readinessProbe.httpGet.port` |  | `"http"` |
| `rangerAuthorizationMatrix.readinessProbe.initialDelaySeconds` |  | `15` |
| `rangerAuthorizationMatrix.readinessProbe.timeoutSeconds` |  | `1` |
| `rangerAuthorizationMatrix.readinessProbe.failureThreshold` |  | `3` |
| `rangerAuthorizationMatrix.readinessProbe.periodSeconds` |  | `15` |
| `rangerAuthorizationMatrix.readinessProbe.successThreshold` |  | `1` |
| `service.rangerAdmin.type` | Ranger Admin service type, could be `ClusterIP`, `LoadBalancer`, `NodePort` | `"ClusterIP"` |
| `service.rangerAdmin.port` | Ranger Admin port to be served | `6080` |
| `service.rangerAdmin.annotations` | Ranger Admin annotations for service | `{}` |
| `service.rangerAuthorizationMatrix.type` | Ranger Authorization Matrix service type, could be `ClusterIP`, `LoadBalancer`, `NodePort` | `"ClusterIP"` |
| `service.rangerAuthorizationMatrix.port` | Ranger Authorization Matrix port to be served | `8080` |
| `service.rangerAuthorizationMatrix.annotations` | Ranger Authorization Matrix annotations for service | `{}` |
| `ingress.enabled` | enable the ingress | `false` |
| `ingress.className` | ingress classname, could be `alb` | `"alb"` |
| `ingress.annotations` | ingress annotation | `{}` |
| `ingress.rangerAdmin.hosts` | hostnames for ingresses and which service paths they should map to | `[]` |
| `ingress.rangerAdmin.tls` | TLS secrets and which hosts they should be used for | `[]` |
| `ingress.rangerAuthorizationMatrix.hosts` | hostnames for ingresses and which service paths they should map to | `[]` |
| `ingress.rangerAuthorizationMatrix.tls` | TLS secrets and which hosts they should be used for | `[]` |



---
_Documentation generated by [Frigate](https://frigate.readthedocs.io)._

