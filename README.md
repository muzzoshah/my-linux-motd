# My Linux MOTD (System Dashboard) 🐧

A fast, compact, and beautiful System Dashboard for Ubuntu. This script replaces your default login message (MOTD) with a comprehensive, color-coded dashboard that displays real-time server metrics directly upon SSH login. It also auto-generates your custom name in ASCII art!

<img width="801" height="853" alt="image" src="https://github.com/user-attachments/assets/b93319a7-69a5-4624-970e-70503734de07" />

*(Note: Upload your screenshot image to the repo and update this link)*

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
