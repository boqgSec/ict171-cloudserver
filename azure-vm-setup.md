# Azure VM Setup

This guide will help set up and deploy Microsoft Azure, using Ubuntu 24.04 LTS

This virtual machine hosts an Nginx web server, a domain, an SSL certificate, and a firewall.

## Create the Virtual machine

```Create a resource > find Virtual Machine```

## Configuration of the Virtual Machine

| Setting              | Value                   |
| -------------------- | ----------------------- |
| Resource Group       | ict171-cloud            |
| Virtual Machine Name | ict171-cloud            |
| Region               | Australia East          |
| Image                | Ubuntu Server 24.04 LTS |
| Size                 | Standard B1s            |
| Authentication Type  | SSH Public Key          |
| Username             | azureuser               |

## Download SSH Key Pair

```ict171-cloud_key.pem```

## Configure Inbound Rules

| Port | Protocol | Purpose           |
| ---- | -------- | ----------------- |
| 22   | TCP      | SSH Remote Access |
| 80   | TCP      | HTTP Web Traffic  |
| 443  | TCP      | HTTPS SSL Traffic |

<img width="454" height="131" alt="image" src="https://github.com/user-attachments/assets/7e47048f-8159-4f32-b6cf-79fb6470f7a2" />


## Connect to your server using SSH

```ssh -i <private-key-file-path> azureuser@52.184.82.227```

input ur .pem file location in the private key file path

<img width="941" height="452" alt="image" src="https://github.com/user-attachments/assets/767b2e3b-26f9-44d8-bf6b-722e7d1ee631" />

---

## Update the server

```
sudo apt update
sudo apt update -y
```

---

## Install Nginx web server
```
sudo apt install nginx -y
```

---

## Verify if the Nginx runs
```
sudo systemctl status nginx
```
You'll see the ```active: running```

<img width="1022" height="274" alt="image" src="https://github.com/user-attachments/assets/faa3ccbb-38b1-4adb-8c50-c53b85981fb5" />
---

## Verify the website works

Connect to your Public IP
```
http://52.184.82.227
```
<img width="1058" height="431" alt="image" src="https://github.com/user-attachments/assets/8aa767ec-5529-4a7c-a3f2-463a7d78703d" />

---

# Benefits of Azure VM 
- Cost Efficiency 
- Secure SSH Access
- Remote server 
- Improved security
- Reduced latency


# Used Software
- Microsoft Azure
- Ubuntu Server 24.04 LTS
- OpenSSH
- Nginx Web Server

