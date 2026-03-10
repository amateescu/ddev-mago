[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/amateescu/ddev-mago/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/amateescu/ddev-mago/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/amateescu/ddev-mago)](https://github.com/amateescu/ddev-mago/commits)
[![release](https://img.shields.io/github/v/release/amateescu/ddev-mago)](https://github.com/amateescu/ddev-mago/releases/latest)

# DDEV Mago

## Overview

This add-on integrates Mago into your [DDEV](https://ddev.com/) project.

## Installation

```bash
ddev add-on get amateescu/ddev-mago
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev describe` | View service status and used ports for Mago |
| `ddev logs -s mago` | Check Mago logs |

## Advanced Customization

To change the Docker image:

```bash
ddev dotenv set .ddev/.env.mago --mago-docker-image="ddev/ddev-utilities:latest"
ddev add-on get amateescu/ddev-mago
ddev restart
```

Make sure to commit the `.ddev/.env.mago` file to version control.

All customization options (use with caution):

| Variable | Flag | Default |
| -------- | ---- | ------- |
| `MAGO_DOCKER_IMAGE` | `--mago-docker-image` | `ddev/ddev-utilities:latest` |

## Credits

**Contributed and maintained by [@amateescu](https://github.com/amateescu)**
