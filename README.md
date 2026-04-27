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

## Renovate documentation resources

* [Shareable config preset](https://docs.renovatebot.com/config-presets/)
* [Key concepts - Presets](https://docs.renovatebot.com/key-concepts/presets/)
