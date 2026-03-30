# oss-audit-24BCE10038
# Open Source Audit — Git
---

##  Student Details

| Field | Details |
|---|---|
| **Name** | Astitva Srivastava |
| **Roll Number** | 24BCE10038 |
| **Course** | Open Source Software (Linux Administration) — CSE0002 |
| **Project Title** | Open Source Audit — Git |

---
##  Chosen Software
 
**Git** — A free and open-source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. Originally created by **Linus Torvalds** in 2005, Git enables developers to track changes in source code, collaborate across teams, and maintain a full history of every modification made to a codebase.

---

##   Repository Structure

```
oss-audit-24BCE10038/
│
├── README.md                        # Project overview and instructions (this file)
│
├── script1_system_identity.sh          # Script 1: System Identity Report
├── script2_foss_package_inspector.sh   # Script 2: FOSS Package Inspector
├── script3_disk_permission_auditor.sh  # Script 3: Disk and Permission Auditor
├── script4_log_analyzer.sh             # Script 4: Log File Analyzer
└── script5_manifesto_generator.sh      # Script 5: Open Source Manifesto Generator


```

##  Shell Scripts — Description
 
###  Script 1: System Identity Report (`script1_system_identity.sh`)
Generates a detailed system identity report including hostname, OS version, kernel info, CPU, RAM, disk usage, current users, and network configuration. Useful for system documentation and audits.
 
**Key Commands Used:** `uname`, `hostname`, `lscpu`, `free`, `df`, `ip`, `who`
 
---
 
###  Script 2: FOSS Package Inspector (`script2_foss_package_inspector.sh`)
Scans the system for installed open-source packages and lists their names, versions, and licenses where available. Demonstrates how to query package managers (`apt`, `dpkg`) to audit FOSS software on a Linux system.
 
**Key Commands Used:** `dpkg -l`, `apt-cache show`, `grep`
 
---
 
###  Script 3: Disk and Permission Auditor (`script3_disk_permission_auditor.sh`)
Audits disk usage and file/directory permissions in a target path. Identifies world-writable files, SUID/SGID bits, and large files that may need attention. Useful for security hardening and sysadmin workflows.
 
**Key Commands Used:** `df`, `du`, `find`, `stat`, `ls -la`
 
---
 
###  Script 4: Log File Analyzer (`script4_log_analyzer.sh`)
Parses system log files (e.g., `/var/log/syslog` or `/var/log/auth.log`) and extracts key events such as errors, warnings, failed login attempts, and sudo usage. Outputs a formatted summary report.
 
**Key Commands Used:** `grep`, `awk`, `cut`, `sort`, `uniq`, `tail`, `wc`
 
---
 
###  Script 5: Open Source Manifesto Generator (`script5_manifesto_generator.sh`)
An interactive script that takes user input (name, favourite FOSS project, and beliefs about open source) and generates a personalised Open Source Manifesto as a formatted text file. Demonstrates string handling, user input, and file I/O in Bash.
 
**Key Commands Used:** `read`, `echo`, `cat`, `tee`, `date`
 
---
---


##  How to Run the Project

### Prerequisites
- A Linux system (Ubuntu 20.04+ recommended) or WSL on Windows
- Git installed (`sudo apt install git`)
- Bash shell (default on most Linux distributions)

### Step-by-Step Instructions

**1. Clone the repository:**
```bash
git clone https://github.com/dev-astitva/oss-audit-24BCE10038.git
```

**2. Navigate to the project directory:**
```bash
cd oss-audit-24BCE10038
```

**3. Give execution permission to all scripts:**
```bash
chmod +x scripts/*.sh
```

**4. Run a specific script:**
```bash
./scripts/script1_system_identity.sh
```

**5. Run all scripts sequentially (optional):**
```bash
for script in scripts/*.sh; do
    echo "===== Running: $script ====="
    bash "$script"
    echo ""
done
```

> **Note:** Some scripts (e.g., Script 3 and Script 4) may require `sudo` privileges to access system files or logs. Run with `sudo` if prompted.

```bash
sudo ./scripts/script3_disk_permission_auditor.sh
sudo ./scripts/script4_log_analyzer.sh
```

---






