This document will help with Installing a Cerbot, generating an SSL and changing your webpage to a HTTPS using Let's Encrypt.

# Make sure everything is up to date

```
sudo apt update
```

# Install the Cerbot

```
sudo apt install certbot python3-certbot-nginx -y
```

# Now check the status of Nginx status

```
sudo systemctl status nginx
```

output:

```
active (running
```
<img width="1055" height="286" alt="image" src="https://github.com/user-attachments/assets/911d80d9-af25-402b-9f65-9345768f391d" />

---
