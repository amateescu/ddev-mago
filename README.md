[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/amateescu/ddev-mago/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/amateescu/ddev-mago/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/amateescu/ddev-mago)](https://github.com/amateescu/ddev-mago/commits)
[![release](https://img.shields.io/github/v/release/amateescu/ddev-mago)](https://github.com/amateescu/ddev-mago/releases/latest)

# ddev-mago

DDEV add-on for [Mago](https://github.com/carthage-software/mago) — the blazing-fast PHP linter, formatter, and static analyzer written in Rust.

## Installation

```bash
ddev add-on get amateescu/ddev-mago
ddev restart
```

## Usage

```bash
ddev mago lint                    # Lint the project
ddev mago lint --fix              # Auto-fix lint issues
ddev mago format                  # Format code
ddev mago format --check          # Check formatting without writing
ddev mago analyze                 # Run static analysis
ddev mago --version               # Show installed version
```

## Updating

The add-on checks for new Mago releases on `ddev start` and notifies you when an update is available. To update:

```bash
ddev add-on get amateescu/ddev-mago
ddev restart
```

## Pinning a Mago version

By default, the add-on installs the latest Mago release. To pin a specific version, add `MAGO_VERSION` to `web_environment` in your `.ddev/config.yaml`:

```yaml
web_environment:
  - MAGO_VERSION=1.14.1
```

Then restart: `ddev restart`

To unpin and go back to the latest version, remove the `MAGO_VERSION` entry and run:

```bash
ddev add-on get amateescu/ddev-mago
ddev restart
```

## Configuration

Mago is configured via a `mago.toml` file in your project root.
See the [Mago documentation](https://mago.carthage.software) for all available options.

## Credits

**Contributed and maintained by [@amateescu](https://github.com/amateescu)**
