fail2ban-shellshock
===================

Additional filters to reduce impact of shellshock scanners

Added the following lines to /etc/fail2ban/jail.local and restart fail2ban.

[apache-shellshock]
enabled  = true
bantime  = 7200
port     = http,https
filter   = apache-shellshock
logpath  = /var/log/apache*/*error.log
maxretry = 2
