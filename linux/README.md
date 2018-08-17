# azure-ansible for linux

A simple example of creating an Azure image from VHD file on Azure using Ansible.

Couple of things you need to set :

export ANSIBLE_HOST_KEY_CHECKING=False

edit vars/azure/credential.yml and enter the ssh public key

run playbook : ansible-playbook -vv create-image.yml --extra-vars '{ "service_principal_username": "xxx", "service_principal_password": "xxx", "service_principal_tenant": "xxx"}'

check out the blobstorage for the image

To-do :

1. You should create a centralize blob storage to store all your images
2. need to delete un-used resources after the image has been built - vm, network, nic and etc
3. more to add ... 