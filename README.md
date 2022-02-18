[![CI](https://github.com/StoneSoupKitchen/ansible-role-journald/actions/workflows/ci.yml/badge.svg)](https://github.com/StoneSoupKitchen/ansible-role-journald/actions/workflows/ci.yml)

# Ansible role: journald

An Ansible role for configuring journald.

## Requirements

Supported operating systems:
* Debian 10 (Buster)
* Debian 11 (Bullseye)

## Role Variables

The following table lists all variables that can be overridden
and their default values.

| Name                     | Default Value | Description                      |
| ------------------------ | ------------- | -------------------------------- |
| `journald_package` | systemd-journal-remote | Name of the journald package. Use `name=ver` format to pin. |
| `journald_package_state` | present | Installation state for the journald package. |

## Examples

```yaml
- hosts: all
  roles:
    - stonesoupkitchen.journald
```

## Development

A Makefile is included for easier development with `pipenv`.
After cloning this repository,
use the following commands to set up an environment.

    pipenv install --dev

To lint your changes with ansible-lint:

    make lint

To run tests with molecule:

    make test

## License

See [LICENSE](./LICENSE).

