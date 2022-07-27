Ansible Managed K8s - by Tyler Bennet
=============



Ansible Tower / Ansible

K8s
## Running the K8s main.yml will deploy the full project to the K8s hosts.
## Some setup is required for the primary controllers. I'll add these later for high availability setup.
## Run the Monitoring.yml to kick off installing helm and any dependencies.

#RUN
ansible-playbook -i hosts/inventory.yml k8s/main.yml -Kk --extra-vars "target=all"


#### https://www.linuxtechi.com/install-kubernetes-on-ubuntu-22-04/ doc source

#RUN
ansible-playbook -i hosts/inventory.yml k3ssetup.yml -Kk --extra-vars "target=prox-aether01"


#ansible-galaxy requirements
ansible-galaxy collection install community.general
pip3 install openshift
pip install apache-airflow[kubernetes]
pip install kubernetes
