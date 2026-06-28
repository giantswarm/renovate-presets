# Renovate presets for Giant Swarm

A collection of custom Renovate config presets to be used by Giant Swarm repos.

Updates made to these configs will automatically and immediately be made available to all repos that are referencing them. No changes in the individual repos is required as long as they have the reference set up in the `extends` property.

## Usage

To make use of these preset you need to add them to your `extends` array within your repos `renovate.json5`. ([Why JSON5?](https://json5.org/))

Multiple presets can be specified and they build on top of each other.

### Minimal example

```json5
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": [
    "github>giantswarm/renovate-presets:default.json5",
  ],
}
```

### Language specific example

```json5
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": [
    "github>giantswarm/renovate-presets:default.json5",
    "github>giantswarm/renovate-presets:lang-go.json5",
  ],
}
```

## Available presets

| Preset | Purpose |
|--------|---------|
| `default.json5` | Base config for all repos. Includes semantic commits, labels, dependency dashboard, ignorePaths/ignoreDeps, architect-orb automerge, CAPI release datasources, `repo:`/`registry:` regex managers for YAML/Dockerfile/Makefiles, vendir manager, and npm/vendir PR policies. |
| `lang-go.json5` | Go-specific additions: groups k8s/CAPI/AWS SDK/test modules, `gomodTidy`, `gomodUpdateImportPaths`. Extends `default.json5`. |
| `lang-python.json5` | Python-specific additions: automerge patch/pin/digest, 14-day PyPI release age delay. Extends `default.json5`. |
| `flux.json5` | Enables the Flux manager for `gotk-components.yaml` files. |
| `customer-management-clusters.json5` | Base config for customer management-cluster GitOps repos. Extends `default.json5` with a weekly Thursday schedule. |
| `deprecated.json5` | Deprecated / low-maintenance repos: disables all routine updates (major/minor/patch/pin/digest/bump) and keeps only security/vulnerability remediation. Extend in addition to `default.json5`. Applied automatically to repos marked `lifecycle: deprecated` with `gen.ci.generate` in `giantswarm/github`. |
| `disable-ansible.json5` | Disables the Ansible manager. |
| `disable-helm-values.json5` | Disables the helm-values manager. |
| `disable-helmv3.json5` | Disables the helmv3 manager. |
| `disable-kustomize.json5` | Disables the kustomize manager. |
| `disable-upstream-charts.json5` | Disables updates for vendored charts under `helm/*/charts/`. |
| `disable-vendir.json5` | Disables the vendir manager. |
| `tests-e2e-app.json5` | Adds `/run app-test-suites` trigger note to PR bodies. |
| `tests-e2e-app-cabbage.json5` | Like `tests-e2e-app` with additional ignores for Cilium/Envoy-Gateway synced paths. |

> **vendir support:** `default.json5` includes a built-in vendir `customManager`. Repos with annotated `vendir.yml` files get automatic version tracking without any extra preset. Annotate each synced ref with:
> ```yaml
> # renovate: datasource=github-releases depName=org/repo
>   ref: v1.2.3
> ```

## Renovate documentation resources

* [Shareable config preset](https://docs.renovatebot.com/config-presets/)
* [Key concepts - Presets](https://docs.renovatebot.com/key-concepts/presets/)
