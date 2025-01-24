Ansible Collection for Managing Workstations
===


Usage
---

* Add `ansible.cfg`
  ```ini
  [defaults]
  roles_path = .galaxy/roles/:roles/
  collections_path = .galaxy/
  ```
* Add `requirements.yml`, then run `ansible-galaxy install -r requirements.yml`
  ```yaml
  ---
  collections:
    - source: https://github.com/8ware/ansible-collection-workstation.git
      type: git
  ```
* Assign roles in `host_vars/locahost.yml`
  ```yaml
  ---
  workstation_setup_roles:
    - local.workstation.security
    - <custom_role>
  ```
* Finally, run `ansible-playbook local.workstation.setup`
