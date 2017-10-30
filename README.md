# mbkp
Mikrotik backup script

This script can be used to centralize the backup configurations of Mikrotics devices.
Each device has its own configuration file in which it can override the standard options.


# Scheduling
Here is crontab example:
```
# VARS:
MCFG="/etc/mikrotik_backup"
MBKP="/usr/local/bin/mbkp"
MLOG="/var/log/mikrotik_backup/log"
# TASKS:
00 03 * * *     $MBKP $MCFG"/somehost.cfg" >>$MLOG 2>>$MLOG             # Comment
```

# Recommended paths:

- /etc/mikrotik_backup		directory where configuration files located

- /usr/local/bin/mbkp		executable bash script with default variables

- /var/log/mikrotik_backup/log	logfile to trace script execution results
