# dwp-demo-connectors
Kafka Connectors for DWP demo cluster

```shell

flux create source git connectors \
    --url=https://github.com/sionsmith/dwp-demo-connectors \
    --branch=main

flux create kustomization connectors \
  --source=GitRepository/connectors \
  --path="./" \
  --prune=true \
  --interval=5m \
  --namespace=flux-system 
```