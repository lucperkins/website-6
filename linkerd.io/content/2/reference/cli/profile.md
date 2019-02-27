+++
date = "2019-02-17T12:00:00-07:00"
title = "profile"
+++

[Service profiles](/2/features/service-profiles/) are Kubernetes custom resource
definitions
([CRD](https://kubernetes.io/docs/concepts/extend-kubernetes/api-extension/custom-resources/)s)
that can provide Linkerd additional information about a service. The `linkerd
profile` outputs service profile configurations for [Kubernetes](https://kubernetes.io)
services.

## Usage

Output a basic template to apply after modification:

```bash
linkerd profile -n emojivoto --template web-scv
```

Generate a profile from an [OpenAPI](https://www.openapis.org/) specification:

```bash
linkerd profile -n emojivoto --open-api web-svc.swagger web-svc
```

Generate a profile from a [Protocol Buffers](https://developers.google.com/protocol-buffers/)
definition:

```bash
linkerd profile -n emojivoto --proto Voting.proto vote-svc
```

Generate a profile by watching live traffic based off of tap data:

```bash
linkerd profile -n emojivoto web-svc --tap deploy/web --tap-duration 10s --tap-route-limit 5
```

{{< cli/flags "profile" >}}
