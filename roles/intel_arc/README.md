Ansible Role Template
=========

[![Molecule test](https://github.com/diademiemi/ansible_collection_diademiemi.jellyfin/actions/workflows/ansible-role-intel_arc.yml/badge.svg)](https://github.com/diademiemi/ansible_collection_diademiemi.jellyfin/actions/workflows/ansible-role-intel_arc.yml)

This is an Ansible role to install and configure intel_arc.

Include more information about intel_arc in this section.

Requirements
------------
These platforms are supported:
- Debian 11  

<!--
- List hardware requirements here  
-->

Role Variables
--------------

Variable | Default | Description
--- | --- | ---
<!--
`variable` | `default` | Variable example
`long_variable` | See [defaults/main.yml](./defaults/main.yml) | Variable referring to defaults
`distro_specific_variable` | See [vars/debian.yml](./vars/debian.yml) | Variable referring to distro-specific variables
-->

Dependencies
------------
<!-- List dependencies on other roles or criteria -->
None

Example Playbook
----------------

```yaml
- name: Use diademiemi.jellyfin.intel_arc role
  hosts: "{{ target | default('intel_arc') }}"
  roles:
    - diademiemi.jellyfin.intel_arc
```

License
-------

MIT

Author Information
------------------

- diademiemi (@diademiemi)

Role Testing
------------

This repository comes with Molecule that run in Podman on the supported platforms.
Install Molecule by running

```bash
pip3 install -r requirements.txt
```

Run the tests with

```bash
molecule test
```

These tests are automatically ran by GitHub Actions on push. If the tests are successful, the role is automatically published to Ansible Galaxy.

GitHub Actions is supposed to fail for this intel_arc repository, as it does not contain any meaningful role. There is an explicit assertion to check if the role name has been changed from `intel_arc` which causes the test to fail.  
