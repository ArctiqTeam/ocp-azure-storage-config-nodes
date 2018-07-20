# OCP Azure Storage Config for Nodes

#### This group of Ansible playbooks and templates will configure your OCP 3.7 or 3.9 Cluster to consume Azure-Disk and Azure-File for PVs. Be aware of what these playbooks do before using them.

## For Azure Disk/ Block

Per the docs:
* https://docs.openshift.com/container-platform/3.7/install_config/configuring_azure.html
* https://docs.openshift.com/container-platform/3.9/install_config/configuring_azure.html

The noted blocks need to be added to masters and nodes in  an OCP cluster for azure storage to work.
These playbooks and the accompanied inventory file facilitate putting these code blocks into place.

1. Please populate the inventory file with your nodes appropriately.
2. Please populate the azure.conf file with your environment details.
3. to add the blocks, run from your Ansible host..

`ansible-playbook -i nodes az-stor-config-add.yml`

4. to remove the blocks, run from your Ansible host..

`ansible-playbook -i nodes az-stor-config-remove.yml`

That's all.

## For Azure File

* ensure the necessary vars in the nodes.inv file are filled.
* ensure the necessary .j2 template files are used with the relevant az-file*.yml files as well.
