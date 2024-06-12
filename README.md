# Bootstrap Fedora Workstation using Ansible
This repo contains a playbook to bootstrap a Fedora Workstation using Ansible (mine happens to be the Red Hat CSB, but any Fedora spin should work as a starting point)

## Running the playbook

Install ansible-core (if needed):
```
sudo dnf install ansible-core
```

Install requirements:
```
ansible-galaxy install -r collections/requirements.yml
```

Run the playbook to boostrap workstation:
- `-K` is needed to prompt for BECOME password if a sudo password is required for the current user
- Set the extra var `user` if you would like to setup a user other than `rgniadek`
```
ansible-playbook bootstrap.yml [-K] [-e user=$USER]
```

## Contributing

`bootstrap.yml` in the repo root is the entrypoint. Most tasks are broken up into seperate tasks files under the `tasks/` directory, you can add tasks to the playbook as neeeded using `ansible.builtin.include_tasks`
