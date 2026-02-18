<p align="center">
  <img src="https://raw.githubusercontent.com/AstralEmu/.github/main/profile/banner-astralemu.svg" alt="AstralEmu" width="100%"/>
</p>

<h1 align="center">Contributing to AstralEmu</h1>

<p align="center">
  <i>Thank you for your interest in contributing. This guide covers how to contribute across all repositories in the organization.</i>
</p>

---

## Table of Contents

- [Getting Started](#getting-started)
- [Where to Contribute](#where-to-contribute)
- [Development Workflow](#development-workflow)
- [Adding Device Support](#adding-device-support)
- [Package Contributions](#package-contributions)
- [Image Builder Contributions](#image-builder-contributions)
- [Documentation](#documentation)
- [Commit Conventions](#commit-conventions)
- [Pull Request Process](#pull-request-process)
- [Coding Standards](#coding-standards)

---

## Getting Started

1. Fork the repository you want to contribute to
2. Clone your fork locally
3. Create a feature branch from `main`
4. Make your changes
5. Test thoroughly
6. Submit a pull request

## Where to Contribute

| Repository | What to Contribute |
|---|---|
| [astralemu](https://github.com/AstralEmu/astralemu) | Image builder, system configs, service management, performance tuning |
| [astralemu-packages](https://github.com/AstralEmu/astralemu-packages) | Emulator build recipes, packaging scripts, cross-distro translation |
| [astralemu.github.io](https://github.com/AstralEmu/astralemu.github.io) | Documentation, guides, device pages |
| [.github](https://github.com/AstralEmu/.github) | Organization-wide templates and community files |

## Development Workflow

```bash
# Fork and clone
git clone git@github.com:YOUR_USERNAME/REPO_NAME.git
cd REPO_NAME

# Create a feature branch
git checkout -b feat/my-feature

# Make changes, then commit
git add .
git commit -m "feat: description of the change"

# Push and open a PR
git push origin feat/my-feature
```

---

## Adding Device Support

AstralEmu supports adding new hardware targets through a simple YAML configuration. To add a new device:

1. Create a device YAML file with:
   - Device codename
   - CPU compilation flags and architecture
   - Vendor-specific package repositories
2. The build farm will automatically:
   - Compile all emulators with the correct CPU flags
   - Mirror and translate vendor packages across all supported distros (Debian, Ubuntu, Fedora, Arch Linux)
   - Generate the per-device performance tuning package

If you want to add support for a device you own, open a **Device Support Request** issue first to discuss the approach.

## Package Contributions

When contributing to the package build system:

- All emulator builds must use `LTO=thin` and `jemalloc` when supported
- Builds must target the exact CPU architecture of the device
- Test your build locally before submitting
- Ensure the package builds cleanly for all target distributions
- Do not include pre-built binaries in PRs — the CI rebuilds everything from source

### Cross-Distribution Translation

The package translation system mirrors vendor repositories across distributions. When contributing:

- Handle differences in directory layouts between distros
- Account for package naming differences
- Include dependency resolution for packages missing or at wrong versions in the target distro
- Test on at least two target distributions

## Image Builder Contributions

The image builder handles:

- **Service management**: Only one service runs at a time (ES-DE is the primary, XFCE/Plasma Mobile/Kodi/Waydroid are secondary)
- **Export formats**: Ensure your changes work across all supported export formats
- **Architecture support**: Validate on the targeted CPU architectures

When modifying the build workflow:

- Maintain the existing fair-use optimizations (skip download/build/upload of unchanged content)
- Respect the 24-hour rebuild cycle
- Test with at least one base system (Ubuntu, Debian, Arch Linux, or Universal Blue)

## Documentation

Documentation lives at [astralemu.github.io](https://github.com/AstralEmu/astralemu.github.io) and is built with Starlight. To contribute:

1. Follow the [Starlight docs](https://starlight.astro.build/) for content structure
2. Place pages in the correct section
3. Test locally with `npm run dev` before submitting
4. Include screenshots where relevant

---

## Commit Conventions

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
type(scope): description

[optional body]
```

### Types

| Type | Usage |
|---|---|
| `feat` | New feature or device support |
| `fix` | Bug fix |
| `perf` | Performance improvement |
| `build` | Build system or CI changes |
| `docs` | Documentation changes |
| `refactor` | Code refactoring |
| `chore` | Maintenance tasks |

### Scopes (examples)

`image-builder`, `packages`, `performance`, `es-de`, `device/<codename>`, `translation`, `ci`

## Pull Request Process

1. **One concern per PR** — Keep PRs focused on a single change
2. **Fill in the PR template** — Describe what, why, and how to test
3. **Ensure CI passes** — All GitHub Actions checks must be green
4. **Wait for review** — A maintainer will review your PR
5. **Address feedback** — Make requested changes in additional commits
6. **Squash on merge** — PRs are squash-merged to keep history clean

---

## Coding Standards

### Shell Scripts (Bash)
- Use `#!/usr/bin/env bash` with `set -euo pipefail`
- Use [ShellCheck](https://www.shellcheck.net/) to lint
- Quote all variables

### YAML (Workflows, Device Configs)
- Use 2-space indentation
- Add comments for non-obvious values
- Validate syntax before committing

### General
- No hardcoded paths — use variables and configs
- Keep scripts idempotent (safe to re-run)
- Prefer clarity over cleverness

## Code of Conduct

All contributors must follow our [Code of Conduct](CODE_OF_CONDUCT.md). Notably, **any contribution related to piracy will be rejected and may result in a ban**.

## Questions?

- Open a [Discussion](https://github.com/orgs/AstralEmu/discussions) for general questions
- Check the [Documentation](https://astralemu.github.io) for guides
- Use issue templates for bugs, feature requests, or device support requests

---

<p align="center">
  <a href="https://astralemu.github.io">Documentation</a> &middot;
  <a href="https://github.com/orgs/AstralEmu/discussions">Community</a> &middot;
  <a href="https://github.com/AstralEmu/astralemu">Main Repository</a>
</p>
