
# Actions-Toolkit

> Reusable Actions and Workflows for my personal projects.

All actions and reusable workflows are designed with transparency and security in mind and can be combined as needed. There are actions for different software ecosystems and languages.

## Versioning

The same immutable git-tag is used for all actions and workflows when they are released. There are no floating-tags for this repository available. The versions are semver based. Third-party actions used internally are referenced with git-sha to prevent unexpected updates and ensure the build-system is reproducible.


## Workflows

| Name                                                                     | Description |
| ------------------------------------------------------------------------ | ----------- |
| [Release GoReleaser](.github/workflows/toolkit-release-goreleaser.yml)   | Releases a GoReleaser project with a OCI-Image, optional signing (Cosign), SBOM, SLSA provenance generation, Changelog and a GitHub release. |


## Actions

| Name                                                                     | Description |
| ------------------------------------------------------------------------ | ----------- |
| [Docker](docker/README.md)   | Creates a OCI-Image with multi-arch support. It can be signed with Cosign optionally. Only ghcr.io is currently supported. |
| [Push-Release](push-release/README.md)   | Commits and pushes possible changes and creates a GitHub-Release. |
| [SBOM](sbom/README.md)   | Creates a SBOM from a OCI-Image. It can be optionally signed and attested with Cosign. |
| [Setup-Cosign](setup-cosign/README.md)   | Run's the cosign-installer and writes the private-key to a `cosign.key` file. |
| [SLSA-Provenance](slsa-provenance/README.md)   | Generates a provenance-file from artifacts (SLSA Level 1). It can be optionally signed and attested with Cosign (SLSA Level 2). |