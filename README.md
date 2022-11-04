# Helm Charts

[Helm](https://helm.sh) charts for [Chainguard](https://chainguard.dev) products.

## Usage

Charts are available in the following formats:

* [Chart Repository](https://helm.sh/docs/topics/chart_repository/)

### Installing from the Chart Repository

The following command can be used to add the chart repository:

```shell
helm repo add chainguard https://chainguard-dev.github.io/helm-charts
helm repo update
```

Once the chart repository has been added, install one of the available charts:

```shell
helm upgrade -i <release_name> chainguard/<chart_name>
```

## Provenance

Charts are signed using the [provenance methods provided by the Helm project](https://helm.sh/docs/topics/provenance/)
as well as uploaded to the [Rekor transparency server](https://github.com/sigstore/rekor)
using the [Helm sigstore plugin](https://github.com/sigstore/helm-sigstore).

Verification of the signed charts can be accomplished by importing the GPG
Public Key that was used to sign the associated chart.

```shell
cat security/pubkey.gpg | gpg --import --batch
```

Once the public key has been imported, charts can be verified using the
`helm verify` and/or `helm tekton verify` commands.

> Note: The public key that was used to sign a particular chart may not be
identical to the public key on the `main` branch. Each chart release has an
associated git tag. The public key that was used to sign the particular chart
will be included in this tag.

## Charts

* [enforce-agent](charts/enforce-agent) - [docs](https://edu.chainguard.dev/chainguard/chainguard-enforce/chainguard-enforce-kubernetes/alternative-installation-methods/)

