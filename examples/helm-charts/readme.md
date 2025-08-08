Demo of uds overrides merging

```
modified values.yaml to include: 

podAnnotations:
  foo: bar

uds bundle overrides:
  podAnnotations:
    hello: world
    doug: was-here

```

commands:

1. zarf package create -a amd64
2. uds create --architecture amd64
3. uds deploy uds-bundle-helm-charts-amd64-0.0.1.tar.zst -a amd64
