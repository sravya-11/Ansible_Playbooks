1. Project Title
# Ansible Playbooks for System Monitoring

2. Description
This repository contains Ansible playbooks for automating system monitoring and maintenance tasks on Windows servers. 
The playbooks help in checking CPU utilization, disk usage, and performing cleanup operations when thresholds are exceeded.

3. Features

CPU Utilization Check – Monitors CPU usage on Windows hosts.
Disk Usage Check & Cleanup – Deletes old files if disk usage exceeds a defined threshold.
Email Notifications – Sends alerts about disk status after cleanup.

4. Playbooks Included

cpu_utilization.yml – Checks CPU usage.
disk_cleanup.yml – Monitors disk usage and cleans old logs if needed.

5. Requirements

Ansible installed on control node.
Windows hosts configured for Ansible (WinRM enabled).
SMTP server details for email notifications.
