```yaml
apiVersion: app.redislabs.com/v1
kind: RedisEnterpriseCluster
metadata:
  name: rec
  labels:
    app: redis-enterprise
spec:
  # Add fields here
  nodes: 3
  redisEnterpriseImageSpec:
    repository: registry.connect.redhat.com/redislabs/redis-enterprise
    versionTag: 7.8.4-66.rhel8-openshift
  redisEnterpriseServicesRiggerImageSpec:
    repository: registry.connect.redhat.com/redislabs/services-manager
  bootstrapperImageSpec:
    repository: registry.connect.redhat.com/redislabs/redis-enterprise-operator
```
