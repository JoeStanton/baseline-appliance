# Baseline Appliance

This repository contains the Ansible provisioning scripts for the
Baseline monitoring server, bundled with:

* A Vagrantfile for testing and development
* Packer configurations for generating hosted/in-house appliances

To deploy real SSL certs, scp them to the /etc/nginx directory, the
playbook will not overwrite real certs placed here.
