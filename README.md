# ryangniadek.bootstrap_workstation collection
This repo contains a collection to bootstrap a Fedora Workstation using Ansible (mine happens to be the Red Hat CSB, but any Fedora spin should work as a starting point).

Possible future plans to incorporate other operating systems.

## Roles in this collection

| Name | Description |
| :--- | :--- |
| [ryangniadek.bootstrap_workstation.users](roles/users/README.md) | Setup one or more users and their standard configuration files |
| [ryangniadek.bootstrap_workstation.packages](roles/packages/README.md) | Install packages and other associated tasks |
| [ryangniadek.bootstrap_workstation.services](roles/services/README.md) | Manages systemd services |
