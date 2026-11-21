# Plugin distribution

## Purpose

Describe the current distributable plugin scaffold.

## Requirements

### Requirement: OpenCode package entrypoint
The package SHALL expose an OpenCode plugin entrypoint that registers no user-facing behavior.

#### Scenario: Load the package
- **WHEN** OpenCode loads the package
- **THEN** the package exports the `oh-my-lore` plugin with an empty setup hook

### Requirement: Codex manifest
The repository SHALL provide a Codex plugin manifest that declares no skills or MCP servers.

#### Scenario: Inspect Codex plugin capabilities
- **WHEN** Codex reads the manifest
- **THEN** it identifies the `oh-my-lore` plugin without declaring capabilities

### Requirement: npm release
The release workflow SHALL publish the package to npm when a version-matching `v*` tag is pushed.

#### Scenario: Publish a tagged version
- **WHEN** a tag matching the package version is pushed
- **THEN** the workflow publishes the public package to npm

#### Scenario: Reject a mismatched tag
- **WHEN** a tag version differs from `package.json`
- **THEN** the workflow fails before publishing
