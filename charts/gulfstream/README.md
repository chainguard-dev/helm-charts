# gulfstream

<!-- This README.md is generated. Please edit README.md.gotmpl -->

![Version: 0.0.1](https://img.shields.io/badge/Version-0.0.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.0.1](https://img.shields.io/badge/AppVersion-0.0.1-informational?style=flat-square)

A helm chart for Chainguard's Gulfstream

**Homepage:** <https://chainguard.dev>

## Quick Installation

To install the helm chart with default values run following command.
The [Values](#Values) section describes the configuration options for this chart.

```shell
helm install [RELEASE_NAME] .
```

## Uninstallation

To uninstall the Helm chart run following command.

```shell
helm uninstall [RELEASE_NAME]
```

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| The Chainguard Team |  | <https://chainguard.dev> |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| chainctl.image.repo | string | `"us.gcr.io/prod-enforce-fabc/chainctl"` |  |
| chainctl.image.version | string | `"sha256:ac373eed9e440b7f00b13cff3d917f8fc4276ca6c8ea6ec842e2408e5b3a1c05"` |  |
| controller.image.repo | string | `"us.gcr.io/prod-enforce-fabc/controlplane"` |  |
| controller.image.version | string | `"sha256:f9760265d67616451fa979d25e4c447bf9e0ba728bbdf6b0409ced34c6514d25"` |  |
| inviteCode | string | `"changeme"` |  |
