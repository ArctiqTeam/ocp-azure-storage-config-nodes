# OCP Azure Storage Config for Nodes

Per the docs:
https://docs.openshift.com/container-platform/3.7/install_config/configuring_azure.html

The noted blocks need to be added to masters and nodes in  an OCP cluster for azure storage to work.
These playbooks and the accompanied inventory file facilitate putting these code blocks into place.

1. Please populate the inventory file with your nodes appropriately.
2. Please populate the azure.conf file with your environment details.
3. to add the blocks, run from your Ansible host..

`ansible-playbook -i nodes az-stor-config-add.yml`

4. to remove the blocks, run from your Ansible host..

`ansible-playbook -i nodes az-stor-config-remove.yml`

That's all.
