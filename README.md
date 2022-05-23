# Home server
## Remote setup
Install Linux on the remote machine. A bare installation will suffice.

## Local setup

A lot of Docker containers are set up with Lets Encrypt. If not available locally, create a new private key for the TransIP API and place it under:
```
~/.keys/transip
```

## Install 
Install Docker:
```
ansible-playbook docker/playbook.yaml -i hosts -l homelab -u nando -kK
```

Install Jenkins
```
ansible-playbook jenkins/playbook.yml -i hosts -l homelab -u nando -kK
```
