# Runbook - Payment Gateway Deployment

## Purpose
This playbook deploys the core payment gateway configuration and restarts the payment service across all payment servers.

## Execution
ansible-playbook -i inventories/production playbooks/deploy_payment_gateway.yml

## Validation
Check service status:
ansible payment_servers -m shell -a "systemctl status payment-gateway"

## Logs
Logs are saved in logs/ansible.log
