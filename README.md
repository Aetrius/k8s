Ansible Managed K3s - by Tyler Bennet
=============



Ansible Tower / Ansible

Prep ansible from a windows PC, Install WSL for Ubuntu
Add an SSH key for the WSL instance
Copy the SSH key to the host to deploy ansible against
Configure hosts/inventory.yml to use the proper yaml syntax
Run the Setup.yml file against the host to configure the networking with Netplan
Run the docker.yml file with the command below and the proper target name from inventory

#RUN
ansible-playbook -i hosts/inventory.yml k3ssetup.yml -Kk --extra-vars "target=prox-aether01"
