# workstation-management    
## Munki

[Munki](https://www.munki.org/) Munki is a set of tools that, used together with a webserver-based repository of packages and package metadata, can be used by OS X administrators to manage software installs (and in many cases removals) on OS X client machines.

Munki can install software packaged in the Apple package format, and also supports Adobe CS3/CS4/CS5/CS6 Enterprise Deployment "packages", and drag-and-drop disk images as installer sources.

Additionally, Munki can be configured to install Apple Software Updates, either from Apple's server, or yours.

Munki is currently in use at organizations all over the world, managing software for tens of thousands of Macs.

## TL;DR;

```console
$ helm install munki
```

## Introduction

This chart bootstraps a [Munki](https://www.munki.org/) macOS Fleet package management deployment on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

## Prerequisites

- Kubernetes 1.4+ with Beta APIs enabled
- PV provisioner support in the underlying infrastructure

## Installing the Chart

To install the chart with the release name `munki`:

```console
$ helm install --namespace wksmgmt --name munki munki
```

> **Tip**: List all releases using `helm list`

## Uninstalling the Chart

To uninstall/delete the `munki` deployment:

```console
$ helm delete munki --purge;
```

The command removes all the Kubernetes components associated with the chart and deletes the release.
