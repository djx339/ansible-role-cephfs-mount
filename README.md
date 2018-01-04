Ansible Role: Mount Cephfs
=========

Mount cephfs on Ubuntu/Debian.

Requirements
------------

Linux kernel must larger than 4.0

Role Variables
--------------

`cephfs_endpoint`: The cephfs to be mount. (Default: `localhost:6789:/`)

`cephfs_mountpoint`: The mountpoint of cephfs. (Default: `/cephfs`)

`cephfs_user`: The user to connect cephfs. (Default: `admin`)

`cephfs_secret`: The secret of `cephfs_user`. (Default: `oj32j90ajsf90jjsdffd==`)

`cephfs_secret_file_prefix`: The prefix of cecret file. (Default: `localhost.`)

Dependencies
------------

None.

Example Playbook
----------------


```yml
- hosts: servers
  vars:
    cephfs_endpoint: ceph.example.com:6789:/
    cephfs_mountpoint: /mnt/cephfs
    cephfs_user: admin
    cephfs_secret: o9238jf9ajsdfje3jf9je==
    cephfs_secret_file_prefix: ceph.example.com.
  roles:
    - { role: djx339.cephfs-mount }
```

License
-------

BSD

Author Information
------------------

This role was created by [Daniel D](https://github.com/djx339).
