#  Stage 01 – Azure Infrastructure Setup

##  Objective

Deploy a publicly accessible Linux VM in Microsoft Azure for honeypot research.

---

##  Virtual Machine Creation

- Debian 12 (Bookworm) selected
- x64 Gen2 architecture
- Trusted Launch enabled
- Availability Zone configured

![01](images/img01.png)
---

##  Azure Policy Issue

During deployment, VM creation failed due to:

![01](images/img02.png)

Policy: Allowed resource deployment regions

Resolution:
- Navigated to Azure Policy → Assignments
- Verified allowed regions
- Selected approved region
- Deployment succeeded

![01](images/img03.png)

![01](images/img04.png)
---

##  Network Configuration

- Virtual Network created
- Public IP assigned
- Network Security Group (NSG) created
- Inbound rule added (0–65535 open)

Ports intentionally exposed for honeypot research

![01](images/img05.png)
---

## SSH Configuration

- SSH key pair generated
- VM credentials reset
- Connected using:

![01](images/img06.png)

```
ssh -i HoneyPot_Key.pem HoneyPot@<Public-IP>
```

![01](images/img07.png)


```
ssh -i sudo apt update &&  sudo apt upgrade -y
```

![01](images/img08.png)