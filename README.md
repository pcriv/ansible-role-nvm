# Ansible Role: NVM

Role to install nvm and multiple nodejs versions.

## Requirements

Tested with Ansible 1.8.4.

## Role Variables

```yaml
---
# This could be set to 'user' to support user installs.
nvm_env: system

nvm_version: v0.4.0

# This sets the nvm global nodejs version.
nvm_default_node_version: stable

# List of nodejs versions to install.
nvm_node_versions:
  - stable

# List of defaults gem to install on each nodejs version.
nvm_packages:
  - bower
  - jslint
  - coffee-script

# List of users to install nvm and nodejs versions to.
# Ignored if nvm_env is set to 'system'
nvm_users: []
```

## Dependencies

- ANXS.git

## Example Playbook

```yaml
- hosts: js-devbox
  roles:
    - pablocrivella.nvm
```

For a more detailed example check this [Playbook](https://github.com/pablocrivella/apps-forge/blob/master/provisioning/js.yml).

## License

MIT

## Author Information

Pablo Crivella Backend Engineer @ NobelBiz.
