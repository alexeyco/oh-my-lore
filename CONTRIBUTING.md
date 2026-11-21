# Contributing

Keep changes small and focused. Describe user-visible behavior in the README and update the relevant plugin manifest when its packaging changes.

## Requirements

- Node.js 22 or newer
- npm

## Branch naming

Do not push directly to `master`. Create a feature branch from `master` using
`feat/<topic>` for a focused change. Replace `<topic>` with a short description,
for example `feat/npm-release-workflow`.

## Commit messages

Use no conventional prefixes and write commit messages in the past tense. For
example: `Added npm release workflow` or `Fixed package metadata`.

## Local checks

```sh
node --check index.js
npm pack --dry-run
```

## Releases

The release workflow publishes a Git tag whose version matches `package.json`. Configure the repository's `NPM_TOKEN` secret with permission to publish the package before creating a release tag. The workflow publishes a public package with npm provenance.

Do not publish directly from a local checkout.
