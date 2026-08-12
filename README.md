# Ansible GCP

Ansible project for automating server configuration and application deployment on Google Cloud Platform (GCP).

## 📁 Project Structure

```text
ansible-gcp/
├── ansible.cfg
├── inventory
├── site.yml
├── index.html.j2
└── README.md
```

### Files

| File            | Description                                    |
| --------------- | ---------------------------------------------- |
| `ansible.cfg`   | Ansible project configuration                  |
| `inventory`     | Defines the target hosts managed by Ansible    |
| `site.yml`      | Main Ansible playbook                          |
| `index.html.j2` | Jinja2 template used to generate the HTML page |
| `README.md`     | Project documentation                          |

## 🛠️ Prerequisites

Make sure the following are installed and configured:

* Ansible
* Google Cloud SDK (`gcloud`)
* A GCP project
* SSH access to the target GCP instance

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

## ⚙️ Inventory

The `inventory` file defines the GCP server that Ansible manages.

Verify the inventory:

```bash
ansible-inventory --list
```

## 🧪 Test Connection

Before running the playbook, test the connection to the target server:

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

## ▶️ Run the Playbook

Run the main playbook with:

```bash
ansible-playbook site.yml
```

The playbook uses `index.html.j2` as a Jinja2 template to generate the HTML content on the target server.

## 🌐 Jinja2 Template

`index.html.j2` is a Jinja2 template used by Ansible to dynamically generate the application's HTML page.

This demonstrates how Ansible can combine:

* Configuration management
* Jinja2 templating
* Automated file deployment

## 🚀 Project Goal

The goal of this project is to learn and demonstrate infrastructure automation using **Ansible + Google Cloud Platform**.

The project can be extended with:

* Ansible Roles
* Package management
* Web server configuration
* Application deployment
* User and SSH management
* Service management
* Security hardening
* Automated provisioning

## 👤 Author

**Pushpa Kumara**

---

> This project is currently under development.
