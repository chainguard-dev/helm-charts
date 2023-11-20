# enforce-agent

<!-- This README.md is generated. Please edit README.md.gotmpl -->

![Version: 0.0.91](https://img.shields.io/badge/Version-0.0.91-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v0.1.197](https://img.shields.io/badge/AppVersion-v0.1.197-informational?style=flat-square)

A helm chart for Chainguard's Enforce Agent.

Documentation for the chart can be found [here](https://edu.chainguard.dev/chainguard/chainguard-enforce/chainguard-enforce-kubernetes/alternative-installation-methods/).

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
| auth.gcp.serviceAccount.email | string | `""` | Email of the GCP Service Account. |
| auth.gcp.serviceAccount.key | string | `""` | The GCP Service Account key.json base64 encoded. This can be generated with: `gcloud iam service-accounts keys create key.json --iam-account=$NAME@@PROJECT.iam.gserviceaccount.com`. |
| clusterName | string | `""` |  |
| enforcerOptions.enableCIPCache | bool | `false` |  |
| enforcerOptions.namespaceEnforcementMode | string | `"opt-in"` |  |
| enforcerOptions.noMatchPolicy | string | `"deny"` |  |
| enforcerOptions.webhookFailOpen | bool | `false` |  |
| inviteCode | string | `""` | Invite code assigned to group where clusters will be registered. This can be generated with: `chainctl iam invite create $GROUP --cluster -ojson | jq -r .code` |
