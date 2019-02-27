+++
date = "2019-02-17T12:00:00-07:00"
title = "endpoints"
+++

The `linkerd endpoints` command provides debug information about the internal
state of the [control plane](/2/reference/architecture/#control-plane)'s
destination container.

{{< note >}}
This cache of service discovery information is populated on-demand via
[Linkerd proxy](/2/reference/architecture/#proxy) requests. This command will return
`No endpoints found.` until a Linkerd proxy begins routing requests.
{{< /note >}}

## Usage

To get all endpoints:

```bash
linkerd endpoints
```

To get the endpoints in a specific Kubernetes namespace:

```bash
linkerd endpoint -n emojivoto
```

To output endpoints as JSON:

```bash
linkerd endpoints -o json
```

{{< cli/flags "endpoints" >}}
