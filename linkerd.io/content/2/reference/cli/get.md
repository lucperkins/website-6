+++
date = "2019-02-17T12:00:00-07:00"
title = "get"
+++

The `linkerd get` command displays one or many mesh resources. Currently, only
[Pod](https://kubernetes.io/docs/concepts/workloads/pods/pod/) resources are
supported (designated by `pods` or `po`).

## Usage

To get all Linkerd-supported Pods:

```bash
linkerd get pods

# Also valid:
linkerd get po
```

To get all Linkerd-supported Pods in a specific namespace:

```bash
linkerd get pods --namespace linkerd
```

{{< cli/flags "get" >}}
