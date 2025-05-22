# Multi-VM Java Web Application Deployment with Vagrant

This project demonstrates the setup of a multi-tier Java web application using Vagrant-managed virtual machines. It supports both **manual** and **automated provisioning** using shell scripts for infrastructure setup.

---

## 📦 Project Overview

This environment consists of **five virtual machines**:

| VM Name | IP Address     | Role        | OS                | Provisioning |
|---------|----------------|-------------|-------------------|--------------|
| web01   | 192.168.56.11  | Web Server  | Ubuntu Jammy (22) | Manual / Automated (nginx.sh) |
| app01   | 192.168.56.12  | App Server  | CentOS Stream 9   | Manual / Automated (tomcat.sh) |
| rmq01   | 192.168.56.13 / .16 | RabbitMQ   | CentOS Stream 9   | Manual / Automated (rabbitmq.sh) |
| mc01    | 192.168.56.14  | Memcached   | CentOS Stream 9   | Manual / Automated (memcache.sh) |
| db01    | 192.168.56.15  | Database    | CentOS Stream 9   | Manual / Automated (mysql.sh) |

---

## 🔧 Manual Provisioning

This setup creates the VMs without running any provisioning scripts. You are expected to install and configure each service manually inside the respective VMs.

### ▶️ Launch Manual VMs

```bash
cd vagrant/Manual_provisioning
vagrant up