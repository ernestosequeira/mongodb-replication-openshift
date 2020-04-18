# MongoDB - Replication
Mongodb 3.2 on openshift 3.11


# 1. Secrets


### Prepare the enviroment for Openshift, create the secrets

```sh
Example:
Name                      Value
==========================================
MONGODB_USER              user01
MONGODB_PASSWORD          password01
MONGODB_DATABASE          sampledb
MONGODB_ADMIN_PASSWORD    admin
MONGODB_REPLICA_NAME      rs0
MONGODB_KEYFILE_VALUE     xxxxx
MONGODB_SERVICE_NAME      mongodb-internal

```

### Deployment MongoDB

```
$ oc login https://openshift.example.com:443 --token={xxxxxxxxxx}
mkdir -p /home/usuario/mongodb
cd /home/usuario/mongodb
git clone https://github.com/ernestosequeira/mongodb-replication-openshift.git
oc new-app -f mongodb-cluster.yaml
```


