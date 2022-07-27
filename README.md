Ansible Managed K8s - by Tyler Bennet
=============



Ansible Tower / Ansible

K8s
## Running the K8s main.yml will deploy the full project to the K8s hosts.

#RUN
ansible-playbook -i hosts/inventory.yml k8s/main.yml -Kk --extra-vars "target=all"




#RUN
ansible-playbook -i hosts/inventory.yml k3ssetup.yml -Kk --extra-vars "target=prox-aether01"


#ansible-galaxy requirements
ansible-galaxy collection install community.general
pip3 install openshift
pip install apache-airflow[kubernetes]
pip install kubernetes
