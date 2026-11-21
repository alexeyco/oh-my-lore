# Contributing

Keep changes small and focused. Describe user-visible behavior in the README and update the relevant plugin manifest when its packaging changes.

## Requirements

- Node.js 22 or newer
- npm

## Branch naming

Use `feat/<topic>` for a focused feature branch. Replace `<topic>` with a short description of the change, for example `feat/npm-release-workflow`.

## Local checks

```sh
node --check index.js
npm pack --dry-run
```

## Releases

The release workflow publishes a Git tag whose version matches `package.json`. Configure the repository's `NPM_TOKEN` secret with permission to publish the package before creating a release tag. The workflow publishes a public package with npm provenance.

Do not publish directly from a local checkout.
