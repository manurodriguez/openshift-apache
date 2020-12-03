# Howto

Authenticate to OCP cluster

```bash
$ oc login --insecure-skip-tls-verify --username=YOUR_USER --password=YOUR_PASS https://YOUR_API:6443
Login successful.
```

Create namespace

```bash
$ oc -n apache-ns apply -f apache-namespace.yaml
namespace/apache-ns created
```

Create deployment

```bash
$ oc -n apache-ns apply -f apache-deployment.yaml 
deployment.apps/apache created
```

Create service

```bash
$ oc -n apache-ns apply -f apache-svc.yaml 
service/apache created
```

Create route

```bash
$ oc -n apache-ns apply -f apache-route.yaml 
route.route.openshift.io/apache created
```

Verify resources are running

```bash
oc get pods -n apache-ns
```


