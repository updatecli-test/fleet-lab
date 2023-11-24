# fleet-lab
Rancher Fleet laboratory

## To Install Fleet

First install the Fleet CustomResourcesDefintions.

```
helm -n cattle-fleet-system install --create-namespace --wait \
    fleet-crd https://github.com/rancher/fleet/releases/download/v0.3.11/fleet-crd-0.3.11.tgz
```

Second install the Fleet controllers.

```
helm -n cattle-fleet-system install --create-namespace --wait \
    fleet https://github.com/rancher/fleet/releases/download/v0.3.11/fleet-0.3.11.tgz
```


Third install the gitjob resource

```
kubectl apply -f gitrepo.yaml 
```
