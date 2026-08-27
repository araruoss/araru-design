# Versioning

Araru Design uses [Semantic Versioning](https://semver.org/) and follows [Conventional Commits](https://www.conventionalcommits.org/). Its version is independent from Araru Server, Web, Android, Desktop and Docs.

Release Please opens a release pull request when releasable commits reach `main`. Merging that pull request updates `CHANGELOG.md`, creates the Git tag `vX.Y.Z` and publishes the corresponding GitHub Release.

## GitHub Actions permissions

The repository must allow GitHub Actions to create pull requests. In GitHub, open **Settings → Actions → General → Workflow permissions**, enable **Read and write permissions**, and enable **Allow GitHub Actions to create and approve pull requests**.

If organization policy does not allow that setting, create a fine-grained token with repository Contents and Pull requests write access, save it as the repository secret `RELEASE_PLEASE_TOKEN`, and the workflow will use it automatically.

## Commit types

- `feat`: new foundation, token, component contract or pattern; minor release.
- `fix`: correction that preserves the public design contract; patch release.
- `docs`: editorial clarification; patch release when included in a release.
- `refactor`: non-breaking restructuring; patch release when included in a release.
- `feat!` or `BREAKING CHANGE`: incompatible token or behavior change; major release.

Do not release only to keep versions aligned with another Araru repository. Translations are maintained in `araru-docs` and do not change this repository's version unless the English design contract changes.
