Ansible Managed K8s - by Tyler Bennet
=============



Ansible Tower / Ansible

Prep ansible from a windows PC, Install WSL for Ubuntu
Add an SSH key for the WSL instance
Copy the SSH key to the host to deploy ansible against
Configure hosts/inventory.yml to use the proper yaml syntax
Run the Setup.yml file against the host to configure the networking with Netplan
Run the docker.yml file with the command below and the proper target name from inventory
#
Configure Nodes

1. Run setup.yml, k3ssetup.yml, containerd.yml, kubecommands.yml on all nodes
2. Run control.yml on the main node
3. Run Join command on remaining nodes

#RUN
ansible-playbook -i hosts/inventory.yml k3ssetup.yml -Kk --extra-vars "target=prox-aether01"
