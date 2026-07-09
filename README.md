# RoboShop Roles Ansible

Ansible playbook repository for deploying RoboShop components with reusable
roles.

## Requirements

- Ansible 2.15 or newer
- Target hosts reachable over SSH
- Inventory groups matching the component names used by the playbook

## Role Structure

This repository keeps component roles under the `roles/` directory:

- `frontend`
- `catalogue`
- `cart`
- `user`
- `shipping`
- `payment`
- `mongodb`
- `mysql`
- `redis`
- `rabbitmq`
- `common`

## Usage

Run the main playbook by passing the component name:

```bash
ansible-playbook main.yaml -e component=frontend
```

Replace `frontend` with another component name when deploying a different
service.

## Galaxy Import

The root `meta/main.yml` file provides the metadata required for Ansible Galaxy
legacy role import testing.
