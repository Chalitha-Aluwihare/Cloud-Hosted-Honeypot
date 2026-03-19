# Stage 02 – Honeypot Platform Installation (T-Pot)

##  Objective

Install and configure the T-Pot multi-honeypot platform on the deployed Azure Debian 12 virtual machine.

---

#  Environment Details

- OS: Debian 12 (Bookworm)
- Cloud: Microsoft Azure
- Public IP: <Your-Public-IP>
- Access Method: SSH Key Authentication

--

# 1️System Preparation

Before installing T-Pot, update the system.

```bash
sudo apt update && sudo apt upgrade -y