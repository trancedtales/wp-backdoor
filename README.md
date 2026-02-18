# ⚠️ WordPress Corruption Simulation Script (Educational Use Only)

This PHP script demonstrates how a WordPress site can be deliberately rendered inoperable by modifying the database and filesystem. It is meant **solely for educational and security awareness purposes**, and should **never be executed on a live or production environment**.

---

## 🧠 Purpose

The script is designed to:
- Show how attackers or misconfigurations can break a WordPress installation.
- Simulate a worst-case scenario for training or security hardening exercises.
- Educate developers and administrators on the importance of backups and secure development practices.

---

## 🚨 What This Script Does

> Running this script will break your WordPress site.

- 🔐 Extracts DB credentials and active theme name from your WordPress setup.
- 🧨 Replaces the `siteurl` and `home` values in the database with a corrupted URL (`http://invalid-url.com`).
- 🧹 Deletes all user accounts by truncating the `wp_users` table.
- 📴 Modifies the active theme’s `functions.php` by appending a `die()` statement.
- 🗃️ Renames the `wp-config.php` file, making the site non-functional.

---

## ⚠️ Disclaimer

> **This script is highly destructive. Use at your own risk.**

- **DO NOT RUN** on any live or production WordPress installation.
- This script is intended for local environments, testing, or sandboxed VMs only.
- The authors/contributors take **no responsibility** for any damage caused by misuse of this code.

---

## 🛠️ Requirements

- PHP 7.4 or higher
- A working WordPress installation (local/dev environment)
- Web server (Apache/Nginx) with `wp-load.php` accessible
- Proper file and directory permissions

---

## 🧪 Setup & Execution

1. Clone or download this repository.
2. Place the script in the root of your WordPress directory.
3. Ensure the file has execution permissions (`chmod 755`).
4. Access the script via the browser or run it from the CLI:
   - Browser: `http://localhost/your-site/simulate-corruption.php`
   - CLI: `php simulate-corruption.php`
5. Observe the changes and recover manually from backups if needed.

---

## 🧯 Recovery

If you have mistakenly run this:
- Restore your WordPress files from a recent backup.
- Restore your database from a backup.
- Rename `wp-config-backup.php` to `wp-config.php` to resume WordPress functionality.
- Recreate user accounts if needed.

---

## 📚 Educational Context

This script can be used to:
- Teach WordPress administrators about system vulnerabilities.
- Practice recovery from disaster scenarios.
- Demonstrate the importance of regular backups and monitoring.

---

## 🧑‍💻 Author

**Aditya Kumar**  
Web Developer | WordPress & React Enthusiast  
[LinkedIn](https://www.linkedin.com/in/trancedtales/) 
---

## 📄 License

This project is licensed under the MIT License.  
See `LICENSE` file for more details.

