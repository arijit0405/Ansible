# 📘 Introduction to Ansible

## ✅ What is Ansible?

Ansible is an open-source IT automation tool developed by Red Hat. It allows you to automate:

* **Provisioning** (spinning up servers)
* **Configuration Management** (installing software, editing config files)
* **Application Deployment**
* **Orchestration** of services across infrastructure

📌 It uses **YAML-based playbooks** and works **agentless** over SSH, making it lightweight and simple.

---

## 🧠 Why Ansible?

| Feature               | Why It Matters                                               |
| --------------------- | ------------------------------------------------------------ |
| ✅ Agentless           | No need to install any agent or software on the target nodes |
| ✅ Easy to Learn       | Uses human-readable YAML syntax                              |
| ✅ Idempotent          | Running a playbook multiple times has the same effect        |
| ✅ Cross-platform      | Works on Linux, macOS, and Windows                           |
| ✅ Extensible          | Use community roles from Ansible Galaxy or write your own    |
| ✅ Great for CM + Apps | Configure servers + deploy apps all in one tool              |
| ✅ Strong Community    | Widely adopted and backed by Red Hat                         |

---

## 🏗️ How Does Ansible Work?

Ansible Control Node runs the commands and connects to the **Managed Nodes** (servers) over **SSH**.

**Basic flow:**

1. You write a **playbook** (set of instructions in YAML)
2. Ansible uses SSH to connect to remote servers
3. Executes tasks like installing packages, starting services, editing config files

---

## 🤩 Core Ansible Concepts

| Term      | Meaning                                                            |
| --------- | ------------------------------------------------------------------ |
| Inventory | List of managed hosts or groups                                    |
| Module    | A single unit of work (e.g., yum, copy, service)                   |
| Task      | A call to a module in a playbook                                   |
| Playbook  | YAML file describing the desired state of your infrastructure      |
| Role      | A reusable collection of tasks, handlers, templates, and variables |
| Facts     | System information gathered from the target hosts                  |

---

## 💡 Common Use Cases

* Install and configure web servers, databases, firewalls
* Deploy multi-tier applications
* Patch operating systems
* Manage user accounts and SSH keys
* Enforce compliance policies

---

## 🎯 Ansible vs Other Tools

| Tool      | Agent Needed? | Complexity | Use Case                     |
| --------- | ------------- | ---------- | ---------------------------- |
| Ansible   | ❌ No          | ⭐ Easy     | CM + Orchestration           |
| Chef      | ✅ Yes         | ❗ Complex  | CM with Ruby DSL             |
| Puppet    | ✅ Yes         | ❗ Complex  | CM with declarative language |
| Terraform | ❌ No          | ⭐ Medium   | Infra provisioning only      |

---

## 🔧 Real-World Example (Simple Playbook)

```yaml
- name: Install Apache Web Server
  hosts: webservers
  become: yes
  tasks:
    - name: Install Apache
      apt:
        name: apache2
        state: present
```

---

## 🚀 Summary

**Ansible = Simplicity + Power**

* Helps automate almost every DevOps operation without agents
* Works well with **Terraform**, **Docker**, **Kubernetes**, **AWS**, etc.
* Still one of the most popular automation tools in **2025**
