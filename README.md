Ansible Managed Games - by Tyler Bennet
=============



Ansible Tower / Ansible

# Prep ansible from a windows PC, Install WSL for Ubuntu
# Add an SSH key for the WSL instance
# Copy the SSH key to the host to deploy ansible against
# Configure hosts/inventory.yml to use the proper yaml syntax
# Run the Setup.yml file against the host to configure the networking with Netplan
# Run the docker.yml file with the command below and the proper target name from inventory

#RUN
ansible-playbook -i hosts/inventory.yml docker.yml -Kk --extra-vars "target=prox-aether01"

# On the host run the start.sh as sudo | root
## i.e. $sudo ./sync.sh
## This will run a docker-compose in a detached state so you can still use the VM without breaking the docker run.
## '$sudo docker ps'  will give you the docker container name.
## '$sudo docker logs container-name' - use the container name from the previous line to see the container logs.


## Copy new plugins to the games/plugins directory. Run the docker.yml file command above to re-deploy any new files.