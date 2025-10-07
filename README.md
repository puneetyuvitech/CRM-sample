# 🧩 SuiteCRM Ansible Playbook (Nginx + MariaDB + PHP-FPM)

This Ansible playbook automates the installation and configuration of **SuiteCRM 8.x** on Ubuntu/Debian servers.  
It provisions all required dependencies — **Nginx**, **MariaDB**, **PHP-FPM**, and configures SuiteCRM with proper permissions, Nginx virtual host, and database setup.

---

## 🚀 Features

- Installs and configures:
  - Nginx
  - MariaDB Server
  - PHP-FPM with all required modules
  - Composer
- Automatically downloads and deploys SuiteCRM
- Creates and configures the SuiteCRM database and user
- Generates a working `config.php`
- Configures Nginx for SuiteCRM
- Secures file and directory permissions
- Runs SuiteCRM CLI installer for a ready-to-use setup

---

## ⚙️ Variables (`vars.yml`)

Below is the default variable configuration used by the playbook:

```yaml
vm_ip: ""
domain_name: "suitecrm.site"
suitecrm_url: "https://suitecrm.com/download/166/suite89/565428/suitecrm-8-9-0.zip"

mysql_root_password: "root"
db_name: "suitecrm_db"
db_user: "suitecrm_user"
db_password: "suitecrm_password"
db_host: "localhost"

admin_user: "admin"
admin_password: "admin"
```
---

## 🔧 Usage
1️⃣ Clone the repository
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>

2️⃣ Edit Variables

1. Open vars.yml and update:

2. Your domain name and vm IP

3. Database credentials

4. SuiteCRM admin credentials

5. SuiteCRM download URL (optional, defaults to 8.9.0)

3️⃣ Run the Playbook
ansible-playbook suitecrm_nginx.ym

At the end of the run, SuiteCRM will be accessible via your configured domain or server IP.

---

🌐 Accessing SuiteCRM

Once installation completes:

1. Open a web browser.

2. Navigate to:

http://your-server-ip/

or

http://suitecrm.site/


3. Log in using:

Username: admin

Password: admin (or whatever you set in vars.yml)

---

