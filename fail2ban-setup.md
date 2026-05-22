# Configuring Fail2Ban

## Update the Server

First, ensure all packages are up to date before installing Fail2Ban

```
sudo apt update
```

---

# Now Install Fail2Ban

Now, install Fail2Ban using apt

```
sudo apt install fail2ban -y
```

---

# Check Fail2Ban status

Verifying that Fail2Ban service is running properly

```
sudo systemctl status fail2ban
```

output:
```
active (running)
```

<img width="1079" height="227" alt="image" src="https://github.com/user-attachments/assets/f3cb834a-7f71-4c92-8608-ed4a890d3a54" />

---
# Create the configuration file

```
sudo nano /etc/fail2base/jail.local
```

If the file already exists and contains other random config data, remove it and recreate the file

```
sudo rm /etc/fail2ban/jail.local
sudo nano /etc/fail2ban/jail.local
```

---

## Configure Fail2Ban

Paste the following configuration into `jail.local`.

```ini
[DEFAULT]
bantime = 1h
findtime = 10m
maxretry = 5
backend = systemd

[sshd]
enabled = true
port = ssh
logpath = %(sshd_log)s
```

# Configuration Explanation

Setting | Purpose 
|---|---|
bantime | Bans IP addresses for 1 hour 
findtime | Monitors failed attempts within 10 minutes 
maxretry | Bans after 5 failed login attempts 
backend | Uses systemd logs 
sshd | Protects SSH service 

---

# Now restart Fail2ban

Apply the config changes

```
sudo systemctl restart fail2ban
```

---

# Make sure the protection is now active

Check Fail2Ban is active

```
sudo fail2ban-client status
```

Output: 

```
Jail list: sshd
```
<img width="585" height="74" alt="image" src="https://github.com/user-attachments/assets/94c40893-0a71-47fb-987b-6751e051c6dd" />

---

# Check SSH Jail2Ban status

```
sudo fail2ban-client status sshd
```
This command displays:
- currently banned IP addresses
- failed login attempts
- total banned IP count

<img width="677" height="186" alt="image" src="https://github.com/user-attachments/assets/f1d92fa5-6c9a-4d4f-b7dc-0e1cda7b20c4" />

---

# Security Benefits

Fail2ban improves security by:
- it Monitors failed SSH login attempts
- Will instantly ban suspicious IP addresses
- Will improve the overall quality/strength of the server
- Reduces brute-force attacks






#
