# Reusable CI/CD Actions

This repository contains reusable GitHub Actions for CI/CD workflows. 

## Available Actions

### check-linear-history
Verifies that a PR maintains linear history (no merge commits).

```yaml
- uses: over88/reusable-cicd-actions/. github/actions/check-linear-history@main
```

### check-branch-updated
Verifies that a branch is up-to-date with the base branch.

```yaml
- uses: over88/reusable-cicd-actions/.github/actions/check-branch-updated@main
  with:
    base-branch:  main
```

### check-version-bump
Verifies that the package.json version has been properly bumped.

```yaml
- uses: over88/reusable-cicd-actions/.github/actions/check-version-bump@main
  with:
    base-ref: ${{ github.event.pull_request.base.sha }}
```

### generate-changelog
Generates a changelog based on git commits.

```yaml
- uses: over88/reusable-cicd-actions/.github/actions/generate-changelog@main
  id: changelog
  with:
    version:  1.0.0
```

## Usage

Reference these actions in your workflows using the full path with version:

```yaml
uses: over88/reusable-cicd-actions/.github/actions/<action-name>@main
```

## License

MIT
