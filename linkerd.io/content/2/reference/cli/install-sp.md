+++
date = "2019-02-17T12:00:00-07:00"
title = "install-sp"
+++

The `linkerd install-sp` command outputs [Kubernetes](https://kubernetes.io)
configs for installing [Linkerd service profiles](/2/features/service-profiles)
into the Linkerd [control plane](/2/reference/architecture/#control-plane).

In order to use `linkerd install-sp` you'll need to have a cluster-wide Linkerd
control plane installed.

{{< note >}}
To confirm that service profiles are supported, verify that the output of
`kubectl api-versions` includes `linkerd.io/v1alpha1`.
{{< /note >}}

## Usage

To install Linkerd service profiles in your Kubernetes cluster:

```bash
linkerd install-sp | kubectl apply -f -
```

### Uninstalling service profiles

To uninstall, use `kubectl delete`:

```bash
linkerd install-sp | kubectl delete -f -
```
