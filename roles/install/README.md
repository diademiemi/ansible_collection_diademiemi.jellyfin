Role Name
=========

This role installs Jellyfin on Debian 11 from the Jellyfin repositories.  

Requirements
------------

- Debian 11 (10 may work but is not tested)

Role Variables
--------------

No variables are required.

Dependencies
------------

None
Example Playbook
----------------

```yaml
- name: Install Jellyfin
  hosts: "{{ target | default('jellyfin') }}"
  roles:
    - diademiemi.jellyfin.install
```

License
-------

MIT

Author Information
------------------

- diademiemi (@diademiemi)