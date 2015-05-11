# Ansible Role: NVM

Role to install nvm and multiple nodejs versions.

## Requirements

Tested with Ansible 1.8.4.

## Role Variables

```yaml
---
# This could be set to 'user' to support user installs.
nmv_env: system

nmv_version: v0.4.0

# This sets the nvm global nodejs version.
nvm_default_node_version: stable

# List of nodejs versions to install.
nvm_node_versions:
  - stable

# List of defaults gem to install on each nodejs version.
nmv_packages:
  - bundler
  - pry
  - rubocop

# List of users to install nvm and nodejs versions to.
# Ignored if nmv_env is set to 'system'
nmv_users: []
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
