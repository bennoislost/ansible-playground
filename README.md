# Ansible Playground

Boilerplate repository to create and test ansible roles.

## Add Roles to playbook

- Symlink your ansible role to `ansible/vendor/roles`

```
ln -s ~/Projects/some/ansible/role ansible/vendor/role
```

- Add role name to the roles node in `ansible/playbooks/provision.yaml`

- Run vagrant `vagrant up` or `vagrant provision`

Copyright Ben McManus 2015