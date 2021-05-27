Role Name
=========

This role will create ssh passwordless connectivity between master and replica servers and vice versa.


Role Variables
--------------

| Variable  |  Required | default   | type  |
| ----      |   ------  |  ----- |  -----   |
| ssh_ssh_setup_action | no | choices: </br>add (default) </br> remove | string  |
| ssh_setup_ssh_dir | no  | ~/.ssh  | string |
| ssh_setup_user| no  | postgres  | string  |
| ssh_setup_ssh_key_name| no | id_rsa  | string  |
| ssh_setup_ssh_auth_key_path| no | /etc/ssh/auth_keys/<ssh_setup_user>  | string |
| ssh_setup_source_host| yes |  none | string |
| ssh_setup_target_hosts|  yes  | none  | list  |

Example Playbook
----------------

```
- name: "Configure source server ssh connection to target server(s)"
  hosts: localhost
  gather_facts: false
  any_errors_fatal: true
  vars:
   ansible_ssh_user: root
  tasks:
    - include_role:
        name: ../roles/ssh_setup
      vars:
        - ssh_setup_source_host: "host_1"
        - ssh_setup_target_hosts:
          - host_2
          - host_3
```
