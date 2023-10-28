Ansible Collection - diademiemi.jellyfin
========================================

This collection is mainly focused at installing Jellyfin on Debian 11 with Intel Arc hardware encoding support.  

I may add support for other distros and hardware in the future if it is requested.  

Contents
========

Roles
------
Role | Description | CI Status
--- | --- | ---
[diademiemi.jellyfin.install](./roles/install/) | Install Jellyfin | [![Molecule test](https://github.com/diademiemi/ansible_collection_diademiemi.jellyfin/actions/workflows/ansible-role-install.yml/badge.svg)](https://github.com/diademiemi/ansible_collection_diademiemi.jellyfin/actions/workflows/ansible-role-install.yml)
[diademiemi.jellyfin.intel_arc](./roles/intel_arc/) | Install necessary Intel Arc drivers for hardware encoding on Debian 11 | [![Molecule test](https://github.com/diademiemi/ansible_collection_diademiemi.jellyfin/actions/workflows/ansible-role-intel_arc.yml/badge.svg)](https://github.com/diademiemi/ansible_collection_diademiemi.jellyfin/actions/workflows/ansible-role-intel_arc.yml)

Click on the role to see the README for that role.  

Collection Structure
--------------

This collection makes use of my [Ansible Role Template repository](https://github.com/diademiemi/ansible_role_%74emplate.git).  The `add-role.sh` script downloads this Template and generates a new role with the name specified. If a `molecule/default/molecule.yml` file is present, it will be ran with GitHub Actions.  
<!-- I use %74 here to encode to a "t" so it doesnt get recursively replaced. The .git causes a redirect so you end up at the right URL :)-->
