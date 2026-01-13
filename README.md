# Maya-Role

[![AlmaLinux9-CI](https://github.com/philnewm/ansible-maya/actions/workflows/almalinux9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-maya/actions/workflows/almalinux9-ci-caller.yml) [![Rocky9-CI](https://github.com/philnewm/ansible-maya/actions/workflows/rocky9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-maya/actions/workflows/rocky9-ci-caller.yml) [![Fedora43-CI](https://github.com/philnewm/ansible-maya/actions/workflows/fedora43-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-maya/actions/workflows/fedora43-ci-caller.yml)

Role description

This role includes a molecule testing setup as a submodule at `molecule/`

## Structure

```code
📦 ansible-maya
 ┣ 📂defaults
 ┃ ┗ 📜main.yml
 ┣ 📂meta
 ┃ ┗ 📜main.yml
 ┣ 📂 molecule
 ┃ ┗ 📂 default
 ┃   ┗ 📜, 📜, 📜, scenario_files
 ┣ 📂tasks
 ┃ ┣ 📜absent.yml
 ┃ ┣ 📜adsk_licensing_install.yml
 ┃ ┣ 📜dependencies.yml
 ┃ ┣ 📜get_setup.yml
 ┃ ┣ 📜main.yml
 ┃ ┣ 📜maya_install.yml
 ┃ ┣ 📜maya_plugins_install.yml
 ┃ ┣ 📜present.yml
 ┃ ┗ 📜tests.yml
 ┣ 📂vars
 ┃ ┗ 📜main.yml
 ┣ 📜README.md
 ┗ 📜requirements.yml

```

Describe and explain role structure.

## Requirements

Elaborate external dependencies and how to use them.

## Role Variables

* defaults/main.yml
  * first_var
  * sec_var
  * third_var
* vars/main.yml
  * first_var
  * sec_var
  * third_var

## Dependencies

List role ansible-galaxy dependencies - if any.

## Example Playbook

Add an example playbook

```yaml
---

tasks:
  - name: Include ansible-maya present
    ansible.builtin.include_role:
      name: ansible-maya
    vars:
      state: present
      maya_version_major: 2026
      maya_version_minor: 3
      maya_version_patch: 0
      license_manager: true
      maya_license_manager_version: "16.0.3.14414"
      maya_plugin_packages:
        - "MayaUSD"
        - "Bifrost"
        - "Substance"
        - "LookdevX"
        - "MtoA"

...
```

## License

Add license - if any.
