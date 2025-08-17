joenyland.zfs
=========================

[![CI](https://github.com/JoeNyland/ansible-zfs-role/actions/workflows/ci.yml/badge.svg)](https://github.com/JoeNyland/ansible-zfs-role/actions/workflows/ci.yml)

Installs ZFS and configures it.

Requirements
------------

None.

Role Variables
--------------

### `zfs_boot_load_keys`

Should encryption keys be loaded at boot? Defaults to `false`.

### `zfs_datasets`

A hash of ZFS datasets. Any properties defined here will be set on the datasets.

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: server
  roles:
    - role: joenyland.zfs
      vars:
        zfs_datasets:
          tank/home/joe:
            compression: lz4
```

License
-------

MIT

Author Information
------------------

⌨️ with ❤️ by [Joe Nyland](https://joe.nyland.io)
