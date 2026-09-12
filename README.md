# My Linux MOTD (System Dashboard) 🐧

A fast, compact, and beautiful System Dashboard for Ubuntu. This script replaces your default login message (MOTD) with a comprehensive, color-coded dashboard that displays real-time server metrics directly upon SSH login. It also auto-generates your custom name in ASCII art!

<img width="801" height="853" alt="image" src="https://github.com/user-attachments/assets/b93319a7-69a5-4624-970e-70503734de07" />

## 🌟 Features

*   **Auto ASCII Art:** Automatically generates your custom name in large ASCII text using `figlet`.
*   **Fast Execution:** Uses `/proc` for CPU and Memory stats (lighter than `top`).
*   **System Info:** OS, Kernel, Uptime, Packages, and Last Login.
*   **Resources:** CPU, Cores, CPU Usage (with progress bar), Memory (with progress bar), Swap, Storage, Load, and Processes.
*   **Security & Network:** CSF Firewall status, Security Updates, Failed SSH attempts, IP Address (IPv4 & IPv6), and Gateway.
*   **Hosting & Services:** Checks active status for SSH, Nginx, Apache, MariaDB, MySQL, and Docker.
*   **Domain Auto-Discovery:** Automatically lists configured domains from Nginx and Apache virtual hosts.

## ⚙️ Prerequisites

This script is optimized for **Ubuntu** (tested on 24.04 LTS). It utilizes standard built-in Linux tools, but make sure you install the following:

*   `figlet` (Required for the auto-generated ASCII art name)
*   `csf` (Optional, for Firewall status display)

Install `figlet` by running:
```bash
sudo apt update && sudo apt install figlet -y

🚀 Installation Guide
Run these commands in your terminal as root or using sudo:

1. Download the script

```bash
sudo wget [https://raw.githubusercontent.com/YOUR_USERNAME/my-linux-motd/main/10-admin-dashboard](https://raw.githubusercontent.com/YOUR_USERNAME/my-linux-motd/main/10-admin-dashboard) -O /etc/update-motd.d/10-admin-dashboard
(⚠️ IMPORTANT: Replace YOUR_USERNAME with your actual GitHub username)

2. Make the script executable

```bash
sudo chmod +x /etc/update-motd.d/10-admin-dashboard

3. Disable default Ubuntu MOTD spam (Optional but recommended)
To keep your dashboard clean, you can disable default Ubuntu news and help messages:

Bash
sudo chmod -x /etc/update-motd.d/10-help-text
sudo chmod -x /etc/update-motd.d/50-motd-news

4. Test it out!
Relogin to your SSH session or run this to view it immediately:

Bash
run-parts /etc/update-motd.d/
🎨 Customization (Make it yours!)
You can easily change the name displayed on the dashboard (Header ASCII art and Footer).

Edit the script on your server:

Bash
sudo nano /etc/update-motd.d/10-admin-dashboard
Find the USER CONFIGURATION section at the very top of the file and change this line to your desired name:

Bash
CUSTOM_NAME="Your Name Here"
Save the file, and the script will automatically generate the new ASCII text on your next login!

📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
