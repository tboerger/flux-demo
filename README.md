# flux-demo

This repository is used for demonstration of my talk about Flux CD.

## Cluster

```console
kind create cluster \
    --name flux-demo
```

## Flux CD

```console
flux bootstrap github \
    --author-email=thomas@webhippie.de \
    --author-name="Thomas Boerger" \
    --owner=tboerger \
    --repository=flux-demo \
    --branch=master \
    --personal=true \
    --private=false \
    --read-write-key=true \
    --path clusters/dev \
    --components-extra=image-reflector-controller,image-automation-controller
```

## Cleanup

```console
kind delete cluster \
    --name flux-demo
```

## Authors

-   [Thomas Boerger](https://github.com/tboerger)

## License

Apache-2.0

## Copyright

```console
Copyright (c) 2025 Thomas Boerger <thomas@webhippie.de>
```
