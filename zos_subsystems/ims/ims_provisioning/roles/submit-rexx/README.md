submit-rexx
=========

This role is a utility used by other roles to submit REXX jobs that need to run in the TSO/E address space.


Requirements
------------

* None

Role Variables
--------------
- ### ** rexx_name **
   The name of the REXX program to run.  This program must be previously sent over using send-template.


Dependencies
------------

Depends on the following roles:

* submit-tso-rexx
* check-job-status
* save-as-dataset

Example Playbook
----------------
```yaml

      - include_role:
          name: submit-rexx
          public: yes
        vars:
          rexx_name: 'IEFJOBSX.j2'
          max_rc: 0

```

## Copyright

© Copyright IBM Corporation 2020

License
-------

Copyright (c) IBM Corporation 2020 Apache License, Version 2.0 (see https://opensource.org/licenses/Apache-2.0)

