# Nipa-project
# ansible all -m ping -i inventory/hosts.ini

# สิ่งที่ต้องติดตั้งในทุก node
# ansible-playbook -i inventory/hosts.ini playbooks/common.yml

# สิ่งที่ต้องติดตั้งในworker node -> mount disk
# ansible-playbook -i inventory/hosts.ini playbooks/longhorn.yml 

# deploy k0s on control-plane and worker nodes
# ansible-playbook -i inventory/hosts.ini playbooks/k0s.yml
Once it finishes, from front-runner you can test:

kubectl get nodes