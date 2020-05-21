# workstation-management
## SAL Reporting console
---

[SAL](https://github.com/salopensource/sal) Sal is a multi-tenanted reporting dashboard for Munki with the ability to display information from Facter. It has a plugin system allowing you to easily build widgets to display your custom information from Facter or Munki's conditional items (or both!).

With Sal, you are able to allow access to reports on certain sets of machines to certain people - for example, giving a manager access to the reports on the machines in their department.

Sal also features powerful search capabilities and application inventory and support for Munki's license tracking.

## TL;DR;

```console
$ helm install sal
```

## Prerequisites

- Kubernetes 1.8+
- PV provisioner support in the underlying infrastructure
- Install a postgres database via a chart:     
```bash
$ helm install --namespace wksmgmt --name sal-postgresql \
  --set postgresUser=saldbuser,postgresPassword=someAwesomePassword,postgresDatabase=saldb postgresql
```

## Installing the Chart

To install the chart with the release name `sal`:

```console
$ helm install --namespace wksmgmt --name sal sal
```

> **Tip**: List all releases using `helm list`

## Uninstalling the Chart

To uninstall/delete the `sal` deployment:

```console
$ helm delete sal --purge;
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

---
