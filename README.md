# Programing Challenge Operations K8S

## APP Link
http://35.187.74.163:31680/

## Create Ansible Env
```shell
VENVDIR=.venv
python3 -m venv $VENVDIR
source $VENVDIR/bin/activate
pip install -U -r requirements.txt
```

## Project Structure
```
programing-challenge-operations-k8s/ansible/
│
├── inventory/               # Directory containing Ansible inventory files
│   └── hosts.yml            # YAML file defining hosts and groups for Ansible to target
│
├── roles/                   # Directory for Ansible roles, modularizing tasks
│   ├── vm/                  # Role for managing VM provisioning (GCE) and VPC firewall configurtion
│   ├── k8s/                 # Role for setting up and configuring the Kubernetes cluster with addons like Calico, Helm
│   ├── db/                  # Role for deploying and managing the PV driver, PV and database
│   └── app/                 # Role for deploying the application, interacting with the MySQL, exposing services through Ingress
│
├── requirements.txt         # Python requirements file for Ansible modules, GCP SDK, and Kubernetes operations
└── create_all.yml           # Main Ansible playbook for orchestrating VM provisioning, K8s setup, DB, and app deployment
```

## Cluster Status

### Cluster Info
![alt text](cluster_info.png)
### Node Info
![alt text](node_info.png)
### All Info
![alt text](all_info_1.png)
![alt text](all_info_2.png)