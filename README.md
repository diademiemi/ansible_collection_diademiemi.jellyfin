# Ansible Collection - diademiemi.jellyfin

This collection is mainly focused at installing Jellyfin on Debian 11 with Intel Arc hardware encoding support.  

I may add support for other distros and hardware in the future if it is requested.  

## Requirements
- Debian 11 (10 may work but is not tested)
- Intel Arc GPU

## Contents 

### Roles
Role | Description
--- | ---
[diademiemi.jellyfin.install](./roles/install/) | Install Jellyfin on Debian 11
[diademiemi.jellyfin.intel_arc](./roles/intel_arc/) | Install necessary Intel Arc drivers for hardware encoding

Check the roles READMEs for more information!  