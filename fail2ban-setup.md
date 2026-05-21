# fail2ban-setup.md



# Make sure software is up-to-date preparing for fail2ban install
sudo apt update



# Now we are going to install fail2ban
sudo apt install fail2ban -y



# Now check the status for fail2ban to make sure it is running
sudo systemctl status fail2ban (Will see active (running))

sudo apt install fail2ban -y

# Now we are going to create the config file
sudo nano /etc/fail2ban/jail.local - Make sure the file is clear if not rm it and re-create

Now paste 

[DEFAULT]
bantime = 1h
findtime = 10m
maxretry = 5

[sshd]
enabled = true
port = ssh
logpath = %(sshd_log)s
backend = systemd


# Restart fail2ban
sudo systemctl restart fail2ban

# Verify thhe protection is in place

sudo fail2ban-client status
You should see Jail list: sshd

# Check the status
sudo fail2ban-client status sshd



<img width="1079" height="227" alt="image" src="https://github.com/user-attachments/assets/f3cb834a-7f71-4c92-8608-ed4a890d3a54" />
