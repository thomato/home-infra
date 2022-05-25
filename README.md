# Home server
Installs my homelab server.

## Prepare server
First run the `setup-server.yml` playbook using the following command:
```
ansible-playbook setup-server.yml -i hosts -kK
```

This asks for the connection password and for the privilege escalation password. After running this, SSH Public Key authencation will be set up as well as passwordless sudo.
