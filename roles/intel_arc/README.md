Role Name
=========

This role installs the necessary Intel Arc drivers for hardware encoding on Debian 11.

It gets many required packages from the releases of [intel/intel-graphics-compiler](https://github.com/intel/intel-graphics-compiler) and compiles Linux 6.2.7 from source. (>=6.2.8 does not work with ZFS, if you don't use ZFS you can change the version.)  

Requirements
------------
- Debian 11 (10 may work but is not tested)
- Intel Arc GPU

Role Variables
--------------

Variable | Default | Description
--- | --- | ---
`jellyfin_intel_arc_opencl_icd_package_version` | `23.05.25593.11` | Intel Arc OpenCL ICD package version
`jellyfin_intel_arc_opencl_igd_package_version` | `1.0.13230.7` | Intel Arc OpenCL IGD package version
`jellyfin_intel_arc_opencl_igdgmm_package_version` | `22.3.0` | Intel Arc OpenCL IGD GMM package version
`jellyfin_intel_arc_debs` | See [defaults/main.yml](./defaults/main.yml) | List of Intel Arc deb packages
`jellyfin_intel_arc_firmware_packages` | See [defaults/main.yml](./defaults/main.yml) | List of Intel Arc firmware packages
`jellyfin_intel_arc_firmware_bins` | See [defaults/main.yml](./defaults/main.yml) | List of Intel Arc firmware binaries
`jellyfin_intel_arc_compile_kernel` | `true` | Whether to compile the kernel or not. Linux 6.2 is required for hardware encoding.
`jellyfin_intel_arc_kernel_major_version` | `6` | Major version of the Linux kernel to compile
`jellyfin_intel_arc_kernel_version` | `6.2.7` | Version of the Linux kernel to compile
`jellyfin_intel_arc_kernel_tar` | See [defaults/main.yml](./defaults/main.yml) | URL of the Linux kernel tarball
`jellyfin_intel_arc_kernel_release` | See [defaults/main.yml](./defaults/main.yml) | Release name of the Linux kernel tarball
`jellyfin_intel_arc_kernel_config` | `/boot/config-{{ ansible_kernel }}` | Path to current kernel config
`jellyfin_intel_arc_kernel_build_deps` | See [defaults/main.yml](./defaults/main.yml) | List of packages required to build the kernel
`jellyfin_intel_arc_kernel_config_values` | See [defaults/main.yml](./defaults/main.yml) | List of kernel config values to set
`jellyfin_intel_arc_kernel_built_debs` | See [defaults/main.yml](./defaults/main.yml) | Path to built kernel debs after compilation

Dependencies
------------

None

Example Playbook
----------------

```yaml
- name: Install Intel Arc drivers for Jellyfin
  hosts: "{{ target | default('jellyfin') }}"
  roles:
    - diademiemi.jellyfin.intel_arc
```


License
-------

MIT

Author Information
------------------

- diademiemi (@diademiemi)