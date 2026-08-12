# Ansible GCP

Ansible project for managing and configuring resources in Google Cloud Platform (GCP).

## 📁 Project Structure

```text
ansible-gcp/
├── ansible.cfg
├── inventory
└── README.md
```

### Files

- **`ansible.cfg`** – Ansible configuration file.
- **`inventory`** – Defines the managed hosts used by Ansible.
- **`README.md`** – Project documentation.

## 🛠️ Prerequisites

Make sure the following are installed and configured:

- Ansible
- Google Cloud SDK (`gcloud`)
- Access to the required GCP project
- SSH access to the target GCP instances

Check the installations:

```bash
ansible --version
gcloud --version
```

## 🔐 GCP Authentication

Authenticate with Google Cloud:

```bash
gcloud auth login
```

Set the required GCP project:

```bash
gcloud config set project <PROJECT_ID>
```

Verify the active project:

```bash
gcloud config get-value project
```

## ⚙️ Ansible Configuration

The `ansible.cfg` file contains the project-specific Ansible configuration.

The inventory file contains the hosts that Ansible will manage.

Check the inventory:

```bash
ansible-inventory --list
```

## 🧪 Test Ansible Connection

Test connectivity to all hosts:

```bash
ansible all -m ping
```

A successful response should look similar to:

```text
<host> | SUCCESS => {
    "changed": false,
    "ping": "pong"
}
```

## ▶️ Running Ansible

Run an Ansible playbook using:

```bash
ansible-playbook <playbook.yml>
```

Example:

```bash
ansible-playbook site.yml
```

## 🚀 Project Goal

This project is intended to automate server configuration and infrastructure management on GCP using Ansible.

Future improvements may include:

- Ansible Playbooks
- Roles
- Package installation
- Application deployment
- Service configuration
- User and SSH management
- Security hardening
- Automated server provisioning

## 👤 Author

**Pushpa Kumara**

---

> This project is currently under development.