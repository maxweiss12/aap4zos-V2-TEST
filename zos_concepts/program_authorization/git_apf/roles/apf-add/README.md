apf-add
===============

Add a batch of libraries to z/OS APF list and make parmlib APF statement entries to a data set or data set member.

Requirements
------------

- Ansible Collection `ibm.ibm_zos_core`

Role Variables
--------------

- `add_list`: A list of dictionaries for batch insertion to the z/OS system APF list.

- `persistent_ds`: A dictionary with a data set or data set member to make APF statement entries.

Example Playbook
----------------

```yaml
- hosts: zos_host
  collections:
    - ibm.ibm_zos_core
  gather_facts: no
  environment: "{{ environment_vars }}"

  tasks:
    - name: Add to APF list
      include_role:
        name: apf-add
```

License
-------

Copyright (c) IBM Corporation 2020
Apache License, Version 2.0 (see https://opensource.org/licenses/Apache-2.0)

Author Information
------------------

- Behnam Al Kajbaf behnam@ibm.com, [@balkajbaf](https://github.com/balkajbaf)

Support
-------

All IBM certified sample playbooks, roles and filters are supported as part of
the Red Hat® Ansible Certified Content for IBM Z offering. Support for samples
is managed through the repositories git issues:
https://github.com/IBM/z_ansible_collections_samples/issues
