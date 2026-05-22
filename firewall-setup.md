# Firewall setup

## Run the main firewall setup

```
sudo ufw allow OpenSSH
sudo ufw allow 'Nginx Full'
sudo ufw allow 51820/udp
sudo ufw enable
```

---

# Then check the status

```
sudo ufw status

```

<img width="527" height="212" alt="image" src="https://github.com/user-attachments/assets/cc7803b7-611b-4335-9d6d-cf7e0c44aa59" />
---
