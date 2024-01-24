
Trino
===========

Fast distributed SQL query engine for big data analytics that helps you explore your data universe


## Configuration

The following table lists the configurable parameters of the Trino chart and their default values.

| Parameter                | Description             | Default        |
| ------------------------ | ----------------------- | -------------- |
| `image.repository` |  | `"897528479702.dkr.ecr.ap-southeast-1.amazonaws.com/eda-trino"` |
| `image.pullPolicy` |  | `"IfNotPresent"` |
| `image.tag` |  | `426` |
| `imagePullSecrets` |  | `[{"name": "registry-credentials"}]` |
| `server.workers` |  | `2` |
| `server.node.environment` |  | `"production"` |
| `server.node.dataDir` |  | `"/data/trino"` |
| `server.node.pluginDir` |  | `"/usr/lib/trino/plugin"` |
| `server.log.trino.level` |  | `"INFO"` |
| `server.config.path` |  | `"/etc/trino"` |
| `server.config.http.port` |  | `8080` |
| `server.config.https.enabled` |  | `false` |
| `server.config.https.port` |  | `8443` |
| `server.config.https.keystore.path` |  | `""` |
| `server.config.authenticationType` |  | `""` |
| `server.config.query.maxMemory` |  | `"4GB"` |
| `server.exchangeManager.name` |  | `"filesystem"` |
| `server.exchangeManager.baseDir` |  | `"/tmp/trino-local-file-system-exchange-manager"` |
| `server.workerExtraConfig` |  | `""` |
| `server.coordinatorExtraConfig` |  | `""` |
| `server.autoscaling.enabled` |  | `false` |
| `server.autoscaling.maxReplicas` |  | `5` |
| `server.autoscaling.targetCPUUtilizationPercentage` |  | `50` |
| `server.catalogSecret` |  | `""` |
| `server.keda.enabled` |  | `false` |
| `server.keda.pollingInterval` |  | `30` |
| `server.keda.cooldownPeriod` |  | `30` |
| `server.keda.minReplicaCount` |  | `2` |
| `server.keda.maxReplicaCount` |  | `5` |
| `server.keda.serverAddress` |  | `""` |
| `server.keda.metricName` |  | `"metric_01"` |
| `server.keda.query` |  | `""` |
| `server.keda.threshold` |  | `"1"` |
| `server.keda.advanced` |  | `{}` |
| `accessControl` |  | `{}` |
| `additionalNodeProperties` |  | `{}` |
| `additionalConfigProperties` |  | `{}` |
| `additionalLogProperties` |  | `{}` |
| `additionalExchangeManagerProperties` |  | `{}` |
| `eventListenerProperties` |  | `{}` |
| `env` |  | `[]` |
| `envFrom` |  | `[]` |
| `initContainers` |  | `{}` |
| `sidecarContainers` |  | `{}` |
| `securityContext.runAsUser` |  | `1000` |
| `securityContext.runAsGroup` |  | `1000` |
| `shareProcessNamespace.coordinator` |  | `false` |
| `shareProcessNamespace.worker` |  | `false` |
| `service.type` |  | `"ClusterIP"` |
| `service.port` |  | `8080` |
| `service.annotations` |  | `{}` |
| `auth` |  | `{}` |
| `serviceAccount.create` |  | `false` |
| `serviceAccount.name` |  | `""` |
| `serviceAccount.annotations` |  | `{}` |
| `secretMounts` |  | `[]` |
| `coordinator.jvm.maxHeapSize` |  | `"8G"` |
| `coordinator.jvm.gcMethod.type` |  | `"UseG1GC"` |
| `coordinator.jvm.gcMethod.g1.heapRegionSize` |  | `"32M"` |
| `coordinator.config.memory.heapHeadroomPerNode` |  | `""` |
| `coordinator.config.query.maxMemoryPerNode` |  | `"1GB"` |
| `coordinator.additionalJVMConfig` |  | `{}` |
| `coordinator.additionalExposedPorts` |  | `{}` |
| `coordinator.resources` |  | `{}` |
| `coordinator.livenessProbe` |  | `{}` |
| `coordinator.readinessProbe` |  | `{}` |
| `coordinator.nodeSelector` |  | `{}` |
| `coordinator.tolerations` |  | `[]` |
| `coordinator.affinity` |  | `{}` |
| `coordinator.additionalConfigFiles` |  | `{}` |
| `coordinator.annotations` |  | `{}` |
| `coordinator.labels` |  | `{}` |
| `coordinator.secretMounts` |  | `[]` |
| `worker.jvm.maxHeapSize` |  | `"8G"` |
| `worker.jvm.gcMethod.type` |  | `"UseG1GC"` |
| `worker.jvm.gcMethod.g1.heapRegionSize` |  | `"32M"` |
| `worker.config.memory.heapHeadroomPerNode` |  | `""` |
| `worker.config.query.maxMemoryPerNode` |  | `"1GB"` |
| `worker.additionalJVMConfig` |  | `{}` |
| `worker.additionalExposedPorts` |  | `{}` |
| `worker.resources` |  | `{}` |
| `worker.livenessProbe` |  | `{}` |
| `worker.readinessProbe` |  | `{}` |
| `worker.nodeSelector` |  | `{}` |
| `worker.tolerations` |  | `[]` |
| `worker.affinity` |  | `{}` |
| `worker.additionalConfigFiles` |  | `{}` |
| `worker.annotations` |  | `{}` |
| `worker.labels` |  | `{}` |
| `worker.secretMounts` |  | `[]` |
| `worker.resourceGroups.enabled` |  | `false` |
| `worker.resourceGroups.mountPath` |  | `""` |
| `worker.resourceGroups.secretName` |  | `""` |
| `worker.gracefulShutdown.enabled` |  | `false` |
| `worker.gracefulShutdown.terminationGracePeriodSeconds` |  | `600` |
| `kafka.mountPath` |  | `"/etc/trino/schemas"` |
| `kafka.tableDescriptions` |  | `{}` |
| `commonLabels` | Labels that get applied to every resource's metadata | `{}` |
| `ingress.enabled` |  | `false` |
| `ingress.className` |  | `""` |
| `ingress.annotations` |  | `{}` |
| `ingress.hosts` |  | `[]` |
| `ingress.tls` |  | `[]` |
| `cache.enabled` |  | `false` |
| `cache.labels.enabled` |  | `false` |
| `cache.annotations` |  | `{}` |
| `cache.accessModes` |  | `["ReadWriteOnce"]` |
| `cache.size` |  | `"100Gi"` |
| `cache.storageClassName` |  | `""` |
| `cache.path` |  | `""` |
| `spillToDisk.enabled` |  | `false` |
| `spillToDisk.labels.enabled` |  | `false` |
| `spillToDisk.annotations` |  | `{}` |
| `spillToDisk.accessModes` |  | `["ReadWriteOnce"]` |
| `spillToDisk.size` |  | `"100Gi"` |
| `spillToDisk.storageClassName` |  | `""` |
| `spillToDisk.path` |  | `""` |
| `persistDataDir.enabled` |  | `false` |
| `persistDataDir.labels.enabled` |  | `false` |
| `persistDataDir.annotations` |  | `{}` |
| `persistDataDir.accessModes` |  | `["ReadWriteOnce"]` |
| `persistDataDir.size` |  | `"1Gi"` |
| `persistDataDir.storageClassName` |  | `""` |
| `rangerGroupSync.enabled` |  | `false` |
| `rangerGroupSync.image.repository` |  | `"897528479702.dkr.ecr.ap-southeast-1.amazonaws.com/eda-ranger-groupsync"` |
| `rangerGroupSync.image.pullPolicy` |  | `"IfNotPresent"` |
| `rangerGroupSync.image.tag` |  | `"latest"` |
| `rangerGroupSync.mountPath` |  | `"/mnt/ranger-group"` |
| `rangerGroupSync.env` |  | `[]` |
| `rangerGroupSync.envFrom` |  | `[]` |
| `rangerGroupSync.refreshPeriod` |  | `"5s"` |
| `rangerGroupSync.resources` |  | `{}` |
| `jmxExporter.coordinator.enabled` |  | `false` |
| `jmxExporter.worker.enabled` |  | `false` |
| `jmxExporter.port` |  | `9933` |
| `jmxExporter.config` |  | `"rules:\n  - pattern: \"trino.execution<name=QueryManager>\"\n  - pattern: \"trino.execution<name=SqlTaskManager>\"\n  - pattern: \"trino.memory.*\"\n  - pattern: \"java.lang.*\"\n"` |
| `jmxExporter.serviceMonitor.enabled` |  | `false` |
| `jmxExporter.serviceMonitor.port` |  | `"jmx-exporter"` |
| `jmxExporter.serviceMonitor.additionalLabels` |  | `{}` |
| `jmxExporter.serviceMonitor.interval` |  | `"1m"` |
| `jmxExporter.serviceMonitor.scrapeTimeout` |  | `"10s"` |
| `jmxExporter.serviceMonitor.path` |  | `"/metrics"` |



---
_Documentation generated by [Frigate](https://frigate.readthedocs.io)._

