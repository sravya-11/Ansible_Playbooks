# Dynamic System Health and CIS Compliance Check Playbook

## Overview
This Ansible playbook dynamically adds a target host and performs:
- **System Health Checks**
  - Memory utilization
  - CPU utilization
  - Disk utilization
- **CIS Compliance Checks**
  - `PASS_MAX_DAYS` in `/etc/login.defs`
  - Disable SSH root login in `/etc/ssh/sshd_config`

It provides clear status messages and restarts SSH if required.

---

## Features
- Dynamic host addition using `add_host`.
- Threshold-based health checks with customizable variables.
- CIS hardening for password policy and SSH configuration.

---

## Variables
You can adjust thresholds in the `vars` section:
```yaml
memory_threshold: 80    # Memory usage alert threshold (%)
cpu_threshold: 85       # CPU usage alert threshold (%)
disk_threshold: 80      # Disk usage alert threshold (%)
pass_max_days_expected: 90  # Password max days policy
```

---

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo>.git
   cd <your-repo>
   ```
2. Run the playbook:
   ```bash
   ansible-playbook health_cis_check.yml -e "target_host=<hostname>"
   ```
   Replace `<hostname>` with the target machine name or IP.

---

## Output
- Displays memory, CPU, and disk utilization status.
- Shows compliance messages for CIS checks.
- Restarts SSH service if configuration changes.

---

## Notes
- Requires SSH access to the target host.
- Tested on Linux systems.

