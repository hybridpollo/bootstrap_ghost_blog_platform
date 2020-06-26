### About
This repository contains the necessary roles to deploy the Ghost blogging  
platform (https://ghost.org/) in an automatically provisioned OpenStack  
virtual machine. 

### Requisites
- Access to an OpenStack Environment
- openstacksdk
- openstacksdk >= 0.12.0
- python >= 2.7
- Ansible 2.x or greater. This was tested with 2.9.6

The Ansible website contains great documentation for the [OpenStack Ansible Modules.](https://docs.ansible.com/ansible/latest/modules/list_of_cloud_modules.html#openstack)


### How to Use
This repository comes with two main playbooks:  

- **deploy-openstack-vm.yaml** - Deploys the OpenStack virtual machine  
- **deploy-ghost-platform.yaml** - Deploys the Ghost blogging platform   
  on the virtual machine deployed with the first playbook.

### Variables

Default role variables are located in the 'roles/<role-name>/defaults/main.yaml' file. 

**deploy-openstack-vm**

`osp_cloud` - The name of the OpenStack cloud used to provisioned the virtual machine  
this is equals to `export OS_CLOUD=<cloud-name>` which references the authentication  
parameters from the OpenStack client configuration file under `~/.config/openstack/clouds.yaml`
