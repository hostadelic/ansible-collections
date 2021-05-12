Ansible Collection - hostadelic.devops
======================================

Miscellaneous elements for Hostadelic DevOps. Reusable but targeted to our
projects.

# Roles

## globals

A role to define various global variables:

- `paths`: Considering the playbook is one level deeper in the directory
  hierarchy than the root repository (e.g. `<root>/playbooks/main.yaml`),
  `paths` will contain variables as `prefix`, `libdir`, `datadir` etc. expanding
  to full paths equivalents of `<root>`, `<root>/lib`, `<root>/var` etc.
- `settings`: Content of `<root>/settings.yaml` if it exists.
- `secrets`: Content of `<root>/secrets.yaml` if it exists.
