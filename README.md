# Home server
Installs my homelab server.

## Prepare server
First run the `setup-server.yml` playbook using the following command:
```
ansible-playbook setup-server.yml -i hosts -kK
```

This asks for the connection password and for the privilege escalation password. After running this, SSH Public Key authencation will be set up as well as passwordless sudo.

## Install containers
First make sure to install all requirements:
```
ansible-galaxy install -r requirements.yml
```

When the server is prepared we can start running the playbooks. For now a lot of separate playbooks are found in the subfolders. These will all be moved to `main.yml`. You can run the main playbook as follows:
```
ansible-playbook main.yml -i hosts
```

Note that the `main.yml` runs independent of `setup-server.yml` and can still be used without it. Just add the `-kK` flag and you're good to go.