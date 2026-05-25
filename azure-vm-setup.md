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
