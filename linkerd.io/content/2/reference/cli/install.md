+++
date = "2019-02-17T12:00:00-07:00"
title = "install"
+++

The `linkerd install` command outputs the YAML configs necessary to install
Linkerd in your [Kubernetes](https://kubernetes.io) cluster.

## Usage

You can pipe the output of the `install` command to
[kubectl](https://kubernetes.io/docs/reference/kubectl/kubectl/) to install
Linkerd directly:

```bash
linkerd install | kubectl apply -f -
```

You can customize the installation using the [CLI flags](#flags) listed below.

### Output to file

You can also output the Linkred config to a file to be used later (and perhaps
committed to version control):

```bash
linkerd install > linkerd.yaml
```

## Tutorial

For a full installation tutorial, see [Installing Linkerd](/2/tasks/install/).

{{< cli/flags "install" >}}
