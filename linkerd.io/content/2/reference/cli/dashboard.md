+++
date = "2019-02-17T12:00:00-07:00"
title = "dashboard"
+++

The `linkerd dashboard` command enables you to access the Linkerd
[dashboard](/2/reference/architecture/#dashboard) via the CLI.

To open the dashboard in your browser:

```bash
linkerd dashboard
```

To specify a port:

```bash
linkerd dashboard -p 9999
```

{{< note >}}
You can also run the dashboard process in the background:

```bash
linkerd dashboard &
```
{{< /note >}}

{{< cli/flags "dashboard" >}}
