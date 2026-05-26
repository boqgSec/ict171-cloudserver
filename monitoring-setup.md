# Setup of Monitoring Script

Create the monitoring scrit in your SSH
```
nano server-monitor.sh
```

Then create your script

```
#!bin/bash
echo "         Server Monitor        "

echo ""
echo "date and time:"
date

echo ""
echo "server uptime:"
uptime

echo ""
echo "memory usage:"
free -h

echo ""
echo "disk usage:"
df -h

echo ""
echo "current logged in users:"
who

echo""
echo"failed ssh login attempts:"
grep "failed password" /var/log/auth.log | tail
```

---
