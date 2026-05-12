# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
however this project does not use Semantic Versioning and there are no releases.
Instead this file uses a date-based structure.

## 2026-05-12

### Added

- Delay npm (JS/TS) dependency updates by 14 days after publication via `minimumReleaseAge`.

## 2026-05-08

### Added

- Configure conventional commits via `semanticCommits*`.

## 2026-05-05

### Changed

- Update `actions/add-to-project` action to v2 (#90).

## 2026-04-27

### Changed

- Convert configuration to JSON5.
- Update README.

## 2026-04-26

### Changed

- Update GitHub artifact actions (#89).
- Update `actions/setup-node` action to v6 (#88).
- Update `actions/checkout` action to v6 (#87).
- Update `actions/upload-artifact` action to v4.6.2 (#86).
- Update `actions/setup-node` action to v4.4.0 (#85).
- Update `actions/download-artifact` action to v4.3.0 (#84).
- Update `actions/checkout` action to v4.3.1 (#83).

## 2026-04-25

### Added

- Add `renovate.json` to manage this repository's own dependencies (#79).

### Changed

- Update `actions/add-to-project` action to v1.0.2 (#81).
- Update `actions-ecosystem/action-add-labels` digest to `18f1af5` (#80).

## 2026-04-23

### Changed

- Align files (#78).

## 2026-04-17

### Changed

- Align files (#77).

## 2026-04-16

### Added

- Add `upstream helm/*/charts/**` to `ignorePaths` (#75).

### Changed

- Align files (#74).

### Fixed

- Use `packageRules` instead of `ignorePaths` in `disable-upstream-charts` preset (#76).

## 2026-02-03

### Changed

- Align files (#72).

## 2026-01-09

### Changed

- Align files (#71).

## 2025-12-22

### Added

- Add Renovate preset to disable `helmv3` dependencies (#70).
- Add Renovate preset to disable `helm-values` dependencies (#69).

## 2025-12-11

### Changed

- Use `github-releases` datasource for cluster release changelogs, then decouple cluster releases from the GitHub datasource to fix tag inference (#68).

## 2025-11-13

### Added

- Add exclusion for Helm v4 (#67).

## 2025-11-07

### Added

- Add Renovate preset for customer management cluster repos (#66).

### Changed

- Align files (#65).

## 2025-10-07

### Removed

- Remove Flux resource version restrictions (#64).

## 2025-09-01

### Added

- Add custom config for Cabbage (#63).

### Changed

- Align files (#61).

## 2025-08-20

### Added

- Check `.sh` files for Regex manager updates (#62).

## 2025-06-26

### Removed

- Remove grouping (#60).

## 2025-06-18

### Added

- Add mocking delete `apiextensions` (#59).

## 2025-06-17

### Added

- Add schema annotation (#58).

## 2025-06-03

### Added

- Add `packageRule` for handling our own GitHub workflow updates (#57).

## 2025-05-15

### Added

- Enable auto-merge for `architect-orb` minor releases (#56).

## 2025-04-24

### Added

- Support quoted versions (#55).
- Support `shared-configs` YAML template format (#54).
- Support `cloudnativePG` image format (#52).

### Changed

- Move CloudNativePG image to the Docker source (#53).

## 2025-02-18

### Added

- Add more deps to those with `-gs` suffix releases (#50).
- Support dep with prerelease suffix (#49).

## 2025-02-11

### Changed

- Align files (#47).

## 2025-01-30

### Added

- Extend releases for `capa`, `capz` and include `capv` and `capvcd` (#48).

## 2024-10-14

### Changed

- Update `CODEOWNERS` (#46).

## 2024-10-10

### Added

- Enable automerge for all patch upgrades (#45).

## 2024-10-03

### Added

- Match `appVersion` (#44).

## 2024-09-27

### Changed

- Exclude Flux system manifests from Kubernetes manager (#42).

### Fixed

- Tweak regex (#43).

## 2024-09-06

### Added

- Add PR body notes for e2e app test suites (#41).

## 2024-08-29

### Changed

- Disable vendir manager (#40).

## 2024-08-28

### Added

- Add Renovate validation step.

### Changed

- Migrate config syntax (#39).
- Bump Node.js to v20.15.
- Pin action versions.
- Ignore `k8s.io/client-go` releases ending in `+incompatible` (#36).

### Fixed

- Fix regex syntax (#37).

## 2024-08-13

### Added

- Support replacing env values in pod specs (#35).

## 2024-07-26

### Added

- Support Tekton param default as just version (#34).

## 2024-07-19

### Added

- Include Makefile to `capa`/`capz` releases (#32).

### Fixed

- Fix Renovate (#33).

## 2024-07-17

### Changed

- Extend releases (#31).

## 2024-07-12

### Added

- Allow Renovate to fetch CAPA releases (#30).

## 2024-07-05

### Added

- Add `controller-runtime` to k8s modules group (#29).
- Group Team Tinkerers test framework modules (#28).

### Changed

- Update `lang-go.json5` (#4).

## 2024-06-13

### Added

- Manually set the URL for the releases SDK changelog (#27).

## 2024-06-06

### Added

- Add support for Dockerfile image repo regex updates (#25).

### Changed

- Exclude `operatorkit` v8 (#26).

## 2024-06-03

### Removed

- Remove grouping of `giantswarm` Go modules (#24).

## 2024-05-31

### Changed

- Switch from `matchPackage*` to `matchDep*` (#23).

## 2024-05-24

### Changed

- Prevent updating `HelmRepository` (#22).
- Prevent updating `HelmRelease` from `helm.toolkit.fluxcd.io/v2beta1` and `ImageUpdateAutomation` from `image.toolkit.fluxcd.io/v1beta1` (#21).

## 2024-05-16

### Removed

- Remove `ignoreUnstable` package rule (#20).

## 2024-05-15

### Added

- Add `ignoreUnstable` for apps that use prereleases (#18).

### Changed

- Update `default.json5` (#19).

## 2024-04-09

### Added

- Add regex registry URL (#17).

## 2024-02-20

### Added

- Add support for `-debug` tagged container images (#16).

## 2024-02-19

### Added

- Add regex to handle `*_release` format versions (#15).

## 2024-01-11

### Added

- Add package rule for `aws-cli` (#14).

## 2023-12-19

### Added

- Auto-merge Go PRs for patch dependency upgrades (#6).

### Changed

- Update Go package group regex to be more specific (#13).

## 2023-12-07

### Added

- Include comment-based regex on image properties (#12).

## 2023-12-01

### Added

- Add source URL for `architect-orb` dependency (#11).

## 2023-11-30

### Removed

- Remove ignore deps for architect (#10).

## 2023-11-15

### Added

- Support `helm_release` resources in Terraform.

## 2023-11-09

### Added

- Group AWS SDK dependencies (#8).

## 2023-11-02

### Changed

- Handle tags with a `v` prefix (#7).

## 2023-10-27

### Changed

- Force `opsctl` to use strict semver versioning (#5).

## 2023-10-23

### Added

- Add JSON5 validate workflow (#2).

## 2023-10-20

### Added

- Add initial preset configurations (#1).

### Fixed

- Add missing comma.

## 2023-10-19

### Added

- Initial commit.
