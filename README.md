# Nipa-project
## 1. Verify Node Connectivity
```bash
ansible all -m ping -i inventory/hosts.ini
```
## 2. สิ่งที่ต้องติดตั้งในทุก node
```bash
ansible-playbook -i inventory/hosts.ini playbooks/common.yml
```

## 3. สิ่งที่ต้องติดตั้งในworker node -> mount disk
```bash
ansible-playbook -i inventory/hosts.ini playbooks/longhorn.yml 
```
## 4. deploy k0s on control-plane and worker nodes
```bash
ansible-playbook -i inventory/hosts.ini playbooks/k0s.yml
```
Once it finishes, from front-runner you can test:
```bash
kubectl get nodes
```
