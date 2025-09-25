# ansible-ecommerce-deploy

This repository contains **Ansible Playbooks** designed to **automate the deployment** of a basic e-commerce website infrastructure.

---

## Project Overview 💡

This project is structured around a three-tier setup using **three CentOS Virtual Machines (VMs)**, simulating a simple, yet robust, production environment:

1.  **Ansible Controller:** This VM hosts the Ansible installation and is where the playbooks are executed to manage the other servers.
2.  **MariaDB Database Server:** This VM is designated to host the **MariaDB** database, which stores the e-commerce website's data.
3.  **Apache (HTTPD) Web Server:** This VM runs the **Apache HTTP Server** (or `httpd` on CentOS/RHEL systems) and hosts the actual e-commerce application files.

---

## Origin and Inspiration ✨

This project is based on and inspired by a similar hands-on exercise found in an **Ansible course on KodeKloud**. It serves as a practical, working example of how to use Ansible to manage heterogeneous environments and implement infrastructure-as-code principles.

---

## Environment Setup ⚙️

You can easily replicate this multi-VM project environment—and customize it to your needs—by following the detailed instructions provided in the original setup repository from KodeKloud:

* **KodeKloud Ansible Basics Repository:** [https://github.com/kodekloudhub/learn-ansible-basics-beginners-course/](https://github.com/kodekloudhub/learn-ansible-basics-beginners-course/)

---

## Key Features 🔑

* **Idempotent Configuration:** Playbooks are designed to ensure consistent and repeatable results, making it safe to run them multiple times.
* **Complete Deployment:** Automates the full setup, including package installation, service configuration, and application deployment across all three VMs.
* **Clear Structure:** Repository is organized for easy understanding and modification of roles and tasks.