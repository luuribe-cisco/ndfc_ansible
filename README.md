# NDFC VRF Student Lab

This exercise is run from the preconfigured Ubuntu WSL 1 environment. The
instructor provides the lab controller credentials separately.

Open Ubuntu and run:

```bash
cd ~/ansible_task
ansible-playbook --syntax-check -i inventory/hosts.yml playbooks/replicate_vrfs.yml
```

Review and correct the lab files before running the playbook against NDFC.
Once the errors are fixed, execution creates missing non-default VRFs on the
Multisite parent. It sends changes to the controller; use the instructor's
lab environment only.

```bash
ansible-playbook -i inventory/hosts.yml playbooks/replicate_vrfs.yml
```

The instructor will provide or update the current lab username and password
in `inventory/group_vars/ndfc_host/credentials.yml`.
