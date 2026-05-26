# Setup of Monitoring Script

Create the monitoring scrit in your SSH
```
nano server-monitor.sh
```

Then create your script

```
#!/bin/bash

echo "SERVER MONITOR"
echo "Date: $(date)"

echo "Uptime: $(uptime -p)"

echo ""
echo "Memory:"

free -h | grep Mem

echo ""
echo "Disk:"

df -h | grep '^/'

echo ""
echo "Users:"
who

echo ""
echo "Failed SSH Attempts:"
grep "Failed password" /var/log/auth.log | tail

```

---


## Give permission
```
chmod +x server-monitor.sh
```
---

## Run the script
```
./server-monitor.sh
```
<img width="760" height="319" alt="image" src="https://github.com/user-attachments/assets/129db60c-24c1-4010-b529-afcc7838320e" />

---
