Python-From-Src
===============

OS: Redhat/CentOS 6/7

Ansible role for installing a particular version of Python from
source.

Requirements
------------

None

Role Variables
--------------

The only role vars that the user needs to worry about are:

- `pyfsrc_version`: The version of python to install
- `pyfsrc_make_default`: Whether to make this version of python the
  default version on the system.
- `pyfsrc_force_install`: Install again even if the specified version
  is already found.

Dependencies
------------

None

Example Playbook
----------------

eg:

```
    - name: Install python
      hosts: localhost
      sudo: yes
      roles:
        - role: python-from-source
          pyfsrc_version: 3.4.3
```

The above playbook will install python version 3.4.3.

The role can be used multiple times with different value of
`pyfsrc_version` to install different versions. This can be useful for
setting up an environment for testing a python lib against multiple
versions by using tox for eg.

License
-------

MIT

Author Information
------------------

Akhil Jalagam
