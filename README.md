[![CI](https://github.com/StoneSoupKitchen/ansible-role-cron/actions/workflows/ci.yml/badge.svg)](https://github.com/StoneSoupKitchen/ansible-role-cron/actions/workflows/ci.yml)

# Ansible role: cron

An Ansible role for configuring cron and at daemons.

## Requirements

Supported operating systems:
* Debian 10 (Buster)
* Debian 11 (Bullseye)

## Role Variables

The following table lists all variables that can be overridden
and their default values.

| Name                     | Default Value | Description                      |
| ------------------------ | ------------- | -------------------------------- |
| `at_package` | at | Name of the at package. Use `name=ver` format to pin. |
| `at_package_state` | present | Installation state for the at package. |
| `cron_package` | cron | Name of the cron package. Use `name=ver` format to pin. |
| `cron_package_state` | present | Installation state for the cron package. |

## Examples

```yaml
- hosts: all
  roles:
    - stonesoupkitchen.cron
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

